---
description: Commencer avec les émulateurs Surface Duo de débogage à distance.
title: Mise en route avec les émulateurs Surface Duo de débogage à distance
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, débogage à distance, android, surface duo
ms.openlocfilehash: a9696e63528a674d349b78fbdec2a1b804f61c49
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398013"
---
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a><span data-ttu-id="5d25c-104">Mise en route avec les émulateurs Surface Duo de débogage à distance</span><span class="sxs-lookup"><span data-stu-id="5d25c-104">Get started with Remote Debugging Surface Duo emulators</span></span>  

<span data-ttu-id="5d25c-105">Dans cet article, vous allez passer en revue le processus de débogage à distance de votre contenu web dans l’application [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur un émulateur [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] à partir d’une instance de bureau de [Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="5d25c-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="5d25c-106">Pour plus d’informations sur le débogage sur un appareil Surface Duo, suivez notre guide pour [le débogage][DevtoolsRemoteDebuggingMain]à distance des appareils Android.</span><span class="sxs-lookup"><span data-stu-id="5d25c-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="5d25c-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="5d25c-107">Before you Begin</span></span>

<span data-ttu-id="5d25c-108">Installez le [SDK Surface Duo avant][MicrosoftDownload100847] d’exécutez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="5d25c-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="5d25c-109">Pour plus d’informations, [accédez à Obtenir le SDK Surface Duo.][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="5d25c-109">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="step-1-navigate-to-edgeinspect"></a><span data-ttu-id="5d25c-110">Étape 1 : Accédez à edge://inspect</span><span class="sxs-lookup"><span data-stu-id="5d25c-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="5d25c-111">Ouvrez une instance de bureau [de Microsoft Edge][MicrosoftEdge]et accédez à `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="5d25c-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Page edge://inspect dans Microsoft Edge sur le bureau" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="5d25c-113">Page `edge://inspect` dans Microsoft Edge sur le bureau</span><span class="sxs-lookup"><span data-stu-id="5d25c-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="5d25c-114">Si la `edge://inspect` page ne reconnaît pas l’émulateur Surface [Duo,][DualScreenAndroidUseEmulator]redémarrez l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="5d25c-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <a name="step-2-launch-the-surface-duo-emulator"></a><span data-ttu-id="5d25c-115">Étape 2 : Lancer l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="5d25c-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="5d25c-116">Lancez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="5d25c-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="5d25c-117">Notez que l’émulateur affiche 2 écrans différents en cours d’exécution sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="5d25c-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="5d25c-119">Émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="5d25c-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a><span data-ttu-id="5d25c-120">Étape 3 : Charger votre contenu web dans Microsoft Edge sur l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="5d25c-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="5d25c-121">Sur l’un ou l’autre écran, effectuez un balayage vers le haut sur le bac Favoris de [l’émulateur Surface Duo][DualScreenAndroidUseEmulator] pour afficher le caisse d’applications.</span><span class="sxs-lookup"><span data-stu-id="5d25c-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="5d25c-122">Choisissez **Edge** pour lancer [l’application Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="5d25c-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Application Microsoft Edge sur l’émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="5d25c-124">Application Microsoft Edge sur l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="5d25c-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="5d25c-125">Accédez au site web ou à l’application que vous souhaitez déboguer dans [l’application Microsoft Edge.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="5d25c-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a><span data-ttu-id="5d25c-126">Étape 4 : Déboguer votre contenu web à partir de l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="5d25c-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="5d25c-127">Revenir à l’instance de bureau [de Microsoft Edge.][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="5d25c-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="5d25c-128">La `edge://inspect` page affiche désormais **l’émulateur SurfaceDuoEmulator** avec une liste des onglets ouverts ou des PLAN en cours d’exécution sur l’émulateur [Surface Duo.][DualScreenAndroidUseEmulator] [][ProgressiveWebAppsIndex]</span><span class="sxs-lookup"><span data-stu-id="5d25c-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La page edge://inspect affiche la liste des onglets ouverts dans l’application Microsoft Edge en cours d’exécution sur l’émulateur" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="5d25c-130">La page affiche la liste des onglets ouverts dans l’application Microsoft Edge en cours `edge://inspect` d’exécution sur l’émulateur</span><span class="sxs-lookup"><span data-stu-id="5d25c-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="5d25c-131">Si **SurfaceDuoEmulator** n’est pas affiché sur la page, essayez d’ouvrir ou de fermer des onglets dans l’application Microsoft Edge sur `edge://inspect` l’émulateur Surface [Duo][DualScreenAndroidUseEmulator]. [][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="5d25c-131">If **SurfaceDuoEmulator** is not displayed on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="5d25c-132">Pour obtenir des étapes de dépannage supplémentaires, accédez à [la section dépannage pour les appareils Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]</span><span class="sxs-lookup"><span data-stu-id="5d25c-132">For additional troubleshooting steps, navigate to [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="5d25c-133">Dans la liste des onglets ouverts en cours d’exécution sur l’émulateur, sélectionnez **Inspecter** sur l’onglet qui a le contenu web à débocher.</span><span class="sxs-lookup"><span data-stu-id="5d25c-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="5d25c-134">Microsoft [Edge DevTools s’ouvre][DevtoolsIndex] dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="5d25c-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="5d25c-135">Choisissez **Toggle Screencast** \( Toggle Screencast \) pour afficher le contenu web à partir de votre émulateur Surface Duo dans la ![ fenêtre ][ImageToggleScreencastIcon] DevTools. [][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="5d25c-135">Choose **Toggle Screencast** \(![Toggle Screencast][ImageToggleScreencastIcon]\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="5d25c-136">Vous pouvez désormais utiliser Microsoft Edge DevTools pour déboguer votre contenu web sur [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="5d25c-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Utilisation de Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="5d25c-138">Utilisation de Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="5d25c-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="5d25c-139">Si vous étendez [l’application Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] sur les deux écrans de l’émulateur, la capture vidéo reflète la nouvelle taille de l’application, mais pas l’avantage.</span><span class="sxs-lookup"><span data-stu-id="5d25c-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="5d25c-140">Pour comprendre l’impact de l’impact sur la disposition de votre contenu web, utilisez l’émulateur [Surface Duo][DualScreenAndroidUseEmulator] au lieu de la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="5d25c-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="5d25c-141">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="5d25c-141">Additional Resources</span></span>  

<span data-ttu-id="5d25c-142">Le site web est une excellente plateforme pour la nouvelle classe d’appareils pliables et à double écran, car vous pouvez écrire votre code HTML, CSS et JavaScript une seule fois et l’avoir très bien sur les appareils à écran unique, double écran et pliables.</span><span class="sxs-lookup"><span data-stu-id="5d25c-142">The web is a great platform for the new class of foldable and dual-screen devices because you may write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="5d25c-143">Pour plus d’informations, accédez aux ressources supplémentaires suivantes pour commencer à créer du contenu web pour ces nouveaux appareils.</span><span class="sxs-lookup"><span data-stu-id="5d25c-143">For more information, navigate to the following additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="5d25c-144">Documentation pour la création d’applications sur des appareils à double écran</span><span class="sxs-lookup"><span data-stu-id="5d25c-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="5d25c-145">L’outil d’explication de la plateforme web Microsoft Edge pour les nouvelles API pour créer des expériences web sur des appareils pliables et à double écran</span><span class="sxs-lookup"><span data-stu-id="5d25c-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="5d25c-146">Enregistrement de la session de la Journée du développeur Microsoft 365 : comment créer des expériences à double écran pour les sites web et les applications web</span><span class="sxs-lookup"><span data-stu-id="5d25c-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

<!-- image links -->  

[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png  

<!-- links -->  

[DevtoolsIndex]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[ProgressiveWebAppsIndex]: ../../progressive-web-apps-chromium/index.md "Applications web progressives sur Windows | Documents Microsoft"  
[DevtoolsRemoteDebuggingMain]: ./index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  
[DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]: ./index.md#troubleshooting-devtools-is-not-detecting-the-android-device "Résolution des problèmes : DevTools ne détecte pas l’appareil Android : mise en place du débogage à distance des appareils Android | Documents Microsoft"  

[DualScreenIndex]: /dual-screen/index "Créer des applications pour les appareils à double écran | Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface DUo | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenir le SDK Surface Duo | Documents Microsoft"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Présentation du nouveau Microsoft Edge"  
[MicrosoftSurfaceDevicesSurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Nouveau modèle Surface Duo | Microsoft Surface"  
[MicrosoftDownload100847]: https://www.microsoft.com/download/details.aspx?id=100847 "Télécharger la version préliminaire du SDK Surface Duo | Centre de téléchargement Microsoft"  

[GooglePlayStoreAppsComMicrosoftEmmx]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge : navigateur web | GooglePlay"  

[GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Primitives de plateforme web pour les expériences | GitHub"  

[YoutubeDxrzwsqxpvc]: https://youtu.be/DXrZWsqXPVc "Comment créer des expériences à double écran pour le site web et les applications web | YouTube"  
