---
description: Les extraits sont des petits scripts que vous pouvez créer et exécuter dans le panneau sources de Microsoft Edge DevTools.  Vous pouvez y accéder et l’exécuter à partir de n’importe quelle page.  Lorsque vous exécutez un snippet, il s’exécute à partir du contexte de la page actuellement ouverte.
title: Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5f6284179aacb471116a2d732507b010c37ef235
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993386"
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





# <span data-ttu-id="e141b-106">Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="e141b-106">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="e141b-107">Si vous vous trouvez vous utilisez le même code dans la [console][DevtoolsConsoleIndex] à plusieurs reprises, envisagez plutôt d’enregistrer le code en tant qu’extrait.</span><span class="sxs-lookup"><span data-stu-id="e141b-107">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="e141b-108">Les extraits sont des scripts que vous créez dans le panneau [sources][DevToolsSourcesPanel] .</span><span class="sxs-lookup"><span data-stu-id="e141b-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="e141b-109">Ils ont accès au contexte JavaScript de la page et vous pouvez les exécuter sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="e141b-109">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="e141b-110">Les extraits de vue sont une alternative aux [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="e141b-110">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="e141b-111">Firefox DevTools possède une fonctionnalité semblable à celle des extraits de blocs- [Notes][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="e141b-111">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="e141b-112">Par exemple, dans la figure suivante, la page d’accueil DevTools sur la gauche et le code source de l’extrait de code à droite.</span><span class="sxs-lookup"><span data-stu-id="e141b-112">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aspect de la page avant d’exécuter l’extrait de page" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="e141b-114">Aspect de la page avant d’exécuter l’extrait de page</span><span class="sxs-lookup"><span data-stu-id="e141b-114">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="e141b-115">Code source de l’extrait de code de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="e141b-115">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="e141b-116">Dans l’illustration suivante, la page s’affiche après l’exécution de l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="e141b-116">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="e141b-117">Le **tiroir** de la console s’affiche pour afficher le `Hello, Snippets!` message indiquant que le Snippet enregistre les journaux et le contenu de la page est totalement modifié.</span><span class="sxs-lookup"><span data-stu-id="e141b-117">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aspect de la page après avoir exécuté l’extrait" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="e141b-119">Aspect de la page après avoir exécuté l’extrait</span><span class="sxs-lookup"><span data-stu-id="e141b-119">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="e141b-120">Ouvrir le volet d’extraits</span><span class="sxs-lookup"><span data-stu-id="e141b-120">Open the Snippets pane</span></span>   

<span data-ttu-id="e141b-121">Le volet d' **extraits** de liste répertorie vos extraits.</span><span class="sxs-lookup"><span data-stu-id="e141b-121">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="e141b-122">Lorsque vous voulez modifier un extrait de rapport, vous devez l’ouvrir à partir du volet **extraits** .</span><span class="sxs-lookup"><span data-stu-id="e141b-122">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Volet Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="e141b-124">Volet **snippets**</span><span class="sxs-lookup"><span data-stu-id="e141b-124">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="e141b-125">Ouvrir le volet des fragments de fenêtre à l’aide d’une souris</span><span class="sxs-lookup"><span data-stu-id="e141b-125">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="e141b-126">Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="e141b-126">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="e141b-127">Le volet **page** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="e141b-127">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Panneau sources avec le volet page ouvert à gauche" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="e141b-129">Panneau **sources** avec le volet **page** ouvert à gauche</span><span class="sxs-lookup"><span data-stu-id="e141b-129">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e141b-130">Cliquez sur l’onglet **extraits** de vue pour ouvrir le volet d' **extraits** .</span><span class="sxs-lookup"><span data-stu-id="e141b-130">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="e141b-131">Vous devrez peut-être cliquer sur **autres onglets** \ ( ![ plus d’onglets ][ImageMoreTabsIcon] \) pour accéder à l’option **extraits** de vue.</span><span class="sxs-lookup"><span data-stu-id="e141b-131">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="e141b-132">Ouvrir le volet d’extraits de fenêtre à l’aide du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="e141b-132">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="e141b-133">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="e141b-133">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="e141b-134">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="e141b-134">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="e141b-135">Commencez `Snippets` à taper, sélectionnez **afficher les extraits**de texte, puis appuyez sur `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="e141b-135">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Commande Afficher les extraits" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="e141b-137">Commande **afficher les extraits**</span><span class="sxs-lookup"><span data-stu-id="e141b-137">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e141b-138">Créer des extraits de</span><span class="sxs-lookup"><span data-stu-id="e141b-138">Create Snippets</span></span>   

### <span data-ttu-id="e141b-139">Créer un snippet via le volet sources</span><span class="sxs-lookup"><span data-stu-id="e141b-139">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="e141b-140">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e141b-140">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e141b-141">Cliquez sur **nouvel extrait**.</span><span class="sxs-lookup"><span data-stu-id="e141b-141">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="e141b-142">Entrez le nom de votre snippet, puis appuyez sur `Enter` Enregistrer.</span><span class="sxs-lookup"><span data-stu-id="e141b-142">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nommer un snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="e141b-144">Nommer un snippet</span><span class="sxs-lookup"><span data-stu-id="e141b-144">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="e141b-145">Créer un snippet via le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="e141b-145">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="e141b-146">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="e141b-146">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="e141b-147">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="e141b-147">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="e141b-148">Commencez `Snippet` à taper, sélectionnez **créer un nouveau Snippet**, puis appuyez sur `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="e141b-148">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Commande de création d’un nouveau Snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="e141b-150">Commande de création d’un nouveau Snippet</span><span class="sxs-lookup"><span data-stu-id="e141b-150">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="e141b-151">Voir [Renommer des extraits de nom](#rename-snippets) si vous souhaitez attribuer un nom personnalisé à votre nouveau snippet.</span><span class="sxs-lookup"><span data-stu-id="e141b-151">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="e141b-152">Modifier des extraits de ce profil</span><span class="sxs-lookup"><span data-stu-id="e141b-152">Edit Snippets</span></span>   

1.  <span data-ttu-id="e141b-153">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e141b-153">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e141b-154">Dans le volet d' **extraits** de code, cliquez sur le nom de l’extrait que vous souhaitez modifier pour l’ouvrir dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="e141b-154">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Éditeur de code" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="e141b-156">**Éditeur de code**</span><span class="sxs-lookup"><span data-stu-id="e141b-156">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e141b-157">Utilisez l' **éditeur de code** pour ajouter du JavaScript à votre snippet.</span><span class="sxs-lookup"><span data-stu-id="e141b-157">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="e141b-158">Lorsqu’un astérisque apparaît en regard du nom de votre snippet, cela signifie que vous avez du code non enregistré.</span><span class="sxs-lookup"><span data-stu-id="e141b-158">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="e141b-159">Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.</span><span class="sxs-lookup"><span data-stu-id="e141b-159">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="e141b-161">Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré.</span><span class="sxs-lookup"><span data-stu-id="e141b-161">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e141b-162">Exécuter des Snippets</span><span class="sxs-lookup"><span data-stu-id="e141b-162">Run Snippets</span></span>   

### <span data-ttu-id="e141b-163">Exécuter un snippet à partir du panneau sources</span><span class="sxs-lookup"><span data-stu-id="e141b-163">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="e141b-164">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e141b-164">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e141b-165">Cliquez sur le nom de l’extrait que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="e141b-165">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="e141b-166">L’extrait de code s’ouvre dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="e141b-166">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="e141b-167">Cliquez sur **exécuter le Snippet** \ (exécuter l’extrait de passe ![ ][ImageRunSnippetIcon] \) ou appuyez sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="e141b-167">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="e141b-168">Exécuter un extrait de commande avec le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="e141b-168">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="e141b-169">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="e141b-169">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="e141b-170">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="e141b-170">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="e141b-171">Supprimez le `>` caractère et tapez le `!` caractère suivi du nom de l’extrait que vous voulez exécuter.</span><span class="sxs-lookup"><span data-stu-id="e141b-171">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Exécution d’un snippet à partir du menu de commandes" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="e141b-173">Exécution d’un snippet à partir du **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="e141b-173">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e141b-174">Appuyez `Enter` pour exécuter l’extrait de.</span><span class="sxs-lookup"><span data-stu-id="e141b-174">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="e141b-175">Renommer des extraits de nom</span><span class="sxs-lookup"><span data-stu-id="e141b-175">Rename Snippets</span></span>   

1.  <span data-ttu-id="e141b-176">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e141b-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e141b-177">Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="e141b-177">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="e141b-178">Supprimer des extraits de</span><span class="sxs-lookup"><span data-stu-id="e141b-178">Delete Snippets</span></span>   

1.  <span data-ttu-id="e141b-179">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="e141b-179">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="e141b-180">Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="e141b-180">Right-click the Snippet name and select **Remove**.</span></span>  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Présentation du panneau sources | Documents Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc-notes | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="e141b-185">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e141b-185">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e141b-186">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="e141b-186">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="e141b-188">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e141b-188">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
