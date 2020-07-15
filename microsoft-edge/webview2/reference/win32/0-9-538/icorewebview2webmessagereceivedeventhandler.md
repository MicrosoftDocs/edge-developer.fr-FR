---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WebMessageReceivedEventHandler
ms.openlocfilehash: 47402035918c49a86c8e973c207d4f54d7d829c7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879351"
---
# <span data-ttu-id="b0c1d-104">interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b0c1d-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="b0c1d-105">L’appelant implémente cette interface pour recevoir l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="b0c1d-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="b0c1d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b0c1d-106">Summary</span></span>

 <span data-ttu-id="b0c1d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b0c1d-107">Members</span></span>                        | <span data-ttu-id="b0c1d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b0c1d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b0c1d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0c1d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b0c1d-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="b0c1d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b0c1d-111">Ses</span><span class="sxs-lookup"><span data-stu-id="b0c1d-111">Members</span></span>

#### <span data-ttu-id="b0c1d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0c1d-112">Invoke</span></span> 

<span data-ttu-id="b0c1d-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="b0c1d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b0c1d-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b0c1d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

