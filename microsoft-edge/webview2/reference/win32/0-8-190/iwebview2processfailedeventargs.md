---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 5ceb24d0d20f580e14e0d5af7ec09881c9ab0eb2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878245"
---
# <span data-ttu-id="184c3-104">0.8.355-interface IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="184c3-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="184c3-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="184c3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="184c3-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="184c3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="184c3-107">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="184c3-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="184c3-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="184c3-108">Summary</span></span>

 <span data-ttu-id="184c3-109">Ses</span><span class="sxs-lookup"><span data-stu-id="184c3-109">Members</span></span>                        | <span data-ttu-id="184c3-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="184c3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="184c3-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="184c3-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="184c3-112">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="184c3-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="184c3-113">Ses</span><span class="sxs-lookup"><span data-stu-id="184c3-113">Members</span></span>

#### <span data-ttu-id="184c3-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="184c3-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="184c3-115">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="184c3-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="184c3-116">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="184c3-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

