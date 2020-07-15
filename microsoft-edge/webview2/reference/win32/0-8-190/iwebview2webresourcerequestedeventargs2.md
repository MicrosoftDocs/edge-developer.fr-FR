---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 80ea596f28d1afeb451ce20d495961ca4eed507a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878112"
---
# <span data-ttu-id="9b60e-104">0.8.355-interface IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="9b60e-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="9b60e-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="9b60e-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="9b60e-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="9b60e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="9b60e-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9b60e-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9b60e-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="9b60e-108">Summary</span></span>

 <span data-ttu-id="9b60e-109">Ses</span><span class="sxs-lookup"><span data-stu-id="9b60e-109">Members</span></span>                        | <span data-ttu-id="9b60e-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9b60e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9b60e-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9b60e-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="9b60e-112">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9b60e-112">The web resource request contexts.</span></span>

## <span data-ttu-id="9b60e-113">Ses</span><span class="sxs-lookup"><span data-stu-id="9b60e-113">Members</span></span>

#### <span data-ttu-id="9b60e-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9b60e-114">get_ResourceContext</span></span> 

<span data-ttu-id="9b60e-115">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9b60e-115">The web resource request contexts.</span></span>

> <span data-ttu-id="9b60e-116">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="9b60e-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

