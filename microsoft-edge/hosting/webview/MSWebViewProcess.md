---
description: Représente un processus WebView.
title: Objet MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565102"
---
# Objet MSWebViewProcess

Représente un processus [WebView](../webview.md) .

```js
var wvprocess = new MSWebViewProcess();
```

## Propriétés

### enterpriseId

ID entreprise du processus.

```js
var enterpriseId = wvprocess.enterpriseId;
```

Cette propriété est en lecture seule.

#### Valeur de propriété
Type: **DOMString**

### isPrivateNetworkClientServerCapabilityEnabled

Obtient une valeur indiquant si le processus [WebView](../webview.md) possède la [déclaration des fonctionnalités](/windows/uwp/packaging/app-capability-declarations) des *réseaux privés (client & serveur)* qui est activée dans le manifeste de l’application.

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

Cette propriété est en lecture seule.

#### Valeur de propriété
Type: **booléen**

## Méthodes

### CreateWebViewAsync

Crée un [WebView](../webview.md) dans un processus spécifique.

```js
wvprocess.createWebviewAsync();
```

#### Valeur renvoyée

Nouveau**`Promise<MSHTMLWebViewElement>`**

### GetWebViews

Retourne une séquence d’objets **MSWebViewProcess** hébergés dans le processus.

#### Valeur renvoyée

Nouveau**`sequence<MSHTMLWebViewElement>`**

### Contrat

Arrête le processus.

```js
wvprocess.terminate();
```

#### Valeur renvoyée

Cette méthode ne renvoie pas de valeur.
