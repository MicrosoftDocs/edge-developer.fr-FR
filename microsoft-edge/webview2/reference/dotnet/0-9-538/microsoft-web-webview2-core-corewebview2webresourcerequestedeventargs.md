---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 53cc31bc714417ab902fa8fdef9fd83f80871f10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879666"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

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

