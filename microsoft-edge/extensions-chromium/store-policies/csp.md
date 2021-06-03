---
description: Stratégie de sécurité de contenu pour les extensions Edge (Chromium).
title: Stratégie de sécurité du contenu (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: edge-chromium, développement d’extensions, extensions de navigateur, addons, centre de partenaires, développeur
ms.openlocfilehash: 8307482e780b4d631edffd976cca7ba724e2ad40
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397516"
---
# <a name="content-security-policy-csp"></a>Stratégie de sécurité du contenu \(CSP\)  

Afin d’atténuer une grande classe de problèmes potentiels de scripts entre sites, le système d’extension Microsoft Edge a incorporé le concept général de stratégie de sécurité du contenu [\(CSP\)][W3CContentSecurityPolicy].  Cela introduit des stratégies assez strictes qui sécurisationnt les extensions par défaut et vous offre la possibilité de créer et d’appliquer des règles régissant les types de contenu qui peuvent être chargés et exécutés par vos extensions et applications.  

En règle générale, le programme CSP fonctionne comme un mécanisme de blocage/mise en liste des listes d’utilisateurs pour les ressources chargées ou exécutés par vos extensions.  La définition d’une stratégie raisonnable pour votre extension vous permet d’examiner attentivement les ressources dont votre extension a besoin et de demander au navigateur de s’assurer qu’il s’agit des seules ressources à qui votre extension a accès.  Les stratégies assurent la sécurité au-delà des autorisations d’hôte que vos demandes d’extension . Il s’agit d’une couche de protection supplémentaire, et non d’un remplacement.  

Sur le web, une telle stratégie est définie via un en-tête ou un élément `meta` HTTP.  Dans le système d Microsoft Edge d’extension, aucun des deux n’est un mécanisme approprié.  Au lieu de cela, une stratégie d’extension est définie à l’aide du `manifest.json` fichier pour l’extension comme suit :  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Pour plus d’informations sur la syntaxe du programme [][W3CContentSecurityPolicy] CSP, consultez les spécifications de la stratégie de sécurité du contenu et l’article « [Une introduction][HTML5RocksIntroductionContentSecurityPolicy] à la stratégie de sécurité du contenu » sur HTML5Rots.  

## <a name="default-policy-restrictions"></a>Restrictions de stratégie par défaut  

Les packages qui ne définissent pas de stratégie de sécurité de contenu ne sont pas définis `manifest_version` par défaut.  Les packages qui choisissent 2 ont la stratégie de sécurité de contenu `manifest_version` par défaut suivante.  

```javascript
script-src 'self'; object-src 'self'
```  

La stratégie ajoute la sécurité en limitant les extensions et les applications de trois manières :  

**Eval et les fonctions associées sont désactivés**  

Le code suivant ne fonctionne pas :  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

L’évaluation de chaînes de JavaScript comme celle-ci est un vecteur d’attaque XSS courant.  Au lieu de cela, vous devez écrire du code comme :

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**JavaScript en ligne n’est pas exécuté**  

JavaScript en ligne n’est pas exécuté.  Cette restriction interdit les blocs inline et les handlers d’événements en `<script>` ligne, tels que `<button onclick="...">` .

La première restriction efface une classe considérable d’attaques de scripts entre sites en vous rendant impossible d’exécuter accidentellement le script fourni par un tiers malveillant.  Toutefois, cela vous oblige à écrire votre code avec une séparation nette entre le contenu et le comportement \(ce que vous devez faire quand même, n’est-ce pas ?\).  Un exemple peut rendre cela plus clair.  Vous pouvez essayer d’écrire une fenêtre d’action de navigateur sous la seule mesure où : `pop-up.html`  

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

Trois choses doivent changer pour que cela fonctionne comme prévu :  

*   La définition doit être déplacée dans un fichier `clickHandler` JavaScript externe \( `popup.js` peut être une bonne cible).  
*   Les définitions de handler d’événements en ligne doivent être réécrites et `addEventListener` extraites dans `popup.js` .  
    Si vous démarrez actuellement votre programme à l’aide de code tel que , envisagez de le remplacer en le raccordant à l’événement du document ou à l’événement de la fenêtre, en fonction de `<body onload="main();">` `DOMContentLoaded` vos `load` besoins.  Utilisez la première, car elle se déclenche généralement plus rapidement.  

*   L’appel doit être réécrit pour éviter de convertir la chaîne `setTimeout` `"awesome(); totallyAwesome()"` en JavaScript pour l’exécution.  
    Ces modifications peuvent ressembler à ce qui suit :  

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

**Seules les ressources de script et d’objet locales sont chargées**  

Les ressources de script et d’objet peuvent uniquement être chargées à partir du package d’extension, et non à partir du web en général.  Cela garantit que votre extension exécute uniquement le code que vous avez spécifiquement approuvé, ce qui empêche une personne malveillante de rediriger votre demande pour une ressource.  

Au lieu d’écrire du code qui dépend du chargement de jQuery \(ou de toute autre bibliothèque\) à partir d’une CDN externe, envisagez d’inclure la version spécifique de jQuery dans votre package d’extension.  Autrement dit, au lieu de :  

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

Téléchargez le fichier, incluez-le dans votre package et écrivez :  

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

## <a name="relaxing-the-default-policy"></a>Relâchement de la stratégie par défaut  

**Inline Script**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Les scripts en ligne peuvent être autorisés en spécifiant le hachage codé en base 64 du code source dans la stratégie.  Ce hachage doit être précédé de l’algorithme de hachage utilisé \(sha256, sha384 ou sha512\).  Par exemple, accédez à [l’utilisation du hachage pour les \<script\> éléments.][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]  

**Script distant**  

Si vous avez besoin de ressources JavaScript ou d’objets externes, vous pouvez relâcher la stratégie dans une certaine mesure en permettant la liste des origines sécurisées à partir des lesquelles les scripts doivent être acceptés.  Vérifiez que les ressources runtime chargées avec des autorisations élevées d’une extension sont exactement les ressources que vous attendez et qu’elles ne sont pas remplacées par une personne malveillante active du réseau.  Comme [les attaques de][WikiManMiddleAttacks] l’homme au milieu sont à la fois triviales et indétectables sur HTTP, ces origines ne sont pas acceptées.  

Actuellement, les développeurs peuvent autoriser les origines de la liste avec les schémas suivants : `blob` `filesystem` , et `https` `extension` .  La partie hôte de l’origine doit être explicitement spécifiée pour les `https` `extension` schémas.  Les caractères génériques tels que https:, et ne sont pas autorisés ; les caractères génériques de sous-domaine tels `https://*` `https://*.com` que sont `https://*.example.com` autorisés.  Les domaines de la [liste Suffixe public][PublicSuffixList] sont également vus comme des domaines de niveau supérieur génériques.  Pour charger une ressource à partir de ces domaines, le sous-domaine doit être explicitement répertorié.  Par exemple, `https://*.cloudfront.net` n’est pas valide, mais `https://XXXX.cloudfront.net` peut `https://*.XXXX.cloudfront.net` l’être. `allowlisted`  

Pour faciliter le développement, les ressources chargées sur HTTP à partir de serveurs sur votre ordinateur local peuvent être `allowlisted` .  Vous pouvez autoriser le script de liste et les sources d’objets sur n’importe quel port de l’un `http://127.0.0.1` ou l’autre `http://localhost` port.  

> [!NOTE]
> La restriction sur les ressources chargées sur HTTP s’applique uniquement aux ressources qui sont directement exécutés.  Vous êtes toujours libre, par exemple, d’établir des connexions à n’importe quelle origine de votre choix ; la stratégie par défaut ne limite aucune des autres directives du programme `XMLHTTPRequest` `connect-src` CSP.  

Une définition de stratégie relâchée qui permet de charger des ressources de script à partir du protocole `example.com` HTTPS peut ressembler à :  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Les `script-src` deux sont définis par la `object-src` stratégie.  Microsoft Edge n’accepte pas une stratégie qui ne limite pas chacune de ces valeurs à \(au moins\) ' `self` '.  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**JavaScript évalué**  

La stratégie par rapport aux fonctions associées telles que , et peuvent être `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` relâchées en ajoutant `unsafe-eval` à votre stratégie :  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Toutefois, vous devez éviter les stratégies de relâchement.  Les fonctions sont des vecteurs d’attaque XSS puissants.  

## <a name="tightening-the-default-policy"></a>Renforcement de la stratégie par défaut  

Vous pouvez, bien entendu, renforcer cette stratégie dans n’importe quelle mesure de votre extension afin d’augmenter la sécurité au détriment de la commodité.  Pour spécifier que votre extension est en mesure de charger uniquement les ressources de n’importe quel type \(images, etc.) à partir du package d’extension associé, par exemple, une stratégie de peut `default-src 'self'` être appropriée.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a>Scripts de contenu  

La stratégie en cours de discussion s’applique aux pages d’arrière-plan et aux pages d’événements de l’extension.  La façon dont les scripts de contenu s’appliquent aux scripts de contenu de l’extension est plus complexe.  

Les scripts de contenu ne sont généralement pas soumis au programme CSP de l’extension.  Étant donné que les scripts de contenu ne sont pas au format HTML, l’impact principal est qu’ils peuvent être utilisés même si le CSP de l’extension ne spécifie pas, bien que cela ne soit pas `eval` `unsafe-eval` recommandé.  En outre, le CSP de la page ne s’applique pas aux scripts de contenu.  Les balises que les scripts de contenu créent et placent dans le DOM de la page sur qui ils s’exécutent sont `<script>` plus complexes.  Ces scripts sont référencés en tant que scripts INJECTÉS DOM à l’avenir.  

Les scripts DOM injectés qui s’exécutent immédiatement après l’injection dans la page s’exécutent comme prévu.  Imagine script de contenu avec le code suivant comme exemple simple :  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Ce script de contenu provoque une `alert` immédiatement sur `document.write()` le .  Notez que cette dernière s’exécute quelle que soit la stratégie qu’une page peut spécifier.
Toutefois, le comportement devient plus complexe à la fois à l’intérieur de ce script DOM injecté et pour tout script qui ne s’exécute pas immédiatement lors de l’injection.  Imagine que votre extension est en cours d’exécution sur une page qui fournit un CSP associé qui spécifie `script-src 'self'` .  Imaginez maintenant que le script de contenu exécute le code suivant :  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Si un utilisateur choisit ce bouton, le `onclick` script ne s’exécute pas.  Cela est dû au fait que le script n’a pas été exécuté immédiatement et que le code n’est pas interprété tant que l’événement n’est pas considéré comme faisant partie du script de contenu, le CSP de la page \(et non de l’extension\) limite le `click` comportement.  Et comme ce CSP ne spécifie pas, le handler d’événements en ligne `unsafe-inline` est bloqué.  
La façon correcte d’implémenter le comportement souhaité dans ce cas peut être d’ajouter le handler en tant que fonction à partir du script de contenu `onclick` comme suit :  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Un autre problème similaire survient si le script de contenu exécute ce qui suit :  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

Dans ce cas, le script s’exécute et l’alerte s’affiche.  Toutefois, prenez ce cas :  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

Pendant que le script initial s’exécute, l’appel `eval` vers est bloqué.  Autrement dit, alors que le runtime du script initial est autorisé, le comportement au sein du script est réglementé par le CSP de la page.  
Ainsi, selon la façon dont vous écrivez des scripts INJECTÉS DOM dans votre extension, les modifications apportées au programme CSP de la page peuvent affecter le comportement de votre extension.  Étant donné que les scripts de contenu ne sont pas affectés par le programme CSP de la page, c’est une bonne raison de placer autant de comportement que possible de votre extension dans le script de contenu plutôt que dans les scripts injectés par DOM.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Présentation de la stratégie de sécurité du | HTML5 Rocks"  
[PublicSuffixList]: https://publicsuffix.org/list "AFFICHER LA LISTE DES SUFFIXES PUBLICS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Utilisation du hachage pour les éléments \<script\> - Stratégie de sécurité du contenu niveau 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Stratégie de sécurité du contenu niveau 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Attaque de l'| Wikipedia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/contentSecurityPolicy)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
