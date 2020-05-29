---
description: Utiliser le volet stockage pour inspecter votre espace de stockage Web, IndexedDB, les cookies et les caches de requête/réponse
title: DevTools-Storage
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, stockage Web, stockage local, stockage de session, IndexedDB, cookies, travailleur de service, cache
ms.custom: seodec18
ms.openlocfilehash: 8de6e1f90f86fa09b116646918c6be1d8cfb0a72
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565521"
---
# Stockage

Utilisez le volet **stockage** pour inspecter et gérer différentes données mises en cache localement, notamment:

 - Paires clé/valeur de [stockage Web](#local-and-session-storage-managers) (stockage*local* et *session* )
 - Données structurées en [BD indexées](#indexeddb-manager)
 - [Cookies](#cookies-list) pour le domaine
 - [Cache](#cache-manager) (paires de requête/réponse) pour le débogage de travailleur de service

Développez l’une de ces catégories et cliquez sur une entrée enfant pour ouvrir son onglet responsable des ressources.

## Gestionnaires de stockage local et de session

Utilisez le *Gestionnaire de stockage local* et le *Gestionnaire de stockage de session* pour inspecter et gérer le stockage Web de votre page. 

Les dossiers **stockage local** et **stockage de sessions** dans le sélecteur de [*ressources*](./debugger.md#resource-picker) du panneau de stockage affichent une liste d’origines pour la page. La sélection de l’une de ces images permet d’ouvrir une table modifiable des paires clé/valeur actuelles définies via [Window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) ou [Window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectivement (et/ou définie directement depuis la [liste de stockage](#storage-list)devtools).

![Gestionnaire de cookies DevTools](./media/storage_web_storage.png)

Dans les onglets stockage *local* et *stockage de session* , vous pouvez:

 - **Actualiser** ( `Ctrl+F5` ) la [liste de stockage](#cookies-list) pour voir l’ensemble des paires clé/valeur actuelles pour le domaine donné. (La liste n’est pas actualisée automatiquement lors des mises à jour de script.)
 - **Simulez la limite de stockage pour le** stockage Web Microsoft Edge. Chaque domaine et sous-domaine dispose de sa propre zone de stockage; Toutefois, il existe une limite combinée:
    - **Sous-domaines:** 5 Mo d’espace
    - **Domaines:** jusqu’à 10 Mo d’espace
    - **Total pour tous les domaines:** jusqu’à 50 Mo d’espace

   Le stockage de session est vidé dès que le dernier onglet de navigateur référençant son origine est fermé. Les entrées de stockage local sont conservées indéfiniment jusqu’à ce qu’elles soient effacées par programme par la page ou manuellement par l’utilisateur:

   **Paramètres**  >  **Effacer les données**  >  de navigation **Cookies et données de sites Web enregistrées**

![Effacer les données de navigation du panneau Paramètres de Microsoft Edge](./media/settings_clear_browsing_data.png)

### Liste de stockage

Dans le tableau *liste des stockages* , vous pouvez:

 - **Examinez et triez** vos paires clé/valeur en cliquant sur le nom d’une colonne dans la table.
 - **Modifiez** la *clé* et la *valeur* d’une entrée existante en cliquant dans la cellule.
 - **Supprimer** ( `Del` ) une entrée de l’option de menu contextuel, cliquez sur *Supprimer l’élément*.
 - **Ajoutez** un nouveau couple clé/valeur en cliquant sur la ligne vide en bas du tableau.


### Associés

| Action              | Raccourci      |
|:--------------------|:--------------|
| Actualiser             | `Ctrl` + `F5` |
| Supprimer l’élément         | `Del`         |
| Copier les éléments sélectionnés | `Ctrl` + `C`  |
| Tout sélectionner          | `Ctrl` + `A`  |


## Gestionnaire de IndexedDB

Utilisez l’onglet **IndexedDB** pour inspecter et gérer les données structurées stockées localement sur un ordinateur client. Plus précisément, vous pouvez inspecter, trier et actualiser vos magasins d’objets et index, et supprimer des entrées clé-valeur individuelles.

> [!TIP]
> Vous pouvez utiliser notre démonstration de [mixage audio](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) pour tester Drive *IndexedDB Manager* dans Microsoft Edge devtools.

Pour supprimer toutes les données de IndexedDB stockées pour l’utilisateur actuel dans Microsoft Edge, utilisez le menu *paramètres* Microsoft Edge:

**...** >  **Paramètres**  >  **Effacer les données**  >  de navigation **Cookies et données de sites Web enregistrées**

Le dossier **IndexedDB** dans le [*Sélecteur de ressources*](./debugger.md#resource-picker) du débogueur affiche une liste des origines provenant des ressources chargées par la page. Toutes les bases de données IndexedDB (IDB) seront répertoriées sous l’origine, ainsi que leurs magasins d’objets. 

![DevTools IndexedDB Manager](./media/storage_indexeddb.png)

### Barre d’outils IndexedDB

À partir de la barre d’outils *IndexedDB* , vous pouvez:

 - **Actualiser** ( `Ctrl+F5` ) pour voir les entrées actuelles dans le magasin d’objets ou l’index de votre base de données. Le gestionnaire IndexedDB n’actualise pas automatiquement les modifications apportées à votre base de données.

### Liste d’entrées du magasin d’objets

Dans la table *magasin d’objets* ou *index* , vous pouvez:

 - **Recherchez et triez** vos paires clé-valeur en cliquant sur n’importe quel nom de colonne dans le tableau.
 - **Actualiser** ( `Ctrl+F5` )
 - **Supprimer l’élément** ( `Del` ) pour supprimer l’entrée sélectionnée dans votre magasin d’objets ou dans votre index. Vous pouvez également effectuer cette opération à partir de l’option de [menu contextuel](#context-menu) , puis *Supprimer l’élément*.
 - **Copier les éléments sélectionnés** ( `Ctrl+C` ) pour copier l’élément sélectionné dans le presse-papiers. Vous pouvez également effectuer cette opération à partir de l’option de [menu contextuel](#context-menu) , puis *copier l’élément sélectionné*.
 - **Sélectionner tout** ( `Ctrl+A` ) pour sélectionner toutes les entrées de votre magasin d’objets ou de votre index. Vous pouvez également effectuer cette opération à partir de l’option de [menu contextuel](#context-menu) , puis *Sélectionner tout*.

Les colonnes du *magasin d’objets* ou de la table d' *index* sont triables:

Colonne | Description
:------------ | :-------------
Clé | Nom de la paire clé-valeur (comme *clé primaire*) lors de l’itération sur un magasin d’objets; Nom de la clé d’index (clé actuelle du curseur) lors de l’itération sur un index
Clé primaire | Nom de la paire clé-valeur (voir les *documents Web MDN* pour plus d’informations sur les [touches](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)IDB)
Valeur | Valeur de la paire clé-valeur

Pour plus d’informations sur les [concepts et l’utilisation](https://developer.mozilla.org/docs/Web/API/IndexedDB_API)de MDN, voir *documents Web* .

### Menu contextuel

En plus de la [barre d’outils *IndexedDB* ](#indexeddb-toolbar), vous pouvez également gérer vos données dans les magasins d’objets ou les index à partir du **menu contextuel** et/ou des [raccourcis](#shortcuts)clavier.

### Associés

Action | Raccourci
:------------ | :-------------
Actualiser | `Ctrl` + `F5`
Supprimer la paire clé-valeur | `Del`
Copier les éléments sélectionnés | `Ctrl` + `C`
Tout sélectionner | `Ctrl` + `A`

## Gestionnaire de cookies

Utilisez le *Gestionnaire de cookies* pour inspecter et gérer les cookies pour le domaine donné. 

Le dossier **cookies** dans le [*Sélecteur de ressources*](./debugger.md#resource-picker) du débogueur affiche une liste des origines provenant des ressources chargées par la page. La sélection de l’une de ces images permet d’ouvrir une table qui représente les cookies actifs définis par un en-tête [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) ou via un script avec [document. cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).

![Gestionnaire de cookies DevTools](./media/storage_cookies.png)

Dans la barre d’outils de l’onglet *cookies* , vous pouvez:

 - **Actualiser** ( `Ctrl+F5` ) [liste des cookies](#cookies-list) pour afficher l’ensemble des cookies actuels pour le domaine donné. (La liste n’est pas actualisée automatiquement.)
 - **Supprimez tous les cookies** ( `Ctrl+Shift+Del` ) (session et permanent) pour le chemin d’accès de la page active.
 - **Supprimez tous les cookies de session** ( `Ctrl+Del` ) pour le chemin d’accès de la page active.

Pour effacer entièrement votre *liste de cookies*, il est possible que vous deviez **Effacer tous les cookies du domaine** à partir de la barre d’outils du panneau [**réseau**](./network.md#toolbar) .

### Liste des cookies

Dans le tableau *liste des cookies* , vous pouvez:

 - **Recherchez et triez** vos cookies en cliquant sur n’importe quel nom de colonne dans le tableau.
 - Pour **modifier** le *nom* et la *valeur* d’un cookie existant, cliquez dans la cellule.
 - **Supprimez** ( `Del` ) un cookie de l’option de [menu contextuel](#context-menu) , puis cliquez sur *supprimer le cookie*.
 - **Ajoutez** un nouveau cookie de session pour le *domaine/chemin d’accès* indiqué en cliquant sur la ligne vide en bas de la table. Cette opération ne fonctionne qu’avec les cookies de session. les cookies permanents (avec des dates d’expiration spécifiques) doivent être définis à l’aide de méthodes traditionnelles. Les valeurs de *domaine* et de *chemin d’accès* sont renseignées automatiquement en fonction de l’emplacement de la page.

Les colonnes de la *liste des cookies* sont triables:

Colonne | Description
:------------ | :-------------
Name | Nom du cookie.
Valeur | Valeur du cookie
Domaine | Nom d’hôte du cookie (risque d’être vide)
Chemin d’accès | Chemin URL du cookie (risque d’être vide)
Arrive à expiration | Durée de vie maximale du cookie en tant qu’horodatage HTTP-date. Si aucun `Expires` ou `Max-Age` n’a été défini, l’entrée est considérée comme un cookie de *session* .
HTTP uniquement | Indique si le cookie a été défini avec une `HttpOnly` directive, indiquant qu’il n’est pas accessible à partir de JavaScript
Sécuriser | Indique si le cookie a été défini avec la `Secure` directive, indiquant qu’il sera uniquement envoyé au serveur à partir d’une demande utilisant SSL et le protocole HTTPS.

Pour plus d’informations sur les propriétés de cookie, voir la référence de l’ensemble de **documents Web MDN** [-cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) .

### Menu contextuel

Outre la [barre d’outils](#cookies-manager)de l’onglet *cookies* , vous pouvez également gérer vos cookies à partir du **menu contextuel** et/ou des [raccourcis](#shortcuts)clavier.

### Associés

| Action                     | Raccourci                 |
|:---------------------------|:-------------------------|
| Actualiser                    | `Ctrl` + `F5`            |
| Supprimer le cookie              | `Del`                    |
| Supprimer tous les cookies         | `Ctrl` + `Shift` + `Del` |
| Supprimer tous les cookies de session | `Ctrl` + `Del`           |
| Copier les éléments sélectionnés        | `Ctrl` + `C`             |
| Tout sélectionner                 | `Ctrl` + `A`             |

### Gestionnaire de cache

Le fait de cliquer sur une entrée de cache spécifique ouvre le gestionnaire de **cache** du travailleur du service, dans lequel vous pouvez inspecter et éventuellement supprimer des entrées de cache (paires*requête* */clé/* valeur):

![Gestionnaire de cache](./media/storage_cache.png)

### Associés

#### Gestionnaire de cache

| Action              | Raccourci      |
|:--------------------|:--------------|
| Actualiser             | `Ctrl` + `F5` |
| Supprimer l’élément         | `Del`         |
| Copier les éléments sélectionnés | `Ctrl` + `C`  |
| Tout sélectionner          | `Ctrl` + `A`  |
