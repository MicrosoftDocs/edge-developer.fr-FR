---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: e2469dd9a587735efcf88a48e0ce950cb4f85239
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653548"
---
# <span data-ttu-id="c0489-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c0489-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c0489-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="c0489-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="c0489-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="c0489-106">Summary</span></span>

 <span data-ttu-id="c0489-107">Ses</span><span class="sxs-lookup"><span data-stu-id="c0489-107">Members</span></span>                        | <span data-ttu-id="c0489-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c0489-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0489-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c0489-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c0489-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c0489-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c0489-111">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="c0489-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="c0489-112">Ses</span><span class="sxs-lookup"><span data-stu-id="c0489-112">Members</span></span>

#### <span data-ttu-id="c0489-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="c0489-113">Invoke</span></span> 

<span data-ttu-id="c0489-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c0489-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c0489-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c0489-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c0489-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="c0489-116">There are no event args and the args parameter will be null.</span></span>

