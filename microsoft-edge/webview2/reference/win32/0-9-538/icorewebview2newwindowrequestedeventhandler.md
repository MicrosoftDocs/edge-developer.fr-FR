---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a39eeadaf1243d57223f3739dce836b1db998998
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698587"
---
# <span data-ttu-id="a9278-104">interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a9278-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="a9278-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a9278-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="a9278-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a9278-106">Summary</span></span>

 <span data-ttu-id="a9278-107">Ses</span><span class="sxs-lookup"><span data-stu-id="a9278-107">Members</span></span>                        | <span data-ttu-id="a9278-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a9278-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a9278-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a9278-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a9278-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="a9278-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a9278-111">Ses</span><span class="sxs-lookup"><span data-stu-id="a9278-111">Members</span></span>

#### <span data-ttu-id="a9278-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a9278-112">Invoke</span></span> 

<span data-ttu-id="a9278-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="a9278-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a9278-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a9278-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

