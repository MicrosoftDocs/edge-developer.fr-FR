---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2NavigationCompletedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2NavigationCompletedEventHandler
ms.openlocfilehash: 7e61f54882d653a28ec31a97c59758eeff300b26
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011264"
---
# <span data-ttu-id="6b12d-104">0.9.579-interface ICoreWebView2NavigationCompletedEventHandler</span><span class="sxs-lookup"><span data-stu-id="6b12d-104">0.9.579 - interface ICoreWebView2NavigationCompletedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventHandler
  : public IUnknown
```

<span data-ttu-id="6b12d-105">L’appelant implémente cette interface pour recevoir l’événement NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="6b12d-105">The caller implements this interface to receive the NavigationCompleted event.</span></span>

## <span data-ttu-id="6b12d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6b12d-106">Summary</span></span>

 <span data-ttu-id="6b12d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6b12d-107">Members</span></span>                        | <span data-ttu-id="6b12d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6b12d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6b12d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6b12d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6b12d-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6b12d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="6b12d-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6b12d-111">Members</span></span>

#### <span data-ttu-id="6b12d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6b12d-112">Invoke</span></span> 

<span data-ttu-id="6b12d-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="6b12d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="6b12d-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="6b12d-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationCompletedEventArgs](icorewebview2navigationcompletedeventargs.md) \* args)</span></span>

