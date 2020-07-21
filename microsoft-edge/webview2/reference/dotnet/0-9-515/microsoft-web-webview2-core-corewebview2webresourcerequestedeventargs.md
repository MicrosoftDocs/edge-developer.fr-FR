---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 656510998879e77c2e7797c700dacc5966299210
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884651"
---
# 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Requête](#request) | La requête HTTP.
[ResourceContext](#resourcecontext) | Les contextes de requête de ressource Web.
[Réponse](#response) | Réponse HTTP.
[GetDeferral](#getdeferral) | Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

## Ses

#### Requête 

La requête HTTP.

> [demande](#request) publique HttpRequestMessage

#### ResourceContext 

Les contextes de requête de ressource Web.

> public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)

#### Réponse 

Réponse HTTP.

> [réponse](#response) HttpResponseMessage publique

#### GetDeferral 

Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

> public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()

Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête réseau ultérieurement.

