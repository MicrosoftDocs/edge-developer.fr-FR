---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: f5c1799225df5460029b3ad0c40db63a2e16113c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011811"
---
# <span data-ttu-id="49e76-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="49e76-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="49e76-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="49e76-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="49e76-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="49e76-106">Summary</span></span>

 <span data-ttu-id="49e76-107">Ses</span><span class="sxs-lookup"><span data-stu-id="49e76-107">Members</span></span>                        | <span data-ttu-id="49e76-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="49e76-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49e76-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="49e76-109">Invoke</span></span>](#invoke) | <span data-ttu-id="49e76-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="49e76-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="49e76-111">Ses</span><span class="sxs-lookup"><span data-stu-id="49e76-111">Members</span></span>

#### <span data-ttu-id="49e76-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="49e76-112">Invoke</span></span> 

<span data-ttu-id="49e76-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="49e76-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="49e76-114">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="49e76-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="49e76-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="49e76-115">There are no event args and the args parameter will be null.</span></span>

