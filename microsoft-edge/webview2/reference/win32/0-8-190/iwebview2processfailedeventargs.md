---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 697a49bfe68f83085f6c961ee2cdd5ab21f3b59b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885820"
---
# <span data-ttu-id="aade2-104">0.8.355-interface IWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aade2-104">0.8.355 - interface IWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="aade2-105">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="aade2-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="aade2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="aade2-106">Summary</span></span>

 <span data-ttu-id="aade2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="aade2-107">Members</span></span>                        | <span data-ttu-id="aade2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="aade2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aade2-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="aade2-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="aade2-110">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="aade2-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="aade2-111">Ses</span><span class="sxs-lookup"><span data-stu-id="aade2-111">Members</span></span>

#### <span data-ttu-id="aade2-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="aade2-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="aade2-113">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="aade2-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="aade2-114">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="aade2-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

