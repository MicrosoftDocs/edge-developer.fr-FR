---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 61805f34ac3ef3a51dcd5b746b77a7bdad8cdb5c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877601"
---
# <span data-ttu-id="65ef9-104">interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="65ef9-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="65ef9-105">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="65ef9-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="65ef9-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="65ef9-106">Summary</span></span>

 <span data-ttu-id="65ef9-107">Ses</span><span class="sxs-lookup"><span data-stu-id="65ef9-107">Members</span></span>                        | <span data-ttu-id="65ef9-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="65ef9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65ef9-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="65ef9-109">get_Source</span></span>](#get_source) | <span data-ttu-id="65ef9-110">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="65ef9-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="65ef9-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="65ef9-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="65ef9-112">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="65ef9-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="65ef9-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="65ef9-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="65ef9-114">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="65ef9-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="65ef9-115">Ses</span><span class="sxs-lookup"><span data-stu-id="65ef9-115">Members</span></span>

#### <span data-ttu-id="65ef9-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="65ef9-116">get_Source</span></span> 

<span data-ttu-id="65ef9-117">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="65ef9-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="65ef9-118">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="65ef9-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="65ef9-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="65ef9-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="65ef9-120">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="65ef9-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="65ef9-121">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="65ef9-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="65ef9-122">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="65ef9-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="65ef9-123">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="65ef9-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="65ef9-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="65ef9-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="65ef9-125">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="65ef9-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="65ef9-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="65ef9-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="65ef9-127">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="65ef9-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="65ef9-128">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="65ef9-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="65ef9-129">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="65ef9-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

