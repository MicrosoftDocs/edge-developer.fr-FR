---
description: Objet dispatché d’un événement de focus contenant la raison et l’emplacement de la navigation
title: Objet FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565110"
---
# Objet FocusNavigationEvent

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

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### Valeur de propriété
Type: **NavigationReason**

### originHeight

Emplacement de la hauteur d’origine de l’élément à donner au focus.

Cette propriété est en lecture seule.

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### Valeur de propriété
Type: **float**

### originLeft

Emplacement de gauche de l’élément à donner au focus.

Cette propriété est en lecture seule.

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### Valeur de propriété
Type: **float**

### originTop

Emplacement supérieur d’origine de l’élément à donner le focus.

Cette propriété est en lecture seule.

```js
var originTop = FocusNavigationEvent.originTop;
```

#### Valeur de propriété
Type: **float**

### originWidth

La largeur d’origine de l’élément à donner au focus.

Cette propriété est en lecture seule.

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### Valeur de propriété
Type: **float**

