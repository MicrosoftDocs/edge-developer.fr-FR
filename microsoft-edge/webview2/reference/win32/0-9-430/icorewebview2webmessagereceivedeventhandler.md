---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: f566cb8aa876304d17e11bb47f24692aefda3b26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883755"
---
# <span data-ttu-id="f7b15-104">0.9.430-interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f7b15-104">0.9.430 - interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="f7b15-105">L’appelant implémente cette interface pour recevoir l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="f7b15-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="f7b15-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f7b15-106">Summary</span></span>

 <span data-ttu-id="f7b15-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f7b15-107">Members</span></span>                        | <span data-ttu-id="f7b15-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f7b15-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f7b15-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7b15-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f7b15-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f7b15-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f7b15-111">Ses</span><span class="sxs-lookup"><span data-stu-id="f7b15-111">Members</span></span>

#### <span data-ttu-id="f7b15-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f7b15-112">Invoke</span></span> 

<span data-ttu-id="f7b15-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f7b15-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f7b15-114">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f7b15-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

