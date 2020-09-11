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
# <span data-ttu-id="c51bd-104">0.9.579-interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c51bd-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="c51bd-105">Arguments d’événement pour l’événement WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="c51bd-105">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="c51bd-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c51bd-106">Summary</span></span>

 <span data-ttu-id="c51bd-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c51bd-107">Members</span></span>                        | <span data-ttu-id="c51bd-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c51bd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c51bd-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="c51bd-109">get_Request</span></span>](#get_request) | <span data-ttu-id="c51bd-110">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="c51bd-110">Web resource request object.</span></span> <span data-ttu-id="c51bd-111">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="c51bd-111">Any modifications to this object will be ignored.</span></span>
[<span data-ttu-id="c51bd-112">get_Response</span><span class="sxs-lookup"><span data-stu-id="c51bd-112">get_Response</span></span>](#get_response) | <span data-ttu-id="c51bd-113">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="c51bd-113">Web resource response object.</span></span>
[<span data-ttu-id="c51bd-114">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="c51bd-114">PopulateResponseContent</span></span>](#populateresponsecontent) | <span data-ttu-id="c51bd-115">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="c51bd-115">Async method to request the Content stream of the response.</span></span>

<span data-ttu-id="c51bd-116">Va contenir la requête telle qu’elle a été envoyée et la réponse telle qu’elle a été reçue.</span><span class="sxs-lookup"><span data-stu-id="c51bd-116">Will contain the request as it was sent and the response as it was received.</span></span> <span data-ttu-id="c51bd-117">Remarque: pour obtenir le flux de contenu de réponse, appelez d’abord PopulateResponseContent et attendez que l’appel asynchrone se termine, sinon l’objet de flux de contenu renvoyé sera null.</span><span class="sxs-lookup"><span data-stu-id="c51bd-117">Note: To get the response content stream, first call PopulateResponseContent and wait for the async call to complete, otherwise the content stream object returned will be null.</span></span>

## <span data-ttu-id="c51bd-118">Ses</span><span class="sxs-lookup"><span data-stu-id="c51bd-118">Members</span></span>

#### <span data-ttu-id="c51bd-119">get_Request</span><span class="sxs-lookup"><span data-stu-id="c51bd-119">get_Request</span></span> 

<span data-ttu-id="c51bd-120">Objet demande de ressources Web.</span><span class="sxs-lookup"><span data-stu-id="c51bd-120">Web resource request object.</span></span> <span data-ttu-id="c51bd-121">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="c51bd-121">Any modifications to this object will be ignored.</span></span>

> <span data-ttu-id="c51bd-122">[get_Request](#get_request)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="c51bd-122">public HRESULT [get_Request](#get_request)(ICoreWebView2WebResourceRequest \*\* request)</span></span>

#### <span data-ttu-id="c51bd-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="c51bd-123">get_Response</span></span> 

<span data-ttu-id="c51bd-124">Objet de réponse aux ressources Web.</span><span class="sxs-lookup"><span data-stu-id="c51bd-124">Web resource response object.</span></span>

> <span data-ttu-id="c51bd-125">valeur publique HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="c51bd-125">public HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \*\* response)</span></span>

<span data-ttu-id="c51bd-126">Toute modification apportée à cet objet sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="c51bd-126">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="c51bd-127">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="c51bd-127">PopulateResponseContent</span></span> 

<span data-ttu-id="c51bd-128">Méthode Async pour demander le flux de contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="c51bd-128">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="c51bd-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)(gestionnaire[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="c51bd-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \* handler)</span></span>

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

