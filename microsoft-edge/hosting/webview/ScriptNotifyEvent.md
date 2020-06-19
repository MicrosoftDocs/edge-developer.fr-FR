---
description: Représente une chaîne de notification transmise à partir du contenu WebView vers l’application.
title: Objet ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752009"
---
# Objet ScriptNotifyEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Objet qui représente un événement déclenché lorsque le contenu contenu dans le [WebView](../webview.md) transmet une chaîne à l’application en utilisant JavaScript.  

## Propriétés  

### callingUri  

Obtient l’URI (Uniform Resource Identifier) de la page qui contient le script qui a déclenché l' **ScriptNotifyEvent**.  

Cette propriété est en lecture seule.  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### Valeur de propriété  

Type: **DOMString**  

### value  

Nom de la méthode transmis à l’application.  

Cette propriété est en lecture seule.  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### Valeur de propriété  

Type: **DOMString**  
