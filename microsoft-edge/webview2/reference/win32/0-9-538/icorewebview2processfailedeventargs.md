---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: af27c39b2ed9ba197ab1c567bcf18a43c3dee932
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010018"
---
# <span data-ttu-id="88a9c-104">0.9.579-interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="88a9c-104">0.9.579 - interface ICoreWebView2ProcessFailedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="88a9c-105">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="88a9c-105">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="88a9c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="88a9c-106">Summary</span></span>

 <span data-ttu-id="88a9c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="88a9c-107">Members</span></span>                        | <span data-ttu-id="88a9c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="88a9c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="88a9c-109">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="88a9c-109">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="88a9c-110">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="88a9c-110">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="88a9c-111">Ses</span><span class="sxs-lookup"><span data-stu-id="88a9c-111">Members</span></span>

#### <span data-ttu-id="88a9c-112">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="88a9c-112">get_ProcessFailedKind</span></span> 

<span data-ttu-id="88a9c-113">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="88a9c-113">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="88a9c-114">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (COREWEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="88a9c-114">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

