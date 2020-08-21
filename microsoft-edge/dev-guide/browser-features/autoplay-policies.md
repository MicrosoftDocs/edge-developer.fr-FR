---
description: Garantir le fonctionnement du contenu multimédia sur votre site
title: Stratégies de lecture automatique-Guide de développement
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: bordure, média, vidéo, audio, lecture automatique
ms.custom: seodec18
ms.openlocfilehash: 39c9bd8e9921167dfc3a9ab1a4cc12b2157f0f6f
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942059"
---
# <span data-ttu-id="9bca6-104">Stratégies de lecture automatique</span><span class="sxs-lookup"><span data-stu-id="9bca6-104">Autoplay Policies</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="9bca6-105">Microsoft Edge offre aux utilisateurs la possibilité de personnaliser leurs préférences de navigation sur les sites Web qui entourent le son par lecture automatique afin de réduire le nombre de distractions sur le Web et de économiser la bande passante.</span><span class="sxs-lookup"><span data-stu-id="9bca6-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="9bca6-106">Par ailleurs, Microsoft Edge supprime automatiquement la lecture automatique de contenus multimédias dans les onglets d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="9bca6-106">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="9bca6-107">Les utilisateurs peuvent personnaliser le comportement du contenu multimédia avec les contrôles de lecture automatique [globaux](#global-media-autoplay-settings) et [par site](#per-site-media-autoplay-settings) , qui fournissent les options suivantes:</span><span class="sxs-lookup"><span data-stu-id="9bca6-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>  

*   `Allow`  <span data-ttu-id="9bca6-108">Par défaut, il continue de lire les vidéos lorsqu’un onglet est d’abord affiché au premier plan, en fonction du site discrétionnaire.</span><span class="sxs-lookup"><span data-stu-id="9bca6-108">The default and will continue to play videos when a tab is first viewed in the foreground, at the site's discretion.</span></span>  

*   `Limit`  <span data-ttu-id="9bca6-109">Restreint la lecture automatique pour ne fonctionner que lorsque les vidéos sont en mode muet, afin que les utilisateurs ne soient jamais surpris par le son.</span><span class="sxs-lookup"><span data-stu-id="9bca6-109">Restricts autoplay to only work when videos are muted, so users are never surprised by sound.</span></span>  <span data-ttu-id="9bca6-110">Lorsque l’utilisateur clique n’importe où sur la page, la lecture automatique est réactivée et continue d’être autorisée dans ce domaine sous cet onglet.</span><span class="sxs-lookup"><span data-stu-id="9bca6-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>  

*   `Block`  <span data-ttu-id="9bca6-111">Interdisez sautoplay sur tous les sites tant que les utilisateurs n’interagissent pas directement avec le contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="9bca6-111">Prevent sautoplay on all sites until users directly interact with the media content.</span></span>  

## <span data-ttu-id="9bca6-112">Paramètres généraux de lecture multimédias</span><span class="sxs-lookup"><span data-stu-id="9bca6-112">Global media autoplay settings</span></span>  

<span data-ttu-id="9bca6-113">Les utilisateurs peuvent contrôler le comportement de lecture automatique par défaut pour tous les sites sous **Paramètres avancés**de  >  **lecture automatique de médias**.</span><span class="sxs-lookup"><span data-stu-id="9bca6-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Paramètres généraux de lecture multimédias" lightbox="../media/autoplay_global.png":::
   <span data-ttu-id="9bca6-115">Paramètres généraux de lecture multimédias</span><span class="sxs-lookup"><span data-stu-id="9bca6-115">Global media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="9bca6-116">Paramètres de lecture automatique de média par site</span><span class="sxs-lookup"><span data-stu-id="9bca6-116">Per-site media autoplay settings</span></span>  

<span data-ttu-id="9bca6-117">Les utilisateurs peuvent contrôler le comportement de la lecture automatique sur une base par site sous la section **autorisations de site Web** du volet informations sur le site Web.</span><span class="sxs-lookup"><span data-stu-id="9bca6-117">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span>  <span data-ttu-id="9bca6-118">Ce paramètre est disponible en cliquant sur l’icône d’information ou sur l’icône de verrouillage située sur le côté gauche de la barre d’adresse, puis en cliquant sur **paramètres de lecture automatique de média** pour commencer.</span><span class="sxs-lookup"><span data-stu-id="9bca6-118">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on **Media autoplay settings** to get started.</span></span>  

<span data-ttu-id="9bca6-119">Les paramètres par site remplacent le paramètre global.</span><span class="sxs-lookup"><span data-stu-id="9bca6-119">Per-site settings override the global setting.</span></span>  <span data-ttu-id="9bca6-120">Par exemple, si le paramètre global est défini pour un utilisateur et qu’il `Allow` change un paramètre par site `Block` , la lecture automatique est bloquée pour ce site.</span><span class="sxs-lookup"><span data-stu-id="9bca6-120">For example, if a user has their global setting set to `Allow` but changes a per-site setting to `Block`, autoplay will be blocked for that site.</span></span>  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Paramètres de lecture automatique de média par site" lightbox="../media/autoplay_per-site.png":::
   <span data-ttu-id="9bca6-122">Paramètres de lecture automatique de média par site</span><span class="sxs-lookup"><span data-stu-id="9bca6-122">Per-site media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="9bca6-123">Meilleures pratiques pour les développeurs Web</span><span class="sxs-lookup"><span data-stu-id="9bca6-123">Best Practices for Web Developers</span></span>  

<span data-ttu-id="9bca6-124">Pour garantir une bonne utilisation de l’utilisateur avec le contenu multimédia hébergé sur votre site, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="9bca6-124">Here's how to ensure a good user experience with media hosted on your site:</span></span>  

*   <span data-ttu-id="9bca6-125">Supposez que l’utilisation d’un élément multimédia nécessite un mouvement utilisateur pour démarrer la lecture \ (car les utilisateurs peuvent bloquer la lecture automatique à tout moment \) et planifier en conséquence.</span><span class="sxs-lookup"><span data-stu-id="9bca6-125">Assume each use of a media element wil require a user gesture to start the playback \(as users can block autoplay at any point in time\) and plan accordingly.</span></span>  <span data-ttu-id="9bca6-126">Les stratégies de lecture globale et globales par site s’appliquent à `<audio>` l’ensemble et aux `<video>` éléments, quelle que soit la façon dont ils sont utilisés sur votre site.</span><span class="sxs-lookup"><span data-stu-id="9bca6-126">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>  

*   <span data-ttu-id="9bca6-127">Assurez-vous que les contrôles multimédias sont toujours présents sur les éléments multimédias et les contenus publicitaires.</span><span class="sxs-lookup"><span data-stu-id="9bca6-127">Ensure that media controls are always present on both site media and ad content.</span></span>  <span data-ttu-id="9bca6-128">Cela permettra aux utilisateurs de redémarrer la lecture si la lecture automatique est bloquée sur la page.</span><span class="sxs-lookup"><span data-stu-id="9bca6-128">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>  

*   <span data-ttu-id="9bca6-129">Évaluez la façon dont la lecture automatique peut affecter l’utilisation des utilisateurs sur votre site Web et envisager d’utiliser la lecture automatique de manière à limiter la lecture de contenu multimédia indésirable.</span><span class="sxs-lookup"><span data-stu-id="9bca6-129">Evaluate how autoplay may affect users' experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span>  <span data-ttu-id="9bca6-130">Si la lecture automatique est une partie essentielle de votre utilisation, envisagez d’utiliser du contenu muet pour commencer et permettre à l’utilisateur d’activer son micro.</span><span class="sxs-lookup"><span data-stu-id="9bca6-130">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span>  <span data-ttu-id="9bca6-131">Pour que le contenu soit coupé en lecture automatique, la source audio doit être soit explicitement muette soit ne pas être définie.</span><span class="sxs-lookup"><span data-stu-id="9bca6-131">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span>  <span data-ttu-id="9bca6-132">Dans le cas contraire, l’élément n’est pas considéré comme muet.</span><span class="sxs-lookup"><span data-stu-id="9bca6-132">Otherwise the element will not be considered as muted.</span></span>  

*   <span data-ttu-id="9bca6-133">Sauf si absolument nécessaire, utilisez les contrôles de navigateur natifs pour la lecture de contenu multimédia.</span><span class="sxs-lookup"><span data-stu-id="9bca6-133">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span>  <span data-ttu-id="9bca6-134">Cela garantira une connaissance homogène pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9bca6-134">This will ensure a consistent experience for users.</span></span>  <span data-ttu-id="9bca6-135">Si vous créez des contrôles personnalisés à la place, assurez-vous que les contrôles multimédias sont toujours présents et que vos contrôles réagissent correctement à la suppression de lecture automatique.</span><span class="sxs-lookup"><span data-stu-id="9bca6-135">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>  

### <span data-ttu-id="9bca6-136">Délégation iframe</span><span class="sxs-lookup"><span data-stu-id="9bca6-136">Iframe delegation</span></span>  

<span data-ttu-id="9bca6-137">La lecture automatique dans un `<iframe>` héritera de l’autorisation de lecture automatique de la page parent quelle que soit l’origine du contenu.</span><span class="sxs-lookup"><span data-stu-id="9bca6-137">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span>  <span data-ttu-id="9bca6-138">Dans un scénario de playlist dans lequel chaque fichier multimédia est hébergé par un autre IFRAME, l’utilisateur ne doit lancer la lecture qu’une seule fois pour l’ensemble de la playlist.</span><span class="sxs-lookup"><span data-stu-id="9bca6-138">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>  

### <span data-ttu-id="9bca6-139">Détection de l’autorisation de lecture automatique</span><span class="sxs-lookup"><span data-stu-id="9bca6-139">Detecting when autoplay is allowed</span></span>  

<span data-ttu-id="9bca6-140">Vous pouvez ajuster vos contrôles de lecture pour afficher l’état correct lorsque la lecture automatique est bloquée en examinant la promesse renvoyée par la `play()` fonction sur l’élément multimédia:</span><span class="sxs-lookup"><span data-stu-id="9bca6-140">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>  

```javascript
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
