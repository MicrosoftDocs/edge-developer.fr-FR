---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: fe84f29798b01aed2787559c717f2893c9eda7f9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885939"
---
# <span data-ttu-id="003b0-104">0.8.355-interface IWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="003b0-104">0.8.355 - interface IWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="003b0-105">L’appelant implémente cette méthode pour recevoir l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="003b0-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="003b0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="003b0-106">Summary</span></span>

 <span data-ttu-id="003b0-107">Ses</span><span class="sxs-lookup"><span data-stu-id="003b0-107">Members</span></span>                        | <span data-ttu-id="003b0-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="003b0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="003b0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="003b0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="003b0-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="003b0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="003b0-111">Ses</span><span class="sxs-lookup"><span data-stu-id="003b0-111">Members</span></span>

#### <span data-ttu-id="003b0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="003b0-112">Invoke</span></span> 

<span data-ttu-id="003b0-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="003b0-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="003b0-114">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="003b0-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2MoveFocusRequestedEventArgs](IWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

