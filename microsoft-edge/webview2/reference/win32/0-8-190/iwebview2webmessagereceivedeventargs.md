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
ms.openlocfilehash: 053e186aec3871b47e2eb5c6684bc00c934c3a77
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653377"
---
# <span data-ttu-id="95e7d-104">interface IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="95e7d-104">interface IWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="95e7d-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="95e7d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="95e7d-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="95e7d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="95e7d-107">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="95e7d-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="95e7d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="95e7d-108">Summary</span></span>

 <span data-ttu-id="95e7d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="95e7d-109">Members</span></span>                        | <span data-ttu-id="95e7d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="95e7d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95e7d-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="95e7d-111">get_Source</span></span>](#get_source) | <span data-ttu-id="95e7d-112">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="95e7d-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="95e7d-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="95e7d-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="95e7d-114">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="95e7d-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="95e7d-115">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="95e7d-115">get_WebMessageAsString</span></span>](#get_webmessageasstring) | <span data-ttu-id="95e7d-116">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="95e7d-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="95e7d-117">Ses</span><span class="sxs-lookup"><span data-stu-id="95e7d-117">Members</span></span>

#### <span data-ttu-id="95e7d-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="95e7d-118">get_Source</span></span> 

<span data-ttu-id="95e7d-119">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="95e7d-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="95e7d-120">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="95e7d-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="95e7d-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="95e7d-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="95e7d-122">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="95e7d-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="95e7d-123">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="95e7d-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="95e7d-124">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="95e7d-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="95e7d-125">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="95e7d-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="95e7d-126">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="95e7d-126">get_WebMessageAsString</span></span> 

<span data-ttu-id="95e7d-127">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="95e7d-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="95e7d-128">valeur publique HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* WebMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="95e7d-128">public HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="95e7d-129">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="95e7d-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="95e7d-130">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="95e7d-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="95e7d-131">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="95e7d-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

