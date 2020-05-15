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
ms.openlocfilehash: 748c4affa73001270e2cf97b3d19db8c8ed23686
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653645"
---
# <span data-ttu-id="af958-104">interface IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="af958-104">interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="af958-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="af958-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="af958-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="af958-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="af958-107">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="af958-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="af958-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="af958-108">Summary</span></span>

 <span data-ttu-id="af958-109">Ses</span><span class="sxs-lookup"><span data-stu-id="af958-109">Members</span></span>                        | <span data-ttu-id="af958-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="af958-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af958-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="af958-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="af958-112">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="af958-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="af958-113">Ses</span><span class="sxs-lookup"><span data-stu-id="af958-113">Members</span></span>

#### <span data-ttu-id="af958-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="af958-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="af958-115">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="af958-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="af958-116">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="af958-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

