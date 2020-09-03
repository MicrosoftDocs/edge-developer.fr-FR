---
description: Ouvrez l’onglet conditions du réseau, désactivez l’option sélectionner automatiquement, puis choisissez dans la liste ou entrez une chaîne personnalisée.
title: Remplacement de la chaîne de l’agent utilisateur à partir de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ecaa1247824e5c3acb07a2c631feab30d25aba8d
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992924"
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

# Remplacement de la chaîne de l’agent utilisateur à partir de Microsoft Edge DevTools  

Pour remplacer la chaîne de l' [agent utilisateur][MDNUserAgent] à partir de Microsoft Edge devtools:  

1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-console-command-menu.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Tapez `network conditions` , sélectionnez **afficher les conditions du réseau**, puis appuyez `Enter` sur l’onglet **conditions réseau** pour l’ouvrir.  
1.  Dans la section **agent utilisateur** , désactivez la case à cocher **sélectionner automatiquement** .  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Désactiver l’option sélectionner automatiquement" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       Désactiver l' **option sélectionner automatiquement**  
    :::image-end:::  
    
1.  Sélectionnez une chaîne d’agent utilisateur dans la liste ou entrez votre propre chaîne personnalisée.  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
