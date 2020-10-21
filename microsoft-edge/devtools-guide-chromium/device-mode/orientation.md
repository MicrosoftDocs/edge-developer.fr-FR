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

# Simuler l’orientation de l’appareil avec Microsoft Edge DevTools  

Effectuez les opérations suivantes pour simuler différentes orientations d’appareil à partir de Microsoft Edge DevTools.  

<!--todo: update device orientation section when available -->  

1.  Sélectionnez `Control` + `Shift` + `P` \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-command-menu.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Tapez `sensors` , choisissez **afficher les capteurs**, puis sélectionnez `Enter` .  L’onglet **capteurs** s’ouvre en bas de la fenêtre devtools.  
1.  Dans la liste **orientation** , sélectionnez l’une des orientations prédéfinies, par exemple `Portrait upside down` , ou choisissez **orientation personnalisée** pour fournir votre propre orientation exacte.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             Sélectionner `Portrait upside down` dans la liste d' **orientation**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Une fois l' **orientation personnalisée**sélectionnée, `alpha` les `beta` champs, et `gamma` sont activés.  
          <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how each axis works.  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          Vous pouvez également définir une orientation personnalisée en faisant glisser le modèle d' **orientation**.  Mettre `Shift` en attente avant de faire pivoter pour faire pivoter le long de l' `alpha` axe.  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             Le **modèle d’orientation**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation & Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation & Motion"  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
