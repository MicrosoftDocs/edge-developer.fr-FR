---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 9aa9a18701621ca78b74b12340ef5132953fbd2b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880667"
---
# <span data-ttu-id="2b304-104">0.9.515-interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2b304-104">0.9.515 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="2b304-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="2b304-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="2b304-106">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="2b304-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="2b304-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="2b304-107">Summary</span></span>

 <span data-ttu-id="2b304-108">Ses</span><span class="sxs-lookup"><span data-stu-id="2b304-108">Members</span></span>                        | <span data-ttu-id="2b304-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2b304-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2b304-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="2b304-110">Invoke</span></span>](#invoke) | <span data-ttu-id="2b304-111">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="2b304-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="2b304-112">Ses</span><span class="sxs-lookup"><span data-stu-id="2b304-112">Members</span></span>

#### <span data-ttu-id="2b304-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="2b304-113">Invoke</span></span> 

<span data-ttu-id="2b304-114">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="2b304-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="2b304-115">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="2b304-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

