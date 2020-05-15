---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 62daeaab702b431f787bc800ab79664fc183c4ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653252"
---
# <span data-ttu-id="6f635-104">interface IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="6f635-104">interface IWebView2WebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="6f635-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="6f635-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="6f635-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="6f635-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="6f635-107">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="6f635-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="6f635-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6f635-108">Summary</span></span>

 <span data-ttu-id="6f635-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6f635-109">Members</span></span>                        | <span data-ttu-id="6f635-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6f635-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6f635-111">Stop</span><span class="sxs-lookup"><span data-stu-id="6f635-111">Stop</span></span>](#stop) | <span data-ttu-id="6f635-112">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="6f635-112">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="6f635-113">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="6f635-113">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="6f635-114">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="6f635-114">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="6f635-115">Ses</span><span class="sxs-lookup"><span data-stu-id="6f635-115">Members</span></span>

#### <span data-ttu-id="6f635-116">Stop</span><span class="sxs-lookup"><span data-stu-id="6f635-116">Stop</span></span> 

<span data-ttu-id="6f635-117">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="6f635-117">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="6f635-118">point d' [arrêt](#stop)public HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="6f635-118">public HRESULT [Stop](#stop)()</span></span>

