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
ms.openlocfilehash: 0efc1656b8204b9775002db49e0e4a5734682cc4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653269"
---
# <span data-ttu-id="ea28b-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ea28b-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="ea28b-105">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="ea28b-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="ea28b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ea28b-106">Summary</span></span>

 <span data-ttu-id="ea28b-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ea28b-107">Members</span></span>                        | <span data-ttu-id="ea28b-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ea28b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea28b-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="ea28b-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="ea28b-110">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="ea28b-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="ea28b-111">Ses</span><span class="sxs-lookup"><span data-stu-id="ea28b-111">Members</span></span>

#### <span data-ttu-id="ea28b-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="ea28b-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="ea28b-113">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="ea28b-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="ea28b-114">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="ea28b-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

