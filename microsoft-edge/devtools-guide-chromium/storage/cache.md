---
description: Découvrez comment afficher les données de cache à partir du panneau Application de Microsoft Edge DevTools.
title: Afficher les données de cache avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 7e0523e3293bbdafa9c3575344714da708fffe62
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397537"
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

# <a name="view-cache-data-with-microsoft-edge-devtools"></a><span data-ttu-id="32a49-104">Afficher les données de cache avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="32a49-104">View cache data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="32a49-105">Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour inspecter les [données de cache.][MDNCache]</span><span class="sxs-lookup"><span data-stu-id="32a49-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="32a49-106">Si vous essayez d’inspecter les [données de cache HTTP,][MDNHTTPCaching] ce n’est pas le guide que vous souhaitez.</span><span class="sxs-lookup"><span data-stu-id="32a49-106">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  <span data-ttu-id="32a49-107">Recherchez les informations dans la colonne **Taille** du **journal réseau.**</span><span class="sxs-lookup"><span data-stu-id="32a49-107">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="32a49-108">Accédez à [Journal de l’activité réseau.][DevtoolsNetworkLogActivity]</span><span class="sxs-lookup"><span data-stu-id="32a49-108">Navigate to [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <a name="view-cache-data"></a><span data-ttu-id="32a49-109">Afficher les données de cache</span><span class="sxs-lookup"><span data-stu-id="32a49-109">View cache data</span></span>  

1.  <span data-ttu-id="32a49-110">Choisissez **l’onglet Application** pour ouvrir le **panneau Application.**</span><span class="sxs-lookup"><span data-stu-id="32a49-110">Choose the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="32a49-111">Le **volet Manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="32a49-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="32a49-113">Volet \*\*\*\* manifeste</span><span class="sxs-lookup"><span data-stu-id="32a49-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32a49-114">Développez la section **Stockage du cache** pour afficher les caches disponibles.</span><span class="sxs-lookup"><span data-stu-id="32a49-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Caches disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       <span data-ttu-id="32a49-116">Caches disponibles</span><span class="sxs-lookup"><span data-stu-id="32a49-116">Available caches</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32a49-117">Choisissez un cache pour afficher le contenu.</span><span class="sxs-lookup"><span data-stu-id="32a49-117">Choose a cache to view the contents.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Afficher le contenu d’un cache" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       <span data-ttu-id="32a49-119">Afficher le contenu d’un cache</span><span class="sxs-lookup"><span data-stu-id="32a49-119">View the contents of a cache</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32a49-120">Choisissez une ressource pour afficher les en-têtes HTTP dans la section sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="32a49-120">Choose a resource to view the HTTP headers in the section below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Afficher les en-têtes HTTP d’une ressource" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       <span data-ttu-id="32a49-122">Afficher les en-têtes HTTP d’une ressource</span><span class="sxs-lookup"><span data-stu-id="32a49-122">View the HTTP headers of a resource</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32a49-123">Sélectionnez **Aperçu** pour afficher le contenu d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="32a49-123">Choose **Preview** to view the content of a resource.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Afficher le contenu d’une ressource" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       <span data-ttu-id="32a49-125">Afficher le contenu d’une ressource</span><span class="sxs-lookup"><span data-stu-id="32a49-125">View the content of a resource</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a><span data-ttu-id="32a49-126">Actualiser une ressource</span><span class="sxs-lookup"><span data-stu-id="32a49-126">Refresh a resource</span></span>  

1.  <span data-ttu-id="32a49-127">[Afficher les données d’un cache.](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="32a49-127">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="32a49-128">Choisissez la ressource que vous souhaitez actualiser.</span><span class="sxs-lookup"><span data-stu-id="32a49-128">Choose the resource that you want to refresh.</span></span>  <span data-ttu-id="32a49-129">DevTools le met en sur évidence pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="32a49-129">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Choisir une ressource à actualiser" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       <span data-ttu-id="32a49-131">Choisir une ressource à actualiser</span><span class="sxs-lookup"><span data-stu-id="32a49-131">Choose a resource to refresh</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32a49-132">Choose **Refresh** \( ![ Refresh ][ImageRefreshIcon] \).</span><span class="sxs-lookup"><span data-stu-id="32a49-132">Choose **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <a name="filter-resources"></a><span data-ttu-id="32a49-133">Filtrer les ressources</span><span class="sxs-lookup"><span data-stu-id="32a49-133">Filter resources</span></span>  

1.  <span data-ttu-id="32a49-134">[Afficher les données d’un cache.](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="32a49-134">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="32a49-135">Utilisez la **zone de texte Filtrer par** chemin d’accès pour filtrer les ressources qui ne correspondent pas au chemin d’accès que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="32a49-135">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrer les ressources qui ne correspondent pas au chemin d’accès spécifié" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       <span data-ttu-id="32a49-137">Filtrer les ressources qui ne correspondent pas au chemin d’accès spécifié</span><span class="sxs-lookup"><span data-stu-id="32a49-137">Filter out resources that do not match the specified path</span></span>  
    :::image-end:::  
    
## <a name="delete-a-resource"></a><span data-ttu-id="32a49-138">Suppression d'une ressource</span><span class="sxs-lookup"><span data-stu-id="32a49-138">Delete a resource</span></span>  

1.  <span data-ttu-id="32a49-139">[Afficher les données d’un cache.](#view-cache-data)</span><span class="sxs-lookup"><span data-stu-id="32a49-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="32a49-140">Choisissez la ressource que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="32a49-140">Choose the resource that you want to delete.</span></span>  <span data-ttu-id="32a49-141">DevTools le met en sur évidence pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="32a49-141">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Choisir une ressource à supprimer" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       <span data-ttu-id="32a49-143">Choisir une ressource à supprimer</span><span class="sxs-lookup"><span data-stu-id="32a49-143">Choose a resource to delete</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32a49-144">Choose **Delete Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).</span><span class="sxs-lookup"><span data-stu-id="32a49-144">Choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <a name="delete-all-cache-data"></a><span data-ttu-id="32a49-145">Supprimer toutes les données de cache</span><span class="sxs-lookup"><span data-stu-id="32a49-145">Delete all cache data</span></span>  

1.  <span data-ttu-id="32a49-146">Ouvrez **Application**  >  **Clear Storage**.</span><span class="sxs-lookup"><span data-stu-id="32a49-146">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="32a49-147">Assurez-vous que la case **à cocher Stockage** du cache est activée.</span><span class="sxs-lookup"><span data-stu-id="32a49-147">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Case à cocher Stockage du cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       <span data-ttu-id="32a49-149">Case **à cocher Stockage** du cache</span><span class="sxs-lookup"><span data-stu-id="32a49-149">The **Cache Storage** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="32a49-150">Choisissez **Effacer les données de site.**</span><span class="sxs-lookup"><span data-stu-id="32a49-150">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       <span data-ttu-id="32a49-152">Bouton **Effacer les données du** site</span><span class="sxs-lookup"><span data-stu-id="32a49-152">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="32a49-153">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="32a49-153">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Journal de l’activité réseau | Documents Microsoft"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="32a49-158">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32a49-158">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="32a49-159">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cache) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="32a49-159">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="32a49-161">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="32a49-161">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
