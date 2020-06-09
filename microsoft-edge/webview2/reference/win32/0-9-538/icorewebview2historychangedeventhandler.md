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
ms.openlocfilehash: 0f14f8d281d4729d797eb5271a19cff67becafab
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698689"
---
# <span data-ttu-id="9e11b-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9e11b-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="9e11b-105">L’appelant implémente cette interface pour recevoir l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="9e11b-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="9e11b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9e11b-106">Summary</span></span>

 <span data-ttu-id="9e11b-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9e11b-107">Members</span></span>                        | <span data-ttu-id="9e11b-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9e11b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e11b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9e11b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9e11b-110">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="9e11b-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="9e11b-111">Ses</span><span class="sxs-lookup"><span data-stu-id="9e11b-111">Members</span></span>

#### <span data-ttu-id="9e11b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9e11b-112">Invoke</span></span> 

<span data-ttu-id="9e11b-113">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="9e11b-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="9e11b-114">[appel](#invoke)vers un HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9e11b-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

