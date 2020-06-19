---
description: Représente un processus WebView.
title: Objet MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752155"
---
# Objet MSWebViewProcess  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Représente un processus [WebView](../webview.md) .  

```javascript
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

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

Cette propriété est en lecture seule.  

#### Valeur de propriété  

Type: **booléen**  

## Méthodes  

### CreateWebViewAsync  

Crée un [WebView](../webview.md) dans un processus spécifique.  

```javascript
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

```javascript
wvprocess.terminate();
```  

#### Valeur renvoyée  

Cette méthode ne renvoie pas de valeur.  
