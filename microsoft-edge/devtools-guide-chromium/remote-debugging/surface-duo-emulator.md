---
description: Familiarisez-vous avec les émulateurs de surface duo pour le débogage à distance.
title: Découvrir les émulateurs de surface duo pour le débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, débogage à distance, Android, surface Duo
ms.openlocfilehash: f44c85c468de3bdd7727695e3f33269584966231
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230635"
---
# Découvrir les émulateurs de surface duo pour le débogage à distance  

Dans cet article, vous parcourez le processus de débogage à distance de votre contenu Web dans l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur un émulateur de [surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] à partir d’une instance de bureau de [Microsoft Edge][MicrosoftEdge].  Pour plus d’informations sur le débogage sur un appareil de surface Duo, suivez notre guide relatif au [débogage à distance des appareils Android][DevtoolsRemoteDebuggingMain].  

## Avant de commencer

Installez le [Kit de développement logiciel (SDK) surface Duo][MicrosoftDownload100847] avant d’exécuter l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].  Pour plus d’informations, reportez-vous à [la rubrique obtention du SDK surface Duo][DualScreenAndroidGetDuoSdk].  

## Étape 1: accédez à edge://inspect  

Ouvrez une instance de bureau de [Microsoft Edge][MicrosoftEdge]et naviguez jusqu’à `edge://inspect` .  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Page edge://inspect dans Microsoft Edge sur le Bureau" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   `edge://inspect`Page dans Microsoft Edge sur le Bureau  
:::image-end:::

> [!NOTE]
> Si la `edge://inspect` page ne reconnaît pas l' [émulateur de surface Duo][DualScreenAndroidUseEmulator], redémarrez l’émulateur.  

## Étape 2: lancer l’émulateur duo de surface  

Lancez l' [émulateur surface Duo][DualScreenAndroidUseEmulator].  Notez que l’émulateur affiche 2 écrans différents en cours d’exécution sur l’émulateur.  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Emulateur de surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   Emulateur de surface Duo  
:::image-end:::  

## Étape 3: charger votre contenu Web dans Microsoft Edge sur l’émulateur de surface Duo  

Sur l’écran, effectuez un balayage vers le haut sur le plateau favoris de l' [émulateur de surface Duo][DualScreenAndroidUseEmulator] pour afficher le tiroir d’applications.  Sélectionnez **Edge** pour lancer l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Application Microsoft Edge sur l’émulateur de surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   Application Microsoft Edge sur l’émulateur de surface Duo  
:::image-end:::  

Accédez au site Web ou à l’application que vous voulez déboguer dans l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].  

## Étape 4: déboguer votre contenu Web à partir de l’émulateur de surface Duo  

Revenez à l’instance de bureau de [Microsoft Edge][MicrosoftEdge].  La `edge://inspect` page affiche maintenant le **SurfaceDuoEmulator** avec une liste des onglets ouverts ou [PWAS][ProgressiveWebAppsIndex] qui s’exécutent sur l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La page edge://inspect affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur." lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   La `edge://inspect` page affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur.  
:::image-end:::  

> [!NOTE]
> Si **SurfaceDuoEmulator** ne figure pas dans la `edge://inspect` page, essayez d’ouvrir ou de fermer des onglets dans l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].  Pour plus d’informations sur la procédure de résolution des problèmes, voir la [section résolution des problèmes pour les appareils Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].  

Dans la liste des onglets ouverts qui s’exécute sur l’émulateur, sélectionnez **inspecter** sous l’onglet qui comporte le contenu Web à déboguer.  Le [devtools Microsoft Edge][DevtoolsIndex] s’ouvre dans une nouvelle fenêtre.  **** ![ ][ImageToggleScreencastIcon] Pour afficher le contenu Web de votre [émulateur duo de surface][DualScreenAndroidUseEmulator] dans la fenêtre devtools, sélectionnez Activer/désactiver la vidéo.  Vous pouvez maintenant utiliser Microsoft Edge DevTools pour déboguer votre contenu Web sur l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Utilisation de Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur de surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   Utilisation de Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur de surface Duo  
:::image-end:::  

> [!NOTE]
> Si vous étendez l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur les deux écrans de l’émulateur, la capture d’écran reflète la nouvelle taille de l’application, mais pas la charnière.  Pour mieux comprendre l’impact de la charnière sur la disposition de votre contenu Web, utilisez l' [émulateur de surface Duo][DualScreenAndroidUseEmulator] au lieu de la vidéo.  

## Ressources complémentaires  

Le Web est une excellente plate-forme pour la nouvelle classe de périphériques pliants et à deux écrans, car vous pouvez écrire votre code HTML, CSS et JavaScript une seule fois et l’utiliser sur un seul écran, sur deux écrans et sur un appareil pliant.  Pour plus d’informations, reportez-vous à ces ressources supplémentaires pour commencer à créer le contenu Web de ces nouveaux appareils.  

*   [Documentation sur la création d’applications sur des appareils à écran double][DualScreenIndex]  
*   [Le préciseur de la plateforme Web Microsoft Edge pour les nouvelles API de création d’expériences sur le Web][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [Enregistrement de la session de la journée du développeur Microsoft 365: création d’expériences de deux écrans pour les sites Web et les applications Web][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Applications Web progressives sur Windows | Documents Microsoft"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Commencer à utiliser le débogage à distance des appareils Android | Documents Microsoft"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Résolution des problèmes: DevTools n’est pas en voie de détecter l’appareil Android-prenez en main le débogage à distance des appareils Android | Documents Microsoft"  

[DualScreenIndex]: /dual-screen/index "Créer des applications pour les appareils à écran double Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur de surface DUo | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Téléchargez le kit de développement logiciel (SDK) surface Duo | Documents Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Présentation du nouveau Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouvelle surface Duo | Microsoft surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Télécharger la version préliminaire du SDK surface Duo | Centre de téléchargement Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge: navigateur Web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitives de plateforme Web pour des expériences compatibles sur les appareils pliants-MicrosoftEdge/MSEdgeExplainers | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Découvrez comment créer des expériences sur deux écrans pour le site Web et les applications Web | YouTube"  
