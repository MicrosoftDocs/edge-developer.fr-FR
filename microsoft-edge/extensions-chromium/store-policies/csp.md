---
description: Extensions de la stratégie de sécurité du contenu pour les extensions Edge (chrome).
title: Stratégie de sécurité du contenu (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: 52d6d0afb38401250183788726013d521a269f06
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565406"
---
# Stratégie de sécurité du contenu \ (CSP \)  

Afin d’atténuer un grand nombre d’erreurs de script intersites potentiels, le système d’extension Microsoft Edge a incorporé le concept général de la [stratégie de sécurité du contenu \ (CSP)][W3CContentSecurityPolicy].  Ce type d’introduction présente certaines stratégies relativement strictes qui rendent les extensions plus sûres par défaut et vous permet de créer et d’appliquer des règles régissant les types de contenu qui peuvent être chargés et exécutés par vos extensions et applications.  

En règle générale, le CSP fonctionne comme un mécanisme bloc/allowlisting pour les ressources chargées ou exécutées par vos extensions.  La définition d’une politique raisonnable pour votre extension vous permet de réfléchir soigneusement aux ressources nécessaires pour votre extension et de demander au navigateur de s’assurer que les seules ressources auxquelles votre extension a accès.  Ces stratégies garantissent la sécurité au-delà des autorisations de l’hôte de vos demandes d’extension. Il s’agit d’une couche de protection supplémentaire et pas d’un remplacement.  

Sur le Web, une telle stratégie est définie via un en-tête ou un `meta` élément http.  Aucun mécanisme approprié n’est nécessaire dans le système d’extension Microsoft Edge.  Au lieu de cela, une stratégie d’extension est définie via le `manifest.json` fichier pour l’extension comme suit:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Pour plus d’informations sur la syntaxe du fournisseur de services cryptographiques, voir la spécification de la [stratégie de sécurité du contenu][W3CContentSecurityPolicy] et l’article [«Présentation de la stratégie de sécurité du contenu»][HTML5RocksIntroductionContentSecurityPolicy] sur HTML5Rocks.  

## Restrictions de stratégie par défaut  

Les packages qui ne définissent aucune `manifest_version` stratégie de sécurité du contenu par défaut ne sont pas définis.  Ceux qui sélectionnent `manifest_version` 2 disposent d’une stratégie de sécurité du contenu par défaut:  

```javascript
script-src 'self'; object-src 'self'
```  

Cette stratégie ajoute de la sécurité en limitant les extensions et applications de trois manières:  

**Les fonctions eval et apparentées sont désactivées**  

Le code comme suit ne fonctionne pas:  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

L’évaluation de chaînes de JavaScript comme celle-ci est un vecteur d’attaque XSS courante.  À la place, vous devez écrire du code comme suit:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**JavaScript intraligne ne s’exécute pas**  

JavaScript Inline ne s’exécute pas.  Cette restriction interdit aux blocs intralignes `<script>` et aux gestionnaires d’événements Inline, tels que `<button onclick="...">` .

La première restriction réapparaît une énorme classe d’attaques de script entre sites en vous rendant impossible d’exécuter accidentellement le script fourni par un tiers malveillant.  Néanmoins, il est nécessaire d’écrire votre code avec une séparation nette entre le contenu et le comportement \ (c’est le cas, vous devez tout de même bien.  Par exemple, il est possible que ce soit plus clair.  Il est possible que vous deviez écrire une action de navigateur contextuelle sous la forme d’un seul `pop-up.html` contenant:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

Trois éléments doivent changer pour que ce processus fonctionne comme prévu.  

*   La `clickHandler` définition doit être déplacée vers un fichier JavaScript externe ( `popup.js` il peut s’agir d’un bon destinataire).  
*   Les définitions des gestionnaires d’événements en ligne doivent être réécrites en termes de `addEventListener` et en extraction `popup.js` .  
    Si vous démarrez actuellement votre programme en utilisant du code tel que `<body onload="main();">` , envisagez de le remplacer par un raccordement à l' `DOMContentLoaded` événement du document ou à l' `load` événement de la fenêtre, en fonction de vos besoins.  Utilisez l’ancien, car il est généralement déclenché plus rapidement.  

*   L' `setTimeout` appel doit être réécrit pour éviter de convertir la chaîne `"awesome(); totallyAwesome()"` en code JavaScript en exécution.  
    Ces modifications pourraient ressembler à ce qui suit:  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**Seules les ressources d’objet et de script local sont chargées.**  

Les ressources de script et d’objet peuvent uniquement être chargées à partir du package d’extension, et non à partir du Web.  Cela permet de s’assurer que votre extension exécute uniquement le code que vous avez approuvé en particulier, ce qui évite à un attaquant du réseau actif de rediriger intentionnellement votre demande de ressource.  

Au lieu d’écrire du code qui dépend de jQuery \ (ou d’une autre bibliothèque), il est conseillé d’inclure la version spécifique de jQuery dans votre package d’extension.  C’est-à-dire, au lieu de:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

Téléchargez le fichier, incluez-le dans votre package, puis écrivez:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## Relaxer la stratégie par défaut  

**Script inline**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Les scripts inline peuvent être autorisés en spécifiant le hachage encodé en base64 du code source de la stratégie.  Ce hachage doit être préfixé à l’aide de l’algorithme de hachage utilisé \ (SHA256, SHA384 ou SHA512 \).  Pour obtenir un exemple, voir [utilisation de hachage pour \ <script \ > éléments][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] .  

**Script distant**  

Si vous avez besoin de ressources d’objets ou JavaScript externes, vous devrez peut-être détendre la stratégie vers une extension limitée d’allowlistings sécurisées à partir desquelles les scripts doivent être acceptés.  Vérifiez que les ressources d’exécution dont le chargement est limité aux ressources dont vous vous attendez et qu’elles ne sont pas remplacées par une attaque réseau active.  En tant qu' [attaques par homme-au-milieu, il][WikiManMiddleAttacks] n’est pas possible d’accepter et de détecter les origines sur http.  

Pour l’instant, les développeurs sont en mesure de verteer avec les schémas suivants: `blob` ,, `filesystem` `https` et `extension` .  La partie hôte de l’origine doit être explicitement spécifiée pour les `https` `extension` schémas et.  Les caractères génériques génériques tels que https: `https://*` et ne `https://*.com` sont pas autorisés; les caractères génériques de sous-domaine tels qu' `https://*.example.com` ils sont autorisés.  Les domaines figurant dans la [liste de suffixes publics][PublicSuffixList] sont également considérés comme des domaines de niveau supérieur génériques.  Pour charger une ressource à partir de ces domaines, le sous-domaine doit être répertorié explicitement.  Par exemple, `https://*.cloudfront.net` n’est pas valide, `https://XXXX.cloudfront.net` mais `https://*.XXXX.cloudfront.net` peut être allowlisted.  

Pour faciliter la mise au point, les ressources chargées sur HTTP à partir de serveurs de votre ordinateur local peuvent être allowlistedes.  Vous pouvez verte des sources d’objet et de script sur n’importe quel port de l’une ou l’autre `http://127.0.0.1` `http://localhost` .  

> [!NOTE]
> La restriction par rapport aux ressources chargées sur HTTP s’applique uniquement aux ressources qui sont exécutées directement.  Vous êtes toujours libre (par exemple, pour créer des connexions de type XMLHTTPRequest à l’origine qui vous plaît); la stratégie par défaut n’est pas limitée `connect-src` ou n’importe quelle autre directive CSP de quelque manière que ce soit.  

Une définition de stratégie souple qui permet le chargement des ressources de script à partir de example.com sur HTTPs peut se présenter comme suit:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Both `script-src` et `object-src` définis par la stratégie.  Microsoft Edge n’accepte pas une stratégie qui ne limite pas chacune de ces valeurs à \ (au moins \) `self` .  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**JavaScript évalué**  

La stratégie par rapport aux `eval()` fonctions associées `setTimeout(String)` et `setInterval(String)` celles- `new Function(String)` ci peuvent être assouplies en les ajoutant `unsafe-eval` à votre stratégie:  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Toutefois, nous vous recommandons vivement de le faire.  Ces fonctions sont des vecteurs d’attaque XSS.  

## Renforcement de la stratégie par défaut  

Vous pouvez, bien entendu, serrer cette politique dans la mesure où votre extension permet d’augmenter la sécurité aux dépens de la commodité.  Pour indiquer que votre extension peut uniquement charger des ressources de tout type \ (images, etc.) à partir du package d’extension associé, par exemple, la stratégie de `default-src 'self'` peut être appropriée.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## Scripts de contenu  

La stratégie en cours de discussion s’applique aux pages d’arrière-plan et aux pages d’événements de l’extension.  La façon dont les scripts s’appliquent aux scripts de contenu de l’extension est plus complexe.  

Les scripts de contenu ne sont généralement pas soumis au CSP de l’extension.  Dans la mesure où les scripts ne sont pas au format HTML, l’impact principal de ces derniers est qu’ils peuvent être utilisés `eval` même si le CSP de l’extension n’est pas spécifié `unsafe-eval` , bien que cela soit déconseillé.  Par ailleurs, le CSP de la page ne s’applique pas aux scripts de contenu.  Plus difficile sont les `<script>` balises que les scripts de contenu créent et placent dans le DOM de la page sur laquelle ils s’exécutent.  Celles-ci sont référencées en tant que scripts injectés DOM.  

Les scripts d’injection DOM qui s’exécutent immédiatement après l’insertion dans la page s’exécutent comme prévu.  Imaginez un script de contenu avec le code suivant comme exemple simple:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Ce script de contenu entraîne une `alert` interdépendance immédiate `document.write()` .  Notez que cette opération s’exécute quelle que soit la stratégie spécifiée par une page.
Toutefois, le comportement devient plus compliqué tant au sein de ce DOM injecté par le script injecté que dans le cas d’une injection.  Imaginez que votre extension s’exécute sur une page qui fournit un CSP associé spécifiant `script-src 'self'` .  Imaginez maintenant que le script de contenu exécute le code suivant:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Si un utilisateur clique sur ce bouton, le `onclick` script ne s’exécute pas.  En effet, le script ne s’est pas exécuté immédiatement et le code n’est pas interprété tant que l’événement Click n’a pas été considéré comme faisant partie du script de contenu, de sorte que le fournisseur de services de cryptographie de la page \ (sans l’extension \) limite ce comportement.  Et dans la mesure où ce fournisseur de services de cryptographie n’est pas spécifié `unsafe-inline` , le gestionnaire d’événements Inline est bloqué.  
Pour implémenter le comportement souhaité dans le cas présent, il est possible d’ajouter le `onclick` Gestionnaire en tant que fonction du script de contenu comme suit:  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Un autre problème semblable se produit si le script de contenu exécute ce qui suit:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

Dans ce cas, le script s’exécute et l’alerte s’affiche.  Toutefois, prenez ce cas:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Pendant l’exécution du script initial, l’appel à `eval` est bloqué.  Autrement dit, lorsque le runtime de script initial est autorisé, le comportement au sein du script est réglementé par le fournisseur de services de cryptographie de la page.  
Par conséquent, en fonction de la manière dont vous écrivez les scripts injectés DOM dans votre extension, les modifications apportées au CSP de la page peuvent affecter le comportement de votre extension.  Dans la mesure où les scripts de contenu ne sont pas affectés par le fournisseur de services cryptographiques de la page, c’est une bonne raison de placer le plus de comportement possible de votre extension dans le script de contenu plutôt que dans les scripts injectés DOM.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Présentation de la politique de sécurité du contenu-Rocks HTML5"  
[PublicSuffixList]: https://publicsuffix.org/list "AFFICHER LA LISTE DES SUFFIXES PUBLICS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Utilisation du hachage pour \ <script \ > éléments-niveau de la stratégie de sécurité du contenu 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Niveau de stratégie de sécurité du contenu 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Attaque de l’homme-au-milieu-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developer.chrome.com/extensions/contentSecurityPolicy).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
