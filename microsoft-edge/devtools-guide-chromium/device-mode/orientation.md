---
title: Simuler l’orientation de l’appareil avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 9e8115819fa6c3209a6c82940e033113783ece0c
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607323"
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





# <span data-ttu-id="829bc-103">Simuler l’orientation de l’appareil avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="829bc-103">Simulate Device Orientation With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="829bc-104">Pour simuler différentes orientations d’appareil à partir de Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="829bc-104">To simulate different device orientations from Microsoft Edge DevTools:</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="829bc-105">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="829bc-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="829bc-106">Figure1</span><span class="sxs-lookup"><span data-stu-id="829bc-106">Figure 1</span></span>  
    > <span data-ttu-id="829bc-107">Menu de commandes</span><span class="sxs-lookup"><span data-stu-id="829bc-107">The Command Menu</span></span>  
    > ![Menu de commandes][ImageCommandMenu]  
    
1.  <span data-ttu-id="829bc-109">Tapez `sensors` , sélectionnez **afficher les capteurs**, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="829bc-109">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="829bc-110">L’onglet **capteurs** s’ouvre en bas de la fenêtre devtools.</span><span class="sxs-lookup"><span data-stu-id="829bc-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="829bc-111">Dans la liste **orientation** , sélectionnez l’une des orientations prédéfinies, par exemple `Portrait upside down` , ou sélectionnez **orientation personnalisée** pour fournir votre propre orientation exacte.</span><span class="sxs-lookup"><span data-stu-id="829bc-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or select **Custom orientation** to provide your own exact orientation.</span></span>  
    
    > ##### <span data-ttu-id="829bc-112">Figure 2</span><span class="sxs-lookup"><span data-stu-id="829bc-112">Figure 2</span></span>  
    > <span data-ttu-id="829bc-113">Sélection `Portrait upside down` dans la liste **orientation**</span><span class="sxs-lookup"><span data-stu-id="829bc-113">Selecting `Portrait upside down` from the **Orientation** list</span></span>  
    > ![Sélection de l’orientation portrait dans la liste orientation][ImageOrientationPortraitUpsideDown]  
    
    <span data-ttu-id="829bc-115">Après avoir sélectionné **orientation personnalisée**, `alpha` les `beta` champs, et `gamma` sont activés.</span><span class="sxs-lookup"><span data-stu-id="829bc-115">After selecting **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
    <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
    <!--todo: update links to alpha, beta, and gamma section when available -->  
    <span data-ttu-id="829bc-116">Vous pouvez également définir une orientation personnalisée en faisant glisser le modèle d' **orientation**.</span><span class="sxs-lookup"><span data-stu-id="829bc-116">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="829bc-117">Mettre `Shift` en attente avant de faire pivoter pour faire pivoter le long de l' `alpha` axe.</span><span class="sxs-lookup"><span data-stu-id="829bc-117">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
    
    > ##### <span data-ttu-id="829bc-118">Figure3</span><span class="sxs-lookup"><span data-stu-id="829bc-118">Figure 3</span></span>  
    > <span data-ttu-id="829bc-119">Le **modèle d’orientation**</span><span class="sxs-lookup"><span data-stu-id="829bc-119">The **Orientation Model**</span></span>  
    > ![Le modèle d’orientation][ImageOrientationModel]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Figure 1: menu de commandes"  
[ImageOrientationPortraitUpsideDown]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png "Figure 2: sélection de l’option portrait à l’envers dans la liste orientation"  
[ImageOrientationModel]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-custom.msft.png "Figure 3: modèle d’orientation"  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation \& Motion"  -->  

> [!NOTE]
> <span data-ttu-id="829bc-124">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="829bc-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="829bc-125">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="829bc-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="829bc-127">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="829bc-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
