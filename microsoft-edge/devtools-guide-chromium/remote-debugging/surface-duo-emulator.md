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
# <a name="get-started-with-remote-debugging-surface-duo-emulators"></a><span data-ttu-id="f915e-104">Mise en route avec le débogage à distance des émulateurs Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f915e-104">Get started with remote debugging Surface Duo emulators</span></span>  

<span data-ttu-id="f915e-105">Dans cet article, vous allez passer en revue le processus de débogage à distance de votre contenu web dans l’application Microsoft Edge sur un émulateur [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] à partir d’une instance de bureau de [Microsoft Edge][GooglePlayStoreAppsComMicrosoftEmmx] . [][MicrosoftEdge]</span><span class="sxs-lookup"><span data-stu-id="f915e-105">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on a [Surface Duo][MicrosoftSurfaceDevicesSurfaceDuo] emulator from a desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="f915e-106">Pour plus d’informations sur le débogage sur un appareil Surface Duo, suivez notre guide pour [le débogage][DevtoolsRemoteDebuggingMain]à distance des appareils Android.</span><span class="sxs-lookup"><span data-stu-id="f915e-106">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][DevtoolsRemoteDebuggingMain].</span></span>  

## <a name="before-you-begin"></a><span data-ttu-id="f915e-107">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="f915e-107">Before you begin</span></span>

<span data-ttu-id="f915e-108">Installez le [SDK Surface Duo avant][MicrosoftDownload100847] d’exécutez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="f915e-108">Install the [Surface Duo SDK][MicrosoftDownload100847] before running the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="f915e-109">Pour plus d’informations, [accédez à Obtenir le SDK Surface Duo.][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="f915e-109">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <a name="step-1-navigate-to-edgeinspect"></a><span data-ttu-id="f915e-110">Étape 1 : Accédez à edge://inspect</span><span class="sxs-lookup"><span data-stu-id="f915e-110">Step 1: Navigate to edge://inspect</span></span>  

<span data-ttu-id="f915e-111">Ouvrez une instance de bureau [de Microsoft Edge][MicrosoftEdge]et accédez à `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="f915e-111">Open a desktop instance of [Microsoft Edge][MicrosoftEdge], and navigate to `edge://inspect`.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page.msft.png" alt-text="Page edge://inspect dans Microsoft Edge sur le Bureau" lightbox="../media/remote-debugging-surface-duo-inspect-page.msft.png":::
   <span data-ttu-id="f915e-113">La `edge://inspect` page dans Microsoft Edge sur le Bureau</span><span class="sxs-lookup"><span data-stu-id="f915e-113">The `edge://inspect` page in Microsoft Edge on the desktop</span></span>  
:::image-end:::

> [!NOTE]
> <span data-ttu-id="f915e-114">Si la `edge://inspect` page ne reconnaît pas l’émulateur Surface [Duo,][DualScreenAndroidUseEmulator]redémarrez l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="f915e-114">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DualScreenAndroidUseEmulator], restart the emulator.</span></span>  

## <a name="step-2-launch-the-surface-duo-emulator"></a><span data-ttu-id="f915e-115">Étape 2 : Lancer l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f915e-115">Step 2: Launch the Surface Duo emulator</span></span>  

<span data-ttu-id="f915e-116">Lancez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="f915e-116">Launch the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="f915e-117">Notez que l’émulateur affiche 2 écrans différents en cours d’exécution sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="f915e-117">Notice that the emulator displays 2 different screens running on the emulator.</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator.msft.png" alt-text="Émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator.msft.png":::
   <span data-ttu-id="f915e-119">Émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f915e-119">The Surface Duo emulator</span></span>  
:::image-end:::  

## <a name="step-3-load-your-web-content-in-microsoft-edge-on-the-surface-duo-emulator"></a><span data-ttu-id="f915e-120">Étape 3 : Charger votre contenu web dans Microsoft Edge sur l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f915e-120">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>  

<span data-ttu-id="f915e-121">Sur l’un ou l’autre écran, effectuez un balayage vers le haut sur le bac Favoris de [l’émulateur Surface Duo][DualScreenAndroidUseEmulator] pour afficher le caisse d’applications.</span><span class="sxs-lookup"><span data-stu-id="f915e-121">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DualScreenAndroidUseEmulator] to display the Apps Drawer.</span></span>  <span data-ttu-id="f915e-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span><span class="sxs-lookup"><span data-stu-id="f915e-122">Choose **Edge** to launch the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-emulator-edge.msft.png" alt-text="Application Microsoft Edge sur l’émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-emulator-edge.msft.png":::
   <span data-ttu-id="f915e-124">Application Microsoft Edge sur l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f915e-124">The Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

<span data-ttu-id="f915e-125">Accédez au site web ou à l’application que vous souhaitez déboguer dans [l’Microsoft Edge app.][GooglePlayStoreAppsComMicrosoftEmmx]</span><span class="sxs-lookup"><span data-stu-id="f915e-125">Navigate to the website or app that you want to debug in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx].</span></span>  

## <a name="step-4-debug-your-web-content-from-the-surface-duo-emulator"></a><span data-ttu-id="f915e-126">Étape 4 : Déboguer votre contenu web à partir de l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f915e-126">Step 4: Debug your web content from the Surface Duo emulator</span></span>  

<span data-ttu-id="f915e-127">Revenir à l’instance de bureau de [Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="f915e-127">Switch back to the desktop instance of [Microsoft Edge][MicrosoftEdge].</span></span>  <span data-ttu-id="f915e-128">La `edge://inspect` page affiche désormais **l’émulateur SurfaceDuoEmulator** avec une liste des onglets ouverts ou des PLAN en cours d’exécution sur l’émulateur [Surface Duo.][DualScreenAndroidUseEmulator] [][ProgressiveWebAppsIndex]</span><span class="sxs-lookup"><span data-stu-id="f915e-128">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][ProgressiveWebAppsIndex] that are running on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png" alt-text="La page edge://inspect affiche la liste des onglets ouverts dans l’application Microsoft Edge’exécution sur l’émulateur" lightbox="../media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png":::
   <span data-ttu-id="f915e-130">La page affiche la liste des onglets ouverts dans `edge://inspect` l’application Microsoft Edge’exécution sur l’émulateur</span><span class="sxs-lookup"><span data-stu-id="f915e-130">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="f915e-131">Si **SurfaceDuoEmulator** n’est pas affiché sur la page, essayez d’ouvrir ou de fermer des onglets dans `edge://inspect` l’application Microsoft Edge [sur][GooglePlayStoreAppsComMicrosoftEmmx] l’émulateur [Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="f915e-131">If **SurfaceDuoEmulator** is not displayed on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] on the [Surface Duo Emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="f915e-132">Pour d’autres étapes de résolution des problèmes, accédez à [la section de dépannage pour les appareils Android.][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice]</span><span class="sxs-lookup"><span data-stu-id="f915e-132">For additional troubleshooting steps, navigate to [troubleshooting section for Android devices][DevtoolsRemoteDebuggingIndexTroubleshootingDevtoolsIsNotDetectingAndroidDevice].</span></span>  

<span data-ttu-id="f915e-133">Dans la liste des onglets ouverts en cours d’exécution sur l’émulateur, sélectionnez **Inspecter** sur l’onglet qui a le contenu web à débocher.</span><span class="sxs-lookup"><span data-stu-id="f915e-133">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span>  <span data-ttu-id="f915e-134">Le [Microsoft Edge DevTools][DevtoolsIndex] s’ouvre dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f915e-134">The [Microsoft Edge DevTools][DevtoolsIndex] will open in a new window.</span></span>  <span data-ttu-id="f915e-135">Choisissez **Toggle Screencast** \( Toggle Screencast \) pour afficher le contenu web à partir de votre émulateur Surface Duo dans la ![ fenêtre ](../media/toggle-screencast-icon.msft.png) DevTools. [][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="f915e-135">Choose **Toggle Screencast** \(![Toggle Screencast](../media/toggle-screencast-icon.msft.png)\) to view the web content from your [Surface Duo emulator][DualScreenAndroidUseEmulator] in the DevTools window.</span></span>  <span data-ttu-id="f915e-136">Vous pouvez désormais utiliser la Microsoft Edge DevTools pour déboguer votre contenu web sur [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="f915e-136">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  

:::image type="complex" source="../media/remote-debugging-surface-duo-devtools.msft.png" alt-text="Utilisation de Microsoft Edge DevTools pour déboguer des Bing dans l’Microsoft Edge sur l’émulateur Surface Duo" lightbox="../media/remote-debugging-surface-duo-devtools.msft.png":::
   <span data-ttu-id="f915e-138">Utilisation de Microsoft Edge DevTools pour déboguer des Bing dans l’Microsoft Edge sur l’émulateur Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f915e-138">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="f915e-139">Si vous étendez [l’Microsoft Edge sur][GooglePlayStoreAppsComMicrosoftEmmx] les deux écrans de l’émulateur, la capture vidéo reflètera la nouvelle taille de l’application, mais pas la nouvelle taille de l’application.</span><span class="sxs-lookup"><span data-stu-id="f915e-139">If you span the [Microsoft Edge app][GooglePlayStoreAppsComMicrosoftEmmx] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span>  <span data-ttu-id="f915e-140">Pour comprendre l’impact de l’impact sur la disposition de votre contenu web, utilisez l’émulateur [Surface Duo][DualScreenAndroidUseEmulator] au lieu de la capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="f915e-140">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DualScreenAndroidUseEmulator] instead of the screencast.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="f915e-141">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="f915e-141">Additional Resources</span></span>  

<span data-ttu-id="f915e-142">Le web est une plate-forme excellente pour la nouvelle classe d’appareils pliables et à double écran, car vous pouvez écrire votre code HTML, CSS et JavaScript une seule fois et l’avoir s’affiche bien sur les appareils à écran unique, double écran et pliables.</span><span class="sxs-lookup"><span data-stu-id="f915e-142">The web is a great platform for the new class of foldable and dual-screen devices because you may write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span>  <span data-ttu-id="f915e-143">Pour plus d’informations, accédez aux ressources supplémentaires suivantes pour commencer à créer du contenu web pour ces nouveaux appareils.</span><span class="sxs-lookup"><span data-stu-id="f915e-143">For more information, navigate to the following additional resources to get started building web content for these new devices.</span></span>  

*   [<span data-ttu-id="f915e-144">Documentation pour la création d’applications sur des appareils à double écran</span><span class="sxs-lookup"><span data-stu-id="f915e-144">Documentation for creating apps on dual-screen devices</span></span>][DualScreenIndex]  
*   [<span data-ttu-id="f915e-145">L Microsoft Edge d’explication de la plateforme web pour les nouvelles API afin de créer des expériences web sur des appareils pliables et à double écran</span><span class="sxs-lookup"><span data-stu-id="f915e-145">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][GithubMicrosoftedgeMsedgeexplainersFoldablesExplainer]  
*   [<span data-ttu-id="f915e-146">Enregistrement de la session Microsoft 365 jour du développeur : comment créer des expériences à double écran pour les sites web et les applications web</span><span class="sxs-lookup"><span data-stu-id="f915e-146">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][YoutubeDxrzwsqxpvc]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="f915e-147">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="f915e-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
