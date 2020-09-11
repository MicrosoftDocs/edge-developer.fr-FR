---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 547e9a451283de55658a95a8134ecb8a838f9e50
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011400"
---
# 0.9.579-interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

