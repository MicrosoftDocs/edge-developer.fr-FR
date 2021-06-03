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
# <a name="simulate-device-orientation-with-microsoft-edge-devtools"></a>Simuler l’orientation de l’appareil Microsoft Edge DevTools  

Effectuer les actions suivantes pour simuler différentes orientations d’appareil Microsoft Edge DevTools.  

<!--todo: update device orientation section when available -->  

1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu Commande" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Menu **Commande**  
    :::image-end:::  
    
1.  Tapez `sensors` , choisissez Afficher les **capteurs,** puis sélectionnez `Enter` .  **L’outil** Capteurs s’ouvre en bas de la fenêtre DevTools.  
1.  Dans la **liste Orientation,** sélectionnez l’une des orientations prédéfines, par exemple, ou choisissez Orientation personnalisée pour fournir `Portrait upside down` votre propre orientation exacte. ****  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Choisir portrait à l’envers à partir de la liste Orientation" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             Choisir `Portrait upside down` dans la liste **Orientation**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Une fois que **vous avez choisi l’orientation**personnalisée, les champs et les champs `alpha` sont `beta` `gamma` activés.  
          <!--To understand how each axis works, navigate to [Alpha][alpha], [Beta][beta], and [Gamma][gamma].  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          Vous pouvez également définir une orientation personnalisée en faisant glisser le modèle **d’orientation.**  Maintenez `Shift` la main avant de faire glisser pour faire pivoter le long de `alpha` l’axe.  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Modèle d’orientation" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             Modèle **d’orientation**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
