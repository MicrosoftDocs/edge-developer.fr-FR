---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a19f8c445d7ff1f6bee24cdd8871c28d41eedebe
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886410"
---
# <span data-ttu-id="6340c-104">0.9.430-interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6340c-104">0.9.430 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="6340c-105">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="6340c-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="6340c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6340c-106">Summary</span></span>

 <span data-ttu-id="6340c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6340c-107">Members</span></span>                        | <span data-ttu-id="6340c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6340c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6340c-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="6340c-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="6340c-110">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="6340c-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="6340c-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6340c-111">Members</span></span>

#### <span data-ttu-id="6340c-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="6340c-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="6340c-113">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="6340c-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="6340c-114">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="6340c-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

