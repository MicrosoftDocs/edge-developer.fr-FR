---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 3c32cd59e75eb81bf69661d01f6044a0628ba35d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653251"
---
# interface IWebView2WebView5 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

Fonctionnalités supplémentaires implémentées par l’objet WebView principal.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Avertit en cas de modification de la propriété ContainsFullScreenElement.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Indique si le WebView contient un élément HTML fullscreen.
[add_WebResourceRequested](#add_webresourcerequested) | Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.

Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md). Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .

## Ses

#### add_ContainsFullScreenElementChanged 

Avertit en cas de modification de la propriété ContainsFullScreenElement.

> [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)par le biais du[mot de passe](IWebView2ContainsFullScreenElementChangedEventHandler.md)

Cela signifie qu’un élément HTML à l’intérieur du WebView est entré en plein écran jusqu’à la taille de l’affichage WebView ou en laissant le plein écran. Cet événement est utile, par exemple, lorsqu’un élément vidéo demande d’être placé en plein écran. L’écouteur de ContainsFullScreenElementChanged peut alors redimensionner le WebView en réponse.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.

> [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)par le biais du mot-clé public HRESULT

#### get_ContainsFullScreenElement 

Indique si le WebView contient un élément HTML fullscreen.

> valeur publique HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.

> [add_WebResourceRequested](#add_webresourcerequested)par le biais du[mot de passe](IWebView2WebResourceRequestedEventHandler.md)

Se déclenche lorsque WebView effectue une requête HTTP à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter. Au moins un filtre doit être ajouté pour que l’événement se déclenche.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### AddWebResourceRequestedFilter 

Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.

> public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) constante resourceContext)

Le paramètre URI peut être une chaîne de caractères génériques (' ': zéro ou plusieurs; '? ': exactement 1). nullptr est l’équivalent de L "". Pour plus d’détails sur les filtres de contexte de ressources, voir WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.

#### RemoveWebResourceRequestedFilter 

Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.

> public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) constante resourceContext)

Si le même filtre a été ajouté plusieurs fois, il doit être supprimé autant de fois que ce dernier a été ajouté pour que la suppression soit effective. Renvoie E_INVALIDARG pour un filtre qui n’a jamais été ajouté.

