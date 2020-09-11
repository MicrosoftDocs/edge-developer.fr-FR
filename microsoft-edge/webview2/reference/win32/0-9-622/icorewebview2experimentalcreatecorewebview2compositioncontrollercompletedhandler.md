---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: fd762c994d4c42e5e92dec09add2aa3b85b0ec80
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011875"
---
# <span data-ttu-id="6c82e-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6c82e-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6c82e-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="6c82e-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="6c82e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6c82e-106">Summary</span></span>

 <span data-ttu-id="6c82e-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6c82e-107">Members</span></span>                        | <span data-ttu-id="6c82e-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6c82e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c82e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6c82e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6c82e-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="6c82e-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6c82e-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6c82e-111">Members</span></span>

#### <span data-ttu-id="6c82e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6c82e-112">Invoke</span></span> 

<span data-ttu-id="6c82e-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="6c82e-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6c82e-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="6c82e-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

