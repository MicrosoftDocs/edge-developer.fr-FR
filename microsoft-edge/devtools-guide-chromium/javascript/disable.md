---
title: Désactiver JavaScript avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f3838b4e8eccf83aaa71be35ff477ec56cbe7455
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581809"
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



Pour afficher un aperçu d’une page Web lorsque JavaScript est désactivé:  

1.  [Ouvrez Microsoft Edge devtools][DevToolsOpen].  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.  
    
    > ##### Figure1  
    > Menu de commandes  
    > ![Menu de commandes][ImageCommandMenu]  
    
1.  Commencez `javascript` à taper, sélectionnez **Désactiver JavaScript**, puis appuyez sur `Enter` la touche pour exécuter la commande.  JavaScript est désormais désactivé.  
    
    > ##### Figure 2  
    > Sélection de l’option **Désactiver JavaScript** dans le menu de commandes  
    > ![Sélection de l’option désactiver JavaScript dans le menu de commandes][ImageDisableJS]  
    
    L’icône d’avertissement jaune en regard de **sources** vous rappelle que JavaScript est désactivé.  
    
    > ##### Figure3  
    > Icône d’avertissement en regard de **sources**  
    > ![Icône d’avertissement en regard de sources][ImageDisableJSWarning]  

JavaScript reste désactivé dans cet onglet tant que vous avez DevTools ouvert.  

Vous pouvez vouloir recharger la page pour voir si et comment la page dépend de JavaScript lors du chargement.  

Pour réactiver JavaScript:  

*   Ouvrez à nouveau le **menu de commandes** et exécutez la `Enable JavaScript` commande.  
*   Fermez DevTools.  

## Commentaires   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Figure 1: menu de commandes"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Figure 2: sélectionnez Désactiver JavaScript dans le menu de commandes"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Figure 3: icône d’avertissement en regard de sources"  

<!-- links -->  

[DevToolsOpen]: ../open.md "Ouvrir Microsoft Edge DevTools"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
