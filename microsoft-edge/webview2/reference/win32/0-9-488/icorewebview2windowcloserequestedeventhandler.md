---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9163eb811e018e346f610dae71d5fdb7e39de186
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885435"
---
# <span data-ttu-id="a2012-104">0.9.515-interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a2012-104">0.9.515 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="a2012-105">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a2012-105">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="a2012-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a2012-106">Summary</span></span>

 <span data-ttu-id="a2012-107">Ses</span><span class="sxs-lookup"><span data-stu-id="a2012-107">Members</span></span>                        | <span data-ttu-id="a2012-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a2012-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a2012-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a2012-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a2012-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="a2012-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a2012-111">Ses</span><span class="sxs-lookup"><span data-stu-id="a2012-111">Members</span></span>

#### <span data-ttu-id="a2012-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a2012-112">Invoke</span></span> 

<span data-ttu-id="a2012-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="a2012-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a2012-114">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="a2012-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="a2012-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a2012-115">There are no event args and the args parameter will be null.</span></span>

