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
ms.openlocfilehash: 9a1f86bbc3f07b67cccb3c5c47fe7032bd13844e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653657"
---
# <span data-ttu-id="533a1-104">interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="533a1-104">interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="533a1-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="533a1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="533a1-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="533a1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="533a1-107">L’appelant implémente cette interface pour recevoir l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="533a1-107">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="533a1-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="533a1-108">Summary</span></span>

 <span data-ttu-id="533a1-109">Ses</span><span class="sxs-lookup"><span data-stu-id="533a1-109">Members</span></span>                        | <span data-ttu-id="533a1-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="533a1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="533a1-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="533a1-111">Invoke</span></span>](#invoke) | <span data-ttu-id="533a1-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="533a1-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="533a1-113">Ses</span><span class="sxs-lookup"><span data-stu-id="533a1-113">Members</span></span>

#### <span data-ttu-id="533a1-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="533a1-114">Invoke</span></span> 

<span data-ttu-id="533a1-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="533a1-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="533a1-116">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="533a1-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2NavigationCompletedEventArgs](ICoreWebView2NavigationCompletedEventArgs.md) \* args)</span></span>

