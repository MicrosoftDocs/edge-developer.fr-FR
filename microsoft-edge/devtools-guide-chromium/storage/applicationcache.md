---
description: Découvrez comment afficher les données du cache d'application à partir du panneau Application de Microsoft Edge DevTools.
title: Afficher les données du cache d'application avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: cbe6623aa3132db4d01cd6b440702eb157525eed
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519141"
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

# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="4e238-104">Afficher les données du cache d'application avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="4e238-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="4e238-105">L'API de cache [d'application est supprimée de la plateforme web.][HTMLStandardOfflineWebApplications]</span><span class="sxs-lookup"><span data-stu-id="4e238-105">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="4e238-106">Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour inspecter les ressources [du cache d'applications.][MDNWebAPIsWindowApplicationCache]</span><span class="sxs-lookup"><span data-stu-id="4e238-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <a name="view-application-cache-data"></a><span data-ttu-id="4e238-107">Afficher les données du cache d'application</span><span class="sxs-lookup"><span data-stu-id="4e238-107">View Application Cache data</span></span>  

1.  <span data-ttu-id="4e238-108">En haut de DevTools, choisissez **l'outil Application.**</span><span class="sxs-lookup"><span data-stu-id="4e238-108">At the top of DevTools, choose the **Application** tool.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="4e238-110">Volet \*\*\*\* manifeste</span><span class="sxs-lookup"><span data-stu-id="4e238-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="4e238-111">Développez la section **Cache d'applications** et choisissez un cache pour afficher les ressources.</span><span class="sxs-lookup"><span data-stu-id="4e238-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Volet Cache d'applications" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="4e238-113">Volet **Cache d'applications**</span><span class="sxs-lookup"><span data-stu-id="4e238-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="4e238-114">Chaque ligne du tableau représente une ressource mise en cache.</span><span class="sxs-lookup"><span data-stu-id="4e238-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="4e238-115">La **colonne Type** représente la catégorie de la [ressource.][MDNHTMLResourcesInAnApplicationCache]</span><span class="sxs-lookup"><span data-stu-id="4e238-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="4e238-116">Catégorie</span><span class="sxs-lookup"><span data-stu-id="4e238-116">Category</span></span> | <span data-ttu-id="4e238-117">Détails</span><span class="sxs-lookup"><span data-stu-id="4e238-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="4e238-118">Cette ressource a été explicitement répertoriée dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="4e238-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="4e238-119">L'URL est un de base pour une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="4e238-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="4e238-120">L'URL de l'autre ressource n'est pas répertoriée dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="4e238-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="4e238-121">`manifest`L'attribut de la ressource indique que le cache est le parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="4e238-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="4e238-122">Le manifeste spécifie que la ressource doit être provenant du réseau.</span><span class="sxs-lookup"><span data-stu-id="4e238-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="4e238-123">En bas du tableau se cachent des icônes d'état indiquant votre connexion réseau et l'état du **cache d'applications.**</span><span class="sxs-lookup"><span data-stu-id="4e238-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="4e238-124">Le **cache d'applications** peut avoir les états suivants.</span><span class="sxs-lookup"><span data-stu-id="4e238-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="4e238-125">État</span><span class="sxs-lookup"><span data-stu-id="4e238-125">State</span></span> | <span data-ttu-id="4e238-126">Détails</span><span class="sxs-lookup"><span data-stu-id="4e238-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="4e238-127">Le manifeste est en cours d'extraction et a été vérifié pour les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="4e238-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="4e238-128">Les ressources sont ajoutées au cache.</span><span class="sxs-lookup"><span data-stu-id="4e238-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="4e238-129">Aucune nouvelle modification n'est apportée au cache.</span><span class="sxs-lookup"><span data-stu-id="4e238-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="4e238-130">Le cache est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="4e238-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="4e238-131">Une nouvelle version du cache est disponible.</span><span class="sxs-lookup"><span data-stu-id="4e238-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Applications Web hors connexion - Html Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressources dans un cache d'application | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache - Api web | MDN"  

> [!NOTE]
> <span data-ttu-id="4e238-136">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e238-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4e238-137">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="4e238-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="4e238-139">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e238-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
