---
description: Ouvrez l’outil Capteurs et sélectionnez les coordonnées dans la liste géolocalisation.
title: Remplacer la géolocalisation avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 8f6ad09b2f8db110f6743aae32e16cc9b1185400
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399000"
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

# <a name="override-geolocation-with-microsoft-edge-devtools"></a>Remplacer la géolocalisation avec Microsoft Edge DevTools  

De nombreux sites web tirez parti de l’emplacement des utilisateurs afin de fournir une expérience plus pertinente aux utilisateurs.  Par exemple, un site web météo peut afficher les prévisions locales dans la zone d’un utilisateur, une fois que l’utilisateur a accordé au site web l’autorisation d’accéder à l’emplacement de l’utilisateur actuel.  

<!--todo: add link to user location section when available -->  

Si vous construisez une interface utilisateur qui change en fonction de l’emplacement de l’utilisateur, vous souhaitez probablement vous assurer que le site se comporte correctement à différents endroits dans le monde.  Pour remplacer votre géolocalisation dans Microsoft Edge DevTools, effectuer les actions suivantes.  

1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) pour ouvrir le **menu Commande.**  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu Commande" lightbox="../media/device-mode-console-command-menu.msft.png":::
       Menu **Commande**  
    :::image-end:::  
    
1.  Tapez `sensors` , choisissez Afficher les **capteurs,** puis sélectionnez `Enter` .  **L’outil** Capteurs s’ouvre en bas de votre fenêtre DevTools.  
1.  Dans la liste **Géolocalisation,** sélectionnez l’une des villes prédéfinies, comme , ou choisissez Emplacement personnalisé pour entrer des coordonnées personnalisées de longitude et de latitude, ou choisissez Emplacement indisponible pour afficher le comportement de votre site lorsque `Tokyo` l’emplacement de **** l’utilisateur n’est pas disponible. ****  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Choisir Tokyo dans la liste géolocalisation" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Choisir `Tokyo` dans la liste **géolocalisation**  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
