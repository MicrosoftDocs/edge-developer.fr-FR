---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 70fb6f75594284560cb0d64663fbda47cc7404d6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879344"
---
# <span data-ttu-id="b71f5-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b71f5-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="b71f5-105">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="b71f5-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="b71f5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b71f5-106">Summary</span></span>

 <span data-ttu-id="b71f5-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b71f5-107">Members</span></span>                        | <span data-ttu-id="b71f5-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b71f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b71f5-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b71f5-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="b71f5-110">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="b71f5-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="b71f5-111">Ses</span><span class="sxs-lookup"><span data-stu-id="b71f5-111">Members</span></span>

#### <span data-ttu-id="b71f5-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="b71f5-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="b71f5-113">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="b71f5-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="b71f5-114">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="b71f5-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

