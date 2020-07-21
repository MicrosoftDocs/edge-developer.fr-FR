---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: dec8bfb2927e823c85f472bd2cab0800ff5f00c7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883748"
---
# 0.9.515-interface ICoreWebView2WebResourceRequestedEventArgs 

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

