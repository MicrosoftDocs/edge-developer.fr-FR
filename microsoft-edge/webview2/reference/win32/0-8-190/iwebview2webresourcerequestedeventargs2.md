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
ms.openlocfilehash: c23e6bcd18e3b0fe7d2ee9b279e65fc81fe89d3d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653314"
---
# <span data-ttu-id="56429-104">interface IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="56429-104">interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="56429-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="56429-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="56429-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="56429-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="56429-107">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="56429-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="56429-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="56429-108">Summary</span></span>

 <span data-ttu-id="56429-109">Ses</span><span class="sxs-lookup"><span data-stu-id="56429-109">Members</span></span>                        | <span data-ttu-id="56429-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="56429-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56429-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="56429-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="56429-112">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="56429-112">The web resource request contexts.</span></span>

## <span data-ttu-id="56429-113">Ses</span><span class="sxs-lookup"><span data-stu-id="56429-113">Members</span></span>

#### <span data-ttu-id="56429-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="56429-114">get_ResourceContext</span></span> 

<span data-ttu-id="56429-115">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="56429-115">The web resource request contexts.</span></span>

> <span data-ttu-id="56429-116">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="56429-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

