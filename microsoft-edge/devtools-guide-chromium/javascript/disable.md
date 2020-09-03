---
description: Ouvrez le menu de commandes et exécutez la commande «désactiver JavaScript».
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: de756e04c91768c49eed50debce97ae91fdaa3bd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10992798"
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

# Désactiver JavaScript avec Microsoft Edge DevTools  

Suivez les étapes ci-dessous pour voir l’apparence et le comportement d’une page Web lorsque JavaScript est désactivé.  

1.  [Ouvrez Microsoft Edge devtools][DevToolsOpen].  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Menu de commandes" lightbox="../media/javascript-console-command.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
1.  Commencez `javascript` à taper, sélectionnez **Désactiver JavaScript**, puis appuyez sur `Enter` la touche pour exécuter la commande.  JavaScript est désormais désactivé.  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Sélectionnez Désactiver JavaScript dans le menu de commandes." lightbox="../media/javascript-console-command-javascript.msft.png":::
       Sélectionnez **Désactiver JavaScript** dans le **menu de commandes** .  
    :::image-end:::  
    
    L’icône d’avertissement jaune en regard de **sources** vous rappelle que JavaScript est désactivé.  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Icône d’avertissement en regard de sources" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       Icône d’avertissement en regard de **sources**  
    :::image-end:::  
    
JavaScript reste désactivé dans l’onglet tant que vous avez DevTools ouvert.  

Vous pouvez vouloir recharger la page pour voir si et comment la page dépend de JavaScript lors du chargement.  

Pour réactiver JavaScript, effectuez les actions suivantes.  

*   Ouvrez à nouveau le **menu de commandes** et exécutez la `Enable JavaScript` commande.  
*   Fermez DevTools.  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
