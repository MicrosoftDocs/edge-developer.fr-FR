---
description: Découvrez comment afficher les SQL web à partir du panneau Application de Microsoft Edge DevTools.
title: Afficher les données de SQL web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 9f684aabf3592220079e6a8595d91cfea6785769
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439597"
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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a>Afficher les données de SQL web avec Microsoft Edge DevTools  

> [!WARNING]
> La spécification de SQL web [n’est pas conservée.][W3CWebSQLStatus]  

Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour inspecter les données SQL Web.  

## <a name="view-web-sql-data"></a>Afficher les données de SQL Web  

1.  Choisissez **l’outil Sources** pour ouvrir **l’outil Sources.**  Le **volet Manifeste** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **** manifeste  
    :::image-end:::  
    
1.  Développez la section **SQL** web pour afficher les bases de données et les tables.  Dans la figure suivante, sous **html5meetup** se trouve une base de données et **les salles** un tableau.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Volet De SQL Web" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       Volet **SQL** Web  
    :::image-end:::  
    
1.  Choisissez une table pour afficher les données de cette table.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Afficher les données d’une table de SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Afficher les données d’une table de SQL Web  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a>Modifier les données de SQL web  

Vous ne pouvez pas modifier les données de SQL web lors de l’affichage d’un tableau de SQL web, comme dans la version précédente.  Toutefois, vous pouvez exécuter des instructions à partir de la console web SQL qui modifient ou suppriment des tables.  Accédez à [Exécuter des requêtes SQL web.](#run-web-sql-queries)  

## <a name="run-web-sql-queries"></a>Exécuter des requêtes SQL web  

1.  Choisissez une base de données pour ouvrir une console pour cette base de données.  
1.  Tapez une instruction web SQL, puis `Enter` sélectionnez-la pour l’exécuter.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Utiliser la console web SQL pour supprimer une ligne d’un tableau" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Utiliser la console web SQL pour supprimer une ligne d’un tableau  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a>Actualiser une table de SQL Web  

DevTools ne met pas à jour les tables en temps réel.  Pour mettre à jour les données d’une table, effectuer les actions suivantes.  

1.  [Afficher les données dans une table de SQL Web.](#view-web-sql-data)  
1.  Choose **Refresh** \( ![ Refresh ](../media/refresh-icon.msft.png) \).  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a>Filtrer les colonnes dans un tableau de SQL Web  

1.  [Afficher les données dans une table de SQL Web.](#view-web-sql-data)  
1.  Utilisez la **zone de texte Colonnes** visibles pour spécifier les colonnes que vous souhaitez afficher.  Fournissez les noms des colonnes sous la mesure d’une liste CSV.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Utiliser la zone de texte Colonnes visibles pour réduire le nombre de colonnes affichées" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Utiliser la **zone de texte Colonnes** visibles pour réduire le nombre de colonnes affichées  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a>Supprimer toutes les données de SQL Web  

1.  Ouvrez **le volet** Effacer le stockage.  
1.  Assurez-vous que **la case à SQL** web est allumée.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Case à cocher SQL web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       Case **à cocher SQL** web  
    :::image-end:::  
    
1.  Choisissez **Effacer les données de site.**  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Bouton **Effacer les données du** site  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de données SQL web | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/websql) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
