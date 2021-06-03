---
description: Utilisez des périphériques virtuels dans Microsoft Edge pour améliorer votre site web pour les appareils à double écran et pliables.
title: Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, émulation, appareil, simulation, mobile, double écran, pliable, Surface Duo, Samsung Samsung Fold
ms.openlocfilehash: c3bd3296afa86d9d2c90c164bc3e9088bc043c3c
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564342"
---
# <a name="emulate-dual-screen-and-foldable-devices-in-microsoft-edge-devtools"></a>Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools  

Dans Microsoft Edge version 89 ou ultérieure, vous pouvez émuler les appareils à double écran et pliables suivants.  

*   [Surface Duo][SurfaceDevicesDuo]  
*   [Samsung Galaxy Fold][SamsungMobileGalaxyFold]  
    
Émulez les appareils et basculez entre les postures suivantes.  

*   Position à écran unique ou pliée  
*   Double écran ou posture dépliée  
    
Activer les API de plateforme [Web](#turn-on-experimental-apis) expérimentales et utiliser la fonctionnalité multimédia [CSS][DualScreenDocsCssMedia] couvrant l’écran et [l’API JavaScript getWindowSegments][DualScreenDocsJSAPI] pour améliorer votre site web \(ou application\) pour les appareils à double écran et pliables.  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Émuler Surface Duo dans Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   Émuler Surface Duo dans Microsoft Edge  
:::image-end:::  

## <a name="turn-on-experimental-apis"></a>Activer les API expérimentales  

Pour utiliser la [fonctionnalité multimédia CSS][DualScreenDocsCssMedia] couvrant l’écran et l’API [JavaScript getWindowSegments,][DualScreenDocsJSAPI]allumez l’indicateur `Experimental Web Platform features` dans Microsoft Edge.  Effectuer les étapes suivantes.  

1.  Naviguez vers`edge://flags` .  
1.  Dans la **zone de texte Indicateurs de recherche,** entrez , choisissez l’indicateur des fonctionnalités de la plateforme Web expérimentale et modifiez Désactivé en `Experimental Web Platform features` **Activé.** **** ****  
1.  Redémarrez Microsoft Edge.  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activer l’indicateur des fonctionnalités de plateforme Web expérimentale" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   Activer **l’indicateur des fonctionnalités de plateforme Web** expérimentale  
:::image-end:::  

> [!NOTE]
> Si vous utilisez des requêtes [multimédias CSS][DualScreenDocsCssMedia] ou l’API d’éumération de segment [JavaScript Windows][DualScreenDocsJSAPI] pour améliorer votre site web ou votre application [pour surface Duo,][SurfaceDevicesDuo]vous devez également activer l’indicateur des fonctionnalités de plateforme **Web** expérimentale dans l’application [Android Microsoft Edge][GooglePlayMicrosoftEdge] sur votre appareil [Surface Duo.][SurfaceDevicesDuo]  
> 
> Si l’indicateur des fonctionnalités de la plateforme **Web** expérimentale est allumé dans les Microsoft Edge de bureau et désactivé dans l’application [Microsoft Edge Android,][GooglePlayMicrosoftEdge]le comportement de votre site web ou de votre application dans l’émulateur Surface Duo dans l’Microsoft Edge de bureau ne correspond pas à l’application [Android Microsoft Edge][GooglePlayMicrosoftEdge] sur [Surface Duo][SurfaceDevicesDuo]. [][MicrosoftEdge]  Assurez-vous que les indicateurs correspondent à tous les appareils Android et Microsoft Edge pour utiliser correctement l’émulateur Surface Duo dans les ordinateurs [de bureau Microsoft Edge][MicrosoftEdge].  

## <a name="test-on-foldable-and-dual-screen-devices"></a>Test sur les appareils pliables et à double écran  

Lorsque vous émulez le [Surface Duo][SurfaceDevicesDuo] dans une posture à double écran dans Microsoft Edge, le seam \(l’espace entre les deux écrans\) est dessiné sur votre site web ou votre application.  

L’affichage émulé correspond à la façon dont votre site web \(ou application\) s’affiche dans [l’application Android Microsoft Edge][GooglePlayMicrosoftEdge] lors de l’exécution sur Surface [Duo][SurfaceDevicesDuo].  Vous de devez peut-être mettre à jour votre site web \(ou application\) pour une meilleure affichage le long du chemin d’accès.  Pour plus d’informations sur l’adaptation de votre site web \(ou application\) au [seam,][DualScreenIntroductionHowWorkSeam]accédez à Comment utiliser le seam .  

La [barre d’outils d’appareil][DevtoolsDeviceModeIndexSimulateMobileViewport] propose des fonctionnalités supplémentaires pour vous aider à tester votre site web ou votre application dans plusieurs postures et orientations.  Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation. Combinez la fonctionnalité **avec Span** \( Span \) pour faire bascule entre un seul écran ou des postures pliées et double écran ![ ou ](../media/span-dark-icon.msft.png) dépliées.  Ensemble, les fonctionnalités vous permettent de tester votre site web ou votre application dans les quatre postures et orientations possibles.  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrice des postures et des orientations pour les appareils à double écran et pliables" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   Matrice des postures et des orientations pour les appareils à double écran et pliables  
:::image-end:::  

L’icône Fonctionnalités **de plateforme Web** expérimentale \( ![ ExperimentalApis \) affiche l’état de l’indicateur des fonctionnalités de plateforme ](../media/experimental-apis-dark-icon.msft.png) **Web** expérimentale.  Si l’indicateur est allumé, l’icône est mise en surbrillion.  Si l’indicateur est désactivé, l’icône n’est pas mise en surbrillion.  Pour activer \(ou désactiver\) l’indicateur, choisissez l’icône ou accédez à l’indicateur et `edge://flags` basculez-le.  

> [!NOTE]
> Voici une liste des problèmes connus actuels.  
> 
> *   Lorsque vous utilisez un [client Bureau à distance Microsoft pour][RemoteDesktopClientDocs] vous connecter à un PC distant et émuler le Surface [Duo][SurfaceDevicesDuo] ou Samsung [Samsung Fold,][SamsungMobileGalaxyFold]le pointeur peut être agité ou sacrculé.  Si vous avez affaire au problème, envoyez [des commentaires.](#getting-in-touch-with-the-microsoft-edge-devtools-team)  

## <a name="additional-resources"></a>Ressources complémentaires  

Voici des ressources supplémentaires qui peuvent vous aider à améliorer votre site web \(ou application\) pour les appareils à double écran.  

*   Pour plus d’informations sur le développement web sur les appareils à double écran, accédez à [Expériences web à double écran.][DualScreenWebIndex]  
*   Installez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]  L’émulateur Surface Duo est différent de l’émulateur dans Microsoft Edge, exécute Android et s’intègre à [Android Studio.][AndroidDeveloperStudio]  Pour plus d’informations, [accédez à Obtenir le SDK Surface Duo.][DualScreenAndroidGetDuoSdk]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode Microsoft Edge devTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Expériences web à double écran | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenir l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Utilisation de la jointure - Introduction aux appareils à double écran | Microsoft Docs"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Fonctionnalité couvrant l’écran multimédia CSS pour la détection à double écran | Microsoft Docs"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "API JavaScript getWindowSegments pour appareils à double écran | Microsoft Docs"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clients Bureau à distance | Documents Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/global/galaxy/galaxy-fold "| Samsung"  
