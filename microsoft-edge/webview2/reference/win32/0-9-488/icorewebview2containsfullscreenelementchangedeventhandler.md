---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 41687dcb162d8d56e773b9050898e9f22bd034ab
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883881"
---
# <span data-ttu-id="3bcff-104">0.9.515-interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3bcff-104">0.9.515 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="3bcff-105">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="3bcff-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="3bcff-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3bcff-106">Summary</span></span>

 <span data-ttu-id="3bcff-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3bcff-107">Members</span></span>                        | <span data-ttu-id="3bcff-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3bcff-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3bcff-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3bcff-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3bcff-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3bcff-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="3bcff-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="3bcff-111">There are no event args for this event.</span></span>

## <span data-ttu-id="3bcff-112">Ses</span><span class="sxs-lookup"><span data-stu-id="3bcff-112">Members</span></span>

#### <span data-ttu-id="3bcff-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="3bcff-113">Invoke</span></span> 

<span data-ttu-id="3bcff-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3bcff-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3bcff-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="3bcff-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="3bcff-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="3bcff-116">There are no event args and the args parameter will be null.</span></span>

