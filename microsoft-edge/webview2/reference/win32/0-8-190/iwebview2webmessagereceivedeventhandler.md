---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 772ad4ce7bd1ae0c1f02475206380c146ecabf7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885743"
---
# <span data-ttu-id="3f637-104">0.8.355-interface IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3f637-104">0.8.355 - interface IWebView2WebMessageReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="3f637-105">L’appelant implémente cette interface pour recevoir l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="3f637-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="3f637-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3f637-106">Summary</span></span>

 <span data-ttu-id="3f637-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3f637-107">Members</span></span>                        | <span data-ttu-id="3f637-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3f637-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3f637-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f637-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3f637-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3f637-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3f637-111">Ses</span><span class="sxs-lookup"><span data-stu-id="3f637-111">Members</span></span>

#### <span data-ttu-id="3f637-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3f637-112">Invoke</span></span> 

<span data-ttu-id="3f637-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3f637-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3f637-114">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3f637-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

