---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NewBrowserVersionAvailableEventHandler
ms.openlocfilehash: 82a5e73b8b928897e5c0af1610631c9e7d636337
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879743"
---
# <span data-ttu-id="baf20-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="baf20-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="baf20-105">L’appelant implémente cette interface pour recevoir des événements NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="baf20-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="baf20-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="baf20-106">Summary</span></span>

 <span data-ttu-id="baf20-107">Ses</span><span class="sxs-lookup"><span data-stu-id="baf20-107">Members</span></span>                        | <span data-ttu-id="baf20-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="baf20-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="baf20-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="baf20-109">Invoke</span></span>](#invoke) | <span data-ttu-id="baf20-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="baf20-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="baf20-111">Ses</span><span class="sxs-lookup"><span data-stu-id="baf20-111">Members</span></span>

#### <span data-ttu-id="baf20-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="baf20-112">Invoke</span></span> 

<span data-ttu-id="baf20-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="baf20-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="baf20-114">[appel](#invoke)HRESULT public ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="baf20-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

