---
title: Afficher les données du cache avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612073"
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

Si vous essayez d’inspecter les données [du cache http][MDNHTTPCaching] , il ne s’agit pas du guide souhaité.  
Recherchez les informations dans la colonne **taille** du journal du **réseau**.  Voir [enregistrement][DevtoolsNetworkLogActivity]de l’activité du réseau.  

## Afficher les données du cache   

1.  Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .  Le volet **manifeste** s’ouvre généralement par défaut.  
    
    > ##### Figure1  
    > Volet manifeste  
    > ![Volet manifeste][ImageManifestPane]  

1.  Développez la section **stockage du cache** pour afficher les caches disponibles.  
    
    > ##### Figure 2  
    > Caches disponibles  
    > ![Caches disponibles][ImageCache]  

1.  Sélectionnez un cache pour afficher le contenu.  
    
    > ##### Figure3  
    > Affichage du contenu d’un cache  
    > ![Affichage du contenu d’un cache][ImageCacheView]  

1.  Sélectionnez une ressource pour afficher les en-têtes HTTP dans la section située sous le tableau.  
    
    > ##### Figure 4  
    > Affichage des en-têtes HTTP d’une ressource  
    > ![Affichage des en-têtes HTTP d’une ressource][ImageViewCacheResource]  

1.  Sélectionnez **Aperçu** pour afficher le contenu d’une ressource.  
    
    > ##### Figure 5  
    > Affichage du contenu d’une ressource  
    > ![Affichage du contenu d’une ressource][ImageCacheContent]  

## Actualiser une ressource   

1.  [Afficher les données d’un cache](#view-cache-data).  
1.  Sélectionnez la ressource que vous voulez actualiser.  DevTools le met en surbrillance pour indiquer qu’il est sélectionné.  
    
    > ##### Figure 6  
    > Sélection d’une ressource  
    > ![Sélection d’une ressource][ImageCacheSelected]  

1.  Sélectionnez **Actualiser** l' ![ actualisation ][ImageRefreshIcon] .  

## Filtrer les ressources   

1.  [Afficher les données d’un cache](#view-cache-data).  
1.  Utilisez la zone de texte **Filtrer par chemin** pour filtrer les ressources qui ne correspondent pas au chemin que vous fournissez.  
    
    > ##### Figure 7  
    > Filtrage des ressources qui ne correspondent pas au chemin spécifié  
    > ![Filtrage des ressources qui ne correspondent pas au chemin spécifié][ImageCacheFilter]  

## Suppression d'une ressource   

1.  [Afficher les données d’un cache](#view-cache-data).  
1.  Sélectionnez la ressource que vous voulez supprimer.  DevTools le met en surbrillance pour indiquer qu’il est sélectionné.  
    
    > ##### Figure8  
    > Sélection d’une ressource  
    > ![Sélection d’une ressource][ImageCacheSelected2]  

1.  Sélectionnez **supprimer** la ![ suppression sélectionnée ][ImageDeleteIcon] .  

## Supprimer toutes les données du cache   

1.  Ouvrez l' **application**  >  **Clear Storage**.  
1.  Vérifiez que la case à cocher **stockage du cache** est activée.  
    
    > ##### Figure9  
    > Case à cocher **stockage du cache**  
    > ![Case à cocher stockage du cache][ImageCacheCheckbox]  

1.  Sélectionnez **effacer les données du site**.  
    
    > ##### Figure10  
    > Bouton **effacer les données du site**  
    > ![Bouton Effacer les données du site][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Figure 2: caches disponibles"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Figure 3: affichage du contenu d’un cache"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Figure 4: affichage des en-têtes HTTP d’une ressource"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Figure 5: affichage du contenu d’une ressource"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Figure 6: sélectionner une ressource"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Figure 7: filtrage des ressources qui ne correspondent pas au chemin spécifié"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Figure 8: sélectionner une ressource"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Figure 9: case à cocher stockage du cache"  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Figure 10: bouton Effacer les données du site"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Journalisation de l’activité du réseau"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/cache) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
