---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: f4238f0d75f39727260296703e84740ca77b30d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877736"
---
# <span data-ttu-id="c2e49-104">0.9.430-interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c2e49-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c2e49-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c2e49-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c2e49-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="c2e49-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="c2e49-107">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="c2e49-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="c2e49-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c2e49-108">Summary</span></span>

 <span data-ttu-id="c2e49-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c2e49-109">Members</span></span>                        | <span data-ttu-id="c2e49-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c2e49-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c2e49-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="c2e49-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="c2e49-112">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="c2e49-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="c2e49-113">Ses</span><span class="sxs-lookup"><span data-stu-id="c2e49-113">Members</span></span>

#### <span data-ttu-id="c2e49-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="c2e49-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="c2e49-115">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="c2e49-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="c2e49-116">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="c2e49-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

