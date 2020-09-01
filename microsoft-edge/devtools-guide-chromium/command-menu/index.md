---
title: Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 09adaadd6f62710b219911f69fbe39ba8edfb61a
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982544"
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





# Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools   

  

Le menu de commandes fournit un moyen rapide de naviguer dans l’interface utilisateur de Microsoft Edge DevTools et d’accomplir des tâches courantes, telles que la [désactivation de JavaScript][JavascriptDisable].  Il est possible que vous connaissiez une fonctionnalité semblable dans le code Visual Studio appelé [palette de commandes][VisualStudioCodeUICommandPalette], qui était l’original du menu de commandes.  

:::image type="complex" source="../media/command-menu-run-command-java.msft.png" alt-text="Utiliser le menu de commande pour désactiver JavaScript" lightbox="../media/command-menu-run-command-java.msft.png":::
   Utiliser le menu de commande pour désactiver JavaScript  
:::image-end:::  

## Ouvrir le menu de commandes   

Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \). Vous avez le choix entre les commandes **personnaliser et contrôler devtools** `...` , puis sélectionner **exécuter**.  

:::image type="complex" source="../media/command-menu-options-run-command.msft.png" alt-text="Commande exécuter" lightbox="../media/command-menu-options-run-command.msft.png":::
   Commande exécuter  
:::image-end:::  

## Afficher les autres actions disponibles   

Si vous utilisez le flux de travail en mode plan dans [ouvrir le menu](#open-the-command-menu)de commandes, le menu de commandes s’ouvre avec un préfixe de `>` caractère dans la zone de texte menu de commandes.  

:::image type="complex" source="../media/command-menu-run-command.msft.png" alt-text="Le caractère de commande" lightbox="../media/command-menu-run-command.msft.png":::
   Le caractère de commande  
:::image-end:::  

Supprimez le `>` caractère et tapez `?` pour afficher d’autres actions disponibles dans le menu de commandes.  

:::image type="complex" source="../media/command-menu-help.msft.png" alt-text="Autres actions disponibles" lightbox="../media/command-menu-help.msft.png":::
   Autres actions disponibles  
:::image-end:::  

 



<!-- links -->  

[JavascriptDisable]: ../javascript/disable.md "Désactiver JavaScript avec Microsoft Edge DevTools | Documents Microsoft"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Palette de commandes-interface utilisateur de code Visual Studio"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
