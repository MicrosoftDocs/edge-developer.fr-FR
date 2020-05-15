---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 8fba2759ce0e264dcde515ee1191ec819f26eef9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653476"
---
# <span data-ttu-id="05ab6-104">interface ICoreWebView2ProcessFailedEventArgs</span><span class="sxs-lookup"><span data-stu-id="05ab6-104">interface ICoreWebView2ProcessFailedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="05ab6-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="05ab6-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="05ab6-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="05ab6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

<span data-ttu-id="05ab6-107">Arguments d’événement pour l’événement ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="05ab6-107">Event args for the ProcessFailed event.</span></span>

## <span data-ttu-id="05ab6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="05ab6-108">Summary</span></span>

 <span data-ttu-id="05ab6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="05ab6-109">Members</span></span>                        | <span data-ttu-id="05ab6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="05ab6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="05ab6-111">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="05ab6-111">get_ProcessFailedKind</span></span>](#get_processfailedkind) | <span data-ttu-id="05ab6-112">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="05ab6-112">The kind of process failure that has occurred.</span></span>

## <span data-ttu-id="05ab6-113">Ses</span><span class="sxs-lookup"><span data-stu-id="05ab6-113">Members</span></span>

#### <span data-ttu-id="05ab6-114">get_ProcessFailedKind</span><span class="sxs-lookup"><span data-stu-id="05ab6-114">get_ProcessFailedKind</span></span> 

<span data-ttu-id="05ab6-115">Type d’échec du processus qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="05ab6-115">The kind of process failure that has occurred.</span></span>

> <span data-ttu-id="05ab6-116">[get_ProcessFailedKind](#get_processfailedkind)par le biais du public HRESULT (CORE_WEBVIEW2_PROCESS_FAILED_KIND \* ProcessFailedKind)</span><span class="sxs-lookup"><span data-stu-id="05ab6-116">public HRESULT [get_ProcessFailedKind](#get_processfailedkind)(CORE_WEBVIEW2_PROCESS_FAILED_KIND \* processFailedKind)</span></span>

