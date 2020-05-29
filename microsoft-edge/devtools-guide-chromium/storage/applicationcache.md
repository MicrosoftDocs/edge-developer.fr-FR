---
title: Afficher les données du cache d’application avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 6ce3087e9c719efbcf4d9ebceb860edd0ed0c3b6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612094"
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





# Afficher les données du cache d’application avec Microsoft Edge DevTools   



> [!WARNING]
> L’API du cache d’application est [supprimée de la plateforme Web][HTMLStandardOfflineWebApplications].  

Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les ressources [du cache d’applications][MDNWebAPIsWindowApplicationCache] .  

## Afficher les données du cache d’application   

1.  Sélectionnez l’onglet **sources** pour ouvrir le panneau **sources** .  Le volet **manifeste** s’ouvre généralement par défaut.  
    
    > ##### Figure1  
    > Volet manifeste  
    > ![Volet manifeste][ImageManifestPane]  

1.  Développez la section cache de l' **application** , puis cliquez sur un cache pour afficher les ressources.  
    
    > ##### Figure 2  
    > Volet cache de l’application  
    > ![Volet cache de l’application][ImageApplicationCachePane]  

Chaque ligne de la table représente une ressource mise en cache.  

La colonne **type** représente la [catégorie de la ressource][MDNHTMLResourcesInAnApplicationCache].  

| Catégorie | Détails |  
|:--- |:--- |  
| `Explicit` | Cette ressource a été explicitement répertoriée dans le manifeste. |  
| `Fallback` | L’URL est une alternative pour une autre ressource.  L’URL de l’autre ressource n’est pas répertoriée dans DevTools. |  
| `Master` | L' `manifest` attribut de la ressource indique que ce cache est le parent de la ressource. |  
| `Network` | Le manifeste indiqué que cette ressource doit provenir du réseau. |  

En bas du tableau figure il existe des icônes de statut indiquant votre connexion réseau et l’état du cache de l’application.  Le cache de l’application doit présenter les États suivants.  

| État | Détails |  
|:--- |:--- |  
| `CHECKING` | Le manifeste est en cours de lecture et vérifie les mises à jour. |  
| `DOWNLOADING` | Les ressources sont ajoutées au cache. |  
| `IDLE` | Le cache ne comporte pas de nouvelles modifications. |  
| `OBSOLETE` | Le cache est en cours de suppression. |  
| `UPDATEREADY` |  Une nouvelle version du cache est disponible. |  

<!--   -->  



<!-- image links -->  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageApplicationCachePane]: /microsoft-edge/devtools-guide-chromium/media/storage-cache-pane-cache-storage-resources.msft.png "Figure 2: volet de cache de l’application"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Applications Web hors connexion-norme HTML"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressources dans le cache de l’application | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-API Web | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
