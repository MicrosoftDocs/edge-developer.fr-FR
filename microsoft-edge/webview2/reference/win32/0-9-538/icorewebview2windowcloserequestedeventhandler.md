---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WindowCloseRequestedEventHandler
ms.openlocfilehash: 34b0f941029251824cdc108e0aca41e6eab93695
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011376"
---
# <span data-ttu-id="f0a75-104">0.9.579-interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f0a75-104">0.9.579 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f0a75-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f0a75-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="f0a75-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f0a75-106">Summary</span></span>

 <span data-ttu-id="f0a75-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f0a75-107">Members</span></span>                        | <span data-ttu-id="f0a75-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f0a75-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0a75-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0a75-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f0a75-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f0a75-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f0a75-111">Ses</span><span class="sxs-lookup"><span data-stu-id="f0a75-111">Members</span></span>

#### <span data-ttu-id="f0a75-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f0a75-112">Invoke</span></span> 

<span data-ttu-id="f0a75-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f0a75-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f0a75-114">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f0a75-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="f0a75-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f0a75-115">There are no event args and the args parameter will be null.</span></span>

