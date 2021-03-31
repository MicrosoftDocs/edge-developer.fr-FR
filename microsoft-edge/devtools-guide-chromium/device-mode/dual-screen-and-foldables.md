---
description: Utilisez des périphériques virtuels dans Microsoft Edge pour améliorer votre site web pour les appareils à double écran et pliables.
title: Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/02/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, émulation, appareil, simulation, mobile, double écran, pliable, Surface Duo, Samsung Samsung Fold
ms.openlocfilehash: bc91c0b7c917d82f169dc7d47e047a587d505353
ms.sourcegitcommit: 12c30ad4ab2664d17c9b7e9d59d7a3cda60ff65c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "11313196"
---
# <span data-ttu-id="9c890-104">Émuler les appareils à double écran et pliables dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9c890-104">Emulate dual-screen and foldable devices in Microsoft Edge DevTools</span></span>  

<span data-ttu-id="9c890-105">Dans Microsoft Edge version 89 ou ultérieure, vous pouvez émuler les appareils pliables et double écran suivants.</span><span class="sxs-lookup"><span data-stu-id="9c890-105">In Microsoft Edge version 89 or later, you may emulate the following dual-screen and foldable devices.</span></span>  

*   [<span data-ttu-id="9c890-106">Surface Duo</span><span class="sxs-lookup"><span data-stu-id="9c890-106">Surface Duo</span></span>][SurfaceDevicesDuo]  
*   [<span data-ttu-id="9c890-107">Samsung Galaxy Fold</span><span class="sxs-lookup"><span data-stu-id="9c890-107">Samsung Galaxy Fold</span></span>][SamsungMobileGalaxyFold]  
    
<span data-ttu-id="9c890-108">Émulez les appareils et basculez entre les postures suivantes.</span><span class="sxs-lookup"><span data-stu-id="9c890-108">Emulate the devices and toggle between the following postures.</span></span>  

*   <span data-ttu-id="9c890-109">Position à écran unique ou pliée</span><span class="sxs-lookup"><span data-stu-id="9c890-109">Single-screen or folded posture</span></span>  
*   <span data-ttu-id="9c890-110">Double écran ou posture dépliée</span><span class="sxs-lookup"><span data-stu-id="9c890-110">Dual-screen or unfolded posture</span></span>  
    
<span data-ttu-id="9c890-111">Activer les API de plateforme [Web](#turn-on-experimental-apis) expérimentales et utiliser la fonctionnalité multimédia [CSS][DualScreenDocsCssMedia] couvrant l’écran et [l’API JavaScript getWindowSegments][DualScreenDocsJSAPI] pour améliorer votre site web \(ou application\) pour les appareils à double écran et pliables.</span><span class="sxs-lookup"><span data-stu-id="9c890-111">[Turn on experimental Web Platform APIs](#turn-on-experimental-apis) and use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI] to enhance your website \(or app\) for dual-screen and foldable devices.</span></span>  

:::image type="complex" source="../media/experiments-surface-duo-emulation.msft.png" alt-text="Émuler Surface Duo dans Microsoft Edge" lightbox="../media/experiments-surface-duo-emulation.msft.png":::  
   <span data-ttu-id="9c890-113">Émuler Surface Duo dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9c890-113">Emulate Surface Duo in Microsoft Edge</span></span>  
:::image-end:::  

## <span data-ttu-id="9c890-114">Activer les API expérimentales</span><span class="sxs-lookup"><span data-stu-id="9c890-114">Turn on experimental APIs</span></span>  

<span data-ttu-id="9c890-115">Pour utiliser la fonctionnalité d’écran multimédia [CSS][DualScreenDocsCssMedia] et l’API [JavaScript getWindowSegments,][DualScreenDocsJSAPI]allumez l’indicateur `Experimental Web Platform features` dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9c890-115">To use the [CSS media screen-spanning feature][DualScreenDocsCssMedia] and [JavaScript getWindowSegments API][DualScreenDocsJSAPI], turn on the `Experimental Web Platform features` flag in Microsoft Edge.</span></span>  <span data-ttu-id="9c890-116">Effectuer les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="9c890-116">Complete the following steps.</span></span>  

1.  <span data-ttu-id="9c890-117">Accédez `edge://flags` à .</span><span class="sxs-lookup"><span data-stu-id="9c890-117">Navigate to `edge://flags`.</span></span>  
1.  <span data-ttu-id="9c890-118">Dans la **zone de texte Indicateurs de recherche,** entrez , choisissez l’indicateur des fonctionnalités de la plateforme Web expérimentale et modifiez Désactivé en `Experimental Web Platform features` **Activé.**  </span><span class="sxs-lookup"><span data-stu-id="9c890-118">In the **Search flags** textbox, enter `Experimental Web Platform features`, choose the **Experimental Web Platform features** flag, and change **Disabled** to **Enabled**.</span></span>  
1.  <span data-ttu-id="9c890-119">Redémarrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="9c890-119">Restart Microsoft Edge.</span></span>  
    
:::image type="complex" source="../media/experiments-dual-screen-emulation-edge-flags.msft.png" alt-text="Activer l’indicateur des fonctionnalités de plateforme Web expérimentale" lightbox="../media/experiments-dual-screen-emulation.msft.png":::
   <span data-ttu-id="9c890-121">Activer **l’indicateur des fonctionnalités de plateforme Web** expérimentale</span><span class="sxs-lookup"><span data-stu-id="9c890-121">Turn on the **Experimental Web Platform features** flag</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="9c890-122">Si vous utilisez des requêtes [multimédias CSS][DualScreenDocsCssMedia] ou l’API d’éumération de segment [Windows JavaScript][DualScreenDocsJSAPI] pour améliorer votre site web ou votre application pour [le Surface Duo,][SurfaceDevicesDuo]vous devez également activer l’indicateur des fonctionnalités de plateforme **web** expérimentale dans l’application Microsoft [Edge Android][GooglePlayMicrosoftEdge] sur votre appareil [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="9c890-122">If you are using [CSS media queries][DualScreenDocsCssMedia] or the [JavaScript Windows Segment Enumeration API][DualScreenDocsJSAPI] to enhance your website or app for the [Surface Duo][SurfaceDevicesDuo], you must also turn on the **Experimental Web Platform features** flag in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on your [Surface Duo][SurfaceDevicesDuo] device.</span></span>  
> 
> <span data-ttu-id="9c890-123">Si l’indicateur des fonctionnalités de la plateforme **Web** expérimentale est allumé dans le bureau [Microsoft Edge][MicrosoftEdge] et désactivé dans l’application Microsoft [Edge Android,][GooglePlayMicrosoftEdge]le comportement de votre site web ou de votre application dans l’émulateur Surface Duo dans le bureau Microsoft Edge ne correspond pas à l’application [Microsoft Edge Android][GooglePlayMicrosoftEdge] sur [Surface Duo.][SurfaceDevicesDuo]</span><span class="sxs-lookup"><span data-stu-id="9c890-123">If the **Experimental Web Platform features** flag is turned on in [desktop Microsoft Edge][MicrosoftEdge] and turned off in the [Android Microsoft Edge app][GooglePlayMicrosoftEdge], the behavior of your website or app in the Surface Duo emulator in desktop Microsoft Edge does not match with the [Android Microsoft Edge app][GooglePlayMicrosoftEdge] on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9c890-124">Assurez-vous que les indicateurs correspondent sur Android et le bureau Microsoft Edge pour utiliser correctement l’émulateur Surface Duo dans [le bureau Microsoft Edge][MicrosoftEdge].</span><span class="sxs-lookup"><span data-stu-id="9c890-124">Ensure that the flags match across Android and desktop Microsoft Edge to successfully use the Surface Duo emulator in [desktop Microsoft Edge][MicrosoftEdge].</span></span>  

## <span data-ttu-id="9c890-125">Test sur les appareils pliables et à double écran</span><span class="sxs-lookup"><span data-stu-id="9c890-125">Test on foldable and dual-screen devices</span></span>  

<span data-ttu-id="9c890-126">Lorsque vous émulez le [Surface Duo][SurfaceDevicesDuo] dans une posture à double écran dans Microsoft Edge, le seam \(l’espace entre les deux écrans\) est dessiné sur votre site web ou votre application.</span><span class="sxs-lookup"><span data-stu-id="9c890-126">When you emulate the [Surface Duo][SurfaceDevicesDuo] in a dual-screen posture in Microsoft Edge, the seam \(the space between the two screens\) is drawn over your website or app.</span></span>  

<span data-ttu-id="9c890-127">L’affichage émulé correspond à la façon dont votre site web \(ou application\) s’affiche dans l’application [Microsoft Edge Android][GooglePlayMicrosoftEdge] lors de l’exécution sur Surface [Duo][SurfaceDevicesDuo].</span><span class="sxs-lookup"><span data-stu-id="9c890-127">The emulated display matches the way your website \(or app\) renders in the [Microsoft Edge Android app][GooglePlayMicrosoftEdge] while running on [Surface Duo][SurfaceDevicesDuo].</span></span>  <span data-ttu-id="9c890-128">Vous de devez peut-être mettre à jour votre site web \(ou application\) pour une meilleure affichage le long du chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="9c890-128">You may have to update your website \(or app\) to display better along the seam.</span></span>  <span data-ttu-id="9c890-129">Pour plus d’informations sur l’adaptation de votre site web \(ou application\) au [seam,][DualScreenIntroductionHowWorkSeam]accédez à Comment utiliser le seam .</span><span class="sxs-lookup"><span data-stu-id="9c890-129">For more information about adapting your website \(or app\) to the seam, navigate to [How to work with the seam][DualScreenIntroductionHowWorkSeam].</span></span>  

<span data-ttu-id="9c890-130">La [barre d’outils d’appareil][DevtoolsDeviceModeIndexSimulateMobileViewport] propose des fonctionnalités supplémentaires pour vous aider à tester votre site web ou votre application dans plusieurs postures et orientations.</span><span class="sxs-lookup"><span data-stu-id="9c890-130">The [Device Toolbar][DevtoolsDeviceModeIndexSimulateMobileViewport] has additional features to help you test your website or app in multiple postures and orientations.</span></span>  <span data-ttu-id="9c890-131">Choose **Rotate** \( ![ Rotate ](../media/rotate-dark-icon.msft.png) \) to rotate the viewport to landscape orientation.</span><span class="sxs-lookup"><span data-stu-id="9c890-131">Choose **Rotate** \(![Rotate](../media/rotate-dark-icon.msft.png)\) to rotate the viewport to landscape orientation.</span></span> <span data-ttu-id="9c890-132">Combinez la fonctionnalité **avec Span** \( Span \) pour faire bascule entre un seul écran ou des postures pliées et double écran ![ ou ](../media/span-dark-icon.msft.png) dépliées.</span><span class="sxs-lookup"><span data-stu-id="9c890-132">Combine the feature with **Span** \(![Span](../media/span-dark-icon.msft.png)\) to toggle between single-screen or folded and dual-screen or unfolded postures.</span></span>  <span data-ttu-id="9c890-133">Ensemble, les fonctionnalités vous permettent de tester votre site web ou votre application dans les quatre postures et orientations possibles.</span><span class="sxs-lookup"><span data-stu-id="9c890-133">Together, the features allow you to test your website or app in all four possible postures and orientations.</span></span>  

:::image type="complex" source="../media/experiments-dual-screen-emulation-rotate-span.msft.png" alt-text="Matrice des postures et des orientations pour les appareils à double écran et pliables" lightbox="../media/experiments-dual-screen-emulation-rotate-span.msft.png":::
   <span data-ttu-id="9c890-135">Matrice des postures et des orientations pour les appareils à double écran et pliables</span><span class="sxs-lookup"><span data-stu-id="9c890-135">Matrix of postures and orientations for dual-screen and foldable devices</span></span>  
:::image-end:::  

<span data-ttu-id="9c890-136">L’icône Fonctionnalités **de plateforme Web** expérimentale \( ![ ExperimentalApis \) affiche l’état de l’indicateur des fonctionnalités de plateforme ](../media/experimental-apis-dark-icon.msft.png) **Web** expérimentale.</span><span class="sxs-lookup"><span data-stu-id="9c890-136">The **Experimental Web Platform features** \(![ExperimentalApis](../media/experimental-apis-dark-icon.msft.png)\) icon displays the state of the **Experimental Web Platform features** flag.</span></span>  <span data-ttu-id="9c890-137">Si l’indicateur est allumé, l’icône est mise en surbrillion.</span><span class="sxs-lookup"><span data-stu-id="9c890-137">If the flag is turned on, the icon is highlighted.</span></span>  <span data-ttu-id="9c890-138">Si l’indicateur est désactivé, l’icône n’est pas mise en surbrillion.</span><span class="sxs-lookup"><span data-stu-id="9c890-138">If the flag is turned off, the icon is not highlighted.</span></span>  <span data-ttu-id="9c890-139">Pour activer \(ou désactiver\) l’indicateur, choisissez l’icône ou accédez à l’indicateur et `edge://flags` basculez-le.</span><span class="sxs-lookup"><span data-stu-id="9c890-139">To turn on \(or off\) the flag, either choose the icon or navigate to `edge://flags` and toggle the flag.</span></span>  

> [!NOTE]
> <span data-ttu-id="9c890-140">Voici une liste des problèmes connus actuels.</span><span class="sxs-lookup"><span data-stu-id="9c890-140">The following is a list of current known issues.</span></span>  
> 
> *   <span data-ttu-id="9c890-141">Lorsque vous utilisez un [client Bureau][RemoteDesktopClientDocs] à distance Microsoft pour vous connecter à un PC distant et émuler le [Surface Duo][SurfaceDevicesDuo] ou Samsung [Samsung Fold,][SamsungMobileGalaxyFold]le pointeur peut être agité ou sacrculé.</span><span class="sxs-lookup"><span data-stu-id="9c890-141">When you use a [Microsoft Remote Desktop client][RemoteDesktopClientDocs] to connect to a remote PC and emulate the [Surface Duo][SurfaceDevicesDuo] or [Samsung Galaxy Fold][SamsungMobileGalaxyFold], the pointer may shake or stutter.</span></span>  <span data-ttu-id="9c890-142">Si vous avez affaire au problème, envoyez [des commentaires.](#getting-in-touch-with-the-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="9c890-142">If you run into the issue, [send feedback](#getting-in-touch-with-the-microsoft-edge-devtools-team).</span></span>  

## <span data-ttu-id="9c890-143">Ressources complémentaires</span><span class="sxs-lookup"><span data-stu-id="9c890-143">Additional Resources</span></span>  

<span data-ttu-id="9c890-144">Voici des ressources supplémentaires qui peuvent vous aider à améliorer votre site web \(ou application\) pour les appareils à double écran.</span><span class="sxs-lookup"><span data-stu-id="9c890-144">Here are additional resources that may help you enhance your website \(or app\) for dual-screen devices.</span></span>  

*   <span data-ttu-id="9c890-145">Pour plus d’informations sur le développement web sur les appareils à double écran, accédez à [Expériences web à double écran.][DualScreenWebIndex]</span><span class="sxs-lookup"><span data-stu-id="9c890-145">For more information about web development on dual-screen devices, navigate to [Dual-screen web experiences][DualScreenWebIndex].</span></span>  
*   <span data-ttu-id="9c890-146">Installez [l’émulateur Surface Duo.][DualScreenAndroidUseEmulator]</span><span class="sxs-lookup"><span data-stu-id="9c890-146">Install the [Surface Duo emulator][DualScreenAndroidUseEmulator].</span></span>  <span data-ttu-id="9c890-147">L’émulateur Surface Duo est différent de l’émulateur dans Microsoft Edge, exécute Android et s’intègre à [Android Studio.][AndroidDeveloperStudio]</span><span class="sxs-lookup"><span data-stu-id="9c890-147">The Surface Duo emulator is different from the emulator in Microsoft Edge, runs Android, and integrates with [Android Studio][AndroidDeveloperStudio].</span></span>  <span data-ttu-id="9c890-148">Pour plus d’informations, [accédez à Obtenir le SDK Surface Duo.][DualScreenAndroidGetDuoSdk]</span><span class="sxs-lookup"><span data-stu-id="9c890-148">For more information, navigate to [Get the Surface Duo SDK][DualScreenAndroidGetDuoSdk].</span></span>  

## <span data-ttu-id="9c890-149">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="9c890-149">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsDeviceModeIndexSimulateMobileViewport]: ../device-mode/index.md#simulate-a-mobile-viewport "Simuler des appareils mobiles avec le mode appareil dans Microsoft Edge DevTools | Microsoft Edge"  

[DualScreenWebIndex]: /dual-screen/web/index "Expériences web à double écran | Documents Microsoft"  
[DualScreenAndroidGetDuoSdk]: /dual-screen/android/get-duo-sdk "Obtenir l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenIntroductionHowWorkSeam]: /dual-screen/introduction#how-to-work-with-the-seam "Comment travailler avec le seam : introduction aux appareils à double écran | Documents Microsoft"  
[DualScreenAndroidUseEmulator]: /dual-screen/android/use-emulator "Utiliser l’émulateur Surface Duo | Documents Microsoft"  
[DualScreenDocsCssMedia]: /dual-screen/web/css-media-spanning "Fonctionnalité d’écran multimédia CSS pour la détection à double écran | Documents Microsoft"  
[DualScreenDocsJSAPI]: /dual-screen/web/javascript-getwindowsegments "L’API JavaScript getWindowSegments pour les appareils à double écran | Documents Microsoft"  

[RemoteDesktopClientDocs]: /windows-server/remote/remote-desktop-services/clients/remote-desktop-clients "Clients Bureau à distance | Documents Microsoft"

[MicrosoftEdge]: https://www.microsoft.com/edge "Microsoft Edge"  

[SurfaceDevicesDuo]: https://www.microsoft.com/surface/devices/surface-duo "Surface Duo | Microsoft Surface"  

[AndroidDeveloperStudio]: https://developer.android.com/studio/ "Android Studio"  

[GooglePlayMicrosoftEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Microsoft Edge | Google Play"  

[SamsungMobileGalaxyFold]: https://www.samsung.com/mobile/galaxy-fold/ "| Samsung"  
