---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ProcessFailedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ProcessFailedEventHandler
ms.openlocfilehash: 98f3f092bc1feb75ea2f94857c31dd80bcb907ee
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011943"
---
# <span data-ttu-id="2bec2-104">interface ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2bec2-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="2bec2-105">L’appelant implémente cette interface pour recevoir des événements ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2bec2-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="2bec2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="2bec2-106">Summary</span></span>

 <span data-ttu-id="2bec2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="2bec2-107">Members</span></span>                        | <span data-ttu-id="2bec2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2bec2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2bec2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2bec2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2bec2-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2bec2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2bec2-111">Ses</span><span class="sxs-lookup"><span data-stu-id="2bec2-111">Members</span></span>

#### <span data-ttu-id="2bec2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2bec2-112">Invoke</span></span> 

<span data-ttu-id="2bec2-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2bec2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2bec2-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2bec2-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>

