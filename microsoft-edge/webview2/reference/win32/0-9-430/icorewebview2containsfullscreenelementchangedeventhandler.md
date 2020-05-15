---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 7c5aece49cf2a3e8e6a65eba3fbb4d46f0ff2997
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653430"
---
# <span data-ttu-id="4eab1-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4eab1-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4eab1-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4eab1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4eab1-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="4eab1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="4eab1-107">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="4eab1-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="4eab1-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4eab1-108">Summary</span></span>

 <span data-ttu-id="4eab1-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4eab1-109">Members</span></span>                        | <span data-ttu-id="4eab1-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4eab1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4eab1-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="4eab1-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4eab1-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4eab1-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4eab1-113">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="4eab1-113">There are no event args for this event.</span></span>

## <span data-ttu-id="4eab1-114">Ses</span><span class="sxs-lookup"><span data-stu-id="4eab1-114">Members</span></span>

#### <span data-ttu-id="4eab1-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="4eab1-115">Invoke</span></span> 

<span data-ttu-id="4eab1-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4eab1-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4eab1-117">[appel](#invoke)de HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4eab1-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="4eab1-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="4eab1-118">There are no event args and the args parameter will be null.</span></span>

