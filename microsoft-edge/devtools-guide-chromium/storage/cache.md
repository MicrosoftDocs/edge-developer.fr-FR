---
description: Découvrez comment afficher les données du cache à partir du panneau application de Microsoft Edge DevTools.
title: Afficher les données du cache avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c920a171ec89925cc79ab741eed01e11d749bf1b
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993295"
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





# <span data-ttu-id="46bce-104">Afficher les données du cache avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="46bce-104">View cache data with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="46bce-105">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les données [du cache][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="46bce-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="46bce-106">Si vous essayez d’inspecter les données [du cache http][MDNHTTPCaching] , il ne s’agit pas du guide souhaité.</span><span class="sxs-lookup"><span data-stu-id="46bce-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="46bce-107">Recherchez les informations dans la colonne **taille** du journal du **réseau**.</span><span class="sxs-lookup"><span data-stu-id="46bce-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="46bce-108">Voir [enregistrement][DevtoolsNetworkLogActivity]de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="46bce-108">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="46bce-109">Afficher les données du cache</span><span class="sxs-lookup"><span data-stu-id="46bce-109">View cache data</span></span>   

1.  <span data-ttu-id="46bce-110">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="46bce-110">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="46bce-111">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="46bce-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="46bce-113">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="46bce-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46bce-114">Développez la section **stockage du cache** pour afficher les caches disponibles.</span><span class="sxs-lookup"><span data-stu-id="46bce-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Caches disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="46bce-116">Caches disponibles</span><span class="sxs-lookup"><span data-stu-id="46bce-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46bce-117">Sélectionnez un cache pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="46bce-117">Select a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Afficher le contenu d’un cache" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="46bce-119">Afficher le contenu d’un cache</span><span class="sxs-lookup"><span data-stu-id="46bce-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46bce-120">Sélectionnez une ressource pour afficher les en-têtes HTTP dans la section située sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="46bce-120">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Afficher les en-têtes HTTP d’une ressource" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="46bce-122">Afficher les en-têtes HTTP d’une ressource</span><span class="sxs-lookup"><span data-stu-id="46bce-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46bce-123">Sélectionnez **Aperçu** pour afficher le contenu d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="46bce-123">Select **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Afficher le contenu d’une ressource" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="46bce-125">Afficher le contenu d’une ressource</span><span class="sxs-lookup"><span data-stu-id="46bce-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="46bce-126">Actualiser une ressource</span><span class="sxs-lookup"><span data-stu-id="46bce-126">Refresh a resource</span></span>   

1.  <span data-ttu-id="46bce-127">[Afficher les données d’un cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="46bce-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="46bce-128">Sélectionnez la ressource que vous voulez actualiser.</span><span class="sxs-lookup"><span data-stu-id="46bce-128">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="46bce-129">DevTools le met en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="46bce-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Sélectionner une ressource" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="46bce-131">Sélectionner une ressource</span><span class="sxs-lookup"><span data-stu-id="46bce-131">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46bce-132">Sélectionnez **Actualiser** /actualiser ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="46bce-132">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="46bce-133">Filtrer les ressources</span><span class="sxs-lookup"><span data-stu-id="46bce-133">Filter resources</span></span>   

1.  <span data-ttu-id="46bce-134">[Afficher les données d’un cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="46bce-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="46bce-135">Utilisez la zone de texte **Filtrer par chemin** pour filtrer les ressources qui ne correspondent pas au chemin que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="46bce-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrer les ressources qui ne correspondent pas au chemin spécifié" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="46bce-137">Filtrer les ressources qui ne correspondent pas au chemin spécifié</span><span class="sxs-lookup"><span data-stu-id="46bce-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="46bce-138">Suppression d'une ressource</span><span class="sxs-lookup"><span data-stu-id="46bce-138">Delete a resource</span></span>   

1.  <span data-ttu-id="46bce-139">[Afficher les données d’un cache](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="46bce-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="46bce-140">Sélectionnez la ressource que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="46bce-140">Select the resource that you want to delete.</span></span>  <span data-ttu-id="46bce-141">DevTools le met en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="46bce-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Sélectionner une ressource" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="46bce-143">Sélectionner une ressource</span><span class="sxs-lookup"><span data-stu-id="46bce-143">Select a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46bce-144">Sélectionnez **Supprimer la sélection** \ ( ![ Supprimer la sélection ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="46bce-144">Select **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="46bce-145">Supprimer toutes les données du cache</span><span class="sxs-lookup"><span data-stu-id="46bce-145">Delete all cache data</span></span>   

1.  <span data-ttu-id="46bce-146">Ouvrez l' **application**  >  **Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="46bce-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="46bce-147">Vérifiez que la case à cocher **stockage du cache** est activée.</span><span class="sxs-lookup"><span data-stu-id="46bce-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Case à cocher stockage du cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="46bce-149">Case à cocher **stockage du cache**</span><span class="sxs-lookup"><span data-stu-id="46bce-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="46bce-150">Sélectionnez **effacer les données du site**.</span><span class="sxs-lookup"><span data-stu-id="46bce-150">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="46bce-152">Bouton **effacer les données du site**</span><span class="sxs-lookup"><span data-stu-id="46bce-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
  


-->  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Journalisation de l’activité du réseau | Documents Microsoft"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP MDN"  

> [!NOTE]
> <span data-ttu-id="46bce-157">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="46bce-157">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="46bce-158">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cache) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="46bce-158">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="46bce-160">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="46bce-160">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
