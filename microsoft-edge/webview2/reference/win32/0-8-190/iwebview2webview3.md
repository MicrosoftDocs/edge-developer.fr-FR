---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: cfb99be772170ee458fa252133f90240d75af3db
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878049"
---
# <span data-ttu-id="17f8f-104">0.8.355-interface IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="17f8f-104">0.8.355 - interface IWebView2WebView3</span></span> 

> [!NOTE]
> <span data-ttu-id="17f8f-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="17f8f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="17f8f-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="17f8f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="17f8f-107">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="17f8f-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="17f8f-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="17f8f-108">Summary</span></span>

 <span data-ttu-id="17f8f-109">Ses</span><span class="sxs-lookup"><span data-stu-id="17f8f-109">Members</span></span>                        | <span data-ttu-id="17f8f-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="17f8f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17f8f-111">Stop</span><span class="sxs-lookup"><span data-stu-id="17f8f-111">Stop</span></span>](#stop) | <span data-ttu-id="17f8f-112">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="17f8f-112">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="17f8f-113">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17f8f-113">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="17f8f-114">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17f8f-114">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="17f8f-115">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17f8f-115">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="17f8f-116">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17f8f-116">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="17f8f-117">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17f8f-117">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="17f8f-118">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17f8f-118">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="17f8f-119">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17f8f-119">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="17f8f-120">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17f8f-120">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="17f8f-121">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="17f8f-121">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="17f8f-122">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="17f8f-122">The title for the current top level document.</span></span>

<span data-ttu-id="17f8f-123">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="17f8f-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="17f8f-124">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="17f8f-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="17f8f-125">Ses</span><span class="sxs-lookup"><span data-stu-id="17f8f-125">Members</span></span>

#### <span data-ttu-id="17f8f-126">Stop</span><span class="sxs-lookup"><span data-stu-id="17f8f-126">Stop</span></span> 

<span data-ttu-id="17f8f-127">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="17f8f-127">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="17f8f-128">point d' [arrêt](#stop)public HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="17f8f-128">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="17f8f-129">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17f8f-129">add_NewWindowRequested</span></span> 

<span data-ttu-id="17f8f-130">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17f8f-130">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="17f8f-131">[add_NewWindowRequested](#add_newwindowrequested)par le biais du[mot de passe](IWebView2NewWindowRequestedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="17f8f-131">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17f8f-132">Se déclenche lorsque le contenu à l’intérieur du WebView est demandé pour ouvrir une nouvelle fenêtre, par exemple via Window. Open.</span><span class="sxs-lookup"><span data-stu-id="17f8f-132">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="17f8f-133">L’application peut transmettre un WebView cible qui sera considéré comme la fenêtre ouverte.</span><span class="sxs-lookup"><span data-stu-id="17f8f-133">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="17f8f-134">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="17f8f-134">remove_NewWindowRequested</span></span> 

<span data-ttu-id="17f8f-135">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="17f8f-135">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="17f8f-136">[remove_NewWindowRequested](#remove_newwindowrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="17f8f-136">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17f8f-137">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17f8f-137">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="17f8f-138">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17f8f-138">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="17f8f-139">[add_DocumentTitleChanged](#add_documenttitlechanged)par le biais du[mot de passe](IWebView2DocumentTitleChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="17f8f-139">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="17f8f-140">L’événement se déclenche lorsque la propriété DocumentTitle de WebView change et qu’il est susceptible de se déclencher avant ou après l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="17f8f-140">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="17f8f-141">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="17f8f-141">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="17f8f-142">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="17f8f-142">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="17f8f-143">[remove_DocumentTitleChanged](#remove_documenttitlechanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="17f8f-143">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="17f8f-144">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="17f8f-144">get_DocumentTitle</span></span> 

<span data-ttu-id="17f8f-145">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="17f8f-145">The title for the current top level document.</span></span>

> <span data-ttu-id="17f8f-146">valeur publique HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="17f8f-146">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="17f8f-147">Si le document ne comporte pas de titre explicite ou s’il est vide, une valeur par défaut qui peut ou ne correspond pas à l’URI du document sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="17f8f-147">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

