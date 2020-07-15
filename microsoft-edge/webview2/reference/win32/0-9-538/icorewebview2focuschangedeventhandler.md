---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2FocusChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2FocusChangedEventHandler
ms.openlocfilehash: fc952437a9d5ffa7bb709bb6fb322438851babcd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879897"
---
# <span data-ttu-id="e5e3d-104">interface ICoreWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e5e3d-104">interface ICoreWebView2FocusChangedEventHandler</span></span> 

```
interface ICoreWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e5e3d-105">L’appelant implémente cette méthode pour recevoir les événements GotFocus et LostFocus.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-105">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="e5e3d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e5e3d-106">Summary</span></span>

 <span data-ttu-id="e5e3d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e5e3d-107">Members</span></span>                        | <span data-ttu-id="e5e3d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e5e3d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5e3d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5e3d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e5e3d-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e5e3d-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-111">There are no event args for this event.</span></span>

## <span data-ttu-id="e5e3d-112">Ses</span><span class="sxs-lookup"><span data-stu-id="e5e3d-112">Members</span></span>

#### <span data-ttu-id="e5e3d-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="e5e3d-113">Invoke</span></span> 

<span data-ttu-id="e5e3d-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e5e3d-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e5e3d-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="e5e3d-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="e5e3d-116">There are no event args and the args parameter will be null.</span></span>

