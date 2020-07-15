---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 82b60e43d059cca25c9c3f44cf6136e32a4469ae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880660"
---
# <span data-ttu-id="c0b8a-104">0.9.515-interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="c0b8a-104">0.9.515 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c0b8a-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="c0b8a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="c0b8a-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="c0b8a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="c0b8a-107">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="c0b8a-107">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="c0b8a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c0b8a-108">Summary</span></span>

 <span data-ttu-id="c0b8a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c0b8a-109">Members</span></span>                        | <span data-ttu-id="c0b8a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c0b8a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0b8a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c0b8a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c0b8a-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="c0b8a-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="c0b8a-113">Ses</span><span class="sxs-lookup"><span data-stu-id="c0b8a-113">Members</span></span>

#### <span data-ttu-id="c0b8a-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="c0b8a-114">Invoke</span></span> 

<span data-ttu-id="c0b8a-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="c0b8a-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="c0b8a-116">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="c0b8a-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

