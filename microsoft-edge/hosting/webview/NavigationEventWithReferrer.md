---
description: Contient des informations de renvoi sur la navigation
title: Objet NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565093"
---
# Objet NavigationEventWithReferrer

Objet qui représente un événement déclenché lorsque la navigation est lancée et que la navigation contient un referer.

## Propriétés

### Referer

URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.

Cette propriété est en lecture seule.

#### Valeur de propriété
Type: **DOMString**


```js
var referer = NavigationEventWithReferrer.referer;
```

### uri

URI (Uniform Resource Identifier) de la destination de la navigation.

Cette propriété est en lecture seule.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Valeur de propriété
Type: **DOMString**
