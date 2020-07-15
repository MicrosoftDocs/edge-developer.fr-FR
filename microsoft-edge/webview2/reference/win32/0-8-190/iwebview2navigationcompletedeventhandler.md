---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 4d1ce0723ecd1ce79cd2a3f95ccd5af9561e6f0b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878406"
---
# <span data-ttu-id="667f9-104">0.8.355-interface IWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="667f9-104">0.8.355 - interface IWebView2NavigationCompletedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="667f9-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="667f9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="667f9-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="667f9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="667f9-107">L’appelant implémente cette interface pour recevoir l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="667f9-107">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="667f9-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="667f9-108">Summary</span></span>

 <span data-ttu-id="667f9-109">Ses</span><span class="sxs-lookup"><span data-stu-id="667f9-109">Members</span></span>                        | <span data-ttu-id="667f9-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="667f9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="667f9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="667f9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="667f9-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="667f9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="667f9-113">Ses</span><span class="sxs-lookup"><span data-stu-id="667f9-113">Members</span></span>

#### <span data-ttu-id="667f9-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="667f9-114">Invoke</span></span> 

<span data-ttu-id="667f9-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="667f9-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="667f9-116">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="667f9-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NavigationCompletedEventArgs](IWebView2NavigationCompletedEventArgs.md) \* args)</span></span>

