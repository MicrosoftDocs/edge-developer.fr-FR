---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: c8444741480ba3b07d2755dcac0ec11f7194a783
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698751"
---
# <span data-ttu-id="21e70-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="21e70-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="21e70-105">L’appelant implémente cette interface pour recevoir des événements NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="21e70-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="21e70-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="21e70-106">Summary</span></span>

 <span data-ttu-id="21e70-107">Ses</span><span class="sxs-lookup"><span data-stu-id="21e70-107">Members</span></span>                        | <span data-ttu-id="21e70-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="21e70-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21e70-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="21e70-109">Invoke</span></span>](#invoke) | <span data-ttu-id="21e70-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="21e70-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="21e70-111">Ses</span><span class="sxs-lookup"><span data-stu-id="21e70-111">Members</span></span>

#### <span data-ttu-id="21e70-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="21e70-112">Invoke</span></span> 

<span data-ttu-id="21e70-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="21e70-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="21e70-114">[appel](#invoke)HRESULT public ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="21e70-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

