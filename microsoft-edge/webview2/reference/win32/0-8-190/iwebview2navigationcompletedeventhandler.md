---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: cf799ae12b977f66bfba4d1b7664e3abc6241304
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885920"
---
# <span data-ttu-id="10bdb-104">0.8.355-interface IWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="10bdb-104">0.8.355 - interface IWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="10bdb-105">L’appelant implémente cette interface pour recevoir l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="10bdb-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="10bdb-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="10bdb-106">Summary</span></span>

 <span data-ttu-id="10bdb-107">Ses</span><span class="sxs-lookup"><span data-stu-id="10bdb-107">Members</span></span>                        | <span data-ttu-id="10bdb-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="10bdb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10bdb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="10bdb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="10bdb-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="10bdb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="10bdb-111">Ses</span><span class="sxs-lookup"><span data-stu-id="10bdb-111">Members</span></span>

#### <span data-ttu-id="10bdb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="10bdb-112">Invoke</span></span> 

<span data-ttu-id="10bdb-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="10bdb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="10bdb-114">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="10bdb-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span></span>

