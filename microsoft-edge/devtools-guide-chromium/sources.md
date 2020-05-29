---
title: Présentation du panneau sources
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601907"
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
   limitations under the License. -->






# <span data-ttu-id="101dd-103">Présentation du panneau sources</span><span class="sxs-lookup"><span data-stu-id="101dd-103">Sources Panel Overview</span></span> 



<span data-ttu-id="101dd-104">Utilisez le volet de **sources** de Microsoft Edge devtools pour:</span><span class="sxs-lookup"><span data-stu-id="101dd-104">Use the Microsoft Edge DevTools **Sources** panel to:</span></span>

*   <span data-ttu-id="101dd-105">[Afficher les fichiers](#view-files).</span><span class="sxs-lookup"><span data-stu-id="101dd-105">[View files](#view-files).</span></span>  
*   <span data-ttu-id="101dd-106">[Modifiez les feuilles CSS et JavaScript](#edit-css-and-javascript).</span><span class="sxs-lookup"><span data-stu-id="101dd-106">[Edit CSS and JavaScript](#edit-css-and-javascript).</span></span>  
*   <span data-ttu-id="101dd-107">[Créez et enregistrez des **extraits** de code JavaScript](#create-save-and-run-snippets), que vous pouvez exécuter sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="101dd-107">[Create and save **Snippets** of JavaScript](#create-save-and-run-snippets), which you may run on any page.</span></span>  <span data-ttu-id="101dd-108">Les **extraits** sont similaires aux bookmarklets.</span><span class="sxs-lookup"><span data-stu-id="101dd-108">**Snippets** are similar to bookmarklets.</span></span>  
*   <span data-ttu-id="101dd-109">[Déboguer JavaScript](#debug-javascript).</span><span class="sxs-lookup"><span data-stu-id="101dd-109">[Debug JavaScript](#debug-javascript).</span></span>  
*   <span data-ttu-id="101dd-110">[Configurez un espace de travail](#set-up-a-workspace)de telle sorte que les modifications que vous apportez dans devtools soient enregistrées dans le code de votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="101dd-110">[Set up a Workspace](#set-up-a-workspace), so that changes you make in DevTools get saved to the code on your file system.</span></span>  

## <span data-ttu-id="101dd-111">Afficher les fichiers</span><span class="sxs-lookup"><span data-stu-id="101dd-111">View files</span></span> 

<span data-ttu-id="101dd-112">Utilisez le volet **page** pour afficher toutes les ressources que la page a chargées.</span><span class="sxs-lookup"><span data-stu-id="101dd-112">Use the **Page** pane to view all of the resources that the page has loaded.</span></span>

> ##### <span data-ttu-id="101dd-113">Figure1</span><span class="sxs-lookup"><span data-stu-id="101dd-113">Figure 1</span></span>  
> <span data-ttu-id="101dd-114">Volet **pages**</span><span class="sxs-lookup"><span data-stu-id="101dd-114">The **Page** pane</span></span>  
> ![Figure 1: volet pages][ImageSourcesPagePane]  

<span data-ttu-id="101dd-116">Organisation de la **page** :</span><span class="sxs-lookup"><span data-stu-id="101dd-116">How the **Page** pane is organized:</span></span>  
*   <span data-ttu-id="101dd-117">Le niveau supérieur, tel que `top` dans la [**figure 1**](#figure-1), représente un [cadre html][W3CHtml4Frames].</span><span class="sxs-lookup"><span data-stu-id="101dd-117">The top-level, such as `top` in [**Figure 1**](#figure-1), represents an [HTML frame][W3CHtml4Frames].</span></span>  <span data-ttu-id="101dd-118">Recherchez `top` sur chaque page visitée.</span><span class="sxs-lookup"><span data-stu-id="101dd-118">Find `top` on every page that you visit.</span></span> `top` <span data-ttu-id="101dd-119">représente le cadre du document principal.</span><span class="sxs-lookup"><span data-stu-id="101dd-119">represents the main document frame.</span></span>  
*   <span data-ttu-id="101dd-120">Le second niveau, tel que `docs.microsoft.com` dans la [**figure 1**](#figure-1), représente une [origine][HtmlstandardOrigin].</span><span class="sxs-lookup"><span data-stu-id="101dd-120">The second-level, such as `docs.microsoft.com` in [**Figure 1**](#figure-1), represents an [origin][HtmlstandardOrigin].</span></span>  
*   <span data-ttu-id="101dd-121">Le troisième niveau, le quatrième niveau, etc., représentent les répertoires et les ressources qui ont été chargés depuis cette origine.</span><span class="sxs-lookup"><span data-stu-id="101dd-121">The third-level, fourth-level, and so on, represent directories and resources that were loaded from that origin.</span></span>  <span data-ttu-id="101dd-122">Par exemple, dans la [**figure 1**](#figure-1) le chemin complet de la ressource `devtools-guide-chromium` est</span><span class="sxs-lookup"><span data-stu-id="101dd-122">For example, in [**Figure 1**](#figure-1) the full path to the resource `devtools-guide-chromium` is</span></span> `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

<span data-ttu-id="101dd-123">Cliquez sur un fichier dans le volet de **page** pour afficher le contenu dans le volet **éditeur** .</span><span class="sxs-lookup"><span data-stu-id="101dd-123">Click a file in the **Page** pane to view the contents in the **Editor** pane.</span></span>  <span data-ttu-id="101dd-124">Il est possible que vous voyiez un type de fichier.</span><span class="sxs-lookup"><span data-stu-id="101dd-124">You may view any type of file.</span></span> <span data-ttu-id="101dd-125">Pour les images, un aperçu de l’image s’affiche.</span><span class="sxs-lookup"><span data-stu-id="101dd-125">For images, you see a preview of the image.</span></span>  

> ##### <span data-ttu-id="101dd-126">Figure 2</span><span class="sxs-lookup"><span data-stu-id="101dd-126">Figure 2</span></span>  
> <span data-ttu-id="101dd-127">Affichage du contenu de `a4d10f71.index-docs.js` dans le volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="101dd-127">Viewing the contents of `a4d10f71.index-docs.js` in the **Editor** pane</span></span>  
> ![Figure2.][ImageSourcesEditorPane]  

## <span data-ttu-id="101dd-130">Modifier CSS et JavaScript</span><span class="sxs-lookup"><span data-stu-id="101dd-130">Edit CSS and JavaScript</span></span> 

<span data-ttu-id="101dd-131">Utilisez le volet **éditeur** pour modifier les feuilles CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="101dd-131">Use the **Editor** pane to edit CSS and JavaScript.</span></span>  <span data-ttu-id="101dd-132">DevTools met à jour la page pour exécuter votre nouveau code.</span><span class="sxs-lookup"><span data-stu-id="101dd-132">DevTools updates the page to run your new code.</span></span> <span data-ttu-id="101dd-133">Par exemple, si vous modifiez un fichier CSS en ajoutant la règle de style ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="101dd-133">For example, if you edit a CSS file by adding the style rule below:</span></span>

```css
.metadata.page-metadata {
    color: red;
}
```

<span data-ttu-id="101dd-134">Vous devez voir que cette modification prend effet immédiatement.</span><span class="sxs-lookup"><span data-stu-id="101dd-134">You should see that change take effect immediately.</span></span>

> ##### <span data-ttu-id="101dd-135">Figure3</span><span class="sxs-lookup"><span data-stu-id="101dd-135">Figure 3</span></span>  
> <span data-ttu-id="101dd-136">Modification de feuilles de style en cascade dans le volet **éditeur** pour changer la couleur du texte du sous-titre en rouge</span><span class="sxs-lookup"><span data-stu-id="101dd-136">Editing CSS in the **Editor** pane to change the text color of the subtitle to red</span></span>  
> ![Figure3.][ImageEditCSS]  

<span data-ttu-id="101dd-139">Les modifications apportées aux feuilles de style CSS sont immédiatement appliquées, sans enregistrement nécessaires.</span><span class="sxs-lookup"><span data-stu-id="101dd-139">CSS changes take effect immediately, no save needed.</span></span> <span data-ttu-id="101dd-140">Pour que les modifications JavaScript soient prises en compte, appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="101dd-140">For JavaScript changes to take effect, press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\).</span></span> <span data-ttu-id="101dd-141">DevTools ne réexécute pas de script, les seules modifications JavaScript qui prennent effet sont celles que vous effectuez dans les fonctions.</span><span class="sxs-lookup"><span data-stu-id="101dd-141">DevTools does not re-run a script, so the only JavaScript changes that take effect are those that you make inside of functions.</span></span>  <span data-ttu-id="101dd-142">Par exemple, dans la [**figure 4**](#figure-4) Notez `console.log('A')` que le fonctionnement ne s’exécute pas `console.log('B')` .</span><span class="sxs-lookup"><span data-stu-id="101dd-142">For example, in [**Figure 4**](#figure-4) note how `console.log('A')` does not run, whereas `console.log('B')` does.</span></span> <span data-ttu-id="101dd-143">Si DevTools réexécute le script entier après avoir apporté la modification, le texte `A` aurait été enregistré dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="101dd-143">If DevTools re-ran the entire script after making the change, then the text `A` would have been logged to the **Console**.</span></span>  

> ##### <span data-ttu-id="101dd-144">Figure 4</span><span class="sxs-lookup"><span data-stu-id="101dd-144">Figure 4</span></span>  
> <span data-ttu-id="101dd-145">Modification de JavaScript dans le volet **éditeur**</span><span class="sxs-lookup"><span data-stu-id="101dd-145">Editing JavaScript in the **Editor** pane</span></span>  
> ![Figure4.][ImageEditJS]  

<span data-ttu-id="101dd-148">DevTools efface vos modifications CSS et JavaScript lorsque vous rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="101dd-148">DevTools erases your CSS and JavaScript changes when you reload the page.</span></span> <span data-ttu-id="101dd-149">Pour savoir comment enregistrer les modifications apportées à votre système de fichiers, voir [configurer un espace de travail](#set-up-a-workspace) .</span><span class="sxs-lookup"><span data-stu-id="101dd-149">See [Set up a Workspace](#set-up-a-workspace) to learn how to save the changes to your file system.</span></span>  

## <span data-ttu-id="101dd-150">Création, enregistrement et exécution d’extraits de fichier</span><span class="sxs-lookup"><span data-stu-id="101dd-150">Create, save, and run Snippets</span></span> 

<span data-ttu-id="101dd-151">Les extraits sont des scripts que vous pouvez exécuter sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="101dd-151">Snippets are scripts which you may run on any page.</span></span> <span data-ttu-id="101dd-152">Imaginez que vous entrez le code suivant à plusieurs reprises dans la **console**pour insérer la bibliothèque jQuery dans une page, de sorte que vous puissiez exécuter des commandes jQuery à partir de la **console**:</span><span class="sxs-lookup"><span data-stu-id="101dd-152">Imagine that you repeatedly type out the following code in the **Console**, in order to insert the jQuery library into a page, so that you may run jQuery commands from the **Console**:</span></span>  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

<span data-ttu-id="101dd-153">Au lieu de cela, vous pouvez enregistrer ce code dans un **extrait** de code et l’exécuter en quelques clics sur le bouton, chaque fois que vous en avez besoin.</span><span class="sxs-lookup"><span data-stu-id="101dd-153">Instead, you may save this code in a **Snippet** and run it with a couple of button clicks, any time you need it.</span></span>  <span data-ttu-id="101dd-154">DevTools enregistre l' **extrait** de fichier dans votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="101dd-154">DevTools saves the **Snippet** to your file system.</span></span>  

> ##### <span data-ttu-id="101dd-155">Figure 5</span><span class="sxs-lookup"><span data-stu-id="101dd-155">Figure 5</span></span>  
> <span data-ttu-id="101dd-156">**Extrait** de la bibliothèque jQuery insérée dans une page</span><span class="sxs-lookup"><span data-stu-id="101dd-156">A **Snippet** that inserts the jQuery library into a page</span></span>  
> ![Figure5.][ImageSnippet]  

<span data-ttu-id="101dd-159">Pour exécuter un **Snippet**:</span><span class="sxs-lookup"><span data-stu-id="101dd-159">To run a **Snippet**:</span></span>

*   <span data-ttu-id="101dd-160">Ouvrez le fichier via le volet **snippets** , puis cliquez sur **exécuter** ![ le bouton exécuter ][ImageRunIcon] .</span><span class="sxs-lookup"><span data-stu-id="101dd-160">Open the file via the **Snippets** pane, and click **Run** ![The Run button][ImageRunIcon].</span></span>  
*   <span data-ttu-id="101dd-161">Ouvrez le **[menu de commandes][DevtoolsGuideChromiumCommandMenuIndex]**, supprimez le `>` caractère, tapez `!` le nom de votre **extrait**de texte, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="101dd-161">Open the **[Command Menu][DevtoolsGuideChromiumCommandMenuIndex]**, delete the `>` character, type `!`, type the name of your **Snippet**, then press `Enter`.</span></span>  

<span data-ttu-id="101dd-162">Pour en savoir plus, voir [exécution d’extraits de code à partir de n’importe quelle page][DevtoolsGuideChromiumJavascriptSnippets] .</span><span class="sxs-lookup"><span data-stu-id="101dd-162">See [Run Snippets Of Code From Any Page][DevtoolsGuideChromiumJavascriptSnippets] to learn more.</span></span>


## <span data-ttu-id="101dd-163">Déboguer JavaScript</span><span class="sxs-lookup"><span data-stu-id="101dd-163">Debug JavaScript</span></span> 

<span data-ttu-id="101dd-164">Au lieu `console.log()` d’utiliser pour induire l’endroit où votre code JavaScript ne pose pas de problème, envisagez plutôt d’utiliser les outils de débogage de Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="101dd-164">Rather than using `console.log()` to infer where your JavaScript is going wrong, consider using the Microsoft Edge DevTools debugging tools, instead.</span></span> <span data-ttu-id="101dd-165">L’idée générale consiste à définir un point d’arrêt, qui est un point d’arrêt intentionnel dans votre code, et à parcourir le runtime de votre code, une ligne à la fois.</span><span class="sxs-lookup"><span data-stu-id="101dd-165">The general idea is to set a breakpoint, which is an intentional stopping place in your code, and then step through the runtime of your code, one line at a time.</span></span> <span data-ttu-id="101dd-166">Lorsque vous parcourez le code, vous pouvez afficher et modifier les valeurs de toutes les propriétés et variables actuellement définies, exécuter JavaScript dans la **console**, etc.</span><span class="sxs-lookup"><span data-stu-id="101dd-166">As you step through the code, you may view and change the values of all currently-defined properties and variables, run JavaScript in the **Console**, and more.</span></span>

<span data-ttu-id="101dd-167">Pour plus d’informations sur les concepts de base du débogage dans DevTools, voir [prendre en main le débogage de code JavaScript][DevtoolsGuideChromiumJavascriptIndex] .</span><span class="sxs-lookup"><span data-stu-id="101dd-167">See [Get Started With Debugging JavaScript][DevtoolsGuideChromiumJavascriptIndex] to learn the basics of debugging in DevTools.</span></span>

> ##### <span data-ttu-id="101dd-168">Figure 6</span><span class="sxs-lookup"><span data-stu-id="101dd-168">Figure 6</span></span>  
> <span data-ttu-id="101dd-169">Débogage de JavaScript</span><span class="sxs-lookup"><span data-stu-id="101dd-169">Debugging JavaScript</span></span>  
> ![Figure6.][ImageDebugging]  

## <span data-ttu-id="101dd-172">Configurer un espace de travail</span><span class="sxs-lookup"><span data-stu-id="101dd-172">Set up a Workspace</span></span> 

<span data-ttu-id="101dd-173">Par défaut, lorsque vous modifiez un fichier dans le panneau **sources** , les modifications correspondantes sont perdues lorsque vous rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="101dd-173">By default, when you edit a file in the **Sources** panel, those changes are lost when you reload the page.</span></span>  <span data-ttu-id="101dd-174">Les **espaces de travail** vous permettent d’enregistrer les modifications que vous apportez dans devtools à votre système de fichiers.</span><span class="sxs-lookup"><span data-stu-id="101dd-174">**Workspaces** enable you to save the changes that you make in DevTools to your file system.</span></span>  <span data-ttu-id="101dd-175">Fondamentalement, cela vous permet d’utiliser DevTools en tant qu’éditeur de code.</span><span class="sxs-lookup"><span data-stu-id="101dd-175">Essentially, this lets you use DevTools as your code editor.</span></span>

<span data-ttu-id="101dd-176">Pour commencer, voir [modifier des fichiers avec des espaces de travail][DevtoolsGuideChromiumWorkspacesIndex] .</span><span class="sxs-lookup"><span data-stu-id="101dd-176">See [Edit Files With Workspaces][DevtoolsGuideChromiumWorkspacesIndex] to get started.</span></span>

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Figure 1: volet pages"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Figure 2: affichage du contenu de a4d10f71. index-docs. js dans le volet éditeur"  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Figure 3: modifier la couleur du texte du sous-titre en rouge"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Figure 4: modification de JavaScript dans le volet éditeur"  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Figure 5: extrait de la bibliothèque jQuery qui est insérée dans une page"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Figure 6: débogage de JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Commencer à utiliser le débogage JavaScript dans Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Modifier des fichiers avec des espaces de travail"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Origine-norme HTML"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Images | W3C"  

> [!NOTE]
> <span data-ttu-id="101dd-189">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="101dd-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="101dd-190">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/sources) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="101dd-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/sources) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="101dd-192">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="101dd-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
