---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 7a4e074d445b4bab11e8e79dc6cfe5346effbb3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653616"
---
# <span data-ttu-id="51f26-104">interface IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="51f26-104">interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="51f26-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="51f26-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="51f26-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="51f26-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="51f26-107">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="51f26-107">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="51f26-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="51f26-108">Summary</span></span>

 <span data-ttu-id="51f26-109">Ses</span><span class="sxs-lookup"><span data-stu-id="51f26-109">Members</span></span>                        | <span data-ttu-id="51f26-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="51f26-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="51f26-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="51f26-111">Invoke</span></span>](#invoke) | <span data-ttu-id="51f26-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="51f26-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="51f26-113">Ses</span><span class="sxs-lookup"><span data-stu-id="51f26-113">Members</span></span>

#### <span data-ttu-id="51f26-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="51f26-114">Invoke</span></span> 

<span data-ttu-id="51f26-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="51f26-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="51f26-116">[appel](#invoke)HRESULT public (résultat HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="51f26-116">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>

