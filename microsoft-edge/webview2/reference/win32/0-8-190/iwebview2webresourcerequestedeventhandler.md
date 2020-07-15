---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: c0980f26ef06497cded81e2f9c7c00162af18d9b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878091"
---
# <span data-ttu-id="4a516-104">0.8.355-interface IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4a516-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4a516-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="4a516-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="4a516-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="4a516-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4a516-107">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="4a516-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="4a516-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4a516-108">Summary</span></span>

 <span data-ttu-id="4a516-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4a516-109">Members</span></span>                        | <span data-ttu-id="4a516-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4a516-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4a516-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="4a516-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4a516-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4a516-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4a516-113">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="4a516-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="4a516-114">Ses</span><span class="sxs-lookup"><span data-stu-id="4a516-114">Members</span></span>

#### <span data-ttu-id="4a516-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="4a516-115">Invoke</span></span> 

<span data-ttu-id="4a516-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4a516-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4a516-117">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4a516-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

