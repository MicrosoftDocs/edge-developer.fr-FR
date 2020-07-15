---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 24651585298998eaa42b2be242785de1bf4d6f84
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879792"
---
# <span data-ttu-id="20938-104">interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="20938-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="20938-105">L’appelant implémente cette interface pour recevoir l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="20938-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="20938-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="20938-106">Summary</span></span>

 <span data-ttu-id="20938-107">Ses</span><span class="sxs-lookup"><span data-stu-id="20938-107">Members</span></span>                        | <span data-ttu-id="20938-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="20938-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="20938-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="20938-109">Invoke</span></span>](#invoke) | <span data-ttu-id="20938-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="20938-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="20938-111">Ses</span><span class="sxs-lookup"><span data-stu-id="20938-111">Members</span></span>

#### <span data-ttu-id="20938-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="20938-112">Invoke</span></span> 

<span data-ttu-id="20938-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="20938-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="20938-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="20938-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>

