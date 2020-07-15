---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 9cd221ac1b528b0be52201daa0c15217534944a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879225"
---
# <span data-ttu-id="e3b31-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e3b31-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e3b31-105">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="e3b31-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="e3b31-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e3b31-106">Summary</span></span>

 <span data-ttu-id="e3b31-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e3b31-107">Members</span></span>                        | <span data-ttu-id="e3b31-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e3b31-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e3b31-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e3b31-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e3b31-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e3b31-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e3b31-111">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="e3b31-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="e3b31-112">Ses</span><span class="sxs-lookup"><span data-stu-id="e3b31-112">Members</span></span>

#### <span data-ttu-id="e3b31-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e3b31-113">Invoke</span></span> 

<span data-ttu-id="e3b31-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e3b31-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e3b31-115">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e3b31-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

