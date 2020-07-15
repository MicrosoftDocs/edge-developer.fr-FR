---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: cf9d04c14f39a9ba1686d5cc9b002041313b645d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879911"
---
# <span data-ttu-id="95c98-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="95c98-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="95c98-105">L’appelant implémente cette interface pour recevoir l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="95c98-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="95c98-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="95c98-106">Summary</span></span>

 <span data-ttu-id="95c98-107">Ses</span><span class="sxs-lookup"><span data-stu-id="95c98-107">Members</span></span>                        | <span data-ttu-id="95c98-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="95c98-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="95c98-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="95c98-109">Invoke</span></span>](#invoke) | <span data-ttu-id="95c98-110">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="95c98-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="95c98-111">Ses</span><span class="sxs-lookup"><span data-stu-id="95c98-111">Members</span></span>

#### <span data-ttu-id="95c98-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="95c98-112">Invoke</span></span> 

<span data-ttu-id="95c98-113">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="95c98-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="95c98-114">[appel](#invoke)vers un HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="95c98-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

