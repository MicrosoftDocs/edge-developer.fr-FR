---
title: Guide des problèmes réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a9a3234f3516bef16328102858363ffcb06251ec
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985379"
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





# <span data-ttu-id="5cf16-103">Guide de problèmes réseau</span><span class="sxs-lookup"><span data-stu-id="5cf16-103">Network issues guide</span></span>   




<span data-ttu-id="5cf16-104">Ce guide vous montre comment détecter les problèmes de réseau ou les opportunités d’optimisation dans le volet réseau de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5cf16-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="5cf16-105">Pour [plus d’informations][NetworkPerformance] sur les concepts de base du **réseau** , voir découvrir le panneau de configuration.</span><span class="sxs-lookup"><span data-stu-id="5cf16-105">See [Get Started][NetworkPerformance] to learn the basics of the **Network** panel.</span></span>  

## <span data-ttu-id="5cf16-106">Demandes mises en file d’attente ou bloquées</span><span class="sxs-lookup"><span data-stu-id="5cf16-106">Queued or stalled requests</span></span>   

**<span data-ttu-id="5cf16-107">Symptômes</span><span class="sxs-lookup"><span data-stu-id="5cf16-107">Symptoms</span></span>**  

<span data-ttu-id="5cf16-108">Six demandes sont en train de télécharger simultanément.</span><span class="sxs-lookup"><span data-stu-id="5cf16-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="5cf16-109">Après cela, une série de demandes est mise en file d’attente ou bloquée.</span><span class="sxs-lookup"><span data-stu-id="5cf16-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="5cf16-110">Après l’exécution de l’une des six premières demandes, une des requêtes de la file d’attente démarre.</span><span class="sxs-lookup"><span data-stu-id="5cf16-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="5cf16-111">Dans la **figure** ci-dessous, les six premières demandes de l' `edge-iconx1024.msft.png` actif commencent simultanément.</span><span class="sxs-lookup"><span data-stu-id="5cf16-111">In the **Waterfall** in the following figure, the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="5cf16-112">Les demandes ultérieures sont bloquées jusqu’à ce que l’une des six nouvelles préfinissements.</span><span class="sxs-lookup"><span data-stu-id="5cf16-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   <span data-ttu-id="5cf16-114">Exemple d’une série mise en file d’attente ou bloquée dans le panneau **réseau**</span><span class="sxs-lookup"><span data-stu-id="5cf16-114">An example of a queued or stalled series in the **Network** panel</span></span>  
:::image-end:::  

**<span data-ttu-id="5cf16-115">Causes</span><span class="sxs-lookup"><span data-stu-id="5cf16-115">Causes</span></span>**  

<span data-ttu-id="5cf16-116">Il y a trop de demandes sur un domaine unique.</span><span class="sxs-lookup"><span data-stu-id="5cf16-116">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="5cf16-117">Sur les connexions HTTP/1.0 ou HTTP/1.1, Microsoft Edge autorise un maximum de six connexions TCP simultanées par hôte.</span><span class="sxs-lookup"><span data-stu-id="5cf16-117">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

**<span data-ttu-id="5cf16-118">Correctifs</span><span class="sxs-lookup"><span data-stu-id="5cf16-118">Fixes</span></span>**  

*   <span data-ttu-id="5cf16-119">Implémentez Domain sharding si vous devez utiliser HTTP/1.0 ou HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="5cf16-119">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="5cf16-120">Utiliser HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="5cf16-120">Use HTTP/2.</span></span>  <span data-ttu-id="5cf16-121">N’utilisez pas le domaine sharding avec HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="5cf16-121">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="5cf16-122">Supprimez ou différez les demandes inutiles de manière à ce que les demandes critiques soient téléchargées plus tôt.</span><span class="sxs-lookup"><span data-stu-id="5cf16-122">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  
    
## <span data-ttu-id="5cf16-123">Temps lent vers le premier octet (TTFB)</span><span class="sxs-lookup"><span data-stu-id="5cf16-123">Slow Time To First Byte (TTFB)</span></span>   

**<span data-ttu-id="5cf16-124">Symptômes</span><span class="sxs-lookup"><span data-stu-id="5cf16-124">Symptoms</span></span>**  

<span data-ttu-id="5cf16-125">Une requête passe un certain temps en attente de réception du premier octet du serveur.</span><span class="sxs-lookup"><span data-stu-id="5cf16-125">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="5cf16-126">Dans l’illustration ci-dessous, la barre verte longue de la **cascade** indique que la requête attendait un certain temps.</span><span class="sxs-lookup"><span data-stu-id="5cf16-126">In the following figure, the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="5cf16-127">Il a été simulé à l’aide d’un profil afin de limiter la vitesse du réseau et d’ajouter un délai.</span><span class="sxs-lookup"><span data-stu-id="5cf16-127">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Exemple d’une requête avec un délai de première octet lent" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   <span data-ttu-id="5cf16-129">Exemple d’une requête avec un délai de première octet lent</span><span class="sxs-lookup"><span data-stu-id="5cf16-129">An example of a request with a slow Time To First Byte</span></span>  
:::image-end:::  

**<span data-ttu-id="5cf16-130">Causes</span><span class="sxs-lookup"><span data-stu-id="5cf16-130">Causes</span></span>**  

*   <span data-ttu-id="5cf16-131">La connexion entre le client et le serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="5cf16-131">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="5cf16-132">La réponse du serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="5cf16-132">The server is slow to respond.</span></span>  <span data-ttu-id="5cf16-133">Hébergez le serveur localement pour déterminer s’il s’agit d’une connexion ou d’un serveur lent.</span><span class="sxs-lookup"><span data-stu-id="5cf16-133">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="5cf16-134">Si vous obtenez encore un temps lente pour le premier octet \ (TTFB \) lors de l’accès à un serveur local, le serveur est lent.</span><span class="sxs-lookup"><span data-stu-id="5cf16-134">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  
    
**<span data-ttu-id="5cf16-135">Correctifs</span><span class="sxs-lookup"><span data-stu-id="5cf16-135">Fixes</span></span>**  

*   <span data-ttu-id="5cf16-136">Si la connexion est lente, envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="5cf16-136">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="5cf16-137">Si le serveur est lent, envisagez d’optimiser les requêtes de base de données, de mettre en cache ou de modifier votre configuration serveur.</span><span class="sxs-lookup"><span data-stu-id="5cf16-137">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  
    
## <span data-ttu-id="5cf16-138">Téléchargement de contenu lent</span><span class="sxs-lookup"><span data-stu-id="5cf16-138">Slow content download</span></span>   

**<span data-ttu-id="5cf16-139">Symptômes</span><span class="sxs-lookup"><span data-stu-id="5cf16-139">Symptoms</span></span>**  

<span data-ttu-id="5cf16-140">Le téléchargement d’une requête prend beaucoup de temps.</span><span class="sxs-lookup"><span data-stu-id="5cf16-140">A request takes a long time to download.</span></span>  

<span data-ttu-id="5cf16-141">Dans l’illustration ci-dessous, la barre bleue longue en **regard du** fichier PNG signifie que le téléchargement a duré longtemps.</span><span class="sxs-lookup"><span data-stu-id="5cf16-141">In the following figure, the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Exemple d’une requête prenant du temps à télécharger" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   <span data-ttu-id="5cf16-143">Exemple d’une requête prenant du temps à télécharger</span><span class="sxs-lookup"><span data-stu-id="5cf16-143">An example of a request that takes a long time to download</span></span>  
:::image-end:::  

**<span data-ttu-id="5cf16-144">Causes</span><span class="sxs-lookup"><span data-stu-id="5cf16-144">Causes</span></span>**  

*   <span data-ttu-id="5cf16-145">La connexion entre le client et le serveur est lente.</span><span class="sxs-lookup"><span data-stu-id="5cf16-145">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="5cf16-146">Un grand nombre de contenus est en cours de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="5cf16-146">A lot of content is being downloaded.</span></span>  
    
**<span data-ttu-id="5cf16-147">Correctifs</span><span class="sxs-lookup"><span data-stu-id="5cf16-147">Fixes</span></span>**  

*   <span data-ttu-id="5cf16-148">Envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="5cf16-148">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="5cf16-149">Envoyez moins d’octets en optimisant vos demandes.</span><span class="sxs-lookup"><span data-stu-id="5cf16-149">Send fewer bytes by optimizing your requests.</span></span>  
    
## <span data-ttu-id="5cf16-150">Compétences de collaboration</span><span class="sxs-lookup"><span data-stu-id="5cf16-150">Contribute knowledge</span></span>  

<span data-ttu-id="5cf16-151">Vous rencontrez un problème réseau qui doit être ajouté à ce guide?</span><span class="sxs-lookup"><span data-stu-id="5cf16-151">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="5cf16-152">Envoyez un tweet à [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="5cf16-152">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="5cf16-153">Pour **Envoyer** ![ des ][ImageSendFeedbackIcon] `Alt` + `Shift` + `I` `Option` + `Shift` + `I` commentaires ou des demandes de fonctionnalité, sélectionnez Envoyer des commentaires \ (envoyer des commentaires \) dans le devtools ou appuyez sur \</span><span class="sxs-lookup"><span data-stu-id="5cf16-153">Select **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="5cf16-154">[Ouvrez un problème][WebFundamentalsIssue] dans le référentiel Samples docs.</span><span class="sxs-lookup"><span data-stu-id="5cf16-154">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  
    
<!--  
  


-->  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Examiner l’activité réseau dans Microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nouveau problème-MicrosoftDocs/Edge-développeur"  

> [!NOTE]
> <span data-ttu-id="5cf16-157">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5cf16-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5cf16-158">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/issues) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Jonathan Garbee][JonathanGarbee] \ (Google Developer expertise pour Web Technology \).</span><span class="sxs-lookup"><span data-stu-id="5cf16-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="5cf16-160">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5cf16-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
