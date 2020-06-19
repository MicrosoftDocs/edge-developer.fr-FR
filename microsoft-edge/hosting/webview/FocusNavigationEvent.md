---
description: Objet dispatché d’un événement de focus contenant la raison et l’emplacement de la navigation
title: Objet FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752163"
---
# Objet FocusNavigationEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Objet distribué de [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) contenant l' [**NavigationReason**](#navigationreason) et l’emplacement.  

## Méthodes  

### requestFocus  

Appelée pour déplacer le focus entre l’application et le WebView.  

### Parameters  

Cette méthode n’a pas de paramètres.  

### Valeur renvoyée  

Cette méthode ne renvoie pas de valeur.  

## Propriétés  

### navigationReason  

Type **NavigationReason**: «gauche», «haut», «droite» ou «bas».  

Cette propriété est en lecture seule.  

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### Valeur de propriété  

Type: **NavigationReason**  

### originHeight  

Emplacement de la hauteur d’origine de l’élément à donner au focus.  

Cette propriété est en lecture seule.  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### Valeur de propriété  

Type: **float**  

### originLeft  

Emplacement de gauche de l’élément à donner au focus.  

Cette propriété est en lecture seule.  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### Valeur de propriété  

Type: **float**  

### originTop  

Emplacement supérieur d’origine de l’élément à donner le focus.  

Cette propriété est en lecture seule.  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### Valeur de propriété  

Type: **float**  

### originWidth  

La largeur d’origine de l’élément à donner au focus.  

Cette propriété est en lecture seule.  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### Valeur de propriété  

Type: **float**  
