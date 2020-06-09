---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: df43e9cb1d036482a73e1ff92446a5a74b921d5d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698154"
---
# <span data-ttu-id="10bed-104">interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="10bed-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="10bed-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="10bed-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="10bed-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="10bed-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="10bed-107">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="10bed-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="10bed-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="10bed-108">Summary</span></span>

 <span data-ttu-id="10bed-109">Ses</span><span class="sxs-lookup"><span data-stu-id="10bed-109">Members</span></span>                        | <span data-ttu-id="10bed-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="10bed-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10bed-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="10bed-111">Invoke</span></span>](#invoke) | <span data-ttu-id="10bed-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="10bed-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="10bed-113">Ses</span><span class="sxs-lookup"><span data-stu-id="10bed-113">Members</span></span>

#### <span data-ttu-id="10bed-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="10bed-114">Invoke</span></span> 

<span data-ttu-id="10bed-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="10bed-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="10bed-116">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="10bed-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

