---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebMessageReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 55ce9b2efc78bd4f0bf153c1e5655ff79d42af94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878154"
---
# <span data-ttu-id="119fb-104">0.8.355-interface IWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="119fb-104">0.8.355 - interface IWebView2WebMessageReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="119fb-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="119fb-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="119fb-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="119fb-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="119fb-107">L’appelant implémente cette interface pour recevoir l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="119fb-107">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="119fb-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="119fb-108">Summary</span></span>

 <span data-ttu-id="119fb-109">Ses</span><span class="sxs-lookup"><span data-stu-id="119fb-109">Members</span></span>                        | <span data-ttu-id="119fb-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="119fb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="119fb-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="119fb-111">Invoke</span></span>](#invoke) | <span data-ttu-id="119fb-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="119fb-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="119fb-113">Ses</span><span class="sxs-lookup"><span data-stu-id="119fb-113">Members</span></span>

#### <span data-ttu-id="119fb-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="119fb-114">Invoke</span></span> 

<span data-ttu-id="119fb-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="119fb-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="119fb-116">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="119fb-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebMessageReceivedEventArgs](IWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

