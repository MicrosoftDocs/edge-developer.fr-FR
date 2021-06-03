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
# <a name="content-security-policy-csp"></a><span data-ttu-id="131e7-104">Stratégie de sécurité du contenu \(CSP\)</span><span class="sxs-lookup"><span data-stu-id="131e7-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="131e7-105">Afin d’atténuer une grande classe de problèmes potentiels de scripts entre sites, le système d’extension Microsoft Edge a incorporé le concept général de stratégie de sécurité du contenu [\(CSP\)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="131e7-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="131e7-106">Cela introduit des stratégies assez strictes qui sécurisationnt les extensions par défaut et vous offre la possibilité de créer et d’appliquer des règles régissant les types de contenu qui peuvent être chargés et exécutés par vos extensions et applications.</span><span class="sxs-lookup"><span data-stu-id="131e7-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="131e7-107">En règle générale, le programme CSP fonctionne comme un mécanisme de blocage/mise en liste des listes d’utilisateurs pour les ressources chargées ou exécutés par vos extensions.</span><span class="sxs-lookup"><span data-stu-id="131e7-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="131e7-108">La définition d’une stratégie raisonnable pour votre extension vous permet d’examiner attentivement les ressources dont votre extension a besoin et de demander au navigateur de s’assurer qu’il s’agit des seules ressources à qui votre extension a accès.</span><span class="sxs-lookup"><span data-stu-id="131e7-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="131e7-109">Les stratégies assurent la sécurité au-delà des autorisations d’hôte que vos demandes d’extension . Il s’agit d’une couche de protection supplémentaire, et non d’un remplacement.</span><span class="sxs-lookup"><span data-stu-id="131e7-109">The policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="131e7-110">Sur le web, une telle stratégie est définie via un en-tête ou un élément `meta` HTTP.</span><span class="sxs-lookup"><span data-stu-id="131e7-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="131e7-111">Dans le système d Microsoft Edge d’extension, aucun des deux n’est un mécanisme approprié.</span><span class="sxs-lookup"><span data-stu-id="131e7-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="131e7-112">Au lieu de cela, une stratégie d’extension est définie à l’aide du `manifest.json` fichier pour l’extension comme suit :</span><span class="sxs-lookup"><span data-stu-id="131e7-112">Instead, an Extension policy is defined using the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="131e7-113">Pour plus d’informations sur la syntaxe du programme [][W3CContentSecurityPolicy] CSP, consultez les spécifications de la stratégie de sécurité du contenu et l’article « [Une introduction][HTML5RocksIntroductionContentSecurityPolicy] à la stratégie de sécurité du contenu » sur HTML5Rots.</span><span class="sxs-lookup"><span data-stu-id="131e7-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <a name="default-policy-restrictions"></a><span data-ttu-id="131e7-114">Restrictions de stratégie par défaut</span><span class="sxs-lookup"><span data-stu-id="131e7-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="131e7-115">Les packages qui ne définissent pas de stratégie de sécurité de contenu ne sont pas définis `manifest_version` par défaut.</span><span class="sxs-lookup"><span data-stu-id="131e7-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="131e7-116">Les packages qui choisissent 2 ont la stratégie de sécurité de contenu `manifest_version` par défaut suivante.</span><span class="sxs-lookup"><span data-stu-id="131e7-116">Packages that choose `manifest_version` 2, have a the follwoing default content security policy.</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="131e7-117">La stratégie ajoute la sécurité en limitant les extensions et les applications de trois manières :</span><span class="sxs-lookup"><span data-stu-id="131e7-117">The policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="131e7-118">Eval et les fonctions associées sont désactivés</span><span class="sxs-lookup"><span data-stu-id="131e7-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="131e7-119">Le code suivant ne fonctionne pas :</span><span class="sxs-lookup"><span data-stu-id="131e7-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="131e7-120">L’évaluation de chaînes de JavaScript comme celle-ci est un vecteur d’attaque XSS courant.</span><span class="sxs-lookup"><span data-stu-id="131e7-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="131e7-121">Au lieu de cela, vous devez écrire du code comme :</span><span class="sxs-lookup"><span data-stu-id="131e7-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="131e7-122">JavaScript en ligne n’est pas exécuté</span><span class="sxs-lookup"><span data-stu-id="131e7-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="131e7-123">JavaScript en ligne n’est pas exécuté.</span><span class="sxs-lookup"><span data-stu-id="131e7-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="131e7-124">Cette restriction interdit les blocs inline et les handlers d’événements en `<script>` ligne, tels que `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="131e7-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="131e7-125">La première restriction efface une classe considérable d’attaques de scripts entre sites en vous rendant impossible d’exécuter accidentellement le script fourni par un tiers malveillant.</span><span class="sxs-lookup"><span data-stu-id="131e7-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="131e7-126">Toutefois, cela vous oblige à écrire votre code avec une séparation nette entre le contenu et le comportement \(ce que vous devez faire quand même, n’est-ce pas ?\).</span><span class="sxs-lookup"><span data-stu-id="131e7-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="131e7-127">Un exemple peut rendre cela plus clair.</span><span class="sxs-lookup"><span data-stu-id="131e7-127">An example may make this clearer.</span></span>  <span data-ttu-id="131e7-128">Vous pouvez essayer d’écrire une fenêtre d’action de navigateur sous la seule mesure où : `pop-up.html`</span><span class="sxs-lookup"><span data-stu-id="131e7-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

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

<span data-ttu-id="131e7-129">Trois choses doivent changer pour que cela fonctionne comme prévu :</span><span class="sxs-lookup"><span data-stu-id="131e7-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="131e7-130">La définition doit être déplacée dans un fichier `clickHandler` JavaScript externe \( `popup.js` peut être une bonne cible).</span><span class="sxs-lookup"><span data-stu-id="131e7-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="131e7-131">Les définitions de handler d’événements en ligne doivent être réécrites et `addEventListener` extraites dans `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="131e7-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="131e7-132">Si vous démarrez actuellement votre programme à l’aide de code tel que , envisagez de le remplacer en le raccordant à l’événement du document ou à l’événement de la fenêtre, en fonction de `<body onload="main();">` `DOMContentLoaded` vos `load` besoins.</span><span class="sxs-lookup"><span data-stu-id="131e7-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="131e7-133">Utilisez la première, car elle se déclenche généralement plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="131e7-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="131e7-134">L’appel doit être réécrit pour éviter de convertir la chaîne `setTimeout` `"awesome(); totallyAwesome()"` en JavaScript pour l’exécution.</span><span class="sxs-lookup"><span data-stu-id="131e7-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="131e7-135">Ces modifications peuvent ressembler à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="131e7-135">Those changes may look something like the following:</span></span>  

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

**<span data-ttu-id="131e7-136">Seules les ressources de script et d’objet locales sont chargées</span><span class="sxs-lookup"><span data-stu-id="131e7-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="131e7-137">Les ressources de script et d’objet peuvent uniquement être chargées à partir du package d’extension, et non à partir du web en général.</span><span class="sxs-lookup"><span data-stu-id="131e7-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="131e7-138">Cela garantit que votre extension exécute uniquement le code que vous avez spécifiquement approuvé, ce qui empêche une personne malveillante de rediriger votre demande pour une ressource.</span><span class="sxs-lookup"><span data-stu-id="131e7-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="131e7-139">Au lieu d’écrire du code qui dépend du chargement de jQuery \(ou de toute autre bibliothèque\) à partir d’une CDN externe, envisagez d’inclure la version spécifique de jQuery dans votre package d’extension.</span><span class="sxs-lookup"><span data-stu-id="131e7-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="131e7-140">Autrement dit, au lieu de :</span><span class="sxs-lookup"><span data-stu-id="131e7-140">That is, instead of:</span></span>  

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

<span data-ttu-id="131e7-141">Téléchargez le fichier, incluez-le dans votre package et écrivez :</span><span class="sxs-lookup"><span data-stu-id="131e7-141">Download the file, include it in your package, and write:</span></span>  

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

## <a name="relaxing-the-default-policy"></a><span data-ttu-id="131e7-142">Relâchement de la stratégie par défaut</span><span class="sxs-lookup"><span data-stu-id="131e7-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="131e7-143">Inline Script</span><span class="sxs-lookup"><span data-stu-id="131e7-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="131e7-144">Les scripts en ligne peuvent être autorisés en spécifiant le hachage codé en base 64 du code source dans la stratégie.</span><span class="sxs-lookup"><span data-stu-id="131e7-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="131e7-145">Ce hachage doit être précédé de l’algorithme de hachage utilisé \(sha256, sha384 ou sha512\).</span><span class="sxs-lookup"><span data-stu-id="131e7-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="131e7-146">Par exemple, accédez à [l’utilisation du hachage pour les \<script\> éléments.][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]</span><span class="sxs-lookup"><span data-stu-id="131e7-146">For an example, navigate to [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage].</span></span>  

**<span data-ttu-id="131e7-147">Script distant</span><span class="sxs-lookup"><span data-stu-id="131e7-147">Remote Script</span></span>**  

<span data-ttu-id="131e7-148">Si vous avez besoin de ressources JavaScript ou d’objets externes, vous pouvez relâcher la stratégie dans une certaine mesure en permettant la liste des origines sécurisées à partir des lesquelles les scripts doivent être acceptés.</span><span class="sxs-lookup"><span data-stu-id="131e7-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="131e7-149">Vérifiez que les ressources runtime chargées avec des autorisations élevées d’une extension sont exactement les ressources que vous attendez et qu’elles ne sont pas remplacées par une personne malveillante active du réseau.</span><span class="sxs-lookup"><span data-stu-id="131e7-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="131e7-150">Comme [les attaques de][WikiManMiddleAttacks] l’homme au milieu sont à la fois triviales et indétectables sur HTTP, ces origines ne sont pas acceptées.</span><span class="sxs-lookup"><span data-stu-id="131e7-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="131e7-151">Actuellement, les développeurs peuvent autoriser les origines de la liste avec les schémas suivants : `blob` `filesystem` , et `https` `extension` .</span><span class="sxs-lookup"><span data-stu-id="131e7-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="131e7-152">La partie hôte de l’origine doit être explicitement spécifiée pour les `https` `extension` schémas.</span><span class="sxs-lookup"><span data-stu-id="131e7-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="131e7-153">Les caractères génériques tels que https:, et ne sont pas autorisés ; les caractères génériques de sous-domaine tels `https://*` `https://*.com` que sont `https://*.example.com` autorisés.</span><span class="sxs-lookup"><span data-stu-id="131e7-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="131e7-154">Les domaines de la [liste Suffixe public][PublicSuffixList] sont également vus comme des domaines de niveau supérieur génériques.</span><span class="sxs-lookup"><span data-stu-id="131e7-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="131e7-155">Pour charger une ressource à partir de ces domaines, le sous-domaine doit être explicitement répertorié.</span><span class="sxs-lookup"><span data-stu-id="131e7-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="131e7-156">Par exemple, `https://*.cloudfront.net` n’est pas valide, mais `https://XXXX.cloudfront.net` peut `https://*.XXXX.cloudfront.net` l’être. `allowlisted`</span><span class="sxs-lookup"><span data-stu-id="131e7-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be `allowlisted`.</span></span>  

<span data-ttu-id="131e7-157">Pour faciliter le développement, les ressources chargées sur HTTP à partir de serveurs sur votre ordinateur local peuvent être `allowlisted` .</span><span class="sxs-lookup"><span data-stu-id="131e7-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be `allowlisted`.</span></span>  <span data-ttu-id="131e7-158">Vous pouvez autoriser le script de liste et les sources d’objets sur n’importe quel port de l’un `http://127.0.0.1` ou l’autre `http://localhost` port.</span><span class="sxs-lookup"><span data-stu-id="131e7-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="131e7-159">La restriction sur les ressources chargées sur HTTP s’applique uniquement aux ressources qui sont directement exécutés.</span><span class="sxs-lookup"><span data-stu-id="131e7-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="131e7-160">Vous êtes toujours libre, par exemple, d’établir des connexions à n’importe quelle origine de votre choix ; la stratégie par défaut ne limite aucune des autres directives du programme `XMLHTTPRequest` `connect-src` CSP.</span><span class="sxs-lookup"><span data-stu-id="131e7-160">You are still free, for example, to make `XMLHTTPRequest` connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="131e7-161">Une définition de stratégie relâchée qui permet de charger des ressources de script à partir du protocole `example.com` HTTPS peut ressembler à :</span><span class="sxs-lookup"><span data-stu-id="131e7-161">A relaxed policy definition which allows script resources to be loaded from `example.com` over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="131e7-162">Les `script-src` deux sont définis par la `object-src` stratégie.</span><span class="sxs-lookup"><span data-stu-id="131e7-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="131e7-163">Microsoft Edge n’accepte pas une stratégie qui ne limite pas chacune de ces valeurs à \(au moins\) ' `self` '.</span><span class="sxs-lookup"><span data-stu-id="131e7-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="131e7-164">JavaScript évalué</span><span class="sxs-lookup"><span data-stu-id="131e7-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="131e7-165">La stratégie par rapport aux fonctions associées telles que , et peuvent être `eval()` `setTimeout(String)` `setInterval(String)` `new Function(String)` relâchées en ajoutant `unsafe-eval` à votre stratégie :</span><span class="sxs-lookup"><span data-stu-id="131e7-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="131e7-166">Toutefois, vous devez éviter les stratégies de relâchement.</span><span class="sxs-lookup"><span data-stu-id="131e7-166">However, you should avoid relaxing policies.</span></span>  <span data-ttu-id="131e7-167">Les fonctions sont des vecteurs d’attaque XSS puissants.</span><span class="sxs-lookup"><span data-stu-id="131e7-167">The functions are notorious XSS attack vectors.</span></span>  

## <a name="tightening-the-default-policy"></a><span data-ttu-id="131e7-168">Renforcement de la stratégie par défaut</span><span class="sxs-lookup"><span data-stu-id="131e7-168">Tightening the default policy</span></span>  

<span data-ttu-id="131e7-169">Vous pouvez, bien entendu, renforcer cette stratégie dans n’importe quelle mesure de votre extension afin d’augmenter la sécurité au détriment de la commodité.</span><span class="sxs-lookup"><span data-stu-id="131e7-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="131e7-170">Pour spécifier que votre extension est en mesure de charger uniquement les ressources de n’importe quel type \(images, etc.) à partir du package d’extension associé, par exemple, une stratégie de peut `default-src 'self'` être appropriée.</span><span class="sxs-lookup"><span data-stu-id="131e7-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <a name="content-scripts"></a><span data-ttu-id="131e7-171">Scripts de contenu</span><span class="sxs-lookup"><span data-stu-id="131e7-171">Content Scripts</span></span>  

<span data-ttu-id="131e7-172">La stratégie en cours de discussion s’applique aux pages d’arrière-plan et aux pages d’événements de l’extension.</span><span class="sxs-lookup"><span data-stu-id="131e7-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="131e7-173">La façon dont les scripts de contenu s’appliquent aux scripts de contenu de l’extension est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="131e7-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="131e7-174">Les scripts de contenu ne sont généralement pas soumis au programme CSP de l’extension.</span><span class="sxs-lookup"><span data-stu-id="131e7-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="131e7-175">Étant donné que les scripts de contenu ne sont pas au format HTML, l’impact principal est qu’ils peuvent être utilisés même si le CSP de l’extension ne spécifie pas, bien que cela ne soit pas `eval` `unsafe-eval` recommandé.</span><span class="sxs-lookup"><span data-stu-id="131e7-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="131e7-176">En outre, le CSP de la page ne s’applique pas aux scripts de contenu.</span><span class="sxs-lookup"><span data-stu-id="131e7-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="131e7-177">Les balises que les scripts de contenu créent et placent dans le DOM de la page sur qui ils s’exécutent sont `<script>` plus complexes.</span><span class="sxs-lookup"><span data-stu-id="131e7-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="131e7-178">Ces scripts sont référencés en tant que scripts INJECTÉS DOM à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="131e7-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="131e7-179">Les scripts DOM injectés qui s’exécutent immédiatement après l’injection dans la page s’exécutent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="131e7-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="131e7-180">Imagine script de contenu avec le code suivant comme exemple simple :</span><span class="sxs-lookup"><span data-stu-id="131e7-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="131e7-181">Ce script de contenu provoque une `alert` immédiatement sur `document.write()` le .</span><span class="sxs-lookup"><span data-stu-id="131e7-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="131e7-182">Notez que cette dernière s’exécute quelle que soit la stratégie qu’une page peut spécifier.</span><span class="sxs-lookup"><span data-stu-id="131e7-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="131e7-183">Toutefois, le comportement devient plus complexe à la fois à l’intérieur de ce script DOM injecté et pour tout script qui ne s’exécute pas immédiatement lors de l’injection.</span><span class="sxs-lookup"><span data-stu-id="131e7-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="131e7-184">Imagine que votre extension est en cours d’exécution sur une page qui fournit un CSP associé qui spécifie `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="131e7-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="131e7-185">Imaginez maintenant que le script de contenu exécute le code suivant :</span><span class="sxs-lookup"><span data-stu-id="131e7-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="131e7-186">Si un utilisateur choisit ce bouton, le `onclick` script ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="131e7-186">If a user chooses that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="131e7-187">Cela est dû au fait que le script n’a pas été exécuté immédiatement et que le code n’est pas interprété tant que l’événement n’est pas considéré comme faisant partie du script de contenu, le CSP de la page \(et non de l’extension\) limite le `click` comportement.</span><span class="sxs-lookup"><span data-stu-id="131e7-187">This is because the script did not immediately run and code is not interpreted until the `click` event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="131e7-188">Et comme ce CSP ne spécifie pas, le handler d’événements en ligne `unsafe-inline` est bloqué.</span><span class="sxs-lookup"><span data-stu-id="131e7-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="131e7-189">La façon correcte d’implémenter le comportement souhaité dans ce cas peut être d’ajouter le handler en tant que fonction à partir du script de contenu `onclick` comme suit :</span><span class="sxs-lookup"><span data-stu-id="131e7-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="131e7-190">Un autre problème similaire survient si le script de contenu exécute ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="131e7-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="131e7-191">Dans ce cas, le script s’exécute et l’alerte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="131e7-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="131e7-192">Toutefois, prenez ce cas :</span><span class="sxs-lookup"><span data-stu-id="131e7-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="131e7-193">Pendant que le script initial s’exécute, l’appel `eval` vers est bloqué.</span><span class="sxs-lookup"><span data-stu-id="131e7-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="131e7-194">Autrement dit, alors que le runtime du script initial est autorisé, le comportement au sein du script est réglementé par le CSP de la page.</span><span class="sxs-lookup"><span data-stu-id="131e7-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="131e7-195">Ainsi, selon la façon dont vous écrivez des scripts INJECTÉS DOM dans votre extension, les modifications apportées au programme CSP de la page peuvent affecter le comportement de votre extension.</span><span class="sxs-lookup"><span data-stu-id="131e7-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="131e7-196">Étant donné que les scripts de contenu ne sont pas affectés par le programme CSP de la page, c’est une bonne raison de placer autant de comportement que possible de votre extension dans le script de contenu plutôt que dans les scripts injectés par DOM.</span><span class="sxs-lookup"><span data-stu-id="131e7-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Présentation de la stratégie de sécurité du | HTML5 Rocks"  
[PublicSuffixList]: https://publicsuffix.org/list "AFFICHER LA LISTE DES SUFFIXES PUBLICS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Utilisation du hachage pour les éléments \<script\> - Stratégie de sécurité du contenu niveau 2 | W3C"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Stratégie de sécurité du contenu niveau 3 | W3C"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Attaque de l'| Wikipedia"  

> [!NOTE]
> <span data-ttu-id="131e7-202">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="131e7-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="131e7-203">La page d’origine se trouve [ici.](https://developer.chrome.com/extensions/contentSecurityPolicy)</span><span class="sxs-lookup"><span data-stu-id="131e7-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="131e7-205">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="131e7-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
