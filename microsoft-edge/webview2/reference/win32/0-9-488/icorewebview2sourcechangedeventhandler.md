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
ms.openlocfilehash: 9135ba6bce6b5260413f47531062ea4c96d196cc
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698133"
---
# <span data-ttu-id="3d721-104">interface ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3d721-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3d721-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3d721-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3d721-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="3d721-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3d721-107">L’appelant implémente cette interface pour recevoir l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="3d721-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="3d721-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3d721-108">Summary</span></span>

 <span data-ttu-id="3d721-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3d721-109">Members</span></span>                        | <span data-ttu-id="3d721-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3d721-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d721-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d721-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3d721-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3d721-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3d721-113">Ses</span><span class="sxs-lookup"><span data-stu-id="3d721-113">Members</span></span>

#### <span data-ttu-id="3d721-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d721-114">Invoke</span></span> 

<span data-ttu-id="3d721-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3d721-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3d721-116">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3d721-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

