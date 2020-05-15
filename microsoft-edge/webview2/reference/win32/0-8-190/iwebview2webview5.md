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
# <span data-ttu-id="c8bd9-104">interface IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="c8bd9-104">interface IWebView2WebView5</span></span> 

> [!NOTE]
> <span data-ttu-id="c8bd9-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c8bd9-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="c8bd9-107">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="c8bd9-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c8bd9-108">Summary</span></span>

 <span data-ttu-id="c8bd9-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c8bd9-109">Members</span></span>                        | <span data-ttu-id="c8bd9-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c8bd9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c8bd9-111">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c8bd9-111">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="c8bd9-112">Avertit en cas de modification de la propriété ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-112">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="c8bd9-113">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c8bd9-113">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="c8bd9-114">Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-114">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="c8bd9-115">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="c8bd9-115">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="c8bd9-116">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-116">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="c8bd9-117">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="c8bd9-117">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="c8bd9-118">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-118">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="c8bd9-119">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c8bd9-119">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="c8bd9-120">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-120">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="c8bd9-121">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c8bd9-121">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="c8bd9-122">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-122">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="c8bd9-123">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="c8bd9-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="c8bd9-124">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="c8bd9-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="c8bd9-125">Ses</span><span class="sxs-lookup"><span data-stu-id="c8bd9-125">Members</span></span>

#### <span data-ttu-id="c8bd9-126">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c8bd9-126">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="c8bd9-127">Avertit en cas de modification de la propriété ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-127">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="c8bd9-128">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)par le biais du[mot de passe](IWebView2ContainsFullScreenElementChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="c8bd9-128">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="c8bd9-129">Cela signifie qu’un élément HTML à l’intérieur du WebView est entré en plein écran jusqu’à la taille de l’affichage WebView ou en laissant le plein écran.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-129">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="c8bd9-130">Cet événement est utile, par exemple, lorsqu’un élément vidéo demande d’être placé en plein écran.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-130">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="c8bd9-131">L’écouteur de ContainsFullScreenElementChanged peut alors redimensionner le WebView en réponse.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-131">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="c8bd9-132">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c8bd9-132">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="c8bd9-133">Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-133">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="c8bd9-134">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="c8bd9-134">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="c8bd9-135">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="c8bd9-135">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="c8bd9-136">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-136">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="c8bd9-137">valeur publique HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="c8bd9-137">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="c8bd9-138">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="c8bd9-138">add_WebResourceRequested</span></span> 

<span data-ttu-id="c8bd9-139">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-139">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="c8bd9-140">[add_WebResourceRequested](#add_webresourcerequested)par le biais du[mot de passe](IWebView2WebResourceRequestedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="c8bd9-140">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="c8bd9-141">Se déclenche lorsque WebView effectue une requête HTTP à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-141">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="c8bd9-142">Au moins un filtre doit être ajouté pour que l’événement se déclenche.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-142">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="c8bd9-143">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c8bd9-143">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="c8bd9-144">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-144">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="c8bd9-145">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="c8bd9-145">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="c8bd9-146">Le paramètre URI peut être une chaîne de caractères génériques (' ': zéro ou plusieurs; '? ': exactement 1).</span><span class="sxs-lookup"><span data-stu-id="c8bd9-146">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="c8bd9-147">nullptr est l’équivalent de L "".</span><span class="sxs-lookup"><span data-stu-id="c8bd9-147">nullptr is equivalent to L"".</span></span> <span data-ttu-id="c8bd9-148">Pour plus d’détails sur les filtres de contexte de ressources, voir WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-148">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="c8bd9-149">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c8bd9-149">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="c8bd9-150">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-150">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="c8bd9-151">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="c8bd9-151">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="c8bd9-152">Si le même filtre a été ajouté plusieurs fois, il doit être supprimé autant de fois que ce dernier a été ajouté pour que la suppression soit effective.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-152">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="c8bd9-153">Renvoie E_INVALIDARG pour un filtre qui n’a jamais été ajouté.</span><span class="sxs-lookup"><span data-stu-id="c8bd9-153">Returns E_INVALIDARG for a filter that was never added.</span></span>

