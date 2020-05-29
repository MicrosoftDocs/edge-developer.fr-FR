---
description: Indique que le WebView tente de télécharger un fichier non pris en charge.
title: Objet UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564625"
---
# Objet UnviewableContentIdentifiedEvent

Indique que [WebView](../webview.md) tente d’accéder à un fichier d’un type de contenu non pris en charge. 

## Propriétés

### Média

Obtient le type de contenu du contenu non affiché.

Cette propriété est en lecture seule

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### Valeur de propriété
Type: **DOMString**

### Referer

URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.

Cette propriété est en lecture seule.


```js
var referer = NavigationEventWithReferrer.referer;
```

#### Valeur de propriété
Type: **DOMString**

### uri

URI (Uniform Resource Identifier) de la destination de la navigation.

Cette propriété est en lecture seule.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Valeur de propriété
Type: **DOMString**
