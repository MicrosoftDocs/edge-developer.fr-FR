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

# <a name="view-cache-data-with-microsoft-edge-devtools"></a>Afficher les données de cache avec Microsoft Edge DevTools  

Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour inspecter les [données de cache.][MDNCache]  

Si vous essayez d’inspecter les [données de cache HTTP,][MDNHTTPCaching] ce n’est pas le guide que vous souhaitez.  Recherchez les informations dans la colonne **Taille** du **journal réseau.**  Accédez à [Journal de l’activité réseau.][DevtoolsNetworkLogActivity]  

## <a name="view-cache-data"></a>Afficher les données de cache  

1.  Choisissez **l’onglet Application** pour ouvrir le **panneau Application.**  Le **volet Manifeste** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **** manifeste  
    :::image-end:::  
    
1.  Développez la section **Stockage du cache** pour afficher les caches disponibles.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Caches disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       Caches disponibles  
    :::image-end:::  
    
1.  Choisissez un cache pour afficher le contenu.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Afficher le contenu d’un cache" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Afficher le contenu d’un cache  
    :::image-end:::  
    
1.  Choisissez une ressource pour afficher les en-têtes HTTP dans la section sous le tableau.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Afficher les en-têtes HTTP d’une ressource" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Afficher les en-têtes HTTP d’une ressource  
    :::image-end:::  
    
1.  Sélectionnez **Aperçu** pour afficher le contenu d’une ressource.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Afficher le contenu d’une ressource" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Afficher le contenu d’une ressource  
    :::image-end:::  
    
## <a name="refresh-a-resource"></a>Actualiser une ressource  

1.  [Afficher les données d’un cache.](#view-cache-data)  
1.  Choisissez la ressource que vous souhaitez actualiser.  DevTools le met en sur évidence pour indiquer qu’il est sélectionné.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Choisir une ressource à actualiser" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Choisir une ressource à actualiser  
    :::image-end:::  
    
1.  Choose **Refresh** \( ![ Refresh ][ImageRefreshIcon] \).  
    
## <a name="filter-resources"></a>Filtrer les ressources  

1.  [Afficher les données d’un cache.](#view-cache-data)  
1.  Utilisez la **zone de texte Filtrer par** chemin d’accès pour filtrer les ressources qui ne correspondent pas au chemin d’accès que vous fournissez.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrer les ressources qui ne correspondent pas au chemin d’accès spécifié" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtrer les ressources qui ne correspondent pas au chemin d’accès spécifié  
    :::image-end:::  
    
## <a name="delete-a-resource"></a>Suppression d'une ressource  

1.  [Afficher les données d’un cache.](#view-cache-data)  
1.  Choisissez la ressource que vous souhaitez supprimer.  DevTools le met en sur évidence pour indiquer qu’il est sélectionné.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Choisir une ressource à supprimer" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Choisir une ressource à supprimer  
    :::image-end:::  
    
1.  Choose **Delete Selected** \( ![ Delete Selected ][ImageDeleteIcon] \).  
    
## <a name="delete-all-cache-data"></a>Supprimer toutes les données de cache  

1.  Ouvrez **Application**  >  **Clear Storage**.  
1.  Assurez-vous que la case **à cocher Stockage** du cache est activée.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Case à cocher Stockage du cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Case **à cocher Stockage** du cache  
    :::image-end:::  
    
1.  Choisissez **Effacer les données de site.**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Bouton **Effacer les données du** site  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

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
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cache) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
