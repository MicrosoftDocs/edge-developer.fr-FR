---
title: Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607425"
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





# Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools   

  

Utilisez le mode appareil pour obtenir un aperçu de l’apparence de votre page et de son exécution sur un appareil mobile.  

Le mode appareil est le nom de la collection libre de fonctionnalités dans Microsoft Edge DevTools qui vous permettent de simuler des appareils mobiles.  Ces fonctionnalités incluent:  

*   [Simulation d’une fenêtre d’affichage mobile](#simulate-a-mobile-viewport)  
*   [Limitation du réseau](#throttle-the-network-only)  
*   [Limitation de l’UC](#throttle-the-cpu-only)  
*   [Simulation de géolocalisation](#override-geolocation)  
*   [Définir l’orientation](#set-orientation)  

## Limitations   

Imaginez le mode appareil comme une [approximation prioritaire][WikiApproximation] de l’apparence de votre page sur un appareil mobile.  Le mode appareil n’exécute pas réellement votre code sur un appareil mobile.  Vous simulez l’expérience utilisateur mobile sur votre ordinateur portable ou votre ordinateur de bureau.  

Certains aspects des appareils mobiles qu’DevTools ne seront jamais en mesure de simuler.  Par exemple, l’architecture des UC mobiles est très différente de l’architecture de l’ordinateur portable ou de l’UC de bureau.  En cas de doute, il est préférable d’exécuter votre page sur un appareil mobile.  Pour afficher, modifier, déboguer et profiler le code d’une page à partir de votre ordinateur portable ou de votre ordinateur de bureau, vous pouvez utiliser [Remote Debugger] [DevToolsRemoteDebugging].  

## Simuler une fenêtre d’affichage mobile   

Cliquez sur **activer/désactiver** ![ le bouton bascule de la barre d’outils ][ImageDeviceToolbarIcon] de l’appareil pour ouvrir l’interface utilisateur qui vous permet de simuler une fenêtre d’affichage mobile.  

> ##### Figure1  
> Barre d’outils de l’appareil  
> ![Barre d’outils de l’appareil][ImageDeviceToolbar]  

Par défaut, la barre d’outils de l’appareil s’ouvre en mode de fenêtre d’affichage réactif.  

### Mode de fenêtre d’affichage réactif   

Faites glisser les poignées pour redimensionner la fenêtre d’affichage en fonction des dimensions dont vous avez besoin.  Vous avez d’autres valeurs dans les zones largeur et hauteur.  Dans la [figure 2](#figure-2), la largeur est définie sur `626` et la hauteur est définie sur `516` .  

> ##### Figure 2  
> Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif  
> ![Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif][ImageResponsiveHandles]  

#### Afficher les requêtes multimédias   

Pour afficher les points d’arrêt de requête multimédias au-dessus de votre fenêtre d’affichage, cliquez sur **plus d’options** , puis sélectionnez **afficher les requêtes multimédias**.  

> ##### Figure3  
> Afficher les requêtes multimédias  
> ![Afficher les requêtes multimédias][ImageShowMediaQueries]  

Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage de telle sorte que le point d’arrêt soit déclenché.  

> ##### Figure 4  
> Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage  
> ![Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage][ImageBreakpoint]  

#### Définir le type d’appareil   

Utilisez la liste **type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.  

> ##### Figure 5  
> Liste **type d’appareil**  
> ![Liste type d’appareil][ImageDeviceType]  

Le tableau ci-dessous décrit les différences entre les options.  La **méthode de rendu** fait référence à la façon dont Microsoft Edge effectue le rendu de la page en tant que fenêtre d’affichage mobile ou de bureau.  **Icône du curseur** désigne le type de curseur qui s’affiche lorsque vous survolez la page.  Les **événements déclenchés** font référence au déclenchement de la page `touch` ou aux `click` événements lorsque vous interagissez avec la page.  

| Option | Méthode de rendu | Icône du curseur | Événements déclenchés |  
|:--- |:--- |:--- |:--- |  
| Appareils mobiles | Appareils mobiles | Cercle | interface tactile |  
| Mobile \ (sans interaction | Appareils mobiles | Normal |  cliquez sur  |  
| Bureau | Bureau | Normal |  cliquez sur  |  
| Bureau \ (effleurement) | Bureau | Cercle | interface tactile |  

> [!NOTE]
> Si vous ne voyez pas la liste **type d’appareil** , cliquez sur plus d' **options** , puis sélectionnez Ajouter un **type d’appareil**.  

### Mode d’affichage de l’appareil mobile   

Pour simuler les dimensions d’un appareil mobile spécifique, sélectionnez-le dans la liste des **appareils** .  

> ##### Figure 6  
> La liste des appareils  
> ![La liste des appareils][ImageDeviceList]  

#### Faire pivoter la fenêtre d’affichage avec l’orientation paysage   

Cliquez **sur faire** pivoter faire pivoter ![ ][ImageRotateIcon] pour faire pivoter la fenêtre d’affichage en orientation paysage.  

> ##### Figure 7  
> Orientation paysage  
> ![Orientation paysage][ImageLandscape]  

> [!NOTE]
> Le bouton **faire pivoter** disparaît si la **barre d’outils** de votre appareil est étroite.  

> ##### Figure8  
> Barre d’outils de l’appareil  
> ![Barre d’outils de l’appareil][ImageDeviceToolbar2]  

Voir aussi [définir l’orientation](#set-orientation).  

#### Afficher le cadre de l’appareil   

Lors de la simulation des dimensions d’un appareil mobile spécifique comme un iPhone 6, ouvrez **plus d’options** , puis sélectionnez Afficher l' **image** de l’appareil pour afficher l’image de l’appareil physique dans la fenêtre d’affichage.  

> [!NOTE]
> Si vous ne voyez pas d’image d’appareil pour un appareil particulier, cela signifie probablement que DevTools n’a pas d’art pour cette option spécifique.  

> ##### Figure9  
> Afficher le cadre de l’appareil  
> ![Afficher le cadre de l’appareil][ImageShowDeviceFrame]  

> ##### Figure10  
> Le cadre de l’appareil pour l’iPhone 6  
> ![Le cadre de l’appareil pour l’iPhone 6][ImageIphoneFrame]  

#### Ajouter un appareil mobile personnalisé   

Pour ajouter un appareil personnalisé:  

1.  Cliquez sur la liste des **appareils** , puis sélectionnez **modifier**.  

> ##### Figure11  
> Sélectionner **modifier**la 
> ![ sélection modifier][ImageEdit]  

1.  Cliquez sur **Ajouter un appareil personnalisé**.  

1.  Entrez le nom, la largeur et la hauteur de l’appareil.  Le [coefficient d’appareil][MDNWindowDevicePixelRatio], la [chaîne de l’agent utilisateur][MDNUserAgent]et les champs [type d’appareil](#set-the-device-type) sont facultatifs.  Le champ type d’appareil est la liste qui est définie sur **mobile** par défaut.  

> ##### Figure12  
> Création d’un appareil personnalisé  
> ![Création d’un appareil personnalisé][ImageAddCustomDevice]  

### Afficher les règles   

Cliquez sur **autres options** , puis sélectionnez **afficher les règles** pour afficher les règles au-dessus et à gauche de votre fenêtre d’affichage.  L’unité de dimensionnement des règles est en pixels.  

> ##### Figure13  
> Afficher les règles  
> ![Afficher les règles][ImageShowRulers]  

> ##### Figure14  
> Règles au-dessus et à gauche de la fenêtre d’affichage  
> ![Règles au-dessus et à gauche de la fenêtre d’affichage][ImageRulers]  

### Effectuer un zoom dans la fenêtre d’affichage   

Utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.  

> ##### Figure15  
> Zoom  
> ![Zoom][ImageZoomViewport]  

## Limiter le réseau et le processeur   

Pour limiter le réseau et le processeur, sélectionnez mobile de **niveau moyen** ou **mobile** de niveau inférieur dans la liste **limitation** .  

> ##### Figure16  
> La liste des limitations  
> ![La liste des limitations][ImageThrottling]  

Le **mobile de niveau supérieur** simule un réseau 3G rapide et accélère votre processeur de manière à ce qu’il soit 4 fois plus lent qu’normal.  Le **téléphone mobile de faible fin** simule un réseau 3G lent et limite votre UC de 6 temps de plus en plus lente.  Gardez à l’esprit que la limitation dépend de la fonctionnalité normale de votre ordinateur portable ou de votre ordinateur de bureau.  

> [!NOTE]
> La liste des **limitations** sera masquée si la **barre d’outils** de votre appareil est étroite.  

> ##### Figure17  
> Barre d’outils de l’appareil  
> ![Barre d’outils de l’appareil][ImageDeviceToolbar3]  

### Limiter le processeur uniquement   

Pour limiter le processeur uniquement, et non le réseau, accédez au panneau **performances** , cliquez sur paramètres de capture des **paramètres de capture** ![ ][ImageCaptureIcon] , puis sélectionnez **4x Slowdown** ou **6 ralentissement** dans la liste **processeur** .  

> ##### Figure 18  
> Liste UC  
> ![Liste UC][ImageCPU]  

### Limiter le réseau uniquement   

Pour limiter le réseau et non le processeur, accédez au panneau **réseau** et sélectionnez **Fast 3G** ou **lente 3G** dans la liste **limitation** .  

> ##### Figure 19  
> La liste des limitations  
> ![La liste des limitations][ImageNetwork]  

`Control` + `Shift` + `P` Vous pouvez appuyer sur \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `3G` , puis sélectionner **activer la limitation Fast 3G** ou **activer la limitation 3G lente**.  

> ##### Figure 20  
> Menu de commandes  
> ![Menu de commandes][ImageCommandMenu]  

Vous pouvez également définir la limitation du réseau dans le panneau **performances** .  Cliquez sur paramètres de capture **paramètres** ![ ][ImageCaptureIcon] de capture, puis sélectionnez **Fast 3G** ou **lente 3G** dans la liste **réseau** .  

> ##### Figure 21  
> Configuration de la limitation du réseau à partir du panneau performances  
> ![Configuration de la limitation du réseau à partir du panneau performances][ImageNetwork2]  

## Remplacer la géolocalisation   

Pour ouvrir l’interface utilisateur de remplacement de géolocalisation cliquez sur **personnaliser et contrôler devtools** `...` , puis sélectionnez **autres**  >  **capteurs**d’outils.  

> ##### Figure 22  
> Capteurs  
> ![Capteurs][ImageSensors]  

Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.  

> ##### Figure 23  
> Afficher les capteurs  
> ![Afficher les capteurs][ImageShowSensors]  

Sélectionnez l’une des présélections dans la liste **géolocalisation** ou sélectionnez **emplacement personnalisé** pour entrer vos propres coordonnées, ou sélectionnez **emplacement non disponible** pour tester le comportement de votre page lorsque la géolocalisation est dans un état d’erreur.  

> ##### Figure 24  
> Géolocalisation  
> ![Géolocalisation][ImageGeolocation]  

## Définir l’orientation   

Pour ouvrir l’interface utilisateur d’orientation, cliquez sur **personnaliser et contrôler devtools** `...` puis sélectionnez **autres**  >  **capteurs**d’outils.  

> ##### Figure 25  
> Capteurs  
> ![Capteurs][ImageSensors2]  

Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.  

> ##### Figure 26  
> Afficher les capteurs  
> ![Afficher les capteurs][ImageShowSensors2]  

Sélectionnez l’une des présélections dans la liste **orientation** ou sélectionnez **orientation personnalisée** pour définir vos propres valeurs alpha, bêta et gamma.  

> ##### Figure 27  
> Orientation  
> ![Orientation][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figure 1: barre d’outils de l’appareil"  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Figure 2: poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Figure 3: afficher les requêtes multimédias"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Figure 4: cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage"  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Figure 5: liste type d’appareil"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Figure 6: liste des appareils"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Figure 7: orientation paysage"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figure 8: barre d’outils de l’appareil"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Figure 9: afficher le cadre de l’appareil"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Figure 10: cadre de l’appareil pour iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Figure 11: sélectionner Modifier"  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Figure 12: création d’un appareil personnalisé"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Figure 13: afficher les règles"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Figure 14: règles au-dessus et à gauche de la fenêtre d’affichage"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Figure 15: zoom"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Figure 16: liste de limitation"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Figure 17: barre d’outils de l’appareil"  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Figure 18: liste UC"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "Figure 19: liste de limitation"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Figure 20: menu de commandes"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Figure 21: configuration de la limitation du réseau à partir du panneau performances"  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figure 22: capteurs"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figure 23: afficher les capteurs"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Figure 24: géolocalisation"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Figure 25: capteurs"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Figure 26: afficher les capteurs"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Figure 27: orientation"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/devtools-Guide-Chromium/Remote-Debugging/index "prenez en main les appareils Android de débogage à distance"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Ordre de rapprochement-premier-ordre-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
