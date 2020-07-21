---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: e47ca26475ba1b59fa4ea8c87a7aada0d8d6695f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884133"
---
# <span data-ttu-id="238ec-104">0.9.430-interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="238ec-104">0.9.430 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="238ec-105">L’appelant implémente cette interface pour recevoir l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="238ec-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="238ec-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="238ec-106">Summary</span></span>

 <span data-ttu-id="238ec-107">Ses</span><span class="sxs-lookup"><span data-stu-id="238ec-107">Members</span></span>                        | <span data-ttu-id="238ec-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="238ec-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="238ec-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="238ec-109">Invoke</span></span>](#invoke) | <span data-ttu-id="238ec-110">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="238ec-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="238ec-111">Ses</span><span class="sxs-lookup"><span data-stu-id="238ec-111">Members</span></span>

#### <span data-ttu-id="238ec-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="238ec-112">Invoke</span></span> 

<span data-ttu-id="238ec-113">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="238ec-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="238ec-114">[appel](#invoke)vers un HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="238ec-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>

