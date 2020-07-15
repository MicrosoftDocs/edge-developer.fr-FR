---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2DocumentStateChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: b669d04ba46b1670610e1efb00b552b2b6b1a4fc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878567"
---
# <span data-ttu-id="bcb61-104">0.8.355-interface IWebView2DocumentStateChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="bcb61-104">0.8.355 - interface IWebView2DocumentStateChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="bcb61-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="bcb61-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="bcb61-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="bcb61-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="bcb61-107">L’appelant implémente cette interface pour recevoir l’événement DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="bcb61-107">The caller implements this interface to receive the DocumentStateChanged event.</span></span>

## <span data-ttu-id="bcb61-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="bcb61-108">Summary</span></span>

 <span data-ttu-id="bcb61-109">Ses</span><span class="sxs-lookup"><span data-stu-id="bcb61-109">Members</span></span>                        | <span data-ttu-id="bcb61-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bcb61-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bcb61-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="bcb61-111">Invoke</span></span>](#invoke) | <span data-ttu-id="bcb61-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bcb61-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="bcb61-113">Ses</span><span class="sxs-lookup"><span data-stu-id="bcb61-113">Members</span></span>

#### <span data-ttu-id="bcb61-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="bcb61-114">Invoke</span></span> 

<span data-ttu-id="bcb61-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bcb61-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bcb61-116">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="bcb61-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DocumentStateChangedEventArgs](IWebView2DocumentStateChangedEventArgs.md) \* args)</span></span>

