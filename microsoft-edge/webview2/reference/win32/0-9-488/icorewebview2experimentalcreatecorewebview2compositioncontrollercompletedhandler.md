---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: f2598d40afc7c7def1c3fec634016f1a64905479
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885666"
---
# <span data-ttu-id="1e3e8-104">0.9.515-interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="1e3e8-104">0.9.515 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="1e3e8-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="1e3e8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="1e3e8-106">Summary</span></span>

 <span data-ttu-id="1e3e8-107">Ses</span><span class="sxs-lookup"><span data-stu-id="1e3e8-107">Members</span></span>                        | <span data-ttu-id="1e3e8-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="1e3e8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1e3e8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e3e8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1e3e8-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="1e3e8-111">Ses</span><span class="sxs-lookup"><span data-stu-id="1e3e8-111">Members</span></span>

#### <span data-ttu-id="1e3e8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="1e3e8-112">Invoke</span></span> 

<span data-ttu-id="1e3e8-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="1e3e8-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="1e3e8-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="1e3e8-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

