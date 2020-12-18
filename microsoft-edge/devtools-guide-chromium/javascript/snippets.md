---
description: Les extraits sont des petits scripts que vous pouvez créer et exécuter dans l’outil sources de Microsoft Edge DevTools.  Vous pouvez accéder aux ressources et les exécuter à partir de n’importe quelle page.  Lorsque vous exécutez un snippet, il s’exécute à partir du contexte de la page Web actuellement ouverte.
title: Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 89b028177016a9194a67bbbe44d08572e5755f95
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230956"
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

# <span data-ttu-id="283e6-106">Exécuter des extraits de code JavaScript sur n’importe quelle page Web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="283e6-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="283e6-107">Si vous exécutez le même code dans la [console][DevtoolsConsoleIndex] de manière répétée, envisagez d’enregistrer le code en tant qu’extrait.</span><span class="sxs-lookup"><span data-stu-id="283e6-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="283e6-108">Les extraits sont des scripts que vous créez dans l’outil [sources][DevToolsSourcesTool] .</span><span class="sxs-lookup"><span data-stu-id="283e6-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="283e6-109">Les extraits de code ont accès au contexte JavaScript de la page Web, et vous pouvez exécuter des extraits de code sur une page Web.</span><span class="sxs-lookup"><span data-stu-id="283e6-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="283e6-110">Les paramètres de sécurité de la plupart des pages Web se bloquent lors du chargement d’autres scripts dans les extraits.</span><span class="sxs-lookup"><span data-stu-id="283e6-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="283e6-111">Pour cette raison, vous devez inclure tout votre code dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="283e6-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="283e6-112">Les extraits de vue sont une alternative aux [bookmarklets][WikiBookmarklet] à la différence que les extraits de la base ne s’exécutent que dans devtools et ne sont pas limités à la longueur autorisée d’une URL.</span><span class="sxs-lookup"><span data-stu-id="283e6-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="283e6-113">L’utilisation d’extraits est un excellent moyen de changer quelques éléments dans une page Web tierce.</span><span class="sxs-lookup"><span data-stu-id="283e6-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="283e6-114">Les changements de code dans les extraits de code sont ajoutés à la page Web actuelle et s’exécutent dans le même contexte.</span><span class="sxs-lookup"><span data-stu-id="283e6-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="283e6-115">Pour plus d’informations sur la modification du code existant d’une page Web, voir [remplacement][DevtoolsJavascriptOverrides].</span><span class="sxs-lookup"><span data-stu-id="283e6-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="283e6-116">Par exemple, dans la figure suivante, la page d’accueil DevTools sur la gauche et le code source de l’extrait de code à droite.</span><span class="sxs-lookup"><span data-stu-id="283e6-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Avant d’exécuter l’extrait de." lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="283e6-118">Page Web avant d’exécuter l’extrait</span><span class="sxs-lookup"><span data-stu-id="283e6-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="283e6-119">Code source de l’extrait de code de la page Web avant d’exécuter l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="283e6-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="283e6-120">Dans l’illustration suivante, la page Web s’affiche après l’exécution de l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="283e6-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="283e6-121">Le **tiroir** de la console s’affiche pour afficher le `Hello, Snippets!` message indiquant que le Snippet enregistre les journaux et le contenu de la page Web s’en trouve entièrement modifié.</span><span class="sxs-lookup"><span data-stu-id="283e6-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="La page Web après l’exécution de l’extrait" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="283e6-123">La page Web après l’exécution de l’extrait</span><span class="sxs-lookup"><span data-stu-id="283e6-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <span data-ttu-id="283e6-124">Ouvrir le volet d’extraits</span><span class="sxs-lookup"><span data-stu-id="283e6-124">Open the Snippets pane</span></span>  

<span data-ttu-id="283e6-125">Le volet d' **extraits** de liste répertorie vos extraits.</span><span class="sxs-lookup"><span data-stu-id="283e6-125">The **Snippets** pane lists your Snippets.</span></span>  <span data-ttu-id="283e6-126">Lorsque vous voulez modifier un extrait de rapport, vous devez l’ouvrir à partir du volet **extraits** .</span><span class="sxs-lookup"><span data-stu-id="283e6-126">When you want to edit a Snippet, you need to open it from the **Snippets** pane.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Volet Snippets" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="283e6-128">Volet **snippets**</span><span class="sxs-lookup"><span data-stu-id="283e6-128">The **Snippets** pane</span></span>  
:::image-end:::  

### <span data-ttu-id="283e6-129">Ouvrir le volet des fragments de fenêtre à l’aide d’une souris</span><span class="sxs-lookup"><span data-stu-id="283e6-129">Open the Snippets pane with a mouse</span></span>  

1.  <span data-ttu-id="283e6-130">Sélectionnez l’onglet **sources** pour ouvrir l’outil **sources** .</span><span class="sxs-lookup"><span data-stu-id="283e6-130">Choose the **Sources** tab to open the **Sources** tool.</span></span>  <span data-ttu-id="283e6-131">Le volet **page** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="283e6-131">The **Page** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Outil sources avec le volet pages ouvert à gauche" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="283e6-133">Outil **sources** avec le volet **pages** ouvert à gauche</span><span class="sxs-lookup"><span data-stu-id="283e6-133">The **Sources** tool with the **Page** pane open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="283e6-134">Cliquez sur l’onglet **extraits** de vue pour ouvrir le volet d' **extraits** .</span><span class="sxs-lookup"><span data-stu-id="283e6-134">Choose the **Snippets** tab to open the **Snippets** pane.</span></span>  <span data-ttu-id="283e6-135">Il est possible que vous deviez sélectionner d' **autres onglets** \ ( ![ plus d’onglets ][ImageMoreTabsIcon] \) pour accéder à l’option d' **extraits** .</span><span class="sxs-lookup"><span data-stu-id="283e6-135">You may need to choose **More Tabs** \(![More Tabs][ImageMoreTabsIcon]\) to access the **Snippets** option.</span></span>  
    
### <span data-ttu-id="283e6-136">Ouvrir le volet d’extraits de fenêtre à l’aide du menu de commandes</span><span class="sxs-lookup"><span data-stu-id="283e6-136">Open the Snippets pane with the Command Menu</span></span>  

1.  <span data-ttu-id="283e6-137">Focalisez votre curseur à un endroit quelconque dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="283e6-137">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="283e6-138">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="283e6-138">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="283e6-139">Tapez `Snippets` , choisissez **afficher les extraits**, puis sélectionnez `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="283e6-139">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Commande Afficher les extraits" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="283e6-141">Commande **afficher les extraits**</span><span class="sxs-lookup"><span data-stu-id="283e6-141">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="283e6-142">Créer des extraits de</span><span class="sxs-lookup"><span data-stu-id="283e6-142">Create Snippets</span></span>  

### <span data-ttu-id="283e6-143">Créer un snippet via le volet sources</span><span class="sxs-lookup"><span data-stu-id="283e6-143">Create a Snippet through the Sources panel</span></span>  

1.  <span data-ttu-id="283e6-144">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="283e6-144">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="283e6-145">Sélectionnez **nouvel extrait**.</span><span class="sxs-lookup"><span data-stu-id="283e6-145">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="283e6-146">Entrez le nom de votre snippet, puis sélectionnez `Enter` Enregistrer.</span><span class="sxs-lookup"><span data-stu-id="283e6-146">Enter a name for your Snippet then select `Enter` to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nommer un snippet" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="283e6-148">Nommer un snippet</span><span class="sxs-lookup"><span data-stu-id="283e6-148">Name a Snippet</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="283e6-149">Créer un snippet via le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="283e6-149">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="283e6-150">Focalisez votre curseur à un endroit quelconque dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="283e6-150">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="283e6-151">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="283e6-151">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="283e6-152">Tapez `Snippet` , choisissez **créer un nouvel extrait**, puis sélectionnez `Enter` pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="283e6-152">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Commande de création d’un nouveau Snippet" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="283e6-154">Commande de création d’un nouveau Snippet</span><span class="sxs-lookup"><span data-stu-id="283e6-154">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="283e6-155">Pour renommer votre nouveau Snippet avec un nom personnalisé, accédez à [Renommer des extraits de nom](#rename-snippets).</span><span class="sxs-lookup"><span data-stu-id="283e6-155">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <span data-ttu-id="283e6-156">Modifier des extraits de ce profil</span><span class="sxs-lookup"><span data-stu-id="283e6-156">Edit Snippets</span></span>  

1.  <span data-ttu-id="283e6-157">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="283e6-157">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="283e6-158">Dans le volet **snippets** , sélectionnez le nom de l’extrait que vous voulez modifier.</span><span class="sxs-lookup"><span data-stu-id="283e6-158">In the **Snippets** pane, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="283e6-159">Il s’ouvre dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="283e6-159">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Éditeur de code" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="283e6-161">**Éditeur de code**</span><span class="sxs-lookup"><span data-stu-id="283e6-161">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="283e6-162">Utilisez l' **éditeur de code** pour ajouter du JavaScript à votre snippet.</span><span class="sxs-lookup"><span data-stu-id="283e6-162">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="283e6-163">Lorsqu’un astérisque apparaît en regard du nom de votre snippet, cela signifie que vous avez du code non enregistré.</span><span class="sxs-lookup"><span data-stu-id="283e6-163">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="283e6-164">Sélectionnez `Control` + `S` \ (Windows, Linux \) ou `Command` + `S` \ (MacOS \) pour l’enregistrer.</span><span class="sxs-lookup"><span data-stu-id="283e6-164">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un astérisque en regard du nom de l’extrait de code indique le code non enregistré" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="283e6-166">Un astérisque en regard du nom de l’extrait de code indique le code non enregistré</span><span class="sxs-lookup"><span data-stu-id="283e6-166">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="283e6-167">Exécuter des Snippets</span><span class="sxs-lookup"><span data-stu-id="283e6-167">Run Snippets</span></span>  

### <span data-ttu-id="283e6-168">Exécuter un snippet à partir du panneau sources</span><span class="sxs-lookup"><span data-stu-id="283e6-168">Run a Snippet from the Sources panel</span></span>  

1.  <span data-ttu-id="283e6-169">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="283e6-169">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="283e6-170">Sélectionnez le nom de l’extrait que vous souhaitez exécuter.</span><span class="sxs-lookup"><span data-stu-id="283e6-170">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="283e6-171">L’extrait de code s’ouvre dans l' **éditeur de code**.</span><span class="sxs-lookup"><span data-stu-id="283e6-171">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="283e6-172">Sélectionnez **exécuter le fragment** de passe \ ( ![ exécuter l’extrait ][ImageRunSnippetIcon] \), ou sélectionnez `Control` + `Enter` \ (Windows, Linux \) ou `Command` + `Enter` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="283e6-172">Choose **Run Snippet** \(![Run Snippet][ImageRunSnippetIcon]\), or select `Control`+`Enter` \(Windows, Linux\) or `Command`+`Enter` \(macOS\).</span></span>  
    
### <span data-ttu-id="283e6-173">Exécuter un extrait de commande avec le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="283e6-173">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="283e6-174">Focalisez votre curseur à un endroit quelconque dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="283e6-174">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="283e6-175">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="283e6-175">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="283e6-176">Supprimez le `>` caractère et tapez le `!` caractère suivi du nom de l’extrait que vous voulez exécuter.</span><span class="sxs-lookup"><span data-stu-id="283e6-176">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Exécution d’un snippet à partir du menu de commandes" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="283e6-178">Exécution d’un snippet à partir du **menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="283e6-178">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="283e6-179">Activez `Enter` cette option pour exécuter l’extrait de.</span><span class="sxs-lookup"><span data-stu-id="283e6-179">Select `Enter` to run the Snippet.</span></span>  

## <span data-ttu-id="283e6-180">Renommer des extraits de nom</span><span class="sxs-lookup"><span data-stu-id="283e6-180">Rename Snippets</span></span>  

1.  <span data-ttu-id="283e6-181">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="283e6-181">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="283e6-182">Placez le curseur sur le nom de l’extrait, ouvrez le menu contextuel, puis cliquez sur **Renommer**.</span><span class="sxs-lookup"><span data-stu-id="283e6-182">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <span data-ttu-id="283e6-183">Supprimer des extraits de</span><span class="sxs-lookup"><span data-stu-id="283e6-183">Delete Snippets</span></span>  

1.  <span data-ttu-id="283e6-184">[Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).</span><span class="sxs-lookup"><span data-stu-id="283e6-184">[Open the **Snippets** pane](#open-the-snippets-pane).</span></span>  
1.  <span data-ttu-id="283e6-185">Placez le curseur sur le nom de l’extrait, ouvrez le menu contextuel, puis cliquez sur **supprimer**.</span><span class="sxs-lookup"><span data-stu-id="283e6-185">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <span data-ttu-id="283e6-186">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="283e6-186">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console | Documents Microsoft"  
[DevToolsSourcesTool]: ../sources/index.md "Présentation de l’outil sources | Documents Microsoft"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Remplacements | Documents Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc-notes | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipédia"  

> [!NOTE]
> <span data-ttu-id="283e6-192">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="283e6-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="283e6-193">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="283e6-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="283e6-195">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="283e6-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
