---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2SourceChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2SourceChangedEventHandler
ms.openlocfilehash: b856211b8a4b4088acc741d4d5626b49340124d1
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879330"
---
# <span data-ttu-id="6be21-104">interface ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6be21-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="6be21-105">L’appelant implémente cette interface pour recevoir l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="6be21-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="6be21-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6be21-106">Summary</span></span>

 <span data-ttu-id="6be21-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6be21-107">Members</span></span>                        | <span data-ttu-id="6be21-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6be21-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6be21-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6be21-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6be21-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6be21-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6be21-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6be21-111">Members</span></span>

#### <span data-ttu-id="6be21-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6be21-112">Invoke</span></span> 

<span data-ttu-id="6be21-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6be21-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6be21-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6be21-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

