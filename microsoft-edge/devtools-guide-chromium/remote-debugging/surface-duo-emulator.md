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
# <span data-ttu-id="c4d1a-104">Découvrir les émulateurs de surface duo pour le débogage à distance</span><span class="sxs-lookup"><span data-stu-id="c4d1a-104">Get Started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="c4d1a-105">Dans cet article, vous parcourez le processus de débogage à distance de votre contenu Web dans l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur un émulateur de [surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] à partir d’une instance de bureau de [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="c4d1a-106">Pour plus d’informations sur le débogage sur un appareil de surface Duo, suivez notre guide relatif au [débogage à distance des appareils Android][DevtoolsRemoteDebuggingMain].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <span data-ttu-id="c4d1a-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="c4d1a-107">Before you Begin</span></span>

<span data-ttu-id="c4d1a-108">Installez le [Kit de développement logiciel (SDK) surface Duo][MicrosoftDownload100847] avant d’exécuter l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="c4d1a-109">Pour plus d’informations, reportez-vous à [la rubrique obtention du SDK surface Duo][DualScreenAndroidGetDuoSdk].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-109">For more information, see [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="c4d1a-110">Étape 1: accédez à edge://inspect</span><span class="sxs-lookup"><span data-stu-id="c4d1a-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="c4d1a-111">Ouvrez une instance de bureau de [Microsoft Edge][MicrosoftEdge]et naviguez jusqu’à `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="c4d1a-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Page edge://inspect dans Microsoft Edge sur le Bureau" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="c4d1a-113">`edge://inspect`Page dans Microsoft Edge sur le Bureau</span><span class="sxs-lookup"><span data-stu-id="c4d1a-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="c4d1a-114">Si la `edge://inspect` page ne reconnaît pas l' [émulateur de surface Duo][DualScreenAndroidUseEmulator], redémarrez l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <span data-ttu-id="c4d1a-115">Étape 2: lancer l’émulateur duo de surface</span><span class="sxs-lookup"><span data-stu-id="c4d1a-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="c4d1a-116">Lancez l' [émulateur surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="c4d1a-117">Notez que l’émulateur affiche 2 écrans différents en cours d’exécution sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Emulateur de surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="c4d1a-119">Emulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="c4d1a-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <span data-ttu-id="c4d1a-120">Étape 3: charger votre contenu Web dans Microsoft Edge sur l’émulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="c4d1a-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="c4d1a-121">Sur l’écran, effectuez un balayage vers le haut sur le plateau favoris de l' [émulateur de surface Duo][DualScreenAndroidUseEmulator] pour afficher le tiroir d’applications.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="c4d1a-122">Sélectionnez **Edge** pour lancer l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Application Microsoft Edge sur l’émulateur de surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="c4d1a-124">Application Microsoft Edge sur l’émulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="c4d1a-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="c4d1a-125">Accédez au site Web ou à l’application que vous voulez déboguer dans l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <span data-ttu-id="c4d1a-126">Étape 4: déboguer votre contenu Web à partir de l’émulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="c4d1a-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="c4d1a-127">Revenez à l’instance de bureau de [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="c4d1a-128">La `edge://inspect` page affiche maintenant le **SurfaceDuoEmulator** avec une liste des onglets ouverts ou [PWAS][ProgressiveWebAppsIndex] qui s’exécutent sur l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La page edge://inspect affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur." lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="c4d1a-130">La `edge://inspect` page affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c4d1a-131">Si **SurfaceDuoEmulator** ne figure pas dans la `edge://inspect` page, essayez d’ouvrir ou de fermer des onglets dans l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-131">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="c4d1a-132">Pour plus d’informations sur la procédure de résolution des problèmes, voir la [section résolution des problèmes pour les appareils Android][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-132">For additional troubleshooting steps, see the [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="c4d1a-133">Dans la liste des onglets ouverts qui s’exécute sur l’émulateur, sélectionnez **inspecter** sous l’onglet qui comporte le contenu Web à déboguer.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="c4d1a-134">Le [devtools Microsoft Edge][DevtoolsIndex] s’ouvre dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="c4d1a-135">\*\*\*\* ![ ][ImageToggleScreencastIcon] Pour afficher le contenu Web de votre [émulateur duo de surface][DualScreenAndroidUseEmulator] dans la fenêtre devtools, sélectionnez Activer/désactiver la vidéo.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-135">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="c4d1a-136">Vous pouvez maintenant utiliser Microsoft Edge DevTools pour déboguer votre contenu Web sur l' [émulateur de surface Duo][DualScreenAndroidUseEmulator].</span><span class="sxs-lookup"><span data-stu-id="c4d1a-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Utilisation de Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur de surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="c4d1a-138">Utilisation de Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="c4d1a-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="c4d1a-139">Si vous étendez l' [application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur les deux écrans de l’émulateur, la capture d’écran reflète la nouvelle taille de l’application, mais pas la charnière.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="c4d1a-140">Pour mieux comprendre l’impact de la charnière sur la disposition de votre contenu Web, utilisez l' [émulateur de surface Duo][DualScreenAndroidUseEmulator] au lieu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <span data-ttu-id="c4d1a-141">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="c4d1a-141">Additional Resources</span></span>  

<span data-ttu-id="c4d1a-142">Le Web est une excellente plate-forme pour la nouvelle classe de périphériques pliants et à deux écrans, car vous pouvez écrire votre code HTML, CSS et JavaScript une seule fois et l’utiliser sur un seul écran, sur deux écrans et sur un appareil pliant.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-142">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="c4d1a-143">Pour plus d’informations, reportez-vous à ces ressources supplémentaires pour commencer à créer le contenu Web de ces nouveaux appareils.</span><span class="sxs-lookup"><span data-stu-id="c4d1a-143">For more information, see these additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="c4d1a-144">Documentation sur la création d’applications sur des appareils à écran double</span><span class="sxs-lookup"><span data-stu-id="c4d1a-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="c4d1a-145">Le préciseur de la plateforme Web Microsoft Edge pour les nouvelles API de création d’expériences sur le Web</span><span class="sxs-lookup"><span data-stu-id="c4d1a-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="c4d1a-146">Enregistrement de la session de la journée du développeur Microsoft 365: création d’expériences de deux écrans pour les sites Web et les applications Web</span><span class="sxs-lookup"><span data-stu-id="c4d1a-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

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
