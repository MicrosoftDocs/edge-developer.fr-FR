---
description: Découvrez comment afficher les données du cache d’application à partir du panneau application de Microsoft Edge DevTools.
title: Afficher les données du cache d’application avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3d73047a8332e4d6cae5f7411f968a7dfe4c3738
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230781"
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

# <span data-ttu-id="0621d-104">Afficher les données du cache d’application avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="0621d-104">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="0621d-105">L’API du cache d’application est [supprimée de la plateforme Web][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="0621d-105">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="0621d-106">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les ressources [du cache d’applications][MDNWebAPIsWindowApplicationCache] .</span><span class="sxs-lookup"><span data-stu-id="0621d-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="0621d-107">Afficher les données du cache d’application</span><span class="sxs-lookup"><span data-stu-id="0621d-107">View Application Cache data</span></span>  

1.  <span data-ttu-id="0621d-108">Sélectionnez l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="0621d-108">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="0621d-109">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="0621d-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="0621d-111">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="0621d-111">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="0621d-112">Développez la section cache de l' **application** , puis choisissez une mise en cache pour afficher les ressources.</span><span class="sxs-lookup"><span data-stu-id="0621d-112">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Volet cache de l’application" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="0621d-114">Volet **cache** de l’application</span><span class="sxs-lookup"><span data-stu-id="0621d-114">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="0621d-115">Chaque ligne de la table représente une ressource mise en cache.</span><span class="sxs-lookup"><span data-stu-id="0621d-115">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="0621d-116">La colonne **type** représente la [catégorie de la ressource][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="0621d-116">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="0621d-117">Catégorie</span><span class="sxs-lookup"><span data-stu-id="0621d-117">Category</span></span> | <span data-ttu-id="0621d-118">Détails</span><span class="sxs-lookup"><span data-stu-id="0621d-118">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="0621d-119">Cette ressource a été explicitement répertoriée dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="0621d-119">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="0621d-120">L’URL est une alternative pour une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="0621d-120">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="0621d-121">L’URL de l’autre ressource n’est pas répertoriée dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="0621d-121">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="0621d-122">L' `manifest` attribut de la ressource indique que le cache est le parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="0621d-122">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="0621d-123">Le manifeste spécifié que la ressource doit provenir du réseau.</span><span class="sxs-lookup"><span data-stu-id="0621d-123">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="0621d-124">En bas du tableau figure il existe des icônes de statut indiquant votre connexion réseau et l’état du **cache**de l’application.</span><span class="sxs-lookup"><span data-stu-id="0621d-124">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="0621d-125">Le **cache** de l’application doit présenter les États suivants.</span><span class="sxs-lookup"><span data-stu-id="0621d-125">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="0621d-126">État</span><span class="sxs-lookup"><span data-stu-id="0621d-126">State</span></span> | <span data-ttu-id="0621d-127">Détails</span><span class="sxs-lookup"><span data-stu-id="0621d-127">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="0621d-128">Le manifeste est en cours de lecture et vérifie les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="0621d-128">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="0621d-129">Les ressources sont ajoutées au cache.</span><span class="sxs-lookup"><span data-stu-id="0621d-129">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="0621d-130">Le cache ne comporte pas de nouvelles modifications.</span><span class="sxs-lookup"><span data-stu-id="0621d-130">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="0621d-131">Le cache est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="0621d-131">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="0621d-132">Une nouvelle version du cache est disponible.</span><span class="sxs-lookup"><span data-stu-id="0621d-132">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Applications Web hors connexion-norme HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressources dans le cache de l’application | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-API Web | MDN"  

> [!NOTE]
> <span data-ttu-id="0621d-137">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0621d-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="0621d-138">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="0621d-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="0621d-140">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="0621d-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
