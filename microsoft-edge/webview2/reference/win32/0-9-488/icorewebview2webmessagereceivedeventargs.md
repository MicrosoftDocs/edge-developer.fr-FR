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
ms.openlocfilehash: c57c0df57915361e2d32024a5512616dea96a923
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653597"
---
# <span data-ttu-id="e5f9b-104">interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e5f9b-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="e5f9b-105">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="e5f9b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e5f9b-106">Summary</span></span>

 <span data-ttu-id="e5f9b-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e5f9b-107">Members</span></span>                        | <span data-ttu-id="e5f9b-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e5f9b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5f9b-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="e5f9b-109">get_Source</span></span>](#get_source) | <span data-ttu-id="e5f9b-110">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="e5f9b-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="e5f9b-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="e5f9b-112">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="e5f9b-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="e5f9b-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="e5f9b-114">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="e5f9b-115">Ses</span><span class="sxs-lookup"><span data-stu-id="e5f9b-115">Members</span></span>

#### <span data-ttu-id="e5f9b-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="e5f9b-116">get_Source</span></span> 

<span data-ttu-id="e5f9b-117">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="e5f9b-118">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="e5f9b-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="e5f9b-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="e5f9b-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="e5f9b-120">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="e5f9b-121">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="e5f9b-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="e5f9b-122">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="e5f9b-123">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="e5f9b-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="e5f9b-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="e5f9b-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="e5f9b-125">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="e5f9b-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="e5f9b-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="e5f9b-127">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="e5f9b-128">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="e5f9b-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="e5f9b-129">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="e5f9b-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

