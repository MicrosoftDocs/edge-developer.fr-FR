---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: bacd1cff4406caffd4d7c3e1ca4c3e320c051443
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878322"
---
# <span data-ttu-id="23e3a-104">0.8.355-interface IWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="23e3a-104">0.8.355 - interface IWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="23e3a-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="23e3a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="23e3a-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="23e3a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="23e3a-107">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="23e3a-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="23e3a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="23e3a-108">Summary</span></span>

 <span data-ttu-id="23e3a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="23e3a-109">Members</span></span>                        | <span data-ttu-id="23e3a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="23e3a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="23e3a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="23e3a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="23e3a-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="23e3a-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="23e3a-113">Ses</span><span class="sxs-lookup"><span data-stu-id="23e3a-113">Members</span></span>

#### <span data-ttu-id="23e3a-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="23e3a-114">Invoke</span></span> 

<span data-ttu-id="23e3a-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="23e3a-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="23e3a-116">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="23e3a-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2NewWindowRequestedEventArgs](IWebView2NewWindowRequestedEventArgs.md) \* args)</span></span>

