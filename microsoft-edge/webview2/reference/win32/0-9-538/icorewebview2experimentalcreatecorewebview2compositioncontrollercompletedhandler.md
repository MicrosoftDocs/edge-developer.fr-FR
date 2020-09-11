---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
ms.openlocfilehash: 8fc3efa6bf1ba9a9e721dcba67e8350ded38cc62
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011134"
---
# <span data-ttu-id="b9806-104">0.9.579-interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b9806-104">0.9.579 - interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b9806-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="b9806-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="b9806-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b9806-106">Summary</span></span>

 <span data-ttu-id="b9806-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b9806-107">Members</span></span>                        | <span data-ttu-id="b9806-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b9806-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9806-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9806-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b9806-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b9806-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b9806-111">Ses</span><span class="sxs-lookup"><span data-stu-id="b9806-111">Members</span></span>

#### <span data-ttu-id="b9806-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9806-112">Invoke</span></span> 

<span data-ttu-id="b9806-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b9806-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b9806-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="b9806-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

