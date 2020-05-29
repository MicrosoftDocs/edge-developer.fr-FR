---
title: Présentation des problèmes de sécurité avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611909"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="13611-103">Présentation des problèmes de sécurité avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="13611-103">Understand Security Issues With Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="13611-104">Ouvrir le volet sécurité</span><span class="sxs-lookup"><span data-stu-id="13611-104">Open the Security panel</span></span>   

<span data-ttu-id="13611-105">Le volet **sécurité** est l’endroit principal de devtools pour vérifier la sécurité d’une page.</span><span class="sxs-lookup"><span data-stu-id="13611-105">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="13611-106">[Ouvrez devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="13611-106">[Open DevTools][DevToolsOpen].</span></span>  

1.  <span data-ttu-id="13611-107">Cliquez sur l’onglet **sécurité** pour ouvrir le volet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="13611-107">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    > ##### <span data-ttu-id="13611-108">Figure1</span><span class="sxs-lookup"><span data-stu-id="13611-108">Figure 1</span></span>  
    > <span data-ttu-id="13611-109">Volet sécurité</span><span class="sxs-lookup"><span data-stu-id="13611-109">The Security panel</span></span>  
    > ![Volet sécurité][ImageSecurityPanel]  
    
## <span data-ttu-id="13611-111">Problèmes courants</span><span class="sxs-lookup"><span data-stu-id="13611-111">Common problems</span></span>   

### <span data-ttu-id="13611-112">Origines principales non sécurisées</span><span class="sxs-lookup"><span data-stu-id="13611-112">Non-secure main origins</span></span>   

<span data-ttu-id="13611-113">Lorsque l’origine principale d’une page n’est pas sécurisée, la **vue d’ensemble** de la sécurité indique que **cette page n’est pas sécurisée**.</span><span class="sxs-lookup"><span data-stu-id="13611-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

> ##### <span data-ttu-id="13611-114">Figure 2</span><span class="sxs-lookup"><span data-stu-id="13611-114">Figure 2</span></span>  
> <span data-ttu-id="13611-115">Page non sécurisée</span><span class="sxs-lookup"><span data-stu-id="13611-115">A non-secure page</span></span>  
> ![Page non sécurisée][ImageNonSecurePage]  

<span data-ttu-id="13611-117">Ce problème survient lorsque l’URL visitée a été demandée sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="13611-117">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="13611-118">Pour garantir la sécurité de votre application, vous devez la demander sur HTTPs.</span><span class="sxs-lookup"><span data-stu-id="13611-118">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="13611-119">Par exemple, si vous observez l’URL dans la barre d’adresses, il est probable que le résultat ressemble à ceci `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="13611-119">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="13611-120">Pour sécuriser l’URL, l’URL devrait être `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="13611-120">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="13611-121">Si vous avez déjà configuré HTTPs sur votre serveur, il vous suffit de configurer votre serveur pour rediriger toutes les demandes HTTP vers HTTPs.</span><span class="sxs-lookup"><span data-stu-id="13611-121">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="13611-122">Si vous n’avez pas configuré HTTPs sur votre serveur, [cryptez][LetsEncrypt] -vous pour démarrer le processus de manière gratuite et relativement simple.</span><span class="sxs-lookup"><span data-stu-id="13611-122">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="13611-123">Vous pouvez également envisagez d’héberger votre site sur un réseau de distribution de contenu (CDN).</span><span class="sxs-lookup"><span data-stu-id="13611-123">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="13611-124">La plupart des sites hôtes CDN les plus importants sur HTTPs par défaut.</span><span class="sxs-lookup"><span data-stu-id="13611-124">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="13611-125">La directive [utiliser HTTPS][WebhintUseHttps] dans [webhint][Webhint] permet d’automatiser le processus de vérification de l’utilisation de toutes les demandes HTTP adressées aux HTTPS.</span><span class="sxs-lookup"><span data-stu-id="13611-125">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="13611-126">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="13611-126">Mixed content</span></span>   

<span data-ttu-id="13611-127">Le **contenu mixte** signifie que l’origine principale d’une page est sécurisée, mais que la page a demandé des ressources d’origines non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="13611-127">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="13611-128">Les pages de contenu mixte ne sont que partiellement protégées, car le contenu HTTP est accessible aux renifleurs et est vulnérable aux attaques par le biais du milieu.</span><span class="sxs-lookup"><span data-stu-id="13611-128">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

> ##### <span data-ttu-id="13611-129">Figure3</span><span class="sxs-lookup"><span data-stu-id="13611-129">Figure 3</span></span>  
> <span data-ttu-id="13611-130">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="13611-130">Mixed content</span></span>  
> ![Contenu mixte][ImageMixedContent]  

<span data-ttu-id="13611-132">Dans la [figure 3](#figure-3), cliquez sur **Afficher 1 requête dans le panneau réseau** pour ouvrir le panneau **réseau** , puis appliquez le `mixed-content:displayed` filtre de sorte que le **Journal réseau** n’affiche que les ressources non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="13611-132">In [Figure 3](#figure-3), click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

> ##### <span data-ttu-id="13611-133">Figure 4</span><span class="sxs-lookup"><span data-stu-id="13611-133">Figure 4</span></span>  
> <span data-ttu-id="13611-134">Ressources mixtes du journal réseau</span><span class="sxs-lookup"><span data-stu-id="13611-134">Mixed resources in the Network Log</span></span>  
> ![Ressources mixtes du journal réseau][ImageMixedResourcesNetworkLog]  

## <span data-ttu-id="13611-136">Afficher les détails</span><span class="sxs-lookup"><span data-stu-id="13611-136">View details</span></span>   

### <span data-ttu-id="13611-137">Afficher le certificat d’origine principal</span><span class="sxs-lookup"><span data-stu-id="13611-137">View main origin certificate</span></span>   

<span data-ttu-id="13611-138">Dans la **vue d’ensemble**de la sécurité, cliquez sur **afficher le certificat** pour inspecter rapidement le certificat de l’origine principale.</span><span class="sxs-lookup"><span data-stu-id="13611-138">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

> ##### <span data-ttu-id="13611-139">Figure 5</span><span class="sxs-lookup"><span data-stu-id="13611-139">Figure 5</span></span>  
> <span data-ttu-id="13611-140">Un certificat d’origine principal;</span><span class="sxs-lookup"><span data-stu-id="13611-140">A main origin certificate</span></span>  
> ![Un certificat d’origine principal;][ImageCertificate]  

### <span data-ttu-id="13611-142">Afficher les détails de l’origine</span><span class="sxs-lookup"><span data-stu-id="13611-142">View origin details</span></span>   

<span data-ttu-id="13611-143">Cliquez sur l’une des entrées dans le volet de navigation de gauche pour afficher les détails de l’origine.</span><span class="sxs-lookup"><span data-stu-id="13611-143">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="13611-144">Dans la page détails, vous pouvez consulter les informations de connexion et de certificat.</span><span class="sxs-lookup"><span data-stu-id="13611-144">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="13611-145">Les informations de transparence du certificat apparaissent également lorsqu’elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="13611-145">Certificate transparency information is also shown when available.</span></span>  

> ##### <span data-ttu-id="13611-146">Figure 6</span><span class="sxs-lookup"><span data-stu-id="13611-146">Figure 6</span></span>  
> <span data-ttu-id="13611-147">Détails de l’origine principale</span><span class="sxs-lookup"><span data-stu-id="13611-147">Main origin details</span></span>  
> ![Détails de l’origine principale][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Figure 1: volet sécurité"  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Figure 2: page non sécurisée"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Figure 3: contenu mixte"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Figure 4: ressources mixtes du journal réseau"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Figure 5: certificat principal d’origine"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Figure 6: détails de l’origine principale"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  


[LetsEncrypt]: https://letsencrypt.org "Utiliser des certificats SSL/TLS sans cryptage"  

[Webhint]: https://webhint.io "Astuce"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Utiliser HTTPs | documentation webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="13611-160">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="13611-160">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="13611-161">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/security/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="13611-161">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="13611-163">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="13611-163">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
