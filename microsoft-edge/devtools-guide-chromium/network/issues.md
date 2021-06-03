---
description: Découvrez comment détecter les problèmes réseau dans le panneau Réseau de Microsoft Edge DevTools.
title: Guide des problèmes de réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c99f43872abe04800880c63ee4126bfcdd633edb
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564979"
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
# <a name="network-issues-guide"></a><span data-ttu-id="a56eb-104">Guide des problèmes de réseau</span><span class="sxs-lookup"><span data-stu-id="a56eb-104">Network issues guide</span></span>  

<span data-ttu-id="a56eb-105">Ce guide vous montre comment détecter les problèmes réseau ou les opportunités d’optimisation dans le panneau Réseau de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="a56eb-105">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="a56eb-106">Pour découvrir les principes de base de **l’outil** Réseau, accédez [à Prise en main][NetworkPerformance].</span><span class="sxs-lookup"><span data-stu-id="a56eb-106">To learn the basics of the **Network** tool, navigate to [Get Started][NetworkPerformance].</span></span>  

## <a name="queued-or-stalled-requests"></a><span data-ttu-id="a56eb-107">Demandes en file d’attente ou bloquées</span><span class="sxs-lookup"><span data-stu-id="a56eb-107">Queued or stalled requests</span></span>  

**<span data-ttu-id="a56eb-108">Symptômes</span><span class="sxs-lookup"><span data-stu-id="a56eb-108">Symptoms</span></span>**  

<span data-ttu-id="a56eb-109">Six demandes sont téléchargées simultanément.</span><span class="sxs-lookup"><span data-stu-id="a56eb-109">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="a56eb-110">Après cela, une série de demandes sont en file d’attente ou bloquées.</span><span class="sxs-lookup"><span data-stu-id="a56eb-110">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="a56eb-111">Une fois l’une des six premières demandes se termine, l’une des demandes de la file d’attente démarre.</span><span class="sxs-lookup"><span data-stu-id="a56eb-111">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="a56eb-112">Dans la **cascade de** la figure suivante, les six premières demandes de ressources démarrent `edge-iconx1024.msft.png` simultanément.</span><span class="sxs-lookup"><span data-stu-id="a56eb-112">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="a56eb-113">Les demandes suivantes sont bloquées jusqu’à ce que l’une des six premières se termine.</span><span class="sxs-lookup"><span data-stu-id="a56eb-113">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Exemple de série en file d’attente ou bloquée dans le panneau Réseau" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="a56eb-115">Exemple d’une série en file d’attente ou bloquée dans **l’outil** Réseau</span><span class="sxs-lookup"><span data-stu-id="a56eb-115">An example of a queued or stalled series in the **Network** tool</span></span>  
:::image-end:::  

**<span data-ttu-id="a56eb-116">Causes</span><span class="sxs-lookup"><span data-stu-id="a56eb-116">Causes</span></span>**  

<span data-ttu-id="a56eb-117">Trop de demandes sont faites sur un seul domaine.</span><span class="sxs-lookup"><span data-stu-id="a56eb-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="a56eb-118">Sur les connexions HTTP/1.0 ou HTTP/1.1, Microsoft Edge autorise un maximum de six connexions TCP simultanées par hôte.</span><span class="sxs-lookup"><span data-stu-id="a56eb-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="a56eb-119">Correctifs</span><span class="sxs-lookup"><span data-stu-id="a56eb-119">Fixes</span></span>**  

*   <span data-ttu-id="a56eb-120">Implémentez le partitionnage de domaine si vous devez utiliser HTTP/1.0 ou HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="a56eb-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="a56eb-121">Utilisez HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="a56eb-121">Use HTTP/2.</span></span>  <span data-ttu-id="a56eb-122">N’utilisez pas le partitionnage de domaine avec HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="a56eb-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="a56eb-123">Supprimer ou différer les demandes inutiles afin que les demandes critiques se téléchargent plus tôt.</span><span class="sxs-lookup"><span data-stu-id="a56eb-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <a name="slow-time-to-first-byte-ttfb"></a><span data-ttu-id="a56eb-124">Slow Time To First Byte (TTFB)</span><span class="sxs-lookup"><span data-stu-id="a56eb-124">Slow Time To First Byte (TTFB)</span></span>  

**<span data-ttu-id="a56eb-125">Symptômes</span><span class="sxs-lookup"><span data-stu-id="a56eb-125">Symptoms</span></span>**  

<span data-ttu-id="a56eb-126">Une demande passe beaucoup de temps à attendre de recevoir le premier byte du serveur.</span><span class="sxs-lookup"><span data-stu-id="a56eb-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="a56eb-127">Dans la figure suivante, la barre longue et verte de la **cascade** indique que la demande attendait longtemps.</span><span class="sxs-lookup"><span data-stu-id="a56eb-127">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="a56eb-128">Cela a été simulé à l’aide d’un profil pour limiter la vitesse du réseau et ajouter un délai.</span><span class="sxs-lookup"><span data-stu-id="a56eb-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Exemple d’une demande dont l’heure est lente jusqu’au premier sur deux byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="a56eb-130">Exemple d’une demande dont l’heure est lente jusqu’au premier sur deux byte</span><span class="sxs-lookup"><span data-stu-id="a56eb-130">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="a56eb-131">Causes</span><span class="sxs-lookup"><span data-stu-id="a56eb-131">Causes</span></span>**  

*   <span data-ttu-id="a56eb-132">La connexion entre le client et le serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="a56eb-132">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="a56eb-133">Le serveur est lent à répondre.</span><span class="sxs-lookup"><span data-stu-id="a56eb-133">The server is slow to respond.</span></span>  <span data-ttu-id="a56eb-134">Hébergez le serveur localement pour déterminer s’il s’agit de la connexion ou du serveur lent.</span><span class="sxs-lookup"><span data-stu-id="a56eb-134">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="a56eb-135">Si vous obtenez toujours une durée lente jusqu’au premier byte \(TTFB\) lors de l’accès à un serveur local, le serveur est lent.</span><span class="sxs-lookup"><span data-stu-id="a56eb-135">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="a56eb-136">Correctifs</span><span class="sxs-lookup"><span data-stu-id="a56eb-136">Fixes</span></span>**  

*   <span data-ttu-id="a56eb-137">Si la connexion est lente, envisagez d’héberger votre contenu sur un CDN ou de modifier les fournisseurs d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="a56eb-137">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="a56eb-138">Si le serveur est lent, envisagez d’optimiser les requêtes de base de données, d’implémenter un cache ou de modifier la configuration de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="a56eb-138">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <a name="slow-content-download"></a><span data-ttu-id="a56eb-139">Téléchargement de contenu lent</span><span class="sxs-lookup"><span data-stu-id="a56eb-139">Slow content download</span></span>  

**<span data-ttu-id="a56eb-140">Symptômes</span><span class="sxs-lookup"><span data-stu-id="a56eb-140">Symptoms</span></span>**  

<span data-ttu-id="a56eb-141">Le téléchargement d’une demande prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="a56eb-141">A request takes a long time to download.</span></span>  

<span data-ttu-id="a56eb-142">Dans la figure suivante, la longue \*\*\*\* barre bleue dans la cascade en face du png signifie que le téléchargement a pris beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="a56eb-142">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Exemple de demande longue à télécharger" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="a56eb-144">Exemple de demande longue à télécharger</span><span class="sxs-lookup"><span data-stu-id="a56eb-144">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="a56eb-145">Causes</span><span class="sxs-lookup"><span data-stu-id="a56eb-145">Causes</span></span>**  

*   <span data-ttu-id="a56eb-146">La connexion entre le client et le serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="a56eb-146">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="a56eb-147">Une grande partie du contenu est en cours de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="a56eb-147">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="a56eb-148">Correctifs</span><span class="sxs-lookup"><span data-stu-id="a56eb-148">Fixes</span></span>**  

*   <span data-ttu-id="a56eb-149">Envisagez d’héberger votre contenu sur un CDN ou de modifier les fournisseurs d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="a56eb-149">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="a56eb-150">Envoyez moins d’octets en optimisant vos demandes.</span><span class="sxs-lookup"><span data-stu-id="a56eb-150">Send fewer bytes by optimizing your requests.</span></span>  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback](../media/smile-icon.msft.png)\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="a56eb-151">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a56eb-151">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspecter l’activité réseau dans Microsoft Edge devTools | Documents Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nouveau problème : MicrosoftDocs/edge-developer"  

> [!NOTE]
> <span data-ttu-id="a56eb-154">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a56eb-154">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a56eb-155">La page d’origine est trouvée ici et est co-auteure par [Les Basques Decéssaisie \(Rédacteur][KayceBasques] technique, Chrome DevTools \& Évérité\) et [Chef Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\). [](https://developers.google.com/web/tools/chrome-devtools/network/issues)</span><span class="sxs-lookup"><span data-stu-id="a56eb-155">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="a56eb-157">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a56eb-157">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors#jonathan-garbee
