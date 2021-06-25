---
description: Découvrez comment afficher les données du cache d’application à partir du panneau Application de Microsoft Edge DevTools.
title: Afficher les données du cache d’application Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 71e71555940d74f2071178be2e6daf0ec2f49dfd
ms.sourcegitcommit: d0a6959c5338cf1927093b4a9ed29a0bc0390b43
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "11615420"
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
# <a name="view-application-cache-data-with-microsoft-edge-devtools"></a>Afficher les données du cache d’application Microsoft Edge DevTools  

> [!WARNING]
> Le cache d’applications est supprimé et vous devez éviter de l’utiliser.  L’API de cache d’applications est supprimée de la plateforme web.  Pour plus d’informations, [accédez à Préparation de la suppression d’AppCache.][WebDevAppcacheRemoval]

Ce guide vous montre comment utiliser Microsoft Edge [DevTools pour][MicrosoftEdgeDevTools] inspecter les ressources [du cache d’applications.][MDNWebAPIsWindowApplicationCache]  

## <a name="view-application-cache-data"></a>Afficher les données du cache d’application  

1.  En haut de DevTools, choisissez **l’outil Application.**  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **** manifeste  
    :::image-end:::  

1.  Développez la section **Cache d’applications** et choisissez un cache pour afficher les ressources.  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Volet Cache d’applications" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       Volet **Cache d’applications**  
    :::image-end:::  

Chaque ligne du tableau représente une ressource mise en cache.  

La **colonne Type** représente la catégorie de la [ressource.][MDNHTMLResourcesInAnApplicationCache]  

| Catégorie | Détails |  
|:--- |:--- |  
| `Explicit` | Cette ressource a été explicitement répertoriée dans le manifeste. |  
| `Fallback` | L’URL est un de base pour une autre ressource.  L’URL de l’autre ressource n’est pas répertoriée dans DevTools. |  
| `Master` | `manifest`L’attribut de la ressource indique que le cache est le parent de la ressource. |  
| `Network` | Le manifeste spécifie que la ressource doit être provenant du réseau. |  

<!--todo:  replace "Master" phrasing if possible.  -->  

En bas du tableau se cachent des icônes d’état indiquant votre connexion réseau et l’état du **cache d’applications.**  Le **cache d’applications** peut avoir les états suivants.  

| État | Détails |  
|:--- |:--- |  
| `CHECKING` | Le manifeste est extrait et les mises à jour sont vérifiées. |  
| `DOWNLOADING` | Des ressources sont ajoutées au cache. |  
| `IDLE` | Le cache n’a pas de nouvelles modifications. |  
| `OBSOLETE` | Le cache est en cours de suppression. |  
| `UPDATEREADY` |  Une nouvelle version du cache est disponible. |  

<!-- links -->  
[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  
<!-- external links: -->
[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ressources dans un cache d’application | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window.applicationCache - Api web | MDN"  

[WebDevAppcacheRemoval]: https://web.dev/appcache-removal "Préparation de la suppression d’AppCache | web.dev"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
