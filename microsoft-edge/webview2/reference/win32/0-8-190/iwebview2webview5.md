---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: bc48c5d495c2182ba39b867fdb46ce7af503f5ba
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884686"
---
# <span data-ttu-id="c30ec-104">0.8.355-interface IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="c30ec-104">0.8.355 - interface IWebView2WebView5</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="c30ec-105">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="c30ec-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="c30ec-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c30ec-106">Summary</span></span>

 <span data-ttu-id="c30ec-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c30ec-107">Members</span></span>                        | <span data-ttu-id="c30ec-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c30ec-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c30ec-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c30ec-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="c30ec-110">Avertit en cas de modification de la propriété ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="c30ec-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="c30ec-111">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c30ec-111">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="c30ec-112">Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.</span><span class="sxs-lookup"><span data-stu-id="c30ec-112">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="c30ec-113">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="c30ec-113">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="c30ec-114">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="c30ec-114">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="c30ec-115">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="c30ec-115">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="c30ec-116">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c30ec-116">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="c30ec-117">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c30ec-117">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="c30ec-118">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c30ec-118">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="c30ec-119">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c30ec-119">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="c30ec-120">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c30ec-120">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="c30ec-121">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="c30ec-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="c30ec-122">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="c30ec-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="c30ec-123">Ses</span><span class="sxs-lookup"><span data-stu-id="c30ec-123">Members</span></span>

#### <span data-ttu-id="c30ec-124">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c30ec-124">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="c30ec-125">Avertit en cas de modification de la propriété ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="c30ec-125">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="c30ec-126">[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)par le biais du[mot de passe](IWebView2ContainsFullScreenElementChangedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="c30ec-126">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="c30ec-127">Cela signifie qu’un élément HTML à l’intérieur du WebView est entré en plein écran jusqu’à la taille de l’affichage WebView ou en laissant le plein écran.</span><span class="sxs-lookup"><span data-stu-id="c30ec-127">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="c30ec-128">Cet événement est utile, par exemple, lorsqu’un élément vidéo demande d’être placé en plein écran.</span><span class="sxs-lookup"><span data-stu-id="c30ec-128">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="c30ec-129">L’écouteur de ContainsFullScreenElementChanged peut alors redimensionner le WebView en réponse.</span><span class="sxs-lookup"><span data-stu-id="c30ec-129">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="c30ec-130">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="c30ec-130">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="c30ec-131">Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.</span><span class="sxs-lookup"><span data-stu-id="c30ec-131">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="c30ec-132">[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)par le biais du mot-clé public HRESULT</span><span class="sxs-lookup"><span data-stu-id="c30ec-132">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="c30ec-133">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="c30ec-133">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="c30ec-134">Indique si le WebView contient un élément HTML fullscreen.</span><span class="sxs-lookup"><span data-stu-id="c30ec-134">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="c30ec-135">valeur publique HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="c30ec-135">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="c30ec-136">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="c30ec-136">add_WebResourceRequested</span></span> 

<span data-ttu-id="c30ec-137">Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c30ec-137">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="c30ec-138">[add_WebResourceRequested](#add_webresourcerequested)par le biais du[mot de passe](IWebView2WebResourceRequestedEventHandler.md)</span><span class="sxs-lookup"><span data-stu-id="c30ec-138">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="c30ec-139">Se déclenche lorsque WebView effectue une requête HTTP à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="c30ec-139">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="c30ec-140">Au moins un filtre doit être ajouté pour que l’événement se déclenche.</span><span class="sxs-lookup"><span data-stu-id="c30ec-140">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="c30ec-141">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c30ec-141">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="c30ec-142">Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c30ec-142">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="c30ec-143">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="c30ec-143">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="c30ec-144">Le paramètre URI peut être une chaîne de caractères génériques (' ': zéro ou plusieurs; '? ': exactement 1).</span><span class="sxs-lookup"><span data-stu-id="c30ec-144">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="c30ec-145">nullptr est l’équivalent de L "".</span><span class="sxs-lookup"><span data-stu-id="c30ec-145">nullptr is equivalent to L"".</span></span> <span data-ttu-id="c30ec-146">Pour plus d’détails sur les filtres de contexte de ressources, voir WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.</span><span class="sxs-lookup"><span data-stu-id="c30ec-146">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="c30ec-147">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="c30ec-147">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="c30ec-148">Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c30ec-148">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="c30ec-149">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) constante resourceContext)</span><span class="sxs-lookup"><span data-stu-id="c30ec-149">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="c30ec-150">Si le même filtre a été ajouté plusieurs fois, il doit être supprimé autant de fois que ce dernier a été ajouté pour que la suppression soit effective.</span><span class="sxs-lookup"><span data-stu-id="c30ec-150">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="c30ec-151">Renvoie E_INVALIDARG pour un filtre qui n’a jamais été ajouté.</span><span class="sxs-lookup"><span data-stu-id="c30ec-151">Returns E_INVALIDARG for a filter that was never added.</span></span>

