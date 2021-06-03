---
description: Utilisez des périphériques virtuels dans Microsoft Edge pour créer des sites web d’abord mobiles.
title: Émuler des appareils mobiles dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, émulation, appareil, simulation, mobile
ms.openlocfilehash: b62a1799b1707fc4c6890bb7ad9ad4aa9afab113
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564405"
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
# <a name="emulate-mobile-devices-in-microsoft-edge-devtools"></a>Émuler des appareils mobiles dans Microsoft Edge DevTools  

Utilisez **l’émulation d’appareil** pour approximativement l’apparence et la réponse de votre page sur un appareil mobile.  Les Microsoft Edge DevTools fournissent un ensemble de fonctionnalités pour vous aider à émuler des appareils mobiles.  La collection inclut les fonctionnalités suivantes.  

*   [Simuler une vue mobile](#simulate-a-mobile-viewport)  
*   [Limiter le réseau](#throttle-the-network-only)  
*   [Limiter l’UC](#throttle-the-cpu-only)  
*   [Simuler la géolocalisation](#override-geolocation)  
*   [Définir l’orientation](#set-orientation)  
*   [Définir la chaîne de l’agent utilisateur](#set-user-agent-string)  

## <a name="limitations"></a>Limitations  

**L’émulation d’appareil** est une [approximation][WikiApproximation] de premier ordre de l’apparence de votre page sur un appareil mobile.  **L’émulation d’appareil** n’exécute pas réellement votre code sur un appareil mobile.  Au lieu de cela, vous simulez l’expérience utilisateur mobile à partir de votre ordinateur portable ou de bureau.  

Certains aspects des appareils mobiles ne sont jamais émulés dans DevTools.  Par exemple, l’architecture des processeurs mobiles est différente de celle des processeurs d’ordinateur portable ou de bureau.  En cas de doute, votre meilleur objectif est d’exécuter réellement votre page sur un appareil mobile.  Utilisez [Débogage à distance][DevToolsRemoteDebugging] pour interagir avec le code d’une page à partir de votre ordinateur pendant que votre page s’exécute réellement sur un appareil mobile.  Vous pouvez afficher, modifier, déboguer, profiler ou les quatre pendant que vous interagissez avec le code.  Votre ordinateur peut être un ordinateur de bureau ou un bloc-notes.  

## <a name="simulate-a-mobile-viewport"></a>Simuler une vue mobile  

Choose **Toggle device emulation**  \( ![ Toggle Device Toolbar ](../media/toggle-device-toolbar-dark-icon.msft.png) \) or choose **Customize and control DevTools** \( `...` \) > Device **emulation** to open the UI that enables you to simulate a mobile viewport.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils Appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
    Barre d’outils Appareil  
:::image-end:::  

Par défaut, la barre d’outils de l’appareil s’ouvre en mode Deport réactif.  

### <a name="responsive-viewport-mode"></a>Mode d’affichage réactif  

Pour tester rapidement l’apparence de votre page sur plusieurs tailles d’écran, faites glisser les poignées pour resizer laport d’affichage à vos dimensions requises.  Vous pouvez également entrer des valeurs spécifiques dans les zones de largeur et de hauteur.  Dans la figure suivante, la largeur est définie sur `626` et la hauteur sur `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Poignées de modification des dimensions de laport d’affichage en mode d’affichage réactif" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
    Poignées de modification des dimensions de laport d’affichage en mode d’affichage réactif  
:::image-end:::  

#### <a name="show-media-queries"></a>Afficher les requêtes multimédias  

Si vous avez défini des requêtes multimédias sur votre page, vous pouvez passer aux dimensions de laport d’affichage dans laquelle ces requêtes multimédias prennent effet en affichant les points d’arrêt des requêtes multimédias au-dessus de votreport d’affichage.  Choose **More options**Show media  >  **queries**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Afficher les requêtes multimédias" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Afficher les requêtes multimédias**  
:::image-end:::  

Choisissez un point d’arrêt pour modifier la largeur de laport d’affichage afin que la requête multimédia soit déclenchée.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Choisir un point d’arrêt pour modifier la largeur de laport d’affichage" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Choisir un point d’arrêt pour modifier la largeur de laport d’affichage  
:::image-end:::  

#### <a name="set-the-device-type"></a>Définir le type d’appareil  

Utilisez la liste **Type d’appareil** pour simuler un appareil mobile ou un appareil de bureau.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Liste des types d’appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Liste **des types d’appareils**  
:::image-end:::  

Le tableau suivant décrit les différences entre les options de type d’appareil disponibles.  La colonne Méthode de rendu indique si Microsoft Edge rendu de la page en tant que port d’affichage mobile ou de bureau.  La colonne Icône du curseur fait référence au type de curseur qui s’affiche lorsque vous pointez sur la page.  La colonne Événements déclenchés indique si la page se déclenche ou s’il s’agit d’événements lorsque `touch` `click` vous interagissez avec la page.  

| Option | Méthode de rendu | Icône curseur | Événements déclenchés |  
|:--- |:--- |:--- |:--- |  
| Appareils mobiles | Appareils mobiles | Cercle | interface tactile |  
| Mobile \(aucune touche\) | Appareils mobiles | Normal |  choisissez |  
| Bureau | Bureau | Normal |  choisissez |  
| Bureau \(tactile\) | Bureau | Cercle | interface tactile |  

> [!NOTE]
> Si la liste **Type d’appareil** n’est pas affichée, sélectionnez **Autres options**Ajouter un  >  **type d’appareil.**  

### <a name="mobile-device-viewport-mode"></a>Mode d’affichage d’appareil mobile  

Pour simuler les dimensions d’un appareil mobile spécifique, sélectionnez l’appareil dans la liste **Des** appareils.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Liste des appareils" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Liste **des appareils**  
:::image-end:::  

#### <a name="rotate-the-viewport-to-landscape-orientation"></a>Faire pivoter laport d’affichage vers l’orientation paysage  

Testez votre page web en orientation paysage.  

*   Pour faire pivoter la vue vers l’orientation paysage, choisissez **Rotation** \( ![ Rotation ](../media/rotate-dark-icon.msft.png) \).  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Page affichée en orientation paysage" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
       Page affichée en orientation paysage  
    :::image-end:::  
    
> [!NOTE]
> Le **bouton Pivoter** disparaît si la barre d’outils **de votre** appareil est étroite.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils Appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Barre **d’outils Appareil**  
:::image-end:::  

Pour plus d’informations, accédez à [Définir l’orientation.](#set-orientation)  

#### <a name="show-device-frame"></a>Afficher le cadre de l’appareil  

Affichez le cadre de l’appareil physique autour de la fenêtre d’affichage lorsque vous simulez les dimensions d’un appareil mobile spécifique, tel qu’un iPhone 6.  

1.  Ouvrez **plus d’options.**  
1.  Choose **Show device frame**.  

> [!NOTE]
> Si un cadre d’appareil pour un appareil particulier n’est pas affiché, cela signifie que DevTools n’a pas d’image pour l’option.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Afficher le cadre de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Afficher le cadre de l’appareil  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Image de l’appareil iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Image de l’appareil iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

#### <a name="add-a-custom-mobile-device"></a>Ajouter un appareil mobile personnalisé  

Si l’option d’appareil mobile dont vous avez besoin n’est pas incluse dans la liste par défaut, vous pouvez ajouter un appareil personnalisé.  Pour ajouter un appareil personnalisé, complétez les étapes suivantes.  

1.  Choose the **Device** list > **Edit**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Choose Edit" lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Choose **Edit**  
    :::image-end:::  
    
1.  Choose **Add custom device**.  
1.  Sur **les appareils émulés,** entrez un nom d’appareil, la largeur de l’écran et la hauteur de l’écran pour l’appareil personnalisé.  Les champs [Ratio de pixels de][MDNWindowDevicePixelRatio]l’appareil, chaîne [d’agent utilisateur][MDNUserAgent]et [type](#set-the-device-type) d’appareil sont facultatifs.  Par défaut, le champ De type d’appareil est **Mobile.**  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Créer un appareil personnalisé" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Créer un appareil personnalisé  
    :::image-end:::  
    
### <a name="show-rulers"></a>Afficher les règles  

Si vous devez mesurer les dimensions de l’écran, vous pouvez utiliser des règles pour mesurer la taille de l’écran en pixels.  Choose **More options**Show  >  **rulers** to display rulers above and to the left of your viewport.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Élément de menu pour afficher les règles" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         Élément de menu pour afficher les règles  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Règles au-dessus et à gauche de la vue" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Règles au-dessus et à gauche de la vue  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

### <a name="zoom-the-viewport"></a>Zoomer la vue  

Pour tester l’apparence de votre page à plusieurs niveaux de zoom, utilisez la liste **Zoom** pour effectuer un zoom avant ou arrière.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Zoom" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Zoom**  
:::image-end:::  

## <a name="throttle-the-network-and-cpu"></a>Limiter le réseau et le processeur  

Les appareils mobiles ont souvent des contraintes de réseau et de processeur.  Veillez à tester la rapidité de chargement de votre page et la façon dont elle répond à différentes vitesses internet et processeur.  

Limiter le réseau et le processeur.  

1.  Choose **Throttle** list and change the preset to **Mid-tier mobile** or **Low-end mobile**.  
    *   **Un appareil mobile intermédiaire** simule `fast 3G` et limitation votre processeur.  Elle est quatre fois plus lente que la normale.  
    *   **Un appareil mobile bas de gamme** simule et limitation votre `slow 3G` processeur.  Elle est six fois plus lente que la normale.  
    
Toutes les limitations sont basées sur les fonctionnalités normales de votre ordinateur portable ou de votre bureau.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Liste Limitation dans la barre d’outils de l’appareil" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Liste **Limitation dans** la barre d’outils de l’appareil  
:::image-end:::  

> [!NOTE]
> Si la liste **Throttle est** masquée, votre **barre d’outils d’appareil** est trop étroite.  Pour accéder à la liste **Limitation,** augmentez la largeur de la barre d’outils **de l’appareil.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Barre d’outils Appareil" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Barre **d’outils Appareil**  
:::image-end:::  

### <a name="throttle-the-cpu-only"></a>Limiter l’UC uniquement  

Pour limiter l’UC uniquement et non le réseau, complétez les étapes suivantes.

1.  Choisissez le **panneau Performances,** puis **sélectionnez Capturer Paramètres** \( Capturer Paramètres ![ ](../media/capture-settings-icon.msft.png) \).
1.  Choisissez **le**  >  **ralentissement 4x du** processeur ou le ralentissement **6x.**
    
    :::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Liste du processeur dans le panneau Performances" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
       Liste **du processeur** dans le panneau **Performances**  
    :::image-end:::  
    
### <a name="throttle-the-network-only"></a>Limiter le réseau uniquement  

Pour limiter le réseau uniquement, complétez les étapes suivantes.

1.  Choisissez **l’outil** Réseau.
1.  Choose **Online**  >  **Fast 3G** or Slow **3G**.
    
    :::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Liste Limitation dans le panneau Réseau" lightbox="../media/device-mode-network-throttle.msft.png":::
       Liste **Limitation** dans le panneau Réseau  
    :::image-end:::  
    
    Ou sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) **** `3G` **** **** pour ouvrir le menu commande, tapez et choisissez Activer la limitation 3G rapide ou Activer la limitation de 3G lente.  
    
    :::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Menu Commande" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
       Menu **Commande**  
    :::image-end:::  
    
Vous pouvez également définir la limitation du réseau à partir du **panneau Performances.**  

1.  Choose **Capture Paramètres** \( Capture Paramètres ![ ](../media/capture-settings-icon.msft.png) \) and choose the **Network** list and change the preset to **Fast 3G** or Slow **3G**.  
    
    :::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Définir la limitation du réseau à partir du panneau Performances" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
       Définir la limitation du réseau à partir du panneau **Performances**  
    :::image-end:::  
    
## <a name="override-geolocation"></a>Remplacer la géolocalisation  

:::row:::
   :::column span="":::
      Si votre page dépend des informations de géolocalisation d’un appareil mobile pour un rendu correct, fournissez différentes géolocalisations à l’aide de l’interface utilisateur de remplacement de la géolocalisation.  

      1.  Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Sensors**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Capteurs** pour la géolocalisation  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Ouvrez le menu Commande.  
          *   Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).  
      1. Tapez `Sensors` et choisissez Afficher les **capteurs.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs pour la géolocalisation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Afficher les capteurs** pour la géolocalisation  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Dans le **panneau Capteurs,** vous pouvez sélectionner l’un des emplacements prédéfinés inclus dans DevTools à l’aide du menu déroulant Emplacement. ****  Pour entrer un emplacement personnalisé, choisissez **Autre...** et entrez les coordonnées de votre emplacement personnalisé.  Pour tester votre page dans un état d’erreur lorsque les informations d’emplacement ne sont pas disponibles, choisissez **Emplacement indisponible.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Panneau capteurs avec un emplacement prédéfiny sélectionné" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
    **Panneau capteurs** avec un emplacement prédéfiny sélectionné.  
:::image-end:::

## <a name="set-orientation"></a>Définir l’orientation  

:::row:::
   :::column span="":::
      Si votre page dépend des informations d’orientation d’un appareil mobile pour s’restituer correctement, ouvrez l’interface utilisateur d’orientation.  

      1.  Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Sensors**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Capteurs d’orientation" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Capteurs d’orientation**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Ouvrez le menu Commande.  
          *   Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).  
      1. Tapez `Sensors` et choisissez Afficher les **capteurs.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Afficher les capteurs pour l’orientation" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Afficher les capteurs pour** l’orientation  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

Dans le **panneau Capteurs,** vous pouvez sélectionner une orientation prédéfinë dans le menu **déroulant** Orientation.  Pour entrer votre propre orientation, choisissez **l’orientation**personnalisée, puis entrez vos propres valeurs [alpha,][MDNDeviceOrientaitonAlpha] [bêta][MDNDeviceOrientaitonBeta]et [gamma.][MDNDeviceOrientaitonGamma]  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Options d’orientation sur le panneau Capteurs" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
    **Options d’orientation** sur le **panneau Capteurs**  
:::image-end:::  

## <a name="set-user-agent-string"></a>Définir la chaîne de l’agent utilisateur  

:::row:::
   :::column span="":::
      Si votre page dépend de la chaîne d’agent utilisateur d’un appareil mobile pour un rendu correct, utilisez le panneau **Conditions** réseau pour fournir différentes chaînes d’agent utilisateur.  
      
      1.  Choose **Customize and control DevTools** \( `...` \) > More **tools**  >  **Network conditions**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png" alt-text="Entrée des conditions réseau dans le menu Plus d’outils" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-network-conditions.msft.png":::
         **Entrée des conditions réseau** dans le menu **Plus d’outils**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      1.  Ouvrez le menu Commande.  
          *   Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).  
      1. Tapez `Network conditions` et choisissez Afficher les conditions **réseau.**  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png" alt-text="Afficher les conditions réseau" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-network-conditions.msft.png":::
         **Afficher les conditions réseau**  
      :::image-end:::  
   :::column-end:::
:::row-end:::  

En regard de **l’agent utilisateur,** cochez la **case** Sélectionner automatiquement.  Ensuite, choisissez **Personnalisé...** pour sélectionner dans une liste de chaînes d’agent utilisateur prédéfinées.  Pour entrer votre propre chaîne d’agent utilisateur, entrez la chaîne **dans Entrer un agent utilisateur personnalisé.**  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png" alt-text="Définir la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS" lightbox="../media/device-mode-toggle-device-toolbar-network-conditions-macos.msft.png":::
    Définir la chaîne de l’agent utilisateur sur Microsoft Edge sur macOS  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /remote-debugging/index.md " Get started with remote debugging Android devices | Microsoft Docs »  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window.devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Agent utilisateur | MDN"  
[MDNDeviceOrientaitonAlpha]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/alpha "DeviceOrientationEvent.alpha, | MDN"  
[MDNDeviceOrientaitonBeta]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/beta "DeviceOrientationEvent.beta, | MDN"  
[MDNDeviceOrientaitonGamma]: https://developer.mozilla.org/en-US/docs/Web/API/DeviceOrientationEvent/gamma "DeviceOrientationEvent.gamma, | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Order of Approximation - First-order - Wikipedia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
