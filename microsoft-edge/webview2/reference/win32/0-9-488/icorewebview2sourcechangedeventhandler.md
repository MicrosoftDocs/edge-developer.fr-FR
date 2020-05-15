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
ms.openlocfilehash: d808f4b112d3688b4e50a2f6b69db38bbb4808c5
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653599"
---
# <span data-ttu-id="728ca-104">interface ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="728ca-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="728ca-105">L’appelant implémente cette interface pour recevoir l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="728ca-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="728ca-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="728ca-106">Summary</span></span>

 <span data-ttu-id="728ca-107">Ses</span><span class="sxs-lookup"><span data-stu-id="728ca-107">Members</span></span>                        | <span data-ttu-id="728ca-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="728ca-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="728ca-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="728ca-109">Invoke</span></span>](#invoke) | <span data-ttu-id="728ca-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="728ca-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="728ca-111">Ses</span><span class="sxs-lookup"><span data-stu-id="728ca-111">Members</span></span>

#### <span data-ttu-id="728ca-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="728ca-112">Invoke</span></span> 

<span data-ttu-id="728ca-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="728ca-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="728ca-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="728ca-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

