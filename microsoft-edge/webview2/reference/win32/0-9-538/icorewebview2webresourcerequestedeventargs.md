---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2e55a43282a7548acefdb0b1ed1b8cac2254ef21
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010389"
---
# 0.9.579-interface ICoreWebView2WebResourceRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement WebResourceRequested.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Demande de ressource Web.
[get_ResourceContext](#get_resourcecontext) | Contexte de demande de ressources Web.
[get_Response](#get_response) | Espace réservé à l’objet de réponse aux ressources Web.
[GetDeferral](#getdeferral) | Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.
[put_Response](#put_response) | Définissez la propriété Response.

## Ses

#### get_Request 

Demande de ressource Web.

> [get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT

Il est possible que l’objet de requête ne dispose pas de certains en-têtes ajoutés par la pile réseau plus tard.

#### get_ResourceContext 

Contexte de demande de ressources Web.

> [get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (COREWEBVIEW2_WEB_RESOURCE_CONTEXT * Context)

#### get_Response 

Espace réservé à l’objet de réponse aux ressources Web.

> valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * Response)

Si cet objet est défini, la demande de ressource Web sera exécutée avec cette réponse.

#### GetDeferral 

Obtenez un objet [ICoreWebView2Deferral](icorewebview2deferral.md) et placez l’événement dans un État différé.

> public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * Report)

Vous pouvez utiliser l’objet [ICoreWebView2Deferral](icorewebview2deferral.md) pour exécuter la requête ultérieurement.

#### put_Response 

Définissez la propriété Response.

> [put_Response](#put_response)par le biais du public[HRESULT (réponse](icorewebview2webresourceresponse.md) )

Un objet de réponse aux ressources Web vide peut être créé à l’aide de CreateWebResourceResponse, puis modifié pour créer la réponse.

