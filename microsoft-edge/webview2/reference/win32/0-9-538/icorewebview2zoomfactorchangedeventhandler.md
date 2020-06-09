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
ms.openlocfilehash: f0b90cec451a80225f657386fa06b8740d6e1385
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698710"
---
# <span data-ttu-id="2b05e-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2b05e-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="2b05e-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="2b05e-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="2b05e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="2b05e-106">Summary</span></span>

 <span data-ttu-id="2b05e-107">Ses</span><span class="sxs-lookup"><span data-stu-id="2b05e-107">Members</span></span>                        | <span data-ttu-id="2b05e-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2b05e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2b05e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2b05e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2b05e-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2b05e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="2b05e-111">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="2b05e-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="2b05e-112">Ses</span><span class="sxs-lookup"><span data-stu-id="2b05e-112">Members</span></span>

#### <span data-ttu-id="2b05e-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="2b05e-113">Invoke</span></span> 

<span data-ttu-id="2b05e-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2b05e-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2b05e-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2b05e-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="2b05e-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="2b05e-116">There are no event args and the args parameter will be null.</span></span>

