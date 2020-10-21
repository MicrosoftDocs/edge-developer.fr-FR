---
description: Pour déplacer Microsoft Edge DevTools en bas ou à gauche de votre fenêtre d’affichage, ou dans une fenêtre séparée.
title: Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 65c0849af5da671bb0d76397d6d9395bc249eaac
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125047"
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

# <span data-ttu-id="11158-104">Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)</span><span class="sxs-lookup"><span data-stu-id="11158-104">Change Microsoft Edge DevTools placement (Undock, Dock To Bottom, Dock To Left)</span></span>  

<span data-ttu-id="11158-105">Par défaut, DevTools est ancré à droite de votre fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="11158-105">By default DevTools is docked to the right of your viewport.</span></span>  <span data-ttu-id="11158-106">Vous pouvez également ancrer en bas, ancrer à gauche, ou détacher la DevTools dans une autre fenêtre.</span><span class="sxs-lookup"><span data-stu-id="11158-106">You may also dock to bottom, dock to left, or undock the DevTools to a separate window.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-right-docked.msft.png" alt-text="Sélectionner ancrer à gauche" lightbox="../media/customize-elements-styles-right-docked.msft.png":::
         <span data-ttu-id="11158-108">Sélectionner</span><span class="sxs-lookup"><span data-stu-id="11158-108">Select</span></span> `Dock To Left`  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-bottom-docked.msft.png" alt-text="Sélectionner ancrer à gauche" lightbox="../media/customize-elements-styles-bottom-docked.msft.png":::
         <span data-ttu-id="11158-110">Sélectionner</span><span class="sxs-lookup"><span data-stu-id="11158-110">Select</span></span> `Dock To Bottom`  
      :::image-end:::  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png" alt-text="Sélectionner ancrer à gauche" lightbox="../media/customize-elements-styles-options-dock-side-highlight-browser.msft.png":::
         <span data-ttu-id="11158-112">Navigateur dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="11158-112">Browser in separate window</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png" alt-text="Sélectionner ancrer à gauche" lightbox="../media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png":::
         <span data-ttu-id="11158-114">DevTools non attaché dans une fenêtre séparée</span><span class="sxs-lookup"><span data-stu-id="11158-114">Undocked DevTools in separate window</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="11158-115">Changer la position dans le menu principal</span><span class="sxs-lookup"><span data-stu-id="11158-115">Change placement from the main menu</span></span>  

1.  <span data-ttu-id="11158-116">Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) et sélectionnez **détacher dans la fenêtre séparée** \ ( ![ détacher ][ImageUndockIcon] \), **ancrer en bas** \ ( ![ ancrer en bas ][ImageBottomIcon] \), ou **ancrer à gauche** , ![ ][ImageLeftIcon]</span><span class="sxs-lookup"><span data-stu-id="11158-116">Choose **Customize And Control DevTools** \(`...`\) and choose **Undock Into Separate Window** \(![Undock][ImageUndockIcon]\), **Dock To Bottom** \(![Dock To Bottom][ImageBottomIcon]\), or **Dock To Left** \(![Dock To Left][ImageLeftIcon]\).</span></span>  
    
    :::image type="complex" source="../media/customize-elements-styles-options-dock-side-highlight.msft.png" alt-text="Sélectionner ancrer à gauche" lightbox="../media/customize-elements-styles-options-dock-side-highlight.msft.png":::
       <span data-ttu-id="11158-118">Sélectionner **détacher dans une fenêtre séparée**</span><span class="sxs-lookup"><span data-stu-id="11158-118">Choose **Undock Into Separate Window**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="11158-119">Changer le positionnement dans le menu de commandes</span><span class="sxs-lookup"><span data-stu-id="11158-119">Change placement from the Command Menu</span></span>  

1.  <span data-ttu-id="11158-120">[Ouvrir le menu de commandes][DevtoolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="11158-120">[Open the Command Menu][DevtoolsCommandMenu].</span></span>  
1.  <span data-ttu-id="11158-121">Exécutez l’une des commandes `Dock To Bottom` suivantes: `Undock Into Separate Window`</span><span class="sxs-lookup"><span data-stu-id="11158-121">Run one of the following commands: `Dock To Bottom`, `Undock Into Separate Window`.</span></span>  <span data-ttu-id="11158-122">Il n’existe actuellement aucune commande pour l’ancrage à gauche, mais vous pouvez y accéder à partir du [menu principal](#change-placement-from-the-main-menu).</span><span class="sxs-lookup"><span data-stu-id="11158-122">Currently there is no command for docking to left, but you may access it from the [main menu](#change-placement-from-the-main-menu).</span></span>  
    
    :::image type="complex" source="../media/customize-elements-styles-command-menu-undo.msft.png" alt-text="Sélectionner ancrer à gauche" lightbox="../media/customize-elements-styles-command-menu-undo.msft.png":::
       <span data-ttu-id="11158-124">Commande détacher</span><span class="sxs-lookup"><span data-stu-id="11158-124">The undock command</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="11158-125">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="11158-125">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageUndockIcon]: ../media/undock-icon.msft.png  
[ImageBottomIcon]: ../media/bottom-icon.msft.png  
[ImageLeftIcon]: ../media/left-icon.msft.png  

<!-- links -->  

[DevtoolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="11158-127">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="11158-127">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="11158-128">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/customize/placement) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="11158-128">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/customize/placement) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="11158-130">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="11158-130">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
