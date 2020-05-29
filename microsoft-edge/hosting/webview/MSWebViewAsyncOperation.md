---
description: Indique si l’opération est réussie ou a échoué.
title: Objet MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: ebb89c0fc645ebcd97357af10af2be650d8218b9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565103"
---
# Objet MSWebViewAsyncOperation

Indique si l’opération est réussie ou a échoué. 

## Événements

### achever

Indique que l’opération est terminée. 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | **Événement**
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |        


### erreur

Indique qu’il y a eu une erreur de fonctionnement.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### Informations sur l’événement

|            |      |
|------------|------|
|**Interface** | **Événement**
|**Synchrone** |Oui |    
|**BD**     |Non |   
|**Annulable**  |Non |            


## Méthodes

### start

Appelée pour lancer la tâche asynchrone. 

```js
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

```js
var error = MSWebViewAsyncOperation.error;
```

#### Valeur de propriété
Type: **DOMError**

### OnComplete

Le gestionnaire d’événements **complet** . 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### Valeur de propriété
Type: **EventHandler**

### erreur

Le gestionnaire d’événements d' **erreur** . 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### Valeur de propriété
Type: **EventHandler**

### readyState

Décrit l’état prêt de l’objet.

Cette propriété est en lecture seule.

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### Valeur de propriété
Type: **courte non signée**

### provoqué

Résultat de l’opération.

Cette propriété est en lecture seule.

```js
var result = MSWebViewAsyncOperation.result;
```

#### Valeur de propriété
Tapez: tout

### target

La cible de l’opération. 

Cette propriété est en lecture seule.

```js
var target = MSWebViewAsyncOperation.target;
```

#### Valeur de propriété
Type: [ **MSHTMLWebViewElement**](../webview.md)

### type

Type de l’opération.

Cette propriété est en lecture seule.

```js
var type = MSWebViewAsyncOperation.type;
```

#### Valeur de propriété
Type: **courte non signée**
