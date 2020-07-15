---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 26bbc2a5c55ebe5a9b7519a87b01c4dd17af375c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879561"
---
# <span data-ttu-id="e1a10-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e1a10-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="e1a10-105">L’appelant implémente cette interface pour recevoir l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e1a10-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="e1a10-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e1a10-106">Summary</span></span>

 <span data-ttu-id="e1a10-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e1a10-107">Members</span></span>                        | <span data-ttu-id="e1a10-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e1a10-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e1a10-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1a10-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e1a10-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e1a10-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e1a10-111">Ses</span><span class="sxs-lookup"><span data-stu-id="e1a10-111">Members</span></span>

#### <span data-ttu-id="e1a10-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e1a10-112">Invoke</span></span> 

<span data-ttu-id="e1a10-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e1a10-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e1a10-114">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e1a10-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

