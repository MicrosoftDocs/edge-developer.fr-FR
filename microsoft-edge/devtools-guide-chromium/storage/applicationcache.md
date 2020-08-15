---
title: Afficher les données du cache d’application avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: fc1800fc54e5fb0d7998c62ce163ece7a461dd82
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931208"
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

# <span data-ttu-id="9f1d9-103">Afficher les données du cache d’application avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9f1d9-103">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="9f1d9-104">L’API du cache d’application est [supprimée de la plateforme Web][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="9f1d9-104">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="9f1d9-105">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les ressources [du cache d’applications][MDNWebAPIsWindowApplicationCache] .</span><span class="sxs-lookup"><span data-stu-id="9f1d9-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="9f1d9-106">Afficher les données du cache d’application</span><span class="sxs-lookup"><span data-stu-id="9f1d9-106">View Application Cache data</span></span>  

1.  <span data-ttu-id="9f1d9-107">Sélectionnez l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="9f1d9-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="9f1d9-108">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-108">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="9f1d9-110">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="9f1d9-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="9f1d9-111">Développez la section cache de l' **application** , puis choisissez une mise en cache pour afficher les ressources.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Volet cache de l’application" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="9f1d9-113">Volet **cache** de l’application</span><span class="sxs-lookup"><span data-stu-id="9f1d9-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="9f1d9-114">Chaque ligne de la table représente une ressource mise en cache.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="9f1d9-115">La colonne **type** représente la [catégorie de la ressource][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="9f1d9-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="9f1d9-116">Catégorie</span><span class="sxs-lookup"><span data-stu-id="9f1d9-116">Category</span></span> | <span data-ttu-id="9f1d9-117">Détails</span><span class="sxs-lookup"><span data-stu-id="9f1d9-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="9f1d9-118">Cette ressource a été explicitement répertoriée dans le manifeste.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="9f1d9-119">L’URL est une alternative pour une autre ressource.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="9f1d9-120">L’URL de l’autre ressource n’est pas répertoriée dans DevTools.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="9f1d9-121">L' `manifest` attribut de la ressource indique que le cache est le parent de la ressource.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="9f1d9-122">Le manifeste spécifié que la ressource doit provenir du réseau.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="9f1d9-123">En bas du tableau figure il existe des icônes de statut indiquant votre connexion réseau et l’état du **cache**de l’application.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="9f1d9-124">Le **cache** de l’application doit présenter les États suivants.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="9f1d9-125">État</span><span class="sxs-lookup"><span data-stu-id="9f1d9-125">State</span></span> | <span data-ttu-id="9f1d9-126">Détails</span><span class="sxs-lookup"><span data-stu-id="9f1d9-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="9f1d9-127">Le manifeste est en cours de lecture et vérifie les mises à jour.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="9f1d9-128">Les ressources sont ajoutées au cache.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="9f1d9-129">Le cache ne comporte pas de nouvelles modifications.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="9f1d9-130">Le cache est en cours de suppression.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="9f1d9-131">Une nouvelle version du cache est disponible.</span><span class="sxs-lookup"><span data-stu-id="9f1d9-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Applications Web hors connexion-norme HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressources dans le cache de l’application | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-API Web | MDN"  

> [!NOTE]
> <span data-ttu-id="9f1d9-136">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9f1d9-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9f1d9-137">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="9f1d9-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="9f1d9-139">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9f1d9-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
