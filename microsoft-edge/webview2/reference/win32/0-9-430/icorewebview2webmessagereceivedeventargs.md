---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: f3002c6e7941cea1f632e1df4ee42a8f38a468b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653641"
---
# <span data-ttu-id="377b8-104">interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="377b8-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="377b8-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="377b8-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="377b8-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="377b8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="377b8-107">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="377b8-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="377b8-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="377b8-108">Summary</span></span>

 <span data-ttu-id="377b8-109">Ses</span><span class="sxs-lookup"><span data-stu-id="377b8-109">Members</span></span>                        | <span data-ttu-id="377b8-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="377b8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="377b8-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="377b8-111">get_Source</span></span>](#get_source) | <span data-ttu-id="377b8-112">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="377b8-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="377b8-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="377b8-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="377b8-114">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="377b8-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="377b8-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="377b8-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="377b8-116">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="377b8-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="377b8-117">Ses</span><span class="sxs-lookup"><span data-stu-id="377b8-117">Members</span></span>

#### <span data-ttu-id="377b8-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="377b8-118">get_Source</span></span> 

<span data-ttu-id="377b8-119">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="377b8-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="377b8-120">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="377b8-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="377b8-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="377b8-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="377b8-122">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="377b8-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="377b8-123">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="377b8-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="377b8-124">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="377b8-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="377b8-125">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="377b8-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="377b8-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="377b8-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="377b8-127">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="377b8-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="377b8-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="377b8-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="377b8-129">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="377b8-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="377b8-130">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="377b8-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="377b8-131">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="377b8-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

