---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 3ff529c649eb455e8ea1b14ebbd25533631d2b99
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011946"
---
# <span data-ttu-id="dc8ab-104">interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="dc8ab-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="dc8ab-105">L’appelant implémente cette interface pour recevoir l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="dc8ab-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="dc8ab-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="dc8ab-106">Summary</span></span>

 <span data-ttu-id="dc8ab-107">Ses</span><span class="sxs-lookup"><span data-stu-id="dc8ab-107">Members</span></span>                        | <span data-ttu-id="dc8ab-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="dc8ab-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc8ab-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc8ab-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dc8ab-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="dc8ab-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="dc8ab-111">Ses</span><span class="sxs-lookup"><span data-stu-id="dc8ab-111">Members</span></span>

#### <span data-ttu-id="dc8ab-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc8ab-112">Invoke</span></span> 

<span data-ttu-id="dc8ab-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="dc8ab-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="dc8ab-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="dc8ab-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>

