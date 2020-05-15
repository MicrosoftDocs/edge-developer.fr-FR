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
ms.openlocfilehash: a8cd4dd948aa00aca7c2ef7d8c0c744b30db37e3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653507"
---
# <span data-ttu-id="04f07-104">interface ICoreWebView2NewWindowRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="04f07-104">interface ICoreWebView2NewWindowRequestedEventHandler</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="04f07-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="04f07-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="04f07-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="04f07-106">Summary</span></span>

 <span data-ttu-id="04f07-107">Ses</span><span class="sxs-lookup"><span data-stu-id="04f07-107">Members</span></span>                        | <span data-ttu-id="04f07-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="04f07-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04f07-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="04f07-109">Invoke</span></span>](#invoke) | <span data-ttu-id="04f07-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="04f07-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="04f07-111">Ses</span><span class="sxs-lookup"><span data-stu-id="04f07-111">Members</span></span>

#### <span data-ttu-id="04f07-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="04f07-112">Invoke</span></span> 

<span data-ttu-id="04f07-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="04f07-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="04f07-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="04f07-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NewWindowRequestedEventArgs](icorewebview2newwindowrequestedeventargs.md) \* args)</span></span>

