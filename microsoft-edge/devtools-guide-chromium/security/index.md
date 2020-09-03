---
description: Utilisez le volet sécurité pour vous assurer qu’une page est entièrement protégée par HTTPs.
title: Présentation des problèmes de sécurité avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 2538f80b08c8162d27f075775075a8b81c5f7725
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993575"
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





# <span data-ttu-id="8e4c3-104">Présentation des problèmes de sécurité avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8e4c3-104">Understand security issues with Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="8e4c3-105">Ouvrir le volet sécurité</span><span class="sxs-lookup"><span data-stu-id="8e4c3-105">Open the Security panel</span></span>   

<span data-ttu-id="8e4c3-106">Le volet **sécurité** est l’endroit principal de devtools pour vérifier la sécurité d’une page.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="8e4c3-107">[Ouvrez devtools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="8e4c3-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="8e4c3-108">Cliquez sur l’onglet **sécurité** pour ouvrir le volet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="8e4c3-108">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Volet sécurité" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="8e4c3-110">Volet **sécurité**</span><span class="sxs-lookup"><span data-stu-id="8e4c3-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="8e4c3-111">Problèmes courants</span><span class="sxs-lookup"><span data-stu-id="8e4c3-111">Common problems</span></span>   

### <span data-ttu-id="8e4c3-112">Origines principales non sécurisées</span><span class="sxs-lookup"><span data-stu-id="8e4c3-112">Non-secure main origins</span></span>   

<span data-ttu-id="8e4c3-113">Lorsque l’origine principale d’une page n’est pas sécurisée, la **vue d’ensemble** de la sécurité indique que **cette page n’est pas sécurisée**.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Page non sécurisée" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="8e4c3-115">Page non sécurisée</span><span class="sxs-lookup"><span data-stu-id="8e4c3-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="8e4c3-116">Ce problème survient lorsque l’URL visitée a été demandée sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="8e4c3-117">Pour garantir la sécurité de votre application, vous devez la demander sur HTTPs.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="8e4c3-118">Par exemple, si vous observez l’URL dans la barre d’adresses, il est probable que le résultat ressemble à ceci `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="8e4c3-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="8e4c3-119">Pour sécuriser l’URL, l’URL devrait être `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="8e4c3-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="8e4c3-120">Si vous avez déjà configuré HTTPs sur votre serveur, il vous suffit de configurer votre serveur pour rediriger toutes les demandes HTTP vers HTTPs.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="8e4c3-121">Si vous n’avez pas configuré HTTPs sur votre serveur, [cryptez][LetsEncrypt] -vous pour démarrer le processus de manière gratuite et relativement simple.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="8e4c3-122">Vous pouvez également envisagez d’héberger votre site sur un réseau de distribution de contenu (CDN).</span><span class="sxs-lookup"><span data-stu-id="8e4c3-122">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="8e4c3-123">La plupart des sites hôtes CDN les plus importants sur HTTPs par défaut.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="8e4c3-124">La directive [utiliser HTTPS][WebhintUseHttps] dans [webhint][Webhint] permet d’automatiser le processus de vérification de l’utilisation de toutes les demandes HTTP adressées aux HTTPS.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="8e4c3-125">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="8e4c3-125">Mixed content</span></span>   

<span data-ttu-id="8e4c3-126">Le **contenu mixte** signifie que l’origine principale d’une page est sécurisée, mais que la page a demandé des ressources d’origines non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="8e4c3-127">Les pages de contenu mixte ne sont que partiellement protégées, car le contenu HTTP est accessible aux renifleurs et est vulnérable aux attaques par le biais du milieu.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Contenu mixte" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="8e4c3-129">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="8e4c3-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="8e4c3-130">Dans la figure précédente, cliquez sur **afficher une requête dans le panneau réseau** pour ouvrir le panneau **réseau** et appliquez le `mixed-content:displayed` filtre de sorte que le **Journal réseau** n’affiche que les ressources non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-130">In the previous figure, click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Ressources mixtes du journal réseau" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="8e4c3-132">Ressources mixtes du **Journal réseau**</span><span class="sxs-lookup"><span data-stu-id="8e4c3-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <span data-ttu-id="8e4c3-133">Afficher les détails</span><span class="sxs-lookup"><span data-stu-id="8e4c3-133">View details</span></span>   

### <span data-ttu-id="8e4c3-134">Afficher le certificat d’origine principal</span><span class="sxs-lookup"><span data-stu-id="8e4c3-134">View main origin certificate</span></span>   

<span data-ttu-id="8e4c3-135">Dans la **vue d’ensemble**de la sécurité, cliquez sur **afficher le certificat** pour inspecter rapidement le certificat de l’origine principale.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-135">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Un certificat d’origine principal;" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="8e4c3-137">Un certificat d’origine principal;</span><span class="sxs-lookup"><span data-stu-id="8e4c3-137">A main origin certificate</span></span>  
:::image-end:::  

### <span data-ttu-id="8e4c3-138">Afficher les détails de l’origine</span><span class="sxs-lookup"><span data-stu-id="8e4c3-138">View origin details</span></span>   

<span data-ttu-id="8e4c3-139">Cliquez sur l’une des entrées dans le volet de navigation de gauche pour afficher les détails de l’origine.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-139">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="8e4c3-140">Dans la page détails, vous pouvez consulter les informations de connexion et de certificat.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="8e4c3-141">Les informations de transparence du certificat apparaissent également lorsqu’elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="8e4c3-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Détails de l’origine principale" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="8e4c3-143">Détails de l’origine principale</span><span class="sxs-lookup"><span data-stu-id="8e4c3-143">Main origin details</span></span>  
:::image-end:::  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevToolsOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  


[LetsEncrypt]: https://letsencrypt.org "Utiliser des certificats SSL/TLS sans cryptage"  

[Webhint]: https://webhint.io "Astuce"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Utiliser HTTPs | documentation webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="8e4c3-149">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e4c3-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8e4c3-150">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/security/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="8e4c3-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="8e4c3-152">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8e4c3-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
