---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 1a541bc5c735f67013464347781de5163a7c01b2
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011981"
---
# <span data-ttu-id="72e58-104">interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="72e58-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="72e58-105">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="72e58-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="72e58-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="72e58-106">Summary</span></span>

 <span data-ttu-id="72e58-107">Ses</span><span class="sxs-lookup"><span data-stu-id="72e58-107">Members</span></span>                        | <span data-ttu-id="72e58-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="72e58-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="72e58-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="72e58-109">get_Source</span></span>](#get_source) | <span data-ttu-id="72e58-110">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="72e58-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="72e58-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="72e58-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="72e58-112">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="72e58-112">The message posted from the WebView content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="72e58-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="72e58-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="72e58-114">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="72e58-114">If the message posted from the WebView content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="72e58-115">Ses</span><span class="sxs-lookup"><span data-stu-id="72e58-115">Members</span></span>

#### <span data-ttu-id="72e58-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="72e58-116">get_Source</span></span> 

<span data-ttu-id="72e58-117">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="72e58-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="72e58-118">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="72e58-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="72e58-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="72e58-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="72e58-120">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="72e58-120">The message posted from the WebView content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="72e58-121">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="72e58-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="72e58-122">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="72e58-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="72e58-123">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="72e58-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="72e58-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="72e58-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="72e58-125">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="72e58-125">If the message posted from the WebView content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="72e58-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="72e58-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="72e58-127">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="72e58-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="72e58-128">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="72e58-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="72e58-129">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="72e58-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

