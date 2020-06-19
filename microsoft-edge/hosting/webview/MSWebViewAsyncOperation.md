---
description: Indique si l’opération est réussie ou a échoué.
title: Objet MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: d6e03af2a0205938f19120076aa0ad622539d7e5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752122"
---
# Objet MSWebViewAsyncOperation  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Indique si l’opération est réussie ou a échoué.  

## Événements  

### achever  

Indique que l’opération est terminée.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### Informations sur l’événement  

|  |  |  
|:--- |:--- |  
| **Interface** | **Événement** |  
| **Synchrone** |Oui |  
| **BD** |Non |   
| **Annulable** |Non |  

### erreur  

Indique qu’il y a eu une erreur de fonctionnement.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### Informations sur l’événement  

|  |  |  
|:--- |:--- |  
| **Interface** | **Événement** |  
| **Synchrone** | Oui |  
| **BD** | Non |  
| **Annulable** | Non |  

## Méthodes  

### start  

Appelée pour lancer la tâche asynchrone.  

```javascript
MSWebViewAsyncOperation.start();
```  

### Parameters  

Cette méthode n’a pas de paramètres.  

### Valeur renvoyée  

Cette méthode ne renvoie pas de valeur.  

## Propriétés  

### erreur  

Erreur qui s’est produite.  

Cette propriété est en lecture seule.  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### Valeur de propriété  

Type: **DOMError**  

### OnComplete  

Le gestionnaire d’événements **complet** .  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### Valeur de propriété  

Type: **EventHandler**  

### erreur  

Le gestionnaire d’événements d' **erreur** .  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### Valeur de propriété  

Type: **EventHandler**  

### readyState  

Décrit l’état prêt de l’objet.  

Cette propriété est en lecture seule.  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### Valeur de propriété  

Type: **courte non signée**  

### provoqué  

Résultat de l’opération.  

Cette propriété est en lecture seule.  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### Valeur de propriété  

Tapez: tout  

### target  

La cible de l’opération.  

Cette propriété est en lecture seule.  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### Valeur de propriété  

Type: [ **MSHTMLWebViewElement**](../webview.md)  

### type  

Type de l’opération.  

Cette propriété est en lecture seule.  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### Valeur de propriété  

Type: **courte non signée**  
