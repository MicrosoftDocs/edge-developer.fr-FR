---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NewWindowRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2623dad17d8e8b34348bdb21a38e900c28eaeebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885442"
---
# <span data-ttu-id="4edfb-104">0.9.515-interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4edfb-104">0.9.515 - interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4edfb-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4edfb-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="4edfb-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="4edfb-106">Summary</span></span>

 <span data-ttu-id="4edfb-107">Ses</span><span class="sxs-lookup"><span data-stu-id="4edfb-107">Members</span></span>                        | <span data-ttu-id="4edfb-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4edfb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4edfb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4edfb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4edfb-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4edfb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4edfb-111">Ses</span><span class="sxs-lookup"><span data-stu-id="4edfb-111">Members</span></span>

#### <span data-ttu-id="4edfb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="4edfb-112">Invoke</span></span> 

<span data-ttu-id="4edfb-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4edfb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4edfb-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4edfb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

