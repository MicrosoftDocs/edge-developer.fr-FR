---
description: Trouvez des informations sur les clés de manifeste prises en charge et leurs problèmes connus/compatibilités chrome.
title: Extensions-clés de manifeste prises en charge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f8413193ddb834eb7e31e4101c2b027c48bc501d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233492"
---
# Clés de manifeste prises en charge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Chaque extension possède un fichier manifeste au format JSON, nommé manifest.jsactivé. Ce fichier fournit des informations importantes concernant l’extension, dont son nom à ses autorisations. Sauf indication contraire dans une note ci-dessous, les propriétés de manifeste Microsoft Edge suivent la même implémentation que Chrome.

Voici un exemple de [fichier manifeste JSON Microsoft Edge](./supported-manifest-keys/json-manifest-example.md).

## Clés requises

Les clés suivantes sont nécessaires:

Clé | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :--------------
[auteur](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author)  | | 
[name](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) | | |
[version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/version) | | |

## Raccourcis clavier recommandés

Les clés suivantes sont recommandées:

Clé | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :--------------
browser_specific_settings | | Indique l’État préféré de l’extension dans le navigateur. Le navigateur peut ou non choisir de le respecter dans une version ultérieure, en fonction de facteurs tels que la réputation de l’extension ou le nombre total de boutons déjà présents dans la barre d’adresses de l’utilisateur. Ce paramètre peut être utilisé pour indiquer la position par défaut de l' `browserAction` icône. </br></br> `"browser_specific_settings": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;`"edge": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`"browser_action_next_to_addressbar": true`</br>&nbsp;&nbsp;&nbsp;&nbsp;`}`</br>`}` </br></br> Non pris en charge dans Chrome.|
[default_locale](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/default_locale)| | |
[description](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/description) | | |
[icônes](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/icons) | | |
[manifest_version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/manifest_version) | | Actuellement ignorées dans Microsoft Edge.



## touches browser_action ou page_action

Vous ne pouvez inclure qu’une des touches suivantes (ou aucune):

Clé | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :--------------
[browser_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action)  | | Microsoft Edge ne prend pas en charge la syntaxe suivante:  `browser_action : {"default_icon" : "icon.png" }`   <br/>La taille des icônes doit être spécifiée. <br/>Tailles par défaut: 20px, 25px, 30px, 40px. <br/> Autres tailles prises en charge: 19px, 35px, 38px.|
[page_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action) | | Microsoft Edge ne prend pas en charge la syntaxe suivante:  `page_action : {"default_icon" : "icon.png" }`   <br/>La taille des icônes doit être spécifiée. <br/>Tailles par défaut: 20px, 25px, 30px, 40px. <br/>Autres tailles prises en charge: 19px, 35px, 38px.|

## Clés facultatives

Les clés suivantes sont facultatives:

Clé | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :--------------
[arrière-plan](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/background) | | Le champ permanent est requis pour Microsoft Edge.
[content_scripts](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/content_scripts)  | | |
[content_security_policy](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_security_policy)  | La stratégie de sécurité du contenu d’une page bloque les WebSockets dans les scripts de contenu et génère une exception non définie. | Pour l’instant, les extensions Microsoft Edge prennent uniquement en charge les [restrictions de stratégie par défaut](https://developer.mozilla.org/Add-ons/WebExtensions/Content_Security_Policy#Default_content_security_policy): `script-src 'self'; object-src 'self'` |
[Incognito](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/incognito) | | | 
key  | | |
options_page | | |
[attribué](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions)  | | |
short_name  | | |
[web_accessible_resources](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/web_accessible_resources) | | |

### Autorisations prises en charge
Les [autorisations](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions) suivantes sont prises en charge:


| Autorisation         | Description                                                                                                                                                                                                                                                                         |
|:-------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<all_urls\>       | Autorise les scripts d’arrière-plan et de contenu à interagir avec toutes les pages Web avec [des privilèges](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions#Host_permissions)supplémentaires.                                                                                  |
| contextMenus       | Donne accès à l' `contextMenus` API. Cela permet d’ajouter des éléments au menu contextuel de Microsoft Edge.                                                                                                                                                                                     |
| les            | Donne accès à l' `cookies` API. Cela permet d’interroger et de modifier les cookies ainsi que de recevoir des notifications en cas de changement.                                                                                                                                                           |
| géolocalisation        | Autorisez l’extension à utiliser l' `geolocation` API HTML5 sans demander l’autorisation de l’utilisateur.                                                                                                                                                                                   |
| inactif               | Donne accès à l' `idle` API. Cela permet de détecter l’état inactif de l’ordinateur.                                                                                                                                                                                    |
| stockage            | Donne accès à l' `storage` API. Cela permet de stocker, récupérer et suivre les modifications apportées aux données utilisateur.                                                                                                                                                                             |
| eux               | Donne accès à l' `tabs` API pour interagir avec le système de tabulation du navigateur. Cela permet de créer, de modifier et de réorganiser les onglets dans le navigateur, y compris les URL associées à chaque onglet.                                                                                       |
| unlimitedStorage   | Autorise [Storage. local](https://developer.mozilla.org/Add-ons/WebExtensions/API/storage/local) à disposer d’un espace de stockage illimité (en fonction des ressources système) au lieu de 5 Mo. Le stockage maximal par paire de valeurs de clé augmente également de 5 Mo au illimité (en fonction des ressources système). |
| Navigation Webnavigation      | Donne accès à l' `webNavigation` API. Cela permet de recevoir des notifications concernant l’état des demandes de navigation.                                                                                                                                                              |
| Instances         | Donne accès à l' `webRequest` API. Cela permet d’observer et d’analyser le trafic, ainsi que d’intercepter, de bloquer ou de modifier la demande en cours de vol.                                                                                                                               |
| webRequestBlocking | Obligatoire si une extension utilise l' `webRequest` API de manière bloquante.                                                                                                                                                                                                           |

'""'
