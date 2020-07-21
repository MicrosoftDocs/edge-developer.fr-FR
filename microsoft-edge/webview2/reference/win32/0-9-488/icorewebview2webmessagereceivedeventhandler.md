---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b69854163a45c09d605cac2f544866d58546c71b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885183"
---
# <span data-ttu-id="bb5d5-104">0.9.515-interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="bb5d5-104">0.9.515 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="bb5d5-105">L’appelant implémente cette interface pour recevoir l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="bb5d5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bb5d5-106">Summary</span></span>

 <span data-ttu-id="bb5d5-107">Ses</span><span class="sxs-lookup"><span data-stu-id="bb5d5-107">Members</span></span>                        | <span data-ttu-id="bb5d5-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bb5d5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bb5d5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="bb5d5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bb5d5-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="bb5d5-111">Ses</span><span class="sxs-lookup"><span data-stu-id="bb5d5-111">Members</span></span>

#### <span data-ttu-id="bb5d5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="bb5d5-112">Invoke</span></span> 

<span data-ttu-id="bb5d5-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bb5d5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bb5d5-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="bb5d5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

