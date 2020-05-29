---
title: Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601345"
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





# Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)   



Par défaut, DevTools est ancré à droite de votre fenêtre d’affichage.  Vous pouvez également ancrer en bas, ancrer à gauche, ou détacher la DevTools dans une autre fenêtre.  

> ##### Figure1  
> Ancrer à gauche  
> ![Ancrer à gauche][ImageDockLeft]  

> ##### Figure 2  
> Ancrer en bas  
> ![Ancrer en bas][ImageDockBottom]  

> ##### Figure3  
> Navigateur dans une fenêtre séparée  
> ![Navigateur dans une fenêtre séparée][ImageUndockBrowser]  

> ##### Figure 4  
> DevTools non attaché dans une fenêtre séparée  
> ![DevTools non attaché dans une fenêtre séparée][ImageUndockDevTools]  

## Changer la position dans le menu principal   

1.  Cliquez sur **personnaliser et contrôler devtools** `...` et sélectionnez **détacher dans une fenêtre indépendante** ![ ][ImageUndockIcon] , **ancrer** en bas ![ à ][ImageBottomIcon] gauche ou **Dock To Left** ![ ][ImageLeftIcon] ancrer à gauche.  
    
    > ##### Figure 5  
    > Sélection du **retrait dans une fenêtre séparée**  
    > ![Sélection du retrait dans une fenêtre séparée][ImageUndockSettings]  
    
## Changer le positionnement dans le menu de commandes   

1.  [Ouvrir le menu de commandes][DevtoolsCommandMenu].  
1.  Exécutez l’une des commandes `Dock To Bottom` suivantes: `Undock Into Separate Window`  Il n’existe actuellement aucune commande pour l’ancrage à gauche, mais vous pouvez y accéder à partir du [menu principal](#change-placement-from-the-main-menu).  
    
    > ##### Figure 6  
    > Commande détacher  
    > ![Commande détacher][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Figure 1: ancrer sur la gauche"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Figure 2: ancrer en bas"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Figure 3: navigateur dans une fenêtre séparée"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Figure 4: DevTools non attaché dans une fenêtre séparée"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Figure 5: sélectionner détacher dans une fenêtre séparée"  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Figure 6: commande détacher"  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/customize/placement) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
