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
ms.openlocfilehash: 8c717bb57a5dc984d6cb2bbbbac79cf91d64fe2f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698663"
---
# <span data-ttu-id="d0ec1-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="d0ec1-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="d0ec1-105">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="d0ec1-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="d0ec1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d0ec1-106">Summary</span></span>

 <span data-ttu-id="d0ec1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d0ec1-107">Members</span></span>                        | <span data-ttu-id="d0ec1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d0ec1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d0ec1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d0ec1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d0ec1-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d0ec1-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="d0ec1-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="d0ec1-111">There are no event args for this event.</span></span>

## <span data-ttu-id="d0ec1-112">Ses</span><span class="sxs-lookup"><span data-stu-id="d0ec1-112">Members</span></span>

#### <span data-ttu-id="d0ec1-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="d0ec1-113">Invoke</span></span> 

<span data-ttu-id="d0ec1-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d0ec1-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d0ec1-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="d0ec1-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="d0ec1-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="d0ec1-116">There are no event args and the args parameter will be null.</span></span>

