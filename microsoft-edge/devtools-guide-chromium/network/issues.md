---
title: Guide de problèmes réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 018a6ef89242d55cefaa974641be456f4501c557
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611804"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="74f95-103">Guide de problèmes réseau</span><span class="sxs-lookup"><span data-stu-id="74f95-103">Network Issues Guide</span></span>   




<span data-ttu-id="74f95-104">Ce guide vous montre comment détecter les problèmes de réseau ou les opportunités d’optimisation dans le volet réseau de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="74f95-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="74f95-105">Pour [plus d’informations][NetworkPerformance] sur les concepts de base du réseau, voir découvrir le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="74f95-105">See [Get Started][NetworkPerformance] to learn the basics of the Network panel.</span></span>  

## <span data-ttu-id="74f95-106">Demandes mises en file d’attente ou bloquées</span><span class="sxs-lookup"><span data-stu-id="74f95-106">Queued or stalled requests</span></span>   

### <span data-ttu-id="74f95-107">Symptômes</span><span class="sxs-lookup"><span data-stu-id="74f95-107">Symptoms</span></span>  

<span data-ttu-id="74f95-108">Six demandes sont en train de télécharger simultanément.</span><span class="sxs-lookup"><span data-stu-id="74f95-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="74f95-109">Après cela, une série de demandes est mise en file d’attente ou bloquée.</span><span class="sxs-lookup"><span data-stu-id="74f95-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="74f95-110">Après l’exécution de l’une des six premières demandes, une des requêtes de la file d’attente démarre.</span><span class="sxs-lookup"><span data-stu-id="74f95-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="74f95-111">Dans la [figure 1](#figure-1) **, les six** premières demandes de l' `edge-iconx1024.msft.png` actif commencent simultanément.</span><span class="sxs-lookup"><span data-stu-id="74f95-111">In the **Waterfall** in [Figure 1](#figure-1), the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="74f95-112">Les demandes ultérieures sont bloquées jusqu’à ce que l’une des six nouvelles préfinissements.</span><span class="sxs-lookup"><span data-stu-id="74f95-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

> ##### <span data-ttu-id="74f95-113">Figure1</span><span class="sxs-lookup"><span data-stu-id="74f95-113">Figure 1</span></span>  
> <span data-ttu-id="74f95-114">Exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="74f95-114">An example of a queued or stalled series in the Network panel</span></span>  
> ![Exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau][ImageStalled]  

### <span data-ttu-id="74f95-116">Causes</span><span class="sxs-lookup"><span data-stu-id="74f95-116">Causes</span></span>  

<span data-ttu-id="74f95-117">Il y a trop de demandes sur un domaine unique.</span><span class="sxs-lookup"><span data-stu-id="74f95-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="74f95-118">Sur les connexions HTTP/1.0 ou HTTP/1.1, Microsoft Edge autorise un maximum de six connexions TCP simultanées par hôte.</span><span class="sxs-lookup"><span data-stu-id="74f95-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

### <span data-ttu-id="74f95-119">Correctifs</span><span class="sxs-lookup"><span data-stu-id="74f95-119">Fixes</span></span>  

*   <span data-ttu-id="74f95-120">Implémentez Domain sharding si vous devez utiliser HTTP/1.0 ou HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="74f95-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="74f95-121">Utiliser HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="74f95-121">Use HTTP/2.</span></span>  <span data-ttu-id="74f95-122">N’utilisez pas le domaine sharding avec HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="74f95-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="74f95-123">Supprimez ou différez les demandes inutiles de manière à ce que les demandes critiques soient téléchargées plus tôt.</span><span class="sxs-lookup"><span data-stu-id="74f95-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  

## <span data-ttu-id="74f95-124">Temps lent vers le premier octet (TTFB)</span><span class="sxs-lookup"><span data-stu-id="74f95-124">Slow Time To First Byte (TTFB)</span></span>   

### <span data-ttu-id="74f95-125">Symptômes</span><span class="sxs-lookup"><span data-stu-id="74f95-125">Symptoms</span></span>  

<span data-ttu-id="74f95-126">Une requête passe un certain temps en attente de réception du premier octet du serveur.</span><span class="sxs-lookup"><span data-stu-id="74f95-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="74f95-127">Dans la [figure 2](#figure-2), la barre verte longue de la **cascade** indique que la demande est en attente pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="74f95-127">In [Figure 2](#figure-2), the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="74f95-128">Il a été simulé à l’aide d’un profil afin de limiter la vitesse du réseau et d’ajouter un délai.</span><span class="sxs-lookup"><span data-stu-id="74f95-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

> ##### <span data-ttu-id="74f95-129">Figure 2</span><span class="sxs-lookup"><span data-stu-id="74f95-129">Figure 2</span></span>  
> <span data-ttu-id="74f95-130">Exemple d’une requête avec un délai de première octet lent</span><span class="sxs-lookup"><span data-stu-id="74f95-130">An example of a request with a slow Time To First Byte</span></span>  
> ![Exemple d’une requête avec un délai de première octet lent][ImageSlowTimeToFirstByte]  

### <span data-ttu-id="74f95-132">Causes</span><span class="sxs-lookup"><span data-stu-id="74f95-132">Causes</span></span>  

*   <span data-ttu-id="74f95-133">La connexion entre le client et le serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="74f95-133">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="74f95-134">La réponse du serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="74f95-134">The server is slow to respond.</span></span>  <span data-ttu-id="74f95-135">Hébergez le serveur localement pour déterminer s’il s’agit d’une connexion ou d’un serveur lent.</span><span class="sxs-lookup"><span data-stu-id="74f95-135">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="74f95-136">Si vous obtenez encore un temps lente pour le premier octet \ (TTFB \) lors de l’accès à un serveur local, le serveur est lent.</span><span class="sxs-lookup"><span data-stu-id="74f95-136">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  

### <span data-ttu-id="74f95-137">Correctifs</span><span class="sxs-lookup"><span data-stu-id="74f95-137">Fixes</span></span>  

*   <span data-ttu-id="74f95-138">Si la connexion est lente, envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="74f95-138">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="74f95-139">Si le serveur est lent, envisagez d’optimiser les requêtes de base de données, de mettre en cache ou de modifier votre configuration serveur.</span><span class="sxs-lookup"><span data-stu-id="74f95-139">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  

## <span data-ttu-id="74f95-140">Téléchargement de contenu lent</span><span class="sxs-lookup"><span data-stu-id="74f95-140">Slow content download</span></span>   

### <span data-ttu-id="74f95-141">Symptômes</span><span class="sxs-lookup"><span data-stu-id="74f95-141">Symptoms</span></span>  

<span data-ttu-id="74f95-142">Le téléchargement d’une requête prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="74f95-142">A request takes a long time to download.</span></span>  

<span data-ttu-id="74f95-143">Dans la [figure 3](#figure-3), une barre bleue longue **en regard du** fichier PNG signifie que le téléchargement a duré longtemps.</span><span class="sxs-lookup"><span data-stu-id="74f95-143">In [Figure 3](#figure-3), the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

> ##### <span data-ttu-id="74f95-144">Figure3</span><span class="sxs-lookup"><span data-stu-id="74f95-144">Figure 3</span></span>  
> <span data-ttu-id="74f95-145">Exemple d’une requête prenant du temps à télécharger</span><span class="sxs-lookup"><span data-stu-id="74f95-145">An example of a request that takes a long time to download</span></span>  
> ![Exemple d’une requête prenant du temps à télécharger][ImageSlowContentDownload]  

### <span data-ttu-id="74f95-147">Causes</span><span class="sxs-lookup"><span data-stu-id="74f95-147">Causes</span></span>  

*   <span data-ttu-id="74f95-148">La connexion entre le client et le serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="74f95-148">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="74f95-149">Un grand nombre de contenus est en cours de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="74f95-149">A lot of content is being downloaded.</span></span>  

### <span data-ttu-id="74f95-150">Correctifs</span><span class="sxs-lookup"><span data-stu-id="74f95-150">Fixes</span></span>  

*   <span data-ttu-id="74f95-151">Envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="74f95-151">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="74f95-152">Envoyez moins d’octets en optimisant vos demandes.</span><span class="sxs-lookup"><span data-stu-id="74f95-152">Send fewer bytes by optimizing your requests.</span></span>  

## <span data-ttu-id="74f95-153">Compétences de collaboration</span><span class="sxs-lookup"><span data-stu-id="74f95-153">Contribute knowledge</span></span>  

<span data-ttu-id="74f95-154">Vous rencontrez un problème réseau qui doit être ajouté à ce guide?</span><span class="sxs-lookup"><span data-stu-id="74f95-154">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="74f95-155">Envoyez un tweet à [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="74f95-155">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="74f95-156">**Send Feedback** ![ ][ImageSendFeedbackIcon] Pour envoyer des commentaires ou des demandes de fonctionnalité, sélectionnez Envoyer des commentaires dans le devtools ou appuyez sur `Alt` + `Shift` + `I` \ (Windows \) ou `Option` + `Shift` + `I` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="74f95-156">Select **Send Feedback** ![Send Feedback][ImageSendFeedbackIcon] in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="74f95-157">[Ouvrez un problème][WebFundamentalsIssue] dans le référentiel Samples docs.</span><span class="sxs-lookup"><span data-stu-id="74f95-157">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  

<!--   -->  



<!-- image links -->  

[ImageSendFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/smile-icon.msft.png  

[ImageStalled]: /microsoft-edge/devtools-guide-chromium/media/network-network-disabled-cache-resources-queue.msft.png "Figure 1: exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau"  
[ImageSlowTimeToFirstByte]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-using-dial-up-profile.msft.png "Figure 2: exemple de requête avec un délai de première octet lent"  
[ImageSlowContentDownload]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-edge-devtools.msft.png "Figure 3: exemple de requête dont le téléchargement prend du temps"  

<!-- links -->  

[NetworkPerformance]: /microsoft-edge/devtools-guide-chromium/network/index "Examiner l’activité réseau dans Microsoft Edge DevTools"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nouveau problème-MicrosoftDocs/Edge-développeur"  

> [!NOTE]
> <span data-ttu-id="74f95-163">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="74f95-163">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="74f95-164">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/issues) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Jonathan Garbee][JonathanGarbee] \ (Google Developer expertise pour Web Technology \).</span><span class="sxs-lookup"><span data-stu-id="74f95-164">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="74f95-166">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="74f95-166">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
