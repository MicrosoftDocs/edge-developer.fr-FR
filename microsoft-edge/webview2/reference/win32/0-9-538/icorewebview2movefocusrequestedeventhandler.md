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
ms.openlocfilehash: a90e7d3479f93d58d72db5c69cca53669a6d4501
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698631"
---
# <span data-ttu-id="cefd2-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="cefd2-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="cefd2-105">L’appelant implémente cette méthode pour recevoir l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="cefd2-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="cefd2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="cefd2-106">Summary</span></span>

 <span data-ttu-id="cefd2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="cefd2-107">Members</span></span>                        | <span data-ttu-id="cefd2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cefd2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cefd2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="cefd2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cefd2-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="cefd2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="cefd2-111">Ses</span><span class="sxs-lookup"><span data-stu-id="cefd2-111">Members</span></span>

#### <span data-ttu-id="cefd2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="cefd2-112">Invoke</span></span> 

<span data-ttu-id="cefd2-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="cefd2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="cefd2-114">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="cefd2-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

