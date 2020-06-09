---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 4183f3a1c60bd9e2bdcff5227426db1f07c313cf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697517"
---
# <span data-ttu-id="f7a68-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f7a68-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="f7a68-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f7a68-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f7a68-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="f7a68-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="f7a68-107">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="f7a68-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="f7a68-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f7a68-108">Summary</span></span>

 <span data-ttu-id="f7a68-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f7a68-109">Members</span></span>                        | <span data-ttu-id="f7a68-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f7a68-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f7a68-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="f7a68-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="f7a68-112">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="f7a68-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="f7a68-113">Ses</span><span class="sxs-lookup"><span data-stu-id="f7a68-113">Members</span></span>

#### <span data-ttu-id="f7a68-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="f7a68-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="f7a68-115">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="f7a68-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="f7a68-116">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="f7a68-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

