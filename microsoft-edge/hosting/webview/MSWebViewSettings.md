---
description: Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d’affichage WebView
title: Objet MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752177"
---
# Objet MSWebViewSettings  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d' [affichage WebView](../webview.md) .  

## Propriétés  

### isIndexedDBEnabled  

Obtient ou définit une valeur qui indique si l’utilisation de IndexedDB est autorisée dans le [WebView](../webview.md).  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### Valeur de propriété  

Type: **booléen**  

**True** si IndexedDB est autorisé dans le **WebView**; Sinon, **false**.  

### isJavaScriptEnabled  

Obtient ou définit une valeur qui indique si l’utilisation de JavaScript est autorisée dans le [WebView](../webview.md).  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### Valeur de propriété  

Type: **booléen**  

**Vrai** JavaScript est autorisé dans le [WebView](../webview.md); Sinon, **false**.  

### isScriptNotifyAllowed  

Obtient ou définit une valeur qui indique si l’utilisation de [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisée dans le [WebView](../webview.md).  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### Valeur de propriété  

Type: **booléen**  

**Vrai** [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisé dans le [WebView](../webview.md); Sinon, **false**.  
