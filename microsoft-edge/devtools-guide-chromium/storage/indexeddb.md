---
title: Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 890e20f65c3b70193a38783f3c9ca5d879d5ac48
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983743"
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





# <span data-ttu-id="9e42f-103">Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9e42f-103">View and change IndexedDB data with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="9e42f-104">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher et modifier des données [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="9e42f-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="9e42f-105">Il part du principe que vous êtes familiarisé avec DevTools.</span><span class="sxs-lookup"><span data-stu-id="9e42f-105">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="9e42f-106">Il suppose également que vous êtes familiarisé avec IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="9e42f-106">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="9e42f-107">Si ce n’est pas le cas, voir [utilisation de IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="9e42f-107">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="9e42f-108">Afficher les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-108">View IndexedDB data</span></span>   

1.  <span data-ttu-id="9e42f-109">Sélectionnez l’onglet **application** pour ouvrir le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="9e42f-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="9e42f-110">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="9e42f-110">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="9e42f-112">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="9e42f-112">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9e42f-113">Développez le menu **IndexedDB** pour afficher les bases de données disponibles.</span><span class="sxs-lookup"><span data-stu-id="9e42f-113">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Menu de IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="9e42f-115">Menu de **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="9e42f-115">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="9e42f-116">\ ( ![ Icône de base de données ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` représente une base de données, où `notes` est le nom de la base de données et `https://mdn.github.io` est l’origine qui accède à la base de données.</span><span class="sxs-lookup"><span data-stu-id="9e42f-116">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="9e42f-117">\ ( ![ Icône de magasin d’objets ][ImageObjectStoreIcon] \) `notes` est un magasin d’objets.</span><span class="sxs-lookup"><span data-stu-id="9e42f-117">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="9e42f-118">le **titre** et le **corps** sont des [index][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="9e42f-118">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9e42f-119">**Limitation connue**  Les bases de données tierces ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="9e42f-119">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="9e42f-120">Par exemple, si vous utilisez un `<iframe>` pour incorporer une publicité sur votre page, et si votre réseau publicitaire utilise IndexedDB, les données IndexedDB pour votre réseau publicitaire ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="9e42f-120">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="9e42f-121">Voir [#943770 de problèmes][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="9e42f-121">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="9e42f-122">Sélectionner une base de données pour afficher l’origine et le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="9e42f-122">Select a database to see the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="La base de données Notes" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="9e42f-124">La base de données **Notes**</span><span class="sxs-lookup"><span data-stu-id="9e42f-124">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9e42f-125">Sélectionnez un magasin d’objets pour afficher les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="9e42f-125">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="9e42f-126">Les données IndexedDB ne sont pas mises à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="9e42f-126">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="9e42f-127">Voir [Actualiser les données de IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="9e42f-127">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Magasin d’objets notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="9e42f-129">Magasin d’objets **Notes**</span><span class="sxs-lookup"><span data-stu-id="9e42f-129">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="9e42f-130">Nombre **total d’entrées** est le nombre total de paires clé-valeur dans le magasin d’objets.</span><span class="sxs-lookup"><span data-stu-id="9e42f-130">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="9e42f-131">**Valeur de générateur de clé** est la clé disponible suivante.</span><span class="sxs-lookup"><span data-stu-id="9e42f-131">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="9e42f-132">Ce champ est affiché uniquement lors de l’utilisation de [générateurs de touches][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="9e42f-132">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="9e42f-133">Sélectionnez une cellule dans la colonne **valeur** pour développer cette valeur.</span><span class="sxs-lookup"><span data-stu-id="9e42f-133">Select a cell in the **Value** column to expand that value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Afficher une valeur IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="9e42f-135">Afficher une valeur **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="9e42f-135">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9e42f-136">Sélectionner un index, tel que **titre** ou **corps** dans l’illustration suivante, pour trier la Banque d’objets en fonction des valeurs de cet index.</span><span class="sxs-lookup"><span data-stu-id="9e42f-136">Select an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Trier un magasin d’objets par index" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="9e42f-138">Trier un magasin d’objets par index</span><span class="sxs-lookup"><span data-stu-id="9e42f-138">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="9e42f-139">Actualiser les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-139">Refresh IndexedDB data</span></span>   

<span data-ttu-id="9e42f-140">Les valeurs IndexedDB dans le panneau d' **application** ne sont pas mises à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="9e42f-140">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="9e42f-141">Sélectionnez **Actualiser** \ ( ![ Actualiser ][ImageReloadIcon] \) lors de l’affichage d’un magasin d’objets pour actualiser les données, ou affichez une base de données, puis cliquez sur **Actualiser la base de données** pour actualiser toutes les données.</span><span class="sxs-lookup"><span data-stu-id="9e42f-141">Select **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Affichage d’une base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="9e42f-143">Affichage d’une base de données</span><span class="sxs-lookup"><span data-stu-id="9e42f-143">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="9e42f-144">Modifier les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-144">Edit IndexedDB data</span></span>   

<span data-ttu-id="9e42f-145">Les valeurs et les clés IndexedDB ne peuvent pas être modifiées dans le panneau de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="9e42f-145">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="9e42f-146">Dans la mesure où DevTools a accès au contexte de page, vous pouvez exécuter du code JavaScript dans DevTools pour modifier les données IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="9e42f-146">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="9e42f-147">Modification de données IndexedDB avec des extraits de niveau</span><span class="sxs-lookup"><span data-stu-id="9e42f-147">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="9e42f-148">Les [extraits][DevtoolsJavascriptSnippets] de code permettent de stocker et d’exécuter des blocs de code JavaScript dans devtools.</span><span class="sxs-lookup"><span data-stu-id="9e42f-148">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="9e42f-149">Lorsque vous exécutez un snippet, le résultat est enregistré dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="9e42f-149">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="9e42f-150">Vous pouvez utiliser un extrait de code pour exécuter du code JavaScript afin de modifier une base de données IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="9e42f-150">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Utiliser un snippet pour interagir avec IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="9e42f-152">Utiliser un snippet pour interagir avec IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-152">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="9e42f-153">Supprimer des données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-153">Delete IndexedDB data</span></span>   

### <span data-ttu-id="9e42f-154">Supprimer une paire clé-valeur IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-154">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="9e42f-155">[Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="9e42f-155">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="9e42f-156">Sélectionnez la paire clé-valeur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="9e42f-156">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="9e42f-157">DevTools le met en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="9e42f-157">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Sélectionner une paire clé-valeur pour la supprimer" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="9e42f-159">Sélectionner une paire clé-valeur pour la supprimer</span><span class="sxs-lookup"><span data-stu-id="9e42f-159">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9e42f-160">Appuyez sur la `Delete` touche ou cliquez sur **Supprimer la sélection** ![ ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="9e42f-160">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Aspect du magasin d’objets après la suppression de la paire clé-valeur" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="9e42f-162">Aspect du magasin d’objets après la suppression de la paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="9e42f-162">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9e42f-163">Supprimer toutes les paires clé-valeur dans un magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="9e42f-163">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="9e42f-164">[Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="9e42f-164">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Afficher un magasin d’objets" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="9e42f-166">Afficher un magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="9e42f-166">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9e42f-167">Sélectionnez **effacer le magasin d’objets** \ ( ![ Vider le magasin d’objets ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="9e42f-167">Select **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="9e42f-168">Supprimer une base de données IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-168">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="9e42f-169">[Affichez la base de données IndexedDB](#view-indexeddb-data) que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="9e42f-169">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="9e42f-170">Sélectionnez **Supprimer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="9e42f-170">Select **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Bouton supprimer la base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="9e42f-172">Bouton **Supprimer la base de données**</span><span class="sxs-lookup"><span data-stu-id="9e42f-172">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="9e42f-173">Supprimer tout le stockage IndexedDB</span><span class="sxs-lookup"><span data-stu-id="9e42f-173">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="9e42f-174">Ouvrir le volet de **stockage effacer** .</span><span class="sxs-lookup"><span data-stu-id="9e42f-174">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="9e42f-175">Vérifiez que la case à cocher **IndexedDB** est activée.</span><span class="sxs-lookup"><span data-stu-id="9e42f-175">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="9e42f-176">Sélectionnez **effacer les données du site**.</span><span class="sxs-lookup"><span data-stu-id="9e42f-176">Select **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Vider le volet stockage" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="9e42f-178">Vider le volet **stockage**</span><span class="sxs-lookup"><span data-stu-id="9e42f-178">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Exécution d’extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: afficher les bases de données iframe IndexedDB-chrome-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Générateur de clés-Concepts de base | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utiliser IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Utilisation d’un index à l’aide d’IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="9e42f-186">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9e42f-186">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9e42f-187">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="9e42f-187">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="9e42f-189">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9e42f-189">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
