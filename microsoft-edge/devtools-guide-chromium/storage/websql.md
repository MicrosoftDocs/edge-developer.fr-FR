---
description: Découvrez comment afficher les données SQL Web à partir du panneau application de Microsoft Edge DevTools.
title: Afficher des données SQL Web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: cc2f726c80fbf0c943b43ff6c131e9479db75b78
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993533"
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





# <span data-ttu-id="d6d22-104">Afficher des données SQL Web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d6d22-104">View Web SQL data with Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="d6d22-105">La spécification Web SQL n’est [pas conservée][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="d6d22-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="d6d22-106">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour inspecter les données SQL Web.</span><span class="sxs-lookup"><span data-stu-id="d6d22-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="d6d22-107">Afficher des données SQL Web</span><span class="sxs-lookup"><span data-stu-id="d6d22-107">View Web SQL Data</span></span>   

1.  <span data-ttu-id="d6d22-108">Sélectionnez l’onglet **sources** pour ouvrir le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="d6d22-108">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="d6d22-109">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="d6d22-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="d6d22-111">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="d6d22-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d6d22-112">Développez la section **SQL Web** pour afficher les bases de données et les tables.</span><span class="sxs-lookup"><span data-stu-id="d6d22-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="d6d22-113">Dans l’illustration ci-dessous, **html5meetup** est une base de données et les **salles** constituent une table.</span><span class="sxs-lookup"><span data-stu-id="d6d22-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Volet Web SQL" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="d6d22-115">Volet **Web SQL**</span><span class="sxs-lookup"><span data-stu-id="d6d22-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d6d22-116">Sélectionnez une table pour afficher les données de cette table.</span><span class="sxs-lookup"><span data-stu-id="d6d22-116">Select a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Afficher les données d’une table SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="d6d22-118">Afficher les données d’une table SQL Web</span><span class="sxs-lookup"><span data-stu-id="d6d22-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d6d22-119">Modifier des données SQL Web</span><span class="sxs-lookup"><span data-stu-id="d6d22-119">Edit Web SQL data</span></span>   

<span data-ttu-id="d6d22-120">Vous ne pouvez pas modifier les données SQL Web lors de l’affichage d’une table SQL Web, comme dans l' **illustration 3** ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="d6d22-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="d6d22-121">Toutefois, vous pouvez exécuter des instructions à partir de la console Web SQL qui modifient ou suppriment des tables.</span><span class="sxs-lookup"><span data-stu-id="d6d22-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="d6d22-122">Voir [exécuter des requêtes SQL Web](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="d6d22-122">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="d6d22-123">Exécuter des requêtes SQL Web</span><span class="sxs-lookup"><span data-stu-id="d6d22-123">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="d6d22-124">Sélectionner une base de données pour ouvrir la console de cette base de données.</span><span class="sxs-lookup"><span data-stu-id="d6d22-124">Select a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="d6d22-125">Tapez une instruction SQL Web, puis appuyez `Enter` dessus pour l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="d6d22-125">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Utiliser la console Web SQL pour supprimer une ligne d’un tableau" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="d6d22-127">Utiliser la console Web SQL pour supprimer une ligne d’un tableau</span><span class="sxs-lookup"><span data-stu-id="d6d22-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d6d22-128">Actualiser une table SQL Web</span><span class="sxs-lookup"><span data-stu-id="d6d22-128">Refresh a Web SQL table</span></span>   

<span data-ttu-id="d6d22-129">DevTools ne met pas à jour les tables en temps réel.</span><span class="sxs-lookup"><span data-stu-id="d6d22-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="d6d22-130">Pour mettre à jour les données d’une table:</span><span class="sxs-lookup"><span data-stu-id="d6d22-130">To update the data in a table:</span></span>  

1.  <span data-ttu-id="d6d22-131">[Afficher les données dans une table SQL Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="d6d22-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="d6d22-132">Sélectionnez **Actualiser** /actualiser ![ ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="d6d22-132">Select **Refresh** \(![Refresh][ImageRefreshIcon]\).</span></span>  
    
## <span data-ttu-id="d6d22-133">Filtrer les colonnes d’une table Web SQL</span><span class="sxs-lookup"><span data-stu-id="d6d22-133">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="d6d22-134">[Afficher les données dans une table SQL Web](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="d6d22-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="d6d22-135">Utilisez la zone de texte **colonnes visibles** pour spécifier les colonnes que vous voulez afficher.</span><span class="sxs-lookup"><span data-stu-id="d6d22-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="d6d22-136">Indiquez les noms des colonnes sous forme de liste CSV.</span><span class="sxs-lookup"><span data-stu-id="d6d22-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Utiliser la zone de texte colonnes visibles pour réduire le nombre de colonnes affichées" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="d6d22-138">Utiliser la zone de texte **colonnes visibles** pour réduire le nombre de colonnes affichées</span><span class="sxs-lookup"><span data-stu-id="d6d22-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d6d22-139">Supprimer toutes les données SQL Web</span><span class="sxs-lookup"><span data-stu-id="d6d22-139">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="d6d22-140">Ouvrir le volet de **stockage effacer** .</span><span class="sxs-lookup"><span data-stu-id="d6d22-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="d6d22-141">Assurez-vous que la case à cocher **SQL Web** est activée.</span><span class="sxs-lookup"><span data-stu-id="d6d22-141">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Case à cocher SQL Web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="d6d22-143">Case à cocher **SQL Web**</span><span class="sxs-lookup"><span data-stu-id="d6d22-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d6d22-144">Sélectionnez **effacer les données du site**.</span><span class="sxs-lookup"><span data-stu-id="d6d22-144">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="d6d22-146">Bouton **effacer les données du site**</span><span class="sxs-lookup"><span data-stu-id="d6d22-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRefreshIcon]: ../media/refresh-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de données SQL Web | W3C"  

> [!NOTE]
> <span data-ttu-id="d6d22-149">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6d22-149">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d6d22-150">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/websql) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="d6d22-150">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="d6d22-152">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d6d22-152">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
