---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2CreateWebViewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 3459bf9c44dc4f0ce10bc383f6f695d4949023da
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878637"
---
# <span data-ttu-id="43b53-104">0.8.355-interface IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="43b53-104">0.8.355 - interface IWebView2CreateWebViewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="43b53-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="43b53-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="43b53-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="43b53-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="43b53-107">L’appelant implémente cette interface pour recevoir le WebView créé par le biais de CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="43b53-107">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="43b53-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="43b53-108">Summary</span></span>

 <span data-ttu-id="43b53-109">Ses</span><span class="sxs-lookup"><span data-stu-id="43b53-109">Members</span></span>                        | <span data-ttu-id="43b53-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="43b53-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="43b53-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="43b53-111">Invoke</span></span>](#invoke) | <span data-ttu-id="43b53-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="43b53-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="43b53-113">Ses</span><span class="sxs-lookup"><span data-stu-id="43b53-113">Members</span></span>

#### <span data-ttu-id="43b53-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="43b53-114">Invoke</span></span> 

<span data-ttu-id="43b53-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="43b53-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="43b53-116">[appel](#invoke)HRESULT public (résultat HRESULT,[IWebView2WebView](IWebView2WebView.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="43b53-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>

