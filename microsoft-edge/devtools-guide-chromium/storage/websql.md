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





# <span data-ttu-id="c2467-103">Afficher des données SQL Web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c2467-103">View Web SQL Data With Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="c2467-104">La spécification Web SQL n’est [pas conservée][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="c2467-104">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="c2467-105">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les données SQL Web.</span><span class="sxs-lookup"><span data-stu-id="c2467-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="c2467-106">Afficher des données SQL Web</span><span class="sxs-lookup"><span data-stu-id="c2467-106">View Web SQL Data</span></span>   

1.  <span data-ttu-id="c2467-107">Sélectionnez l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="c2467-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="c2467-108">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2467-108">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="c2467-109">Figure1</span><span class="sxs-lookup"><span data-stu-id="c2467-109">Figure 1</span></span>  
    > <span data-ttu-id="c2467-110">Volet manifeste</span><span class="sxs-lookup"><span data-stu-id="c2467-110">The Manifest pane</span></span>  
    > ![Volet manifeste][ImageManifestPane]  
    
1.  <span data-ttu-id="c2467-112">Développez la section **SQL Web** pour afficher les bases de données et les tables.</span><span class="sxs-lookup"><span data-stu-id="c2467-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="c2467-113">Dans la [figure 2](#figure-2) située sous **html5meetup** , une base de données et des **salles** constituent une table.</span><span class="sxs-lookup"><span data-stu-id="c2467-113">In [Figure 2](#figure-2) below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    > ##### <span data-ttu-id="c2467-114">Figure 2</span><span class="sxs-lookup"><span data-stu-id="c2467-114">Figure 2</span></span>  
    > <span data-ttu-id="c2467-115">Volet Web SQL</span><span class="sxs-lookup"><span data-stu-id="c2467-115">The Web SQL pane</span></span>  
    > ![Volet Web SQL][ImageWebSQLPane]  

1.  <span data-ttu-id="c2467-117">Sélectionnez une table pour afficher les données de cette table.</span><span class="sxs-lookup"><span data-stu-id="c2467-117">Select a table to view the data for that table.</span></span>  
    
    > ##### <span data-ttu-id="c2467-118">Figure3</span><span class="sxs-lookup"><span data-stu-id="c2467-118">Figure 3</span></span>  
    > <span data-ttu-id="c2467-119">Affichage des données de la table Web de **salles**</span><span class="sxs-lookup"><span data-stu-id="c2467-119">Viewing the data of the **rooms** Web SQL table</span></span>  
    > ![Affichage des données d’une table SQL Web][ImageWebSQLTable]  

## <span data-ttu-id="c2467-121">Modifier des données SQL Web</span><span class="sxs-lookup"><span data-stu-id="c2467-121">Edit Web SQL data</span></span>   

<span data-ttu-id="c2467-122">Vous ne pouvez pas modifier les données SQL Web lors de l’affichage d’une table SQL Web, comme dans l' **illustration 3** ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="c2467-122">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="c2467-123">Toutefois, vous pouvez exécuter des instructions à partir de la console Web SQL qui modifient ou suppriment des tables.</span><span class="sxs-lookup"><span data-stu-id="c2467-123">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="c2467-124">Voir [exécuter des requêtes SQL Web](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="c2467-124">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="c2467-125">Exécuter des requêtes SQL Web</span><span class="sxs-lookup"><span data-stu-id="c2467-125">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="c2467-126">Sélectionner une base de données pour ouvrir la console de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="c2467-126">Select a database to open a console for that database.</span></span>  

1.  <span data-ttu-id="c2467-127">Tapez une instruction SQL Web, puis appuyez `Enter` dessus pour l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="c2467-127">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    > ##### <span data-ttu-id="c2467-128">Figure 4</span><span class="sxs-lookup"><span data-stu-id="c2467-128">Figure 4</span></span>  
    > <span data-ttu-id="c2467-129">Utilisation de la console Web SQL pour supprimer une ligne de la table **salles**</span><span class="sxs-lookup"><span data-stu-id="c2467-129">Using the Web SQL Console to delete a row from the **rooms** table</span></span>  
    > ![Utiliser la console Web SQL pour supprimer une ligne d’un tableau][ImageWebSQLEdit]  

## <span data-ttu-id="c2467-131">Actualiser une table SQL Web</span><span class="sxs-lookup"><span data-stu-id="c2467-131">Refresh a Web SQL table</span></span>   

<span data-ttu-id="c2467-132">DevTools ne met pas à jour les tables en temps réel.</span><span class="sxs-lookup"><span data-stu-id="c2467-132">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="c2467-133">Pour mettre à jour les données d’une table:</span><span class="sxs-lookup"><span data-stu-id="c2467-133">To update the data in a table:</span></span>  

1.  <span data-ttu-id="c2467-134">[Afficher les données dans une table SQL Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="c2467-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="c2467-135">Sélectionnez **Actualiser** l' ![ actualisation ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="c2467-135">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="c2467-136">Filtrer les colonnes d’une table Web SQL</span><span class="sxs-lookup"><span data-stu-id="c2467-136">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="c2467-137">[Afficher les données dans une table SQL Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="c2467-137">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="c2467-138">Utilisez la zone de texte **colonnes visibles** pour spécifier les colonnes que vous voulez afficher.</span><span class="sxs-lookup"><span data-stu-id="c2467-138">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="c2467-139">Indiquez les noms des colonnes sous forme de liste CSV.</span><span class="sxs-lookup"><span data-stu-id="c2467-139">Provide the column names as a CSV list.</span></span>  
    
    > ##### <span data-ttu-id="c2467-140">Figure 5</span><span class="sxs-lookup"><span data-stu-id="c2467-140">Figure 5</span></span>  
    > <span data-ttu-id="c2467-141">Utilisation de la zone de texte **colonnes visibles** pour afficher uniquement les `room_name` `last_updated` colonnes et</span><span class="sxs-lookup"><span data-stu-id="c2467-141">Using the **Visible Columns** text box to only show the `room_name` and `last_updated` columns</span></span>  
    > ![Utilisation de la zone de texte colonnes visibles pour réduire le nombre de colonnes affichées][ImageWebSQLFilter]  

## <span data-ttu-id="c2467-143">Supprimer toutes les données SQL Web</span><span class="sxs-lookup"><span data-stu-id="c2467-143">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="c2467-144">Ouvrir le volet de **stockage effacer** .</span><span class="sxs-lookup"><span data-stu-id="c2467-144">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="c2467-145">Assurez-vous que la case à cocher **SQL Web** est activée.</span><span class="sxs-lookup"><span data-stu-id="c2467-145">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="c2467-146">Figure 6</span><span class="sxs-lookup"><span data-stu-id="c2467-146">Figure 6</span></span>  
    > <span data-ttu-id="c2467-147">Case à cocher **SQL Web**</span><span class="sxs-lookup"><span data-stu-id="c2467-147">The **Web SQL** checkbox</span></span>  
    > ![Case à cocher SQL Web][ImageWebSQLCheckbox]  

1.  <span data-ttu-id="c2467-149">Sélectionnez **effacer les données du site**.</span><span class="sxs-lookup"><span data-stu-id="c2467-149">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="c2467-150">Figure 7</span><span class="sxs-lookup"><span data-stu-id="c2467-150">Figure 7</span></span>  
    > <span data-ttu-id="c2467-151">Bouton **effacer les données du site**</span><span class="sxs-lookup"><span data-stu-id="c2467-151">The **Clear Site Data** button</span></span>  
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
> <span data-ttu-id="c2467-162">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c2467-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c2467-163">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/websql) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="c2467-163">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="c2467-165">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c2467-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
