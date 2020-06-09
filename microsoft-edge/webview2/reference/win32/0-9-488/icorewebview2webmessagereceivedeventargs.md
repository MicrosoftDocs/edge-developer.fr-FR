---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 6e0c20f8763e8895c4b5ebdcdfe9ea7d70aca2b8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698126"
---
# <span data-ttu-id="c4572-104">interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c4572-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c4572-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c4572-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c4572-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="c4572-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="c4572-107">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="c4572-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="c4572-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c4572-108">Summary</span></span>

 <span data-ttu-id="c4572-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c4572-109">Members</span></span>                        | <span data-ttu-id="c4572-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c4572-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4572-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="c4572-111">get_Source</span></span>](#get_source) | <span data-ttu-id="c4572-112">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="c4572-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="c4572-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="c4572-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="c4572-114">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="c4572-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="c4572-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="c4572-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="c4572-116">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="c4572-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="c4572-117">Ses</span><span class="sxs-lookup"><span data-stu-id="c4572-117">Members</span></span>

#### <span data-ttu-id="c4572-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="c4572-118">get_Source</span></span> 

<span data-ttu-id="c4572-119">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="c4572-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="c4572-120">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="c4572-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="c4572-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="c4572-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="c4572-122">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="c4572-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="c4572-123">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="c4572-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="c4572-124">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c4572-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="c4572-125">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="c4572-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="c4572-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="c4572-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="c4572-127">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="c4572-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="c4572-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="c4572-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="c4572-129">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="c4572-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="c4572-130">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="c4572-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="c4572-131">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="c4572-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

