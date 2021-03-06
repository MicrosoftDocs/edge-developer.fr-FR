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
# <a name="storage"></a>Stockage

Utilisez le **panneau de** stockage pour inspecter et gérer diverses données mises en cache localement, notamment :  

*   [Paires](#local-and-session-storage-managers) clé/valeurs de stockage Web \(Stockage local et de session\)  
*   [Données structurées de base de données](#indexeddb-manager) indexées  
*   [Cookies](#cookies-list) pour le domaine  
*   [Cache](#cache-manager) \(request/response pairs\) for service worker debugging  

Développez l’une de ces catégories et cliquez sur une entrée enfant pour ouvrir l’onglet Gestionnaire de ressources.  

## <a name="local-and-session-storage-managers"></a>Responsables de stockage local et de session  

Utilisez le gestionnaire de stockage local et le gestionnaire de stockage de session pour inspecter et gérer le stockage web de votre page.  

Les **dossiers Stockage local** et **Stockage** de [](./debugger.md#resource-picker) session à l’intérieur du s sélectionneur de ressources du panneau de stockage affichent la liste des origines de la page.  La sélection de l’une de ces images ouvre une table modifiable des paires clé/valeur actuelles définies via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) ou [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivement \(et/ou définies directement à partir de la liste de stockage DevTools [](#storage-list)\).  

![Gestionnaire de stockage DevTools](./media/storage_web_storage.png)  

Dans les onglets Stockage local et Stockage de session, vous pouvez :  

*   **Actualisez** \( \) la liste de stockage pour voir l’ensemble actuel de `Ctrl+F5` paires [](#cookies-list) clé/valeurs pour le domaine donné.  \(La liste n’est pas actualisée automatiquement lors des mises à jour de script.\)  
*   **Simulez l’atteinte de la limite de**  stockage pour le stockage web Microsoft Edge.  Chaque domaine et sous-domaine possède sa propre zone de stockage, mais il existe une limite combinée :  
    *   **Sous-domaine :** jusqu’à 5 Mo d’espace  
    *   **Domaines :** jusqu’à 10 Mo d’espace  
    *   **Total pour tous les domaines**: jusqu’à 50 Mo d’espace  

   Le stockage de session est effacé dès que le dernier onglet du navigateur référent à son origine est fermé.  Les entrées de stockage local persistent indéfiniment jusqu’à ce qu’elles soient effacées par programme par la page ou manuellement par l’utilisateur :  

   **Paramètres**  >  **Effacer les données de navigation**  >  **Cookies et données de site web enregistrées**  

![Effacer les données de navigation du panneau Paramètres de Microsoft Edge](./media/settings_clear_browsing_data.png)  

### <a name="storage-list"></a>Liste de stockage  

À partir de la table de liste stockage, vous pouvez :  

*   **Inspectez et tez** `key/value` vos paires en cliquant sur l’un ou l’autre nom de colonne du tableau.  
*   **Modifiez** `Key` le et une entrée existante en `Value` cliquant dans la cellule.  
*   **Supprimer** \( \) une entrée à partir de l’option de menu context le clic `Del` droit, **Supprimer l’élément**.  
*   **Ajoutez** une `key/value` nouvelle paire en cliquant sur la ligne vide en bas du tableau.  

### <a name="shortcuts"></a>Raccourcis

| Action | Raccourci |  
|:--- |:--- |  
| Actualiser | `Ctrl`+`F5` |  
| Supprimer l’élément | `Del` |  
| Copier les éléments sélectionnés | `Ctrl`+`C` |  
| Tout sélectionner | `Ctrl`+`A` |  

## <a name="indexeddb-manager"></a>Gestionnaire IndexedDB  

Utilisez **l’onglet IndexedDB** pour inspecter et gérer les données structurées stockées localement sur un ordinateur client.  Plus précisément, vous pouvez inspecter/trier et actualiser vos magasins d’objets et index, ainsi que supprimer des entrées clé-valeur individuelles.  

> [!TIP]
> Vous pouvez utiliser notre [démonstration Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) pour tester le gestionnaire *IndexedDB* dans Microsoft Edge DevTools.  

Pour supprimer toutes les données IndexedDB stockées pour l’utilisateur actuel dans Microsoft Edge, utilisez le menu **Paramètres** de Microsoft Edge :  

**...** >  **Paramètres**  >  **Effacer les données de navigation**  >  **Cookies et données de site web enregistrées**  

Le dossier à l’intérieur du s sélectionneur de ressources du débogger affiche la liste des origines des `IndexedDB` ressources chargées par la page. [](./debugger.md#resource-picker)  Toutes les bases de données IndexedDB \(IDB\) sont répertoriées sous l’origine, ainsi que leurs magasins d’objets.  

![Gestionnaire IndexedDB DevTools](./media/storage_indexeddb.png)  

### <a name="indexeddb-toolbar"></a>Barre d’outils IndexedDB  

À partir de la barre d’outils IndexedDB, vous pouvez :  

*   **Actualisez** \( \) pour voir les entrées actuelles dans le magasin d’objets ou `Ctrl` + `F5` l’index de votre base de données.  Le gestionnaire IndexedDB n’est pas actualisé automatiquement lorsque des modifications sont apportées à votre base de données.  

### <a name="object-store-entries-list"></a>Liste des entrées du magasin d’objets  

À partir du magasin d’objets ou de la table Index, vous pouvez :  

*   **Inspectez et tez** vos paires clé-valeur en cliquant sur n’importe quel nom de colonne du tableau.  
*   **Refresh** \( `Ctrl` + `F5` \)  
*   **Supprimez l’élément** \( \) pour supprimer l’entrée sélectionnée dans votre magasin `Del` d’objets ou index.  Vous pouvez également le faire à partir de l’option de [menu](#context-menu) context un clic droit, **Supprimer l’élément.**  
*   **Copiez les éléments sélectionnés** \( \) pour copier l’élément `Ctrl` + `C` sélectionné dans votre Presse-papiers.  Vous pouvez également le faire à partir de l’option de [menu](#context-menu) context un clic droit, **Copier l’élément sélectionné.**  
*   **Sélectionnez toutes** les \( \) pour sélectionner toutes les entrées de votre magasin `Ctrl` + `A` d’objets ou index.  Vous pouvez également le faire à partir de l’option de menu contexto de [clic](#context-menu) droit, **Sélectionner tout.**  

Les colonnes du magasin d’objets ou de la table Index sont triables :  

| Colonne | Description |  
|:--- |:--- |  
| Clé | Nom de la paire clé-valeur \(identique à **la**clé primaire \) lors de l’itère sur un magasin d’objets ; Nom de la clé d’index \(clé actuelle du curseur\) lors d’une itération sur un index |  
| Clé primaire | Nom de la paire clé-valeur \(voir **documents web MDN** pour plus d’informations sur les clés [IDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)\) |  
| Valeur | Valeur de la paire clé-valeur |  

Consultez des *documents web MDN pour* en savoir plus sur les concepts et l’utilisation [d’IndexedDB.](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)  

### <a name="context-menu"></a>Menu contextuel  

Outre la barre d’outils [ *IndexedDB,* ](#indexeddb-toolbar)vous pouvez également gérer vos données dans les magasins d’objets ou les index à partir du **menu** Context et/ou des [raccourcis clavier.](#shortcuts)  

### <a name="shortcuts"></a>Raccourcis

| Action | Raccourci |  
|:--- |:--- |  
| Actualiser | `Ctrl`+`F5` |  
| Supprimer la paire clé-valeur | `Del` |  
| Copier les éléments sélectionnés | `Ctrl`+`C` |  
| Tout sélectionner | `Ctrl +`A' |  

## <a name="cookies-manager"></a>Gestionnaire de cookies  

Utilisez le Gestionnaire de cookies pour inspecter et gérer les cookies pour le domaine donné.  

Le dossier à l’intérieur du s sélectionneur de ressources du débogger affiche la liste des origines des `Cookies` ressources chargées par la page. [](./debugger.md#resource-picker)  La sélection de l’une de ces images ouvre une table représentant les cookies actuels, définies par l’en-tête [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) ou via un script avec [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).  

![Gestionnaire de cookies DevTools](./media/storage_cookies.png)  

À partir de la barre d’outils de l’onglet Cookies, vous pouvez :  

*   **Actualisez** \( \) la liste cookies pour voir l’ensemble actuel de `Ctrl` + `F5` cookies pour le domaine donné. [](#cookies-list)  \(La liste n’est pas actualisée automatiquement.\)  
*   **Supprimez tous les cookies** \( `Ctrl` + `Shift` + `Del` \) \(session et permanent\) pour le chemin d’accès de la page actuelle.  
*   **Supprimez tous les cookies de session** \( `Ctrl` + `Del` \) pour le chemin d’accès de la page actuelle.  

Pour effacer complètement votre liste de cookies, vous devrez peut-être effacer tous les **cookies** pour le domaine à partir de la [barre d’outils](./network.md#toolbar) du panneau réseau.  

### <a name="cookies-list"></a>Liste des cookies  

À partir du tableau de liste cookies, vous pouvez :  

*   **Inspectez et tez** vos cookies en cliquant sur n’importe quel nom de colonne dans le tableau.  
*   **Modifiez** `Name` le cookie existant en `Value` cliquant dans la cellule.  
*   **Supprimez** \( `Del` \) un cookie à partir de l’option de [menu contextiqué avec](#context-menu) le bouton droit, `Delete cookie` .  
*   **Ajoutez** un nouveau cookie de session pour l’donnée en cliquant sur la `Domain/Path` ligne vide en bas du tableau.  Cela fonctionne uniquement pour les cookies de session ; les cookies permanents \(avec des dates d’expiration spécifiques\) doivent être définies avec des méthodes traditionnelles.  Les `Domain` `Path` valeurs et les valeurs sont remplies automatiquement en fonction de l’emplacement de la page.  

Les colonnes de la liste cookies peuvent être triées :

| Colonne | Description |  
| :--- | :--- |  
| Name | Nom du cookie |  
| Valeur | Valeur du cookie |  
| Domaine | Nom d’hôte du cookie \(peut être vide\) |  
| Chemin d'accès | Chemin d’URL du cookie \(peut être vide\) |  
| Arrive à expiration | Durée de vie maximale du cookie sous la forme d’un timestamp HTTP-date.  Si aucune `Expires` entrée ou `Max-Age` n’a été définie, l’entrée est considérée comme un cookie de session.  |  
| HTTP uniquement | Indique si le cookie a été définie avec une directive, indiquant qu’il est `HttpOnly` inaccessible à partir de JavaScript |  
| Sécuriser | Indique si le cookie a été définie avec la directive, indiquant qu’il sera uniquement envoyé au serveur à partir d’une demande à l’aide de `Secure` SSL et du protocole HTTPS.  |  

Pour plus **d’informations sur** les propriétés des cookies, voir la référence [set-cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) de la documentation web MDN.  

### <a name="context-menu"></a>Menu contextuel  

Outre la barre d’outils de l’onglet [Cookies,](#cookies-manager)vous pouvez également gérer vos cookies à partir du **menu** Context et/ou des [raccourcis clavier.](#shortcuts)  

### <a name="shortcuts"></a>Raccourcis  

| Action | Raccourci |  
|:--- |:--- |  
| Actualiser | `Ctrl`+`F5` |  
| Supprimer un cookie | `Del` |  
| Supprimer tous les cookies | `Ctrl`+`Shift`+`Del` |  
| Supprimer tous les cookies de session | `Ctrl`+`Del` |  
| Copier les éléments sélectionnés | `Ctrl`+`C` |  
| Tout sélectionner | `Ctrl`+`A` |  

### <a name="cache-manager"></a>Gestionnaire de cache  

Cliquer sur une entrée de cache spécifique **** ouvre le gestionnaire de cache de travail du service, où vous pouvez inspecter et éventuellement supprimer des entrées de cache \( et `Request` `Response` paires clé/valeur\) :  

![Gestionnaire de cache](./media/storage_cache.png)  

### <a name="shortcuts"></a>Raccourcis  

#### <a name="cache-manager"></a>Gestionnaire de cache  

| Action | Raccourci |  
|:--- |:--- |  
| Actualiser | `Ctrl`+`F5` |  
| Supprimer l’élément | `Del` |  
| Copier les éléments sélectionnés | `Ctrl`+`C` |  
| Tout sélectionner | `Ctrl`+`A` |  
