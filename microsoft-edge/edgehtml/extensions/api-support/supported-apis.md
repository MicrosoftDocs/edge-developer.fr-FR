---
description: Trouvez des informations sur les API actuelles et futures ainsi que leurs problèmes connus/compatibilités chrome.
title: API prises en charge par les extensions
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, développement Web, html, CSS, JavaScript, développeur
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: b8cf13f42c99779f23eaa7b941093752fb25b207
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233495"
---
# API prises en charge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Vous trouverez ci-dessous une liste détaillée de membres API pris en charge. Le développement de la plateforme de extension étant en cours, consultez régulièrement les mises à jour.

> [!NOTE]
>  - Pour Microsoft Edge, toutes les API d’extension font partie de l' `browser` espace de noms, par exemple `browser.browserAction.disable()` .
>  - Les API d’extension Microsoft Edge utilisent des rappels, sans promesse.


## Problèmes de surarc

Les problèmes connus suivants peuvent se présenter sur la plateforme d’extension et être corrigés prochainement:

- Lorsque vous utilisez la `url()` propriété CSS, les URL absolues utilisant ne `ms-browser-extension://` fonctionnent pas comme dans Chrome. Pour éviter ce problème, utilisez à la place des chemins d’accès relatifs aux ressources (en commençant par le répertoire de l’extension racine).
- `window.open()` ne fonctionne pas dans les scripts d’arrière-plan de l’extension. Utilisez-le à la `browser.windows.create()` place.
- Les cookies partagés sont pris en charge, mais le script en arrière-plan de l’extension ne peut pas accéder aux cookies de session définis dans l’onglet avant l’activation de l’extension. Ce problème ne concerne pas les cookies persistants.
- Si seules les autorisations non prises en charge sont spécifiées pour une extension, c.-à-d. `activeTab`, la tentative d’charger de l’extension entraîne la désinstallation de l’extension avec le message suivant: «un problème est survenu avec vos extensions, c’est pourquoi nous devions les réinstaller. Vous devez le réactiver. "
- Le déclenchement d’un téléchargement par le biais d’une balise d’ancrage cachée échoue à partir des scripts en arrière-plan. Pour cela, vous devez effectuer cette opération à partir d’une page de poste.


## favoris

Les `bookmarks` API suivantes sont prises en charge:

| API                                   | Problèmes connus                                             | Incompatibilités chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [favoris](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks) | | |
| [signets. créer](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/create) | | |
| [signets. supprimer](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/remove) | | |
| [signets. getTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/getTree) |  | |
| [signets. déplacer](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/move) | | |
| [signets. removeTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/removeTree) | | |
| [signets. mettre à jour](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/update)            | | |


## browserAction

Les `browserAction` API suivantes sont prises en charge:

| API                                   | Problèmes connus                                             | Incompatibilités chrome
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [browserAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction) | | |
| [browserAction. Disable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/disable) | | |
| [browserAction. Enable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/enable) | | |
| [browserAction.getBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeBackgroundColor) |  | |
| [browserAction.setBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeBackgroundColor) | | |
| [browserAction.onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/onClicked) | | |
| [browserAction.setBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeText)            | | |
| [browserAction.setPopup](https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setPopup)  | | |
| [browserAction.getBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeText)   | | |
| [browserAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setIcon) | `browserAction.setIcon` ne persiste pas. <br/><br/> Le `imageData` paramètre n’est pas pris en charge. <br/><br/> `path` est un paramètre obligatoire.| |
| [browserAction. getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getTitle) | | |
| [browserAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setTitle) | | |

## contextMenus

Les `contextMenus` API suivantes sont prises en charge:

| API                    | Problèmes connus | Incompatibilités chrome
|------------------------|--------------|----------------------|
| [contextMenus](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus)  |  | |
| [contextMenus. ContextType](https://developer.mozilla.org/Add-ons/WebExtensions/API/contextMenus/ContextType) | `"page_action"` `ContextType` ne s’affiche pas dans le menu contextuel d’action de la page.| Microsoft Edge ne prend pas en charge le `"launcher"` `ContextType` .|
| [contextMenus. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/create)    | Lorsque les extensions ne fournissent pas a `contextmenuid` , le `id` généré n’est pas unique. | |
| [contextMenus.onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/onClicked) | | |
| [contextMenus. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/remove) | | |
| [contextMenus. removeAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/removeAll) | | |
| [contextMenus. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/update) | | |

## les

Les `cookies` API suivantes sont prises en charge:

| API                    | Problèmes connus | Incompatibilités chrome
|------------------------|--------------|----------------------|
| [les](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/cookies)  |  | |
| [cookies. Get](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/get)    |  | |
| [cookies. getAll](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAll) |   | Si aucune URL n’est fournie, les cookies sont extraits uniquement pour les URL des onglets actuellement ouverts. Dans Chrome, tous les cookies sont présents sur l’ordinateur d’un utilisateur. |
| [cookies. getAllCookieStores](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAllCookieStores)  | | Retourne toujours le même magasin de cookies par défaut avec l’ID «0». Tous les cookies appartiennent à ce Store. |
| [cookies. onChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/onChanged)    | | Non pris en charge. |
| [cookies. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/remove) |  | |
| [cookies. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/set)    |  | |



## long

Les `extension` API suivantes sont prises en charge:

| API                                   | Problèmes connus | Incompatibilités chrome
|---------------------------------------|----------------------------------------------------------|-------------|
[long](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension) | | |
[extension. getBackgroundPage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getBackgroundPage) | | |
[extension. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getURL) | | |
[extension. getViews](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/getViews) | | |
[extension. isAllowedIncognitoAccess](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/isAllowedIncognitoAccess) | | | 
[extension.inIncognitoContext](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/inIncognitoContext) | | | 



## i18n

Les `i18n` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------| :-------- | :---------------------
[i18n](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n) | | |
[i18n. getAcceptLanguages](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getAcceptLanguages) | | |
[i18n. getMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/i18n/getMessage) | `i18n.getMessage` la clé non valide lève une exception au lieu d’échouer harmonieusement. <br/><br/> `i18n.getMessage` l’argument attend des chaînes, mais doit également autoriser un int ou lever une exception. | |
[i18n. getUILanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getUILanguage) | | |

## inactif

Les `idle` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------| :-------- | :---------------------
[inactif](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle) | | |
[Idle. setDetectionInterval](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/setDetectionInterval) | | |
[Idle. queryState](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/queryState) | | |

## notifications

Les `notifications` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------| :-------- | :---------------------
[notifications](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) | | |
[Déclaration. NotificationOptions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/NotificationOptions) | | |
[Déclaration. TemplateType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/TemplateType) | | |
[notifications. effacer](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/clear) | | |
[notifications. créer](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/create) | | |
[notifications. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/getAll) | | |
[notifications. mise à jour](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/update) | | |
[notifications. onButtonClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onButtonClicked) | | |
[notifications. onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClicked) | | |
[notifications. onClosed](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClosed) | | |
notifications. onPermissionLevelChanged | | |
notifications. getPermissionLevel | | |

## pageAction

Les `pageAction` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :--------------------
[pageAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction) | | |
[pageAction.getPopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getPopup) | | |
[pageAction. getTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getTitle) | | |
[pageAction. Hide](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/hide) | | |
[pageAction.onClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/onClicked) | | |
[pageAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setIcon) | | Le `imageData` paramètre n’est pas pris en charge. <br/><br/> `path` est un paramètre obligatoire. |
[pageAction.setPopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setPopup) | | |
[pageAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setTitle) | | |
[pageAction. Show](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/show) | | |



## Runtime

Les `runtime` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :-------------------
[Runtime](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime) | | |
[Runtime. port. Disconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. port. onDisconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. port. postMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Connect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connect) | | |
[Runtime. connectNative](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) | | |
[runtime.id](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id) | | |
[Runtime. getBackgroundPage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/getBackgroundPage) | | |
[Runtime. getManifest](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getManifest) | | |
[Runtime. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getURL) | | |
[Runtime. lastError](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/lastError) | | |
[Runtime. Reload](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/reload) | | |
[Runtime. sendMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage) | Les pages d’extension Microsoft Edge peuvent utiliser `runtime.sendMessage` / `onMessage` pour envoyer des messages à eux-mêmes. <br/><br/> `runtime.sendmessage` n’est pas pris en charge dans les pages du site. | Microsoft Edge ne prend pas en charge le `options` paramètre.|
[Runtime. sendNativeMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) | | |
[Runtime. setUninstallUrl](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/setUninstallUrl) | | |
[Runtime. onConnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onConnect) | | |
[Runtime. onInstalled](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onInstalled) | | |
[Runtime. onMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onMessage) | `tab` l’objet dans l' `runtime.onMessage` événement n’est pas entièrement implémenté. | `MessageSender.tlsChannelId` n’est pas pris en charge dans Microsoft Edge.|

## stockage

Les `storage` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :------------------------
[stockage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage) |  | |
[Storage. local. Get](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/get)  | | |
[Storage. local. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/remove)  | | |
[Storage. local. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/set)  | | |
[Storage. local. Clear](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/clear) | | |
[Storage. local. getBytesInUse](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/getBytesInUse) | | `storage.local` les données sont conservées dans un format différent de chrome, provoquant la retour d’une valeur différente lors de l’appel `storage.local.getBytesInUse` .  <br/><br/>Par exemple: `storage.local.set({ "k": { "s": "âas" } }` retourne 13 dans chrome et 50 dans Microsoft Edge.|
[Storage. Sync. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/get) | Si le nombre combiné de caractères dans les `name` champs du manifeste et du `author` manifeste dépasse 31 caractères, `storage.sync` il est possible que l’espace de noms ne fonctionne pas. | |
[Storage. Sync. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/remove) | | |
[Storage. Sync. Set](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/set) | | |
[Storage. onChanged](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/onChanged) | | |

## eux

Les `tabs` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------------ | :------------- | :----------------
[eux](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[onglets. captureVisibleTab](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/captureVisibleTab) | | |
[onglet créer](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/create) | | `selected`, `pinned` et ne `openerTabId` sont pas pris en charge. |
[onglets. detectLanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/detectLanguage) | | |
[tabs.executeScript](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/executeScript) | `runAt` est ignorée, mais elle est activée. L’exécution du script dans une image spécifique n’est pas encore prise en charge. | |
[onglets. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/get) | Les pages d’options, lors de la demande d’un onglet qui n’est pas dans sa fenêtre, échouent à cet appel. | |
[tabulations. getCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/getCurrent) | | |
[onglets. insertCSS](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/insertCSS) | `runAt` est ignorée, mais elle est activée. | `cssOrigin` n’est pas pris en charge. |
[onglets. onActivated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onActivated) | | |
[onglets. onAttached](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onAttached) | | |
[onglets. onCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onCreated) | | |
[onglets. onDetached](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[onglets. onRemoved](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onRemoved) | | |
[onglets. onReplaced](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/onReplaced) | | |
[onglets. onUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onUpdated) | Après la désinstallation/réinstallation, l’URL n’est pas reçue tant que Microsoft Edge n’est pas redémarré. | |
[onglets. Query](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/query) | `pinned``audible`et `muted` ne sont pas encore pris en charge. <br/><br/> `"popup"` `windowType` n’est pas encore pris en charge. | `highlighted` n’est pas pris en charge. <br/><br/> `"panel"`, `"app"` et ne `"devtools"` `windowType` sont pas pris en charge. |
[tabulations. Reload](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/reload) | | Microsoft Edge ne prend pas en charge les promesses. |
[onglet. suppression](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/remove) | | |
[onglets. sendMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/sendMessage) | Message une image spécifique n’est pas encore prise en charge. `tabs.sendMessage` ne jamais envoyer de réponse après une actualisation de tabulation si aucun `runtime.onMessage` écouteur n’est présent sur l’onglet réception. | |
[eux. Délimité](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/Tab) | `audible`, `mutedInfo` , `inPrivate` , `width` et les `height` Propriétés ne sont pas encore prises en charge. | `openerTabId``selected`et les `highlighted` Propriétés ne sont pas prises en charge. |
[onglets. mise à jour](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/update) | `pinned` et `muted` ne sont pas encore pris en charge. | `highlighted` et ne `selected` sont pas pris en charge. |


## Navigation Webnavigation

Les `webNavigation` API suivantes sont prises en charge:


| API                                                                                                                                                           | Problèmes connus                                | Incompatibilités chrome                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [Navigation Webnavigation](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation)                                                     | Les ID de tabulation sont incorrects.                      | Le filtrage, TransitionTypes et TransitionQualifiers ne sont pas pris en charge. <br/><br/> Dans le cas d’un onglet, tous `processIds` seront identiques. |
| [Webnavigation. getAllFrames](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getAllFrames)                           | Ne comprend pas les éléments Object-As-IFRAME. |                                                                                                                             |
| [Webnavigation. getFrame](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getFrame)                                   |                                             |                                                                                                                             |
| [Webnavigation. onBeforeNavigate](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onBeforeNavigate)                   |                                             |                                                                                                                             |
| [Webnavigation. onCommitted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onCommitted)                                           |                                             |                                                                                                                             |
| [Webnavigation. onCompleted](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCompleted)                             |                                             |                                                                                                                             |
| [Webnavigation. onCreatedNavigationTarget](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCreatedNavigationTarget) |                                             |                                                                                                                             |
| [Webnavigation. onDOMContentLoaded](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onDOMContentLoaded)               |                                             |                                                                                                                             |
| [Webnavigation. onErrorOccurred](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onErrorOccurred)                     |                                             |                                                                                                                             |
| [Webnavigation. onHistoryStateUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onHistoryStateUpdated)         |                                             |                                                                                                                             |
| [Webnavigation. onReferenceFragmentUpdated](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onReferenceFragmentUpdated)            |                                             |                                                                                                                             |
| [Webnavigation. onTabReplaced](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onTabReplaced)                         |                                             | Non pris en charge.                                                                                                              |
| [Webnavigation. TransitionType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionType)                       |                                             |                                                                                                                             |
| [Webnavigation. TransitionQualifier](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionQualifier)             |                                             |                                                                                                                             |

## Instances

Les `webRequest` API suivantes sont prises en charge:

API | Problèmes connus | Incompatibilités chrome
:------ | :----- | :-------
[Instances](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest) | `webRequest` non pris en charge pour le mode synchrone `XmlHttpRequests` . | Les requêtes réseau issues d’extensions, telles que des options, des pages d’arrière-plan ou de fenêtre contextuelle, ne sont pas prises en charge.<br/><br/> Les requêtes réseau de `<object>` et `<embed>` les éléments ne sont pas pris en charge.<br/><br/> Les en-têtes ne peuvent pas être modifiés pour les demandes mises en cache.  |
[handlerBehaviorChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/handlerBehaviorChanged) | | Les modifications apportées aux gestionnaires sont gérées automatiquement dans Microsoft Edge.<br/><br/>L’appel n’a aucun effet.  |
[onAuthRequired](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onAuthRequired) | | |
[onBeforeRedirect](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRedirect) | | |
[onBeforeRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRequest) | | `requestBody` n’est pas pris en charge. |
[onBeforeSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeSendHeaders) | | |
[onCompleted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onCompleted) | | |
[onErrorOccurred](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onErrorOccurred) | | |
[onHeadersReceived](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onHeadersReceived) | |  |
[onResponseStarted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onResponseStarted) | |  |
[onSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onSendHeaders) | | |

## windows

Les `windows` API suivantes sont prises en charge:


| API                                                                                                                               | Problèmes connus                                                   | Incompatibilités chrome                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [windows](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows)                                     |                                                                | `Window` les objets ne prennent pas en charge la `alwaysOnTop` propriété dans Microsoft Edge. <br/><br/>InPrivate n’est pas pris en charge. |
| [Windows. CreateType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/CreateType)                            |                                                                | `"panel"` et ne `"detached_panel"` sont pas pris en charge dans Microsoft Edge.                                           |
| [Windows. Create](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/create)                                    |                                                                | `tabId` le paramètre de déchirement d’une tabulation n’est pas pris en charge.                                                       |
| [Windows. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/get)                             |                                                                |                                                                                                                 |
| [Windows. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getAll)                       | `windows.getAll({populate: true})` propriété manquant `tabs` . |                                                                                                                 |
| [Windows. getCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getCurrent)               |                                                                |                                                                                                                 |
| [Windows. getLastFocused](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getLastFocused)       |                                                                |                                                                                                                 |
| [Windows. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/update)                       | La spécification de position n’est pas prise en charge.                          | `"minimized"`/`"maximized"`/`"fullscreen"` et ne `drawAttention` sont pas pris en charge dans Microsoft Edge.             |
| [Windows. onCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/onCreated)                 |                                                                | `WindowType` le filtre n’est pas pris en charge.                                                                           |
| [Windows. onFocusChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/onFocusChanged)                    |                                                                | `WindowType` le filtre n’est pas pris en charge.                                                                           |
| [Windows. WindowState](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowState)                          | `"minimized"`, `"maximized"` ne `"fullscreen"` sont pas pris en charge. | `"docked"` n’est pas pris en charge dans Microsoft Edge.                                                                  |
| [Windows. WindowType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowType)                            |                                                                | `"panel"`, `"app"` et ne `"devtools"` sont pas pris en charge dans Microsoft Edge.                                       |
| [Windows. WINDOW_ID_CURRENT](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_CURRENT) |                                                                |                                                                                                                 |
| [Windows. WINDOW_ID_NONE](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_NONE)       |                                                                |                                                                                                                 |
