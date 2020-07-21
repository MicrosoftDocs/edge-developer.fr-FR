---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 056667b4ee1995763fee81c8d7a9be31496f7f3e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886513"
---
# interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

Arguments d’événement pour l’événement WebResourceResponseReceived.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Objet demande de ressources Web. Toute modification apportée à cet objet sera ignorée.
[get_Response](#get_response) | Objet de réponse aux ressources Web.
[PopulateResponseContent](#populateresponsecontent) | Méthode Async pour demander le flux de contenu de la réponse.

Va contenir la requête telle qu’elle a été envoyée et la réponse telle qu’elle a été reçue. Remarque: pour obtenir le flux de contenu de réponse, appelez d’abord PopulateResponseContent et attendez que l’appel asynchrone se termine, sinon l’objet de flux de contenu renvoyé sera null.

## Ses

#### get_Request 

Objet demande de ressources Web. Toute modification apportée à cet objet sera ignorée.

> [get_Request](#get_request)par le biais du public HRESULT

#### get_Response 

Objet de réponse aux ressources Web.

> valeur publique HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse * * Response)

Toute modification apportée à cet objet sera ignorée.

#### PopulateResponseContent 

Méthode Async pour demander le flux de contenu de la réponse.

> public HRESULT [PopulateResponseContent](#populateresponsecontent)(gestionnaire[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) *)

```cpp
                    args->PopulateResponseContent(
                        Callback<
                            ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler>(
                            [this, webResourceRequest, webResourceResponse](HRESULT result) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get()) + L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```

