---
description: Contient des informations sur la navigation complète de WebView
title: Objet NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565099"
---
# Objet NavigationCompletedEvent

Objet qui représente un événement déclenché lorsque le [WebView](../webview.md) a fini de charger le contenu actuel ou en cas d’échec de la navigation.

## Propriétés
    
### uri

URI (Uniform Resource Identifier) de la navigation.

Cette propriété est en lecture seule.

```js
var uri = NavigationCompletedEvent.uri;
```

#### Valeur de propriété
Type: **DOMString**

### Propriétés IsSuccess

Obtient une valeur qui indique si la navigation s’est déroulée correctement.

Cette propriété est en lecture seule

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### Valeur de propriété
Type: **booléen**

### webErrorStatus

Si la navigation a échoué, obtient une valeur qui indique pourquoi.

Cette propriété est en lecture seule

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### Valeur de propriété
Type: **longue non signée**
