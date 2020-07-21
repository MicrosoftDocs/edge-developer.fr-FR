---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: a095b1ed085cd49a597195e01da21cde53b9095d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884742"
---
# <span data-ttu-id="3afad-104">0.8.355-interface IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="3afad-104">0.8.355 - interface IWebView2WebView3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="3afad-105">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="3afad-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="3afad-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3afad-106">Summary</span></span>

 <span data-ttu-id="3afad-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3afad-107">Members</span></span>                        | <span data-ttu-id="3afad-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3afad-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3afad-109">Stop</span><span class="sxs-lookup"><span data-stu-id="3afad-109">Stop</span></span>](#stop) | <span data-ttu-id="3afad-110">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="3afad-110">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="3afad-111">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="3afad-111">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="3afad-112">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="3afad-112">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="3afad-113">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="3afad-113">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="3afad-114">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="3afad-114">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="3afad-115">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="3afad-115">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="3afad-116">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="3afad-116">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="3afad-117">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="3afad-117">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="3afad-118">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="3afad-118">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="3afad-119">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="3afad-119">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="3afad-120">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="3afad-120">The title for the current top level document.</span></span>

<span data-ttu-id="3afad-121">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="3afad-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="3afad-122">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="3afad-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="3afad-123">Ses</span><span class="sxs-lookup"><span data-stu-id="3afad-123">Members</span></span>

#### <span data-ttu-id="3afad-124">Stop</span><span class="sxs-lookup"><span data-stu-id="3afad-124">Stop</span></span> 

<span data-ttu-id="3afad-125">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="3afad-125">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="3afad-126">point d' [arrêt](#stop)public HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="3afad-126">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="3afad-127">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="3afad-127">add_NewWindowRequested</span></span> 

<span data-ttu-id="3afad-128">Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="3afad-128">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="3afad-129">[add_NewWindowRequested](#add_newwindowrequested)par le biais du[mot de passe](IWebView2NewWindowRequestedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="3afad-129">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="3afad-130">Se déclenche lorsque le contenu à l’intérieur du WebView est demandé pour ouvrir une nouvelle fenêtre, par exemple via Window. Open.</span><span class="sxs-lookup"><span data-stu-id="3afad-130">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="3afad-131">L’application peut transmettre un WebView cible qui sera considéré comme la fenêtre ouverte.</span><span class="sxs-lookup"><span data-stu-id="3afad-131">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="3afad-132">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="3afad-132">remove_NewWindowRequested</span></span> 

<span data-ttu-id="3afad-133">Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="3afad-133">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="3afad-134">[remove_NewWindowRequested](#remove_newwindowrequested)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="3afad-134">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="3afad-135">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="3afad-135">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="3afad-136">Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="3afad-136">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="3afad-137">[add_DocumentTitleChanged](#add_documenttitlechanged)par le biais du[mot de passe](IWebView2DocumentTitleChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="3afad-137">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="3afad-138">L’événement se déclenche lorsque la propriété DocumentTitle de WebView change et qu’il est susceptible de se déclencher avant ou après l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="3afad-138">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="3afad-139">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="3afad-139">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="3afad-140">Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="3afad-140">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="3afad-141">[remove_DocumentTitleChanged](#remove_documenttitlechanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="3afad-141">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="3afad-142">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="3afad-142">get_DocumentTitle</span></span> 

<span data-ttu-id="3afad-143">Titre du document de niveau supérieur actuel.</span><span class="sxs-lookup"><span data-stu-id="3afad-143">The title for the current top level document.</span></span>

> <span data-ttu-id="3afad-144">valeur publique HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span><span class="sxs-lookup"><span data-stu-id="3afad-144">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="3afad-145">Si le document ne comporte pas de titre explicite ou s’il est vide, une valeur par défaut qui peut ou ne correspond pas à l’URI du document sera utilisée.</span><span class="sxs-lookup"><span data-stu-id="3afad-145">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

