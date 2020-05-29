---
title: Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581816"
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





# <span data-ttu-id="55ad0-103">Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="55ad0-103">Run Snippets Of JavaScript On Any Page With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="55ad0-104">Si vous vous trouvez vous utilisez le même code dans la [console][DevtoolsConsoleIndex] à plusieurs reprises, envisagez plutôt d’enregistrer le code en tant qu’extrait.</span><span class="sxs-lookup"><span data-stu-id="55ad0-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="55ad0-105">Les extraits sont des scripts que vous créez dans le [panneau **sources** ][DevToolsSourcesPanel].</span><span class="sxs-lookup"><span data-stu-id="55ad0-105">Snippets are scripts that you author in the [**Sources** panel][DevToolsSourcesPanel].</span></span>  <span data-ttu-id="55ad0-106">Ils ont accès au contexte JavaScript de la page et vous pouvez les exécuter sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="55ad0-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="55ad0-107">Les extraits de vue sont une alternative aux [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="55ad0-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="55ad0-108">Firefox DevTools possède une fonctionnalité semblable à celle des extraits de blocs- [Notes][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="55ad0-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="55ad0-109">Par exemple, la [**figure 1**](#figure-1) montre la page d’accueil devtools sur la gauche et le code source de l’extrait de code à droite.</span><span class="sxs-lookup"><span data-stu-id="55ad0-109">For example, [**Figure 1**](#figure-1) shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

> ##### <span data-ttu-id="55ad0-110">Figure1</span><span class="sxs-lookup"><span data-stu-id="55ad0-110">Figure 1</span></span>  
> <span data-ttu-id="55ad0-111">Aspect de la page avant d’exécuter l’extrait de page</span><span class="sxs-lookup"><span data-stu-id="55ad0-111">How the page looks before running the Snippet</span></span>  
> ![Aspect de la page avant d’exécuter l’extrait de page][ImageSnippetSplitScreen]  

<span data-ttu-id="55ad0-113">L’extrait de code source de la [**figure 1**](#figure-1):</span><span class="sxs-lookup"><span data-stu-id="55ad0-113">The Snippet source code from [**Figure 1**](#figure-1):</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="55ad0-114">La [**figure 2**](#figure-2) montre à quoi ressemble la page après avoir exécuté l’extrait de méthode.</span><span class="sxs-lookup"><span data-stu-id="55ad0-114">[**Figure 2**](#figure-2) shows how the page looks after running the Snippet.</span></span>  <span data-ttu-id="55ad0-115">Le **tiroir** de la console s’affiche pour afficher le `Hello, Snippets!` message indiquant que le Snippet enregistre les journaux et le contenu de la page est totalement modifié.</span><span class="sxs-lookup"><span data-stu-id="55ad0-115">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

> ##### <span data-ttu-id="55ad0-116">Figure 2</span><span class="sxs-lookup"><span data-stu-id="55ad0-116">Figure 2</span></span>  
> <span data-ttu-id="55ad0-117">Aspect de la page après avoir exécuté l’extrait</span><span class="sxs-lookup"><span data-stu-id="55ad0-117">How the page looks after running the Snippet</span></span>  
> ![Aspect de la page après avoir exécuté l’extrait][ImageSnippetSplitScreenAfter]  

## <span data-ttu-id="55ad0-119">Ouvrir le volet d’extraits</span><span class="sxs-lookup"><span data-stu-id="55ad0-119">Open the Snippets pane</span></span>   

<span data-ttu-id="55ad0-120">Le volet d' **extraits** de liste répertorie vos extraits.</span><span class="sxs-lookup"><span data-stu-id="55ad0-120">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="55ad0-121">Lorsque vous voulez modifier un extrait de rapport, vous devez l’ouvrir à partir du volet **extraits** .</span><span class="sxs-lookup"><span data-stu-id="55ad0-121">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

> ##### <span data-ttu-id="55ad0-122">Figure3</span><span class="sxs-lookup"><span data-stu-id="55ad0-122">Figure 3</span></span>  
> <span data-ttu-id="55ad0-123">Volet **snippets**</span><span class="sxs-lookup"><span data-stu-id="55ad0-123">The **Snippets** pane</span></span>  
> ![Volet Snippets][ImageSnippetsPane]  

### <span data-ttu-id="55ad0-125">Ouvrir le volet des fragments de fenêtre à l’aide d’une souris</span><span class="sxs-lookup"><span data-stu-id="55ad0-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="55ad0-126">Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="55ad0-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="55ad0-127">Le volet **page** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="55ad0-127">The **Page** pane usually opens by default.</span></span>  

    > ##### <span data-ttu-id="55ad0-128">Figure 4</span><span class="sxs-lookup"><span data-stu-id="55ad0-128">Figure 4</span></span>  
    > <span data-ttu-id="55ad0-129">Panneau **sources** avec le volet **page** ouvert à gauche</span><span class="sxs-lookup"><span data-stu-id="55ad0-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    > ![Panneau sources avec le volet page ouvert à gauche][ImageSourcesPageEmpty]  

1.  <span data-ttu-id="55ad0-131">Cliquez sur l’onglet **extraits** de vue pour ouvrir le volet d' **extraits** .</span><span class="sxs-lookup"><span data-stu-id="55ad0-131">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="55ad0-132">Vous devrez peut-être cliquer sur **autres onglets** pour ![ ][ImageMoreTabsIcon] accéder à l’option **extraits** de vue.</span><span class="sxs-lookup"><span data-stu-id="55ad0-132">You might need to click **More Tabs** ![More Tabs][ImageMoreTabsIcon] in order to access the **Snippets** option.</span></span>  

### <span data-ttu-id="55ad0-133">Ouvrir le volet d’extraits de fenêtre à l’aide du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="55ad0-133">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="55ad0-134">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="55ad0-134">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="55ad0-135">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="55ad0-135">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="55ad0-136">Commencez `Snippets` à taper, sélectionnez **afficher les extraits**de texte, puis appuyez sur `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="55ad0-136">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="55ad0-137">Figure 5</span><span class="sxs-lookup"><span data-stu-id="55ad0-137">Figure 5</span></span>  
    > <span data-ttu-id="55ad0-138">Commande **afficher les extraits**</span><span class="sxs-lookup"><span data-stu-id="55ad0-138">The **Show Snippets** command</span></span>  
    > ![Commande Afficher les extraits][ImageShowSnippetsSearch]  

## <span data-ttu-id="55ad0-140">Créer des extraits de</span><span class="sxs-lookup"><span data-stu-id="55ad0-140">Create Snippets</span></span>   

### <span data-ttu-id="55ad0-141">Créer un snippet via le volet sources</span><span class="sxs-lookup"><span data-stu-id="55ad0-141">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="55ad0-142">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="55ad0-142">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="55ad0-143">Cliquez sur **nouvel extrait**.</span><span class="sxs-lookup"><span data-stu-id="55ad0-143">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="55ad0-144">Entrez le nom de votre snippet, puis appuyez sur `Enter` Enregistrer.</span><span class="sxs-lookup"><span data-stu-id="55ad0-144">Enter a name for your Snippet then press `Enter` to save.</span></span>  

    > ##### <span data-ttu-id="55ad0-145">Figure 6</span><span class="sxs-lookup"><span data-stu-id="55ad0-145">Figure 6</span></span>  
    > <span data-ttu-id="55ad0-146">Attribution d’un nom à un snippet</span><span class="sxs-lookup"><span data-stu-id="55ad0-146">Naming a Snippet</span></span>  
    > ![Attribution d’un nom à un snippet][ImageSnippetName]  

### <span data-ttu-id="55ad0-148">Créer un snippet via le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="55ad0-148">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="55ad0-149">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="55ad0-149">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="55ad0-150">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="55ad0-150">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="55ad0-151">Commencez `Snippet` à taper, sélectionnez **créer un nouveau Snippet**, puis appuyez sur `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="55ad0-151">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  

    > ##### <span data-ttu-id="55ad0-152">Figure 7</span><span class="sxs-lookup"><span data-stu-id="55ad0-152">Figure 7</span></span>  
    > <span data-ttu-id="55ad0-153">Commande de création d’un nouveau Snippet</span><span class="sxs-lookup"><span data-stu-id="55ad0-153">The command for creating a new Snippet</span></span>  
    > ![Commande de création d’un nouveau Snippet][ImageCreateSnippetSearch]  

<span data-ttu-id="55ad0-155">Voir [Renommer des extraits de nom](#rename-snippets) si vous souhaitez attribuer un nom personnalisé à votre nouveau snippet.</span><span class="sxs-lookup"><span data-stu-id="55ad0-155">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="55ad0-156">Modifier des extraits de ce profil</span><span class="sxs-lookup"><span data-stu-id="55ad0-156">Edit Snippets</span></span>   

1.  <span data-ttu-id="55ad0-157">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="55ad0-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="55ad0-158">Dans le volet d' **extraits** de code, cliquez sur le nom de l’extrait que vous souhaitez modifier pour l’ouvrir dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="55ad0-158">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  

    > ##### <span data-ttu-id="55ad0-159">Figure8</span><span class="sxs-lookup"><span data-stu-id="55ad0-159">Figure 8</span></span>  
    > <span data-ttu-id="55ad0-160">Éditeur de code</span><span class="sxs-lookup"><span data-stu-id="55ad0-160">The Code Editor</span></span>  
    > ![Éditeur de code][ImageSnippetEditor]  

1.  <span data-ttu-id="55ad0-162">Utilisez l' **éditeur de code** pour ajouter du JavaScript à votre snippet.</span><span class="sxs-lookup"><span data-stu-id="55ad0-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="55ad0-163">Lorsqu’un astérisque apparaît en regard du nom de votre snippet, cela signifie que vous avez du code non enregistré.</span><span class="sxs-lookup"><span data-stu-id="55ad0-163">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="55ad0-164">Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.</span><span class="sxs-lookup"><span data-stu-id="55ad0-164">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  

    > ##### <span data-ttu-id="55ad0-165">Figure9</span><span class="sxs-lookup"><span data-stu-id="55ad0-165">Figure 9</span></span>  
    > <span data-ttu-id="55ad0-166">Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré.</span><span class="sxs-lookup"><span data-stu-id="55ad0-166">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    > ![Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré.][ImageUnsavedSnippet]  

## <span data-ttu-id="55ad0-168">Exécuter des Snippets</span><span class="sxs-lookup"><span data-stu-id="55ad0-168">Run Snippets</span></span>   

### <span data-ttu-id="55ad0-169">Exécuter un snippet à partir du panneau sources</span><span class="sxs-lookup"><span data-stu-id="55ad0-169">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="55ad0-170">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="55ad0-170">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="55ad0-171">Cliquez sur le nom de l’extrait que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="55ad0-171">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="55ad0-172">L’extrait de code s’ouvre dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="55ad0-172">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="55ad0-173">Cliquez sur **exécuter** l’extrait ![ ][ImageRunSnippetIcon] de snippet, ou appuyez sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="55ad0-173">Click **Run Snippet** ![Run Snippet][ImageRunSnippetIcon], or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  

### <span data-ttu-id="55ad0-174">Exécuter un extrait de commande avec le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="55ad0-174">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="55ad0-175">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="55ad0-175">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="55ad0-176">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="55ad0-176">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="55ad0-177">Supprimez le `>` caractère et tapez le `!` caractère suivi du nom de l’extrait que vous voulez exécuter.</span><span class="sxs-lookup"><span data-stu-id="55ad0-177">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  

    > ##### <span data-ttu-id="55ad0-178">Figure10</span><span class="sxs-lookup"><span data-stu-id="55ad0-178">Figure 10</span></span>  
    > <span data-ttu-id="55ad0-179">Exécution d’un snippet à partir du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="55ad0-179">Running a Snippet from the Command Menu</span></span>  
    > ![Exécution d’un snippet à partir du menu de commandes][ImageRunSnippetCommand]  

1.  <span data-ttu-id="55ad0-181">Appuyez `Enter` pour exécuter l’extrait de.</span><span class="sxs-lookup"><span data-stu-id="55ad0-181">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="55ad0-182">Renommer des extraits de nom</span><span class="sxs-lookup"><span data-stu-id="55ad0-182">Rename Snippets</span></span>   

1.  <span data-ttu-id="55ad0-183">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="55ad0-183">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="55ad0-184">Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="55ad0-184">Right-click the Snippet name and select **Rename**.</span></span>  

## <span data-ttu-id="55ad0-185">Supprimer des extraits de</span><span class="sxs-lookup"><span data-stu-id="55ad0-185">Delete Snippets</span></span>   

1.  <span data-ttu-id="55ad0-186">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="55ad0-186">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="55ad0-187">Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="55ad0-187">Right-click the Snippet name and select **Remove**.</span></span>  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Figure 1: apparence de la page avant de l’exécuter"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Figure 2: aspect de la page après avoir exécuté l’extrait"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Figure 3: volet Snippets"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Figure 4: volet de sources avec le volet de pages ouvert à gauche"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Figure 5: commande Afficher les extraits"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Figure 6: nommer un snippet"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Figure 7: commande de création d’un nouveau Snippet"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Figure 8: éditeur de code"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Figure 9: un astérisque en regard du nom de l’extrait de code, qui indique le code non enregistré."  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Figure 10: exécution d’un snippet à partir du menu de commandes"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console"  
[DevToolsSourcesPanel]: ../sources.md "Présentation du panneau sources"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc-notes | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="55ad0-202">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="55ad0-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="55ad0-203">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="55ad0-203">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="55ad0-205">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="55ad0-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
