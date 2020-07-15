---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 40474d6b1169467022e5bb47e82eba3883edc2aa
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878098"
---
# 0.8.355-interface IWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Request](#get_request) | La requête HTTP.
[get_Response](#get_response) | Réponse HTTP.
[put_Response](#put_response) | Définissez la propriété Response.
[GetDeferral](#getdeferral) | Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.

## Ses

#### get_Request 

La requête HTTP.

> [get_Request](#get_request)par le biais[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) du public HRESULT

#### get_Response 

Réponse HTTP.

> valeur publique HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) * * Response)

#### put_Response 

Définissez la propriété Response.

> [put_Response](#put_response)par le biais du public[HRESULT (réponse](IWebView2WebResourceResponse.md) )

#### GetDeferral 

Obtenez un objet [IWebView2Deferral](IWebView2Deferral.md) et placez l’événement dans un État différé.

> public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * Report)

Vous pouvez utiliser l’objet [IWebView2Deferral](IWebView2Deferral.md) pour terminer la requête réseau ultérieurement.

