---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: b1ef893b559933d3cc507b09257a884b8646046d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877993"
---
# <span data-ttu-id="16240-104">0.9.430-interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="16240-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="16240-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="16240-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="16240-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="16240-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="16240-107">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="16240-107">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="16240-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="16240-108">Summary</span></span>

 <span data-ttu-id="16240-109">Ses</span><span class="sxs-lookup"><span data-stu-id="16240-109">Members</span></span>                        | <span data-ttu-id="16240-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="16240-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16240-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="16240-111">Invoke</span></span>](#invoke) | <span data-ttu-id="16240-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="16240-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="16240-113">Ses</span><span class="sxs-lookup"><span data-stu-id="16240-113">Members</span></span>

#### <span data-ttu-id="16240-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="16240-114">Invoke</span></span> 

<span data-ttu-id="16240-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="16240-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="16240-116">[appel](#invoke)HRESULT public (résultat HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="16240-116">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>

