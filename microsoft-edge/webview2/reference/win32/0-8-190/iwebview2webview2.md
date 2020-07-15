---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 52218ddcbecdaf3bdb736af877493c85d4460c10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878042"
---
# <span data-ttu-id="9f6a9-104">0.8.355-interface IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="9f6a9-104">0.8.355 - interface IWebView2WebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="9f6a9-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="9f6a9-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="9f6a9-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="9f6a9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="9f6a9-107">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="9f6a9-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="9f6a9-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="9f6a9-108">Summary</span></span>

 <span data-ttu-id="9f6a9-109">Ses</span><span class="sxs-lookup"><span data-stu-id="9f6a9-109">Members</span></span>                        | <span data-ttu-id="9f6a9-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9f6a9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9f6a9-111">Stop</span><span class="sxs-lookup"><span data-stu-id="9f6a9-111">Stop</span></span>](#stop) | <span data-ttu-id="9f6a9-112">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="9f6a9-112">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="9f6a9-113">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="9f6a9-113">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="9f6a9-114">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="9f6a9-114">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="9f6a9-115">Ses</span><span class="sxs-lookup"><span data-stu-id="9f6a9-115">Members</span></span>

#### <span data-ttu-id="9f6a9-116">Stop</span><span class="sxs-lookup"><span data-stu-id="9f6a9-116">Stop</span></span> 

<span data-ttu-id="9f6a9-117">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="9f6a9-117">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="9f6a9-118">point d' [arrêt](#stop)public HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="9f6a9-118">public HRESULT [Stop](#stop)()</span></span>

