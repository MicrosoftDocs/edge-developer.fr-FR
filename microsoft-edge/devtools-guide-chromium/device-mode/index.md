---
description: Utilisez des périphériques virtuels dans Microsoft Edge pour créer des sites Web de premier prénom.
title: Émuler des appareils mobiles dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, émulation, appareil, simulation, mobile
ms.openlocfilehash: c70b81eabb145461eac7d1b9a8f438d6a18fbc89
ms.sourcegitcommit: cc96ada9679b23feb841e46f19d8077251c4a4df
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "10997061"
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

# Émuler des appareils mobiles dans Microsoft Edge DevTools  

Utilisez l' **émulation d’appareil** pour rapprocher l’apparence de votre page et la réponse sur un appareil mobile.  Le Microsoft Edge DevTools fournit un ensemble de fonctionnalités pour vous aider à émuler les appareils mobiles.  La collection inclut les fonctionnalités suivantes.  

*   [Simuler une fenêtre d’affichage mobile](#simulate-a-mobile-viewport)  
*   [Limiter le réseau](#throttle-the-network-only)  
*   [Limiter le processeur](#throttle-the-cpu-only)  
*   [Simuler géolocalisation](#override-geolocation)  
*   [Définir l’orientation](#set-orientation)  
*   [Définir la chaîne de l’agent utilisateur](#set-user-agent-string)  

## Limitations  

L' **émulation d’appareil** est une [approximation première commande][WikiApproximation] de l’apparence de votre page sur un appareil mobile.  L' **émulation d’appareil** n’exécute pas réellement votre code sur un appareil mobile.  À la place, vous simulez l’expérience utilisateur mobile sur votre ordinateur portable ou votre ordinateur de bureau.  

Certains aspects des appareils mobiles ne sont jamais émulés dans DevTools.  Par exemple, l’architecture des UC mobiles est différente de l’architecture de l’ordinateur portable ou de l’UC de bureau.  En cas de doute, il est préférable d’exécuter votre page sur un appareil mobile.  Utilisez [débogage à distance] [DevToolsRemoteDebugging] pour interagir avec le code d’une page à partir de votre ordinateur, tandis que votre page s’exécute réellement sur un appareil mobile.  Vous pouvez afficher, modifier, déboguer, profiler ou les quatre lorsque vous interagissez avec le code.  Votre ordinateur est-il possible d’un bloc-notes ou d’un ordinateur de bureau.  

## Simuler une fenêtre d’affichage mobile  

Sélectionnez **basculer l’émulation d’appareil**  \ ( ![ activez la barre d’outils de l’appareil ][ImageDeviceToolbarIcon] \) ou sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > l' **émulation d’appareil** pour ouvrir l’interface utilisateur qui vous permet de simuler une fenêtre d’affichage mobile.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    Barre d’outils de l’appareil  
:::image-end:::  

Par défaut, la barre d’outils de l’appareil s’ouvre en mode de fenêtre d’affichage réactif.  

### Mode de fenêtre d’affichage réactif  

Pour tester rapidement l’aspect de votre page sur plusieurs tailles d’écran, faites glisser les poignées pour redimensionner la fenêtre d’affichage selon vos besoins.  Vous pouvez également entrer des valeurs spécifiques dans les zones largeur et hauteur.  Dans l’illustration suivante, la largeur est définie sur `626` et la hauteur est définie sur `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Poignées permettant de modifier les dimensions de la fenêtre d’affichage en mode de fenêtre d’affichage réactif  
:::image-end:::  

#### Afficher les requêtes multimédias  

Si vous avez défini des requêtes multimédias sur votre page, accédez aux dimensions de la fenêtre d’affichage dans lesquelles ces requêtes multimédias sont prises en compte en affichant des points d’arrêt de requête multimédia au-dessus de votre fenêtre d’affichage.  Sélectionnez **autres options**  >  **afficher les requêtes multimédias**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Afficher les requêtes multimédias" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Afficher les requêtes multimédias**  
:::image-end:::  

Choisissez un point d’arrêt pour modifier la largeur de la fenêtre d’affichage de telle sorte que la requête multimédia soit déclenchée.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Sélectionner un point d’arrêt pour modifier la largeur de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Sélectionner un point d’arrêt pour modifier la largeur de la fenêtre d’affichage  
:::image-end:::  

#### Définir le type d’appareil  

Utilisez la liste **type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste type d’appareil" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Liste **type d’appareil**  
:::image-end:::  

Le tableau suivant décrit les différences entre les options de type d’appareil disponibles.  La colonne méthode de rendu fait référence au rendu de la page par Microsoft Edge en tant qu’affichage mobile ou de bureau.  La colonne icône du curseur fait référence au type de curseur qui s’affiche lorsque vous pointez sur la page.  La colonne déclenchée Events indique si la page déclenche ou a des `touch` `click` événements lorsque vous interagissez avec la page.  

| Option | Méthode de rendu | Icône du curseur | Événements déclenchés |  
|:--- |:--- |:--- |:--- |  
| Appareils mobiles | Appareils mobiles | Cercle | interface tactile |  
| Mobile \ (sans interaction | Appareils mobiles | Normal |  cliquez sur  |  
| Bureau | Bureau | Normal |  cliquez sur  |  
| Bureau \ (effleurement) | Bureau | Cercle | interface tactile |  

> [!NOTE]
> Si la liste **type d’appareil** n’est pas affichée, sélectionnez **autres options**  >  **Ajouter un type d’appareil**.  

### Mode d’affichage de l’appareil mobile  

Pour simuler les dimensions d’un appareil mobile spécifique, sélectionnez-le dans la liste des **appareils** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="La liste des appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   La liste des **appareils**  
:::image-end:::  

#### Faire pivoter la fenêtre d’affichage avec l’orientation paysage  

Testez votre page Web en orientation paysage.  

*   Pour faire pivoter la fenêtre d’affichage en orientation paysage, sélectionnez **faire pivoter** \ ( ![ rotation ][ImageRotateIcon] \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Page affichée en orientation paysage" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Page affichée en orientation paysage  
    :::image-end:::  
    
> [!NOTE]
> Le bouton **faire pivoter** disparaît si la **barre d’outils** de votre appareil est étroite.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Barre d’outils** de l’appareil  
:::image-end:::  

Pour plus d’informations, voir [définir l’orientation](#set-orientation).  

#### Afficher le cadre de l’appareil  

Affichez le frame d’appareil physique à l’écran de la fenêtre d’affichage lorsque vous simulez les dimensions d’un appareil mobile spécifique tel qu’un iPhone 6.  

1.  Ouvrez **plus d’options**.  
1.  Sélectionnez **afficher le cadre**de l’appareil.  

> [!NOTE]
> Si vous ne voyez pas d’image d’appareil pour un appareil particulier, cela signifie que DevTools n’a pas d’image pour cette option.  

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

Si l’option d’appareil mobile dont vous avez besoin ne figure pas dans la liste par défaut, vous pouvez ajouter un appareil personnalisé.  Pour ajouter un appareil personnalisé, procédez comme suit.  

1.  Choisissez la liste des **appareils** > **modifier**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Sélectionnez Modifier." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Sélectionnez **modifier** .  
    :::image-end:::  
    
1.  Sélectionnez **Ajouter un appareil personnalisé**.  
1.  Sur les **appareils émulés**, entrez le nom d’un appareil, la largeur de l’écran et la hauteur de l’écran de l’appareil personnalisé.  Le [coefficient d’appareil][MDNWindowDevicePixelRatio], la [chaîne de l’agent utilisateur][MDNUserAgent]et les champs [type d’appareil](#set-the-device-type) sont facultatifs.  Le champ type d’appareil utilise par défaut la valeur **mobile**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Créer un appareil personnalisé" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Créer un appareil personnalisé  
    :::image-end:::  
    
### Afficher les règles  

Si vous avez besoin de mesurer les dimensions de l’écran, vous pouvez utiliser des règles pour mesurer la taille de l’écran en pixels.  Sélectionnez **autres options**  >  **afficher les règles** pour afficher les règles au-dessus et à gauche de votre fenêtre d’affichage.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Option de menu pour afficher les règles" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Option de menu pour afficher les règles  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Règles au-dessus et à gauche de la fenêtre d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Règles au-dessus et à gauche de la fenêtre d’affichage  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### Effectuer un zoom dans la fenêtre d’affichage  

Pour tester l’apparence de votre page à plusieurs niveaux de zoom, utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## Limiter le réseau et le processeur  

Les appareils mobiles sont souvent dotés de contraintes réseau et UC.  Assurez-vous d’avoir testé la rapidité de chargement de la page et la manière dont elle réagit aux différentes vitesses d’utilisation de l’Internet et du processeur.  

Limiter le réseau et le processeur.  

1.  Choisissez liste de **limitations** et sélectionnez mobile de **niveau supérieur** ou mobile de niveau **inférieur**.  
    *   Le **mobile milieu de niveau** simule `fast 3G` et limite votre processeur.  Il est quatre fois plus lent qu’normal.  
    *   Un **mobile de bas de gamme** simule `slow 3G` et limite votre processeur.  Il est plus lent que le nombre normal.  
    
Toutes les limitations dépendent de la fonctionnalité normale de votre ordinateur portable ou de votre ordinateur de bureau.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Liste de limitations de la barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Liste de **limitations** de la barre d’outils de l’appareil  
:::image-end:::  

> [!NOTE]
> Si la **liste des limitations** est masquée, votre **barre d’outils** de l’appareil est trop étroite.  Pour accéder à la **liste de limitation**, augmentez la largeur de la **barre d’outils**de l’appareil.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Barre d’outils** de l’appareil  
:::image-end:::  

### Limiter le processeur uniquement  

Pour limiter le processeur et non le réseau, procédez comme suit.

1.  Sélectionnez le panneau **performances** , puis choisissez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \).
1.  Sélectionnez **CPU**  >  **ralentissement** de l’UC 4x ou **6 ralentissements**.
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Liste UC du panneau de performance" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Liste **UC** du panneau de **performance**  
    :::image-end:::  
    
### Limiter le réseau uniquement  

Pour limiter le réseau uniquement, procédez comme suit.

1.  Choisissez le panneau **réseau** .
1.  Choisissez **connexion**  >  **Fast 3G** ou **lente 3G**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Liste de limitations du panneau réseau" lightbox="../media/device-mode-network-throttle.msft.png":::
       Liste de **limitations** du panneau réseau  
    :::image-end:::  
    
    `Control` + `Shift` + `P` Vous pouvez sélectionner \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**, taper `3G` , puis sélectionner **activer la limitation Fast 3G** ou **activer la limitation 3G lente**.  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menu de commandes" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       **Menu de commandes**  
    :::image-end:::  
    
Vous pouvez également définir la limitation du réseau dans le panneau **performances** .  

1.  Sélectionnez **paramètres de capture** \ ( ![ paramètres de capture ][ImageCaptureIcon] \), puis choisissez la liste des **réseaux** et définissez le paramètre prédéfini sur **Fast 3G** ou **lente 3G**.  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Définir la limitation du réseau à partir du panneau performances" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Définir la limitation du réseau à partir du panneau **performances**  
    :::image-end:::  
    
## Remplacer la géolocalisation  

:::row:::
   :::column span="":::
      Si votre page dépend d’informations géolocalisation d’un appareil mobile pour s’afficher correctement, fournissez des géolocalisation différentes à l’aide de l’interface utilisateur de remplacement de géolocalisation.  

      1.  Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus**de  >  **capteurs**d’outils.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Capteurs** pour la géolocalisation  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Ouvrir le menu de commandes.  
          *   Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).  
      1. Tapez `Sensors` , puis sélectionnez **afficher les capteurs**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Afficher les capteurs** pour la géolocalisation  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Dans le panneau **capteurs** , vous pouvez sélectionner l’un des emplacements prédéfinis inclus dans devtools à l’aide du menu déroulant **emplacement** .  Pour entrer un emplacement personnalisé, sélectionnez **autres...** et entrez les coordonnées de votre emplacement personnalisé.  Pour tester votre page dans un état d’erreur lorsque les informations de géolocalisation ne sont pas disponibles, sélectionnez **emplacement non disponible**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Panneau capteurs avec une position prédéfinie sélectionnée" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    Panneau **capteurs** avec une position prédéfinie sélectionnée  
:::image-end:::

## Définir l’orientation  

:::row:::
   :::column span="":::
      Si votre page dépend des informations d’orientation d’un appareil mobile pour s’afficher correctement, ouvrez l’interface utilisateur d’orientation.  

      1.  Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus**de  >  **capteurs**d’outils.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs d’orientation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Capteurs** d’orientation  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Ouvrir le menu de commandes.  
          *   Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).  
      1. Tapez `Sensors` , puis sélectionnez **afficher les capteurs**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs d’orientation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Afficher les capteurs** d’orientation  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Dans le panneau **capteurs** , vous pouvez sélectionner une orientation prédéfinie dans le menu déroulant **orientation** .  Pour entrer votre propre orientation, choisissez **orientation personnalisée**, puis entrez vos valeurs [alpha][MDNDeviceOrientaitonAlpha], [bêta][MDNDeviceOrientaitonBeta]et [gamma][MDNDeviceOrientaitonGamma] .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Options d’orientation dans le panneau capteurs" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    Options d' **orientation** dans le panneau **capteurs**  
:::image-end:::  

## Définir une chaîne d’agent utilisateur  

:::row:::
   :::column span="":::
      Si votre page dépend de la chaîne de l’agent utilisateur d’un appareil mobile pour s’afficher correctement, utilisez le volet de **conditions réseau** pour fournir différentes chaînes d’agent utilisateur.  
      
      1.  Sélectionnez **personnaliser et contrôler devtools** \ ( `...` \) > **plus d’outils**  >  **conditions réseau**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrée conditions réseau dans le menu plus d’outils" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         Entrée **conditions réseau** dans le menu **plus d’outils**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Ouvrir le menu de commandes.  
          *   Sélectionnez `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).  
      1. Tapez `Network conditions` , puis choisissez **afficher les conditions du réseau**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Afficher les conditions réseau" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Afficher les conditions réseau**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En regard d' **agent utilisateur**, décochez la case **sélectionner automatiquement** .  Ensuite, sélectionnez **Custom (personnalisé)...** pour effectuer une sélection dans une liste de chaînes prédéfinies agent utilisateur.  Pour entrer votre propre chaîne d’agent utilisateur, entrez la chaîne dans **entrer un agent utilisateur personnalisé**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Définissez la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS." lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Définissez la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS.  
:::image-end:::  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.MD "mise en route des appareils Android de débogage à distance | Documents Microsoft  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent. alpha | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent. beta | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent. gamma | MDN"  

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
