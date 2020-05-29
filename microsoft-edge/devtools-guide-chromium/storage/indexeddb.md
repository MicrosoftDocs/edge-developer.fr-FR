---
title: Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612087"
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





# <span data-ttu-id="45f8d-103">Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="45f8d-103">View And Change IndexedDB Data With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="45f8d-104">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher et modifier des données [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="45f8d-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="45f8d-105">Il part du principe que vous êtes familiarisé avec DevTools.</span><span class="sxs-lookup"><span data-stu-id="45f8d-105">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="45f8d-106">Il suppose également que vous êtes familiarisé avec IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="45f8d-106">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="45f8d-107">Si ce n’est pas le cas, voir [utilisation de IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="45f8d-107">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="45f8d-108">Afficher les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-108">View IndexedDB data</span></span>   

1.  <span data-ttu-id="45f8d-109">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="45f8d-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="45f8d-110">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="45f8d-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="45f8d-111">Figure1</span><span class="sxs-lookup"><span data-stu-id="45f8d-111">Figure 1</span></span>  
    > <span data-ttu-id="45f8d-112">Volet manifeste</span><span class="sxs-lookup"><span data-stu-id="45f8d-112">The Manifest pane</span></span>  
    > ![Volet manifeste][ImageManifest]  

1.  <span data-ttu-id="45f8d-114">Développez le menu **IndexedDB** pour afficher les bases de données disponibles.</span><span class="sxs-lookup"><span data-stu-id="45f8d-114">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    > ##### <span data-ttu-id="45f8d-115">Figure 2</span><span class="sxs-lookup"><span data-stu-id="45f8d-115">Figure 2</span></span>  
    > <span data-ttu-id="45f8d-116">Menu de **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="45f8d-116">The **IndexedDB** menu</span></span>  
    > ![Menu de IndexedDB][ImageIndexedDBMenu]  
    
    *   ![<span data-ttu-id="45f8d-118">Icône de base de données ][ImageDatabaseIcon] `notes - https://mdn.github.io` représente une base de données, où `notes` est le nom de la base de données et `https://mdn.github.io` est l’origine qui accède à la base de données.</span><span class="sxs-lookup"><span data-stu-id="45f8d-118">Database icon][ImageDatabaseIcon] `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   ![<span data-ttu-id="45f8d-119">L’icône magasin ][ImageObjectStoreIcon] `notes` d’objets est un magasin d’objets.</span><span class="sxs-lookup"><span data-stu-id="45f8d-119">Object Store icon][ImageObjectStoreIcon] `notes` is an object store.</span></span>  
    *   <span data-ttu-id="45f8d-120">le **titre** et le **corps** sont des [index][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="45f8d-120">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="45f8d-121">**Limitation connue**  Les bases de données tierces ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="45f8d-121">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="45f8d-122">Par exemple, si vous utilisez un `<iframe>` pour incorporer une publicité sur votre page, et si votre réseau publicitaire utilise IndexedDB, les données IndexedDB pour votre réseau publicitaire ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="45f8d-122">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="45f8d-123">Voir [#943770 de problèmes][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="45f8d-123">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="45f8d-124">Sélectionner une base de données pour afficher l’origine et le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="45f8d-124">Select a database to see the origin and version number.</span></span>  
    
    > ##### <span data-ttu-id="45f8d-125">Figure3</span><span class="sxs-lookup"><span data-stu-id="45f8d-125">Figure 3</span></span>  
    > <span data-ttu-id="45f8d-126">La base de données **Notes**</span><span class="sxs-lookup"><span data-stu-id="45f8d-126">The **notes** database</span></span>  
    > ![La base de données Notes][ImageIndexedDBDatabase]  
    
1.  <span data-ttu-id="45f8d-128">Sélectionnez un magasin d’objets pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="45f8d-128">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="45f8d-129">Les données IndexedDB ne sont pas mises à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="45f8d-129">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="45f8d-130">Voir [Actualiser les données de IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="45f8d-130">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="45f8d-131">Figure 4</span><span class="sxs-lookup"><span data-stu-id="45f8d-131">Figure 4</span></span>  
    > <span data-ttu-id="45f8d-132">Magasin d’objets **Notes**</span><span class="sxs-lookup"><span data-stu-id="45f8d-132">The **notes** object store</span></span>  
    > ![Magasin d’objets notes][ImageIndexedDBObjectStore]  

    *   <span data-ttu-id="45f8d-134">Nombre **total d’entrées** est le nombre total de paires clé-valeur dans le magasin d’objets.</span><span class="sxs-lookup"><span data-stu-id="45f8d-134">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="45f8d-135">**Valeur de générateur de clé** est la clé disponible suivante.</span><span class="sxs-lookup"><span data-stu-id="45f8d-135">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="45f8d-136">Ce champ est affiché uniquement lors de l’utilisation de [générateurs de touches][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="45f8d-136">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  

1.  <span data-ttu-id="45f8d-137">Sélectionnez une cellule dans la colonne **valeur** pour développer cette valeur.</span><span class="sxs-lookup"><span data-stu-id="45f8d-137">Select a cell in the **Value** column to expand that value.</span></span>  
    
    > ##### <span data-ttu-id="45f8d-138">Figure 5</span><span class="sxs-lookup"><span data-stu-id="45f8d-138">Figure 5</span></span>  
    > <span data-ttu-id="45f8d-139">Affichage d’une valeur IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-139">Viewing an IndexedDB value</span></span>  
    > ![Affichage d’une valeur IndexedDB][ImageIndexedBDValue]  
    
1.  <span data-ttu-id="45f8d-141">Sélectionnez un index, tel que **titre** ou **corps** dans la [figure 6](#figure-6), pour trier le magasin d’objets en fonction des valeurs de cet index.</span><span class="sxs-lookup"><span data-stu-id="45f8d-141">Select an index, such as **title** or **body** in [Figure 6](#figure-6), to sort the object store according to the values of that index.</span></span>  
   
    > ##### <span data-ttu-id="45f8d-142">Figure 6</span><span class="sxs-lookup"><span data-stu-id="45f8d-142">Figure 6</span></span>  
    > <span data-ttu-id="45f8d-143">Magasin d’objets trié par ordre alphabétique en fonction de la clé de **titre**</span><span class="sxs-lookup"><span data-stu-id="45f8d-143">An object store that is sorted alphabetically according to the **title** key</span></span>  
    > ![Tri d’un magasin d’objets par index][ImageIndexedDBIndex]  

## <span data-ttu-id="45f8d-145">Actualiser les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-145">Refresh IndexedDB data</span></span>   

<span data-ttu-id="45f8d-146">Les valeurs IndexedDB dans le panneau d' **application** ne sont pas mises à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="45f8d-146">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="45f8d-147">Sélectionnez **Actualiser** ![ ][ImageReloadIcon] l’actualisation lors de l’affichage d’un magasin d’objets pour actualiser les données, ou affichez une base de données et cliquez sur **Actualiser la base de données** pour actualiser toutes les données.</span><span class="sxs-lookup"><span data-stu-id="45f8d-147">Select **Refresh** ![Refresh][ImageReloadIcon] when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

> ##### <span data-ttu-id="45f8d-148">Figure 7</span><span class="sxs-lookup"><span data-stu-id="45f8d-148">Figure 7</span></span>  
> <span data-ttu-id="45f8d-149">Affichage d’une base de données</span><span class="sxs-lookup"><span data-stu-id="45f8d-149">Viewing a database</span></span>  
> ![Affichage d’une base de données][ImageIndexedDBDatabase2]  

## <span data-ttu-id="45f8d-151">Modifier les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-151">Edit IndexedDB data</span></span>   

<span data-ttu-id="45f8d-152">Les valeurs et les clés IndexedDB ne peuvent pas être modifiées dans le panneau de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="45f8d-152">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="45f8d-153">Dans la mesure où DevTools a accès au contexte de page, vous pouvez exécuter du code JavaScript dans DevTools pour modifier les données IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="45f8d-153">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="45f8d-154">Modification de données IndexedDB avec des extraits de niveau</span><span class="sxs-lookup"><span data-stu-id="45f8d-154">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="45f8d-155">Les [extraits][DevtoolsJavascriptSnippets] de code permettent de stocker et d’exécuter des blocs de code JavaScript dans devtools.</span><span class="sxs-lookup"><span data-stu-id="45f8d-155">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="45f8d-156">Lorsque vous exécutez un snippet, le résultat est enregistré dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="45f8d-156">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="45f8d-157">Vous pouvez utiliser un extrait de code pour exécuter du code JavaScript afin de modifier une base de données IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="45f8d-157">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

> ##### <span data-ttu-id="45f8d-158">Figure8</span><span class="sxs-lookup"><span data-stu-id="45f8d-158">Figure 8</span></span>  
> <span data-ttu-id="45f8d-159">Utilisation d’un snippet pour interagir avec IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-159">Using a Snippet to interact with IndexedDB</span></span>  
> ![Utilisation d’un snippet pour interagir avec IndexedDB][ImageIndexedDBSnippet]  

## <span data-ttu-id="45f8d-161">Supprimer des données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-161">Delete IndexedDB data</span></span>   

### <span data-ttu-id="45f8d-162">Supprimer une paire clé-valeur IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-162">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="45f8d-163">[Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="45f8d-163">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="45f8d-164">Sélectionnez la paire clé-valeur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="45f8d-164">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="45f8d-165">DevTools le met en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="45f8d-165">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="45f8d-166">Figure9</span><span class="sxs-lookup"><span data-stu-id="45f8d-166">Figure 9</span></span>  
    > <span data-ttu-id="45f8d-167">Sélection d’une paire clé-valeur pour la supprimer</span><span class="sxs-lookup"><span data-stu-id="45f8d-167">Selecting a key-value pair in order to delete it</span></span>  
    > ![Sélection d’une paire clé-valeur pour la supprimer][ImageIndexedDBKeyValuePair]  

1.  <span data-ttu-id="45f8d-169">Appuyez sur la `Delete` touche ou cliquez sur supprimer la suppression **sélectionnée** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="45f8d-169">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  
    
    > ##### <span data-ttu-id="45f8d-170">Figure10</span><span class="sxs-lookup"><span data-stu-id="45f8d-170">Figure 10</span></span>  
    > <span data-ttu-id="45f8d-171">Aspect du magasin d’objets après la suppression de la paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="45f8d-171">How the object store looks after the key-value pair has been deleted</span></span>  
    > ![Aspect du magasin d’objets après la suppression de la paire clé-valeur][ImageIndexedDBKeyValuePairDeleted]  

### <span data-ttu-id="45f8d-173">Supprimer toutes les paires clé-valeur dans un magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="45f8d-173">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="45f8d-174">[Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="45f8d-174">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="45f8d-175">Figure11</span><span class="sxs-lookup"><span data-stu-id="45f8d-175">Figure 11</span></span>  
    > <span data-ttu-id="45f8d-176">Affichage d’un magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="45f8d-176">Viewing an object store</span></span>  
    > ![Affichage d’un magasin d’objets][ImageIndexedDBObjectStore]  

1.  <span data-ttu-id="45f8d-178">Sélectionnez effacer le magasin d’objets du **magasin d’objets** ![ ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="45f8d-178">Select **Clear object store** ![Clear object store][ImageClearIcon].</span></span>  

### <span data-ttu-id="45f8d-179">Supprimer une base de données IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-179">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="45f8d-180">[Affichez la base de données IndexedDB](#view-indexeddb-data) que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="45f8d-180">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="45f8d-181">Sélectionnez **Supprimer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="45f8d-181">Select **Delete database**.</span></span>  
    
    > ##### <span data-ttu-id="45f8d-182">Figure12</span><span class="sxs-lookup"><span data-stu-id="45f8d-182">Figure 12</span></span>  
    > <span data-ttu-id="45f8d-183">Bouton **Supprimer la base de données**</span><span class="sxs-lookup"><span data-stu-id="45f8d-183">The **Delete database** button</span></span>  
    > ![Bouton supprimer la base de données][ImageIndexedDBDatabase]  

### <span data-ttu-id="45f8d-185">Supprimer tout le stockage IndexedDB</span><span class="sxs-lookup"><span data-stu-id="45f8d-185">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="45f8d-186">Ouvrir le volet de **stockage effacer** .</span><span class="sxs-lookup"><span data-stu-id="45f8d-186">Open the **Clear storage** pane.</span></span>  

1.  <span data-ttu-id="45f8d-187">Vérifiez que la case à cocher **IndexedDB** est activée.</span><span class="sxs-lookup"><span data-stu-id="45f8d-187">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  

1.  <span data-ttu-id="45f8d-188">Sélectionnez **effacer les données du site**.</span><span class="sxs-lookup"><span data-stu-id="45f8d-188">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="45f8d-189">Figure13</span><span class="sxs-lookup"><span data-stu-id="45f8d-189">Figure 13</span></span>  
    > <span data-ttu-id="45f8d-190">Vider le volet **stockage** pour ![ Vider le volet stockage][ImageIndexedDBClearStorage]</span><span class="sxs-lookup"><span data-stu-id="45f8d-190">The **Clear storage** pane ![The Clear storage pane][ImageIndexedDBClearStorage]</span></span>  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Figure 1: volet manifeste"  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Figure 2: menu IndexedDB"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Figure 3: notes_db base de données"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Figure 4: magasin d’objets notes_os"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Figure 5: affichage d’une valeur IndexedDB"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Figure 6: tri d’un magasin d’objets par index"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Figure 7: affichage d’une base de données"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Figure 8: utilisation d’un snippet pour interagir avec IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Figure 9: sélection d’une paire clé-valeur pour la supprimer"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Figure 10: apparence du magasin d’objets après la suppression de la paire clé-valeur"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Figure 11: affichage d’un magasin d’objets"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Figure 12: bouton supprimer la base de données"  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Figure 13: volet de stockage clair"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: afficher les bases de données iframe IndexedDB-chrome-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Générateur de clés-Concepts de base | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utiliser IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Utilisation d’un index à l’aide d’IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="45f8d-211">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45f8d-211">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="45f8d-212">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="45f8d-212">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="45f8d-214">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="45f8d-214">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
