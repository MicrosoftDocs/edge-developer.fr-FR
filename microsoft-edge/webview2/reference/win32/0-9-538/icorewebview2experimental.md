---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2Experimental
ms.openlocfilehash: 98f13193e73781f9f7371db05ed3ca99ca93c128
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886544"
---
# interface ICoreWebView2Experimental 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[add_WebResourceResponseReceived](#add_webresourceresponsereceived) | Ajoutez un gestionnaire d’événements pour l’événement WebResourceResponseReceived.
[remove_WebResourceResponseReceived](#remove_webresourceresponsereceived) | Supprime le gestionnaire d’événements WebResourceResponseReceived précédemment ajouté avec add_WebResourceResponseReceived.

## Ses

#### add_WebResourceResponseReceived 

Ajoutez un gestionnaire d’événements pour l’événement WebResourceResponseReceived.

> [add_WebResourceResponseReceived](#add_webresourceresponsereceived)par le biais du[mot de passe](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md)

L’événement WebResourceResponseReceived se déclenche après que le WebView a reçu et traité la réponse à une demande de ressource Resource. Les arguments d’événement incluent le WebResourceRequest envoyé par le filaire et WebResourceResponse reçu, y compris les en-têtes supplémentaires ajoutés par la pile réseau qui n’ont pas été inclus dans le cadre de l’événement WebResourceRequested associé, tels que les en-têtes d’authentification. 
```cpp
    wil::com_ptr<ICoreWebView2Experimental> webviewExperimental;
    CHECK_FAILURE(m_appWindow->GetWebView()->QueryInterface(IID_PPV_ARGS(&webviewExperimental)));
    CHECK_FAILURE(webviewExperimental->add_WebResourceResponseReceived(
        Callback<ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler>(
            [this](
                ICoreWebView2Experimental* sender,
                ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs* args) {           
                wil::com_ptr<ICoreWebView2WebResourceRequest> request;
                CHECK_FAILURE(args->get_Request(&request));
                wil::unique_cotaskmem_string uri;
                CHECK_FAILURE(request->get_Uri(&uri));
                if (wcscmp(uri.get(), L"https://authenticationtest.com/HTTPAuth/") == 0)
                {
                    wil::com_ptr<ICoreWebView2HttpRequestHeaders> requestHeaders;
                    CHECK_FAILURE(request->get_Headers(&requestHeaders));

                    wil::unique_cotaskmem_string authHeaderValue;
                    if (requestHeaders->GetHeader(L"Authorization", &authHeaderValue) == S_OK)
                    {
                        std::wstring message(L"Authorization: ");
                        message += authHeaderValue.get();
                        MessageBox(nullptr, message.c_str(), nullptr, MB_OK);
                        m_appWindow->DeleteComponent(this);
                    }
                }
                
                return S_OK;
            })
            .Get(),
        &m_webResourceResponseReceivedToken));
```

#### remove_WebResourceResponseReceived 

Supprime le gestionnaire d’événements WebResourceResponseReceived précédemment ajouté avec add_WebResourceResponseReceived.

> [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)par le biais du mot-clé public HRESULT

