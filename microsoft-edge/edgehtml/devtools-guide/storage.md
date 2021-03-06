---
description: Utiliser le panneau de stockage pour inspecter votre stockage web, IndexedDB, les cookies et les caches de demande/réponse
title: Stockage | DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, stockage web, stockage local, stockage de session, indexeddb, cookies, service de travail, cache
ms.custom: seodec18
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3e970ae0d8ca3a43a309eff7b77400aa3ced5b21
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398895"
---
# <a name="storage"></a><span data-ttu-id="cebed-104">Stockage</span><span class="sxs-lookup"><span data-stu-id="cebed-104">Storage</span></span>

<span data-ttu-id="cebed-105">Utilisez le **panneau de** stockage pour inspecter et gérer diverses données mises en cache localement, notamment :</span><span class="sxs-lookup"><span data-stu-id="cebed-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>  

*   <span data-ttu-id="cebed-106">[Paires](#local-and-session-storage-managers) clé/valeurs de stockage Web \(Stockage local et de session\)</span><span class="sxs-lookup"><span data-stu-id="cebed-106">[Web storage](#local-and-session-storage-managers) \(Local and Session storage\) key/values pairs</span></span>  
*   <span data-ttu-id="cebed-107">[Données structurées de base de données](#indexeddb-manager) indexées</span><span class="sxs-lookup"><span data-stu-id="cebed-107">[Indexed DB](#indexeddb-manager) structured data</span></span>  
*   <span data-ttu-id="cebed-108">[Cookies](#cookies-list) pour le domaine</span><span class="sxs-lookup"><span data-stu-id="cebed-108">[Cookies](#cookies-list) for the domain</span></span>  
*   <span data-ttu-id="cebed-109">[Cache](#cache-manager) \(request/response pairs\) for service worker debugging</span><span class="sxs-lookup"><span data-stu-id="cebed-109">[Cache](#cache-manager) \(request/response pairs\) for service worker debugging</span></span>  

<span data-ttu-id="cebed-110">Développez l’une de ces catégories et cliquez sur une entrée enfant pour ouvrir l’onglet Gestionnaire de ressources.</span><span class="sxs-lookup"><span data-stu-id="cebed-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>  

## <a name="local-and-session-storage-managers"></a><span data-ttu-id="cebed-111">Responsables de stockage local et de session</span><span class="sxs-lookup"><span data-stu-id="cebed-111">Local and Session storage managers</span></span>  

<span data-ttu-id="cebed-112">Utilisez le gestionnaire de stockage local et le gestionnaire de stockage de session pour inspecter et gérer le stockage web de votre page.</span><span class="sxs-lookup"><span data-stu-id="cebed-112">Use the Local Storage manager and Session Storage manager to inspect and manage the web storage for your page.</span></span>  

<span data-ttu-id="cebed-113">Les **dossiers Stockage local** et **Stockage** de [](./debugger.md#resource-picker) session à l’intérieur du s sélectionneur de ressources du panneau de stockage affichent la liste des origines de la page.</span><span class="sxs-lookup"><span data-stu-id="cebed-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [Resource picker](./debugger.md#resource-picker) display a list of origins for the page.</span></span>  <span data-ttu-id="cebed-114">La sélection de l’une de ces images ouvre une table modifiable des paires clé/valeur actuelles définies via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) ou [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivement \(et/ou définies directement à partir de la liste de stockage DevTools [](#storage-list)\).</span><span class="sxs-lookup"><span data-stu-id="cebed-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively \(and/or set directly from the  DevTools [Storage list](#storage-list)\).</span></span>  

![Gestionnaire de stockage DevTools](./media/storage_web_storage.png)  

<span data-ttu-id="cebed-116">Dans les onglets Stockage local et Stockage de session, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cebed-116">From the Local Storage and Session Storage tabs you can:</span></span>  

*   <span data-ttu-id="cebed-117">**Actualisez** \( \) la liste de stockage pour voir l’ensemble actuel de `Ctrl+F5` paires [](#cookies-list) clé/valeurs pour le domaine donné.</span><span class="sxs-lookup"><span data-stu-id="cebed-117">**Refresh** \(`Ctrl+F5`\) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span>  <span data-ttu-id="cebed-118">\(La liste n’est pas actualisée automatiquement lors des mises à jour de script.\)</span><span class="sxs-lookup"><span data-stu-id="cebed-118">\(The list does not auto-refresh upon script updates.\)</span></span>  
*   <span data-ttu-id="cebed-119">**Simulez l’atteinte de la limite de**  stockage pour le stockage web Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="cebed-119">**Simulate reaching the storage limit**  for Microsoft Edge web storage.</span></span>  <span data-ttu-id="cebed-120">Chaque domaine et sous-domaine possède sa propre zone de stockage, mais il existe une limite combinée :</span><span class="sxs-lookup"><span data-stu-id="cebed-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>  
    *   <span data-ttu-id="cebed-121">**Sous-domaine :** jusqu’à 5 Mo d’espace</span><span class="sxs-lookup"><span data-stu-id="cebed-121">**Subdomains**:  up to 5 MBs of space</span></span>  
    *   <span data-ttu-id="cebed-122">**Domaines :** jusqu’à 10 Mo d’espace</span><span class="sxs-lookup"><span data-stu-id="cebed-122">**Domains**:  up to 10 MBs of space</span></span>  
    *   <span data-ttu-id="cebed-123">**Total pour tous les domaines**: jusqu’à 50 Mo d’espace</span><span class="sxs-lookup"><span data-stu-id="cebed-123">**Total for all domains**:  up to 50 MBs of space</span></span>  

   <span data-ttu-id="cebed-124">Le stockage de session est effacé dès que le dernier onglet du navigateur référent à son origine est fermé.</span><span class="sxs-lookup"><span data-stu-id="cebed-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span>  <span data-ttu-id="cebed-125">Les entrées de stockage local persistent indéfiniment jusqu’à ce qu’elles soient effacées par programme par la page ou manuellement par l’utilisateur :</span><span class="sxs-lookup"><span data-stu-id="cebed-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>  

   <span data-ttu-id="cebed-126">**Paramètres**  >  **Effacer les données de navigation**  >  **Cookies et données de site web enregistrées**</span><span class="sxs-lookup"><span data-stu-id="cebed-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

![Effacer les données de navigation du panneau Paramètres de Microsoft Edge](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a><span data-ttu-id="cebed-128">Liste de stockage</span><span class="sxs-lookup"><span data-stu-id="cebed-128">Storage list</span></span>  

<span data-ttu-id="cebed-129">À partir de la table de liste stockage, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cebed-129">From the Storage list table you can:</span></span>  

*   <span data-ttu-id="cebed-130">**Inspectez et tez** `key/value` vos paires en cliquant sur l’un ou l’autre nom de colonne du tableau.</span><span class="sxs-lookup"><span data-stu-id="cebed-130">**Inspect and sort** your `key/value` pairs by clicking on either column name in the table.</span></span>  
*   <span data-ttu-id="cebed-131">**Modifiez** `Key` le et une entrée existante en `Value` cliquant dans la cellule.</span><span class="sxs-lookup"><span data-stu-id="cebed-131">**Edit** the `Key` and `Value` of an existing entry by clicking in the cell.</span></span>  
*   <span data-ttu-id="cebed-132">**Supprimer** \( \) une entrée à partir de l’option de menu context le clic `Del` droit, **Supprimer l’élément**.</span><span class="sxs-lookup"><span data-stu-id="cebed-132">**Delete** \(`Del`\) an entry from the right-click context menu option, **Delete item**.</span></span>  
*   <span data-ttu-id="cebed-133">**Ajoutez** une `key/value` nouvelle paire en cliquant sur la ligne vide en bas du tableau.</span><span class="sxs-lookup"><span data-stu-id="cebed-133">**Add** a new `key/value` pair by clicking on the empty row at the bottom of the table.</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="cebed-134">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="cebed-134">Shortcuts</span></span>

| <span data-ttu-id="cebed-135">Action</span><span class="sxs-lookup"><span data-stu-id="cebed-135">Action</span></span> | <span data-ttu-id="cebed-136">Raccourci</span><span class="sxs-lookup"><span data-stu-id="cebed-136">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="cebed-137">Actualiser</span><span class="sxs-lookup"><span data-stu-id="cebed-137">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="cebed-138">Supprimer l’élément</span><span class="sxs-lookup"><span data-stu-id="cebed-138">Delete item</span></span> | `Del` |  
| <span data-ttu-id="cebed-139">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="cebed-139">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="cebed-140">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="cebed-140">Select all</span></span> | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a><span data-ttu-id="cebed-141">Gestionnaire IndexedDB</span><span class="sxs-lookup"><span data-stu-id="cebed-141">IndexedDB manager</span></span>  

<span data-ttu-id="cebed-142">Utilisez **l’onglet IndexedDB** pour inspecter et gérer les données structurées stockées localement sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="cebed-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span>  <span data-ttu-id="cebed-143">Plus précisément, vous pouvez inspecter/trier et actualiser vos magasins d’objets et index, ainsi que supprimer des entrées clé-valeur individuelles.</span><span class="sxs-lookup"><span data-stu-id="cebed-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>  

> [!TIP]
> <span data-ttu-id="cebed-144">Vous pouvez utiliser notre [démonstration Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) pour tester le gestionnaire *IndexedDB* dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="cebed-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="cebed-145">Pour supprimer toutes les données IndexedDB stockées pour l’utilisateur actuel dans Microsoft Edge, utilisez le menu **Paramètres** de Microsoft Edge :</span><span class="sxs-lookup"><span data-stu-id="cebed-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge **Settings** menu:</span></span>  

<span data-ttu-id="cebed-146">**...** >  **Paramètres**  >  **Effacer les données de navigation**  >  **Cookies et données de site web enregistrées**</span><span class="sxs-lookup"><span data-stu-id="cebed-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>  

<span data-ttu-id="cebed-147">Le dossier à l’intérieur du s sélectionneur de ressources du débogger affiche la liste des origines des `IndexedDB` ressources chargées par la page. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="cebed-147">The `IndexedDB` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="cebed-148">Toutes les bases de données IndexedDB \(IDB\) sont répertoriées sous l’origine, ainsi que leurs magasins d’objets.</span><span class="sxs-lookup"><span data-stu-id="cebed-148">Any IndexedDB \(IDB\) databases will be listed under the origin, along with their object stores.</span></span>  

![Gestionnaire IndexedDB DevTools](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a><span data-ttu-id="cebed-150">Barre d’outils IndexedDB</span><span class="sxs-lookup"><span data-stu-id="cebed-150">IndexedDB Toolbar</span></span>  

<span data-ttu-id="cebed-151">À partir de la barre d’outils IndexedDB, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cebed-151">From the IndexedDB toolbar you can:</span></span>  

*   <span data-ttu-id="cebed-152">**Actualisez** \( \) pour voir les entrées actuelles dans le magasin d’objets ou `Ctrl` + `F5` l’index de votre base de données.</span><span class="sxs-lookup"><span data-stu-id="cebed-152">**Refresh** \(`Ctrl`+`F5`\) to see the current entries in the object store or index of your database.</span></span>  <span data-ttu-id="cebed-153">Le gestionnaire IndexedDB n’est pas actualisé automatiquement lorsque des modifications sont apportées à votre base de données.</span><span class="sxs-lookup"><span data-stu-id="cebed-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>  

### <a name="object-store-entries-list"></a><span data-ttu-id="cebed-154">Liste des entrées du magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="cebed-154">Object store entries list</span></span>  

<span data-ttu-id="cebed-155">À partir du magasin d’objets ou de la table Index, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cebed-155">From the Object store or Index table you can:</span></span>  

*   <span data-ttu-id="cebed-156">**Inspectez et tez** vos paires clé-valeur en cliquant sur n’importe quel nom de colonne du tableau.</span><span class="sxs-lookup"><span data-stu-id="cebed-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="cebed-157">**Refresh** \( `Ctrl` + `F5` \)</span><span class="sxs-lookup"><span data-stu-id="cebed-157">**Refresh** \(`Ctrl`+`F5`\)</span></span>  
*   <span data-ttu-id="cebed-158">**Supprimez l’élément** \( \) pour supprimer l’entrée sélectionnée dans votre magasin `Del` d’objets ou index.</span><span class="sxs-lookup"><span data-stu-id="cebed-158">**Delete item** \(`Del`\) to remove the selected entry in your object store or index.</span></span>  <span data-ttu-id="cebed-159">Vous pouvez également le faire à partir de l’option de [menu](#context-menu) context un clic droit, **Supprimer l’élément.**</span><span class="sxs-lookup"><span data-stu-id="cebed-159">You can also do this from the right-click [context menu](#context-menu) option, **Delete item**.</span></span>  
*   <span data-ttu-id="cebed-160">**Copiez les éléments sélectionnés** \( \) pour copier l’élément `Ctrl` + `C` sélectionné dans votre Presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="cebed-160">**Copy selected items** \(`Ctrl`+`C`\) to copy the selected item to your clipboard.</span></span>  <span data-ttu-id="cebed-161">Vous pouvez également le faire à partir de l’option de [menu](#context-menu) context un clic droit, **Copier l’élément sélectionné.**</span><span class="sxs-lookup"><span data-stu-id="cebed-161">You can also do this from the right-click [context menu](#context-menu) option, **Copy selected item**.</span></span>  
*   <span data-ttu-id="cebed-162">**Sélectionnez toutes** les \( \) pour sélectionner toutes les entrées de votre magasin `Ctrl` + `A` d’objets ou index.</span><span class="sxs-lookup"><span data-stu-id="cebed-162">**Select all** \(`Ctrl`+`A`\) to select all the entries in your object store or index.</span></span>  <span data-ttu-id="cebed-163">Vous pouvez également le faire à partir de l’option de menu contexto de [clic](#context-menu) droit, **Sélectionner tout.**</span><span class="sxs-lookup"><span data-stu-id="cebed-163">You can also do this from the right-click [context menu](#context-menu) option, **Select all**.</span></span>  

<span data-ttu-id="cebed-164">Les colonnes du magasin d’objets ou de la table Index sont triables :</span><span class="sxs-lookup"><span data-stu-id="cebed-164">The columns of the Object store or Index table are sortable:</span></span>  

| <span data-ttu-id="cebed-165">Colonne</span><span class="sxs-lookup"><span data-stu-id="cebed-165">Column</span></span> | <span data-ttu-id="cebed-166">Description</span><span class="sxs-lookup"><span data-stu-id="cebed-166">Description</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="cebed-167">Clé</span><span class="sxs-lookup"><span data-stu-id="cebed-167">Key</span></span> | <span data-ttu-id="cebed-168">Nom de la paire clé-valeur \(identique à **la**clé primaire \) lors de l’itère sur un magasin d’objets ; Nom de la clé d’index \(clé actuelle du curseur\) lors d’une itération sur un index</span><span class="sxs-lookup"><span data-stu-id="cebed-168">Name of the key-value pair \(same as **Primary Key**\) when iterating over an object store; Name of the index key \(cursor's current key\) when iterating over an index</span></span> |  
| <span data-ttu-id="cebed-169">Clé primaire</span><span class="sxs-lookup"><span data-stu-id="cebed-169">Primary Key</span></span> | <span data-ttu-id="cebed-170">Nom de la paire clé-valeur \(voir **documents web MDN** pour plus d’informations sur les clés [IDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span><span class="sxs-lookup"><span data-stu-id="cebed-170">Name of the key-value pair \(see **MDN web docs** for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\)</span></span> |  
| <span data-ttu-id="cebed-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="cebed-171">Value</span></span> | <span data-ttu-id="cebed-172">Valeur de la paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="cebed-172">Value of the key-value pair</span></span> |  

<span data-ttu-id="cebed-173">Consultez des *documents web MDN pour* en savoir plus sur les concepts et l’utilisation [d’IndexedDB.](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)</span><span class="sxs-lookup"><span data-stu-id="cebed-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>  

### <a name="context-menu"></a><span data-ttu-id="cebed-174">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="cebed-174">Context menu</span></span>  

<span data-ttu-id="cebed-175">Outre la barre d’outils [ *IndexedDB,* ](#indexeddb-toolbar)vous pouvez également gérer vos données dans les magasins d’objets ou les index à partir du **menu** Context et/ou des [raccourcis clavier.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="cebed-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="cebed-176">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="cebed-176">Shortcuts</span></span>

| <span data-ttu-id="cebed-177">Action</span><span class="sxs-lookup"><span data-stu-id="cebed-177">Action</span></span> | <span data-ttu-id="cebed-178">Raccourci</span><span class="sxs-lookup"><span data-stu-id="cebed-178">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="cebed-179">Actualiser</span><span class="sxs-lookup"><span data-stu-id="cebed-179">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="cebed-180">Supprimer la paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="cebed-180">Delete key-value pair</span></span> | `Del` |  
| <span data-ttu-id="cebed-181">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="cebed-181">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="cebed-182">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="cebed-182">Select all</span></span> | `Ctrl +`<span data-ttu-id="cebed-183">A'</span><span class="sxs-lookup"><span data-stu-id="cebed-183">A\`</span></span> |  

## <a name="cookies-manager"></a><span data-ttu-id="cebed-184">Gestionnaire de cookies</span><span class="sxs-lookup"><span data-stu-id="cebed-184">Cookies manager</span></span>  

<span data-ttu-id="cebed-185">Utilisez le Gestionnaire de cookies pour inspecter et gérer les cookies pour le domaine donné.</span><span class="sxs-lookup"><span data-stu-id="cebed-185">Use the Cookies manager to inspect and manage the cookies for the given domain.</span></span>  

<span data-ttu-id="cebed-186">Le dossier à l’intérieur du s sélectionneur de ressources du débogger affiche la liste des origines des `Cookies` ressources chargées par la page. [](./debugger.md#resource-picker)</span><span class="sxs-lookup"><span data-stu-id="cebed-186">The `Cookies` folder inside the Debugger's [Resource picker](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span>  <span data-ttu-id="cebed-187">La sélection de l’une de ces images ouvre une table représentant les cookies actuels, définies par l’en-tête [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) ou via un script avec [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span><span class="sxs-lookup"><span data-stu-id="cebed-187">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>  

![Gestionnaire de cookies DevTools](./media/storage_cookies.png)  

<span data-ttu-id="cebed-189">À partir de la barre d’outils de l’onglet Cookies, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cebed-189">From the Cookies tab toolbar you can:</span></span>  

*   <span data-ttu-id="cebed-190">**Actualisez** \( \) la liste cookies pour voir l’ensemble actuel de `Ctrl` + `F5` cookies pour le domaine donné. [](#cookies-list)</span><span class="sxs-lookup"><span data-stu-id="cebed-190">**Refresh** \(`Ctrl`+`F5`\) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span>  <span data-ttu-id="cebed-191">\(La liste n’est pas actualisée automatiquement.\)</span><span class="sxs-lookup"><span data-stu-id="cebed-191">\(The list does not auto-refresh.\)</span></span>  
*   <span data-ttu-id="cebed-192">**Supprimez tous les cookies** \( `Ctrl` + `Shift` + `Del` \) \(session et permanent\) pour le chemin d’accès de la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="cebed-192">**Delete all cookies** \(`Ctrl`+`Shift`+`Del`\) \(session and permanent\) for the path of the current page.</span></span>  
*   <span data-ttu-id="cebed-193">**Supprimez tous les cookies de session** \( `Ctrl` + `Del` \) pour le chemin d’accès de la page actuelle.</span><span class="sxs-lookup"><span data-stu-id="cebed-193">**Delete all session cookies** \(`Ctrl`+`Del`\) for the path of the current page.</span></span>  

<span data-ttu-id="cebed-194">Pour effacer complètement votre liste de cookies, vous devrez peut-être effacer tous les **cookies** pour le domaine à partir de la [barre d’outils](./network.md#toolbar) du panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="cebed-194">To completely clear your Cookies list, you might need to **Clear all cookies for the domain** from the [Network](./network.md#toolbar) panel toolbar.</span></span>  

### <a name="cookies-list"></a><span data-ttu-id="cebed-195">Liste des cookies</span><span class="sxs-lookup"><span data-stu-id="cebed-195">Cookies list</span></span>  

<span data-ttu-id="cebed-196">À partir du tableau de liste cookies, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="cebed-196">From the Cookies list table you can:</span></span>  

*   <span data-ttu-id="cebed-197">**Inspectez et tez** vos cookies en cliquant sur n’importe quel nom de colonne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="cebed-197">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>  
*   <span data-ttu-id="cebed-198">**Modifiez** `Name` le cookie existant en `Value` cliquant dans la cellule.</span><span class="sxs-lookup"><span data-stu-id="cebed-198">**Edit** the `Name` and `Value` of an existing cookie by clicking in the cell.</span></span>  
*   <span data-ttu-id="cebed-199">**Supprimez** \( `Del` \) un cookie à partir de l’option de [menu contextiqué avec](#context-menu) le bouton droit, `Delete cookie` .</span><span class="sxs-lookup"><span data-stu-id="cebed-199">**Delete** \(`Del`\) a cookie from the right-click [context menu](#context-menu) option, `Delete cookie`.</span></span>  
*   <span data-ttu-id="cebed-200">**Ajoutez** un nouveau cookie de session pour l’donnée en cliquant sur la `Domain/Path` ligne vide en bas du tableau.</span><span class="sxs-lookup"><span data-stu-id="cebed-200">**Add** a new session cookie for the given `Domain/Path` by clicking on the empty row at the bottom of the table.</span></span>  <span data-ttu-id="cebed-201">Cela fonctionne uniquement pour les cookies de session ; les cookies permanents \(avec des dates d’expiration spécifiques\) doivent être définies avec des méthodes traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="cebed-201">This only works for session cookies; permanent cookies \(with specific expiry dates\) must be set with traditional methods.</span></span>  <span data-ttu-id="cebed-202">Les `Domain` `Path` valeurs et les valeurs sont remplies automatiquement en fonction de l’emplacement de la page.</span><span class="sxs-lookup"><span data-stu-id="cebed-202">The `Domain` and `Path` values are auto-filled according to the location of the page.</span></span>  

<span data-ttu-id="cebed-203">Les colonnes de la liste cookies peuvent être triées :</span><span class="sxs-lookup"><span data-stu-id="cebed-203">The columns of the Cookies list are sortable:</span></span>

| <span data-ttu-id="cebed-204">Colonne</span><span class="sxs-lookup"><span data-stu-id="cebed-204">Column</span></span> | <span data-ttu-id="cebed-205">Description</span><span class="sxs-lookup"><span data-stu-id="cebed-205">Description</span></span> |  
| :--- | :--- |  
| <span data-ttu-id="cebed-206">Name</span><span class="sxs-lookup"><span data-stu-id="cebed-206">Name</span></span> | <span data-ttu-id="cebed-207">Nom du cookie</span><span class="sxs-lookup"><span data-stu-id="cebed-207">Name of the cookie</span></span> |  
| <span data-ttu-id="cebed-208">Valeur</span><span class="sxs-lookup"><span data-stu-id="cebed-208">Value</span></span> | <span data-ttu-id="cebed-209">Valeur du cookie</span><span class="sxs-lookup"><span data-stu-id="cebed-209">Value of the cookie</span></span> |  
| <span data-ttu-id="cebed-210">Domaine</span><span class="sxs-lookup"><span data-stu-id="cebed-210">Domain</span></span> | <span data-ttu-id="cebed-211">Nom d’hôte du cookie \(peut être vide\)</span><span class="sxs-lookup"><span data-stu-id="cebed-211">Host name of the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="cebed-212">Chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="cebed-212">Path</span></span> | <span data-ttu-id="cebed-213">Chemin d’URL du cookie \(peut être vide\)</span><span class="sxs-lookup"><span data-stu-id="cebed-213">URL path for the cookie \(may be empty\)</span></span> |  
| <span data-ttu-id="cebed-214">Arrive à expiration</span><span class="sxs-lookup"><span data-stu-id="cebed-214">Expires</span></span> | <span data-ttu-id="cebed-215">Durée de vie maximale du cookie sous la forme d’un timestamp HTTP-date.</span><span class="sxs-lookup"><span data-stu-id="cebed-215">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span>  <span data-ttu-id="cebed-216">Si aucune `Expires` entrée ou `Max-Age` n’a été définie, l’entrée est considérée comme un cookie de session.</span><span class="sxs-lookup"><span data-stu-id="cebed-216">If no `Expires` or `Max-Age` was set, the entry is considered a Session cookie.</span></span>  |  
| <span data-ttu-id="cebed-217">HTTP uniquement</span><span class="sxs-lookup"><span data-stu-id="cebed-217">HTTP only</span></span> | <span data-ttu-id="cebed-218">Indique si le cookie a été définie avec une directive, indiquant qu’il est `HttpOnly` inaccessible à partir de JavaScript</span><span class="sxs-lookup"><span data-stu-id="cebed-218">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span> |  
| <span data-ttu-id="cebed-219">Sécuriser</span><span class="sxs-lookup"><span data-stu-id="cebed-219">Secure</span></span> | <span data-ttu-id="cebed-220">Indique si le cookie a été définie avec la directive, indiquant qu’il sera uniquement envoyé au serveur à partir d’une demande à l’aide de `Secure` SSL et du protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="cebed-220">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>  |  

<span data-ttu-id="cebed-221">Pour plus **d’informations sur** les propriétés des cookies, voir la référence [set-cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) de la documentation web MDN.</span><span class="sxs-lookup"><span data-stu-id="cebed-221">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>  

### <a name="context-menu"></a><span data-ttu-id="cebed-222">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="cebed-222">Context menu</span></span>  

<span data-ttu-id="cebed-223">Outre la barre d’outils de l’onglet [Cookies,](#cookies-manager)vous pouvez également gérer vos cookies à partir du **menu** Context et/ou des [raccourcis clavier.](#shortcuts)</span><span class="sxs-lookup"><span data-stu-id="cebed-223">In addition to the Cookies tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>  

### <a name="shortcuts"></a><span data-ttu-id="cebed-224">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="cebed-224">Shortcuts</span></span>  

| <span data-ttu-id="cebed-225">Action</span><span class="sxs-lookup"><span data-stu-id="cebed-225">Action</span></span> | <span data-ttu-id="cebed-226">Raccourci</span><span class="sxs-lookup"><span data-stu-id="cebed-226">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="cebed-227">Actualiser</span><span class="sxs-lookup"><span data-stu-id="cebed-227">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="cebed-228">Supprimer un cookie</span><span class="sxs-lookup"><span data-stu-id="cebed-228">Delete cookie</span></span> | `Del` |  
| <span data-ttu-id="cebed-229">Supprimer tous les cookies</span><span class="sxs-lookup"><span data-stu-id="cebed-229">Delete all cookies</span></span> | `Ctrl`+`Shift`+`Del` |  
| <span data-ttu-id="cebed-230">Supprimer tous les cookies de session</span><span class="sxs-lookup"><span data-stu-id="cebed-230">Delete all session cookies</span></span> | `Ctrl`+`Del` |  
| <span data-ttu-id="cebed-231">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="cebed-231">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="cebed-232">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="cebed-232">Select all</span></span> | `Ctrl`+`A` |  

### <a name="cache-manager"></a><span data-ttu-id="cebed-233">Gestionnaire de cache</span><span class="sxs-lookup"><span data-stu-id="cebed-233">Cache manager</span></span>  

<span data-ttu-id="cebed-234">Cliquer sur une entrée de cache spécifique \*\*\*\* ouvre le gestionnaire de cache de travail du service, où vous pouvez inspecter et éventuellement supprimer des entrées de cache \( et `Request` `Response` paires clé/valeur\) :</span><span class="sxs-lookup"><span data-stu-id="cebed-234">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries \(`Request` and `Response` key/value pairs\):</span></span>  

![Gestionnaire de cache](./media/storage_cache.png)  

### <a name="shortcuts"></a><span data-ttu-id="cebed-236">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="cebed-236">Shortcuts</span></span>  

#### <a name="cache-manager"></a><span data-ttu-id="cebed-237">Gestionnaire de cache</span><span class="sxs-lookup"><span data-stu-id="cebed-237">Cache manager</span></span>  

| <span data-ttu-id="cebed-238">Action</span><span class="sxs-lookup"><span data-stu-id="cebed-238">Action</span></span> | <span data-ttu-id="cebed-239">Raccourci</span><span class="sxs-lookup"><span data-stu-id="cebed-239">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="cebed-240">Actualiser</span><span class="sxs-lookup"><span data-stu-id="cebed-240">Refresh</span></span> | `Ctrl`+`F5` |  
| <span data-ttu-id="cebed-241">Supprimer l’élément</span><span class="sxs-lookup"><span data-stu-id="cebed-241">Delete item</span></span> | `Del` |  
| <span data-ttu-id="cebed-242">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="cebed-242">Copy selected items</span></span> | `Ctrl`+`C` |  
| <span data-ttu-id="cebed-243">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="cebed-243">Select all</span></span> | `Ctrl`+`A` |  
