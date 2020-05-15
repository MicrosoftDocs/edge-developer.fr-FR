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
ms.openlocfilehash: 436e0e33180c65afcce0487fffeff5f168dceab7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653256"
---
# interface IWebView2WebView3 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebView3
  : public IWebView2WebView
```

Fonctionnalités supplémentaires implémentées par l’objet WebView principal.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Stop](#stop) | Arrêtez toutes les navigations et les extractions de ressources en attente.
[add_NewWindowRequested](#add_newwindowrequested) | Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | Titre du document de niveau supérieur actuel.

Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md). Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .

## Ses

#### Stop 

Arrêtez toutes les navigations et les extractions de ressources en attente.

> point d' [arrêt](#stop)public HRESULT ()

#### add_NewWindowRequested 

Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.

> [add_NewWindowRequested](#add_newwindowrequested)par le biais du[mot de passe](IWebView2NewWindowRequestedEventHandler.md)

Se déclenche lorsque le contenu à l’intérieur du WebView est demandé pour ouvrir une nouvelle fenêtre, par exemple via Window. Open. L’application peut transmettre un WebView cible qui sera considéré comme la fenêtre ouverte.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.

> [remove_NewWindowRequested](#remove_newwindowrequested)par le biais du mot-clé public HRESULT

#### add_DocumentTitleChanged 

Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.

> [add_DocumentTitleChanged](#add_documenttitlechanged)par le biais du[mot de passe](IWebView2DocumentTitleChangedEventHandler.md)

L’événement se déclenche lorsque la propriété DocumentTitle de WebView change et qu’il est susceptible de se déclencher avant ou après l’événement NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.

> [remove_DocumentTitleChanged](#remove_documenttitlechanged)par le biais du mot-clé public HRESULT

#### get_DocumentTitle 

Titre du document de niveau supérieur actuel.

> valeur publique HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR * title)

Si le document ne comporte pas de titre explicite ou s’il est vide, une valeur par défaut qui peut ou ne correspond pas à l’URI du document sera utilisée.

