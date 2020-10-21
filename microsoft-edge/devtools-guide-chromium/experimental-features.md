---
description: Dernières fonctionnalités expérimentales de Microsoft Edge DevTools
title: Fonctionnalités expérimentales
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, expérience
ms.openlocfilehash: 65cf178596abfbaaac0e80bf205035838967cf59
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124893"
---
# Fonctionnalités expérimentales  

Microsoft Edge DevTools fournit l’accès à des fonctionnalités expérimentales toujours en développement.  Vous pouvez tester et [fournir des commentaires](#providing-feedback-on-experimental-features) avant la sortie de chaque fonctionnalité.  

Si les fonctionnalités expérimentales sont disponibles dans tous les canaux de Microsoft Edge, vous pouvez obtenir les dernières fonctionnalités expérimentales à l’aide du canal des Canaries Microsoft Edge.  

## Activer les fonctionnalités expérimentales  

Pour activer ou désactiver les fonctionnalités expérimentales dans Microsoft Edge, procédez comme suit.  

1.  [Ouvrez devtools][DevtoolsOpen].  
     *   Sélectionnez `Control` + `Shift` + `I` \ (Windows, Linux \) ou `Command` + `Option` + `I` \ (MacOS \).  Pour plus d’informations, accédez à [raccourcis clavier de Microsoft Edge devtools][DevToolsShortcuts].  
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
| [Émulation: prise en charge du mode double écran](#emulation-support-dual-screen-mode) | 84 ou version ultérieure |  
| [Activer les nouvelles fonctionnalités de débogage de grille CSS](#enable-new-css-grid-debugging-features) | 85 ou version ultérieure |  
| [Activer la prise en charge du déplacement des onglets entre les panneaux](#enable-support-to-move-tabs-between-panels) | 85 ou version ultérieure |  
| [Activer webhint](#enable-webhint) | 85 ou version ultérieure |  
| [Activer la console réseau](#enable-network-console) | 85 ou version ultérieure |  
| [Visionneuse de commandes source](#source-order-viewer) | 86 ou version ultérieure |  

### Émulation: prise en charge du mode double écran  

Fournit des fonctionnalités supplémentaires pour l’émulation de deux nouveaux périphériques à écran double et pliant dans Microsoft Edge.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  

Émuler les appareils et basculer entre les positions suivantes.  

*   un écran ou une position pliée  
*   position à deux écrans ou dépliées  
    
[Activez les API de plateforme Web expérimentales](#enable-experimental-apis) et utilisez la [fonctionnalité de répartition d’écran de média CSS][DualScreenDocsCssMedia] et l' [API getWindowSegments JavaScript][DualScreenDocsJSAPI] pour améliorer votre site Web \ (ou l’application \) pour les appareils à double écran et pliant.  

:::image type="complex" source="./media/experiments-surface-duo-emulation.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-surface-duo-emulation.msft.png":::  
   Émuler surface duo dans Microsoft Edge  
:::image-end:::  

#### Activer les API expérimentales  

Pour utiliser la [fonctionnalité de répartition d’écran de média CSS][DualScreenDocsCssMedia] et l' [API getWindowSegments JavaScript][DualScreenDocsJSAPI], activez l' `Experimental Web Platform features` indicateur dans Microsoft Edge.  Procédez comme suit.  

1.  Accédez à `edge://flags` .  
1.  Dans la zone de texte **indicateurs de recherche** , entrez `Experimental Web Platform features` , sélectionnez l’indicateur **fonctionnalités de plateforme Web expérimentales** , puis **désactivez** l' **option**désactivé.  
1.  Redémarrez MicrosoftEdge.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-dual-screen-emulation.msft.png":::
   Activer l’indicateur de fonctionnalités de plateforme Web expérimentale  
:::image-end:::  

> [!NOTE]
> Si vous utilisez des [requêtes multimédias CSS][DualScreenDocsCssMedia] ou l’API d' [énumération de segment Windows JavaScript][DualScreenDocsJSAPI] pour améliorer votre site Web ou votre application pour le duo de [surface][SurfaceDevicesDuo], vous devez également activer l' [Android Microsoft Edge app][GooglePlayMicrosoftEdge] indicateur de **fonctionnalités de plateforme Web** [Surface Duo][SurfaceDevicesDuo]  
> 
> Si l’indicateur fonctionnalités de la **plateforme Web expérimentée** est activé dans la version de [Bureau de Microsoft Edge][MicrosoftEdge] et désactivée dans l' [application Microsoft Edge Android][GooglePlayMicrosoftEdge], le comportement de votre site Web ou de votre application dans l’émulateur de surface duo dans l’application de bureau Microsoft Edge ne correspond pas à l' [application Android Microsoft Edge][GooglePlayMicrosoftEdge] sur le [Duo][SurfaceDevicesDuo].  Assurez-vous que les indicateurs sont mis en correspondance entre Android et Microsoft Edge pour pouvoir utiliser l’émulateur de surface duo dans [Microsoft Edge][MicrosoftEdge].  

#### Tests sur des appareils à écran double et pliant  

Lorsque vous émulez le [duo de surface][SurfaceDevicesDuo] dans une position sur deux écrans dans Microsoft Edge, la couture (espace entre les deux écrans \) est tracée sur votre site Web ou votre application.  

L’affichage émulé correspond au mode de rendu de votre site Web (ou de l’application) dans l' [application Microsoft Edge Android][GooglePlayMicrosoftEdge] sur [surface Duo][SurfaceDevicesDuo].  Il est possible que vous deviez mettre à jour votre site Web \ (ou l’application \) pour l’afficher mieux le long de la couture.  Pour plus d’informations sur l’adaptation de votre site Web (ou de l’application \) à la couture, accédez à l' [utilisation de la couture][DualScreenIntroductionHowWorkSeam] dans la documentation surface Duo.  

La [barre d’outils][DevtoolsDeviceModeIndexSimulateMobileViewport] de l’appareil inclut des fonctionnalités supplémentaires pour vous aider à tester votre site Web ou votre application en plusieurs positions et orientations.  Sélectionnez **faire pivoter** \ ( ![ faire pivoter ][ImageRotateIcon] ) pour faire pivoter la fenêtre d’affichage en orientation paysage. Combinez la fonctionnalité avec la **plage** \ ( ![ span ][ImageSpanIcon] \) pour basculer entre les positions à un seul écran ou pliées en deux ou non pliées.  Ensemble, les fonctionnalités permettent le test de votre site Web ou de votre application dans les quatre positions et orientations possibles.  

:::image type="complex" source="./media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matrice de positions et d’orientations pour les appareils à écran double et pliant  
:::image-end:::  

Les **fonctionnalités de la plateforme Web expérimentales** \ ( ![ ExperimentalApis ][ImageExperimentalApisIcon] \) affichent l’état de l’indicateur de **fonctionnalités de plateforme Web expérimentale** .  Si l’indicateur est activé, l’icône est mise en évidence.  Si l’indicateur est désactivé, l’icône n’est pas mise en surbrillance.  Pour activer \ (ou désactivé) l’indicateur, accédez à l’indicateur `edge://flags` et activez-le.  

<!-- Commenting out until the icon issue is fixed in Edge Canary
The **Experimental Web Platform features** \(![ExperimentalApis][ImageExperimentalApisIcon]\) icon displays the state of the **Experimental Web Platform features** flag.  If the flag is turned on, the icon is highlighted.  If the flag is turned off, the icon is not highlighted.  To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.   -->  

Voici d’autres ressources qui peuvent vous aider à améliorer votre site Web \ (ou l’application \) pour les périphériques à deux écrans:
*   Pour plus d’informations sur le développement Web sur les appareils à deux écrans, voir [expériences sur le Web à deux écrans][DualScreenWebIndex].  
*   Installez l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].  Il est différent de l’émulateur dans Microsoft Edge, émule le duo de surface sur lequel s’exécute Android et intégré à [Android Studio][AndroidDeveloperStudio].  Pour plus d’informations, accédez au [Kit de développement logiciel (SDK) surface Duo][DualScreenAndroidGetDuoSdk].  

> [!NOTE]
> Voici une liste des problèmes connus actuels.  
> 
> *   Lorsque vous utilisez un [client de bureau à distance Microsoft][RemoteDesktopClientDocs] pour vous connecter à un PC distant et émuler le pli de [surface Duo][SurfaceDevicesDuo] ou [Samsung Galaxy][SamsungMobileGalaxyFold], le pointeur risque de secouer ou d’interruption.  Si vous rencontrez ce problème, [envoyez des commentaires](#providing-feedback-on-experimental-features).  

### Activer les nouvelles fonctionnalités de débogage de grille CSS  

Cette fonctionnalité expérimentale fournit un certain nombre de nouvelles visualisations pour vous aider à déboguer des dispositions de grille CSS.  Pour afficher un aperçu des dernières fonctionnalités expérimentales, [activez cette expérience](#turn-on-experimental-features) et rechargez devtools.  Cette expérience est activée par défaut dans Microsoft Edge 87 et les versions ultérieures.  

#### Affichage des superpositions de la grille sur le survol avec l’outil inspecter  

L’outil **Inspect** vous permet d’identifier et de visualiser rapidement les dispositions d’une grille CSS dans un site Web en les plaçant au-dessus à l’aide de la souris.  **Inspect** ![ ](./media/inspect-icon.msft.png) Dans le coin supérieur gauche de devtools, sélectionnez l’icône inspecter \ (Inspect \).  Ensuite, pointez sur un élément Grid sur le site Web que vous déboguez.  Les plans sont affichés dans la grille, et l’ombrage indique l’emplacement des espaces de la grille, le cas échéant.  

:::image type="complex" source="./media/grid-inspect.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/grid-inspect.msft.png":::
   Affichage de grilles avec l’outil Inspect  
:::image-end:::  

#### Affichage de superpositions de grille persistante  

Dans Edge 86 et les versions ultérieures, la fonctionnalité de grille de feuilles de style  Les superpositions persistantes offrent plusieurs avantages.  

*   Les superpositions persistantes restent visibles sur la page lorsque vous faites défiler, déplacez la souris et utilisez les autres fonctionnalités du DevTools.  
*   Plusieurs superpositions persistantes peuvent être activées en même temps, ce qui vous permet de revoir de nombreux dispositions en une seule fois.  
*   Les superpositions persistantes proposent de nombreuses options de configuration, telles que le masquage et l’affichage des noms des zones de la grille, des espaces de grille, des tailles de suivi, etc.  

Il existe deux façons d’activer ou de désactiver une superposition de grille persistante.  

*   Choisissez le losange de **grille** en regard d’un élément Grid affiché dans l’arborescence DOM de l’outil **éléments** .  
    
    :::image type="complex" source="./media/grid-adorner.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/grid-adorner.msft.png":::
       Losange grille dans l’outil éléments  
    :::image-end:::  
    
*   Ouvrez le nouveau panneau de **disposition** situé dans l’outil éléments, puis activez la case à cocher en regard de chaque élément de grille que vous souhaitez mettre en surbrillance.  
    
    :::image type="complex" source="./media/grid-layout-zoom.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/grid-layout-zoom.msft.png":::
       Panneau de disposition  
    :::image-end:::  
    
#### Configuration de la superposition persistante  

Le nouveau panneau de **disposition** , situé dans l’outil **éléments** , ainsi que les onglets **Styles** et **calculs** dans les 86 et les versions ultérieures, les options de configuration des surfaces pour les superpositions persistantes.  

:::image type="complex" source="./media/experiments-grid.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-grid.msft.png":::
   Fonctionnalité de débogage de grille CSS  
:::image-end:::  

### Activer la prise en charge du déplacement des onglets entre les panneaux  

En règle générale, il est possible que les outils tels que les **éléments** et le **réseau** s’ouvrent uniquement dans le panneau principal qui se trouve en haut du devtools.  Outils tels que l' **affichage 3D** et les **problèmes** qui s’ouvrent normalement uniquement dans le panneau du **tiroir** situé en bas du devtools.  Après avoir choisi l’expérience, vous pouvez déplacer des outils entre les volets supérieur et inférieur.  Pour déplacer un outil, pointez sur celui-ci, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez **déplacer vers le haut** ou **déplacer vers le bas**.   Cette expérience vous permet de personnaliser la disposition de votre DevTools.  Pour afficher ou masquer le panneau de la **tiroir** , sélectionnez `Escape` .  

:::image type="complex" source="./media/experiments-move-panels.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-move-panels.msft.png":::
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

:::image type="complex" source="./media/experiments-webhint.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-webhint.msft.png":::
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
1.  Cliquez sur **Envoyer**.  

:::image type="complex" source="./media/network-network-console.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/network-network-console.msft.png":::
   **Console réseau** dans le tiroir de la **console**  
:::image-end:::  

<!--Available in Microsoft Edge version 85 and later.  -->  

### Visionneuse de commandes source  

La **visionneuse de commandes source** est une expérience qui affiche l’ordre des éléments dans la source de la page.  L’ordre de l’affichage à l’écran risque de différer de l’ordre de la source, ce qui déconcerte le lecteur d’écran et les utilisateurs du clavier.  Utilisez l’expérience de la **visionneuse de commandes sources** pour trouver les différences entre l’ordre d’affichage à l’écran et l’ordre de la source.  

Après avoir activé l’expérience, assurez-vous de redémarrer l’DevTools.  Pour utiliser la **visionneuse de commandes sources**, procédez comme suit.  

1.  Ouvrir le volet des **éléments** .  
1.  Ouvrez le volet **accessibilité** dans le panneau du tiroir.  
1.  Dans la section **visionneuse de commandes sources** , activez la case à cocher **afficher l’ordre source** .  
1.  Mettez en surbrillance un élément HTML pour afficher une superposition de l’ordre dans la source de la page.  

:::image type="complex" source="./media/experiments-source-order-viewer.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/experiments-source-order-viewer.msft.png":::
   **Visionneuse de commandes source** dans le volet **accessibilité**  
:::image-end:::  

<!--Available in Microsoft Edge version 86 and later.  -->  

## Fonctionnalités expérimentales antérieures  

*   la [vue 3D][Devtools3dViewIndex] est désormais disponible et activée par défaut dans Microsoft Edge version 83 ou ultérieure.  
*   La [Personnalisation des raccourcis clavier][DevtoolsCustomKeyboardShortcuts] est désormais disponible et activée par défaut dans Microsoft Edge version 86 ou ultérieure.  

## Fourniture de commentaires sur les fonctionnalités expérimentales  

Pour transmettre des commentaires sur les expériences DevTools Microsoft Edge, ou tout autre élément associé à DevTools.  

*   Envoyez vos commentaires à l’aide de l’icône **Envoyer des commentaires** dans le devtools  
*   Tweeter sur [@EdgeDevTools][TwitterEdgedevtools]  

:::image type="complex" source="./media/bing-devtools-send-feedback.msft.png" alt-text="Liste des expériences dans les paramètres de DevTools" lightbox="./media/bing-devtools-send-feedback.msft.png":::
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
[DevtoolsCustomKeyboardShortcuts]: ./customize/shortcuts.md "Personnaliser les raccourcis clavier dans Microsoft Edge DevTools | Documents Microsoft"

[DualScreenWebIndex]: /dual-screen/web/index "Expérience Web sur deux écrans | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenez l’émulateur Duo surface | Documents Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment utiliser la couture-Introduction aux périphériques à écran double Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur de surface Duo | Documents Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Fonctionnalité de répartition d’écran de média CSS pour la détection sur deux écrans | Documents Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour les appareils à deux écrans | Documents Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clients Bureau à distance | Documents Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "Pli Galaxy | Magnétoscope"  

[TwitterEdgedevtools]: https://www.twitter.com/EdgeDevTools "Microsoft Edge DevTools | Twitter"  

[WebhintMain]: https://webhint.io "Astuce"  
