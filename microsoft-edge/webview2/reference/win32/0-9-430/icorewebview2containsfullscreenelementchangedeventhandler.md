---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 497a6b19800b6bb69712b57a4e4484d3f73662c5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881164"
---
# <span data-ttu-id="1de59-104">0.9.430-interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1de59-104">0.9.430 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1de59-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="1de59-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="1de59-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="1de59-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1de59-107">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="1de59-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="1de59-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="1de59-108">Summary</span></span>

 <span data-ttu-id="1de59-109">Ses</span><span class="sxs-lookup"><span data-stu-id="1de59-109">Members</span></span>                        | <span data-ttu-id="1de59-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="1de59-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1de59-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="1de59-111">Invoke</span></span>](#invoke) | <span data-ttu-id="1de59-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="1de59-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1de59-113">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="1de59-113">There are no event args for this event.</span></span>

## <span data-ttu-id="1de59-114">Ses</span><span class="sxs-lookup"><span data-stu-id="1de59-114">Members</span></span>

#### <span data-ttu-id="1de59-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="1de59-115">Invoke</span></span> 

<span data-ttu-id="1de59-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="1de59-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1de59-117">[appel](#invoke)de HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1de59-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="1de59-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="1de59-118">There are no event args and the args parameter will be null.</span></span>

