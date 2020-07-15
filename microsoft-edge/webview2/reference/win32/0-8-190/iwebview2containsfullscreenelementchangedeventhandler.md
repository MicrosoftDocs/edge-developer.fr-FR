---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 70e9ad7782fe495ffd366664ecb132edd0c57df5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878651"
---
# <span data-ttu-id="d4805-104">0.8.355-interface IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d4805-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="d4805-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d4805-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d4805-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="d4805-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d4805-107">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="d4805-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="d4805-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d4805-108">Summary</span></span>

 <span data-ttu-id="d4805-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d4805-109">Members</span></span>                        | <span data-ttu-id="d4805-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d4805-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d4805-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="d4805-111">Invoke</span></span>](#invoke) | <span data-ttu-id="d4805-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d4805-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d4805-113">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="d4805-113">There are no event args for this event.</span></span>

## <span data-ttu-id="d4805-114">Ses</span><span class="sxs-lookup"><span data-stu-id="d4805-114">Members</span></span>

#### <span data-ttu-id="d4805-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="d4805-115">Invoke</span></span> 

<span data-ttu-id="d4805-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d4805-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d4805-117">[appel](#invoke)vers un HRESULT public ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d4805-117">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="d4805-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="d4805-118">There are no event args and the args parameter will be null.</span></span>

