---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: 0477f9868dc472cab71dad4b10ff85fa034515a1
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011998"
---
# <span data-ttu-id="f8e54-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f8e54-104">interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f8e54-105">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="f8e54-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="f8e54-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f8e54-106">Summary</span></span>

 <span data-ttu-id="f8e54-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f8e54-107">Members</span></span>                        | <span data-ttu-id="f8e54-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f8e54-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8e54-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8e54-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f8e54-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f8e54-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="f8e54-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="f8e54-111">There are no event args for this event.</span></span>

## <span data-ttu-id="f8e54-112">Ses</span><span class="sxs-lookup"><span data-stu-id="f8e54-112">Members</span></span>

#### <span data-ttu-id="f8e54-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="f8e54-113">Invoke</span></span> 

<span data-ttu-id="f8e54-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f8e54-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f8e54-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f8e54-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f8e54-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f8e54-116">There are no event args and the args parameter will be null.</span></span>

