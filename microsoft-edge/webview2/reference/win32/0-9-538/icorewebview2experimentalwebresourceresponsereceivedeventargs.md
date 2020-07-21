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
# <span data-ttu-id="e7963-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e7963-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="e7963-105">Arguments d’événement pour l’événement WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="e7963-105">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="e7963-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e7963-106">Summary</span></span>

 <span data-ttu-id="e7963-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e7963-107">Members</span></span>                        | <span data-ttu-id="e7963-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e7963-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e7963-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="e7963-109">get_Request</span></span>](#get_request) | <span data-ttu-id="e7963-110">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="e7963-110">Web resource request object.</span></span> <span data-ttu-id="e7963-111">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="e7963-111">Any modifications to this object will be ignored.</span></span>
[<span data-ttu-id="e7963-112">get_Response</span><span class="sxs-lookup"><span data-stu-id="e7963-112">get_Response</span></span>](#get_response) | <span data-ttu-id="e7963-113">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="e7963-113">Web resource response object.</span></span>
[<span data-ttu-id="e7963-114">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="e7963-114">PopulateResponseContent</span></span>](#populateresponsecontent) | <span data-ttu-id="e7963-115">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="e7963-115">Async method to request the Content stream of the response.</span></span>

<span data-ttu-id="e7963-116">Va contenir la requête telle qu’elle a été envoyée et la réponse telle qu’elle a été reçue.</span><span class="sxs-lookup"><span data-stu-id="e7963-116">Will contain the request as it was sent and the response as it was received.</span></span> <span data-ttu-id="e7963-117">Remarque: pour obtenir le flux de contenu de réponse, appelez d’abord PopulateResponseContent et attendez que l’appel asynchrone se termine, sinon l’objet de flux de contenu renvoyé sera null.</span><span class="sxs-lookup"><span data-stu-id="e7963-117">Note: To get the response content stream, first call PopulateResponseContent and wait for the async call to complete, otherwise the content stream object returned will be null.</span></span>

## <span data-ttu-id="e7963-118">Ses</span><span class="sxs-lookup"><span data-stu-id="e7963-118">Members</span></span>

#### <span data-ttu-id="e7963-119">get_Request</span><span class="sxs-lookup"><span data-stu-id="e7963-119">get_Request</span></span> 

<span data-ttu-id="e7963-120">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="e7963-120">Web resource request object.</span></span> <span data-ttu-id="e7963-121">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="e7963-121">Any modifications to this object will be ignored.</span></span>

> <span data-ttu-id="e7963-122">[get_Request](#get_request)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e7963-122">public HRESULT [get_Request](#get_request)(ICoreWebView2WebResourceRequest \*\* request)</span></span>

#### <span data-ttu-id="e7963-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="e7963-123">get_Response</span></span> 

<span data-ttu-id="e7963-124">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="e7963-124">Web resource response object.</span></span>

> <span data-ttu-id="e7963-125">valeur publique HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="e7963-125">public HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \*\* response)</span></span>

<span data-ttu-id="e7963-126">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="e7963-126">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="e7963-127">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="e7963-127">PopulateResponseContent</span></span> 

<span data-ttu-id="e7963-128">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="e7963-128">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="e7963-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)(gestionnaire[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="e7963-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \* handler)</span></span>

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

