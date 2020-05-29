---
title: Afficher des données SQL Web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 7a1e3e47f6761cfdb23488683107ed0df6a8f4e2
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612059"
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

1.  Sélectionnez l’onglet **sources** pour ouvrir le panneau **sources** .  Le volet **manifeste** s’ouvre généralement par défaut.  
    
    > ##### Figure1  
    > Volet manifeste  
    > ![Volet manifeste][ImageManifestPane]  
    
1.  Développez la section **SQL Web** pour afficher les bases de données et les tables.  Dans la [figure 2](#figure-2) située sous **html5meetup** , une base de données et des **salles** constituent une table.  
    
    > ##### Figure 2  
    > Volet Web SQL  
    > ![Volet Web SQL][ImageWebSQLPane]  

1.  Sélectionnez une table pour afficher les données de cette table.  
    
    > ##### Figure3  
    > Affichage des données de la table Web de **salles**  
    > ![Affichage des données d’une table SQL Web][ImageWebSQLTable]  

## Modifier des données SQL Web   

Vous ne pouvez pas modifier les données SQL Web lors de l’affichage d’une table SQL Web, comme dans l' **illustration 3** ci-dessus.  Toutefois, vous pouvez exécuter des instructions à partir de la console Web SQL qui modifient ou suppriment des tables.  Voir [exécuter des requêtes SQL Web](#run-web-sql-queries).  

## Exécuter des requêtes SQL Web   

1.  Sélectionner une base de données pour ouvrir la console de cette base de données.  

1.  Tapez une instruction SQL Web, puis appuyez `Enter` dessus pour l’exécuter.  
    
    > ##### Figure 4  
    > Utilisation de la console Web SQL pour supprimer une ligne de la table **salles**  
    > ![Utiliser la console Web SQL pour supprimer une ligne d’un tableau][ImageWebSQLEdit]  

## Actualiser une table SQL Web   

DevTools ne met pas à jour les tables en temps réel.  Pour mettre à jour les données d’une table:  

1.  [Afficher les données dans une table SQL Web](#view-web-sql-data).  
1.  Sélectionnez **Actualiser** l' ![ actualisation ][ImageRefreshIcon] .  

## Filtrer les colonnes d’une table Web SQL   

1.  [Afficher les données dans une table SQL Web](#view-web-sql-data).  
1.  Utilisez la zone de texte **colonnes visibles** pour spécifier les colonnes que vous voulez afficher.  Indiquez les noms des colonnes sous forme de liste CSV.  
    
    > ##### Figure 5  
    > Utilisation de la zone de texte **colonnes visibles** pour afficher uniquement les `room_name` `last_updated` colonnes et  
    > ![Utilisation de la zone de texte colonnes visibles pour réduire le nombre de colonnes affichées][ImageWebSQLFilter]  

## Supprimer toutes les données SQL Web   

1.  Ouvrir le volet de **stockage effacer** .  
1.  Assurez-vous que la case à cocher **SQL Web** est activée.  
    
    > ##### Figure 6  
    > Case à cocher **SQL Web**  
    > ![Case à cocher SQL Web][ImageWebSQLCheckbox]  

1.  Sélectionnez **effacer les données du site**.  
    
    > ##### Figure 7  
    > Bouton **effacer les données du site**  
    > ![Bouton Effacer les données du site][ImageClearWebSQL]  

 



<!-- image links -->  

[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Figure 1: volet manifeste"  
[ImageWebSQLPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql.msft.png "Figure 2: volet Web SQL"  
[ImageWebSQLTable]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png "Figure 3: affichage des données d’une table SQL Web"  
[ImageWebSQLEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-commands.msft.png "Figure 4: utilisation de la console Web SQL pour supprimer une ligne d’un tableau"  
[ImageWebSQLFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png "Figure 5: utilisation de la zone de texte colonnes visibles pour réduire le nombre de colonnes affichées"  
[ImageWebSQLCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-web-sql.msft.png "Figure 6: case à cocher SQL Web"  
[ImageClearWebSQL]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-clear-site-data-button.msft.png "Figure 7: bouton Effacer les données du site"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de données SQL Web | W3C"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/websql) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
