---
description: Ouvrez l’onglet capteurs et sélectionnez coordonnées dans la liste géolocalisation.
title: Remplacer le géolocalisation avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 269e7ca4bf259aa168c06ac0fd915604731463c4
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992987"
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

# Remplacer le géolocalisation avec Microsoft Edge DevTools  

De nombreux sites Web tirent parti de l’emplacement de l’utilisateur, afin de fournir une utilisation plus pertinente aux utilisateurs.  Par exemple, un site Web météo peut afficher la prévision locale dans la zone d’un utilisateur, une fois que l’utilisateur a accordé l’autorisation de site Web pour accéder à l’emplacement actuel de l’utilisateur.  

<!--todo: add link to user location section when available -->  

Si vous créez une interface utilisateur qui change en fonction de l’emplacement de l’utilisateur, vous devez probablement vous assurer que le site se comporte correctement à différents emplacements du monde.  Pour ignorer votre géolocalisation dans Microsoft Edge DevTools, effectuez les actions suivantes.  

1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-command-menu.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Tapez `sensors` , sélectionnez **afficher les capteurs**, puis appuyez sur `Enter` .  L’onglet **capteurs** s’ouvre en bas de la fenêtre devtools.  
1.  Dans la liste de **géolocalisation** , sélectionnez l’une des villes prédéfinies, par exemple `Tokyo` , ou sélectionnez **emplacement personnalisé** pour entrer des coordonnées de longitude et de latitude personnalisées, ou sélectionnez **emplacement non disponible** pour voir l’apparence de votre site lorsque l’emplacement de l’utilisateur n’est pas disponible.  
    
    :::image type="complex" source="../media/device-mode-console-sensors-geolocation-tokyo.msft.png" alt-text="Sélectionner Tokyo dans la liste de géolocalisation" lightbox="../media/device-mode-console-sensors-geolocation-tokyo.msft.png":::
       Sélectionner `Tokyo` dans la liste de **géolocalisation**  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
