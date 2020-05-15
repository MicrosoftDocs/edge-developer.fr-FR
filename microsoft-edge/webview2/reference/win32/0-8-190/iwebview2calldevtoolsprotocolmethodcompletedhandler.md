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
ms.openlocfilehash: 826bca5300957e9e135abb74cf591245b78b4644
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653631"
---
# <span data-ttu-id="3e1c6-104">interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="3e1c6-104">interface IWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3e1c6-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3e1c6-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3e1c6-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="3e1c6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="3e1c6-107">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="3e1c6-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="3e1c6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3e1c6-108">Summary</span></span>

 <span data-ttu-id="3e1c6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3e1c6-109">Members</span></span>                        | <span data-ttu-id="3e1c6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3e1c6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3e1c6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="3e1c6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3e1c6-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="3e1c6-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="3e1c6-113">Ses</span><span class="sxs-lookup"><span data-stu-id="3e1c6-113">Members</span></span>

#### <span data-ttu-id="3e1c6-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="3e1c6-114">Invoke</span></span> 

<span data-ttu-id="3e1c6-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="3e1c6-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="3e1c6-116">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="3e1c6-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>

