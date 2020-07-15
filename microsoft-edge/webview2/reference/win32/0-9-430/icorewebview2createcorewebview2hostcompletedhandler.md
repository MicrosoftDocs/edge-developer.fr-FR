---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 6a707465fa08667e9915a77fdc93ee018e0f9631
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881122"
---
# <span data-ttu-id="b6fff-104">0.9.430-interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b6fff-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b6fff-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b6fff-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b6fff-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="b6fff-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b6fff-107">L’appelant implémente cette interface pour recevoir les CoreWebView2Host créées via CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="b6fff-107">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="b6fff-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b6fff-108">Summary</span></span>

 <span data-ttu-id="b6fff-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b6fff-109">Members</span></span>                        | <span data-ttu-id="b6fff-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b6fff-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b6fff-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b6fff-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b6fff-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b6fff-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b6fff-113">Ses</span><span class="sxs-lookup"><span data-stu-id="b6fff-113">Members</span></span>

#### <span data-ttu-id="b6fff-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="b6fff-114">Invoke</span></span> 

<span data-ttu-id="b6fff-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b6fff-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b6fff-116">[appel](#invoke)HRESULT public (résultat HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="b6fff-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>

