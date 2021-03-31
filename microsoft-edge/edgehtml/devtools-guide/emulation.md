---
description: Utiliser le volet d’émulation pour tester différents profils de navigateur, tailles d’écran et résolutions, et coordonnées d’emplacement GPS
title: Émulation DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, émulation d’appareil, conception réactive, géolocalisation, résolution
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: af740472f22a8b322c03cb672a3da909ef195fac
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233035"
---
# <span data-ttu-id="83577-104">Émulation</span><span class="sxs-lookup"><span data-stu-id="83577-104">Emulation</span></span>  

> [!NOTE]
> <span data-ttu-id="83577-105">Le nouveau Microsoft Edge est conçu à l’aide du chrome et commence à la version 75.</span><span class="sxs-lookup"><span data-stu-id="83577-105">The new Microsoft Edge is built using Chromium, and starts at version 75.</span></span>  <span data-ttu-id="83577-106">Pour plus d’informations, [Téléchargez le nouveau Microsoft Edge][MicrosoftNewEdge]et testez les nouveaux [outils de développement Microsoft Edge (chrome)][DevtoolsGuideChromium].</span><span class="sxs-lookup"><span data-stu-id="83577-106">For more information, [download the new Microsoft Edge][MicrosoftNewEdge], and try out the new [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromium].</span></span>  
> 
> <span data-ttu-id="83577-107">Pour émuler différents appareils, navigateurs, tailles d’écran et résolutions dans le nouveau DevTools, accédez à la section [émuler des appareils mobiles dans Microsoft Edge \(chrome \) devtools][DevtoolsGuideChromiumDeviceMode].</span><span class="sxs-lookup"><span data-stu-id="83577-107">To emulate different devices, browsers, screen sizes, and resolutions in the new DevTools, navigate to [Emulate Mobile Devices in Microsoft Edge \(Chromium\) DevTools][DevtoolsGuideChromiumDeviceMode].</span></span>  

<span data-ttu-id="83577-108">Le panneau d' **émulation** facilite les activités suivantes.</span><span class="sxs-lookup"><span data-stu-id="83577-108">The **Emulation** panel helps with the following activities.</span></span>    

*   <span data-ttu-id="83577-109">Simuler divers [profils d’appareil](#device), [navigateurs](#browser-profile), tailles d' [écran et résolutions](#display)</span><span class="sxs-lookup"><span data-stu-id="83577-109">Simulate various [device profiles](#device), [browsers](#browser-profile), and [screen sizes and resolutions](#display)</span></span>  
*   <span data-ttu-id="83577-110">Tester différents [paramètres et coordonnées de géolocalisation](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="83577-110">Test different [geolocation settings and coordinates](#geolocation)</span></span>  

:::image type="complex" source="./media/emulation.png" alt-text="Panneau d’émulation Microsoft Edge DevTools" lightbox="./media/emulation.png":::
   <span data-ttu-id="83577-112">Panneau d' **émulation** Microsoft Edge devtools</span><span class="sxs-lookup"><span data-stu-id="83577-112">The Microsoft Edge DevTools **Emulation** panel</span></span>  
:::image-end:::  

1.  <span data-ttu-id="83577-113">Le bouton **conserver les paramètres d’émulation** vous permet d’enregistrer les modifications que vous avez effectuées à partir des paramètres d’émulation de bureau par défaut, même lorsque vous fermez et rouvrez le devtools.</span><span class="sxs-lookup"><span data-stu-id="83577-113">The **Persist Emulation settings** button saves any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span>  

1.  <span data-ttu-id="83577-114">Le bouton **Réinitialiser les paramètres d’émulation** rétablit les paramètres d’émulation par défaut du profil du navigateur de bureau et de la chaîne de l’agent utilisateur Microsoft Edge avec le GPS désactivé.</span><span class="sxs-lookup"><span data-stu-id="83577-114">The **Reset Emulation settings** button resets your emulation settings back to the default Desktop browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>  

1.  <span data-ttu-id="83577-115">Lorsque l’une de ces options est modifiée par défaut, l’onglet d' **émulation** affiche une alerte d’information indiquant qu’un aspect du comportement de votre navigateur est émulé.</span><span class="sxs-lookup"><span data-stu-id="83577-115">When any of these options are changed from the default, the **Emulation** tab displays an informational alert to indicate that some aspect of the behavior of your browser is being emulated.</span></span>  

## <span data-ttu-id="83577-116">Appareil</span><span class="sxs-lookup"><span data-stu-id="83577-116">Device</span></span>  

<span data-ttu-id="83577-117">Faites votre choix parmi une liste prédéfinie de profils d’appareils Windows qui configurent automatiquement les autres options d’émulation ou spécifiez votre propre configuration **personnalisée** .</span><span class="sxs-lookup"><span data-stu-id="83577-117">Pick from a preset list of Windows device profiles that automatically configure the other emulation options or specify your own **Custom** configuration.</span></span>  <span data-ttu-id="83577-118">Revenez à la **valeur par défaut** pour réinitialiser tous les outils d’émulation.</span><span class="sxs-lookup"><span data-stu-id="83577-118">Switch back to **Default** to reset all the emulation tools.</span></span>  

## <span data-ttu-id="83577-119">Mode</span><span class="sxs-lookup"><span data-stu-id="83577-119">Mode</span></span>  

### <span data-ttu-id="83577-120">Profil du navigateur</span><span class="sxs-lookup"><span data-stu-id="83577-120">Browser profile</span></span>  

<span data-ttu-id="83577-121">Pour simuler une page en cours d’exécution sur un appareil Windows Phone, il est recommandé de changer le paramètre de **Profil du navigateur** sur **Windows Phone**.</span><span class="sxs-lookup"><span data-stu-id="83577-121">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to **Windows Phone**.</span></span>  

#### <span data-ttu-id="83577-122">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="83577-122">User agent string</span></span>  

<span data-ttu-id="83577-123">La modification de la chaîne de l’agent utilisateur pour reproduire un autre navigateur est une bonne première étape du débogage des erreurs qui se produisent uniquement dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="83577-123">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span>  

<span data-ttu-id="83577-124">Les scripts utilisent la chaîne de l’agent utilisateur pour détecter le navigateur utilisé.</span><span class="sxs-lookup"><span data-stu-id="83577-124">Scripts use the user agent string to detect which browser is used.</span></span>  <span data-ttu-id="83577-125">Le script est susceptible d’être frontal, principal, principal, frontal et principal.</span><span class="sxs-lookup"><span data-stu-id="83577-125">Script may be front-end, back-end, or front-end and back-end.</span></span>  <span data-ttu-id="83577-126">Même si votre code n’utilise pas la détection de navigateur, votre code peut en hériter à partir d’une bibliothèque JavaScript tierce ou d’un script côté serveur.</span><span class="sxs-lookup"><span data-stu-id="83577-126">Although your code does not use browser detection, your code may inherit it from a third-party JavaScript library or server-side script.</span></span>  

<span data-ttu-id="83577-127">Dans le cas d’une détection de navigateur, vous pouvez mettre à l’échelle les fonctionnalités de votre navigateur (ou changer \) dans votre page Web à l’aide d’hypothèses sur les fonctionnalités du navigateur.</span><span class="sxs-lookup"><span data-stu-id="83577-127">The problem with browser detection is that you may scale-back \(or change\) features in your webpage using assumptions about browser capabilities.</span></span> <span data-ttu-id="83577-128">À la place, vous devez envisager de détecter les fonctionnalités de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="83577-128">Instead, you should consider using feature detection to detect the capabilities of your browser.</span></span>  <span data-ttu-id="83577-129">Un comportement inattendu est susceptible de se produire en raison de l’une des situations suivantes.</span><span class="sxs-lookup"><span data-stu-id="83577-129">Unexpected behavior may occur because of one of the following situations.</span></span>  

*   <span data-ttu-id="83577-130">Le code ciblé sur Windows Internet Explorer 8 s’exécute différemment dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="83577-130">Code targeted at Windows Internet Explorer 8 may run differently in Microsoft Edge.</span></span>  
*   <span data-ttu-id="83577-131">Une fonctionnalité prise en charge par votre navigateur est désactivée en raison d’une supposition faite par le développeur.</span><span class="sxs-lookup"><span data-stu-id="83577-131">A feature that your browser should support is disabled, because of an assumption made by the developer.</span></span>  

<span data-ttu-id="83577-132">Si la modification de la chaîne de l’agent utilisateur permet de résoudre le problème, la détection du navigateur est probablement coupable.</span><span class="sxs-lookup"><span data-stu-id="83577-132">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>  

## <span data-ttu-id="83577-133">Affichage</span><span class="sxs-lookup"><span data-stu-id="83577-133">Display</span></span>  

<span data-ttu-id="83577-134">Afficher l’émulation pour afficher un aperçu de votre site sur différentes tailles et résolutions d’écran.</span><span class="sxs-lookup"><span data-stu-id="83577-134">Display emulation to preview your site on different screen sizes and resolutions.</span></span>  

*   <span data-ttu-id="83577-135">écrans de bureau classiques</span><span class="sxs-lookup"><span data-stu-id="83577-135">conventional desktop monitors</span></span>  
*   <span data-ttu-id="83577-136">écrans mobiles plus petits</span><span class="sxs-lookup"><span data-stu-id="83577-136">smaller mobile screens</span></span>  
*   <span data-ttu-id="83577-137">affichages de haute résolution plus récents</span><span class="sxs-lookup"><span data-stu-id="83577-137">newer high-resolution displays</span></span>  

<span data-ttu-id="83577-138">Les émulations sont adaptées pour essayer de correspondre aux dimensions physiques des écrans émulés.</span><span class="sxs-lookup"><span data-stu-id="83577-138">Emulations are adapted to try to match the physical dimensions of the screens being emulated.</span></span>  <span data-ttu-id="83577-139">Les pixels émulés apparaissent comme comprimés ou développés.</span><span class="sxs-lookup"><span data-stu-id="83577-139">Emulated pixels may appear compressed or expanded.</span></span> <span data-ttu-id="83577-140">Il n’est pas recommandé d’utiliser l’émulation si vous avez besoin de tester le positionnement des éléments HTML en pixels.</span><span class="sxs-lookup"><span data-stu-id="83577-140">Emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span>  <span data-ttu-id="83577-141">L’émulation est toutefois bien adaptée aux tests de conception réactive et à l’identification de grands problèmes de positionnement d’éléments.</span><span class="sxs-lookup"><span data-stu-id="83577-141">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>  

### <span data-ttu-id="83577-142">Orientation</span><span class="sxs-lookup"><span data-stu-id="83577-142">Orientation</span></span>  

<span data-ttu-id="83577-143">Choisissez le mode **paysage** ou **portrait** .</span><span class="sxs-lookup"><span data-stu-id="83577-143">Choose from **Landscape** or **Portrait** mode.</span></span>  

### <span data-ttu-id="83577-144">Résolution</span><span class="sxs-lookup"><span data-stu-id="83577-144">Resolution</span></span>  

<span data-ttu-id="83577-145">Faites votre choix parmi une liste prédéfinie de résolutions d’appareils populaires ou spécifiez votre propre configuration **personnalisée** .  Les résolutions de 80 pouces et 3820 x 2160 sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="83577-145">Choose from a preset list of popular device resolutions, or specify your own **Custom** config.  Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>  

## <span data-ttu-id="83577-146">Géolocalisation</span><span class="sxs-lookup"><span data-stu-id="83577-146">Geolocation</span></span>  

<span data-ttu-id="83577-147">Si votre site Web utilise l' [API de géolocalisation][MdnGeolocationUsing] pour fournir des services de géolocalisation, les activités suivantes sont disponibles dans la commodité de votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="83577-147">If your website uses the [Geolocation API][MdnGeolocationUsing] to provide location-based services, the following activities are available from the convenience of your desktop.</span></span>  

*   <span data-ttu-id="83577-148">Testez facilement différentes coordonnées GPS</span><span class="sxs-lookup"><span data-stu-id="83577-148">easily test different GPS coordinates</span></span>  
*   <span data-ttu-id="83577-149">Testez facilement différents États des capteurs</span><span class="sxs-lookup"><span data-stu-id="83577-149">easily test different sensor states</span></span>  

<span data-ttu-id="83577-150">Les paramètres remplacent toutes les coordonnées GPS réelles et l’état du capteur sur les appareils qui prennent en charge la géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="83577-150">The settings override any actual GPS coordinates and the sensor state on devices that support geolocation.</span></span>  

<span data-ttu-id="83577-151">Votre site Web doit demander l’autorisation d’un utilisateur et l’octroyer avant de l’emplacement de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="83577-151">Your website must request and be granted permission from a user before using the device location.</span></span>  <span data-ttu-id="83577-152">Testez le comportement de votre site avec et sans autorisation d’emplacement du panneau **paramètres** de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="83577-152">Test how your site behaves with and without location permissions from the Microsoft Edge **Settings** panel.</span></span>  

<span data-ttu-id="83577-153">**...** >  **Paramètres**  >  **Afficher les paramètres avancés**  >  Autorisations de site **Web**  >  **Gestion**</span><span class="sxs-lookup"><span data-stu-id="83577-153">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>  

:::image type="complex" source="./media/settings_manage_permissions.png" alt-text="Gérer les autorisations de site Web à partir du panneau Paramètres de Microsoft Edge" lightbox="./media/settings_manage_permissions.png":::
   <span data-ttu-id="83577-155">Gérer les autorisations de site Web à partir du panneau **paramètres** de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="83577-155">Manage website permissions from the Microsoft Edge **Settings** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="83577-156">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="83577-156">Shortcuts</span></span>

| <span data-ttu-id="83577-157">Action</span><span class="sxs-lookup"><span data-stu-id="83577-157">Action</span></span>  | <span data-ttu-id="83577-158">Raccourci</span><span class="sxs-lookup"><span data-stu-id="83577-158">Shortcut</span></span>  |  
|:--- |:--- |  
| <span data-ttu-id="83577-159">Réinitialiser les paramètres d’émulation</span><span class="sxs-lookup"><span data-stu-id="83577-159">Reset Emulation settings</span></span> | `Ctrl`+`Shift`+`L` |  

<!-- links -->  


[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsGuideChromiumDeviceMode]: /microsoft-edge/devtools-guide-chromium/device-mode "Émuler des appareils mobiles dans Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftNewEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  

[MdnGeolocationUsing]: https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation "API de géolocalisation | MDN"  
