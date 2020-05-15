---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: f9bedb19620b0669d4aac35be4786702940b2a72
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653345"
---
# <span data-ttu-id="04d96-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="04d96-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="04d96-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="04d96-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="04d96-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="04d96-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="04d96-107">Arguments d’événement pour l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="04d96-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="04d96-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="04d96-108">Summary</span></span>

 <span data-ttu-id="04d96-109">Ses</span><span class="sxs-lookup"><span data-stu-id="04d96-109">Members</span></span>                        | <span data-ttu-id="04d96-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="04d96-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04d96-111">Source</span><span class="sxs-lookup"><span data-stu-id="04d96-111">Source</span></span>](#source) | <span data-ttu-id="04d96-112">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="04d96-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="04d96-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="04d96-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="04d96-114">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="04d96-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="04d96-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="04d96-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="04d96-116">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="04d96-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="04d96-117">Ses</span><span class="sxs-lookup"><span data-stu-id="04d96-117">Members</span></span>

#### <span data-ttu-id="04d96-118">Source</span><span class="sxs-lookup"><span data-stu-id="04d96-118">Source</span></span> 

<span data-ttu-id="04d96-119">URI du document qui a envoyé ce message Web.</span><span class="sxs-lookup"><span data-stu-id="04d96-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="04d96-120">[source](#source) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="04d96-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="04d96-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="04d96-121">WebMessageAsJson</span></span> 

<span data-ttu-id="04d96-122">Le message publié à partir du contenu de l’affichage Web dans l’hôte converti en chaîne JSON.</span><span class="sxs-lookup"><span data-stu-id="04d96-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="04d96-123">[WebMessageAsJson](#webmessageasjson) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="04d96-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="04d96-124">Utilisez cette fonction pour communiquer par le biais d’objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="04d96-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="04d96-125">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsJson suivantes:</span><span class="sxs-lookup"><span data-stu-id="04d96-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="04d96-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="04d96-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="04d96-127">Si le message publié à partir du contenu WebView sur l’hôte est de type chaîne, cette méthode retourne la valeur de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="04d96-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="04d96-128">chaîne publique [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="04d96-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="04d96-129">Si le message publié est un autre type de type JavaScript, cette méthode échoue avec E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="04d96-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="04d96-130">Utilisez cette fonction pour communiquer via des chaînes simples.</span><span class="sxs-lookup"><span data-stu-id="04d96-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="04d96-131">Par exemple, les appels de postMessage suivants génèrent les valeurs WebMessageAsString suivantes:</span><span class="sxs-lookup"><span data-stu-id="04d96-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

