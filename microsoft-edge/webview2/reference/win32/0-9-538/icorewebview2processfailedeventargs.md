---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: c01d98ca997a0b4e288ecaa8ede609c93fc84ea1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698618"
---
# <span data-ttu-id="ca154-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ca154-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="ca154-105">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="ca154-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="ca154-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ca154-106">Summary</span></span>

 <span data-ttu-id="ca154-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ca154-107">Members</span></span>                        | <span data-ttu-id="ca154-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ca154-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ca154-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="ca154-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="ca154-110">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="ca154-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="ca154-111">Ses</span><span class="sxs-lookup"><span data-stu-id="ca154-111">Members</span></span>

#### <span data-ttu-id="ca154-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="ca154-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="ca154-113">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="ca154-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="ca154-114">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="ca154-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

