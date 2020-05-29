---
description: Représente une chaîne de notification transmise à partir du contenu WebView vers l’application.
title: Objet ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564626"
---
# Objet ScriptNotifyEvent

Objet qui représente un événement déclenché lorsque le contenu contenu dans le [WebView](../webview.md) transmet une chaîne à l’application en utilisant JavaScript.

## Propriétés
    
### callingUri

Obtient l’URI (Uniform Resource Identifier) de la page qui contient le script qui a déclenché l' **ScriptNotifyEvent**.

Cette propriété est en lecture seule.

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### Valeur de propriété
Type: **DOMString**

### value

Nom de la méthode transmis à l’application.

Cette propriété est en lecture seule.

```js
var value = ScriptNotifyEvent.value;
```

#### Valeur de propriété
Type: **DOMString**