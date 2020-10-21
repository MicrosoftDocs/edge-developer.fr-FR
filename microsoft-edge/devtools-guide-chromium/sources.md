---
description: Afficher et modifier des fichiers, créer des extraits de code, déboguer JavaScript et configurer des espaces de travail dans le panneau sources de Microsoft Edge DevTools.
title: Vue d’ensemble du volet Sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 971ee6e112daaba828a8b754b63eee73ea51e99e
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125327"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <span data-ttu-id="53165-104">Vue d’ensemble du volet Sources</span><span class="sxs-lookup"><span data-stu-id="53165-104">Sources panel overview</span></span>  

<span data-ttu-id="53165-105">Utilisez le volet de **sources** de Microsoft Edge devtools pour effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="53165-105">Use the Microsoft Edge DevTools **Sources** panel to perform the following actions.</span></span>  

*   <span data-ttu-id="53165-106">[Afficher les fichiers](#view-files).</span><span class="sxs-lookup"><span data-stu-id="53165-106">[View files](#view-files).</span></span>  
*   <span data-ttu-id="53165-107">[Modifiez les feuilles CSS et JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="53165-107">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="53165-108">[Créez et enregistrez des **extraits** de code JavaScript](#create-save-and-run-snippets), que vous pouvez exécuter sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="53165-108">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="53165-109">Les **extraits** sont similaires aux bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="53165-109">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="53165-110">[Déboguer JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="53165-110">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="53165-111">[Configurez un espace de travail](#set-up-a-workspace)de telle sorte que les modifications que vous apportez dans devtools soient enregistrées dans le code de votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="53165-111">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  
    
## <span data-ttu-id="53165-112">Afficher les fichiers</span><span class="sxs-lookup"><span data-stu-id="53165-112">View files</span></span>  

<span data-ttu-id="53165-113">Utilisez le volet **page** pour afficher toutes les ressources que la page a chargées.</span><span class="sxs-lookup"><span data-stu-id="53165-113">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

:::image type="complex" source="./media/sources-page-pane.msft.png" alt-text="Volet pages" lightbox="./media/sources-page-pane.msft.png":::
   <span data-ttu-id="53165-115">Volet **pages**</span><span class="sxs-lookup"><span data-stu-id="53165-115">The **Page** pane</span></span>  
:::image-end:::  

<span data-ttu-id="53165-116">Organisation de la **page** :</span><span class="sxs-lookup"><span data-stu-id="53165-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="53165-117">Le niveau supérieur, tel que `top` dans l’illustration précédente, représente un [cadre html][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="53165-117">The top-level, such as `top` in the previous figure, represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="53165-118">Recherchez `top` sur chaque page visitée.</span><span class="sxs-lookup"><span data-stu-id="53165-118">Find `top` on every page that you visit.</span></span>  `top` <span data-ttu-id="53165-119">représente le cadre du document principal.</span><span class="sxs-lookup"><span data-stu-id="53165-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="53165-120">Le second niveau, tel que `docs.microsoft.com` dans l’illustration précédente, représente une [origine][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="53165-120">The second-level, such as `docs.microsoft.com` in the previous figure, represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="53165-121">Le troisième niveau, le quatrième niveau, etc., représentent les répertoires et les ressources qui ont été chargés depuis cette origine.</span><span class="sxs-lookup"><span data-stu-id="53165-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="53165-122">Par exemple, dans l’illustration précédente, le chemin d’accès complet à la ressource `devtools-guide-chromium` est</span><span class="sxs-lookup"><span data-stu-id="53165-122">For example, in the previous figure the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  
    
<span data-ttu-id="53165-123">Cliquez sur un fichier dans le volet de **page** pour afficher le contenu dans le volet **éditeur** .</span><span class="sxs-lookup"><span data-stu-id="53165-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="53165-124">Il est possible que vous voyiez un type de fichier.</span><span class="sxs-lookup"><span data-stu-id="53165-124">You may view any type of file.</span></span>  <span data-ttu-id="53165-125">Pour les images, un aperçu de l’image est affiché.</span><span class="sxs-lookup"><span data-stu-id="53165-125">For images, a preview of the image is displayed.</span></span>  

:::image type="complex" source="./media/sources-editor-pane.msft.png" alt-text="Volet pages" lightbox="./media/sources-editor-pane.msft.png":::
   <span data-ttu-id="53165-127">Afficher le contenu de `a4d10f71.index-docs.js` dans le volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="53165-127">View the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="53165-128">Modifier CSS et JavaScript</span><span class="sxs-lookup"><span data-stu-id="53165-128">Edit CSS and JavaScript</span></span>  

<span data-ttu-id="53165-129">Utilisez le volet **éditeur** pour modifier les feuilles CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="53165-129">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="53165-130">DevTools met à jour la page pour exécuter votre nouveau code.</span><span class="sxs-lookup"><span data-stu-id="53165-130">DevTools updates the page to run your new code.</span></span>  <span data-ttu-id="53165-131">Par exemple, si vous modifiez un fichier CSS en ajoutant la règle de style ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="53165-131">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="53165-132">Cette modification doit prendre effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="53165-132">That change should take effect immediately.</span></span>

:::image type="complex" source="./media/edit-css.msft.png" alt-text="Volet pages" lightbox="./media/edit-css.msft.png":::
   <span data-ttu-id="53165-134">Modification de CSS dans le volet **éditeur** pour changer la couleur du texte du sous-titre en rouge</span><span class="sxs-lookup"><span data-stu-id="53165-134">Edit CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
:::image-end:::  

<span data-ttu-id="53165-135">Les modifications apportées aux feuilles de style CSS sont immédiatement appliquées, sans enregistrement nécessaires.</span><span class="sxs-lookup"><span data-stu-id="53165-135">CSS changes take effect immediately, no save needed.</span></span>  <span data-ttu-id="53165-136">Pour que les modifications JavaScript soient prises en compte, sélectionnez `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="53165-136">For JavaScript changes to take effect, select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\).</span></span>  <span data-ttu-id="53165-137">DevTools ne réexécute pas de script, les seules modifications JavaScript qui prennent effet sont celles que vous effectuez dans les fonctions.</span><span class="sxs-lookup"><span data-stu-id="53165-137">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="53165-138">Par exemple, dans l’illustration suivante, vous remarquerez que le fonctionnement `console.log('A')` ne fonctionne pas `console.log('B')` .</span><span class="sxs-lookup"><span data-stu-id="53165-138">For example, in the following figure, notice how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span>  <span data-ttu-id="53165-139">Si DevTools réexécute le script entier après avoir apporté la modification, le texte `A` aurait été enregistré dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="53165-139">If DevTools re-runs the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

:::image type="complex" source="./media/edit-js.msft.png" alt-text="Volet pages" lightbox="./media/edit-js.msft.png":::
   <span data-ttu-id="53165-141">Modification de JavaScript dans le volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="53165-141">Editing JavaScript in the **Editor** pane</span></span>  
:::image-end:::  

<span data-ttu-id="53165-142">DevTools efface vos modifications CSS et JavaScript lorsque vous rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="53165-142">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span>  <span data-ttu-id="53165-143">Naviguez jusqu’à [configurer un espace de travail](#set-up-a-workspace) pour découvrir comment enregistrer les modifications apportées à votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="53165-143">Navigate to [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="53165-144">Création, enregistrement et exécution d’extraits de fichier</span><span class="sxs-lookup"><span data-stu-id="53165-144">Create, save, and run Snippets</span></span>  

<span data-ttu-id="53165-145">Les extraits sont des scripts que vous pouvez exécuter sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="53165-145">Snippets are scripts which you may run on any page.</span></span>  <span data-ttu-id="53165-146">Imaginez que vous entrez le code suivant à plusieurs reprises dans la **console**pour insérer la bibliothèque jQuery dans une page, de sorte que vous puissiez exécuter des commandes jQuery à partir de la **console**:</span><span class="sxs-lookup"><span data-stu-id="53165-146">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="53165-147">Au lieu de cela, vous pouvez enregistrer ce code dans un **extrait** de code et l’exécuter en quelques clics sur le bouton, chaque fois que vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="53165-147">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="53165-148">DevTools enregistre l' **extrait** de fichier dans votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="53165-148">DevTools saves the **Snippet** to your file system.</span></span>  

:::image type="complex" source="./media/snippet.msft.png" alt-text="Volet pages" lightbox="./media/snippet.msft.png":::
   <span data-ttu-id="53165-150">**Extrait** de la bibliothèque jQuery insérée dans une page</span><span class="sxs-lookup"><span data-stu-id="53165-150">A **Snippet** that inserts the jQuery library into a page</span></span>  
:::image-end:::  

<span data-ttu-id="53165-151">Pour exécuter un **Snippet**:</span><span class="sxs-lookup"><span data-stu-id="53165-151">To run a **Snippet**:</span></span>

*   <span data-ttu-id="53165-152">Ouvrez le fichier à l’aide du volet **snippets** , puis sélectionnez **exécuter** \ ( ![ bouton exécuter ][ImageRunIcon] \).</span><span class="sxs-lookup"><span data-stu-id="53165-152">Open the file using the **Snippets** pane, and choose **Run** \(![The Run button][ImageRunIcon]\).</span></span>  
*   <span data-ttu-id="53165-153">Ouvrez le **[menu de commandes][DevtoolsGuideChromiumCommandMenuIndex]**, supprimez le `>` caractère, tapez `!` le nom de votre **extrait**de texte, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="53165-153">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then select `Enter`.</span></span>  
    
<span data-ttu-id="53165-154">Pour plus d’informations, accédez à [exécuter des extraits de code à partir de n’importe quelle page][DevtoolsGuideChromiumJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="53165-154">Navigate to [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>

## <span data-ttu-id="53165-155">Déboguer JavaScript</span><span class="sxs-lookup"><span data-stu-id="53165-155">Debug JavaScript</span></span>  

<span data-ttu-id="53165-156">Au lieu `console.log()` d’utiliser pour induire l’endroit où votre code JavaScript ne pose pas de problème, envisagez plutôt d’utiliser les outils de débogage de Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="53165-156">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span>  <span data-ttu-id="53165-157">L’idée générale consiste à définir un point d’arrêt, qui est un point d’arrêt intentionnel dans votre code, et à parcourir le runtime de votre code, une ligne à la fois.</span><span class="sxs-lookup"><span data-stu-id="53165-157">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span>  <span data-ttu-id="53165-158">Lorsque vous parcourez le code, vous pouvez afficher et modifier les valeurs de toutes les propriétés et variables actuellement définies, exécuter JavaScript dans la **console**, etc.</span><span class="sxs-lookup"><span data-stu-id="53165-158">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="53165-159">Pour plus d’informations sur le débogage dans DevTools, accédez à la section [commencer le débogage][DevtoolsGuideChromiumJavascriptIndex] .</span><span class="sxs-lookup"><span data-stu-id="53165-159">Navigate to [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

:::image type="complex" source="./media/debugging.msft.png" alt-text="Volet pages" lightbox="./media/debugging.msft.png":::
   <span data-ttu-id="53165-161">Déboguer JavaScript</span><span class="sxs-lookup"><span data-stu-id="53165-161">Debug JavaScript</span></span>  
:::image-end:::  

## <span data-ttu-id="53165-162">Configurer un espace de travail</span><span class="sxs-lookup"><span data-stu-id="53165-162">Set up a Workspace</span></span>  

<span data-ttu-id="53165-163">Par défaut, lorsque vous modifiez un fichier dans le panneau **sources** , les modifications correspondantes sont perdues lorsque vous rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="53165-163">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="53165-164">Les **espaces de travail** vous permettent d’enregistrer les modifications que vous apportez dans devtools à votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="53165-164">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="53165-165">Fondamentalement, DevTools peut être utilisé en tant qu’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="53165-165">Essentially, DevTools is able to be used as your code editor.</span></span>

<span data-ttu-id="53165-166">Accédez à l' [édition de fichiers avec des espaces de travail][DevtoolsGuideChromiumWorkspacesIndex] pour commencer.</span><span class="sxs-lookup"><span data-stu-id="53165-166">Navigate to [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

## <span data-ttu-id="53165-167">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="53165-167">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRunIcon]: ./media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: ./command-menu/index.md "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: ./javascript/index.md "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: ./javascript/snippets.md "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: ./workspaces/index.md "Modifier des fichiers avec des espaces de travail"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origine-norme HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Images | W3C"  

> [!NOTE]
> <span data-ttu-id="53165-174">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="53165-174">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="53165-175">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/sources) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="53165-175">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="53165-177">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="53165-177">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
