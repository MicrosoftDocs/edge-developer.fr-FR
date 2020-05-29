---
description: Utiliser le volet d’émulation pour tester différents profils de navigateur, tailles d’écran et résolutions, et coordonnées d’emplacement GPS
title: Émulation DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, émulation d’appareil, conception réactive, géolocalisation, résolution
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565570"
---
# <span data-ttu-id="d39cb-104">Émulation</span><span class="sxs-lookup"><span data-stu-id="d39cb-104">Emulation</span></span>

<span data-ttu-id="d39cb-105">Le panneau d' *émulation* vous permet d’effectuer les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="d39cb-105">The *Emulation* panel helps you to:</span></span>
 - <span data-ttu-id="d39cb-106">Simuler divers [profils d’appareil](#device), [navigateurs](#browser-profile), tailles d' [écran et résolutions](#display)</span><span class="sxs-lookup"><span data-stu-id="d39cb-106">Simulate various [device profiles](#device), [browsers](#browser-profile), [screen sizes and resolutions](#display)</span></span>
 - <span data-ttu-id="d39cb-107">Tester différents [paramètres et coordonnées de géolocalisation](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="d39cb-107">Test different [geolocation settings and coordinates](#geolocation)</span></span>

![Panneau d’émulation Microsoft Edge DevTools](./media/emulation.png)

1. <span data-ttu-id="d39cb-109">Le bouton **conserver les paramètres d’émulation** de bureau enregistre les modifications que vous avez effectuées à partir des paramètres d’émulation de bureau par défaut, même lorsque vous fermez et rouvrez le devtools.</span><span class="sxs-lookup"><span data-stu-id="d39cb-109">The **Persist Emulation settings** button will save any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span> 

2. <span data-ttu-id="d39cb-110">Le bouton **Réinitialiser les paramètres d’émulation** rétablit les paramètres d’émulation de votre navigateur de *Bureau* par défaut et de la chaîne de l’agent utilisateur Microsoft Edge pour lesquels le GPS est désactivé.</span><span class="sxs-lookup"><span data-stu-id="d39cb-110">The **Reset Emulation settings** button will reset your emulation settings back to the default *Desktop* browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>

3. <span data-ttu-id="d39cb-111">Lorsque l’une de ces options est modifiée par défaut, l’onglet **émulation** affiche une alerte d’information indiquant que l’aspect du comportement de votre navigateur est émulé.</span><span class="sxs-lookup"><span data-stu-id="d39cb-111">When any of these options are changed from the default, the **Emulation** tab will show an informational alert to indicate that some aspect of your browser's behavior is being emulated.</span></span>

## <span data-ttu-id="d39cb-112">Appareil</span><span class="sxs-lookup"><span data-stu-id="d39cb-112">Device</span></span>

<span data-ttu-id="d39cb-113">Faites votre choix parmi une liste prédéfinie de profils d’appareils Windows qui configurent automatiquement les autres options d’émulation ou spécifiez votre propre configuration *personnalisée* .</span><span class="sxs-lookup"><span data-stu-id="d39cb-113">Pick from a preset list of Windows device profiles which  automatically configure the other emulation options or specify your own *Custom* configuation.</span></span> <span data-ttu-id="d39cb-114">Revenez à la *valeur par défaut* pour réinitialiser tous les outils d’émulation.</span><span class="sxs-lookup"><span data-stu-id="d39cb-114">Switch back to *Default* to reset all the emulation tools.</span></span>

## <span data-ttu-id="d39cb-115">Mode</span><span class="sxs-lookup"><span data-stu-id="d39cb-115">Mode</span></span>

### <span data-ttu-id="d39cb-116">Profil du navigateur</span><span class="sxs-lookup"><span data-stu-id="d39cb-116">Browser profile</span></span>
<span data-ttu-id="d39cb-117">Pour simuler une page en cours d’exécution sur un appareil Windows Phone, il est recommandé de changer le paramètre de **Profil du navigateur** sur *Windows Phone*.</span><span class="sxs-lookup"><span data-stu-id="d39cb-117">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to *Windows Phone*.</span></span>

#### <span data-ttu-id="d39cb-118">Chaîne de l’agent utilisateur</span><span class="sxs-lookup"><span data-stu-id="d39cb-118">User agent string</span></span>

<span data-ttu-id="d39cb-119">La modification de la chaîne de l’agent utilisateur pour reproduire un autre navigateur est une bonne première étape du débogage des erreurs qui se produisent uniquement dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d39cb-119">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span> 

<span data-ttu-id="d39cb-120">Les scripts frontal et/ou principal peuvent parfois utiliser une chaîne d’agent utilisateur pour détecter le navigateur que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="d39cb-120">Front end and/or back end scripts sometimes use the user agent string  to detect which browser you're using.</span></span> <span data-ttu-id="d39cb-121">Même si vous n’utilisez pas la détection de navigateur dans votre propre code, vous utilisez peut-être une bibliothèque JavaScript tierce ou un script côté serveur.</span><span class="sxs-lookup"><span data-stu-id="d39cb-121">And even when you're not using browser detection in your own code, you may be using a third-party JavaScript library or server-side script that does.</span></span>

<span data-ttu-id="d39cb-122">Le problème lié à la détection du navigateur est qu’il est souvent utilisé pour mettre à l’échelle ou changer les fonctionnalités d’une page Web en fonction de ce que votre navigateur peut faire, au lieu de détecter ce que votre navigateur peut faire à l’aide de la détection de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="d39cb-122">The problem with browser detection is that it's often used to scale back or change the features in a webpage based on what the developer writing the script thinks your browser can do, rather than detecting what your browser can actually do using feature detection.</span></span> <span data-ttu-id="d39cb-123">Cela peut entraîner un comportement inattendu, car le code ciblé sur Windows Internet Explorer 8 peut s’exécuter très différemment dans Microsoft Edge. vous pouvez également désactiver la prise en charge des fonctionnalités de votre navigateur en raison d’une supposition faite par le développeur.</span><span class="sxs-lookup"><span data-stu-id="d39cb-123">This can cause unexpected behavior, because code targeted at Windows Internet Explorer 8 can run very differently in Microsoft Edge; or a feature your browser is perfectly capable of supporting might be disabled because of an assumption made by the developer.</span></span>

<span data-ttu-id="d39cb-124">Si la modification de la chaîne de l’agent utilisateur permet de résoudre le problème, la détection du navigateur est probablement coupable.</span><span class="sxs-lookup"><span data-stu-id="d39cb-124">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>

## <span data-ttu-id="d39cb-125">Affichage</span><span class="sxs-lookup"><span data-stu-id="d39cb-125">Display</span></span>

<span data-ttu-id="d39cb-126">L’émulation d’affichage vous permet d’afficher un aperçu de votre site sur différentes tailles et résolutions d’écran: des écrans de bureau classiques aux écrans mobiles plus petits ou des écrans de haute résolution plus récents.</span><span class="sxs-lookup"><span data-stu-id="d39cb-126">Display emulation lets you preview your site on different screen sizes and resolutions: from conventional desktop monitors to smaller mobile screens or newer high-resolution displays.</span></span>

<span data-ttu-id="d39cb-127">Les émulations sont adaptées pour essayer de correspondre aux dimensions physiques des écrans émulés.</span><span class="sxs-lookup"><span data-stu-id="d39cb-127">Emulations are adapted to try and match the physical dimensions of the screens being emulated.</span></span> <span data-ttu-id="d39cb-128">Les pixels émulés peuvent apparaître comme comprimés ou développés, et l’émulation n’est pas recommandée si vous avez besoin de tester le positionnement des éléments HTML en pixels.</span><span class="sxs-lookup"><span data-stu-id="d39cb-128">Emulated pixels might appear compressed or expanded, and emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span> <span data-ttu-id="d39cb-129">L’émulation est toutefois bien adaptée aux tests de conception réactive et à l’identification de grands problèmes de positionnement d’éléments.</span><span class="sxs-lookup"><span data-stu-id="d39cb-129">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>

### <span data-ttu-id="d39cb-130">Orientation</span><span class="sxs-lookup"><span data-stu-id="d39cb-130">Orientation</span></span>

<span data-ttu-id="d39cb-131">Choisissez le mode *paysage* ou *portrait* .</span><span class="sxs-lookup"><span data-stu-id="d39cb-131">Choose from *Landscape* or *Portrait* mode.</span></span>

### <span data-ttu-id="d39cb-132">Résolution</span><span class="sxs-lookup"><span data-stu-id="d39cb-132">Resolution</span></span>

<span data-ttu-id="d39cb-133">Faites votre choix parmi une liste prédéfinie de résolutions d’appareils populaires ou spécifiez votre propre configuration *personnalisée* . Les résolutions de 80 pouces et 3820 x 2160 sont prises en charge.</span><span class="sxs-lookup"><span data-stu-id="d39cb-133">Choose from a preset list of popular device resolutions, or specify your own *Custom* config. Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>

## <span data-ttu-id="d39cb-134">Géolocalisation</span><span class="sxs-lookup"><span data-stu-id="d39cb-134">Geolocation</span></span>

<span data-ttu-id="d39cb-135">Si votre site utilise l' [API de géolocalisation](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) pour fournir des services de géolocalisation, vous pouvez facilement tester différentes coordonnées GPS et États de capteur à partir de la commodité de votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="d39cb-135">If your site uses the [Geolocation API](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) to provide location-based services, you can easily test different GPS coordinates and sensor states from the convenience of your desktop.</span></span> <span data-ttu-id="d39cb-136">Ces paramètres remplaceront les coordonnées GPS et l’état du capteur sur les ordinateurs qui prennent en charge la géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="d39cb-136">These settings will override any actual GPS coordinates and the sensor state on machines that support geolocation.</span></span> 

<span data-ttu-id="d39cb-137">Comme pour toute utilisation de données personnelles sur le Web, vos utilisateurs doivent d’abord accorder l’autorisation de votre site à l’utilisation de leur emplacement.</span><span class="sxs-lookup"><span data-stu-id="d39cb-137">As with any usage of personal data on the web, your users will first need to grant your site permission to use their location.</span></span> <span data-ttu-id="d39cb-138">Vous pouvez tester le comportement de votre site avec et sans autorisation d’emplacement du panneau *paramètres* de Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="d39cb-138">You can test how your site behaves with and without location permissions from the Microsoft Edge *Settings* panel:</span></span>

<span data-ttu-id="d39cb-139">**...** >  **Paramètres**  >  **Afficher les paramètres avancés**  >  Autorisations de site **Web**  >  **Gestion**</span><span class="sxs-lookup"><span data-stu-id="d39cb-139">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>

![Gérer les autorisations de site Web à partir du panneau Paramètres de Microsoft Edge](./media/settings_manage_permissions.png)

## <span data-ttu-id="d39cb-141">Associés</span><span class="sxs-lookup"><span data-stu-id="d39cb-141">Shortcuts</span></span>

| <span data-ttu-id="d39cb-142">Action</span><span class="sxs-lookup"><span data-stu-id="d39cb-142">Action</span></span>                   | <span data-ttu-id="d39cb-143">Raccourci</span><span class="sxs-lookup"><span data-stu-id="d39cb-143">Shortcut</span></span>               |
|:-------------------------|:-----------------------|
| <span data-ttu-id="d39cb-144">Réinitialiser les paramètres d’émulation</span><span class="sxs-lookup"><span data-stu-id="d39cb-144">Reset Emulation settings</span></span> | `CTRL` + `SHIFT` + `L` |
