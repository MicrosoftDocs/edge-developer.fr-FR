---
description: Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d’affichage WebView
title: Objet MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565100"
---
# Objet MSWebViewSettings

Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d' [affichage WebView](../webview.md) .

## Propriétés

### isIndexedDBEnabled

Obtient ou définit une valeur qui indique si l’utilisation de IndexedDB est autorisée dans le [WebView](../webview.md).

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### Valeur de propriété
Type: **booléen**

**True** si IndexedDB est autorisé dans le **WebView**; Sinon, **false**. 

### isJavaScriptEnabled

Obtient ou définit une valeur qui indique si l’utilisation de JavaScript est autorisée dans le [WebView](../webview.md).

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### Valeur de propriété
Type: **booléen**

**Vrai** JavaScript est autorisé dans le [WebView](../webview.md); Sinon, **false**. 

### isScriptNotifyAllowed

Obtient ou définit une valeur qui indique si l’utilisation de [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisée dans le [WebView](../webview.md).

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### Valeur de propriété
Type: **booléen**

**Vrai** [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisé dans le [WebView](../webview.md); Sinon, **false**. 
