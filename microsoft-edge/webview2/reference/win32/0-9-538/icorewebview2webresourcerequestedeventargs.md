---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 3613ed9b2ef562e8760de1a88322ef028ddf4ca9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879218"
---
# interface ICoreWebView2WebResourceRequestedEventArgs 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Request](#get_request) | La requête HTTP.
[get_ResourceContext](#get_resourcecontext) | Les contextes de requête de ressource Web.
[get_Response](#get_response) | Réponse HTTP.
[GetDeferral](#getdeferral) | Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.
[put_Response](#put_response) | Définissez la propriété Response.

## Ses

#### get_Request 

La requête HTTP.

> [get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT

#### get_ResourceContext 

Les contextes de requête de ressource Web.

> [get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT * Context)

#### get_Response 

Réponse HTTP.

> valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * Response)

#### GetDeferral 

Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.

> public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Report)

Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour terminer la requête réseau ultérieurement.

#### put_Response 

Définissez la propriété Response.

> [put_Response](#put_response)par le biais du public[HRESULT (réponse](icorewebview2webresourceresponse.md) )

