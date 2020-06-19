---
description: Indique que le WebView tente de télécharger un fichier non pris en charge.
title: Objet UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752012"
---
# Objet UnviewableContentIdentifiedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Indique que [WebView](../webview.md) tente d’accéder à un fichier d’un type de contenu non pris en charge.  

## Propriétés  

### Média  

Obtient le type de contenu du contenu non affiché.  

Cette propriété est en lecture seule  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### Valeur de propriété  

Type: **DOMString**  

### Referer  

URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.  

Cette propriété est en lecture seule.  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### Valeur de propriété  

Type: **DOMString**  

### uri  

URI (Uniform Resource Identifier) de la destination de la navigation.  

Cette propriété est en lecture seule.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Valeur de propriété  

Type: **DOMString**  
