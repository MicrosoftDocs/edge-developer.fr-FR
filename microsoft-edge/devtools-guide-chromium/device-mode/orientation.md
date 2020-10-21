---
description: Ouvrez l’onglet capteurs et accédez à la section orientation.
title: Simuler l’orientation de l’appareil avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 01e6d3a24513b504665dbe0c03d9e72cc1f97533
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124956"
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

# <span data-ttu-id="49f0c-104">Simuler l’orientation de l’appareil avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="49f0c-104">Simulate device orientation with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="49f0c-105">Effectuez les opérations suivantes pour simuler différentes orientations d’appareil à partir de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="49f0c-105">Complete the following actions to simulate different device orientations from Microsoft Edge DevTools.</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="49f0c-106">Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="49f0c-106">Select `Control`+`Shift`+`P` \(Windows, Linux\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="49f0c-108">**Menu de commandes**</span><span class="sxs-lookup"><span data-stu-id="49f0c-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="49f0c-109">Tapez `sensors` , choisissez **afficher les capteurs**, puis sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="49f0c-109">Type `sensors`, choose **Show Sensors**, and select `Enter`.</span></span>  <span data-ttu-id="49f0c-110">L’onglet **capteurs** s’ouvre en bas de la fenêtre devtools.</span><span class="sxs-lookup"><span data-stu-id="49f0c-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="49f0c-111">Dans la liste **orientation** , sélectionnez l’une des orientations prédéfinies, par exemple `Portrait upside down` , ou choisissez **orientation personnalisée** pour fournir votre propre orientation exacte.</span><span class="sxs-lookup"><span data-stu-id="49f0c-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or choose **Custom orientation** to provide your own exact orientation.</span></span>  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             <span data-ttu-id="49f0c-113">Sélectionner `Portrait upside down` dans la liste d' **orientation**</span><span class="sxs-lookup"><span data-stu-id="49f0c-113">Select `Portrait upside down` from the **Orientation** list</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="49f0c-114">Une fois l' **orientation personnalisée**sélectionnée, `alpha` les `beta` champs, et `gamma` sont activés.</span><span class="sxs-lookup"><span data-stu-id="49f0c-114">After you choose **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
          <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how each axis works.  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          <span data-ttu-id="49f0c-115">Vous pouvez également définir une orientation personnalisée en faisant glisser le modèle d' **orientation**.</span><span class="sxs-lookup"><span data-stu-id="49f0c-115">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="49f0c-116">Mettre `Shift` en attente avant de faire pivoter pour faire pivoter le long de l' `alpha` axe.</span><span class="sxs-lookup"><span data-stu-id="49f0c-116">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             <span data-ttu-id="49f0c-118">Le **modèle d’orientation**</span><span class="sxs-lookup"><span data-stu-id="49f0c-118">The **Orientation Model**</span></span>  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <span data-ttu-id="49f0c-119">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="49f0c-119">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> <span data-ttu-id="49f0c-120">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49f0c-120">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="49f0c-121">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="49f0c-121">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="49f0c-123">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="49f0c-123">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
