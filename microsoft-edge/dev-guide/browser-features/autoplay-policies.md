---
description: Garantir le fonctionnement du contenu multimédia sur votre site
title: Guide de développement-stratégies de lecture automatique
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 9/17/2018
ms.topic: article
ms.prod: microsoft-edge
keywords: bordure, média, vidéo, audio, lecture automatique
ms.custom: seodec18
ms.openlocfilehash: 397c6f0a22359dbfab7c44370b0429147b7c9834
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564701"
---
# <span data-ttu-id="ae10a-104">Stratégies de lecture automatique</span><span class="sxs-lookup"><span data-stu-id="ae10a-104">Autoplay Policies</span></span>

<span data-ttu-id="ae10a-105">Microsoft Edge offre aux utilisateurs la possibilité de personnaliser leurs préférences de navigation sur les sites Web qui entourent le son par lecture automatique afin de réduire le nombre de distractions sur le Web et de économiser la bande passante.</span><span class="sxs-lookup"><span data-stu-id="ae10a-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span> <span data-ttu-id="ae10a-106">En outre, Microsoft Edge supprime automatiquement la lecture automatique de contenus multimédias dans les onglets d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ae10a-106">Additionaly, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>

<span data-ttu-id="ae10a-107">Les utilisateurs peuvent personnaliser le comportement du contenu multimédia avec les contrôles de lecture automatique [globaux](#global-media-autoplay-settings) et [par site](#per-site-media-autoplay-settings) , qui fournissent les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="ae10a-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>

- <span data-ttu-id="ae10a-108">**Allow** est la valeur par défaut et continue de lire les vidéos lorsqu’un onglet est d’abord affiché au premier plan, à l’aide du site discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="ae10a-108">**Allow**  is the default and will continue to play videos when a tab is first viewed in the foreground, at the site’s discretion.</span></span>

- <span data-ttu-id="ae10a-109">**Limit** limitera la lecture automatique de manière à ne fonctionner que lorsque les vidéos sont muettes, afin que les utilisateurs ne soient jamais surpris par le son.</span><span class="sxs-lookup"><span data-stu-id="ae10a-109">**Limit** will restrict autoplay to only work when videos are muted, so users are never surprised by sound.</span></span> <span data-ttu-id="ae10a-110">Lorsque l’utilisateur clique n’importe où sur la page, la lecture automatique est réactivée et continue d’être autorisée dans ce domaine sous cet onglet.</span><span class="sxs-lookup"><span data-stu-id="ae10a-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>

- <span data-ttu-id="ae10a-111">**Bloquer** empêche la lecture automatique sur tous les sites tant que les utilisateurs n’interagissent pas avec le contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae10a-111">**Block** will prevent autoplay on all sites until users directly interact with the media content.</span></span>

## <span data-ttu-id="ae10a-112">Paramètres généraux de lecture multimédias</span><span class="sxs-lookup"><span data-stu-id="ae10a-112">Global media autoplay settings</span></span>

<span data-ttu-id="ae10a-113">Les utilisateurs peuvent contrôler le comportement de lecture automatique par défaut pour tous les sites sous **Paramètres avancés**de  >  **lecture automatique de médias**.</span><span class="sxs-lookup"><span data-stu-id="ae10a-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>

![Paramètres généraux de lecture multimédias](../media/autoplay_global.png)

## <span data-ttu-id="ae10a-115">Paramètres de lecture automatique de média par site</span><span class="sxs-lookup"><span data-stu-id="ae10a-115">Per-site media autoplay settings</span></span>

<span data-ttu-id="ae10a-116">Les utilisateurs peuvent contrôler le comportement de la lecture automatique sur une base par site sous la section **autorisations de site Web** du volet informations sur le site Web.</span><span class="sxs-lookup"><span data-stu-id="ae10a-116">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span> <span data-ttu-id="ae10a-117">Ce paramètre est disponible en cliquant sur l’icône d’information ou sur l’icône de verrouillage située sur le côté gauche de la barre d’adresse, puis en cliquant sur «paramètres de lecture automatique de média» pour commencer.</span><span class="sxs-lookup"><span data-stu-id="ae10a-117">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on “Media autoplay settings” to get started.</span></span>

<span data-ttu-id="ae10a-118">Les paramètres par site remplacent le paramètre global.</span><span class="sxs-lookup"><span data-stu-id="ae10a-118">Per-site settings override the global setting.</span></span> <span data-ttu-id="ae10a-119">Par exemple, si un utilisateur a défini le paramètre global sur «Allow» mais qu’il définit un paramètre par site en «Block», la lecture automatique est bloquée pour ce site.</span><span class="sxs-lookup"><span data-stu-id="ae10a-119">For example, if a user has their global setting set to “Allow” but changes a per-site setting to “Block”, autoplay will be blocked for that site.</span></span>

![Paramètres de lecture automatique de média par site](../media/autoplay_per-site.png)
 
## <span data-ttu-id="ae10a-121">Meilleures pratiques pour les développeurs Web</span><span class="sxs-lookup"><span data-stu-id="ae10a-121">Best Practices for Web Developers</span></span>

<span data-ttu-id="ae10a-122">Pour garantir une bonne utilisation de l’utilisateur avec le contenu multimédia hébergé sur votre site, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ae10a-122">Here's how to ensure a good user experience with media hosted on your site:</span></span>

- <span data-ttu-id="ae10a-123">Supposez que chaque utilisation d’un élément multimédia nécessite un mouvement utilisateur pour démarrer la lecture (car les utilisateurs peuvent bloquer la lecture automatique à tout moment) et planifier en conséquence.</span><span class="sxs-lookup"><span data-stu-id="ae10a-123">Assume  each use of a media element wil require a user gesture to start the playback (as users can block autoplay at any point in time) and plan accordingly.</span></span>  <span data-ttu-id="ae10a-124">Les stratégies de lecture globale et globales par site s’appliquent à `<audio>` l’ensemble et aux `<video>` éléments, quelle que soit la façon dont ils sont utilisés sur votre site.</span><span class="sxs-lookup"><span data-stu-id="ae10a-124">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>

- <span data-ttu-id="ae10a-125">Assurez-vous que les contrôles multimédias sont toujours présents sur les éléments multimédias et les contenus publicitaires.</span><span class="sxs-lookup"><span data-stu-id="ae10a-125">Ensure that media controls are always present on both site media and ad content.</span></span> <span data-ttu-id="ae10a-126">Cela permettra aux utilisateurs de redémarrer la lecture si la lecture automatique est bloquée sur la page.</span><span class="sxs-lookup"><span data-stu-id="ae10a-126">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>

- <span data-ttu-id="ae10a-127">Évaluez la façon dont la lecture automatique peut affecter l’utilisation des utilisateurs sur votre site Web et envisager d’utiliser la lecture automatique de manière à limiter la lecture de contenu multimédia indésirable.</span><span class="sxs-lookup"><span data-stu-id="ae10a-127">Evaluate how autoplay may affect users’ experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span> <span data-ttu-id="ae10a-128">Si la lecture automatique est une partie essentielle de votre utilisation, envisagez d’utiliser du contenu muet pour commencer et permettre à l’utilisateur d’activer son micro.</span><span class="sxs-lookup"><span data-stu-id="ae10a-128">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span> <span data-ttu-id="ae10a-129">Pour que le contenu soit coupé en lecture automatique, la source audio doit être soit explicitement muette soit ne pas être définie.</span><span class="sxs-lookup"><span data-stu-id="ae10a-129">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span> <span data-ttu-id="ae10a-130">Dans le cas contraire, l’élément n’est pas considéré comme muet.</span><span class="sxs-lookup"><span data-stu-id="ae10a-130">Otherwise the element will not be considered as muted.</span></span>

- <span data-ttu-id="ae10a-131">Sauf si absolument nécessaire, utilisez les contrôles de navigateur natifs pour la lecture de contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae10a-131">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span> <span data-ttu-id="ae10a-132">Cela garantira une connaissance homogène pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ae10a-132">This will ensure a consistent experience for users.</span></span> <span data-ttu-id="ae10a-133">Si vous créez des contrôles personnalisés à la place, assurez-vous que les contrôles multimédias sont toujours présents et que vos contrôles réagissent correctement à la suppression de lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="ae10a-133">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>

### <span data-ttu-id="ae10a-134">Délégation iframe</span><span class="sxs-lookup"><span data-stu-id="ae10a-134">Iframe delegation</span></span>

<span data-ttu-id="ae10a-135">La lecture automatique dans un `<iframe>` héritera de l’autorisation de lecture automatique de la page parent quelle que soit l’origine du contenu.</span><span class="sxs-lookup"><span data-stu-id="ae10a-135">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span> <span data-ttu-id="ae10a-136">Dans un scénario de playlist dans lequel chaque fichier multimédia est hébergé par un autre IFRAME, l’utilisateur ne doit lancer la lecture qu’une seule fois pour l’ensemble de la playlist.</span><span class="sxs-lookup"><span data-stu-id="ae10a-136">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>

### <span data-ttu-id="ae10a-137">Détection de l’autorisation de lecture automatique</span><span class="sxs-lookup"><span data-stu-id="ae10a-137">Detecting when autoplay is allowed</span></span>

<span data-ttu-id="ae10a-138">Vous pouvez ajuster vos contrôles de lecture pour afficher l’état correct lorsque la lecture automatique est bloquée en examinant la promesse renvoyée par la `play()` fonction sur l’élément multimédia:</span><span class="sxs-lookup"><span data-stu-id="ae10a-138">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>

```Javascript

var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}

```
