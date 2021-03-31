---
description: Utilisez le Panneau de sécurité pour vous assurer qu’une page est entièrement protégée par HTTPS.
title: Comprendre les problèmes de sécurité avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397775"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a><span data-ttu-id="92418-104">Comprendre les problèmes de sécurité avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="92418-104">Understand security issues with Microsoft Edge DevTools</span></span>  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a><span data-ttu-id="92418-105">Ouvrir le panneau de sécurité</span><span class="sxs-lookup"><span data-stu-id="92418-105">Open the Security panel</span></span>  

<span data-ttu-id="92418-106">Le **panneau** de sécurité est l’endroit principal dans DevTools pour l’inspection de la sécurité d’une page.</span><span class="sxs-lookup"><span data-stu-id="92418-106">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="92418-107">[Ouvrez DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="92418-107">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="92418-108">Sélectionnez **l’onglet** Sécurité pour ouvrir **l’outil** Sécurité.</span><span class="sxs-lookup"><span data-stu-id="92418-108">Choose the **Security** tab to open the **Security** tool.</span></span>  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Panneau de sécurité" lightbox="../media/security-security-overview-secure.msft.png":::
       <span data-ttu-id="92418-110">Panneau **de** sécurité</span><span class="sxs-lookup"><span data-stu-id="92418-110">The **Security** panel</span></span>  
    :::image-end:::  
    
## <a name="common-problems"></a><span data-ttu-id="92418-111">Problèmes courants</span><span class="sxs-lookup"><span data-stu-id="92418-111">Common problems</span></span>  

### <a name="non-secure-main-origins"></a><span data-ttu-id="92418-112">Origines principales non sécurisées</span><span class="sxs-lookup"><span data-stu-id="92418-112">Non-secure main origins</span></span>  

<span data-ttu-id="92418-113">Lorsque l’origine principale d’une page n’est pas sécurisée, la vue **d’ensemble** de la sécurité indique **que cette page n’est pas sécurisée.**</span><span class="sxs-lookup"><span data-stu-id="92418-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Page non sécurisée" lightbox="../media/security-security-overview-non-secure.msft.png":::
   <span data-ttu-id="92418-115">Page non sécurisée</span><span class="sxs-lookup"><span data-stu-id="92418-115">A non-secure page</span></span>  
:::image-end:::  

<span data-ttu-id="92418-116">Ce problème se produit lorsque l’URL que vous avez visitée a été demandée sur HTTP.</span><span class="sxs-lookup"><span data-stu-id="92418-116">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="92418-117">Pour le sécuriser, vous devez le demander sur HTTPS.</span><span class="sxs-lookup"><span data-stu-id="92418-117">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="92418-118">Par exemple, si vous examinez l’URL dans votre barre d’adresses, elle ressemble probablement à `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="92418-118">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="92418-119">Pour sécuriser l’URL doit être `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="92418-119">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="92418-120">Si vous avez déjà configuré HTTPS sur votre serveur, il vous suffit de configurer votre serveur pour qu’il redirige toutes les requêtes HTTP vers HTTPS.</span><span class="sxs-lookup"><span data-stu-id="92418-120">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="92418-121">Si vous [n’avez][LetsEncrypt] pas installé HTTPS sur votre serveur, chiffrer offre un moyen gratuit et relativement simple de démarrer le processus.</span><span class="sxs-lookup"><span data-stu-id="92418-121">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="92418-122">Vous pouvez également envisager d’héberger votre site sur un CDN.</span><span class="sxs-lookup"><span data-stu-id="92418-122">Or, you may consider hosting your site on a CDN.</span></span>  <span data-ttu-id="92418-123">La plupart des PRINCIPAUX CDN hébergent des sites sur HTTPS par défaut maintenant.</span><span class="sxs-lookup"><span data-stu-id="92418-123">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="92418-124">[L’indication Utiliser HTTPS][WebhintUseHttps] dans [webhint][Webhint] peut vous aider à automatiser le processus de s’assurer que toutes les requêtes HTTP sont dirigées vers HTTPS.</span><span class="sxs-lookup"><span data-stu-id="92418-124">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <a name="mixed-content"></a><span data-ttu-id="92418-125">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="92418-125">Mixed content</span></span>  

<span data-ttu-id="92418-126">**Le contenu mixte** signifie que l’origine principale d’une page est sécurisée, mais que la page a demandé des ressources à partir d’origines non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="92418-126">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="92418-127">Les pages de contenu mixte ne sont que partiellement protégées, car le contenu HTTP est accessible aux renifleurs et vulnérable aux attaques de l’homme au milieu.</span><span class="sxs-lookup"><span data-stu-id="92418-127">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Contenu mixte" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   <span data-ttu-id="92418-129">Contenu mixte</span><span class="sxs-lookup"><span data-stu-id="92418-129">Mixed content</span></span>  
:::image-end:::  

<span data-ttu-id="92418-130">Dans la figure précédente, choisissez Afficher **1**  dans le panneau Réseau pour ouvrir l’outil Réseau et appliquer le filtre afin que le journal réseau affiche uniquement les ressources `mixed-content:displayed` non  sécurisées.</span><span class="sxs-lookup"><span data-stu-id="92418-130">In the previous figure, choose **View 1 request in Network panel** to open the **Network** tool and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Ressources mixtes dans le journal réseau" lightbox="../media/security-network-filter.msft.png":::
   <span data-ttu-id="92418-132">Ressources mixtes dans le **journal réseau**</span><span class="sxs-lookup"><span data-stu-id="92418-132">Mixed resources in the **Network Log**</span></span>  
:::image-end:::  

## <a name="view-details"></a><span data-ttu-id="92418-133">Afficher les détails</span><span class="sxs-lookup"><span data-stu-id="92418-133">View details</span></span>  

### <a name="view-main-origin-certificate"></a><span data-ttu-id="92418-134">Afficher le certificat d’origine principale</span><span class="sxs-lookup"><span data-stu-id="92418-134">View main origin certificate</span></span>  

<span data-ttu-id="92418-135">Dans la **vue d’ensemble de**la sécurité, choisissez **Afficher le certificat** pour inspecter rapidement le certificat pour l’origine principale.</span><span class="sxs-lookup"><span data-stu-id="92418-135">From the **Security Overview**, choose **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Un certificat d’origine principale" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   <span data-ttu-id="92418-137">Un certificat d’origine principale</span><span class="sxs-lookup"><span data-stu-id="92418-137">A main origin certificate</span></span>  
:::image-end:::  

### <a name="view-origin-details"></a><span data-ttu-id="92418-138">Afficher les détails de l’origine</span><span class="sxs-lookup"><span data-stu-id="92418-138">View origin details</span></span>  

<span data-ttu-id="92418-139">Choisissez l’une des entrées du navigation gauche pour afficher les détails de l’origine.</span><span class="sxs-lookup"><span data-stu-id="92418-139">Choose one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="92418-140">À partir de la page de détails, vous pouvez afficher les informations de connexion et de certificat.</span><span class="sxs-lookup"><span data-stu-id="92418-140">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="92418-141">Les informations de transparence des certificats sont également affichées lorsqu’elles sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="92418-141">Certificate transparency information is also shown when available.</span></span>  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Détails de l’origine principale" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   <span data-ttu-id="92418-143">Détails de l’origine principale</span><span class="sxs-lookup"><span data-stu-id="92418-143">Main origin details</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="92418-144">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="92418-144">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevToolsOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[LetsEncrypt]: https://letsencrypt.org "Chiffrement - Certificats SSL/TLS gratuits"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Utiliser le protocole HTTPS | documentation webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="92418-150">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92418-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="92418-151">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/security/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="92418-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="92418-153">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="92418-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
