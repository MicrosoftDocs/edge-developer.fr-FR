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
ms.openlocfilehash: 91c4e7885526def5de6fd1910a4a6f06c6a6953a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653350"
---
# <span data-ttu-id="44ddd-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="44ddd-104">interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="44ddd-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="44ddd-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="44ddd-106">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2CompositionController.</span><span class="sxs-lookup"><span data-stu-id="44ddd-106">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2CompositionController.</span></span>

## <span data-ttu-id="44ddd-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="44ddd-107">Summary</span></span>

 <span data-ttu-id="44ddd-108">Ses</span><span class="sxs-lookup"><span data-stu-id="44ddd-108">Members</span></span>                        | <span data-ttu-id="44ddd-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="44ddd-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="44ddd-110">Invoke</span><span class="sxs-lookup"><span data-stu-id="44ddd-110">Invoke</span></span>](#invoke) | <span data-ttu-id="44ddd-111">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="44ddd-111">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="44ddd-112">Ses</span><span class="sxs-lookup"><span data-stu-id="44ddd-112">Members</span></span>

#### <span data-ttu-id="44ddd-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="44ddd-113">Invoke</span></span> 

<span data-ttu-id="44ddd-114">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="44ddd-114">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="44ddd-115">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* WebView)</span><span class="sxs-lookup"><span data-stu-id="44ddd-115">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) \* webView)</span></span>

