---
title: Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601345"
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





# <span data-ttu-id="77cb8-103">Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)</span><span class="sxs-lookup"><span data-stu-id="77cb8-103">Change Microsoft Edge DevTools Placement (Undock, Dock To Bottom, Dock To Left)</span></span>   



<span data-ttu-id="77cb8-104">Par défaut, DevTools est ancré à droite de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="77cb8-104">By default DevTools is docked to the right of your viewport.</span></span>  <span data-ttu-id="77cb8-105">Vous pouvez également ancrer en bas, ancrer à gauche, ou détacher la DevTools dans une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="77cb8-105">You may also dock to bottom, dock to left, or undock the DevTools to a separate window.</span></span>  

> ##### <span data-ttu-id="77cb8-106">Figure1</span><span class="sxs-lookup"><span data-stu-id="77cb8-106">Figure 1</span></span>  
> <span data-ttu-id="77cb8-107">Ancrer à gauche</span><span class="sxs-lookup"><span data-stu-id="77cb8-107">Dock To Left</span></span>  
> ![Ancrer à gauche][ImageDockLeft]  

> ##### <span data-ttu-id="77cb8-109">Figure 2</span><span class="sxs-lookup"><span data-stu-id="77cb8-109">Figure 2</span></span>  
> <span data-ttu-id="77cb8-110">Ancrer en bas</span><span class="sxs-lookup"><span data-stu-id="77cb8-110">Dock To Bottom</span></span>  
> ![Ancrer en bas][ImageDockBottom]  

> ##### <span data-ttu-id="77cb8-112">Figure3</span><span class="sxs-lookup"><span data-stu-id="77cb8-112">Figure 3</span></span>  
> <span data-ttu-id="77cb8-113">Navigateur dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="77cb8-113">Browser in separate window</span></span>  
> ![Navigateur dans une fenêtre séparée][ImageUndockBrowser]  

> ##### <span data-ttu-id="77cb8-115">Figure 4</span><span class="sxs-lookup"><span data-stu-id="77cb8-115">Figure 4</span></span>  
> <span data-ttu-id="77cb8-116">DevTools non attaché dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="77cb8-116">Undocked DevTools in separate window</span></span>  
> ![DevTools non attaché dans une fenêtre séparée][ImageUndockDevTools]  

## <span data-ttu-id="77cb8-118">Changer la position dans le menu principal</span><span class="sxs-lookup"><span data-stu-id="77cb8-118">Change placement from the main menu</span></span>   

1.  <span data-ttu-id="77cb8-119">Cliquez sur **personnaliser et contrôler devtools** `...` et sélectionnez **détacher dans une fenêtre indépendante** ![ ][ImageUndockIcon] , **ancrer** en bas ![ à ][ImageBottomIcon] gauche ou **Dock To Left** ![ ][ImageLeftIcon] ancrer à gauche.</span><span class="sxs-lookup"><span data-stu-id="77cb8-119">Click **Customize And Control DevTools** `...` and select **Undock Into Separate Window** ![Undock][ImageUndockIcon], **Dock To Bottom** ![Dock To Bottom][ImageBottomIcon], or **Dock To Left** ![Dock To Left][ImageLeftIcon].</span></span>  
    
    > ##### <span data-ttu-id="77cb8-120">Figure 5</span><span class="sxs-lookup"><span data-stu-id="77cb8-120">Figure 5</span></span>  
    > <span data-ttu-id="77cb8-121">Sélection du **retrait dans une fenêtre séparée**</span><span class="sxs-lookup"><span data-stu-id="77cb8-121">Selecting **Undock Into Separate Window**</span></span>  
    > ![Sélection du retrait dans une fenêtre séparée][ImageUndockSettings]  
    
## <span data-ttu-id="77cb8-123">Changer le positionnement dans le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="77cb8-123">Change placement from the Command Menu</span></span>   

1.  <span data-ttu-id="77cb8-124">[Ouvrir le menu de commandes][DevtoolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="77cb8-124">[Open the Command Menu][DevtoolsCommandMenu].</span></span>  
1.  <span data-ttu-id="77cb8-125">Exécutez l’une des commandes `Dock To Bottom` suivantes: `Undock Into Separate Window`</span><span class="sxs-lookup"><span data-stu-id="77cb8-125">Run one of the following commands: `Dock To Bottom`, `Undock Into Separate Window`.</span></span>  <span data-ttu-id="77cb8-126">Il n’existe actuellement aucune commande pour l’ancrage à gauche, mais vous pouvez y accéder à partir du [menu principal](#change-placement-from-the-main-menu).</span><span class="sxs-lookup"><span data-stu-id="77cb8-126">Currently there is no command for docking to left, but you may access it from the [main menu](#change-placement-from-the-main-menu).</span></span>  
    
    > ##### <span data-ttu-id="77cb8-127">Figure 6</span><span class="sxs-lookup"><span data-stu-id="77cb8-127">Figure 6</span></span>  
    > <span data-ttu-id="77cb8-128">Commande détacher</span><span class="sxs-lookup"><span data-stu-id="77cb8-128">The undock command</span></span>  
    > ![Commande détacher][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Figure 1: ancrer sur la gauche"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Figure 2: ancrer en bas"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Figure 3: navigateur dans une fenêtre séparée"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Figure 4: DevTools non attaché dans une fenêtre séparée"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Figure 5: sélectionner détacher dans une fenêtre séparée"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Figure 6: commande détacher"  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="77cb8-137">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="77cb8-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="77cb8-138">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/customize/placement) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="77cb8-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/customize/placement) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="77cb8-140">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="77cb8-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
