---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: fea602ee66d1183c1cd78da02471274ea43b38e8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878588"
---
# <span data-ttu-id="3b3d1-104">0.8.355-interface IWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3b3d1-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3b3d1-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3b3d1-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3b3d1-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="3b3d1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="3b3d1-107">L’appelant implémente cette interface pour recevoir des événements DevToolsProtocolEventReceived à partir du [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="3b3d1-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the [IWebView2WebView](IWebView2WebView.md).</span></span>

## <span data-ttu-id="3b3d1-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3b3d1-108">Summary</span></span>

 <span data-ttu-id="3b3d1-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3b3d1-109">Members</span></span>                        | <span data-ttu-id="3b3d1-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3b3d1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3b3d1-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="3b3d1-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3b3d1-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3b3d1-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3b3d1-113">Ses</span><span class="sxs-lookup"><span data-stu-id="3b3d1-113">Members</span></span>

#### <span data-ttu-id="3b3d1-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="3b3d1-114">Invoke</span></span> 

<span data-ttu-id="3b3d1-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3b3d1-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3b3d1-116">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3b3d1-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2DevToolsProtocolEventReceivedEventArgs](IWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>

