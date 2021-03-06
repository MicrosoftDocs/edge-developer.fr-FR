---
description: Commencer avec les émulateurs Surface Duo de débogage à distance.
title: Mise en route avec les émulateurs Surface Duo de débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, débogage à distance, android, surface duo
ms.openlocfilehash: 49b16f3c920735b34d44455bae437442cac3bf6e
ms.sourcegitcommit: bff24ab1f0a66aaf4c7f5ff81cea3eb28c6d8380
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/26/2021
ms.locfileid: "11461240"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a>Mise en route avec le débogage à distance des émulateurs Surface Duo  

Dans cet article, vous allez passer en revue le processus de débogage à distance de votre contenu web dans l’application Microsoft Edge sur un émulateur [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] à partir d’une instance de bureau de [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] . [][MicrosoftEdge]  Pour plus d’informations sur le débogage sur un appareil Surface Duo, suivez notre guide pour [le débogage][DevtoolsRemoteDebuggingMain]à distance des appareils Android.  

## <a name="before-you-begin"></a>Avant de commencer

Installez le [SDK Surface Duo avant][MicrosoftDownload100847] d’exécutez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]  Pour plus d’informations, [accédez à Obtenir le SDK Surface Duo.][DualScreenAndroidGetDuoSdk]  

## <a name="step-1-navigate-to-edgeinspect"></a>Étape 1 : Accédez à edge://inspect  

Ouvrez une instance de bureau [de Microsoft Edge][MicrosoftEdge]et accédez à `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Page edge://inspect dans Microsoft Edge sur le Bureau" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   La `edge://inspect` page dans Microsoft Edge sur le Bureau  
:::image-end:::

> [!NOTE]
> Si la `edge://inspect` page ne reconnaît pas l’émulateur Surface [Duo,][DualScreenAndroidUseEmulator]redémarrez l’émulateur.  

## <a name="step-2-launch-the-surface-duo-emulator"></a>Étape 2 : Lancer l’émulateur Surface Duo  

Lancez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]  Notez que l’émulateur affiche 2 écrans différents en cours d’exécution sur l’émulateur.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Émulateur Surface Duo  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a>Étape 3 : Charger votre contenu web dans Microsoft Edge sur l’émulateur Surface Duo  

Sur l’un ou l’autre écran, effectuez un balayage vers le haut sur le bac Favoris de [l’émulateur Surface Duo][DualScreenAndroidUseEmulator] pour afficher le caisse d’applications.  Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Application Microsoft Edge sur l’émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   Application Microsoft Edge sur l’émulateur Surface Duo  
:::image-end:::  

Accédez au site web ou à l’application que vous souhaitez déboguer dans [l’Microsoft Edge app.][GooglePlayStoreAppsComMicrosoftEmmx]  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a>Étape 4 : Déboguer votre contenu web à partir de l’émulateur Surface Duo  

Revenir à l’instance de bureau de [Microsoft Edge][MicrosoftEdge].  La `edge://inspect` page affiche désormais **l’émulateur SurfaceDuoEmulator** avec une liste des onglets ouverts ou des PLAN en cours d’exécution sur l’émulateur [Surface Duo.][DualScreenAndroidUseEmulator] [][ProgressiveWebAppsIndex]  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La page edge://inspect affiche la liste des onglets ouverts dans l’application Microsoft Edge’exécution sur l’émulateur" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   La page affiche la liste des onglets ouverts dans `edge://inspect` l’application Microsoft Edge’exécution sur l’émulateur  
:::image-end:::  

> [!NOTE]
> Si **SurfaceDuoEmulator** n’est pas affiché sur la page, essayez d’ouvrir ou de fermer des onglets dans `edge://inspect` l’application Microsoft Edge [sur][GooglePlayStoreAppsComMicrosoftEmmx] l’émulateur [Surface Duo.][DualScreenAndroidUseEmulator]  Pour d’autres étapes de résolution des problèmes, accédez à [la section de dépannage pour les appareils Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]  

Dans la liste des onglets ouverts en cours d’exécution sur l’émulateur, sélectionnez **Inspecter** sur l’onglet qui a le contenu web à débocher.  Le [Microsoft Edge DevTools][DevtoolsIndex] s’ouvre dans une nouvelle fenêtre.  Choisissez **Toggle Screencast** \( Toggle Screencast \) pour afficher le contenu web à partir de votre émulateur Surface Duo dans la ![ fenêtre ](../media/toggle-screencast-icon.msft.png) DevTools. [][DualScreenAndroidUseEmulator]  Vous pouvez désormais utiliser la Microsoft Edge DevTools pour déboguer votre contenu web sur [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Utilisation de Microsoft Edge DevTools pour déboguer des Bing dans l’Microsoft Edge sur l’émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Utilisation de Microsoft Edge DevTools pour déboguer des Bing dans l’Microsoft Edge sur l’émulateur Surface Duo  
:::image-end:::  

> [!NOTE]
> Si vous étendez [l’Microsoft Edge sur][GooglePlayStoreAppsComMicrosoftEmmx] les deux écrans de l’émulateur, la capture vidéo reflètera la nouvelle taille de l’application, mais pas la nouvelle taille de l’application.  Pour comprendre l’impact de l’impact sur la disposition de votre contenu web, utilisez l’émulateur [Surface Duo][DualScreenAndroidUseEmulator] au lieu de la capture vidéo.  

## <a name="additional-resources"></a>Ressources complémentaires  

Le web est une plate-forme excellente pour la nouvelle classe d’appareils pliables et à double écran, car vous pouvez écrire votre code HTML, CSS et JavaScript une seule fois et l’avoir s’affiche bien sur les appareils à écran unique, double écran et pliables.  Pour plus d’informations, accédez aux ressources supplémentaires suivantes pour commencer à créer du contenu web pour ces nouveaux appareils.  

*   [Documentation pour la création d’applications sur des appareils à double écran][DualScreenIndex]  
*   [L Microsoft Edge d’explication de la plateforme web pour les nouvelles API afin de créer des expériences web sur des appareils pliables et à double écran][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Enregistrement de la session Microsoft 365 jour du développeur : comment créer des expériences à double écran pour les sites web et les applications web][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Applications web progressives sur Windows | Documents Microsoft"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Résolution des problèmes : DevTools ne détecte pas l’appareil Android : mise en place du débogage à distance des appareils Android | Documents Microsoft"  

[DualScreenIndex]: /dual-screen/index "Créer des applications pour les appareils à double écran | Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface DUo | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenir le SDK Surface Duo | Documents Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Présentation de la nouvelle Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouveau modèle Surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Télécharger la version préliminaire du SDK Surface Duo | Centre de téléchargement Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge : navigateur web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitives de plateforme web pour les expériences | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Comment créer des expériences à double écran pour le site web et les applications web | YouTube"  
