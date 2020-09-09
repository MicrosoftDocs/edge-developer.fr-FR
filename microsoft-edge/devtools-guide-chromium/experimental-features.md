---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: c78e9aa5e0b4d808dd67d607a954b185ddcf54e7
ms.sourcegitcommit: 6b577cb118f34f3ff2c65eab2908b65f155dc151
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2020
ms.locfileid: "11004007"
---
# Fonctionnalités expérimentales  

Microsoft Edge DevTools fournit l’accès à des fonctionnalités expérimentales toujours en développement.  Vous pouvez tester et envoyer des[Commentaires](#providing-feedback-on-experimental-features) avant la sortie de chaque fonctionnalité.  

Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.  

## Activer les fonctionnalités expérimentales  

Procédez comme suit pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge.  

1.  [Ouvrez devtools][DevtoolsOpen].  
     *   Sélectionnez `Control` + `Shift` + `I` \ (Windows \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, reportez-vous à la rubrique [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  
1.  Ouvrez le volet [paramètres][DevToolsCustomizeSettings] .  
    *   Sélectionnez `Shift` + `?` .  Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  
1.  Sur le côté gauche du volet **paramètres** , sélectionnez la section **expériences** .  
    
    :::image type="complex" source="./media/experiments-devtools.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-devtools.msft.png":::
       Liste des expériences dans les paramètres de DevTools  
    :::image-end:::  
    
1.  Sur la page **expériences** , faites défiler la liste de toutes les fonctionnalités expérimentales disponibles, puis cochez la case en regard de chaque fonctionnalité que vous voulez tester.  
1.  Fermez et rouvrez Microsoft Edge DevTools.  

> [!NOTE]
> Les fonctionnalités expérimentales sont constamment mises à jour et peuvent entraîner des problèmes de performances.  Pour désactiver une fonctionnalité expérimentale, ouvrez la page **expériences** , puis décochez la case de la fonctionnalité expérimental que vous souhaitez désactiver.  

## Fonctionnalités expérimentales mises en évidence  

Les sections suivantes décrivent les nouvelles fonctionnalités expérimentales disponibles dans Microsoft Edge.  

| Fonctionnalités expérimentales | Version de Microsoft Edge |  
|:--- |:--- |  
| [Activer l’onglet Paramètres de raccourcis clavier personnalisés](#enable-custom-keyboard-shortcuts-settings-tab) | 84 ou version ultérieure |
| [Émulation: prise en charge du mode double écran](#emulation-support-dual-screen-mode) | 84 ou version ultérieure |  
| [Activer les nouvelles fonctionnalités de débogage de grille CSS](#enable-new-css-grid-debugging-features) | 85 ou version ultérieure |  
| [Activer la prise en charge du déplacement des onglets entre les panneaux](#enable-support-to-move-tabs-between-panels) | 85 ou version ultérieure |  
| [Activer webhint](#enable-webhint) | 85 ou version ultérieure |  
| [Activer la console réseau](#enable-network-console) | 85 ou version ultérieure |  
| [Activer la visionneuse de commandes sources](#enable-source-order-viewer) | 86 ou version ultérieure |  

### Activer l’onglet Paramètres de raccourcis clavier personnalisés  

Fournit une nouvelle page de **raccourcis** dans les [paramètres de devtools][DevToolsCustomizeSettings] pour faire correspondre les [raccourcis clavier][DevToolsShortcuts] du devtools au [code Microsoft Visual Studio][VisualstudioCode].  

Après avoir activé l’expérience, rouvrez les [paramètres de devtools][DevToolsCustomizeSettings] à l’aide de la sélection `Shift` + `?` .  Accédez à la page nouveau **raccourcis** .  Sélectionnez **devtools (par défaut)** dans le menu déroulant **correspondant aux raccourcis de** la liste déroulante, puis sélectionnez **Visual Studio code**.  Les raccourcis clavier dans le DevTools correspondent désormais aux raccourcis pour les actions équivalentes dans le code Visual Studio.  

:::image type="complex" source="./media/experiments-keyboard-shortcut.msft.png" alt-text="Faire correspondre les raccourcis clavier du DevTools au code Visual Studio" lightbox="./media/experiments-keyboard-shortcut.msft.png":::
   Faire correspondre les raccourcis clavier du DevTools au code Visual Studio  
:::image-end:::  

Par exemple, dans Windows, le raccourci clavier pour suspendre ou continuer à exécuter un script dans le [code Visual Studio][VisualstudioCodeShortcutsKeyboardWindows] est `F5` .  Avec la valeur prédéfinie **devtools (par défaut)** , le même raccourci dans devtools est `F8` .  Le raccourci est également associé au **code Visual Studio** prédéfini `F5` .  

### Émulation: prise en charge du mode double écran  

Fournit des fonctionnalités supplémentaires pour l’émulation de deux nouveaux périphériques à écran double et pliant dans Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  

Émuler les appareils et basculer entre les positions suivantes.  

*   un écran ou une position pliée  
*   position à deux écrans ou dépliées  

Utilisez les [API d’expérimentation](#enable-experimental-apis) pour améliorer votre site Web \ (ou App \) pour un appareil.  Vous pouvez également utiliser les [requêtes de média CSS et l’API d’énumération de segment Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

<!-- This image was taken in Chromium Canary since we don't yet have an Edge Canary that has Stan's changes -->  

:::image type="complex" source="./media/experiments-dual-screen-emulation.msft.png" alt-text="Émuler surface duo dans Microsoft Edge" lightbox="./media/experiments-dual-screen-emulation.msft.png":::  
   Émuler surface duo dans Microsoft Edge  
:::image-end:::  

#### Activer les API expérimentales  

Pour [activer cette expérience](#turn-on-experimental-features) dans Microsoft Edge devtools, suivez les étapes ci-dessous.  

1.  Accédez à `edge://flags` .  
1.  Dans la zone de texte **indicateurs de recherche** , entrez `Experimental Web Platform features` , sélectionnez l’indicateur **fonctionnalités de plateforme Web expérimentales** , puis **désactivez** l' **option**désactivé.  
1.  Redémarrez MicrosoftEdge.  

Pour améliorer votre site Web ou votre application sur des appareils à écran double et pliant, accédez aux [requêtes de média CSS et à l’API d’énumération de segment Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].

[Activez cette expérience](#turn-on-experimental-features) dans Microsoft Edge devtools.  

1.  Ouvrez un nouvel onglet dans Microsoft Edge et naviguez jusqu’à `edge://flags` .  
1.  Dans la zone de texte **indicateurs de recherche** , entrez `Experimental Web Platform features` , sélectionnez **fonctionnalités expérimentales de plateforme Web**, puis sélectionnez **désactivé** pour **activer**.  
1.  Redémarrez MicrosoftEdge.  

Pour plus d’informations sur l’amélioration de votre site Web (ou de l’application \) pour les appareils à écran double et pliant, accédez aux [requêtes de média CSS et à l’API d’énumération de segment Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables].  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activer l’indicateur de fonctionnalités de plateforme Web expérimentale" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Activer l’indicateur de fonctionnalités de plateforme Web expérimentale  
:::image-end:::  

> [!NOTE]
> Si vous utilisez des [requêtes multimédias CSS ou l’API d’énumération de segment Windows JavaScript][GitHubMicrosoftedgeMsedgeexplainerFoldables] pour améliorer votre site Web ou votre application pour le [duo de surface][SurfaceDevicesDuo], vous devez également activer l' [Android Microsoft Edge app][GooglePlayMicrosoftEdge] indicateur de **fonctionnalités de plateforme Web** [Surface Duo][SurfaceDevicesDuo]
> 
> Si l’indicateur fonctionnalités de la **plateforme Web expérimentée** est activé dans la version de [Bureau de Microsoft Edge][MicrosoftEdge] et désactivée dans l' [application Microsoft Edge pour Android][GooglePlayMicrosoftEdge], le comportement de votre site Web ou de votre application dans l’émulateur de surface duo dans l’application de bureau Microsoft Edge ne correspond pas à l' [application Microsoft Edge pour Android][GooglePlayMicrosoftEdge] sur [surface Duo][SurfaceDevicesDuo].  Assurez-vous que les indicateurs sont mis en correspondance entre Android et Microsoft Edge pour pouvoir utiliser l’émulateur de surface duo dans [Microsoft Edge][MicrosoftEdge].  

#### Tests sur des appareils à écran double et pliant  

Lorsque vous émulez le [duo de surface][SurfaceDevicesDuo] dans une position sur deux écrans dans Microsoft Edge, la **couture** est tracée sur votre site Web ou application.  

> [!NOTE]
> La **couture** est l’espace entre les deux écrans.  

L’affichage émulé de votre site Web (ou de l’application) est une représentation correcte.  Il correspond à l’affichage dans l' [application Microsoft Edge Android][GooglePlayMicrosoftEdge] sur [surface Duo][SurfaceDevicesDuo].  Mettez à jour le contenu pour l’afficher mieux le long de la **couture**.  Pour plus d’informations sur l’adaptation de votre site Web (ou de l’application \) à la **couture**, accédez à l' [utilisation de la couture][DualScreenIntroductionHowWorkSeam] dans la documentation surface Duo.  

La [barre d’outils][DevtoolsDeviceModeIndexSimulateMobileViewport] de l’appareil inclut des fonctionnalités supplémentaires pour vous aider à tester votre site Web ou votre application en plusieurs positions et orientations.  Sélectionnez **faire pivoter** \ ( ![ faire pivoter ][ImageRotateIcon] ) pour faire pivoter la fenêtre d’affichage en orientation paysage. Combinez la fonctionnalité avec la **plage** \ ( ![ span ][ImageSpanIcon] \) pour basculer entre les positions à un seul écran ou pliées en deux ou non pliées.  Ensemble, les fonctionnalités permettent le test de votre site Web ou de votre application dans les quatre positions et orientations possibles.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrice de positions et d’orientations pour les appareils à écran double et pliant" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matrice de positions et d’orientations pour les appareils à écran double et pliant  
:::image-end:::  

Les **fonctionnalités de la plateforme Web expérimentales** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) affichent l’état de l’indicateur de **fonctionnalités de plateforme Web expérimentale** .  Si l’indicateur est activé, l’icône est mise en évidence.  Si l’indicateur est désactivé, l’icône n’est pas mise en surbrillance.  Pour activer \ (ou désactivé) l’indicateur, sélectionnez l’icône ou accédez à `edge://flags` l’indicateur et activez-le.  

#### Ressources supplémentaires  
*   Pour plus d’informations sur le développement, accédez à [expériences sur le Web à deux écrans][DualScreenWebIndex].  
*   Installez l’émulateur surface Duo].  Elle est différente de l’émulateur dans Microsoft Edge.  Il émule le duo de surface exécutant Android et intégré à [Android Studio][AndroidDeveloperStudio].  Pour plus d’informations, accédez au [Kit de développement logiciel (SDK) surface Duo][DualScreenAndroidGetDuoSdk].  

### Activer les nouvelles fonctionnalités de débogage de grille CSS  

Permet d’améliorer les visualisations sur la page lorsque vous déboguez des sites Web dotés de dispositions CSS.  Vous pouvez personnaliser davantage les superpositions dans les paramètres de DevTools.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Fonctionnalité de débogage de grille CSS" lightbox="./media/experiments-grid.msft.png":::
   Fonctionnalité de débogage de grille CSS  
:::image-end:::  

Pour afficher un aperçu des dernières fonctionnalités expérimentales, effectuez les actions suivantes.  

1.  Dans la section **expériences** , sélectionnez l’option **activer les nouvelles fonctionnalités de débogage de grille CSS (options de configuration disponibles dans le volet barre latérale des éléments après le redémarrage)** .  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer la prise en charge du déplacement des onglets entre les panneaux  

En règle générale, il est possible que les outils tels que les **éléments** et le **réseau** s’ouvrent uniquement dans le panneau principal qui se trouve en haut du devtools.  Outils tels que l' **affichage 3D** et les **problèmes** qui s’ouvrent normalement uniquement dans le panneau du **tiroir** situé en bas du devtools.  Après avoir choisi l’expérience, vous pouvez déplacer des outils entre les volets supérieur et inférieur.  Pour déplacer un outil, pointez sur celui-ci, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le haut** ou **déplacer vers le bas**.   Cette expérience vous permet de personnaliser la disposition de votre DevTools.  Pour afficher ou masquer le panneau de la **tiroir** , sélectionnez `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Déplacement d’un onglet entre les panneaux" lightbox="./media/experiments-move-panels.msft.png":::
   Déplacement d’un onglet entre les panneaux  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer webhint  

[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur les sites Web et les pages Web locales.  Type de commentaires fourni par [webhint][WebhintMain].  

*   accessibilité  
*   compatibilité entre les navigateurs  
*   sécurité  
*   les  
*   PWA  
*   autres problèmes courants liés au développement Web  

L’expérience [webhint][WebhintMain] affiche le commentaire de webhint dans le volet [problèmes][DevtoolsIssues] .  Sélectionnez un problème pour afficher la documentation de la solution et une liste des ressources affectées sur votre site Web.  Sélectionnez un lien vers une ressource pour ouvrir le volet **réseau**, **sources**ou **éléments** approprié dans devtools.  

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Commentaires de webhint dans le volet problèmes" lightbox="./media/experiments-webhint.msft.png":::
   Commentaires de webhint dans le volet **problèmes**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer la console réseau  

**Network console** est le titre d’une expérience visant à faire des requêtes réseau synthétiques sur http.  Vous pouvez utiliser l’expérience de la **console réseau** pour envoyer des demandes d’API Web.  

Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.  Pour utiliser la **console réseau**, procédez comme suit.    

1.  Ouvrez le volet **réseau** .  
1.  Recherchez la demande réseau que vous souhaitez modifier et renvoyer.  
1.  Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **modifier, puis relire**.  
1.  Lorsque la **console réseau** s’ouvre, modifiez les informations de requête réseau.  
1.  Sélectionnez **Envoyer**.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Console réseau dans le tiroir de la console" lightbox="./media/network-network-console.msft.png":::
   **Console réseau** dans le tiroir de la **console**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Activer la visionneuse de commandes sources  

La **visionneuse de commandes source** est une expérience qui affiche l’ordre des éléments dans la source de la page.  L’ordre de l’affichage à l’écran risque de différer de l’ordre de la source, ce qui déconcerte le lecteur d’écran et les utilisateurs du clavier.  Utilisez l’expérience de la **visionneuse de commandes sources** pour trouver les différences entre l’ordre d’affichage à l’écran et l’ordre de la source.  

Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.  Pour utiliser la visionneuse de commandes source:  

1.  Ouvrir le volet des **éléments** .  
1.  Ouvrez le volet **accessibilité** dans le panneau du tiroir.  
1.  Dans la section **visionneuse de commandes sources** , activez la case à cocher **afficher l’ordre source** .  
1.  Mettez en surbrillance un élément HTML pour afficher une superposition de l’ordre dans la source de la page.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Visionneuse de commandes source dans le volet accessibilité" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Visionneuse de commandes source** dans le volet **accessibilité**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Fonctionnalités expérimentales antérieures  

*   la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.  

## Fourniture de commentaires sur les fonctionnalités expérimentales  

Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.  

*   Envoyez vos commentaires à l’aide de l’icône **Envoyer des commentaires** dans le devtools  
*   Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Icône Envoyer des commentaires dans Microsoft Edge DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
   Icône **Envoyer des commentaires** dans Microsoft Edge devtools  
:::image-end:::  

<!--  
## Getting in touch with the Microsoft Edge DevTools team  

[!INCLUDE [contact DevTools team note](./includes/contact-devtools-team-note.md)]  
-->  

<!-- image links -->  

[ImageRotateIcon]: ./media/rotate-dark-icon.msft.png  
[ImageSpanIcon]: ./media/span-dark-icon.msft.png  
[ImageExperimentalApisIcon]: ./media/experimental-apis-dark-icon.msft.png  

<!-- links -->  

[Devtools3dViewIndex]: ./3d-view/index.md "Affichage 3D | Documents Microsoft"  
[DevToolsCustomizeSettings]: ./customize/index.md#settings "Paramètres-personnaliser Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsDeviceModeIndexSimulateMobileViewport]: ./device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Microsoft Edge"  
[DevtoolsIssues]: ./issues/index.md "Recherchez et corrigez les problèmes liés à l’outil problèmes dans Microsoft Edge DevTools Documents Microsoft"  
[DevToolsShortcuts]: ./shortcuts.md "Raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"  
[DevtoolsOpen]: ./open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[DualScreenWebIndex]: /dual-screen/web/index "Expérience Web sur deux écrans | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenez l’émulateur Duo surface | Documents Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment utiliser la couture-Introduction aux périphériques à écran double Documents Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft surface"  

[VisualstudioCode]: https://code.visualstudio.com "Code Microsoft Visual Studio"  
[VisualstudioCodeShortcutsKeyboardWindows]: https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf "Raccourcis clavier dans Visual Studio pour Windows | Code Microsoft Visual Studio"  

[GitHubMicrosoftedgeMsedgeexplainerFoldables]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitives de plateforme Web pour expériences sur les appareils pliants | GitHub"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Pli Galaxy | Magnétoscope"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "Astuce"  
