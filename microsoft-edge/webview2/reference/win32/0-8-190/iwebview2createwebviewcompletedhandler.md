---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2CreateWebViewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 381f46c6682a77905d9caa720e4ba9b2d1d531b7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886151"
---
# <span data-ttu-id="197b2-104">0.8.355-interface IWebView2CreateWebViewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="197b2-104">0.8.355 - interface IWebView2CreateWebViewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebViewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="197b2-105">L’appelant implémente cette interface pour recevoir le WebView créé par le biais de CreateWebView.</span><span class="sxs-lookup"><span data-stu-id="197b2-105">The caller implements this interface to receive the WebView created via CreateWebView.</span></span>

## <span data-ttu-id="197b2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="197b2-106">Summary</span></span>

 <span data-ttu-id="197b2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="197b2-107">Members</span></span>                        | <span data-ttu-id="197b2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="197b2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="197b2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="197b2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="197b2-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="197b2-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="197b2-111">Ses</span><span class="sxs-lookup"><span data-stu-id="197b2-111">Members</span></span>

#### <span data-ttu-id="197b2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="197b2-112">Invoke</span></span> 

<span data-ttu-id="197b2-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="197b2-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="197b2-114">[appel](#invoke)HRESULT public (résultat HRESULT,[IWebView2WebView](IWebView2WebView.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="197b2-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2WebView](IWebView2WebView.md) \* webView)</span></span>

