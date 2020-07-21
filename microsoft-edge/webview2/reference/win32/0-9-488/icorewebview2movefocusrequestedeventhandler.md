---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 45f9b638347d096ce89c9fcaac1bfb7e904ebee9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886296"
---
# <span data-ttu-id="e57ae-104">0.9.515-interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e57ae-104">0.9.515 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e57ae-105">L’appelant implémente cette méthode pour recevoir l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="e57ae-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="e57ae-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e57ae-106">Summary</span></span>

 <span data-ttu-id="e57ae-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e57ae-107">Members</span></span>                        | <span data-ttu-id="e57ae-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e57ae-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e57ae-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e57ae-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e57ae-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e57ae-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="e57ae-111">Ses</span><span class="sxs-lookup"><span data-stu-id="e57ae-111">Members</span></span>

#### <span data-ttu-id="e57ae-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e57ae-112">Invoke</span></span> 

<span data-ttu-id="e57ae-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e57ae-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e57ae-114">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e57ae-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

