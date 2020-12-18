---
description: Utiliser le volet stockage pour inspecter votre espace de stockage Web, IndexedDB, les cookies et les caches de requête/réponse
title: DevTools-Storage
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, stockage Web, stockage local, stockage de session, IndexedDB, cookies, travailleur de service, cache
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 90a2e2fdb0f329c3d83f52beb9eba169bdd48520
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232889"
---
# <span data-ttu-id="167c4-104">Stockage</span><span class="sxs-lookup"><span data-stu-id="167c4-104">Storage</span></span>

<span data-ttu-id="167c4-105">Utilisez le volet **stockage** pour inspecter et gérer différentes données mises en cache localement, notamment:</span><span class="sxs-lookup"><span data-stu-id="167c4-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>

 - <span data-ttu-id="167c4-106">Paires clé/valeur de [stockage Web](#local-and-session-storage-managers) (stockage*local* et *session* )</span><span class="sxs-lookup"><span data-stu-id="167c4-106">[Web storage](#local-and-session-storage-managers) (*Local* and *Session* storage) key/values pairs</span></span>
 - <span data-ttu-id="167c4-107">Données structurées en [BD indexées](#indexeddb-manager)</span><span class="sxs-lookup"><span data-stu-id="167c4-107">[Indexed DB](#indexeddb-manager) structured data</span></span>
 - <span data-ttu-id="167c4-108">[Cookies](#cookies-list) pour le domaine</span><span class="sxs-lookup"><span data-stu-id="167c4-108">[Cookies](#cookies-list) for the domain</span></span>
 - <span data-ttu-id="167c4-109">[Cache](#cache-manager) (paires de requête/réponse) pour le débogage de travailleur de service</span><span class="sxs-lookup"><span data-stu-id="167c4-109">[Cache](#cache-manager) (request/response pairs) for service worker debugging</span></span>

<span data-ttu-id="167c4-110">Développez l’une de ces catégories et cliquez sur une entrée enfant pour ouvrir son onglet responsable des ressources.</span><span class="sxs-lookup"><span data-stu-id="167c4-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>

## <span data-ttu-id="167c4-111">Gestionnaires de stockage local et de session</span><span class="sxs-lookup"><span data-stu-id="167c4-111">Local and Session storage managers</span></span>

<span data-ttu-id="167c4-112">Utilisez le *Gestionnaire de stockage local* et le *Gestionnaire de stockage de session* pour inspecter et gérer le stockage Web de votre page.</span><span class="sxs-lookup"><span data-stu-id="167c4-112">Use the *Local Storage manager* and *Session Storage manager* to inspect and manage the web storage for  your page.</span></span> 

<span data-ttu-id="167c4-113">Les dossiers **stockage local** et **stockage de sessions** dans le sélecteur de [*ressources*](./debugger.md#resource-picker) du panneau de stockage affichent une liste d’origines pour la page.</span><span class="sxs-lookup"><span data-stu-id="167c4-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [*Resource picker*](./debugger.md#resource-picker) display a list of origins for the page.</span></span> <span data-ttu-id="167c4-114">La sélection de l’une de ces images permet d’ouvrir une table modifiable des paires clé/valeur actuelles définies via [Window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) ou [Window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivement (et/ou définie directement depuis la [liste de stockage](#storage-list)devtools).</span><span class="sxs-lookup"><span data-stu-id="167c4-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively (and/or set directly from the  DevTools [Storage list](#storage-list)).</span></span>

![Gestionnaire de stockage local DevTools](./media/storage_web_storage.png)

<span data-ttu-id="167c4-116">Dans les onglets stockage *local* et *stockage de session* , vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="167c4-116">From the *Local Storage* and *Session Storage* tabs you can:</span></span>

 - <span data-ttu-id="167c4-117">**Actualiser** ( `Ctrl+F5` ) la [liste de stockage](#cookies-list) pour voir l’ensemble des paires clé/valeur actuelles pour le domaine donné.</span><span class="sxs-lookup"><span data-stu-id="167c4-117">**Refresh** (`Ctrl+F5`) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span> <span data-ttu-id="167c4-118">(La liste n’est pas actualisée automatiquement lors des mises à jour de script.)</span><span class="sxs-lookup"><span data-stu-id="167c4-118">(The list does not auto-refresh upon script updates.)</span></span>
 - <span data-ttu-id="167c4-119">**Simulez la limite de stockage pour le** stockage Web Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="167c4-119">**Simulate reaching the storage limit** for Microsoft Edge web storage.</span></span> <span data-ttu-id="167c4-120">Chaque domaine et sous-domaine dispose de sa propre zone de stockage; Toutefois, il existe une limite combinée:</span><span class="sxs-lookup"><span data-stu-id="167c4-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>
    - <span data-ttu-id="167c4-121">**Sous-domaines:** 5 Mo d’espace</span><span class="sxs-lookup"><span data-stu-id="167c4-121">**Subdomains:** up to 5 MBs of space</span></span>
    - <span data-ttu-id="167c4-122">**Domaines:** jusqu’à 10 Mo d’espace</span><span class="sxs-lookup"><span data-stu-id="167c4-122">**Domains:** up to 10 MBs of space</span></span>
    - <span data-ttu-id="167c4-123">**Total pour tous les domaines:** jusqu’à 50 Mo d’espace</span><span class="sxs-lookup"><span data-stu-id="167c4-123">**Total for all domains:** up to 50 MBs of space</span></span>

   <span data-ttu-id="167c4-124">Le stockage de session est vidé dès que le dernier onglet de navigateur référençant son origine est fermé.</span><span class="sxs-lookup"><span data-stu-id="167c4-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span> <span data-ttu-id="167c4-125">Les entrées de stockage local sont conservées indéfiniment jusqu’à ce qu’elles soient effacées par programme par la page ou manuellement par l’utilisateur:</span><span class="sxs-lookup"><span data-stu-id="167c4-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>

   <span data-ttu-id="167c4-126">**Paramètres**  >  **Effacer les données**  >  de navigation **Cookies et données de sites Web enregistrées**</span><span class="sxs-lookup"><span data-stu-id="167c4-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

![Effacer les données de navigation du panneau Paramètres de Microsoft Edge](./media/settings_clear_browsing_data.png)

### <span data-ttu-id="167c4-128">Liste de stockage</span><span class="sxs-lookup"><span data-stu-id="167c4-128">Storage list</span></span>

<span data-ttu-id="167c4-129">Dans le tableau *liste des stockages* , vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="167c4-129">From the *Storage list* table you can:</span></span>

 - <span data-ttu-id="167c4-130">**Examinez et triez** vos paires clé/valeur en cliquant sur le nom d’une colonne dans la table.</span><span class="sxs-lookup"><span data-stu-id="167c4-130">**Inspect and sort** your key/value pairs by clicking on either column name in the table.</span></span>
 - <span data-ttu-id="167c4-131">**Modifiez** la *clé* et la *valeur* d’une entrée existante en cliquant dans la cellule.</span><span class="sxs-lookup"><span data-stu-id="167c4-131">**Edit** the *Key* and *Value* of an existing entry by clicking in the cell.</span></span>
 - <span data-ttu-id="167c4-132">**Supprimer** ( `Del` ) une entrée de l’option de menu contextuel, cliquez sur *Supprimer l’élément*.</span><span class="sxs-lookup"><span data-stu-id="167c4-132">**Delete** (`Del`) an entry from the right-click context menu option, *Delete item*.</span></span>
 - <span data-ttu-id="167c4-133">**Ajoutez** un nouveau couple clé/valeur en cliquant sur la ligne vide en bas du tableau.</span><span class="sxs-lookup"><span data-stu-id="167c4-133">**Add** a new key/value pair by clicking on the empty row at the bottom of the table.</span></span>


### <span data-ttu-id="167c4-134">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="167c4-134">Shortcuts</span></span>

| <span data-ttu-id="167c4-135">Action</span><span class="sxs-lookup"><span data-stu-id="167c4-135">Action</span></span>              | <span data-ttu-id="167c4-136">Raccourci</span><span class="sxs-lookup"><span data-stu-id="167c4-136">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="167c4-137">Actualiser</span><span class="sxs-lookup"><span data-stu-id="167c4-137">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="167c4-138">Supprimer l’élément</span><span class="sxs-lookup"><span data-stu-id="167c4-138">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="167c4-139">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="167c4-139">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="167c4-140">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="167c4-140">Select all</span></span>          | `Ctrl` + `A`  |


## <span data-ttu-id="167c4-141">Gestionnaire de IndexedDB</span><span class="sxs-lookup"><span data-stu-id="167c4-141">IndexedDB manager</span></span>

<span data-ttu-id="167c4-142">Utilisez l’onglet **IndexedDB** pour inspecter et gérer les données structurées stockées localement sur un ordinateur client.</span><span class="sxs-lookup"><span data-stu-id="167c4-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span> <span data-ttu-id="167c4-143">Plus précisément, vous pouvez inspecter, trier et actualiser vos magasins d’objets et index, et supprimer des entrées clé-valeur individuelles.</span><span class="sxs-lookup"><span data-stu-id="167c4-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>

> [!TIP]
> <span data-ttu-id="167c4-144">Vous pouvez utiliser notre démonstration de [mixage audio](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) pour tester Drive *IndexedDB Manager* dans Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="167c4-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>

<span data-ttu-id="167c4-145">Pour supprimer toutes les données de IndexedDB stockées pour l’utilisateur actuel dans Microsoft Edge, utilisez le menu *paramètres* Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="167c4-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge *Settings* menu:</span></span>

<span data-ttu-id="167c4-146">**...** >  **Paramètres**  >  **Effacer les données**  >  de navigation **Cookies et données de sites Web enregistrées**</span><span class="sxs-lookup"><span data-stu-id="167c4-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

<span data-ttu-id="167c4-147">Le dossier **IndexedDB** dans le [*Sélecteur de ressources*](./debugger.md#resource-picker) du débogueur affiche une liste des origines provenant des ressources chargées par la page.</span><span class="sxs-lookup"><span data-stu-id="167c4-147">The **IndexedDB** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="167c4-148">Toutes les bases de données IndexedDB (IDB) seront répertoriées sous l’origine, ainsi que leurs magasins d’objets.</span><span class="sxs-lookup"><span data-stu-id="167c4-148">Any IndexedDB (IDB) databases will be listed under the origin, along with their object stores.</span></span> 

![DevTools IndexedDB Manager](./media/storage_indexeddb.png)

### <span data-ttu-id="167c4-150">Barre d’outils IndexedDB</span><span class="sxs-lookup"><span data-stu-id="167c4-150">IndexedDB Toolbar</span></span>

<span data-ttu-id="167c4-151">À partir de la barre d’outils *IndexedDB* , vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="167c4-151">From the *IndexedDB* toolbar you can:</span></span>

 - <span data-ttu-id="167c4-152">**Actualiser** ( `Ctrl+F5` ) pour voir les entrées actuelles dans le magasin d’objets ou l’index de votre base de données.</span><span class="sxs-lookup"><span data-stu-id="167c4-152">**Refresh** (`Ctrl+F5`) to see the current entries in the object store or index of your database.</span></span> <span data-ttu-id="167c4-153">Le gestionnaire IndexedDB n’actualise pas automatiquement les modifications apportées à votre base de données.</span><span class="sxs-lookup"><span data-stu-id="167c4-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>

### <span data-ttu-id="167c4-154">Liste d’entrées du magasin d’objets</span><span class="sxs-lookup"><span data-stu-id="167c4-154">Object store entries list</span></span>

<span data-ttu-id="167c4-155">Dans la table *magasin d’objets* ou *index* , vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="167c4-155">From the *Object store* or *Index* table you can:</span></span>

 - <span data-ttu-id="167c4-156">**Recherchez et triez** vos paires clé-valeur en cliquant sur n’importe quel nom de colonne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="167c4-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="167c4-157">**Actualiser** ( `Ctrl+F5` )</span><span class="sxs-lookup"><span data-stu-id="167c4-157">**Refresh** (`Ctrl+F5`)</span></span>
 - <span data-ttu-id="167c4-158">**Supprimer l’élément** ( `Del` ) pour supprimer l’entrée sélectionnée dans votre magasin d’objets ou dans votre index.</span><span class="sxs-lookup"><span data-stu-id="167c4-158">**Delete item** (`Del`) to remove the selected entry in your object store or index.</span></span> <span data-ttu-id="167c4-159">Vous pouvez également effectuer cette opération à partir de l’option de [menu contextuel](#context-menu) , puis *Supprimer l’élément*.</span><span class="sxs-lookup"><span data-stu-id="167c4-159">You can also do this from the right-click [context menu](#context-menu) option, *Delete item*.</span></span>
 - <span data-ttu-id="167c4-160">**Copier les éléments sélectionnés** ( `Ctrl+C` ) pour copier l’élément sélectionné dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="167c4-160">**Copy selected items** (`Ctrl+C`) to copy the selected item to your clipboard.</span></span> <span data-ttu-id="167c4-161">Vous pouvez également effectuer cette opération à partir de l’option de [menu contextuel](#context-menu) , puis *copier l’élément sélectionné*.</span><span class="sxs-lookup"><span data-stu-id="167c4-161">You can also do this from the right-click [context menu](#context-menu) option, *Copy selected item*.</span></span>
 - <span data-ttu-id="167c4-162">**Sélectionner tout** ( `Ctrl+A` ) pour sélectionner toutes les entrées de votre magasin d’objets ou de votre index.</span><span class="sxs-lookup"><span data-stu-id="167c4-162">**Select all** (`Ctrl+A`) to select all the entries in your object store or index.</span></span> <span data-ttu-id="167c4-163">Vous pouvez également effectuer cette opération à partir de l’option de [menu contextuel](#context-menu) , puis *Sélectionner tout*.</span><span class="sxs-lookup"><span data-stu-id="167c4-163">You can also do this from the right-click [context menu](#context-menu) option, *Select all*.</span></span>

<span data-ttu-id="167c4-164">Les colonnes du *magasin d’objets* ou de la table d' *index* sont triables:</span><span class="sxs-lookup"><span data-stu-id="167c4-164">The columns of the *Object store* or *Index* table are sortable:</span></span>

<span data-ttu-id="167c4-165">Colonne</span><span class="sxs-lookup"><span data-stu-id="167c4-165">Column</span></span> | <span data-ttu-id="167c4-166">Description</span><span class="sxs-lookup"><span data-stu-id="167c4-166">Description</span></span>
:------------ | :-------------
<span data-ttu-id="167c4-167">Clé</span><span class="sxs-lookup"><span data-stu-id="167c4-167">Key</span></span> | <span data-ttu-id="167c4-168">Nom de la paire clé-valeur (comme *clé primaire*) lors de l’itération sur un magasin d’objets; Nom de la clé d’index (clé actuelle du curseur) lors de l’itération sur un index</span><span class="sxs-lookup"><span data-stu-id="167c4-168">Name of the key-value pair (same as *Primary Key*) when iterating over an object store; Name of the index key (cursor's current key) when iterating over an index</span></span>
<span data-ttu-id="167c4-169">Clé primaire</span><span class="sxs-lookup"><span data-stu-id="167c4-169">Primary Key</span></span> | <span data-ttu-id="167c4-170">Nom de la paire clé-valeur (voir les *documents Web MDN* pour plus d’informations sur les [touches](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)IDB)</span><span class="sxs-lookup"><span data-stu-id="167c4-170">Name of the key-value pair (see *MDN web docs* for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database))</span></span>
<span data-ttu-id="167c4-171">Valeur</span><span class="sxs-lookup"><span data-stu-id="167c4-171">Value</span></span> | <span data-ttu-id="167c4-172">Valeur de la paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="167c4-172">Value of the key-value pair</span></span>

<span data-ttu-id="167c4-173">Pour plus d’informations sur les [concepts et l’utilisation](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)de MDN, voir *documents Web* .</span><span class="sxs-lookup"><span data-stu-id="167c4-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>

### <span data-ttu-id="167c4-174">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="167c4-174">Context menu</span></span>

<span data-ttu-id="167c4-175">En plus de la [barre d’outils *IndexedDB* ](#indexeddb-toolbar), vous pouvez également gérer vos données dans les magasins d’objets ou les index à partir du **menu contextuel** et/ou des [raccourcis](#shortcuts)clavier.</span><span class="sxs-lookup"><span data-stu-id="167c4-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="167c4-176">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="167c4-176">Shortcuts</span></span>

<span data-ttu-id="167c4-177">Action</span><span class="sxs-lookup"><span data-stu-id="167c4-177">Action</span></span> | <span data-ttu-id="167c4-178">Raccourci</span><span class="sxs-lookup"><span data-stu-id="167c4-178">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="167c4-179">Actualiser</span><span class="sxs-lookup"><span data-stu-id="167c4-179">Refresh</span></span> | `Ctrl` + `F5`
<span data-ttu-id="167c4-180">Supprimer la paire clé-valeur</span><span class="sxs-lookup"><span data-stu-id="167c4-180">Delete key-value pair</span></span> | `Del`
<span data-ttu-id="167c4-181">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="167c4-181">Copy selected items</span></span> | `Ctrl` + `C`
<span data-ttu-id="167c4-182">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="167c4-182">Select all</span></span> | `Ctrl` + `A`

## <span data-ttu-id="167c4-183">Gestionnaire de cookies</span><span class="sxs-lookup"><span data-stu-id="167c4-183">Cookies manager</span></span>

<span data-ttu-id="167c4-184">Utilisez le *Gestionnaire de cookies* pour inspecter et gérer les cookies pour le domaine donné.</span><span class="sxs-lookup"><span data-stu-id="167c4-184">Use the *Cookies manager* to inspect and manage the cookies for the given domain.</span></span> 

<span data-ttu-id="167c4-185">Le dossier **cookies** dans le [*Sélecteur de ressources*](./debugger.md#resource-picker) du débogueur affiche une liste des origines provenant des ressources chargées par la page.</span><span class="sxs-lookup"><span data-stu-id="167c4-185">The **Cookies** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="167c4-186">La sélection de l’une de ces images permet d’ouvrir une table qui représente les cookies actifs définis par un en-tête [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) ou via un script avec [document. cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span><span class="sxs-lookup"><span data-stu-id="167c4-186">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>

![Gestionnaire de cookies DevTools](./media/storage_cookies.png)

<span data-ttu-id="167c4-188">Dans la barre d’outils de l’onglet *cookies* , vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="167c4-188">From the *Cookies* tab toolbar you can:</span></span>

 - <span data-ttu-id="167c4-189">**Actualiser** ( `Ctrl+F5` ) [liste des cookies](#cookies-list) pour afficher l’ensemble des cookies actuels pour le domaine donné.</span><span class="sxs-lookup"><span data-stu-id="167c4-189">**Refresh** (`Ctrl+F5`) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span> <span data-ttu-id="167c4-190">(La liste n’est pas actualisée automatiquement.)</span><span class="sxs-lookup"><span data-stu-id="167c4-190">(The list does not auto-refresh.)</span></span>
 - <span data-ttu-id="167c4-191">**Supprimez tous les cookies** ( `Ctrl+Shift+Del` ) (session et permanent) pour le chemin d’accès de la page active.</span><span class="sxs-lookup"><span data-stu-id="167c4-191">**Delete all cookies** (`Ctrl+Shift+Del`) (session and permanent) for the path of the current page.</span></span>
 - <span data-ttu-id="167c4-192">**Supprimez tous les cookies de session** ( `Ctrl+Del` ) pour le chemin d’accès de la page active.</span><span class="sxs-lookup"><span data-stu-id="167c4-192">**Delete all session cookies** (`Ctrl+Del`) for the path of the current page.</span></span>

<span data-ttu-id="167c4-193">Pour effacer entièrement votre *liste de cookies*, il est possible que vous deviez **Effacer tous les cookies du domaine** à partir de la barre d’outils du panneau [**réseau**](./network.md#toolbar) .</span><span class="sxs-lookup"><span data-stu-id="167c4-193">To completely clear your *Cookies list*, you might need to **Clear all cookies for the domain** from the [**Network**](./network.md#toolbar) panel toolbar.</span></span>

### <span data-ttu-id="167c4-194">Liste des cookies</span><span class="sxs-lookup"><span data-stu-id="167c4-194">Cookies list</span></span>

<span data-ttu-id="167c4-195">Dans le tableau *liste des cookies* , vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="167c4-195">From the *Cookies list* table you can:</span></span>

 - <span data-ttu-id="167c4-196">**Recherchez et triez** vos cookies en cliquant sur n’importe quel nom de colonne dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="167c4-196">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="167c4-197">Pour **modifier** le *nom* et la *valeur* d’un cookie existant, cliquez dans la cellule.</span><span class="sxs-lookup"><span data-stu-id="167c4-197">**Edit** the *Name* and *Value* of an existing cookie by clicking in the cell.</span></span>
 - <span data-ttu-id="167c4-198">**Supprimez** ( `Del` ) un cookie de l’option de [menu contextuel](#context-menu) , puis cliquez sur *supprimer le cookie*.</span><span class="sxs-lookup"><span data-stu-id="167c4-198">**Delete** (`Del`) a cookie from the right-click [context menu](#context-menu) option, *Delete cookie*.</span></span>
 - <span data-ttu-id="167c4-199">**Ajoutez** un nouveau cookie de session pour le *domaine/chemin d’accès* indiqué en cliquant sur la ligne vide en bas de la table.</span><span class="sxs-lookup"><span data-stu-id="167c4-199">**Add** a new session cookie for the given *Domain/Path* by clicking on the empty row at the bottom of the table.</span></span> <span data-ttu-id="167c4-200">Cette opération ne fonctionne qu’avec les cookies de session. les cookies permanents (avec des dates d’expiration spécifiques) doivent être définis à l’aide de méthodes traditionnelles.</span><span class="sxs-lookup"><span data-stu-id="167c4-200">This only works for session cookies; permanent cookies (with specific expiry dates) must be set with traditional methods.</span></span> <span data-ttu-id="167c4-201">Les valeurs de *domaine* et de *chemin d’accès* sont renseignées automatiquement en fonction de l’emplacement de la page.</span><span class="sxs-lookup"><span data-stu-id="167c4-201">The *Domain* and *Path* values are auto-filled according to the location of the page.</span></span>

<span data-ttu-id="167c4-202">Les colonnes de la *liste des cookies* sont triables:</span><span class="sxs-lookup"><span data-stu-id="167c4-202">The columns of the *Cookies list* are sortable:</span></span>

<span data-ttu-id="167c4-203">Colonne</span><span class="sxs-lookup"><span data-stu-id="167c4-203">Column</span></span> | <span data-ttu-id="167c4-204">Description</span><span class="sxs-lookup"><span data-stu-id="167c4-204">Description</span></span>
:------------ | :-------------
<span data-ttu-id="167c4-205">Name</span><span class="sxs-lookup"><span data-stu-id="167c4-205">Name</span></span> | <span data-ttu-id="167c4-206">Nom du cookie.</span><span class="sxs-lookup"><span data-stu-id="167c4-206">Name of the cookie</span></span>
<span data-ttu-id="167c4-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="167c4-207">Value</span></span> | <span data-ttu-id="167c4-208">Valeur du cookie</span><span class="sxs-lookup"><span data-stu-id="167c4-208">Value of the cookie</span></span>
<span data-ttu-id="167c4-209">Domaine</span><span class="sxs-lookup"><span data-stu-id="167c4-209">Domain</span></span> | <span data-ttu-id="167c4-210">Nom d’hôte du cookie (risque d’être vide)</span><span class="sxs-lookup"><span data-stu-id="167c4-210">Host name of the cookie (may be empty)</span></span>
<span data-ttu-id="167c4-211">Chemin d'accès</span><span class="sxs-lookup"><span data-stu-id="167c4-211">Path</span></span> | <span data-ttu-id="167c4-212">Chemin URL du cookie (risque d’être vide)</span><span class="sxs-lookup"><span data-stu-id="167c4-212">URL path for the cookie (may be empty)</span></span>
<span data-ttu-id="167c4-213">Arrive à expiration</span><span class="sxs-lookup"><span data-stu-id="167c4-213">Expires</span></span> | <span data-ttu-id="167c4-214">Durée de vie maximale du cookie en tant qu’horodatage HTTP-date.</span><span class="sxs-lookup"><span data-stu-id="167c4-214">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span> <span data-ttu-id="167c4-215">Si aucun `Expires` ou `Max-Age` n’a été défini, l’entrée est considérée comme un cookie de *session* .</span><span class="sxs-lookup"><span data-stu-id="167c4-215">If no `Expires` or `Max-Age` was set, the entry is considered a *Session* cookie.</span></span>
<span data-ttu-id="167c4-216">HTTP uniquement</span><span class="sxs-lookup"><span data-stu-id="167c4-216">HTTP only</span></span> | <span data-ttu-id="167c4-217">Indique si le cookie a été défini avec une `HttpOnly` directive, indiquant qu’il n’est pas accessible à partir de JavaScript</span><span class="sxs-lookup"><span data-stu-id="167c4-217">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span>
<span data-ttu-id="167c4-218">Sécuriser</span><span class="sxs-lookup"><span data-stu-id="167c4-218">Secure</span></span> | <span data-ttu-id="167c4-219">Indique si le cookie a été défini avec la `Secure` directive, indiquant qu’il sera uniquement envoyé au serveur à partir d’une demande utilisant SSL et le protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="167c4-219">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>

<span data-ttu-id="167c4-220">Pour plus d’informations sur les propriétés de cookie, voir la référence de l’ensemble de **documents Web MDN** [-cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) .</span><span class="sxs-lookup"><span data-stu-id="167c4-220">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>

### <span data-ttu-id="167c4-221">Menu contextuel</span><span class="sxs-lookup"><span data-stu-id="167c4-221">Context menu</span></span>

<span data-ttu-id="167c4-222">Outre la [barre d’outils](#cookies-manager)de l’onglet *cookies* , vous pouvez également gérer vos cookies à partir du **menu contextuel** et/ou des [raccourcis](#shortcuts)clavier.</span><span class="sxs-lookup"><span data-stu-id="167c4-222">In addition to the *Cookies* tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="167c4-223">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="167c4-223">Shortcuts</span></span>

| <span data-ttu-id="167c4-224">Action</span><span class="sxs-lookup"><span data-stu-id="167c4-224">Action</span></span>                     | <span data-ttu-id="167c4-225">Raccourci</span><span class="sxs-lookup"><span data-stu-id="167c4-225">Shortcut</span></span>                 |
|:---------------------------|:-------------------------|
| <span data-ttu-id="167c4-226">Actualiser</span><span class="sxs-lookup"><span data-stu-id="167c4-226">Refresh</span></span>                    | `Ctrl` + `F5`            |
| <span data-ttu-id="167c4-227">Supprimer le cookie</span><span class="sxs-lookup"><span data-stu-id="167c4-227">Delete cookie</span></span>              | `Del`                    |
| <span data-ttu-id="167c4-228">Supprimer tous les cookies</span><span class="sxs-lookup"><span data-stu-id="167c4-228">Delete all cookies</span></span>         | `Ctrl` + `Shift` + `Del` |
| <span data-ttu-id="167c4-229">Supprimer tous les cookies de session</span><span class="sxs-lookup"><span data-stu-id="167c4-229">Delete all session cookies</span></span> | `Ctrl` + `Del`           |
| <span data-ttu-id="167c4-230">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="167c4-230">Copy selected items</span></span>        | `Ctrl` + `C`             |
| <span data-ttu-id="167c4-231">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="167c4-231">Select all</span></span>                 | `Ctrl` + `A`             |

### <span data-ttu-id="167c4-232">Gestionnaire de cache</span><span class="sxs-lookup"><span data-stu-id="167c4-232">Cache manager</span></span>

<span data-ttu-id="167c4-233">Le fait de cliquer sur une entrée de cache spécifique ouvre le gestionnaire de **cache** du travailleur du service, dans lequel vous pouvez inspecter et éventuellement supprimer des entrées de cache (paires*requête* */clé/* valeur):</span><span class="sxs-lookup"><span data-stu-id="167c4-233">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs):</span></span>

![Gestionnaire de cache](./media/storage_cache.png)

### <span data-ttu-id="167c4-235">Raccourcis</span><span class="sxs-lookup"><span data-stu-id="167c4-235">Shortcuts</span></span>

#### <span data-ttu-id="167c4-236">Gestionnaire de cache</span><span class="sxs-lookup"><span data-stu-id="167c4-236">Cache manager</span></span>

| <span data-ttu-id="167c4-237">Action</span><span class="sxs-lookup"><span data-stu-id="167c4-237">Action</span></span>              | <span data-ttu-id="167c4-238">Raccourci</span><span class="sxs-lookup"><span data-stu-id="167c4-238">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="167c4-239">Actualiser</span><span class="sxs-lookup"><span data-stu-id="167c4-239">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="167c4-240">Supprimer l’élément</span><span class="sxs-lookup"><span data-stu-id="167c4-240">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="167c4-241">Copier les éléments sélectionnés</span><span class="sxs-lookup"><span data-stu-id="167c4-241">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="167c4-242">Tout sélectionner</span><span class="sxs-lookup"><span data-stu-id="167c4-242">Select all</span></span>          | `Ctrl` + `A`  |
