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

# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a>Afficher les données du cache d'application avec Microsoft Edge DevTools  

> [!WARNING]
> L'API de cache [d'application est supprimée de la plateforme web.][HTMLStandardOfflineWebApplications]  

Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour inspecter les ressources [du cache d'applications.][MDNWebAPIsWindowApplicationCache]  

## <a name="view-application-cache-data"></a>Afficher les données du cache d'application  

1.  En haut de DevTools, choisissez **l'outil Application.**  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **** manifeste  
    :::image-end:::  

1.  Développez la section **Cache d'applications** et choisissez un cache pour afficher les ressources.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Volet Cache d'applications" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       Volet **Cache d'applications**  
    :::image-end:::  

Chaque ligne du tableau représente une ressource mise en cache.  

La **colonne Type** représente la catégorie de la [ressource.][MDNHTMLResourcesInAnApplicationCache]  

| Catégorie | Détails |  
|:--- |:--- |  
| `Explicit` | Cette ressource a été explicitement répertoriée dans le manifeste. |  
| `Fallback` | L'URL est un de base pour une autre ressource.  L'URL de l'autre ressource n'est pas répertoriée dans DevTools. |  
| `Master` | `manifest`L'attribut de la ressource indique que le cache est le parent de la ressource. |  
| `Network` | Le manifeste spécifie que la ressource doit être provenant du réseau. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

En bas du tableau se cachent des icônes d'état indiquant votre connexion réseau et l'état du **cache d'applications.**  Le **cache d'applications** peut avoir les états suivants.  

| État | Détails |  
|:--- |:--- |  
| `CHECKING` | Le manifeste est en cours d'extraction et a été vérifié pour les mises à jour. |  
| `DOWNLOADING` | Les ressources sont ajoutées au cache. |  
| `IDLE` | Aucune nouvelle modification n'est apportée au cache. |  
| `OBSOLETE` | Le cache est en cours de suppression. |  
| `UPDATEREADY` |  Une nouvelle version du cache est disponible. |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Applications Web hors connexion - Html Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressources dans un cache d'application | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache - Api web | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
