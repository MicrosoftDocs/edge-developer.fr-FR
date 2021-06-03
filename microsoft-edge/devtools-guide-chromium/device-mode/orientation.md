---
description: Ouvrez l’outil Capteurs et accédez à la section Orientation.
title: Simuler l’orientation de l’appareil Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 71527d8dce0d7a0563feef0081ce12d40eeb5e1a
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564307"
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
# <a name="simulate-device-orientation-with-microsoft-edge-devtools"></a><span data-ttu-id="cc45c-104">Simuler l’orientation de l’appareil Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cc45c-104">Simulate device orientation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="cc45c-105">Effectuer les actions suivantes pour simuler différentes orientations d’appareil Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cc45c-105">Complete the following actions to simulate different device orientations from Microsoft Edge DevTools.</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="cc45c-106">Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**</span><span class="sxs-lookup"><span data-stu-id="cc45c-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu Commande" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="cc45c-108">Menu **Commande**</span><span class="sxs-lookup"><span data-stu-id="cc45c-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="cc45c-109">Tapez `sensors` , choisissez Afficher les **capteurs,** puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="cc45c-109">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="cc45c-110">**L’outil** Capteurs s’ouvre en bas de la fenêtre DevTools.</span><span class="sxs-lookup"><span data-stu-id="cc45c-110">The **Sensors** tool opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="cc45c-111">Dans la **liste Orientation,** sélectionnez l’une des orientations prédéfines, par exemple, ou choisissez Orientation personnalisée pour fournir `Portrait upside down` votre propre orientation exacte. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="cc45c-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or choose **Custom orientation** to provide your own exact orientation.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Choisir portrait à l’envers à partir de la liste Orientation" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             <span data-ttu-id="cc45c-113">Choisir `Portrait upside down` dans la liste **Orientation**</span><span class="sxs-lookup"><span data-stu-id="cc45c-113">Choose `Portrait upside down` from the **Orientation** list</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="cc45c-114">Une fois que **vous avez choisi l’orientation**personnalisée, les champs et les champs `alpha` sont `beta` `gamma` activés.</span><span class="sxs-lookup"><span data-stu-id="cc45c-114">After you choose **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
          <!--To understand how each axis works, navigate to [Alpha][alpha], [Beta][beta], and [Gamma][gamma].  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          <span data-ttu-id="cc45c-115">Vous pouvez également définir une orientation personnalisée en faisant glisser le modèle **d’orientation.**</span><span class="sxs-lookup"><span data-stu-id="cc45c-115">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="cc45c-116">Maintenez `Shift` la main avant de faire glisser pour faire pivoter le long de `alpha` l’axe.</span><span class="sxs-lookup"><span data-stu-id="cc45c-116">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Modèle d’orientation" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             <span data-ttu-id="cc45c-118">Modèle **d’orientation**</span><span class="sxs-lookup"><span data-stu-id="cc45c-118">The **Orientation Model**</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="cc45c-119">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="cc45c-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> <span data-ttu-id="cc45c-120">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cc45c-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cc45c-121">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="cc45c-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="cc45c-123">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cc45c-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
