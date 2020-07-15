---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 715af5cbf2bbaf8301e39dce1516019102b61ab1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877328"
---
# <span data-ttu-id="32890-104">0.9.515-interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="32890-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="32890-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="32890-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="32890-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="32890-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="32890-107">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="32890-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="32890-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="32890-108">Summary</span></span>

 <span data-ttu-id="32890-109">Ses</span><span class="sxs-lookup"><span data-stu-id="32890-109">Members</span></span>                        | <span data-ttu-id="32890-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="32890-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="32890-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="32890-111">Invoke</span></span>](#invoke) | <span data-ttu-id="32890-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="32890-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="32890-113">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="32890-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="32890-114">Ses</span><span class="sxs-lookup"><span data-stu-id="32890-114">Members</span></span>

#### <span data-ttu-id="32890-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="32890-115">Invoke</span></span> 

<span data-ttu-id="32890-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="32890-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="32890-117">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="32890-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

