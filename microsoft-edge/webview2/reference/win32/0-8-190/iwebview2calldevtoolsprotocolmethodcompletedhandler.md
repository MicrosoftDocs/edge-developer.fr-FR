---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: b8501c7287d5160f0fac980752721c83a0f48de7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886233"
---
# <span data-ttu-id="95de2-104">0.8.355-interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="95de2-104">0.8.355 - interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="95de2-105">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="95de2-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="95de2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="95de2-106">Summary</span></span>

 <span data-ttu-id="95de2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="95de2-107">Members</span></span>                        | <span data-ttu-id="95de2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="95de2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95de2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="95de2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="95de2-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="95de2-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="95de2-111">Ses</span><span class="sxs-lookup"><span data-stu-id="95de2-111">Members</span></span>

#### <span data-ttu-id="95de2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="95de2-112">Invoke</span></span> 

<span data-ttu-id="95de2-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="95de2-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="95de2-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="95de2-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>

