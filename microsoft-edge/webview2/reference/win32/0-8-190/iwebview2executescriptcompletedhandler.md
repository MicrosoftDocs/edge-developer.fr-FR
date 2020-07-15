---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: ecd3215c343925614b81d5da96fbf996350fd5a5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878504"
---
# <span data-ttu-id="ebfa6-104">0.8.355-interface IWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ebfa6-104">0.8.355 - interface IWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ebfa6-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="ebfa6-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ebfa6-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="ebfa6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ebfa6-107">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="ebfa6-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="ebfa6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="ebfa6-108">Summary</span></span>

 <span data-ttu-id="ebfa6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="ebfa6-109">Members</span></span>                        | <span data-ttu-id="ebfa6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ebfa6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ebfa6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ebfa6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ebfa6-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="ebfa6-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ebfa6-113">Ses</span><span class="sxs-lookup"><span data-stu-id="ebfa6-113">Members</span></span>

#### <span data-ttu-id="ebfa6-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ebfa6-114">Invoke</span></span> 

<span data-ttu-id="ebfa6-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="ebfa6-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ebfa6-116">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="ebfa6-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

