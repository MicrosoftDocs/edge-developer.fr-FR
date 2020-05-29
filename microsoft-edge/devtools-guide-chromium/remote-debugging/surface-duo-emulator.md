---
title: Découvrir les émulateurs de surface duo pour le débogage à distance
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, débogage à distance, Android, surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621501"
---
# Découvrir les émulateurs de surface duo pour le débogage à distance

Dans cet article, vous parcourez le processus de débogage à distance de votre contenu Web dans l' [application Microsoft Edge][AndroidEdge] sur un émulateur de [surface Duo][SurfaceDuo] à partir d’une instance de bureau de [Microsoft Edge][DesktopEdge]. Pour plus d’informations sur le débogage sur un appareil de surface Duo, suivez notre guide relatif au [débogage à distance des appareils Android][RemoteDebuggingAndroid].

## Avant de commencer

Installez le [Kit de développement logiciel (SDK) surface Duo][DuoSdk] avant d’exécuter l' [émulateur de surface Duo][DuoEmulator]. Pour plus d’informations, reportez-vous à [la rubrique obtention du SDK surface Duo][DuoSdkdocs].

## Étape 1: accédez à edge://inspect

Ouvrez une instance de bureau de [Microsoft Edge][DesktopEdge]et naviguez jusqu’à `edge://inspect` .

> ##### Figure1  
> `edge://inspect`Page dans Microsoft Edge sur le bureau ![ page Edge://Inspect dans Microsoft Edge sur le Bureau][ImageEdgeInspect]

> [!NOTE]
> Si la `edge://inspect` page ne reconnaît pas l' [émulateur de surface Duo][DuoEmulator], redémarrez l’émulateur.

## Étape 2: lancer l’émulateur duo de surface

Lancez l' [émulateur surface Duo][DuoEmulator]. Notez que l’émulateur affiche 2 écrans différents en cours d’exécution sur l’émulateur.

> ##### Figure 2
> ![Émulateur Duo surface Duo][ImageDuoEmulator]  

## Étape 3: charger votre contenu Web dans Microsoft Edge sur l’émulateur de surface Duo

Sur l’écran, effectuez un balayage vers le haut sur le plateau favoris de l' [émulateur de surface Duo][DuoEmulator] pour afficher le tiroir d’applications. Sélectionnez **Edge** pour lancer l' [application Microsoft Edge][AndroidEdge].

> ##### Figure3
> Application Microsoft Edge sur l’émulateur Duo surface pour ![ l’application Microsoft Edge sur l’émulateur de surface Duo][ImageDuoEmulatorEdge]  

Accédez au site Web ou à l’application que vous voulez déboguer dans l' [application Microsoft Edge][AndroidEdge].

## Étape 4: déboguer votre contenu Web à partir de l’émulateur de surface Duo 

Revenez à l’instance de bureau de [Microsoft Edge][DesktopEdge]. La `edge://inspect` page affiche maintenant le **SurfaceDuoEmulator** avec une liste des onglets ouverts ou [PWAS][PwaDocs] qui s’exécutent sur l' [émulateur de surface Duo][DuoEmulator].

> ##### Figure 4
> La `edge://inspect` page affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur ![ la page Edge://Inspect affiche une liste des onglets ouverts dans l’application Microsoft Edge en cours d’exécution sur l’émulateur][ImageEdgeInspectTargets]  

> [!NOTE]
> Si **SurfaceDuoEmulator** ne figure pas dans la `edge://inspect` page, essayez d’ouvrir ou de fermer des onglets dans l' [application Microsoft Edge][AndroidEdge] sur l' [émulateur de surface Duo][DuoEmulator]. Pour plus d’informations sur la procédure de résolution des problèmes, voir la [section résolution des problèmes pour les appareils Android][TroubleshootingAndroid].

Dans la liste des onglets ouverts qui s’exécute sur l’émulateur, sélectionnez **inspecter** sous l’onglet qui comporte le contenu Web à déboguer. Le [devtools Microsoft Edge][DevToolsDocs] s’ouvre dans une nouvelle fenêtre. **Toggle Screencast** ![ ][ImageToggleScreencastIcon] Pour afficher le contenu Web à partir de votre [émulateur de surface Duo][DuoEmulator] dans la fenêtre devtools, sélectionnez Activer/désactiver l’affichage de la capture d’écran. Vous pouvez maintenant utiliser Microsoft Edge DevTools pour déboguer votre contenu Web sur l' [émulateur de surface Duo][DuoEmulator].

> ##### Figure 5
> À l’aide de l’application Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur duo de surface ![ à l’aide de Microsoft Edge devtools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur de surface Duo][ImageDevTools]  

> [!NOTE]
> Si vous étendez l' [application Microsoft Edge][AndroidEdge] sur les deux écrans de l’émulateur, la capture d’écran reflète la nouvelle taille de l’application, mais pas la charnière. Pour mieux comprendre l’impact de la charnière sur la disposition de votre contenu Web, utilisez l' [émulateur de surface Duo][DuoEmulator] au lieu de la vidéo.

## Ressources complémentaires

Le Web est une excellente plate-forme pour la nouvelle classe de périphériques pliants et à deux écrans, car vous pouvez écrire votre code HTML, CSS et JavaScript une seule fois et l’utiliser sur un seul écran, sur deux écrans et sur un appareil pliant. Pour plus d’informations, reportez-vous à ces ressources supplémentaires pour commencer à créer le contenu Web de ces nouveaux appareils.

- [Documentation sur la création d’applications sur des appareils à écran double][DualScreenDocs]
- [Le préciseur de la plateforme Web Microsoft Edge pour les nouvelles API de création d’expériences sur le Web][WebPlatformExplainer]
- [Enregistrement de la session de la journée du développeur Microsoft 365: création d’expériences de deux écrans pour les sites Web et les applications Web][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Figure 1: page edge://inspect dans Microsoft Edge sur le Bureau"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Figure 2: émulateur duo de surface"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Figure 3: application Microsoft Edge sur l’émulateur de surface Duo"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Figure 4: la page edge://inspect affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur"
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Figure 5: utilisation de Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur de surface Duo"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Découvrir les appareils Android de débogage à distance"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Applications Web progressives sur Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Résolution des problèmes: DevTools ne détecte pas l’appareil Android"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Application Microsoft Edge Android"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Présentation de surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Présentation du nouveau Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Utiliser l’émulateur de surface DUo"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Version préliminaire du SDK surface Duo"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Télécharger le kit de développement logiciel (SDK) surface Duo"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Créer des applications pour les appareils à écran double"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitives de plateforme Web pour expériences sur les appareils pliants"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Découvrez comment créer des expériences sur deux écrans pour le site Web et les applications Web"
