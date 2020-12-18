---
description: Découvrez comment afficher les données du cache à partir du panneau application de Microsoft Edge DevTools.
title: Afficher les données du cache avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 770001beb9b7eebd4dae76355a1f3e41a8021ecb
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230802"
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

# Afficher les données du cache avec Microsoft Edge DevTools  

Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les données [du cache][MDNCache] .  

Si vous essayez d’inspecter les données [du cache http][MDNHTTPCaching] , il ne s’agit pas du guide souhaité.  Recherchez les informations dans la colonne **taille** du journal du **réseau**.  Naviguez jusqu’à [log Activity Network][DevtoolsNetworkLogActivity].  

## Afficher les données du cache  

1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **manifeste**  
    :::image-end:::  
    
1.  Développez la section **stockage du cache** pour afficher les caches disponibles.  
    
    :::image type="complex" source="../media/storage-application-cache-storage.msft.png" alt-text="Caches disponibles" lightbox="../media/storage-application-cache-storage.msft.png":::
       Caches disponibles  
    :::image-end:::  
    
1.  Sélectionnez un cache pour afficher le contenu.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-root-headers.msft.png" alt-text="Afficher le contenu d’un cache" lightbox="../media/storage-application-cache-storage-domain-root-headers.msft.png":::
       Afficher le contenu d’un cache  
    :::image-end:::  
    
1.  Sélectionnez une ressource pour afficher les en-têtes HTTP dans la section située sous le tableau.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-index-headers.msft.png" alt-text="Afficher les en-têtes HTTP d’une ressource" lightbox="../media/storage-application-cache-storage-index-headers.msft.png":::
       Afficher les en-têtes HTTP d’une ressource  
    :::image-end:::  
    
1.  Sélectionnez **Aperçu** pour afficher le contenu d’une ressource.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-js-preview.msft.png" alt-text="Afficher le contenu d’une ressource" lightbox="../media/storage-application-cache-storage-domain-js-preview.msft.png":::
       Afficher le contenu d’une ressource  
    :::image-end:::  
    
## Actualiser une ressource  

1.  [Afficher les données d’un cache](#view-cache-data).  
1.  Sélectionnez la ressource que vous voulez actualiser.  DevTools le met en surbrillance pour indiquer qu’il est sélectionné.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-domain-refresh.msft.png" alt-text="Sélectionner une ressource à actualiser" lightbox="../media/storage-application-cache-storage-domain-refresh.msft.png":::
       Sélectionner une ressource à actualiser  
    :::image-end:::  
    
1.  Cliquez sur **Actualiser** , puis sur ![ Actualiser ][ImageRefreshIcon] .  
    
## Filtrer les ressources  

1.  [Afficher les données d’un cache](#view-cache-data).  
1.  Utilisez la zone de texte **Filtrer par chemin** pour filtrer les ressources qui ne correspondent pas au chemin que vous fournissez.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-filter.msft.png" alt-text="Filtrer les ressources qui ne correspondent pas au chemin spécifié" lightbox="../media/storage-application-cache-storage-filter.msft.png":::
       Filtrer les ressources qui ne correspondent pas au chemin spécifié  
    :::image-end:::  
    
## Suppression d'une ressource  

1.  [Afficher les données d’un cache](#view-cache-data).  
1.  Sélectionnez la ressource que vous voulez supprimer.  DevTools le met en surbrillance pour indiquer qu’il est sélectionné.  
    
    :::image type="complex" source="../media/storage-application-cache-storage-delete-selected.msft.png" alt-text="Sélectionner une ressource à supprimer" lightbox="../media/storage-application-cache-storage-delete-selected.msft.png":::
       Sélectionner une ressource à supprimer  
    :::image-end:::  
    
1.  Sélectionnez **Supprimer la sélection** \ ( ![ Supprimer la sélection ][ImageDeleteIcon] \).  
    
## Supprimer toutes les données du cache  

1.  Ouvrez l' **application**  >  **Clear Storage**.  
1.  Vérifiez que la case à cocher **stockage du cache** est activée.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png" alt-text="Case à cocher stockage du cache" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox.msft.png":::
       Case à cocher **stockage du cache**  
    :::image-end:::  
    
1.  Sélectionnez **effacer les données du site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png":::
       Bouton **effacer les données du site**  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsNetworkLogActivity]: ../network/index.md#log-network-activity  "Journalisation de l’activité du réseau | Documents Microsoft"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cache) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
