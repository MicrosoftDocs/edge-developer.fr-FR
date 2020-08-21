---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: Ce guide fournit une vue d’ensemble des normes et fonctionnalités de développement incluses dans Microsoft Edge.
title: Nouvelles fonctionnalités et API dans EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.openlocfilehash: a15888bc8c1314d61d436759e5d63be942174ea4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941936"
---
# <span data-ttu-id="4208a-104">Nouveautés de EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="4208a-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="4208a-105">Vous trouverez ci-dessous une liste des nouvelles fonctionnalités et mises à jour fournies dans [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) Web Platform, dans le cadre de la [mise à jour de Windows 10 pour les créateurs de la mise à jour de Windows 10](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) (10/2017, Build 16299 \).</span><span class="sxs-lookup"><span data-stu-id="4208a-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="4208a-106">Pour plus d’informations sur les builds d’aperçu Windows Insider spécifiques, voir le Guide de [Microsoft Edge changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) et [les nouveautés dans EdgeHTML](../whats-new.md).</span><span class="sxs-lookup"><span data-stu-id="4208a-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="4208a-107">Vous trouverez ci-dessous le lien permanent pour la liste des modifications suivante:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md) .</span><span class="sxs-lookup"><span data-stu-id="4208a-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <span data-ttu-id="4208a-108">Fonctionnalités nouvelles et mises à jour</span><span class="sxs-lookup"><span data-stu-id="4208a-108">New and updated features</span></span>  

### <span data-ttu-id="4208a-109">Disposition Grille CSS</span><span class="sxs-lookup"><span data-stu-id="4208a-109">CSS Grid Layout</span></span>  

<span data-ttu-id="4208a-110">Microsoft Edge prend désormais en charge l’implémentation non-prérésolue de la [disposition Grid CSS](https://www.w3.org/TR/css-grid-1).</span><span class="sxs-lookup"><span data-stu-id="4208a-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="4208a-111">La [disposition Grille](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) définit un système de disposition sur une grille en deux dimensions qui permet d’utiliser une fluidité de la disposition avec des valeurs flottantes ou des scripts.</span><span class="sxs-lookup"><span data-stu-id="4208a-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="4208a-112">L’exemple ci-dessous utilise la disposition Grid CSS pour créer la structure d’une page Web de base.</span><span class="sxs-lookup"><span data-stu-id="4208a-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="4208a-113">Disposition Grille CSS</span><span class="sxs-lookup"><span data-stu-id="4208a-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="4208a-114">Pour en savoir plus sur les feuilles de style CSS de stylet <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> </a> , voir MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="4208a-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <span data-ttu-id="4208a-115">Ajuster l’objet CSS et la position de l’objet</span><span class="sxs-lookup"><span data-stu-id="4208a-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="4208a-116">EdgeHTML 16 instaure une prise en charge des propriétés CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) et [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) .</span><span class="sxs-lookup"><span data-stu-id="4208a-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="4208a-117">Ces propriétés contrôlent la position et la taille du contenu remplacé au sein de la zone de contenu.</span><span class="sxs-lookup"><span data-stu-id="4208a-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <span data-ttu-id="4208a-118">Outils de développement</span><span class="sxs-lookup"><span data-stu-id="4208a-118">Developer Tools</span></span>  

<span data-ttu-id="4208a-119">Dans cette version, nous avons commencé un important effort de refactorisation de Microsoft Edge DevTools pour améliorer la fiabilité et les performances, ainsi que les nouvelles fonctionnalités que vous pouvez commencer à utiliser aujourd’hui sur les builds [Windows Insider](https://insider.windows.com) .</span><span class="sxs-lookup"><span data-stu-id="4208a-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="4208a-120">Consultez le [Guide Microsoft Edge devtools](../whats-new.md) pour en savoir plus sur les modifications.</span><span class="sxs-lookup"><span data-stu-id="4208a-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <span data-ttu-id="4208a-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="4208a-121">JavaScript</span></span>  

<span data-ttu-id="4208a-122">[EdgeHTMLx](https://blogs.windows.com/msedgedev/2017/10/31) , xxx xxxxxxx XX xxxxxxx XX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX, XXXXXXXXX, xxx xxxx xxxxxxxxx xxxxxxx xxxxxxxxx xxxxxxxxx xxxxxxx xxxxxxxxx `try` / `finally` .</span><span class="sxs-lookup"><span data-stu-id="4208a-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="4208a-123">De plus, les fonctionnalités d’abord prévisualisées dans EdgeHTML 15 sont désormais stables et activées par défaut:</span><span class="sxs-lookup"><span data-stu-id="4208a-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <span data-ttu-id="4208a-124">Nouvelles fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="4208a-124">New features</span></span>  

<span data-ttu-id="4208a-125">Activé par défaut</span><span class="sxs-lookup"><span data-stu-id="4208a-125">On by default</span></span>  

*   <span data-ttu-id="4208a-126">[Ensemble d’assemblys](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP ([démo](https://webassembly.org/demo))</span><span class="sxs-lookup"><span data-stu-id="4208a-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="4208a-127">Mémoire partagée et Atomic.</span><span class="sxs-lookup"><span data-stu-id="4208a-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <span data-ttu-id="4208a-128">API de demande de paiement</span><span class="sxs-lookup"><span data-stu-id="4208a-128">Payment Request API</span></span>  

<span data-ttu-id="4208a-129">L' [API de demande de paiement](../windows-integration/payment-request-api.md) est une norme ouverte et multiplateforme qui permet aux navigateurs d’agir en tant qu’intermédiaire entre commerçants, consommateurs et modes de paiement (par exemple, des cartes de crédit) stockées dans le Cloud.</span><span class="sxs-lookup"><span data-stu-id="4208a-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="4208a-130">L’API dans EdgeHTML 16 a été mise à jour pour correspondre à la dernière spécification de l' [API de demande de paiement](https://w3c.github.io/payment-request) du W3C.</span><span class="sxs-lookup"><span data-stu-id="4208a-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="4208a-131">Cela inclut les opérations suivantes:</span><span class="sxs-lookup"><span data-stu-id="4208a-131">This includes:</span></span>  

*   <span data-ttu-id="4208a-132">Prise en charge de la `canMakePayment()` méthode</span><span class="sxs-lookup"><span data-stu-id="4208a-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="4208a-133">Prise en charge de la `requestId` propriété</span><span class="sxs-lookup"><span data-stu-id="4208a-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="4208a-134">Prise en charge de la `id` propriété</span><span class="sxs-lookup"><span data-stu-id="4208a-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="4208a-135">La valeur par défaut du `complete()` paramètre de la méthode est `result` passée de «» à «Unknown».</span><span class="sxs-lookup"><span data-stu-id="4208a-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <span data-ttu-id="4208a-136">Worker du service</span><span class="sxs-lookup"><span data-stu-id="4208a-136">Service Workers</span></span>  

<span data-ttu-id="4208a-137">Les [travailleurs de service](https://www.w3.org/TR/service-workers-1) sont des scripts pilotés par des événements qui s’exécutent en arrière-plan d’une page Web.</span><span class="sxs-lookup"><span data-stu-id="4208a-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="4208a-138">Les travailleurs de service activent les fonctionnalités qui ne sont disponibles que pour les applications natives telles que l’interception et la gestion des demandes à partir du réseau, la gestion et la gestion de la synchronisation en arrière-plan et des notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="4208a-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="4208a-139">La prise en charge du travailleur de service est toujours en développement, mais vous pouvez tester votre PWA dans Microsoft Edge avec le support technique de votre service d’expérimentation en activant la fonctionnalité Worker Worker dans `about:flags` .</span><span class="sxs-lookup"><span data-stu-id="4208a-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <span data-ttu-id="4208a-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="4208a-140">WebVR</span></span>  

<span data-ttu-id="4208a-141">WebVR pour Microsoft Edge a ajouté la prise en charge des [contrôleurs de mouvement](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span><span class="sxs-lookup"><span data-stu-id="4208a-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="4208a-142">Ces contrôleurs disposent d’une position précise dans l’espace, ce qui permet d’interagir avec une fine graine avec des objets numériques dans la réalité virtuelle.</span><span class="sxs-lookup"><span data-stu-id="4208a-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Contrôleurs de mouvement" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="4208a-144">Contrôleurs de mouvement</span><span class="sxs-lookup"><span data-stu-id="4208a-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="4208a-145">WebVR a également été optimisé pour prendre en charge deux types d’expériences différents.</span><span class="sxs-lookup"><span data-stu-id="4208a-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="4208a-146">PCs-ordinateurs de bureau et ordinateurs portables **Windows mixte** avec graphiques intégrés.</span><span class="sxs-lookup"><span data-stu-id="4208a-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="4208a-147">Lorsque vous êtes branché sur ces appareils, nos casques immersives s’exécutent à 60 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="4208a-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="4208a-148">**Windows mixte Real Real PC** -ordinateurs de bureau et ordinateurs portables avec graphiques discrets.</span><span class="sxs-lookup"><span data-stu-id="4208a-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="4208a-149">Lorsque vous êtes branché sur ces appareils, nos casques immersives s’exécutent à 90 images par seconde.</span><span class="sxs-lookup"><span data-stu-id="4208a-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="4208a-150">Les deux installation prennent en charge les mêmes expériences de vidéo et de jeu.</span><span class="sxs-lookup"><span data-stu-id="4208a-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="4208a-151">Pour plus d’informations sur les prochaines mises à jour de Windows Mixed Reality, consultez le billet de blog consacré à la mise à jour des congés pour [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) .</span><span class="sxs-lookup"><span data-stu-id="4208a-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="4208a-152">Pour les guides et les démonstrations, voir le [Guide du développeur de WebVR](/microsoft-edge/webvr).</span><span class="sxs-lookup"><span data-stu-id="4208a-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="4208a-153">Dans la mesure où la spécification WebVR est toujours en développement, la mise en œuvre de Microsoft Edge peut changer plus tard.</span><span class="sxs-lookup"><span data-stu-id="4208a-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <span data-ttu-id="4208a-154">Nouvelles API dans EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="4208a-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="4208a-155">Voici la liste complète des nouvelles API dans EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="4208a-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="4208a-156">Ils sont répertoriés au format de `[interface name].[api name]` .</span><span class="sxs-lookup"><span data-stu-id="4208a-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="4208a-157">Bien que les API suivantes soient exposées dans le DOM, le comportement de bout en bout de certains peut toujours être en développement.</span><span class="sxs-lookup"><span data-stu-id="4208a-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="4208a-158">Reportez-vous à la rubrique  [État de plateforme Microsoft Edge](https://developer.microsoft.com/microsoft-edge/platform/status) pour le mot officiel sur la prise en charge des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="4208a-158">Refer to  [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="4208a-159">Nouvelles API dans EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="4208a-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="4208a-160">Voir le stylet <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> nouvelles API dans EdgeHTML 16 </a> par MSEdgeDev ( <a href='https://codepen.io/MSEdgeDev'> @MSEdgeDev </a> ) sur <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="4208a-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <span data-ttu-id="4208a-161">Versions précédentes de EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="4208a-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="4208a-162">EdgeHTML 12/Windows Build 10240 (7/2015)</span><span class="sxs-lookup"><span data-stu-id="4208a-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="4208a-163">EdgeHTML 13/Windows Build 10586 (11/2015)</span><span class="sxs-lookup"><span data-stu-id="4208a-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="4208a-164">EdgeHTML 14/Windows Build 14393 (8/2016)</span><span class="sxs-lookup"><span data-stu-id="4208a-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="4208a-165">EdgeHTML 15/Windows Build 15063 (4/2017)</span><span class="sxs-lookup"><span data-stu-id="4208a-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
