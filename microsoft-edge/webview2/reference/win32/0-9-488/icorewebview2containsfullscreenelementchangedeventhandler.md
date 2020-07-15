---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: ff5cedad802f0f367e694ddf5c62290276fa4aa4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880919"
---
# <span data-ttu-id="243eb-104">0.9.515-interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="243eb-104">0.9.515 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="243eb-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="243eb-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="243eb-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="243eb-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="243eb-107">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="243eb-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="243eb-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="243eb-108">Summary</span></span>

 <span data-ttu-id="243eb-109">Ses</span><span class="sxs-lookup"><span data-stu-id="243eb-109">Members</span></span>                        | <span data-ttu-id="243eb-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="243eb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="243eb-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="243eb-111">Invoke</span></span>](#invoke) | <span data-ttu-id="243eb-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="243eb-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="243eb-113">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="243eb-113">There are no event args for this event.</span></span>

## <span data-ttu-id="243eb-114">Ses</span><span class="sxs-lookup"><span data-stu-id="243eb-114">Members</span></span>

#### <span data-ttu-id="243eb-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="243eb-115">Invoke</span></span> 

<span data-ttu-id="243eb-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="243eb-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="243eb-117">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="243eb-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="243eb-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="243eb-118">There are no event args and the args parameter will be null.</span></span>

