---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 00aaddcc732076e4f7aa808b04132641fe7fe969
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886443"
---
# 0.9.430-interface ICoreWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Request](#get_request) | La requête HTTP.
[get_Response](#get_response) | Réponse HTTP.
[put_Response](#put_response) | Définissez la propriété Response.
[GetDeferral](#getdeferral) | Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.
[get_ResourceContext](#get_resourcecontext) | Les contextes de requête de ressource Web.

## Ses

#### get_Request 

La requête HTTP.

> [get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) du public HRESULT

#### get_Response 

Réponse HTTP.

> valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) * * Response)

#### put_Response 

Définissez la propriété Response.

> [put_Response](#put_response)par le biais du public[HRESULT (réponse](ICoreWebView2WebResourceResponse.md) )

#### GetDeferral 

Obtenez un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) et placez l’événement dans un État différé.

> public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * Report)

Vous pouvez utiliser l’objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) pour terminer la requête réseau ultérieurement.

#### get_ResourceContext 

Les contextes de requête de ressource Web.

> [get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT * Context)

