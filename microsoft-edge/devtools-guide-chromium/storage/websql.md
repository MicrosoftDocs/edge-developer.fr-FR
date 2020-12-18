---
description: Découvrez comment afficher les données SQL Web à partir du panneau application de Microsoft Edge DevTools.
title: Afficher des données SQL Web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 802f21cb4cadfa3ee08ddd8feeea8b8132551740
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231173"
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

# Afficher des données SQL Web avec Microsoft Edge DevTools  

> [!WARNING]
> La spécification Web SQL n’est [pas conservée][W3CWebSQLStatus].  

Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les données SQL Web.  

## Afficher des données SQL Web  

1.  Sélectionnez l’onglet **sources** pour ouvrir l’outil **sources** .  Le volet **manifeste** s’ouvre généralement par défaut.  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       Volet **manifeste**  
    :::image-end:::  
    
1.  Développez la section **SQL Web** pour afficher les bases de données et les tables.  Dans l’illustration ci-dessous, **html5meetup** est une base de données et les **salles** constituent une table.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Volet Web SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       Volet **Web SQL**  
    :::image-end:::  
    
1.  Sélectionnez une table pour afficher les données de cette table.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Afficher les données d’une table SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       Afficher les données d’une table SQL Web  
    :::image-end:::  
    
## Modifier des données SQL Web  

Vous ne pouvez pas modifier les données SQL Web lors de l’affichage d’une table SQL Web, comme ci-dessus.  Toutefois, vous pouvez exécuter des instructions à partir de la console Web SQL qui modifient ou suppriment des tables.  Voir [exécuter des requêtes SQL Web](#run-web-sql-queries).  

## Exécuter des requêtes SQL Web  

1.  Choisissez une base de données pour ouvrir la console de cette base de données.  
1.  Tapez une instruction SQL Web, puis sélectionnez `Enter` pour l’exécuter.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Utiliser la console Web SQL pour supprimer une ligne d’un tableau" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       Utiliser la console Web SQL pour supprimer une ligne d’un tableau  
    :::image-end:::  
    
## Actualiser une table SQL Web  

DevTools ne met pas à jour les tables en temps réel.  Pour mettre à jour les données d’une table, procédez comme suit.  

1.  [Afficher les données dans une table SQL Web](#view-web-sql-data).  
1.  Cliquez sur **Actualiser** , puis sur ![ Actualiser ][ImageRefreshIcon] .  
    
## Filtrer les colonnes d’une table Web SQL  

1.  [Afficher les données dans une table SQL Web](#view-web-sql-data).  
1.  Utilisez la zone de texte **colonnes visibles** pour spécifier les colonnes que vous voulez afficher.  Indiquez les noms des colonnes sous forme de liste CSV.  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Utiliser la zone de texte colonnes visibles pour réduire le nombre de colonnes affichées" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       Utiliser la zone de texte **colonnes visibles** pour réduire le nombre de colonnes affichées  
    :::image-end:::  
    
## Supprimer toutes les données SQL Web  

1.  Ouvrir le volet de **stockage effacer** .  
1.  Assurez-vous que la case à cocher **SQL Web** est activée.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Case à cocher SQL Web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       Case à cocher **SQL Web**  
    :::image-end:::  
    
1.  Sélectionnez **effacer les données du site**.  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       Bouton **effacer les données du site**  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de données SQL Web | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/websql) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
