---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011850"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Arguments d’événement pour l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Requête](#request) | Demande de ressource Web.
[ResourceContext](#resourcecontext) | Contexte de demande de ressources Web.
[Réponse](#response) | Espace réservé à l’objet de réponse aux ressources Web.
[GetDeferral](#getdeferral) | Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

## Ses

#### Requête 

Demande de ressource Web.

> [demande](#request) publique [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md)

Il est possible que l’objet de requête ne dispose pas de certains en-têtes ajoutés par la pile réseau plus tard.

#### ResourceContext 

Contexte de demande de ressources Web.

> public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)

#### Réponse 

Espace réservé à l’objet de réponse aux ressources Web.

> réponse [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response) publique

Si cet objet est défini, la demande de ressource Web sera exécutée avec cette réponse. Un objet de réponse aux ressources Web vide peut être créé à l’aide de CreateWebResourceResponse, puis modifié pour créer la réponse.

#### GetDeferral 

Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.

> public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()

Vous pouvez utiliser l’objet CoreWebView2Deferral pour exécuter la requête ultérieurement.

