---
description: Ce guide fournit une vue d’ensemble des fonctionnalités et normes de développement incluses dans EdgeHTML 16.
title: Nouvelles fonctionnalités et API dans EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
keywords: edge, développement web, html, css, javascript, développeur
ms.openlocfilehash: e6ec2ec4a3152e9dfe73938784968fe3403d99cf
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399196"
---
# <a name="whats-new-in-edgehtml-16"></a><span data-ttu-id="28b4d-104">Nouveautés de EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="28b4d-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="28b4d-105">Voici une liste des fonctionnalités nouvelles et mises à jour livrées sur la plateforme web [EdgeHTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) dans le cadre de [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span><span class="sxs-lookup"><span data-stu-id="28b4d-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="28b4d-106">Pour plus d’informations sur les modifications apportées aux builds Windows Insider Preview spécifiques, voir le microsoft [Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) et les nouveautés dans [EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="28b4d-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="28b4d-107">Voici le lien de la liste de modifications suivante  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) :</span><span class="sxs-lookup"><span data-stu-id="28b4d-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <a name="new-and-updated-features"></a><span data-ttu-id="28b4d-108">Fonctionnalités nouvelles et mises à jour</span><span class="sxs-lookup"><span data-stu-id="28b4d-108">New and updated features</span></span>  

### <a name="css-grid-layout"></a><span data-ttu-id="28b4d-109">Disposition de la grille CSS</span><span class="sxs-lookup"><span data-stu-id="28b4d-109">CSS Grid Layout</span></span>  

<span data-ttu-id="28b4d-110">Microsoft Edge prend désormais en charge l’implémentation sans préfixe de la disposition de [grille CSS.](https://www.w3.org/TR/css-grid-1)</span><span class="sxs-lookup"><span data-stu-id="28b4d-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="28b4d-111">[La disposition en](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) grille définit un système de disposition en grille à deux dimensions qui offre plus de fluidité de disposition que possible avec le positionnement à l’aide de flottants ou de scripts.</span><span class="sxs-lookup"><span data-stu-id="28b4d-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="28b4d-112">L’exemple ci-dessous utilise la disposition de grille CSS pour créer la structure d’une page web de base.</span><span class="sxs-lookup"><span data-stu-id="28b4d-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="28b4d-113">Disposition de la grille CSS</span><span class="sxs-lookup"><span data-stu-id="28b4d-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="28b4d-114">Voir la disposition de la <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> grille CSS </a> stylet par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) sur </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="28b4d-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <a name="css-object-fit-and-object-position"></a><span data-ttu-id="28b4d-115">Ajustement de l’objet CSS et position de l’objet</span><span class="sxs-lookup"><span data-stu-id="28b4d-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="28b4d-116">EdgeHTML 16 introduit la prise en charge des propriétés CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) et [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="28b4d-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="28b4d-117">Ces propriétés contrôlent la position et la taille du contenu remplacé dans la zone de contenu.</span><span class="sxs-lookup"><span data-stu-id="28b4d-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <a name="developer-tools"></a><span data-ttu-id="28b4d-118">Outils de développement</span><span class="sxs-lookup"><span data-stu-id="28b4d-118">Developer Tools</span></span>  

<span data-ttu-id="28b4d-119">Cette version a démarré un effort majeur de refactoriser Microsoft Edge DevTools pour améliorer la robustesse et les performances, et nous avons également ajouté de nouvelles fonctionnalités que vous pouvez commencer à utiliser aujourd’hui sur les builds [Windows Insider.](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="28b4d-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="28b4d-120">Consultez le [guide Microsoft Edge DevTools pour](../whats-new.md) en savoir plus sur ce qui a changé !</span><span class="sxs-lookup"><span data-stu-id="28b4d-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <a name="javascript"></a><span data-ttu-id="28b4d-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="28b4d-121">JavaScript</span></span>  

<span data-ttu-id="28b4d-122">[EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/31) s’appuie sur les optimisations des performances JavaScript des versions précédentes en développez la capacité du moteur DeCaler à différer/différer des fonctions, à utiliser des caches en ligne polymorphes et à optimiser les fonctions avec des `try` / `finally` blocs.</span><span class="sxs-lookup"><span data-stu-id="28b4d-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="28b4d-123">En outre, les fonctionnalités d’abord prévisualisations dans EdgeHTML 15 sont désormais stables et activées par défaut :</span><span class="sxs-lookup"><span data-stu-id="28b4d-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <a name="new-features"></a><span data-ttu-id="28b4d-124">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="28b4d-124">New features</span></span>  

<span data-ttu-id="28b4d-125">Activé par défaut</span><span class="sxs-lookup"><span data-stu-id="28b4d-125">On by default</span></span>  

*   <span data-ttu-id="28b4d-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="28b4d-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="28b4d-127">Mémoire partagée et atomiques</span><span class="sxs-lookup"><span data-stu-id="28b4d-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <a name="payment-request-api"></a><span data-ttu-id="28b4d-128">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="28b4d-128">Payment Request API</span></span>  

<span data-ttu-id="28b4d-129">[L’API](../windows-integration/payment-request-api.md) de demande de paiement est une norme ouverte inter-navigateur qui permet aux navigateurs d’agir en tant qu’intermédiaires entre les marchands, les consommateurs et les modes de paiement \(tels que les cartes de crédit\) que les consommateurs ont stockés dans le cloud.</span><span class="sxs-lookup"><span data-stu-id="28b4d-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="28b4d-130">L’API dans EdgeHTML 16 a été mise à jour pour correspondre à la dernière spécification de [l’API](https://w3c.github.io/payment-request) de demande de paiement W3C.</span><span class="sxs-lookup"><span data-stu-id="28b4d-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="28b4d-131">Cela inclut les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="28b4d-131">This includes:</span></span>  

*   <span data-ttu-id="28b4d-132">Prise en charge de la `canMakePayment()` méthode</span><span class="sxs-lookup"><span data-stu-id="28b4d-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="28b4d-133">Prise en charge de la `requestId` propriété</span><span class="sxs-lookup"><span data-stu-id="28b4d-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="28b4d-134">Prise en charge de la `id` propriété</span><span class="sxs-lookup"><span data-stu-id="28b4d-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="28b4d-135">La valeur par défaut du paramètre de la méthode est modifiée `complete()` de « » à « unknown `result` »</span><span class="sxs-lookup"><span data-stu-id="28b4d-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <a name="service-workers"></a><span data-ttu-id="28b4d-136">Worker du service</span><span class="sxs-lookup"><span data-stu-id="28b4d-136">Service Workers</span></span>  

<span data-ttu-id="28b4d-137">[Les travailleurs de](https://www.w3.org/TR/service-workers-1) service sont des scripts pilotés par des événements qui s’exécutent en arrière-plan d’une page web.</span><span class="sxs-lookup"><span data-stu-id="28b4d-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="28b4d-138">Les employés de service activent des fonctionnalités auparavant disponibles uniquement avec les applications natives, telles que l’interception et la gestion des demandes en provenance du réseau, la gestion et la gestion de la synchronisation en arrière-plan, du stockage local et des notifications Push.</span><span class="sxs-lookup"><span data-stu-id="28b4d-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="28b4d-139">La prise en charge du service de travail est toujours en cours de développement, mais vous pouvez tester votre PWA dans Microsoft Edge avec notre support de travail de service expérimental en activant la fonctionnalité de travail de service dans `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="28b4d-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <a name="webvr"></a><span data-ttu-id="28b4d-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="28b4d-140">WebVR</span></span>  

<span data-ttu-id="28b4d-141">WebVR pour Microsoft Edge a ajouté la prise en charge des [contrôleurs de mouvement.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)</span><span class="sxs-lookup"><span data-stu-id="28b4d-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="28b4d-142">Ces contrôleurs ont une position précise dans l’espace, ce qui permet une interaction précise avec les objets numériques dans la réalité virtuelle.</span><span class="sxs-lookup"><span data-stu-id="28b4d-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Contrôleurs de mouvement" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="28b4d-144">Contrôleurs de mouvement</span><span class="sxs-lookup"><span data-stu-id="28b4d-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="28b4d-145">WebVR a également été optimisé pour prendre en charge deux types d’expériences différents.</span><span class="sxs-lookup"><span data-stu-id="28b4d-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="28b4d-146">**PC Windows Mixed Reality :** ordinateurs de bureau et ordinateurs portables avec des graphiques intégrés.</span><span class="sxs-lookup"><span data-stu-id="28b4d-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="28b4d-147">Lorsqu’ils sont branchés sur ces appareils, nos casques immersifs s’exécutent à 60 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="28b4d-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="28b4d-148">**PC Windows Mixed Reality Ultra :** ordinateurs de bureau et ordinateurs portables avec des graphiques discrets.</span><span class="sxs-lookup"><span data-stu-id="28b4d-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="28b4d-149">Lorsqu’ils sont branchés sur ces appareils, nos casques immersifs s’exécutent à 90 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="28b4d-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="28b4d-150">Les deux configurations ront les mêmes expériences immersives vidéo et de jeu.</span><span class="sxs-lookup"><span data-stu-id="28b4d-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="28b4d-151">Pour plus d’informations sur les mises à jour Windows Mixed Reality à venir, consultez le billet de blog sur les mises à jour de [congés Windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)</span><span class="sxs-lookup"><span data-stu-id="28b4d-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="28b4d-152">Pour obtenir des guides et des démonstrations, voir le Guide du développeur [WebVR.](/microsoft-edge/webvr)</span><span class="sxs-lookup"><span data-stu-id="28b4d-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="28b4d-153">Étant donné que les spécifications WebVR sont toujours en cours de développement, l’implémentation de Microsoft Edge peut changer ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="28b4d-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <a name="new-apis-in-edgehtml-16"></a><span data-ttu-id="28b4d-154">Nouvelles API dans EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="28b4d-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="28b4d-155">Voici la liste complète des nouvelles API dans EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="28b4d-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="28b4d-156">Ils sont répertoriés au format `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="28b4d-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="28b4d-157">Bien que les API suivantes soient exposées dans le DOM, le comportement de bout en bout de certaines d’entre elles est peut-être encore en cours de développement.</span><span class="sxs-lookup"><span data-stu-id="28b4d-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="28b4d-158">Reportez-vous [à l’état de la](https://developer.microsoft.com/microsoft-edge/platform/status) plateforme Microsoft Edge pour le mot officiel sur la prise en charge des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="28b4d-158">Refer to [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="28b4d-159">Nouvelles API dans EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="28b4d-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="28b4d-160">Voir les nouvelles API stylet dans <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> EdgeHTML 16 </a> par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev ) sur </a> <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="28b4d-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <a name="previous-edgehtml-releases"></a><span data-ttu-id="28b4d-161">Versions EdgeHTML précédentes</span><span class="sxs-lookup"><span data-stu-id="28b4d-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="28b4d-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="28b4d-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="28b4d-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="28b4d-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="28b4d-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="28b4d-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="28b4d-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="28b4d-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
