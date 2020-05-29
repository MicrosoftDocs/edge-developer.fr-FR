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
# <span data-ttu-id="4a54a-103">Découvrir les émulateurs de surface duo pour le débogage à distance</span><span class="sxs-lookup"><span data-stu-id="4a54a-103">Get Started with Remote Debugging Surface Duo emulators</span></span>

<span data-ttu-id="4a54a-104">Dans cet article, vous parcourez le processus de débogage à distance de votre contenu Web dans l' [application Microsoft Edge][AndroidEdge] sur un émulateur de [surface Duo][SurfaceDuo] à partir d’une instance de bureau de [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="4a54a-104">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][AndroidEdge] on a [Surface Duo][SurfaceDuo] emulator from a desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="4a54a-105">Pour plus d’informations sur le débogage sur un appareil de surface Duo, suivez notre guide relatif au [débogage à distance des appareils Android][RemoteDebuggingAndroid].</span><span class="sxs-lookup"><span data-stu-id="4a54a-105">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][RemoteDebuggingAndroid].</span></span>

## <span data-ttu-id="4a54a-106">Avant de commencer</span><span class="sxs-lookup"><span data-stu-id="4a54a-106">Before you Begin</span></span>

<span data-ttu-id="4a54a-107">Installez le [Kit de développement logiciel (SDK) surface Duo][DuoSdk] avant d’exécuter l' [émulateur de surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="4a54a-107">Install the [Surface Duo SDK][DuoSdk] before running the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="4a54a-108">Pour plus d’informations, reportez-vous à [la rubrique obtention du SDK surface Duo][DuoSdkdocs].</span><span class="sxs-lookup"><span data-stu-id="4a54a-108">For more information, see [Get the Surface Duo SDK][DuoSdkdocs].</span></span>

## <span data-ttu-id="4a54a-109">Étape 1: accédez à edge://inspect</span><span class="sxs-lookup"><span data-stu-id="4a54a-109">Step 1: Navigate to edge://inspect</span></span>

<span data-ttu-id="4a54a-110">Ouvrez une instance de bureau de [Microsoft Edge][DesktopEdge]et naviguez jusqu’à `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="4a54a-110">Open a desktop instance of [Microsoft Edge][DesktopEdge], and navigate to `edge://inspect`.</span></span>

> ##### <span data-ttu-id="4a54a-111">Figure1</span><span class="sxs-lookup"><span data-stu-id="4a54a-111">Figure 1</span></span>  
> <span data-ttu-id="4a54a-112">`edge://inspect`Page dans Microsoft Edge sur le bureau ![ page Edge://Inspect dans Microsoft Edge sur le Bureau][ImageEdgeInspect]</span><span class="sxs-lookup"><span data-stu-id="4a54a-112">The `edge://inspect` page in Microsoft Edge on the desktop ![The edge://inspect page in Microsoft Edge on the desktop][ImageEdgeInspect]</span></span>

> [!NOTE]
> <span data-ttu-id="4a54a-113">Si la `edge://inspect` page ne reconnaît pas l' [émulateur de surface Duo][DuoEmulator], redémarrez l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="4a54a-113">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DuoEmulator], restart the emulator.</span></span>

## <span data-ttu-id="4a54a-114">Étape 2: lancer l’émulateur duo de surface</span><span class="sxs-lookup"><span data-stu-id="4a54a-114">Step 2: Launch the Surface Duo emulator</span></span>

<span data-ttu-id="4a54a-115">Lancez l' [émulateur surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="4a54a-115">Launch the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="4a54a-116">Notez que l’émulateur affiche 2 écrans différents en cours d’exécution sur l’émulateur.</span><span class="sxs-lookup"><span data-stu-id="4a54a-116">Notice that the emulator displays 2 different screens running on the emulator.</span></span>

> ##### <span data-ttu-id="4a54a-117">Figure 2</span><span class="sxs-lookup"><span data-stu-id="4a54a-117">Figure 2</span></span>
> <span data-ttu-id="4a54a-118">![Émulateur Duo surface Duo][ImageDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="4a54a-118">The Surface Duo emulator ![The Surface Duo emulator][ImageDuoEmulator]</span></span>  

## <span data-ttu-id="4a54a-119">Étape 3: charger votre contenu Web dans Microsoft Edge sur l’émulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="4a54a-119">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>

<span data-ttu-id="4a54a-120">Sur l’écran, effectuez un balayage vers le haut sur le plateau favoris de l' [émulateur de surface Duo][DuoEmulator] pour afficher le tiroir d’applications.</span><span class="sxs-lookup"><span data-stu-id="4a54a-120">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DuoEmulator] to display the Apps Drawer.</span></span> <span data-ttu-id="4a54a-121">Sélectionnez **Edge** pour lancer l' [application Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="4a54a-121">Choose **Edge** to launch the [Microsoft Edge app][AndroidEdge].</span></span>

> ##### <span data-ttu-id="4a54a-122">Figure3</span><span class="sxs-lookup"><span data-stu-id="4a54a-122">Figure 3</span></span>
> <span data-ttu-id="4a54a-123">Application Microsoft Edge sur l’émulateur Duo surface pour ![ l’application Microsoft Edge sur l’émulateur de surface Duo][ImageDuoEmulatorEdge]</span><span class="sxs-lookup"><span data-stu-id="4a54a-123">The Microsoft Edge app on the Surface Duo emulator ![The Microsoft Edge app on the Surface Duo emulator][ImageDuoEmulatorEdge]</span></span>  

<span data-ttu-id="4a54a-124">Accédez au site Web ou à l’application que vous voulez déboguer dans l' [application Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="4a54a-124">Navigate to the website or app that you want to debug in the [Microsoft Edge app][AndroidEdge].</span></span>

## <span data-ttu-id="4a54a-125">Étape 4: déboguer votre contenu Web à partir de l’émulateur de surface Duo</span><span class="sxs-lookup"><span data-stu-id="4a54a-125">Step 4: Debug your web content from the Surface Duo emulator</span></span> 

<span data-ttu-id="4a54a-126">Revenez à l’instance de bureau de [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="4a54a-126">Switch back to the desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="4a54a-127">La `edge://inspect` page affiche maintenant le **SurfaceDuoEmulator** avec une liste des onglets ouverts ou [PWAS][PwaDocs] qui s’exécutent sur l' [émulateur de surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="4a54a-127">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaDocs] that are running on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="4a54a-128">Figure 4</span><span class="sxs-lookup"><span data-stu-id="4a54a-128">Figure 4</span></span>
> <span data-ttu-id="4a54a-129">La `edge://inspect` page affiche une liste des onglets ouverts dans l’application Microsoft Edge qui s’exécute sur l’émulateur ![ la page Edge://Inspect affiche une liste des onglets ouverts dans l’application Microsoft Edge en cours d’exécution sur l’émulateur][ImageEdgeInspectTargets]</span><span class="sxs-lookup"><span data-stu-id="4a54a-129">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator ![The edge://inspect page displays a list of the open tabs in the Microsoft Edge app running on the emulator][ImageEdgeInspectTargets]</span></span>  

> [!NOTE]
> <span data-ttu-id="4a54a-130">Si **SurfaceDuoEmulator** ne figure pas dans la `edge://inspect` page, essayez d’ouvrir ou de fermer des onglets dans l' [application Microsoft Edge][AndroidEdge] sur l' [émulateur de surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="4a54a-130">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][AndroidEdge] on the [Surface Duo Emulator][DuoEmulator].</span></span> <span data-ttu-id="4a54a-131">Pour plus d’informations sur la procédure de résolution des problèmes, voir la [section résolution des problèmes pour les appareils Android][TroubleshootingAndroid].</span><span class="sxs-lookup"><span data-stu-id="4a54a-131">For additional troubleshooting steps, see the [troubleshooting section for Android devices][TroubleshootingAndroid].</span></span>

<span data-ttu-id="4a54a-132">Dans la liste des onglets ouverts qui s’exécute sur l’émulateur, sélectionnez **inspecter** sous l’onglet qui comporte le contenu Web à déboguer.</span><span class="sxs-lookup"><span data-stu-id="4a54a-132">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span> <span data-ttu-id="4a54a-133">Le [devtools Microsoft Edge][DevToolsDocs] s’ouvre dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4a54a-133">The [Microsoft Edge DevTools][DevToolsDocs] will open in a new window.</span></span> <span data-ttu-id="4a54a-134">**Toggle Screencast** ![ ][ImageToggleScreencastIcon] Pour afficher le contenu Web à partir de votre [émulateur de surface Duo][DuoEmulator] dans la fenêtre devtools, sélectionnez Activer/désactiver l’affichage de la capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="4a54a-134">Choose **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the web content from your [Surface Duo emulator][DuoEmulator] in the DevTools window.</span></span> <span data-ttu-id="4a54a-135">Vous pouvez maintenant utiliser Microsoft Edge DevTools pour déboguer votre contenu Web sur l' [émulateur de surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="4a54a-135">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="4a54a-136">Figure 5</span><span class="sxs-lookup"><span data-stu-id="4a54a-136">Figure 5</span></span>
> <span data-ttu-id="4a54a-137">À l’aide de l’application Microsoft Edge DevTools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur duo de surface ![ à l’aide de Microsoft Edge devtools pour déboguer Bing dans l’application Microsoft Edge sur l’émulateur de surface Duo][ImageDevTools]</span><span class="sxs-lookup"><span data-stu-id="4a54a-137">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator ![Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator][ImageDevTools]</span></span>  

> [!NOTE]
> <span data-ttu-id="4a54a-138">Si vous étendez l' [application Microsoft Edge][AndroidEdge] sur les deux écrans de l’émulateur, la capture d’écran reflète la nouvelle taille de l’application, mais pas la charnière.</span><span class="sxs-lookup"><span data-stu-id="4a54a-138">If you span the [Microsoft Edge app][AndroidEdge] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span> <span data-ttu-id="4a54a-139">Pour mieux comprendre l’impact de la charnière sur la disposition de votre contenu Web, utilisez l' [émulateur de surface Duo][DuoEmulator] au lieu de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="4a54a-139">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DuoEmulator] instead of the screencast.</span></span>

## <span data-ttu-id="4a54a-140">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="4a54a-140">Additional Resources</span></span>

<span data-ttu-id="4a54a-141">Le Web est une excellente plate-forme pour la nouvelle classe de périphériques pliants et à deux écrans, car vous pouvez écrire votre code HTML, CSS et JavaScript une seule fois et l’utiliser sur un seul écran, sur deux écrans et sur un appareil pliant.</span><span class="sxs-lookup"><span data-stu-id="4a54a-141">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span> <span data-ttu-id="4a54a-142">Pour plus d’informations, reportez-vous à ces ressources supplémentaires pour commencer à créer le contenu Web de ces nouveaux appareils.</span><span class="sxs-lookup"><span data-stu-id="4a54a-142">For more information, see these additional resources to get started building web content for these new devices.</span></span>

- [<span data-ttu-id="4a54a-143">Documentation sur la création d’applications sur des appareils à écran double</span><span class="sxs-lookup"><span data-stu-id="4a54a-143">Documentation for creating apps on dual-screen devices</span></span>][DualScreenDocs]
- [<span data-ttu-id="4a54a-144">Le préciseur de la plateforme Web Microsoft Edge pour les nouvelles API de création d’expériences sur le Web</span><span class="sxs-lookup"><span data-stu-id="4a54a-144">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][WebPlatformExplainer]
- [<span data-ttu-id="4a54a-145">Enregistrement de la session de la journée du développeur Microsoft 365: création d’expériences de deux écrans pour les sites Web et les applications Web</span><span class="sxs-lookup"><span data-stu-id="4a54a-145">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][DeveloperDay]

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
