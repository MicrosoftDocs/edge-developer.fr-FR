---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2CreateWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 9937fe08f440ce468f178e4ac17935bbb8a1a8ed
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886170"
---
# <span data-ttu-id="d9d76-104">0.8.355-interface IWebView2CreateWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="d9d76-104">0.8.355 - interface IWebView2CreateWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="d9d76-105">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="d9d76-105">The caller implements this interface to receive the WebView2Environment created via CreateWebView2Environment.</span></span>

## <span data-ttu-id="d9d76-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d9d76-106">Summary</span></span>

 <span data-ttu-id="d9d76-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d9d76-107">Members</span></span>                        | <span data-ttu-id="d9d76-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d9d76-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9d76-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9d76-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d9d76-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="d9d76-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="d9d76-111">Ses</span><span class="sxs-lookup"><span data-stu-id="d9d76-111">Members</span></span>

#### <span data-ttu-id="d9d76-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d9d76-112">Invoke</span></span> 

<span data-ttu-id="d9d76-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="d9d76-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="d9d76-114">[appel](#invoke)HRESULT public (résultat HRESULT,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span><span class="sxs-lookup"><span data-stu-id="d9d76-114">public HRESULT [Invoke](#invoke)(HRESULT result,[IWebView2Environment](IWebView2Environment.md) \* webViewEnvironment)</span></span>

