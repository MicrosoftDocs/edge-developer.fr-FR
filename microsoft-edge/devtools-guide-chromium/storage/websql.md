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

# <a name="view-web-sql-data-with-microsoft-edge-devtools"></a><span data-ttu-id="5de64-104">Afficher les données de SQL web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5de64-104">View Web SQL data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="5de64-105">La spécification de SQL web [n’est pas conservée.][W3CWebSQLStatus]</span><span class="sxs-lookup"><span data-stu-id="5de64-105">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="5de64-106">Ce guide vous montre comment utiliser [Microsoft Edge DevTools][MicrosoftEdgeDevTools] pour inspecter les données SQL Web.</span><span class="sxs-lookup"><span data-stu-id="5de64-106">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <a name="view-web-sql-data"></a><span data-ttu-id="5de64-107">Afficher les données de SQL Web</span><span class="sxs-lookup"><span data-stu-id="5de64-107">View Web SQL Data</span></span>  

1.  <span data-ttu-id="5de64-108">Choisissez **l’outil Sources** pour ouvrir **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="5de64-108">Choose the **Sources** tool to open the **Sources** tool.</span></span>  <span data-ttu-id="5de64-109">Le **volet Manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="5de64-109">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="5de64-111">Volet  manifeste</span><span class="sxs-lookup"><span data-stu-id="5de64-111">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5de64-112">Développez la section **SQL** web pour afficher les bases de données et les tables.</span><span class="sxs-lookup"><span data-stu-id="5de64-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="5de64-113">Dans la figure suivante, sous **html5meetup** se trouve une base de données et **les salles** un tableau.</span><span class="sxs-lookup"><span data-stu-id="5de64-113">In the following figure, below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql.msft.png" alt-text="Volet De SQL Web" lightbox="../media/storage-application-storage-web-sql.msft.png":::
       <span data-ttu-id="5de64-115">Volet **SQL** Web</span><span class="sxs-lookup"><span data-stu-id="5de64-115">The **Web SQL** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5de64-116">Choisissez une table pour afficher les données de cette table.</span><span class="sxs-lookup"><span data-stu-id="5de64-116">Choose a table to view the data for that table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png" alt-text="Afficher les données d’une table de SQL Web" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png":::
       <span data-ttu-id="5de64-118">Afficher les données d’une table de SQL Web</span><span class="sxs-lookup"><span data-stu-id="5de64-118">View the data of a Web SQL table</span></span>  
    :::image-end:::  
    
## <a name="edit-web-sql-data"></a><span data-ttu-id="5de64-119">Modifier les données de SQL web</span><span class="sxs-lookup"><span data-stu-id="5de64-119">Edit Web SQL data</span></span>  

<span data-ttu-id="5de64-120">Vous ne pouvez pas modifier les données de SQL web lors de l’affichage d’un tableau de SQL web, comme dans la version précédente.</span><span class="sxs-lookup"><span data-stu-id="5de64-120">You are not able to edit Web SQL data when viewing a Web SQL table, such as in previous above.</span></span>  <span data-ttu-id="5de64-121">Toutefois, vous pouvez exécuter des instructions à partir de la console web SQL qui modifient ou suppriment des tables.</span><span class="sxs-lookup"><span data-stu-id="5de64-121">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="5de64-122">Accédez à [Exécuter des requêtes SQL web.](#run-web-sql-queries)</span><span class="sxs-lookup"><span data-stu-id="5de64-122">Navigate to [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <a name="run-web-sql-queries"></a><span data-ttu-id="5de64-123">Exécuter des requêtes SQL web</span><span class="sxs-lookup"><span data-stu-id="5de64-123">Run Web SQL queries</span></span>  

1.  <span data-ttu-id="5de64-124">Choisissez une base de données pour ouvrir une console pour cette base de données.</span><span class="sxs-lookup"><span data-stu-id="5de64-124">Choose a database to open a console for that database.</span></span>  
1.  <span data-ttu-id="5de64-125">Tapez une instruction web SQL, puis `Enter` sélectionnez-la pour l’exécuter.</span><span class="sxs-lookup"><span data-stu-id="5de64-125">Type a Web SQL statement, then select `Enter` to run it.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png" alt-text="Utiliser la console web SQL pour supprimer une ligne d’un tableau" lightbox="../media/storage-application-storage-web-sql-html5meetup-commands.msft.png":::
       <span data-ttu-id="5de64-127">Utiliser la console web SQL pour supprimer une ligne d’un tableau</span><span class="sxs-lookup"><span data-stu-id="5de64-127">Use the Web SQL Console to delete a row from a table</span></span>  
    :::image-end:::  
    
## <a name="refresh-a-web-sql-table"></a><span data-ttu-id="5de64-128">Actualiser une table de SQL Web</span><span class="sxs-lookup"><span data-stu-id="5de64-128">Refresh a Web SQL table</span></span>  

<span data-ttu-id="5de64-129">DevTools ne met pas à jour les tables en temps réel.</span><span class="sxs-lookup"><span data-stu-id="5de64-129">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="5de64-130">Pour mettre à jour les données d’une table, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="5de64-130">To update the data in a table, complete the following actions.</span></span>  

1.  <span data-ttu-id="5de64-131">[Afficher les données dans une table de SQL Web.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="5de64-131">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5de64-132">Choose **Refresh** \( ![ Refresh ](../media/refresh-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="5de64-132">Choose **Refresh** \(![Refresh](../media/refresh-icon.msft.png)\).</span></span>  
    
## <a name="filter-out-columns-in-a-web-sql-table"></a><span data-ttu-id="5de64-133">Filtrer les colonnes dans un tableau de SQL Web</span><span class="sxs-lookup"><span data-stu-id="5de64-133">Filter out columns in a Web SQL table</span></span>  

1.  <span data-ttu-id="5de64-134">[Afficher les données dans une table de SQL Web.](#view-web-sql-data)</span><span class="sxs-lookup"><span data-stu-id="5de64-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5de64-135">Utilisez la **zone de texte Colonnes** visibles pour spécifier les colonnes que vous souhaitez afficher.</span><span class="sxs-lookup"><span data-stu-id="5de64-135">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="5de64-136">Fournissez les noms des colonnes sous la mesure d’une liste CSV.</span><span class="sxs-lookup"><span data-stu-id="5de64-136">Provide the column names as a CSV list.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png" alt-text="Utiliser la zone de texte Colonnes visibles pour réduire le nombre de colonnes affichées" lightbox="../media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png":::
       <span data-ttu-id="5de64-138">Utiliser la **zone de texte Colonnes** visibles pour réduire le nombre de colonnes affichées</span><span class="sxs-lookup"><span data-stu-id="5de64-138">Use the **Visible Columns** text box to reduce the number of columns shown</span></span>  
    :::image-end:::  
    
## <a name="delete-all-web-sql-data"></a><span data-ttu-id="5de64-139">Supprimer toutes les données de SQL Web</span><span class="sxs-lookup"><span data-stu-id="5de64-139">Delete all Web SQL data</span></span>  

1.  <span data-ttu-id="5de64-140">Ouvrez **le volet** Effacer le stockage.</span><span class="sxs-lookup"><span data-stu-id="5de64-140">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="5de64-141">Assurez-vous que **la case à SQL** web est allumée.</span><span class="sxs-lookup"><span data-stu-id="5de64-141">Make sure that the **Web SQL** checkbox is turned on.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-web-sql.msft.png" alt-text="Case à cocher SQL web" lightbox="../media/storage-application-clear-storage-web-sql.msft.png":::
       <span data-ttu-id="5de64-143">Case **à cocher SQL** web</span><span class="sxs-lookup"><span data-stu-id="5de64-143">The **Web SQL** checkbox</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5de64-144">Choisissez **Effacer les données de site.**</span><span class="sxs-lookup"><span data-stu-id="5de64-144">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-clear-site-data-button.msft.png" alt-text="Bouton Effacer les données du site" lightbox="../media/storage-application-clear-storage-clear-site-data-button.msft.png":::
       <span data-ttu-id="5de64-146">Bouton **Effacer les données du** site</span><span class="sxs-lookup"><span data-stu-id="5de64-146">The **Clear Site Data** button</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="5de64-147">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="5de64-147">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "Base de données SQL web | W3C"  

> [!NOTE]
> <span data-ttu-id="5de64-150">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5de64-150">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5de64-151">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/websql) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="5de64-151">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="5de64-153">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5de64-153">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
