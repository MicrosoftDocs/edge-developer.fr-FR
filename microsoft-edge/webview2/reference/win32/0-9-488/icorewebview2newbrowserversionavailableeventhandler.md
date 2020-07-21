---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: aa59efbb0b47977b41236950c47a01d6d95ee123
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886291"
---
# <span data-ttu-id="c8673-104">0.9.515-interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="c8673-104">0.9.515 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="c8673-105">L’appelant implémente cette interface pour recevoir des événements NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="c8673-105">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="c8673-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c8673-106">Summary</span></span>

 <span data-ttu-id="c8673-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c8673-107">Members</span></span>                        | <span data-ttu-id="c8673-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c8673-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c8673-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c8673-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c8673-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c8673-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="c8673-111">Ses</span><span class="sxs-lookup"><span data-stu-id="c8673-111">Members</span></span>

#### <span data-ttu-id="c8673-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="c8673-112">Invoke</span></span> 

<span data-ttu-id="c8673-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c8673-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c8673-114">[appel](#invoke)HRESULT public ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c8673-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

