---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 58bb4b7f34b2917ec16ead051d1df8d6e6885f6d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010382"
---
# <span data-ttu-id="553da-104">0.9.579-interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="553da-104">0.9.579 - interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="553da-105">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="553da-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="553da-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="553da-106">Summary</span></span>

 <span data-ttu-id="553da-107">Ses</span><span class="sxs-lookup"><span data-stu-id="553da-107">Members</span></span>                        | <span data-ttu-id="553da-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="553da-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="553da-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="553da-109">get_Source</span></span>](#get_source) | <span data-ttu-id="553da-110">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="553da-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="553da-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="553da-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="553da-112">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="553da-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="553da-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="553da-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="553da-114">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="553da-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="553da-115">Ses</span><span class="sxs-lookup"><span data-stu-id="553da-115">Members</span></span>

#### <span data-ttu-id="553da-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="553da-116">get_Source</span></span> 

<span data-ttu-id="553da-117">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="553da-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="553da-118">valeur publique HRESULT [get_Source](#get_source)(LPWSTR \* source)</span><span class="sxs-lookup"><span data-stu-id="553da-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="553da-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="553da-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="553da-120">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="553da-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="553da-121">valeur publique HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="553da-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="553da-122">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="553da-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="553da-123">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="553da-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="553da-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="553da-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="553da-125">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="553da-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="553da-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="553da-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="553da-127">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="553da-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="553da-128">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="553da-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="553da-129">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="553da-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

