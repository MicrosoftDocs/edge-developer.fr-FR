---
title: Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 6973f28a0cb530e8928976adb1354fa7471ee343
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985260"
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

Cliquez sur le **bouton bascule de la barre d’outils** de l’appareil \ ( ![ activez la barre d’outils de ][ImageDeviceToolbarIcon] l’appareil \) pour ouvrir l’interface utilisateur qui vous permet de simuler une fenêtre d’affichage mobile.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Barre d’outils de l’appareil  
:::image-end:::  

Par défaut, la barre d’outils de l’appareil s’ouvre en mode de fenêtre d’affichage réactif.  

### Mode de fenêtre d’affichage réactif   

Faites glisser les poignées pour redimensionner la fenêtre d’affichage en fonction des dimensions dont vous avez besoin.  Vous avez d’autres valeurs dans les zones largeur et hauteur.  Dans l’illustration suivante, la largeur est définie sur `626` et la hauteur est définie sur `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif  
:::image-end:::  

#### Afficher les requêtes multimédias   

Pour afficher les points d’arrêt de requête multimédias au-dessus de votre fenêtre d’affichage, cliquez sur **plus d’options** , puis sélectionnez **afficher les requêtes multimédias**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Afficher les requêtes multimédias" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Afficher les requêtes multimédias**  
:::image-end:::  

Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage de telle sorte que le point d’arrêt soit déclenché.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Cliquez sur un point d’arrêt pour modifier la largeur de la fenêtre d’affichage  
:::image-end:::  

#### Définir le type d’appareil   

Utilisez la liste **type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste type d’appareil" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Liste **type d’appareil**  
:::image-end:::  

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

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La liste des appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   La liste des **appareils**  
:::image-end:::  

#### Faire pivoter la fenêtre d’affichage avec l’orientation paysage   

Cliquez sur **faire pivoter** \ ( ![ faire pivoter ][ImageRotateIcon] ) pour faire pivoter la fenêtre d’affichage en orientation paysage.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Orientation paysage" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   Orientation paysage  
:::image-end:::  

> [!NOTE]
> Le bouton **faire pivoter** disparaît si la **barre d’outils** de votre appareil est étroite.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Barre d’outils** de l’appareil  
:::image-end:::  

Voir aussi [définir l’orientation](#set-orientation).  

#### Afficher le cadre de l’appareil   

Lors de la simulation des dimensions d’un appareil mobile spécifique comme un iPhone 6, ouvrez **plus d’options** , puis sélectionnez Afficher l' **image** de l’appareil pour afficher l’image de l’appareil physique dans la fenêtre d’affichage.  

> [!NOTE]
> Si vous ne voyez pas d’image d’appareil pour un appareil particulier, cela signifie probablement que DevTools n’a pas d’art pour cette option spécifique.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Afficher le cadre de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Afficher le cadre de l’appareil  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Le cadre de l’appareil pour l’iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Le cadre de l’appareil pour l’iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Ajouter un appareil mobile personnalisé   

Pour ajouter un appareil personnalisé:  

1.  Cliquez sur la liste des **appareils** , puis sélectionnez **modifier**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Sélectionnez Modifier." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Sélectionnez **modifier** .  
    :::image-end:::  
    
1.  Cliquez sur **Ajouter un appareil personnalisé**.  
1.  Entrez le nom, la largeur et la hauteur de l’appareil.  Le [coefficient d’appareil][MDNWindowDevicePixelRatio], la [chaîne de l’agent utilisateur][MDNUserAgent]et les champs [type d’appareil](#set-the-device-type) sont facultatifs.  Le champ type d’appareil est la liste qui est définie sur **mobile** par défaut.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Créer un appareil personnalisé" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Appareil personnalisé de création  
    :::image-end:::  

### Afficher les règles   

Cliquez sur **autres options** , puis sélectionnez **afficher les règles** pour afficher les règles au-dessus et à gauche de votre fenêtre d’affichage.  L’unité de dimensionnement des règles est en pixels.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Afficher les règles" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **Afficher les règles**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Règles au-dessus et à gauche de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Règles au-dessus et à gauche de la fenêtre d’affichage  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Effectuer un zoom dans la fenêtre d’affichage   

Utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Limiter le réseau et le processeur   

Pour limiter le réseau et le processeur, sélectionnez mobile de **niveau moyen** ou **mobile** de niveau inférieur dans la liste **limitation** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="La liste des limitations" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   La liste des **limitations**  
:::image-end:::  

Le **mobile de niveau supérieur** simule un réseau 3G rapide et accélère votre processeur de manière à ce qu’il soit 4 fois plus lent qu’normal.  Le **téléphone mobile de faible fin** simule un réseau 3G lent et limite votre UC de 6 temps de plus en plus lente.  Gardez à l’esprit que la limitation dépend de la fonctionnalité normale de votre ordinateur portable ou de votre ordinateur de bureau.  

> [!NOTE]
> La liste des **limitations** est cachée si la **barre d’outils** de votre appareil est étroite.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Barre d’outils** de l’appareil  
:::image-end:::  

### Limiter le processeur uniquement   

Pour limiter le processeur uniquement, et non le réseau, accédez au panneau **performance** , cliquez sur **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \), puis sélectionnez **4x Slowdown** ou en 6 points de **ralentissement** dans la liste **processeur** .  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Liste UC" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   Liste **UC**  
:::image-end:::  

### Limiter le réseau uniquement   

Pour limiter le réseau et non le processeur, accédez au panneau **réseau** et sélectionnez **Fast 3G** ou **lente 3G** dans la liste **limitation** .  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="La liste des limitations" lightbox="../media/device-mode-network-throttle.msft.png":::
   La liste des **limitations**  
:::image-end:::  

`Control` + `Shift` + `P` Vous pouvez appuyer sur \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**, taper `3G` , puis sélectionner **activer la limitation Fast 3G** ou **activer la limitation 3G lente**.  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   **Menu de commandes**  
:::image-end:::  

Vous pouvez également définir la limitation du réseau dans le panneau **performances** .  Cliquez sur **paramètres de capture** \ (paramètres de ![ capture ][ImageCaptureIcon] \), puis sélectionnez **Fast 3G** ou **lente 3G** dans la liste **réseau** .  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Définir la limitation du réseau à partir du panneau performances" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   Définir la limitation du réseau à partir du panneau **performances**  
:::image-end:::  

## Remplacer la géolocalisation   

Pour ouvrir l’interface utilisateur de remplacement de géolocalisation cliquez sur **personnaliser et contrôler devtools** \ ( `...` \), puis sélectionnez **autres**  >  **capteurs**d’outils.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **Capteurs**  
:::image-end:::  

Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **Afficher les capteurs**  
:::image-end:::  

Sélectionnez l’une des présélections dans la liste **géolocalisation** ou sélectionnez **emplacement personnalisé** pour entrer vos propres coordonnées, ou sélectionnez **emplacement non disponible** pour tester le comportement de votre page lorsque la géolocalisation est dans un état d’erreur.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **Géolocalisation**  
:::image-end:::  

## Définir l’orientation   

:::row:::
   :::column span="":::
      Pour ouvrir l’interface utilisateur d’orientation, cliquez sur **personnaliser et contrôler devtools** `...` puis sélectionnez **autres**  >  **capteurs**d’outils.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Capteurs**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Vous pouvez ou appuyer sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, taper `Sensors` , puis sélectionner **afficher les capteurs**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Afficher les capteurs**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Sélectionnez l’une des présélections dans la liste **orientation** ou sélectionnez **orientation personnalisée** pour définir vos propres valeurs alpha, bêta et gamma.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Orientation" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **Orientation**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "mise en route des appareils Android de débogage à distance | Documents Microsoft  

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
