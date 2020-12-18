---
description: Découvrez comment afficher et modifier des données IndexedDB à l’aide du volet de l’application et d’extraits.
title: Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 03e6d04050677a0ba153c6adc06dd795cc42115d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231201"
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

# <span data-ttu-id="97988-104">Afficher et modifier des données de IndexedDB avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="97988-104">View and change IndexedDB data with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="97988-105">Ce guide vous montre comment utiliser [Microsoft Edge devtools][MicrosoftEdgeDevTools] pour afficher et modifier des données [IndexedDB][MDNIndexedDBAPI] .</span><span class="sxs-lookup"><span data-stu-id="97988-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="97988-106">Il part du principe que vous êtes familiarisé avec DevTools.</span><span class="sxs-lookup"><span data-stu-id="97988-106">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="97988-107">Il suppose également que vous êtes familiarisé avec IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="97988-107">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="97988-108">Si ce n’est pas le cas, accédez à [utiliser IndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="97988-108">If not, navigate to [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="97988-109">Afficher les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-109">View IndexedDB data</span></span>  

1.  <span data-ttu-id="97988-110">Sélectionnez l’onglet **application** pour ouvrir l’outil de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="97988-110">Choose the **Application** tab to open the **Application** tool.</span></span>  <span data-ttu-id="97988-111">Le volet **manifeste** s’ouvre généralement par défaut.</span><span class="sxs-lookup"><span data-stu-id="97988-111">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest-empty.msft.png" alt-text="Volet manifeste" lightbox="../media/storage-application-manifest-empty.msft.png":::
       <span data-ttu-id="97988-113">Volet **manifeste**</span><span class="sxs-lookup"><span data-stu-id="97988-113">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="97988-114">Développez le menu **IndexedDB** pour connaître les bases de données disponibles.</span><span class="sxs-lookup"><span data-stu-id="97988-114">Expand the **IndexedDB** menu to review which databases are available.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb.msft.png" alt-text="Menu de IndexedDB" lightbox="../media/storage-application-storage-indexeddb.msft.png":::
       <span data-ttu-id="97988-116">Menu de **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="97988-116">The **IndexedDB** menu</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="97988-117">\ ( ![ Icône de base de données ][ImageDatabaseIcon] \) `notes - https://mdn.github.io` représente une base de données, où `notes` est le nom de la base de données et `https://mdn.github.io` est l’origine qui accède à la base de données.</span><span class="sxs-lookup"><span data-stu-id="97988-117">\(![Database icon][ImageDatabaseIcon]\) `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   <span data-ttu-id="97988-118">\ ( ![ Icône de magasin d’objets ][ImageObjectStoreIcon] \) `notes` est un magasin d’objets.</span><span class="sxs-lookup"><span data-stu-id="97988-118">\(![Object Store icon][ImageObjectStoreIcon]\) `notes` is an object store.</span></span>  
    *   <span data-ttu-id="97988-119">le **titre** et le **corps** sont des [index][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="97988-119">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="97988-120">**Limitation connue**  Les bases de données tierces ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="97988-120">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="97988-121">Par exemple, si vous utilisez un `<iframe>` pour incorporer une publicité sur votre page, et si votre réseau publicitaire utilise IndexedDB, les données IndexedDB pour votre réseau publicitaire ne sont pas visibles.</span><span class="sxs-lookup"><span data-stu-id="97988-121">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="97988-122">Accédez à [#943770 problème][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="97988-122">Navigate to [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="97988-123">Choisissez une base de données pour vérifier l’origine et le numéro de version.</span><span class="sxs-lookup"><span data-stu-id="97988-123">Choose a database to review the origin and version number.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db.msft.png" alt-text="La base de données Notes" lightbox="../media/storage-application-storage-indexeddb-notes_db.msft.png":::
       <span data-ttu-id="97988-125">La base de données **Notes**</span><span class="sxs-lookup"><span data-stu-id="97988-125">The **notes** database</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="97988-126">Sélectionnez un magasin d’objets pour passer en revue les paires clé-valeur.</span><span class="sxs-lookup"><span data-stu-id="97988-126">Choose an object store to review the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="97988-127">Les données IndexedDB ne sont pas mises à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="97988-127">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="97988-128">Accédez à [Actualiser les données de IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="97988-128">Navigate to [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png" alt-text="Magasin d’objets notes" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png":::
       <span data-ttu-id="97988-130">Magasin d’objets **Notes**</span><span class="sxs-lookup"><span data-stu-id="97988-130">The **notes** object store</span></span>  
    :::image-end:::  
    
    *   <span data-ttu-id="97988-131">Nombre **total d’entrées** est le nombre total de paires clé-valeur dans le magasin d’objets.</span><span class="sxs-lookup"><span data-stu-id="97988-131">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="97988-132">**Valeur de générateur de clé** est la clé disponible suivante.</span><span class="sxs-lookup"><span data-stu-id="97988-132">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="97988-133">Le champ est affiché uniquement lors de l’utilisation de [générateurs de touches][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="97988-133">The field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  
    
1.  <span data-ttu-id="97988-134">Choisissez une cellule dans la colonne **valeur** pour développer la valeur.</span><span class="sxs-lookup"><span data-stu-id="97988-134">Choose a cell in the **Value** column to expand the value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png" alt-text="Afficher une valeur IndexedDB" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png":::
       <span data-ttu-id="97988-136">Afficher une valeur **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="97988-136">View an **IndexedDB** value</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="97988-137">Choisissez un index, tel que **titre** ou **corps** dans l’illustration suivante, pour trier la Banque d’objets en fonction des valeurs de cet index.</span><span class="sxs-lookup"><span data-stu-id="97988-137">Choose an index, such as **title** or **body** in the following figure, to sort the object store according to the values of that index.</span></span>  
   
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png" alt-text="Trier un magasin d’objets par index" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png":::
       <span data-ttu-id="97988-139">Trier un magasin d’objets par index</span><span class="sxs-lookup"><span data-stu-id="97988-139">Sort an object store by an index</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="97988-140">Actualiser les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-140">Refresh IndexedDB data</span></span>  

<span data-ttu-id="97988-141">Les valeurs IndexedDB dans l’outil d' **application** ne sont pas mises à jour en temps réel.</span><span class="sxs-lookup"><span data-stu-id="97988-141">IndexedDB values in the **Application** tool do not update in real-time.</span></span>  <span data-ttu-id="97988-142">Sélectionnez **Actualiser** \ ( ![ Actualiser ][ImageReloadIcon] \) lors de l’affichage d’un magasin d’objets pour actualiser les données, ou affichez une base de données et sélectionnez **Actualiser la base de données** pour actualiser toutes les données.</span><span class="sxs-lookup"><span data-stu-id="97988-142">Choose **Refresh** \(![Refresh][ImageReloadIcon]\) when viewing an object store to refresh the data, or view a database and choose **Refresh database** to refresh all data.</span></span>  

:::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png" alt-text="Affichage d’une base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png":::
   <span data-ttu-id="97988-144">Affichage d’une base de données</span><span class="sxs-lookup"><span data-stu-id="97988-144">View a database</span></span>  
:::image-end:::  

## <span data-ttu-id="97988-145">Modifier les données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-145">Edit IndexedDB data</span></span>  

<span data-ttu-id="97988-146">Les valeurs et les clés de IndexedDB ne sont pas modifiables à partir de l’outil de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="97988-146">IndexedDB keys and values are not editable from the **Application** tool.</span></span>  <span data-ttu-id="97988-147">Dans la mesure où DevTools a accès au contexte de page, vous pouvez exécuter du code JavaScript dans DevTools pour modifier les données IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="97988-147">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="97988-148">Modification de données IndexedDB avec des extraits de niveau</span><span class="sxs-lookup"><span data-stu-id="97988-148">Edit IndexedDB data with Snippets</span></span>  

<span data-ttu-id="97988-149">Les [extraits][DevtoolsJavascriptSnippets] de code permettent de stocker et d’exécuter des blocs de code JavaScript dans devtools.</span><span class="sxs-lookup"><span data-stu-id="97988-149">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="97988-150">Lorsque vous exécutez un snippet, le résultat est enregistré dans la **console**.</span><span class="sxs-lookup"><span data-stu-id="97988-150">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="97988-151">Vous pouvez utiliser un extrait de code pour exécuter du code JavaScript afin de modifier une base de données IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="97988-151">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

:::image type="complex" source="../media/storage-sources-snippets-indexeddb-output.msft.png" alt-text="Utiliser un snippet pour interagir avec IndexedDB" lightbox="../media/storage-sources-snippets-indexeddb-output.msft.png":::
   <span data-ttu-id="97988-153">Utiliser un snippet pour interagir avec IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-153">Use a Snippet to interact with IndexedDB</span></span>  
:::image-end:::  

## <span data-ttu-id="97988-154">Supprimer des données de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-154">Delete IndexedDB data</span></span>  

### <span data-ttu-id="97988-155">Supprimer une paire clé-valeur IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-155">Delete an IndexedDB key-value pair</span></span>  

1.  <span data-ttu-id="97988-156">[Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="97988-156">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="97988-157">Sélectionnez la paire clé-valeur que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="97988-157">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="97988-158">DevTools le met en surbrillance pour indiquer qu’il est sélectionné.</span><span class="sxs-lookup"><span data-stu-id="97988-158">DevTools highlights it to indicate that it is selected.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png" alt-text="Sélectionner une paire clé-valeur pour la supprimer" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png":::
       <span data-ttu-id="97988-160">Sélectionner une paire clé-valeur pour la supprimer</span><span class="sxs-lookup"><span data-stu-id="97988-160">Select a key-value pair in order to delete it</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="97988-161">Appuyez sur la `Delete` touche ou sélectionnez **Supprimer la sélection** \ (supprimer la ![ sélection ][ImageDeleteIcon] ).</span><span class="sxs-lookup"><span data-stu-id="97988-161">Press the `Delete` key or choose **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png" alt-text="Aspect du magasin d’objets après la suppression de la paire clé-valeur" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png":::
       <span data-ttu-id="97988-163">Aspect du magasin d’objets après la suppression de la paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="97988-163">How the object store looks after the key-value pair has been deleted</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="97988-164">Supprimer toutes les paires clé-valeur dans un magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="97988-164">Delete all key-value pairs in an object store</span></span>  

1.  <span data-ttu-id="97988-165">[Afficher un magasin d’objets IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="97988-165">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png" alt-text="Afficher un magasin d’objets" lightbox="../media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png":::
       <span data-ttu-id="97988-167">Afficher un magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="97988-167">View an object store</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="97988-168">Sélectionnez **effacer le magasin d’objets** \ ( ![ effacer le magasin d’objets ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="97988-168">Choose **Clear object store** \(![Clear object store][ImageClearIcon]\).</span></span>  
    
### <span data-ttu-id="97988-169">Supprimer une base de données IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-169">Delete an IndexedDB database</span></span>  

1.  <span data-ttu-id="97988-170">[Affichez la base de données IndexedDB](#view-indexeddb-data) que vous voulez supprimer.</span><span class="sxs-lookup"><span data-stu-id="97988-170">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="97988-171">Cliquez sur **Supprimer la base de données**.</span><span class="sxs-lookup"><span data-stu-id="97988-171">Choose **Delete database**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png" alt-text="Bouton supprimer la base de données" lightbox="../media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png":::
       <span data-ttu-id="97988-173">Bouton **Supprimer la base de données**</span><span class="sxs-lookup"><span data-stu-id="97988-173">The **Delete database** button</span></span>  
    :::image-end:::  
    
### <span data-ttu-id="97988-174">Supprimer tout le stockage IndexedDB</span><span class="sxs-lookup"><span data-stu-id="97988-174">Delete all IndexedDB storage</span></span>  

1.  <span data-ttu-id="97988-175">Ouvrir le volet de **stockage effacer** .</span><span class="sxs-lookup"><span data-stu-id="97988-175">Open the **Clear storage** pane.</span></span>  
1.  <span data-ttu-id="97988-176">Vérifiez que la case à cocher **IndexedDB** est activée.</span><span class="sxs-lookup"><span data-stu-id="97988-176">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  
1.  <span data-ttu-id="97988-177">Sélectionnez **effacer les données du site**.</span><span class="sxs-lookup"><span data-stu-id="97988-177">Choose **Clear site data**.</span></span>  
    
    :::image type="complex" source="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png" alt-text="Vider le volet stockage" lightbox="../media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png":::
       <span data-ttu-id="97988-179">Vider le volet **stockage**</span><span class="sxs-lookup"><span data-stu-id="97988-179">The **Clear storage** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="97988-180">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="97988-180">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDatabaseIcon]: ../media/database-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  
[ImageObjectStoreIcon]: ../media/object-store-icon.msft.png  
[ImageReloadIcon]: ../media/reload-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevtoolsJavascriptSnippets]: ../javascript/snippets.md "Exécution d’extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools | Documents Microsoft"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: afficher les bases de données iframe IndexedDB-chrome-monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Générateur de clés-Concepts de base | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Utiliser IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Utilisation d’un index à l’aide d’IndexedDB | MDN"  

> [!NOTE]
> <span data-ttu-id="97988-188">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="97988-188">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="97988-189">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="97988-189">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="97988-191">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="97988-191">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
