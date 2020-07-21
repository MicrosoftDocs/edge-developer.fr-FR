---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 4dfe2296312ac3ff3e9c67667c660aafcea38211
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885757"
---
# <span data-ttu-id="d50e4-104">0.8.355-interface IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d50e4-104">0.8.355 - interface IWebView2WebMessageReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="d50e4-105">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="d50e4-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="d50e4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d50e4-106">Summary</span></span>

 <span data-ttu-id="d50e4-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d50e4-107">Members</span></span>                        | <span data-ttu-id="d50e4-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d50e4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d50e4-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="d50e4-109">get_Source</span></span>](#get_source) | <span data-ttu-id="d50e4-110">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="d50e4-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="d50e4-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d50e4-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="d50e4-112">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="d50e4-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="d50e4-113">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d50e4-113">get_WebMessageAsString</span></span>](#get_webmessageasstring) | <span data-ttu-id="d50e4-114">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="d50e4-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="d50e4-115">Ses</span><span class="sxs-lookup"><span data-stu-id="d50e4-115">Members</span></span>

#### <span data-ttu-id="d50e4-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="d50e4-116">get_Source</span></span> 

<span data-ttu-id="d50e4-117">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="d50e4-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="d50e4-118">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="d50e4-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="d50e4-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="d50e4-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="d50e4-120">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="d50e4-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="d50e4-121">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="d50e4-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="d50e4-122">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d50e4-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="d50e4-123">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="d50e4-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="d50e4-124">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="d50e4-124">get_WebMessageAsString</span></span> 

<span data-ttu-id="d50e4-125">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="d50e4-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="d50e4-126">valeur publique HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* WebMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="d50e4-126">public HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="d50e4-127">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="d50e4-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="d50e4-128">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="d50e4-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="d50e4-129">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="d50e4-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

