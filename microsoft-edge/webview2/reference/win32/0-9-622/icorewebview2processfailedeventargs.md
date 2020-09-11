---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 0f4ce5d4922b7a721ce2652fadfa5169a52cb458
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011945"
---
# <span data-ttu-id="8ac52-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8ac52-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="8ac52-105">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="8ac52-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="8ac52-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8ac52-106">Summary</span></span>

 <span data-ttu-id="8ac52-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8ac52-107">Members</span></span>                        | <span data-ttu-id="8ac52-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8ac52-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8ac52-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="8ac52-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="8ac52-110">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="8ac52-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="8ac52-111">Ses</span><span class="sxs-lookup"><span data-stu-id="8ac52-111">Members</span></span>

#### <span data-ttu-id="8ac52-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="8ac52-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="8ac52-113">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="8ac52-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="8ac52-114">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="8ac52-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

