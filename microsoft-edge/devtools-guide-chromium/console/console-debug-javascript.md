---
description: Les erreurs JavaScript sont signalées par les outils de développement et déboguer chacune d’elles dans la console
title: Suivi des erreurs à l’aide de la console
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/13/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ebd12f8932332b3e63162ab6952577bdb43bbccd
ms.sourcegitcommit: 2e516a92272e38d8073603f860ae49f944718670
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/13/2021
ms.locfileid: "11483410"
---
# <a name="debug-errors-reported-in-console"></a><span data-ttu-id="319d9-104">Erreurs de débogage signalées dans la console</span><span class="sxs-lookup"><span data-stu-id="319d9-104">Debug errors reported in Console</span></span>  

<span data-ttu-id="319d9-105">La première expérience que vous avez avec la **console est** probablement une erreur dans un script.</span><span class="sxs-lookup"><span data-stu-id="319d9-105">The first experience you have with the **Console** is probably an error in a script.</span></span>  <span data-ttu-id="319d9-106">Pour l’essayer, accédez à [l’erreur JavaScript signalée dans l’outil console.][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]</span><span class="sxs-lookup"><span data-stu-id="319d9-106">To try it, navigate to [JavaScript error reported in the Console tool][GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml].</span></span>  

<span data-ttu-id="319d9-107">Si vous ouvrez DevTools dans le navigateur, un bouton en haut à droite affiche une erreur pour la page web.</span><span class="sxs-lookup"><span data-stu-id="319d9-107">If you open DevTools in the browser, a button on the top right displays an error for the webpage.</span></span>  
<span data-ttu-id="319d9-108">Choisissez le bouton pour vous aider à vous rendre sur la **console** et vous donner plus d’informations sur l’erreur.</span><span class="sxs-lookup"><span data-stu-id="319d9-108">Choose the button to take you to the **Console** and give you more information about the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-error.msft.png" alt-text="DevTools fournit des informations détaillées sur l’erreur dans la console" lightbox="../media/console-debug-displays-error.msft.png":::
   <span data-ttu-id="319d9-110">DevTools fournit des informations détaillées sur l’erreur dans la **console**</span><span class="sxs-lookup"><span data-stu-id="319d9-110">DevTools gives detailed information about the error in the **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="319d9-111">À partir des informations, vous pouvez collecter que l’erreur se trouve sur la ligne 16 du `error.html` fichier.</span><span class="sxs-lookup"><span data-stu-id="319d9-111">From the information, you may gather that the error is on line 16 of the `error.html` file.</span></span>  <span data-ttu-id="319d9-112">Si vous choisissez le lien à droite de la console, il vous permet d’utiliser l’outil Sources et met en évidence la ligne de `error.html:16` code avec \*\*\*\* l’erreur. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="319d9-112">If you choose the `error.html:16` link on the right of the **Console**, it takes you to the **Sources** tool and highlights the line of code with the error.</span></span>  

:::image type="complex" source="../media/console-debug-displays-in-sources.msft.png" alt-text="L’outil Sources met en évidence la ligne de code à l’origine de l’erreur" lightbox="../media/console-debug-displays-in-sources.msft.png":::
   <span data-ttu-id="319d9-114">**L’outil Sources** met en évidence la ligne de code à l’origine de l’erreur</span><span class="sxs-lookup"><span data-stu-id="319d9-114">The **Sources** tool highlights the line of code that causes the error</span></span>  
:::image-end:::  

<span data-ttu-id="319d9-115">Le script tente d’obtenir le premier élément du document et `h2` de peindre une bordure rouge autour de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="319d9-115">The script tries to get the first `h2` element in the document and paint a red border around it.</span></span>  <span data-ttu-id="319d9-116">Mais aucun `h2` élément n’existe, le script échoue.</span><span class="sxs-lookup"><span data-stu-id="319d9-116">But no `h2` element exists, so the script fails.</span></span>  

## <a name="find-and-debug-network-issues"></a><span data-ttu-id="319d9-117">Rechercher et déboguer des problèmes réseau</span><span class="sxs-lookup"><span data-stu-id="319d9-117">Find and debug network issues</span></span>  

<span data-ttu-id="319d9-118">Les autres erreurs que la **console** signale sont des erreurs réseau.</span><span class="sxs-lookup"><span data-stu-id="319d9-118">Other errors that the **Console** reports are network errors.</span></span>  <span data-ttu-id="319d9-119">Pour l’afficher en action, accédez à l’erreur [réseau signalée dans la console.][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]</span><span class="sxs-lookup"><span data-stu-id="319d9-119">To display it in action, navigate to the [Network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error.msft.png" alt-text="La console affiche un réseau et une erreur JavaScript" lightbox="../media/console-debug-network-error.msft.png":::
   <span data-ttu-id="319d9-121">**La console** affiche un réseau et une erreur JavaScript</span><span class="sxs-lookup"><span data-stu-id="319d9-121">**Console** displays a Network and a JavaScript error</span></span>  
:::image-end:::  

<span data-ttu-id="319d9-122">Le tableau `loading` s’affiche, mais rien ne change sur la page web, car les données ne sont jamais récupérées.</span><span class="sxs-lookup"><span data-stu-id="319d9-122">The table displays `loading`, but nothing changes on the webpage because the data is never retrieved.</span></span>  <span data-ttu-id="319d9-123">Dans la **console,** les deux erreurs suivantes se sont produites.</span><span class="sxs-lookup"><span data-stu-id="319d9-123">In the **Console**, the following two errors occurred.</span></span>  

*   <span data-ttu-id="319d9-124">Erreur réseau qui commence par la `GET` méthode HTTP suivie d’un URI.</span><span class="sxs-lookup"><span data-stu-id="319d9-124">A network error that starts with `GET` HTTP method followed by a URI.</span></span>  
*   <span data-ttu-id="319d9-125">Une `Uncaught (in promise) TypeError: data.forEach is not a function` erreur.</span><span class="sxs-lookup"><span data-stu-id="319d9-125">An `Uncaught (in promise) TypeError: data.forEach is not a function` error.</span></span>  
    
<span data-ttu-id="319d9-126">Si vous choisissez le `network-error.html:40` lien dans la **console,** DevTools vous permet d’utiliser l’outil **Sources.**</span><span class="sxs-lookup"><span data-stu-id="319d9-126">If you choose the `network-error.html:40` link in the **Console**, DevTools takes you to the **Sources** tool.</span></span>  <span data-ttu-id="319d9-127">La ligne de code problématique est mise en surbrillant et suivie d’un `error` bouton \( `x` \).</span><span class="sxs-lookup"><span data-stu-id="319d9-127">The problematic line of code is highlighted and followed by an `error` \(`x`\) button.</span></span>  <span data-ttu-id="319d9-128">Pour afficher le `Failed to load resource: the server responded with a status of 404 ()` message d’erreur, choisissez le bouton **d’erreur** `x` \( \).</span><span class="sxs-lookup"><span data-stu-id="319d9-128">To display the `Failed to load resource: the server responded with a status of 404 ()` error message, choose the **error** \(`x`\) button.</span></span>  


:::row:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-code-line.msft.png" alt-text="Choisissez le lien vers la page web et le code dans lequel l’erreur se produit ouvre l’outil Sources" lightbox="../media/console-debug-network-error-code-line.msft.png":::
         <span data-ttu-id="319d9-130">Choisissez le lien vers la page web et le code dans lequel l’erreur se produit ouvre **l’outil Sources**</span><span class="sxs-lookup"><span data-stu-id="319d9-130">Choose the link to the webpage and code where the error occurs line opens the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/console-debug-network-error-sources.msft.png" alt-text="Pour rechercher l’erreur dans JavaScript, utilisez l’outil Sources" lightbox="../media/console-debug-network-error-sources.msft.png":::
         <span data-ttu-id="319d9-132">Pour rechercher l’erreur dans JavaScript, utilisez **l’outil Sources**</span><span class="sxs-lookup"><span data-stu-id="319d9-132">To find the error in JavaScript, use the **Sources** tool</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="319d9-133">Dans l’exemple, l’erreur vous informe que l’URL demandée est in trouvée.</span><span class="sxs-lookup"><span data-stu-id="319d9-133">In the example, the error informs you that the requested URL isn't found.</span></span>  <span data-ttu-id="319d9-134">Ensuite, terminez les actions suivantes pour ouvrir **l’outil** Réseau.</span><span class="sxs-lookup"><span data-stu-id="319d9-134">Next, complete the following actions to open the **Network** tool.</span></span>  

1.  <span data-ttu-id="319d9-135">Ouvrez la **console.**</span><span class="sxs-lookup"><span data-stu-id="319d9-135">Open the **Console**.</span></span>  
1.  <span data-ttu-id="319d9-136">Choisissez l’URI associé à l’erreur.</span><span class="sxs-lookup"><span data-stu-id="319d9-136">Choose the URI associated with the error.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-url.msft.png" alt-text="La console affiche un code d’état HTTP de l’erreur après qu’une ressource n’est pas chargée" lightbox="../media/console-debug-network-error-url.msft.png":::
   <span data-ttu-id="319d9-138">**La console** affiche un code d’état HTTP de l’erreur après qu’une ressource n’est pas chargée</span><span class="sxs-lookup"><span data-stu-id="319d9-138">**Console** displays an HTTP status code of the error after a resource isn't loaded</span></span>  
:::image-end:::  

:::row:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network.msft.png" alt-text="L’outil Réseau affiche plus d’informations sur la demande qui a échoué" lightbox="../media/console-debug-network-error-network.msft.png":::
           <span data-ttu-id="319d9-140">**L’outil** Réseau affiche plus d’informations sur la demande qui a échoué</span><span class="sxs-lookup"><span data-stu-id="319d9-140">The **Network** tool displays more information about the failed request</span></span>  
        :::image-end:::  
    :::column-end:::
    :::column:::
        :::image type="complex" source="../media/console-debug-network-error-network-detail.msft.png" alt-text="L’inspection des en-têtes dans l’outil Réseau peut donner plus d’informations" lightbox="../media/console-debug-network-error-network-detail.msft.png":::
           <span data-ttu-id="319d9-142">L’inspection des en-têtes dans **l’outil** Réseau peut donner plus d’informations</span><span class="sxs-lookup"><span data-stu-id="319d9-142">Inspect the headers in the **Network** tool may give more insight</span></span>  
        :::image-end:::  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="319d9-143">Quel était le problème ?</span><span class="sxs-lookup"><span data-stu-id="319d9-143">What was the problem?</span></span>  <span data-ttu-id="319d9-144">Deux barres obliques \( `//` \) se produisent dans l’URI demandé après le `repos` mot.</span><span class="sxs-lookup"><span data-stu-id="319d9-144">Two slash characters \(`//`\) occur in the requested URI after the word `repos`.</span></span>  <span data-ttu-id="319d9-145">Ouvrez **l’outil Sources** et inspectez la ligne 26.</span><span class="sxs-lookup"><span data-stu-id="319d9-145">Open the **Sources** tool and inspect line 26.</span></span>  <span data-ttu-id="319d9-146">Une barre oblique finale \( \) se produit à la fin de `/` l’URI de base.</span><span class="sxs-lookup"><span data-stu-id="319d9-146">A trailing slash character \(`/`\) occurs at the end of the base URI.</span></span>  

:::image type="complex" source="../media/console-debug-network-error-code-error.msft.png" alt-text="L’outil Sources affiche la ligne de code avec l’erreur" lightbox="../media/console-debug-network-error-code-error.msft.png":::
   <span data-ttu-id="319d9-148">**L’outil Sources** affiche la ligne de code avec l’erreur</span><span class="sxs-lookup"><span data-stu-id="319d9-148">The **Sources** tool displays the line of code with the error</span></span>  
:::image-end:::  

<span data-ttu-id="319d9-149">Pour passer en revue aucune erreur dans la **console,** accédez à [Erreur réseau fixe signalée dans la console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span><span class="sxs-lookup"><span data-stu-id="319d9-149">To review no errors in the **Console**, navigate to [Fixed network error reported in Console][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml].</span></span>  

:::image type="complex" source="../media/console-debug-network-error-fixed.msft.png" alt-text="L’exemple sans erreur charge les informations de GitHub et les affiche" lightbox="../media/console-debug-network-error-fixed.msft.png":::
   <span data-ttu-id="319d9-151">L’exemple sans erreur charge les informations de GitHub et les affiche</span><span class="sxs-lookup"><span data-stu-id="319d9-151">The example without any errors loads information from GitHub and displays it</span></span>  
:::image-end:::  

<span data-ttu-id="319d9-152">Veillez à fournir des techniques de codage conviviales pour éviter les expériences utilisateur précédentes.</span><span class="sxs-lookup"><span data-stu-id="319d9-152">Ensure you provide defensive coding techniques to avoid the previous user experiences.</span></span>  <span data-ttu-id="319d9-153">Assurez-vous également que votre code capture les erreurs et affiche chacune d’elles dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="319d9-153">Also, ensure your code catches errors and display each in the **Console**.</span></span>  <span data-ttu-id="319d9-154">Accédez au [rapport d’erreurs réseau dans la console et l’interface][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] utilisateur et examinez les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="319d9-154">Navigate to [Network error reporting in Console and UI][GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml] and review the following items.</span></span>  

*   <span data-ttu-id="319d9-155">Fournissez une interface utilisateur à l’utilisateur pour qu’un problème se soit passé.</span><span class="sxs-lookup"><span data-stu-id="319d9-155">Provide UI to the user that something went wrong.</span></span>  
*   <span data-ttu-id="319d9-156">Dans la **console,** fournissez des informations utiles sur l’erreur réseau à partir de votre code.</span><span class="sxs-lookup"><span data-stu-id="319d9-156">In the **Console**, provide helpful information about the Network error from your code.</span></span>  
    
:::image type="complex" source="../media/console-debug-network-error-report.msft.png" alt-text="Exemple qui capture et signale les erreurs" lightbox="../media/console-debug-network-error-report.msft.png":::
   <span data-ttu-id="319d9-158">Exemple qui capture et signale les erreurs</span><span class="sxs-lookup"><span data-stu-id="319d9-158">An example that catches and reports errors</span></span>  
:::image-end:::  

<span data-ttu-id="319d9-159">L’extrait de code suivant capture et signale les erreurs à l’aide de la `handleErrors` méthode, en particulier la `throw Error` ligne.</span><span class="sxs-lookup"><span data-stu-id="319d9-159">The following code snippet catches and reports errors using the `handleErrors` method, specifically the `throw Error` line.</span></span>  

```javascript
const handleErrors = (response) => {
    if (!response.ok) {
        let message = 'Could not load the information'
        document.querySelector('tbody').innerHTML = `
        <tr><td colspan=3>Error ${message}</td></tr>
        `;
        throw Error(response.status + ' ' + response.statusText);
    }
    return response;
};
```  

## <a name="create-errors-and-traces-in-the-console"></a><span data-ttu-id="319d9-160">Créer des erreurs et des suivis dans la console</span><span class="sxs-lookup"><span data-stu-id="319d9-160">Create errors and traces in the Console</span></span>

<span data-ttu-id="319d9-161">Outre l’exemple de la section précédente, vous pouvez également créer différentes erreurs et problèmes de `throw Error` suivi dans la **console.**</span><span class="sxs-lookup"><span data-stu-id="319d9-161">Besides the `throw Error` example in the previous section, you may also create different errors and trace problems in the **Console**.</span></span>  
<span data-ttu-id="319d9-162">Pour afficher deux messages d’erreur créés dans la **console,** accédez à Création de rapports d’erreurs et [d’assertions dans la console.][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]</span><span class="sxs-lookup"><span data-stu-id="319d9-162">To display two created error messages in the **Console**, navigate to [Creating error reports and assertions in Console][GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml].</span></span>  

:::image type="complex" source="../media/console-debug-error-assert.msft.png" alt-text="Messages d’erreur créés à partir de la console" lightbox="../media/console-debug-error-assert.msft.png":::
   <span data-ttu-id="319d9-164">Messages d’erreur créés à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="319d9-164">Error messages created from **Console**</span></span>  
:::image-end:::  

<span data-ttu-id="319d9-165">L’extrait de code suivant a été utilisé dans l’exemple précédent.</span><span class="sxs-lookup"><span data-stu-id="319d9-165">The following code snippet was used in the previous example.</span></span>  

```javascript
function first(name) { second(name); }
function second(name) { third(name); }
function third(name) {
    if (!name) {
        console.error(`Name isn't defined :(`)
    } else {
        console.assert(
            name.length <= 8, 
            `"${name} is not less than eight letters"`
        );
    }
}
first();
first('Console');
first('Microsoft Edge Canary');
```  

<span data-ttu-id="319d9-166">Vous avez trois fonctions qui se demandent l’une l’autre successivement.</span><span class="sxs-lookup"><span data-stu-id="319d9-166">You have three functions that request each other in succession.</span></span>  

*   `first()`  
*   `second()`  
*   `third()`  
    
<span data-ttu-id="319d9-167">Chacun envoie un `name` argument à l’autre.</span><span class="sxs-lookup"><span data-stu-id="319d9-167">Each sends a `name` argument to the other.</span></span>  <span data-ttu-id="319d9-168">Dans la fonction, vous vérifiez si l’argument existe et, si ce n’est pas le cas, vous enregistrez une erreur qui `third()` `name` n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="319d9-168">In the `third()` function, you check if the `name` argument exists and if it doesn't, you log an error that name isn't defined.</span></span>  <span data-ttu-id="319d9-169">Si `name` elle est définie, vous utilisez la méthode pour vérifier si `assert()` `name` l’argument a une longueur de moins de huit lettres.</span><span class="sxs-lookup"><span data-stu-id="319d9-169">If `name` is defined, you use the `assert()` method to check if the `name` argument is fewer than eight letters long.</span></span>  <span data-ttu-id="319d9-170">Vous demandez la `first()` fonction trois fois, avec les paramètres suivants.</span><span class="sxs-lookup"><span data-stu-id="319d9-170">You request the `first()` function three times, with the following parameters.</span></span>  

*   <span data-ttu-id="319d9-171">Aucun argument qui déclenche la `console.error()` méthode dans la `third()` fonction.</span><span class="sxs-lookup"><span data-stu-id="319d9-171">No argument that triggers the `console.error()` method in the `third()` function.</span></span>  
*   <span data-ttu-id="319d9-172">Le terme en tant que paramètre de la fonction ne provoque pas d’erreur, car l’argument existe et est `Console` plus court que huit `first()` `name` lettres.</span><span class="sxs-lookup"><span data-stu-id="319d9-172">The term `Console` as a parameter to the `first()` function doesn't cause an error because `name` argument exists and is shorter than eight letters.</span></span>  
*   <span data-ttu-id="319d9-173">L’expression en tant que paramètre pour fonctionner entraîne le signalement d’une erreur par la méthode, car le paramètre `Microsoft Edge Canary` est plus de huit `first()` `console.assert()` lettres.</span><span class="sxs-lookup"><span data-stu-id="319d9-173">The phrase `Microsoft Edge Canary` as a parameter to `first()` function causes the `console.assert()` method to report an error, because the parameter is longer than eight letters.</span></span>  
    
<span data-ttu-id="319d9-174">Utilisez la méthode `console.assert()` pour créer des rapports d’erreurs conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="319d9-174">Use the `console.assert()` method to create conditional error reports.</span></span>  <span data-ttu-id="319d9-175">Les deux exemples suivants ont le même résultat, mais l’un d’entre vous a besoin d’une `if{}` instruction supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="319d9-175">The following two examples have the same result, but one needs an extra `if{}` statement.</span></span>  

```javascript
let x = 20;
if (x < 40) { console.error(`${x} is too small`) };
console.assert(x >= 40, `${x} is too small`) 
```  

> [!IMPORTANT]
> <span data-ttu-id="319d9-176">Les deuxième et troisième lignes du code effectuent le même test.</span><span class="sxs-lookup"><span data-stu-id="319d9-176">The second and third lines of the code perform the same test.</span></span>  <span data-ttu-id="319d9-177">Étant donné que l’assertion doit enregistrer un résultat négatif, vous devez la tester `x < 40` dans la cas et pour `if` `x >= 40` l’assertion.</span><span class="sxs-lookup"><span data-stu-id="319d9-177">Because the assertion needs to record a negative result, you test for `x < 40` in the `if` case and `x >= 40` for the assertion.</span></span>  

<span data-ttu-id="319d9-178">Si vous ne savez pas quelle fonction demande une autre fonction, utilisez la méthode pour suivre les fonctions qui sont `console.trace()` demandées pour obtenir la fonction actuelle.</span><span class="sxs-lookup"><span data-stu-id="319d9-178">If you aren't sure which function requests another function, use the `console.trace()` method to track which functions are requested to get to the current one.</span></span>  <span data-ttu-id="319d9-179">Pour afficher le suivi dans la **console,** accédez à [Création de suivis dans la console.][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]</span><span class="sxs-lookup"><span data-stu-id="319d9-179">To display the trace in the **Console**, navigate to [Creating traces in Console][GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml].</span></span>  

```javascript
function here() {there()}
function there() {everywhere()}
function everywhere() {
    console.trace();
}
here();
there();
```  

<span data-ttu-id="319d9-180">Le résultat est un suivi à afficher qui est nommé, puis dans le `here()` `there()` deuxième exemple `everywhere()` qu’il est nommé `everywhere()` .</span><span class="sxs-lookup"><span data-stu-id="319d9-180">The result is a trace to display that `here()` is named `there()` and then `everywhere()` and in the second example that it's named `everywhere()`.</span></span>  

:::image type="complex" source="../media/console-debug-trace.msft.png" alt-text="Suivi créé à partir de la console" lightbox="../media/console-debug-trace.msft.png":::
   <span data-ttu-id="319d9-182">Suivi créé à partir de la **console**</span><span class="sxs-lookup"><span data-stu-id="319d9-182">A trace created from **Console**</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="319d9-183">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="319d9-183">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamplesConsoleErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error.html "Erreur JavaScript signalée dans l’outil console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleErrorAssertHtml]: https://microsoftedge.github.io/DevToolsSamples/console/error-assert.html "Création de rapports d’erreurs et d’assertions dans console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error.html "Erreur réseau signalée dans console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorFixedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-fixed.html "Erreur réseau corrigée signalée dans console | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleNetworkErrorReportedHtml]: https://microsoftedge.github.io/DevToolsSamples/console/network-error-reported.html "Rapport d’erreurs réseau dans la console et l’interface | GitHub"  
[GithubMicrosoftedgeDevtoolssamplesConsoleTraceHtml]: https://microsoftedge.github.io/DevToolsSamples/console/trace.html "Création de suivis dans la console | GitHub"  
