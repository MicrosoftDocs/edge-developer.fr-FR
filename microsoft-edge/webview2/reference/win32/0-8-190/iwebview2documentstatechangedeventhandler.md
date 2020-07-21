---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2DocumentStateChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 3d6bf8345e88dde213c15e51c26056d0239f0230
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886109"
---
# <span data-ttu-id="3bb2d-104">0.8.355-interface IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3bb2d-104">0.8.355 - interface IWebView2DocumentStateChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3bb2d-105">L’appelant implémente cette interface pour recevoir l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="3bb2d-105">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="3bb2d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3bb2d-106">Summary</span></span>

 <span data-ttu-id="3bb2d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3bb2d-107">Members</span></span>                        | <span data-ttu-id="3bb2d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3bb2d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3bb2d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3bb2d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3bb2d-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3bb2d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3bb2d-111">Ses</span><span class="sxs-lookup"><span data-stu-id="3bb2d-111">Members</span></span>

#### <span data-ttu-id="3bb2d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3bb2d-112">Invoke</span></span> 

<span data-ttu-id="3bb2d-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3bb2d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3bb2d-114">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3bb2d-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>

