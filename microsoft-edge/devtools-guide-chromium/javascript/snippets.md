---
title: Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3a5ae986e3080a0b6a8b1bf34b0e0efc44c90303
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981994"
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





# <span data-ttu-id="69a9e-103">Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="69a9e-103">Run snippets of JavaScript on any page with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="69a9e-104">Si vous vous trouvez vous utilisez le même code dans la [console][DevtoolsConsoleIndex] à plusieurs reprises, envisagez plutôt d’enregistrer le code en tant qu’extrait.</span><span class="sxs-lookup"><span data-stu-id="69a9e-104">If you find yourself running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="69a9e-105">Les extraits sont des scripts que vous créez dans le panneau [sources][DevToolsSourcesPanel] .</span><span class="sxs-lookup"><span data-stu-id="69a9e-105">Snippets are scripts that you author in the [Sources][DevToolsSourcesPanel] panel.</span></span>  <span data-ttu-id="69a9e-106">Ils ont accès au contexte JavaScript de la page et vous pouvez les exécuter sur n’importe quelle page.</span><span class="sxs-lookup"><span data-stu-id="69a9e-106">They have access to the JavaScript context of the page, and you can run them on any page.</span></span>  <span data-ttu-id="69a9e-107">Les extraits de vue sont une alternative aux [bookmarklets][WikiBookmarklet].</span><span class="sxs-lookup"><span data-stu-id="69a9e-107">Snippets are an alternative to [bookmarklets][WikiBookmarklet].</span></span>  
<span data-ttu-id="69a9e-108">Firefox DevTools possède une fonctionnalité semblable à celle des extraits de blocs- [Notes][MDNScratchpad].</span><span class="sxs-lookup"><span data-stu-id="69a9e-108">Firefox DevTools has a feature similar to Snippets called [Scratchpad][MDNScratchpad].</span></span>  

<span data-ttu-id="69a9e-109">Par exemple, dans la figure suivante, la page d’accueil DevTools sur la gauche et le code source de l’extrait de code à droite.</span><span class="sxs-lookup"><span data-stu-id="69a9e-109">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Aspect de la page avant d’exécuter l’extrait de page" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   <span data-ttu-id="69a9e-111">Aspect de la page avant d’exécuter l’extrait de page</span><span class="sxs-lookup"><span data-stu-id="69a9e-111">How the page looks before running the Snippet</span></span>  
:::image-end:::  

<span data-ttu-id="69a9e-112">Code source de l’extrait de code de la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="69a9e-112">The Snippet source code from the previous figure.</span></span>  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

<span data-ttu-id="69a9e-113">Dans l’illustration suivante, la page s’affiche après l’exécution de l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="69a9e-113">In the following figure, the page appears after running the Snippet.</span></span>  <span data-ttu-id="69a9e-114">Le **tiroir** de la console s’affiche pour afficher le `Hello, Snippets!` message indiquant que le Snippet enregistre les journaux et le contenu de la page est totalement modifié.</span><span class="sxs-lookup"><span data-stu-id="69a9e-114">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the page changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Aspect de la page après avoir exécuté l’extrait" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="69a9e-116">Aspect de la page après avoir exécuté l’extrait</span><span class="sxs-lookup"><span data-stu-id="69a9e-116">How the page looks after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="69a9e-117">Ouvrir le volet d’extraits</span><span class="sxs-lookup"><span data-stu-id="69a9e-117">Open the Snippets pane</span></span>   

<span data-ttu-id="69a9e-118">Le volet d' **extraits** de liste répertorie vos extraits.</span><span class="sxs-lookup"><span data-stu-id="69a9e-118">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="69a9e-119">Lorsque vous voulez modifier un extrait de rapport, vous devez l’ouvrir à partir du volet **extraits** .</span><span class="sxs-lookup"><span data-stu-id="69a9e-119">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Volet Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="69a9e-121">Volet **snippets**</span><span class="sxs-lookup"><span data-stu-id="69a9e-121">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="69a9e-122">Ouvrir le volet des fragments de fenêtre à l’aide d’une souris</span><span class="sxs-lookup"><span data-stu-id="69a9e-122">Open the Snippets pane with a mouse</span></span>   

1.  <span data-ttu-id="69a9e-123">Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="69a9e-123">Click the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="69a9e-124">Le volet **page** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="69a9e-124">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Panneau sources avec le volet page ouvert à gauche" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="69a9e-126">Panneau **sources** avec le volet **page** ouvert à gauche</span><span class="sxs-lookup"><span data-stu-id="69a9e-126">The **Sources** panel with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69a9e-127">Cliquez sur l’onglet **extraits** de vue pour ouvrir le volet d' **extraits** .</span><span class="sxs-lookup"><span data-stu-id="69a9e-127">Click the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="69a9e-128">Vous devrez peut-être cliquer sur **autres onglets** \ ( ![ plus d’onglets ][ImageMoreTabsIcon] \) pour accéder à l’option **extraits** de vue.</span><span class="sxs-lookup"><span data-stu-id="69a9e-128">You might need to click **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) in order to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="69a9e-129">Ouvrir le volet d’extraits de fenêtre à l’aide du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="69a9e-129">Open the Snippets pane with the Command Menu</span></span>   

1.  <span data-ttu-id="69a9e-130">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="69a9e-130">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="69a9e-131">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="69a9e-131">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="69a9e-132">Commencez `Snippets` à taper, sélectionnez **afficher les extraits**de texte, puis appuyez sur `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="69a9e-132">Start typing `Snippets`, select **Show Snippets**, and then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Commande Afficher les extraits" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="69a9e-134">Commande **afficher les extraits**</span><span class="sxs-lookup"><span data-stu-id="69a9e-134">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="69a9e-135">Créer des extraits de</span><span class="sxs-lookup"><span data-stu-id="69a9e-135">Create Snippets</span></span>   

### <span data-ttu-id="69a9e-136">Créer un snippet via le volet sources</span><span class="sxs-lookup"><span data-stu-id="69a9e-136">Create a Snippet through the Sources panel</span></span>   

1.  <span data-ttu-id="69a9e-137">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="69a9e-137">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="69a9e-138">Cliquez sur **nouvel extrait**.</span><span class="sxs-lookup"><span data-stu-id="69a9e-138">Click **New snippet**.</span></span>  
1.  <span data-ttu-id="69a9e-139">Entrez le nom de votre snippet, puis appuyez sur `Enter` Enregistrer.</span><span class="sxs-lookup"><span data-stu-id="69a9e-139">Enter a name for your Snippet then press `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nommer un snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="69a9e-141">Nommer un snippet</span><span class="sxs-lookup"><span data-stu-id="69a9e-141">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="69a9e-142">Créer un snippet via le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="69a9e-142">Create a Snippet through the Command Menu</span></span>   

1.  <span data-ttu-id="69a9e-143">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="69a9e-143">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="69a9e-144">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="69a9e-144">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="69a9e-145">Commencez `Snippet` à taper, sélectionnez **créer un nouveau Snippet**, puis appuyez sur `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="69a9e-145">Start typing `Snippet`, select **Create new snippet**, then press `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Commande de création d’un nouveau Snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="69a9e-147">Commande de création d’un nouveau Snippet</span><span class="sxs-lookup"><span data-stu-id="69a9e-147">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="69a9e-148">Voir [Renommer des extraits de nom](#rename-snippets) si vous souhaitez attribuer un nom personnalisé à votre nouveau snippet.</span><span class="sxs-lookup"><span data-stu-id="69a9e-148">See [Rename Snippets](#rename-snippets) if you'd like to give your new Snippet a custom name.</span></span>  

## <span data-ttu-id="69a9e-149">Modifier des extraits de ce profil</span><span class="sxs-lookup"><span data-stu-id="69a9e-149">Edit Snippets</span></span>   

1.  <span data-ttu-id="69a9e-150">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="69a9e-150">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="69a9e-151">Dans le volet d' **extraits** de code, cliquez sur le nom de l’extrait que vous souhaitez modifier pour l’ouvrir dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="69a9e-151">In the **Snippets** pane click the name of the Snippet that you want to edit in order to open it in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Éditeur de code" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="69a9e-153">**Éditeur de code**</span><span class="sxs-lookup"><span data-stu-id="69a9e-153">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69a9e-154">Utilisez l' **éditeur de code** pour ajouter du JavaScript à votre snippet.</span><span class="sxs-lookup"><span data-stu-id="69a9e-154">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="69a9e-155">Lorsqu’un astérisque apparaît en regard du nom de votre snippet, cela signifie que vous avez du code non enregistré.</span><span class="sxs-lookup"><span data-stu-id="69a9e-155">When an asterisk appears next to the name of your Snippet it means you have unsaved code.</span></span> <span data-ttu-id="69a9e-156">Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.</span><span class="sxs-lookup"><span data-stu-id="69a9e-156">Press `Control`+`S` \(Windows\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="69a9e-158">Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré.</span><span class="sxs-lookup"><span data-stu-id="69a9e-158">An asterisk next to the Snippet name, which indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="69a9e-159">Exécuter des Snippets</span><span class="sxs-lookup"><span data-stu-id="69a9e-159">Run Snippets</span></span>   

### <span data-ttu-id="69a9e-160">Exécuter un snippet à partir du panneau sources</span><span class="sxs-lookup"><span data-stu-id="69a9e-160">Run a Snippet from the Sources panel</span></span>   

1.  <span data-ttu-id="69a9e-161">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="69a9e-161">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="69a9e-162">Cliquez sur le nom de l’extrait que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="69a9e-162">Click the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="69a9e-163">L’extrait de code s’ouvre dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="69a9e-163">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="69a9e-164">Cliquez sur **exécuter le Snippet** \ (exécuter l’extrait de passe ![ ][ImageRunSnippetIcon] \) ou appuyez sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="69a9e-164">Click **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or press `Control`+`Enter` \(Windows\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="69a9e-165">Exécuter un extrait de commande avec le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="69a9e-165">Run a Snippet with the Command Menu</span></span>   

1.  <span data-ttu-id="69a9e-166">Focalisez votre curseur à l’intérieur du DevTools.</span><span class="sxs-lookup"><span data-stu-id="69a9e-166">Focus your cursor somewhere inside of DevTools.</span></span>  
1.  <span data-ttu-id="69a9e-167">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="69a9e-167">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="69a9e-168">Supprimez le `>` caractère et tapez le `!` caractère suivi du nom de l’extrait que vous voulez exécuter.</span><span class="sxs-lookup"><span data-stu-id="69a9e-168">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Exécution d’un snippet à partir du menu de commandes" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="69a9e-170">Exécution d’un snippet à partir du **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="69a9e-170">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="69a9e-171">Appuyez `Enter` pour exécuter l’extrait de.</span><span class="sxs-lookup"><span data-stu-id="69a9e-171">Press `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="69a9e-172">Renommer des extraits de nom</span><span class="sxs-lookup"><span data-stu-id="69a9e-172">Rename Snippets</span></span>   

1.  <span data-ttu-id="69a9e-173">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="69a9e-173">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="69a9e-174">Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="69a9e-174">Right-click the Snippet name and select **Rename**.</span></span>  
    
## <span data-ttu-id="69a9e-175">Supprimer des extraits de</span><span class="sxs-lookup"><span data-stu-id="69a9e-175">Delete Snippets</span></span>   

1.  <span data-ttu-id="69a9e-176">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="69a9e-176">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="69a9e-177">Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="69a9e-177">Right-click the Snippet name and select **Remove**.</span></span>  
    
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
> <span data-ttu-id="69a9e-182">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69a9e-182">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="69a9e-183">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="69a9e-183">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="69a9e-185">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="69a9e-185">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
