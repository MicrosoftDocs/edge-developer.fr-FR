---
description: Extensions de la stratégie de sécurité du contenu pour les extensions Edge (chrome).
title: Stratégie de sécurité du contenu (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-chrome, développement d’extensions, extensions de navigateur, compléments, Centre des partenaires, développeur
ms.openlocfilehash: f3769639465d048c42ad0705f74598fbd1db8a20
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015715"
---
# <span data-ttu-id="d876a-104">Stratégie de sécurité du contenu \ (CSP \)</span><span class="sxs-lookup"><span data-stu-id="d876a-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="d876a-105">Afin d’atténuer un grand nombre d’erreurs de script intersites potentiels, le système d’extension Microsoft Edge a incorporé le concept général de la [stratégie de sécurité du contenu \ (CSP)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="d876a-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="d876a-106">Ce type d’introduction présente certaines stratégies relativement strictes qui rendent les extensions plus sûres par défaut et vous permet de créer et d’appliquer des règles régissant les types de contenu qui peuvent être chargés et exécutés par vos extensions et applications.</span><span class="sxs-lookup"><span data-stu-id="d876a-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="d876a-107">En règle générale, le CSP fonctionne comme un mécanisme bloc/allowlisting pour les ressources chargées ou exécutées par vos extensions.</span><span class="sxs-lookup"><span data-stu-id="d876a-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="d876a-108">La définition d’une politique raisonnable pour votre extension vous permet de réfléchir soigneusement aux ressources nécessaires pour votre extension et de demander au navigateur de s’assurer que les seules ressources auxquelles votre extension a accès.</span><span class="sxs-lookup"><span data-stu-id="d876a-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="d876a-109">Ces stratégies garantissent la sécurité au-delà des autorisations de l’hôte de vos demandes d’extension. Il s’agit d’une couche de protection supplémentaire et pas d’un remplacement.</span><span class="sxs-lookup"><span data-stu-id="d876a-109">These policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="d876a-110">Sur le Web, une telle stratégie est définie via un en-tête ou un `meta` élément http.</span><span class="sxs-lookup"><span data-stu-id="d876a-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="d876a-111">Aucun mécanisme approprié n’est nécessaire dans le système d’extension Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d876a-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="d876a-112">Au lieu de cela, une stratégie d’extension est définie via le `manifest.json` fichier pour l’extension comme suit:</span><span class="sxs-lookup"><span data-stu-id="d876a-112">Instead, an Extension policy is defined via the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="d876a-113">Pour plus d’informations sur la syntaxe du fournisseur de services cryptographiques, voir la spécification de la [stratégie de sécurité du contenu][W3CContentSecurityPolicy] et l’article [«Présentation de la stratégie de sécurité du contenu»][HTML5RocksIntroductionContentSecurityPolicy] sur HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="d876a-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <span data-ttu-id="d876a-114">Restrictions de stratégie par défaut</span><span class="sxs-lookup"><span data-stu-id="d876a-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="d876a-115">Les packages qui ne définissent aucune `manifest_version` stratégie de sécurité du contenu par défaut ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="d876a-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="d876a-116">Ceux qui sélectionnent `manifest_version` 2 disposent d’une stratégie de sécurité du contenu par défaut:</span><span class="sxs-lookup"><span data-stu-id="d876a-116">Those that select `manifest_version` 2, have a default content security policy of:</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="d876a-117">Cette stratégie ajoute de la sécurité en limitant les extensions et applications de trois manières:</span><span class="sxs-lookup"><span data-stu-id="d876a-117">This policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="d876a-118">Les fonctions eval et apparentées sont désactivées</span><span class="sxs-lookup"><span data-stu-id="d876a-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="d876a-119">Le code comme suit ne fonctionne pas:</span><span class="sxs-lookup"><span data-stu-id="d876a-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="d876a-120">L’évaluation de chaînes de JavaScript comme celle-ci est un vecteur d’attaque XSS courante.</span><span class="sxs-lookup"><span data-stu-id="d876a-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="d876a-121">À la place, vous devez écrire du code comme suit:</span><span class="sxs-lookup"><span data-stu-id="d876a-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="d876a-122">JavaScript intraligne ne s’exécute pas</span><span class="sxs-lookup"><span data-stu-id="d876a-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="d876a-123">JavaScript Inline ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="d876a-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="d876a-124">Cette restriction interdit aux blocs intralignes `<script>` et aux gestionnaires d’événements Inline, tels que `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="d876a-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="d876a-125">La première restriction réapparaît une énorme classe d’attaques de script entre sites en vous rendant impossible d’exécuter accidentellement le script fourni par un tiers malveillant.</span><span class="sxs-lookup"><span data-stu-id="d876a-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="d876a-126">Néanmoins, il est nécessaire d’écrire votre code avec une séparation nette entre le contenu et le comportement \ (c’est le cas, vous devez tout de même bien.</span><span class="sxs-lookup"><span data-stu-id="d876a-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="d876a-127">Par exemple, il est possible que ce soit plus clair.</span><span class="sxs-lookup"><span data-stu-id="d876a-127">An example may make this clearer.</span></span>  <span data-ttu-id="d876a-128">Il est possible que vous deviez écrire une action de navigateur contextuelle sous la forme d’un seul `pop-up.html` contenant:</span><span class="sxs-lookup"><span data-stu-id="d876a-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

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

<span data-ttu-id="d876a-129">Trois éléments doivent changer pour que ce processus fonctionne comme prévu.</span><span class="sxs-lookup"><span data-stu-id="d876a-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="d876a-130">La `clickHandler` définition doit être déplacée vers un fichier JavaScript externe ( `popup.js` il peut s’agir d’un bon destinataire).</span><span class="sxs-lookup"><span data-stu-id="d876a-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="d876a-131">Les définitions des gestionnaires d’événements en ligne doivent être réécrites en termes de `addEventListener` et en extraction `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="d876a-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="d876a-132">Si vous démarrez actuellement votre programme en utilisant du code tel que `<body onload="main();">` , envisagez de le remplacer par un raccordement à l' `DOMContentLoaded` événement du document ou à l' `load` événement de la fenêtre, en fonction de vos besoins.</span><span class="sxs-lookup"><span data-stu-id="d876a-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="d876a-133">Utilisez l’ancien, car il est généralement déclenché plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="d876a-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="d876a-134">L' `setTimeout` appel doit être réécrit pour éviter de convertir la chaîne `"awesome(); totallyAwesome()"` en code JavaScript en exécution.</span><span class="sxs-lookup"><span data-stu-id="d876a-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="d876a-135">Ces modifications pourraient ressembler à ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="d876a-135">Those changes may look something like the following:</span></span>  

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

**<span data-ttu-id="d876a-136">Seules les ressources d’objet et de script local sont chargées.</span><span class="sxs-lookup"><span data-stu-id="d876a-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="d876a-137">Les ressources de script et d’objet peuvent uniquement être chargées à partir du package d’extension, et non à partir du Web.</span><span class="sxs-lookup"><span data-stu-id="d876a-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="d876a-138">Cela permet de s’assurer que votre extension exécute uniquement le code que vous avez approuvé en particulier, ce qui évite à un attaquant du réseau actif de rediriger intentionnellement votre demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="d876a-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="d876a-139">Au lieu d’écrire du code qui dépend de jQuery \ (ou d’une autre bibliothèque), il est conseillé d’inclure la version spécifique de jQuery dans votre package d’extension.</span><span class="sxs-lookup"><span data-stu-id="d876a-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="d876a-140">C’est-à-dire, au lieu de:</span><span class="sxs-lookup"><span data-stu-id="d876a-140">That is, instead of:</span></span>  

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

<span data-ttu-id="d876a-141">Téléchargez le fichier, incluez-le dans votre package, puis écrivez:</span><span class="sxs-lookup"><span data-stu-id="d876a-141">Download the file, include it in your package, and write:</span></span>  

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

## <span data-ttu-id="d876a-142">Relaxer la stratégie par défaut</span><span class="sxs-lookup"><span data-stu-id="d876a-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="d876a-143">Script inline</span><span class="sxs-lookup"><span data-stu-id="d876a-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="d876a-144">Les scripts inline peuvent être autorisés en spécifiant le hachage encodé en base64 du code source de la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d876a-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="d876a-145">Ce hachage doit être préfixé à l’aide de l’algorithme de hachage utilisé \ (SHA256, SHA384 ou SHA512 \).</span><span class="sxs-lookup"><span data-stu-id="d876a-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="d876a-146">Pour obtenir un exemple, voir [utilisation de hachage pour les \<script\> éléments][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] .</span><span class="sxs-lookup"><span data-stu-id="d876a-146">See [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] for an example.</span></span>  

**<span data-ttu-id="d876a-147">Script distant</span><span class="sxs-lookup"><span data-stu-id="d876a-147">Remote Script</span></span>**  

<span data-ttu-id="d876a-148">Si vous avez besoin de ressources d’objets ou JavaScript externes, vous devrez peut-être détendre la stratégie vers une extension limitée d’allowlistings sécurisées à partir desquelles les scripts doivent être acceptés.</span><span class="sxs-lookup"><span data-stu-id="d876a-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="d876a-149">Vérifiez que les ressources d’exécution dont le chargement est limité aux ressources dont vous vous attendez et qu’elles ne sont pas remplacées par une attaque réseau active.</span><span class="sxs-lookup"><span data-stu-id="d876a-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="d876a-150">En tant qu' [attaques par homme-au-milieu, il][WikiManMiddleAttacks] n’est pas possible d’accepter et de détecter les origines sur http.</span><span class="sxs-lookup"><span data-stu-id="d876a-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="d876a-151">Pour l’instant, les développeurs sont en mesure de verteer avec les schémas suivants: `blob` ,, `filesystem` `https` et `extension` .</span><span class="sxs-lookup"><span data-stu-id="d876a-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="d876a-152">La partie hôte de l’origine doit être explicitement spécifiée pour les `https` `extension` schémas et.</span><span class="sxs-lookup"><span data-stu-id="d876a-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="d876a-153">Les caractères génériques génériques tels que https: `https://*` et ne `https://*.com` sont pas autorisés; les caractères génériques de sous-domaine tels qu' `https://*.example.com` ils sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="d876a-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="d876a-154">Les domaines figurant dans la [liste de suffixes publics][PublicSuffixList] sont également considérés comme des domaines de niveau supérieur génériques.</span><span class="sxs-lookup"><span data-stu-id="d876a-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="d876a-155">Pour charger une ressource à partir de ces domaines, le sous-domaine doit être répertorié explicitement.</span><span class="sxs-lookup"><span data-stu-id="d876a-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="d876a-156">Par exemple, `https://*.cloudfront.net` n’est pas valide, `https://XXXX.cloudfront.net` mais `https://*.XXXX.cloudfront.net` peut être allowlisted.</span><span class="sxs-lookup"><span data-stu-id="d876a-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be allowlisted.</span></span>  

<span data-ttu-id="d876a-157">Pour faciliter la mise au point, les ressources chargées sur HTTP à partir de serveurs de votre ordinateur local peuvent être allowlistedes.</span><span class="sxs-lookup"><span data-stu-id="d876a-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be allowlisted.</span></span>  <span data-ttu-id="d876a-158">Vous pouvez verte des sources d’objet et de script sur n’importe quel port de l’une ou l’autre `http://127.0.0.1` `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="d876a-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="d876a-159">La restriction par rapport aux ressources chargées sur HTTP s’applique uniquement aux ressources qui sont exécutées directement.</span><span class="sxs-lookup"><span data-stu-id="d876a-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="d876a-160">Vous êtes toujours libre (par exemple, pour créer des connexions de type XMLHTTPRequest à l’origine qui vous plaît); la stratégie par défaut n’est pas limitée `connect-src` ou n’importe quelle autre directive CSP de quelque manière que ce soit.</span><span class="sxs-lookup"><span data-stu-id="d876a-160">You are still free, for example, to make XMLHTTPRequest connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="d876a-161">Une définition de stratégie souple qui permet le chargement des ressources de script à partir de example.com sur HTTPs peut se présenter comme suit:</span><span class="sxs-lookup"><span data-stu-id="d876a-161">A relaxed policy definition which allows script resources to be loaded from example.com over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="d876a-162">Both `script-src` et `object-src` définis par la stratégie.</span><span class="sxs-lookup"><span data-stu-id="d876a-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="d876a-163">Microsoft Edge n’accepte pas une stratégie qui ne limite pas chacune de ces valeurs à \ (au moins \) `self` .</span><span class="sxs-lookup"><span data-stu-id="d876a-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="d876a-164">JavaScript évalué</span><span class="sxs-lookup"><span data-stu-id="d876a-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="d876a-165">La stratégie par rapport aux `eval()` fonctions associées `setTimeout(String)` et `setInterval(String)` celles- `new Function(String)` ci peuvent être assouplies en les ajoutant `unsafe-eval` à votre stratégie:</span><span class="sxs-lookup"><span data-stu-id="d876a-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="d876a-166">Toutefois, nous vous recommandons vivement de le faire.</span><span class="sxs-lookup"><span data-stu-id="d876a-166">However, we strongly recommend against doing this.</span></span>  <span data-ttu-id="d876a-167">Ces fonctions sont des vecteurs d’attaque XSS.</span><span class="sxs-lookup"><span data-stu-id="d876a-167">These functions are notorious XSS attack vectors.</span></span>  

## <span data-ttu-id="d876a-168">Renforcement de la stratégie par défaut</span><span class="sxs-lookup"><span data-stu-id="d876a-168">Tightening the default policy</span></span>  

<span data-ttu-id="d876a-169">Vous pouvez, bien entendu, serrer cette politique dans la mesure où votre extension permet d’augmenter la sécurité aux dépens de la commodité.</span><span class="sxs-lookup"><span data-stu-id="d876a-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="d876a-170">Pour indiquer que votre extension peut uniquement charger des ressources de tout type \ (images, etc.) à partir du package d’extension associé, par exemple, la stratégie de `default-src 'self'` peut être appropriée.</span><span class="sxs-lookup"><span data-stu-id="d876a-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <span data-ttu-id="d876a-171">Scripts de contenu</span><span class="sxs-lookup"><span data-stu-id="d876a-171">Content Scripts</span></span>  

<span data-ttu-id="d876a-172">La stratégie en cours de discussion s’applique aux pages d’arrière-plan et aux pages d’événements de l’extension.</span><span class="sxs-lookup"><span data-stu-id="d876a-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="d876a-173">La façon dont les scripts s’appliquent aux scripts de contenu de l’extension est plus complexe.</span><span class="sxs-lookup"><span data-stu-id="d876a-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="d876a-174">Les scripts de contenu ne sont généralement pas soumis au CSP de l’extension.</span><span class="sxs-lookup"><span data-stu-id="d876a-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="d876a-175">Dans la mesure où les scripts ne sont pas au format HTML, l’impact principal de ces derniers est qu’ils peuvent être utilisés `eval` même si le CSP de l’extension n’est pas spécifié `unsafe-eval` , bien que cela soit déconseillé.</span><span class="sxs-lookup"><span data-stu-id="d876a-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="d876a-176">Par ailleurs, le CSP de la page ne s’applique pas aux scripts de contenu.</span><span class="sxs-lookup"><span data-stu-id="d876a-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="d876a-177">Plus difficile sont les `<script>` balises que les scripts de contenu créent et placent dans le DOM de la page sur laquelle ils s’exécutent.</span><span class="sxs-lookup"><span data-stu-id="d876a-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="d876a-178">Celles-ci sont référencées en tant que scripts injectés DOM.</span><span class="sxs-lookup"><span data-stu-id="d876a-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="d876a-179">Les scripts d’injection DOM qui s’exécutent immédiatement après l’insertion dans la page s’exécutent comme prévu.</span><span class="sxs-lookup"><span data-stu-id="d876a-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="d876a-180">Imaginez un script de contenu avec le code suivant comme exemple simple:</span><span class="sxs-lookup"><span data-stu-id="d876a-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="d876a-181">Ce script de contenu entraîne une `alert` interdépendance immédiate `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="d876a-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="d876a-182">Notez que cette opération s’exécute quelle que soit la stratégie spécifiée par une page.</span><span class="sxs-lookup"><span data-stu-id="d876a-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="d876a-183">Toutefois, le comportement devient plus compliqué tant au sein de ce DOM injecté par le script injecté que dans le cas d’une injection.</span><span class="sxs-lookup"><span data-stu-id="d876a-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="d876a-184">Imaginez que votre extension s’exécute sur une page qui fournit un CSP associé spécifiant `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="d876a-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="d876a-185">Imaginez maintenant que le script de contenu exécute le code suivant:</span><span class="sxs-lookup"><span data-stu-id="d876a-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="d876a-186">Si un utilisateur clique sur ce bouton, le `onclick` script ne s’exécute pas.</span><span class="sxs-lookup"><span data-stu-id="d876a-186">If a user clicks on that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="d876a-187">En effet, le script ne s’est pas exécuté immédiatement et le code n’est pas interprété tant que l’événement Click n’a pas été considéré comme faisant partie du script de contenu, de sorte que le fournisseur de services de cryptographie de la page \ (sans l’extension \) limite ce comportement.</span><span class="sxs-lookup"><span data-stu-id="d876a-187">This is because the script did not immediately run and code is not interpreted until the click event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="d876a-188">Et dans la mesure où ce fournisseur de services de cryptographie n’est pas spécifié `unsafe-inline` , le gestionnaire d’événements Inline est bloqué.</span><span class="sxs-lookup"><span data-stu-id="d876a-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="d876a-189">Pour implémenter le comportement souhaité dans le cas présent, il est possible d’ajouter le `onclick` Gestionnaire en tant que fonction du script de contenu comme suit:</span><span class="sxs-lookup"><span data-stu-id="d876a-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="d876a-190">Un autre problème semblable se produit si le script de contenu exécute ce qui suit:</span><span class="sxs-lookup"><span data-stu-id="d876a-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="d876a-191">Dans ce cas, le script s’exécute et l’alerte s’affiche.</span><span class="sxs-lookup"><span data-stu-id="d876a-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="d876a-192">Toutefois, prenez ce cas:</span><span class="sxs-lookup"><span data-stu-id="d876a-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="d876a-193">Pendant l’exécution du script initial, l’appel à `eval` est bloqué.</span><span class="sxs-lookup"><span data-stu-id="d876a-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="d876a-194">Autrement dit, lorsque le runtime de script initial est autorisé, le comportement au sein du script est réglementé par le fournisseur de services de cryptographie de la page.</span><span class="sxs-lookup"><span data-stu-id="d876a-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="d876a-195">Par conséquent, en fonction de la manière dont vous écrivez les scripts injectés DOM dans votre extension, les modifications apportées au CSP de la page peuvent affecter le comportement de votre extension.</span><span class="sxs-lookup"><span data-stu-id="d876a-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="d876a-196">Dans la mesure où les scripts de contenu ne sont pas affectés par le fournisseur de services cryptographiques de la page, c’est une bonne raison de placer le plus de comportement possible de votre extension dans le script de contenu plutôt que dans les scripts injectés DOM.</span><span class="sxs-lookup"><span data-stu-id="d876a-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Présentation de la politique de sécurité du contenu-Rocks HTML5"  
[PublicSuffixList]: https://publicsuffix.org/list "AFFICHER LA LISTE DES SUFFIXES PUBLICS"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Utilisation du hachage pour \ <script \ > éléments-niveau de la stratégie de sécurité du contenu 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Niveau de stratégie de sécurité du contenu 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Attaque de l’homme-au-milieu-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="d876a-202">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d876a-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d876a-203">La page d’origine est disponible [ici](https://developer.chrome.com/extensions/contentSecurityPolicy).</span><span class="sxs-lookup"><span data-stu-id="d876a-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="d876a-205">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d876a-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
