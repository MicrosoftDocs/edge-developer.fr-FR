---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 552421aa003be2ea52493f16ad94ed2b08e8c3a9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011927"
---
# <span data-ttu-id="8f8e5-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8f8e5-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="8f8e5-105">Arguments d’événement pour l’événement WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-105">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="8f8e5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8f8e5-106">Summary</span></span>

 <span data-ttu-id="8f8e5-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8f8e5-107">Members</span></span>                        | <span data-ttu-id="8f8e5-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8f8e5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8f8e5-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="8f8e5-109">get_Request</span></span>](#get_request) | <span data-ttu-id="8f8e5-110">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-110">Web resource request object.</span></span> <span data-ttu-id="8f8e5-111">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-111">Any modifications to this object will be ignored.</span></span>
[<span data-ttu-id="8f8e5-112">get_Response</span><span class="sxs-lookup"><span data-stu-id="8f8e5-112">get_Response</span></span>](#get_response) | <span data-ttu-id="8f8e5-113">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-113">Web resource response object.</span></span>
[<span data-ttu-id="8f8e5-114">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="8f8e5-114">PopulateResponseContent</span></span>](#populateresponsecontent) | <span data-ttu-id="8f8e5-115">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-115">Async method to request the Content stream of the response.</span></span>

<span data-ttu-id="8f8e5-116">Va contenir la requête telle qu’elle a été envoyée et la réponse telle qu’elle a été reçue.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-116">Will contain the request as it was sent and the response as it was received.</span></span> <span data-ttu-id="8f8e5-117">Remarque: pour obtenir le flux de contenu de réponse, appelez d’abord PopulateResponseContent et attendez que l’appel asynchrone se termine, sinon l’objet de flux de contenu renvoyé sera null.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-117">Note: To get the response content stream, first call PopulateResponseContent and wait for the async call to complete, otherwise the content stream object returned will be null.</span></span>

## <span data-ttu-id="8f8e5-118">Ses</span><span class="sxs-lookup"><span data-stu-id="8f8e5-118">Members</span></span>

#### <span data-ttu-id="8f8e5-119">get_Request</span><span class="sxs-lookup"><span data-stu-id="8f8e5-119">get_Request</span></span> 

<span data-ttu-id="8f8e5-120">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-120">Web resource request object.</span></span> <span data-ttu-id="8f8e5-121">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-121">Any modifications to this object will be ignored.</span></span>

> <span data-ttu-id="8f8e5-122">[get_Request](#get_request)par le biais[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="8f8e5-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="8f8e5-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="8f8e5-123">get_Response</span></span> 

<span data-ttu-id="8f8e5-124">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-124">Web resource response object.</span></span>

> <span data-ttu-id="8f8e5-125">valeur publique HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="8f8e5-125">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="8f8e5-126">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-126">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="8f8e5-127">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="8f8e5-127">PopulateResponseContent</span></span> 

<span data-ttu-id="8f8e5-128">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="8f8e5-128">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="8f8e5-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)(gestionnaire[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="8f8e5-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \* handler)</span></span>

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

