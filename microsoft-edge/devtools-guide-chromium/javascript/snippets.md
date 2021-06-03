---
description: Les extraits de code sont de petits scripts que vous pouvez écrire et exécuter dans l’outil Sources de Microsoft Edge DevTools.  Vous pouvez accéder aux ressources et les exécuter à partir de n’importe quelle page web.  Lorsque vous exécutez un extrait de code, il s’exécute à partir du contexte de la page web actuellement ouverte.
title: Exécuter des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 4a84e959f652320f40a501a26e9ba763c7348b33
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564111"
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
# <a name="run-snippets-of-javascript-on-any-webpage-with-microsoft-edge-devtools"></a><span data-ttu-id="75d25-106">Exécuter des extraits de code JavaScript sur n’importe quelle page web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="75d25-106">Run snippets of JavaScript on any webpage with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="75d25-107">Si vous exécutez le même code dans la [console][DevtoolsConsoleIndex] à plusieurs reprises, envisagez plutôt d’enregistrer le code en tant qu’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="75d25-107">If you are running the same code in the [Console][DevtoolsConsoleIndex] repeatedly, consider saving the code as a Snippet instead.</span></span>  <span data-ttu-id="75d25-108">Les extraits de code sont des scripts que vous avez écrits dans [l’outil Sources.][DevToolsSourcesTool]</span><span class="sxs-lookup"><span data-stu-id="75d25-108">Snippets are scripts that you author in the [Sources][DevToolsSourcesTool] tool.</span></span>  <span data-ttu-id="75d25-109">Les extraits de code ont accès au contexte JavaScript de la page web et vous pouvez exécuter des extraits de code sur n’importe quelle page web.</span><span class="sxs-lookup"><span data-stu-id="75d25-109">Snippets have access to the JavaScript context of the webpage, and you may run snippets on any webpage.</span></span>  <span data-ttu-id="75d25-110">Les paramètres de sécurité de la plupart des pages web bloquent le chargement d’autres scripts dans des extraits de code.</span><span class="sxs-lookup"><span data-stu-id="75d25-110">The security settings of most webpages block from loading other scripts in Snippets.</span></span>  <span data-ttu-id="75d25-111">Pour cette raison, vous devez inclure tout votre code dans un seul fichier.</span><span class="sxs-lookup"><span data-stu-id="75d25-111">For that reason, you must include all your code in one file.</span></span>  

<span data-ttu-id="75d25-112">Les extraits de code [][WikiBookmarklet] sont une alternative aux signets avec la différence que les extraits de code s’exécutent uniquement dans DevTools et ne sont pas limités à la longueur autorisée d’une URL.</span><span class="sxs-lookup"><span data-stu-id="75d25-112">Snippets are an alternative to [bookmarklets][WikiBookmarklet] with the difference that Snippets only run in DevTools and are not limited to the allowed length of a URL.</span></span>  

<span data-ttu-id="75d25-113">L’utilisation d’extraits de code est un excellent moyen de modifier quelques éléments dans une page web tierce.</span><span class="sxs-lookup"><span data-stu-id="75d25-113">Using Snippets is an excellent way to change a few things in a third-party webpage.</span></span>  <span data-ttu-id="75d25-114">Les modifications de code dans les extraits de code sont ajoutées à la page web actuelle et s’exécutent dans le même contexte.</span><span class="sxs-lookup"><span data-stu-id="75d25-114">Code changes in Snippets are added to the current webpage and run in the same context.</span></span>  <span data-ttu-id="75d25-115">Pour plus d’informations sur la modification du code existant d’une page web, accédez [à Remplacements.][DevtoolsJavascriptOverrides]</span><span class="sxs-lookup"><span data-stu-id="75d25-115">For more information about changing the existing code of a webpage, navigate to [Overrides][DevtoolsJavascriptOverrides].</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="75d25-116">Par exemple, la figure suivante montre la page d’accueil de DevTools à gauche et du code source d’extrait de code à droite.</span><span class="sxs-lookup"><span data-stu-id="75d25-116">For example, in the following figure shows the DevTools homepage on the left and some Snippet source code on the right.</span></span>  
      
      :::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Avant d’exécution de l’extrait de code" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
         <span data-ttu-id="75d25-118">Page web avant l’exécution de l’extrait de code</span><span class="sxs-lookup"><span data-stu-id="75d25-118">The webpage before running the Snippet</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="75d25-119">Code source de l’extrait de code à partir de la page web avant d’exécutez l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="75d25-119">The Snippet source code from the webpage before running the Snippet.</span></span>  
      
      ```javascript
      console.log('Hello, Snippets!');
      document.body.innerHTML = '';
      var p = document.createElement('p');
      p.textContent = 'Hello, Snippets!';
      document.body.appendChild(p);
      ```
   :::column-end:::
:::row-end:::  

<span data-ttu-id="75d25-120">Dans la figure suivante, la page web apparaît après l’exécution de l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="75d25-120">In the following figure, the webpage appears after running the Snippet.</span></span>  <span data-ttu-id="75d25-121">Le **caisse de la** console s’affiche pour afficher le message journal de l’extrait de code et le contenu de la page web change `Hello, Snippets!` complètement.</span><span class="sxs-lookup"><span data-stu-id="75d25-121">The **Console Drawer** pops up to display the `Hello, Snippets!` message that the Snippet logs, and the content of the webpage changes completely.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Page web après l’exécution de l’extrait de code" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   <span data-ttu-id="75d25-123">Page web après l’exécution de l’extrait de code</span><span class="sxs-lookup"><span data-stu-id="75d25-123">The webpage after running the Snippet</span></span>  
:::image-end:::  

## <a name="open-the-snippets-tab"></a><span data-ttu-id="75d25-124">Ouvrir l’onglet Extraits de code</span><span class="sxs-lookup"><span data-stu-id="75d25-124">Open the Snippets tab</span></span>  

<span data-ttu-id="75d25-125">**L’onglet Extraits** de code, dans le volet **Navigateur** à gauche, répertorie vos extraits de code.</span><span class="sxs-lookup"><span data-stu-id="75d25-125">The **Snippets** tab, in the **Navigator** pane on the left, lists your Snippets.</span></span>  <span data-ttu-id="75d25-126">Lorsque vous souhaitez modifier un extrait de code, vous devez l’ouvrir à partir de l’onglet Extraits **de** code.</span><span class="sxs-lookup"><span data-stu-id="75d25-126">When you want to edit a Snippet, you need to open it from the **Snippets** tab.</span></span>  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Onglet Extraits de code" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   <span data-ttu-id="75d25-128">Onglet **Extraits de** code</span><span class="sxs-lookup"><span data-stu-id="75d25-128">The **Snippets** tab</span></span>  
:::image-end:::  

### <a name="open-the-snippets-tab-with-a-mouse"></a><span data-ttu-id="75d25-129">Ouvrir l’onglet Extraits de code avec une souris</span><span class="sxs-lookup"><span data-stu-id="75d25-129">Open the Snippets tab with a mouse</span></span>  

1.  <span data-ttu-id="75d25-130">Sélectionnez **l’onglet Sources.**  **L’outil Sources** s’affiche.</span><span class="sxs-lookup"><span data-stu-id="75d25-130">Choose the **Sources** tab.  The **Sources** tool appears.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Outil Sources avec l’onglet Page ouvert à gauche" lightbox="../media/javascript-sources-page-pane.msft.png":::
       <span data-ttu-id="75d25-132">Outil **Sources** avec l’onglet **Page** ouvert à gauche</span><span class="sxs-lookup"><span data-stu-id="75d25-132">The **Sources** tool with the **Page** tab open on the left</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="75d25-133">Dans le **volet Navigateur** (à gauche), sélectionnez l’onglet **Extraits de** code.  Pour accéder à **l’option** Extraits de code, vous devrez peut-être sélectionner **Plus d’onglets** \( ![ Autres onglets ](../media/more-tabs-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="75d25-133">In the **Navigator** pane (on the left), choose the **Snippets** tab.  To access the **Snippets** option, you may need to choose **More tabs** \(![More tabs](../media/more-tabs-icon.msft.png)\).</span></span>  
    
### <a name="open-the-snippets-tab-with-the-command-menu"></a><span data-ttu-id="75d25-134">Ouvrir l’onglet Extraits de code avec le menu Commande</span><span class="sxs-lookup"><span data-stu-id="75d25-134">Open the Snippets tab with the Command Menu</span></span>  

1.  <span data-ttu-id="75d25-135">Sélectionnez n’importe quoi dans DevTools, afin que DevTools ait le focus.</span><span class="sxs-lookup"><span data-stu-id="75d25-135">Select anything in DevTools, so that DevTools has focus.</span></span>  
1.  <span data-ttu-id="75d25-136">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le menu Commande.</span><span class="sxs-lookup"><span data-stu-id="75d25-136">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="75d25-137">Tapez `Snippets` , choisissez Afficher les **extraits**de code, puis `Enter` sélectionnez pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="75d25-137">Type `Snippets`, choose **Show Snippets**, and then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Commande Afficher les extraits de code" lightbox="../media/javascript-search-show-snippets.msft.png":::
       <span data-ttu-id="75d25-139">Commande **Afficher les extraits de** code</span><span class="sxs-lookup"><span data-stu-id="75d25-139">The **Show Snippets** command</span></span>  
    :::image-end:::  
    
## <a name="create-snippets"></a><span data-ttu-id="75d25-140">Créer des extraits de code</span><span class="sxs-lookup"><span data-stu-id="75d25-140">Create Snippets</span></span>  

### <a name="create-a-snippet-through-the-sources-tool"></a><span data-ttu-id="75d25-141">Créer un extrait de code via l’outil Sources</span><span class="sxs-lookup"><span data-stu-id="75d25-141">Create a Snippet through the Sources tool</span></span>  

1.  <span data-ttu-id="75d25-142">[Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)</span><span class="sxs-lookup"><span data-stu-id="75d25-142">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="75d25-143">Choose **New snippet**.</span><span class="sxs-lookup"><span data-stu-id="75d25-143">Choose **New snippet**.</span></span>  
1.  <span data-ttu-id="75d25-144">Entrez un nom pour votre extrait de code, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="75d25-144">Enter a name for your Snippet, and then select `Enter`.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Nommer un extrait de code" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       <span data-ttu-id="75d25-146">Nommer un extrait de code</span><span class="sxs-lookup"><span data-stu-id="75d25-146">Name a Snippet</span></span>  
    :::image-end:::  
    
### <a name="create-a-snippet-through-the-command-menu"></a><span data-ttu-id="75d25-147">Créer un extrait de code dans le menu Commande</span><span class="sxs-lookup"><span data-stu-id="75d25-147">Create a Snippet through the Command Menu</span></span>  

1.  <span data-ttu-id="75d25-148">Concentrez votre curseur quelque part dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="75d25-148">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="75d25-149">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le menu Commande.</span><span class="sxs-lookup"><span data-stu-id="75d25-149">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="75d25-150">Tapez `Snippet` , choisissez Créer un extrait de **code,** puis `Enter` sélectionnez pour exécuter la commande.</span><span class="sxs-lookup"><span data-stu-id="75d25-150">Type `Snippet`, choose **Create new snippet**, then select `Enter` to run the command.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Commande de création d’un extrait de code" lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       <span data-ttu-id="75d25-152">Commande de création d’un extrait de code</span><span class="sxs-lookup"><span data-stu-id="75d25-152">The command for creating a new Snippet</span></span>  
    :::image-end:::  
    
<span data-ttu-id="75d25-153">Pour renommer votre nouvel extrait de code avec un nom personnalisé, accédez à Renommer les [extraits de code.](#rename-snippets)</span><span class="sxs-lookup"><span data-stu-id="75d25-153">To rename your new Snippet with a custom name, navigate to [Rename Snippets](#rename-snippets).</span></span>  

## <a name="edit-snippets"></a><span data-ttu-id="75d25-154">Modifier les extraits de code</span><span class="sxs-lookup"><span data-stu-id="75d25-154">Edit Snippets</span></span>  

1.  <span data-ttu-id="75d25-155">[Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)</span><span class="sxs-lookup"><span data-stu-id="75d25-155">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="75d25-156">Dans **l’onglet Extraits** de code, choisissez le nom de l’extrait de code à modifier.</span><span class="sxs-lookup"><span data-stu-id="75d25-156">In the **Snippets** tab, choose the name of the Snippet that you want to edit.</span></span>  <span data-ttu-id="75d25-157">Il s’ouvre dans **l’éditeur de code.**</span><span class="sxs-lookup"><span data-stu-id="75d25-157">It opens in the **Code Editor**.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Éditeur de code" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       <span data-ttu-id="75d25-159">Éditeur **de code**</span><span class="sxs-lookup"><span data-stu-id="75d25-159">The **Code Editor**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="75d25-160">Utilisez **l’Éditeur de code** pour ajouter JavaScript à votre extrait de code.</span><span class="sxs-lookup"><span data-stu-id="75d25-160">Use the **Code Editor** to add JavaScript to your Snippet.</span></span>  
1.  <span data-ttu-id="75d25-161">Lorsqu’un astérisque apparaît à côté du nom de votre extrait de code, cela signifie que vous avez du code nonavé.</span><span class="sxs-lookup"><span data-stu-id="75d25-161">When an asterisk appears next to the name of your Snippet, it means you have unsaved code.</span></span>  <span data-ttu-id="75d25-162">Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) à enregistrer.</span><span class="sxs-lookup"><span data-stu-id="75d25-162">Select `Control`+`S` \(Windows, Linux\) or `Command`+`S` \(macOS\) to save.</span></span>  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Un astérisque à côté du nom de l’extrait de code indique du code nonavé" lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       <span data-ttu-id="75d25-164">Un astérisque à côté du nom de l’extrait de code indique du code nonavé</span><span class="sxs-lookup"><span data-stu-id="75d25-164">An asterisk next to the Snippet name indicates unsaved code</span></span>  
    :::image-end:::  
    
## <a name="run-snippets"></a><span data-ttu-id="75d25-165">Exécuter des extraits de code</span><span class="sxs-lookup"><span data-stu-id="75d25-165">Run Snippets</span></span>  

### <a name="run-a-snippet-from-the-sources-tool"></a><span data-ttu-id="75d25-166">Exécuter un extrait de code à partir de l’outil Sources</span><span class="sxs-lookup"><span data-stu-id="75d25-166">Run a Snippet from the Sources tool</span></span>  

1.  <span data-ttu-id="75d25-167">[Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)</span><span class="sxs-lookup"><span data-stu-id="75d25-167">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="75d25-168">Choisissez le nom de l’extrait de code à exécuter.</span><span class="sxs-lookup"><span data-stu-id="75d25-168">Choose the name of the Snippet that you want to run.</span></span>  <span data-ttu-id="75d25-169">L’extrait de code s’ouvre dans **l’éditeur de code.**</span><span class="sxs-lookup"><span data-stu-id="75d25-169">The Snippet opens in the **Code Editor**.</span></span>  
1.  <span data-ttu-id="75d25-170">Choose **Run snippet** \( ![ Run Snippet ](../media/run-snippet-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="75d25-170">Choose **Run snippet** \(![Run Snippet](../media/run-snippet-icon.msft.png)\).</span></span>
    
### <a name="run-a-snippet-with-the-command-menu"></a><span data-ttu-id="75d25-171">Exécuter un extrait de code avec le menu Commande</span><span class="sxs-lookup"><span data-stu-id="75d25-171">Run a Snippet with the Command Menu</span></span>  

1.  <span data-ttu-id="75d25-172">Concentrez votre curseur quelque part dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="75d25-172">Focus your cursor somewhere in DevTools.</span></span>  
1.  <span data-ttu-id="75d25-173">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le menu Commande.</span><span class="sxs-lookup"><span data-stu-id="75d25-173">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu.</span></span>  
1.  <span data-ttu-id="75d25-174">Supprimez le caractère et tapez le caractère suivi du nom de l’extrait de code à `>` `!` exécuter.</span><span class="sxs-lookup"><span data-stu-id="75d25-174">Delete the `>` character and type the `!` character followed by the name of the Snippet that you want to run.</span></span>  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Exécution d’un extrait de code à partir du menu Commande" lightbox="../media/javascript-search-run-command.msft.png":::
       <span data-ttu-id="75d25-176">Exécution d’un extrait de code à partir du **menu Commande**</span><span class="sxs-lookup"><span data-stu-id="75d25-176">Running a Snippet from the **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="75d25-177">Sélectionnez `Enter` pour exécuter l’extrait de code.</span><span class="sxs-lookup"><span data-stu-id="75d25-177">Select `Enter` to run the Snippet.</span></span>  

## <a name="rename-snippets"></a><span data-ttu-id="75d25-178">Renommer les extraits de code</span><span class="sxs-lookup"><span data-stu-id="75d25-178">Rename Snippets</span></span>  

1.  <span data-ttu-id="75d25-179">[Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)</span><span class="sxs-lookup"><span data-stu-id="75d25-179">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="75d25-180">Pointez sur le nom de l’extrait de code, ouvrez le menu contextuel \(clic droit\), puis choisissez **Renommer.**</span><span class="sxs-lookup"><span data-stu-id="75d25-180">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Rename**.</span></span>  
    
## <a name="delete-snippets"></a><span data-ttu-id="75d25-181">Supprimer des extraits de code</span><span class="sxs-lookup"><span data-stu-id="75d25-181">Delete Snippets</span></span>  

1.  <span data-ttu-id="75d25-182">[Ouvrez l’onglet Extraits de code.](#open-the-snippets-tab)</span><span class="sxs-lookup"><span data-stu-id="75d25-182">[Open the Snippets tab](#open-the-snippets-tab).</span></span>  
1.  <span data-ttu-id="75d25-183">Pointez sur le nom de l’extrait de code, ouvrez le menu contextuel \(clic droit\), puis choisissez **Supprimer.**</span><span class="sxs-lookup"><span data-stu-id="75d25-183">Hover on the Snippet name, open the contextual menu \(right-click\), and choose **Remove**.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="75d25-184">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="75d25-184">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Vue d’ensemble de la console | Documents Microsoft"  
[DevToolsSourcesTool]: ../sources/index.md "Vue d’ensemble de l’outil Sources | Documents Microsoft"  
[DevtoolsJavascriptOverrides]: ./overrides.md "Remplace les | Documents Microsoft"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Scratchpad | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet | Wikipedia"  

> [!NOTE]
> <span data-ttu-id="75d25-190">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="75d25-190">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="75d25-191">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="75d25-191">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="75d25-193">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="75d25-193">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
