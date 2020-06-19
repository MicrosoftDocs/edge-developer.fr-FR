---
description: Contient des informations sur la navigation complète de WebView
title: Objet NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752136"
---
# Objet NavigationCompletedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Objet qui représente un événement déclenché lorsque le [WebView](../webview.md) a fini de charger le contenu actuel ou en cas d’échec de la navigation.  

## Propriétés  

### uri  

URI (Uniform Resource Identifier) de la navigation.  

Cette propriété est en lecture seule.  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### Valeur de propriété  

Type: **DOMString**  

### Propriétés IsSuccess  

Obtient une valeur qui indique si la navigation s’est déroulée correctement.  

Cette propriété est en lecture seule.  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### Valeur de propriété  

Type: **booléen**  

### webErrorStatus  

Si la navigation a échoué, obtient une valeur qui indique pourquoi.  

Cette propriété est en lecture seule.  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### Valeur de propriété  

Type: **longue non signée**  
