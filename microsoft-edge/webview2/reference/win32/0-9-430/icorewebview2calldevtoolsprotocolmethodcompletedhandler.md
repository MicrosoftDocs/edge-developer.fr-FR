---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: d7f44614e7322759446812481c9fa05c807b5eac
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653432"
---
# <span data-ttu-id="f845b-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f845b-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f845b-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f845b-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f845b-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="f845b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f845b-107">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="f845b-107">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="f845b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f845b-108">Summary</span></span>

 <span data-ttu-id="f845b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f845b-109">Members</span></span>                        | <span data-ttu-id="f845b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f845b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f845b-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f845b-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f845b-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="f845b-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f845b-113">Ses</span><span class="sxs-lookup"><span data-stu-id="f845b-113">Members</span></span>

#### <span data-ttu-id="f845b-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f845b-114">Invoke</span></span> 

<span data-ttu-id="f845b-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="f845b-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f845b-116">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="f845b-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR returnObjectAsJson)</span></span>

