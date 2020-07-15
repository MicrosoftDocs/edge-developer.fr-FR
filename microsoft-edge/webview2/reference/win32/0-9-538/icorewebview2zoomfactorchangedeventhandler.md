---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ZoomFactorChangedEventHandler
ms.openlocfilehash: 74cd0451e111780078714b17e5bd1097c56d6b2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877573"
---
# <span data-ttu-id="875f5-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="875f5-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="875f5-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="875f5-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="875f5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="875f5-106">Summary</span></span>

 <span data-ttu-id="875f5-107">Ses</span><span class="sxs-lookup"><span data-stu-id="875f5-107">Members</span></span>                        | <span data-ttu-id="875f5-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="875f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="875f5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="875f5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="875f5-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="875f5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="875f5-111">Utilisez la propriété ICoreWebView2Controller. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="875f5-111">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="875f5-112">Ses</span><span class="sxs-lookup"><span data-stu-id="875f5-112">Members</span></span>

#### <span data-ttu-id="875f5-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="875f5-113">Invoke</span></span> 

<span data-ttu-id="875f5-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="875f5-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="875f5-115">[appel](#invoke)de HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="875f5-115">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="875f5-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="875f5-116">There are no event args and the args parameter will be null.</span></span>

