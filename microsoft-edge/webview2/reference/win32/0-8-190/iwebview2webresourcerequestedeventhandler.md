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
ms.openlocfilehash: 602c00258e9ff3362269ebe90de8306ecbd7503e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653313"
---
# <span data-ttu-id="db3a7-104">interface IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="db3a7-104">interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="db3a7-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="db3a7-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="db3a7-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="db3a7-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="db3a7-107">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="db3a7-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="db3a7-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="db3a7-108">Summary</span></span>

 <span data-ttu-id="db3a7-109">Ses</span><span class="sxs-lookup"><span data-stu-id="db3a7-109">Members</span></span>                        | <span data-ttu-id="db3a7-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="db3a7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="db3a7-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="db3a7-111">Invoke</span></span>](#invoke) | <span data-ttu-id="db3a7-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="db3a7-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="db3a7-113">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="db3a7-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="db3a7-114">Ses</span><span class="sxs-lookup"><span data-stu-id="db3a7-114">Members</span></span>

#### <span data-ttu-id="db3a7-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="db3a7-115">Invoke</span></span> 

<span data-ttu-id="db3a7-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="db3a7-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="db3a7-117">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="db3a7-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

