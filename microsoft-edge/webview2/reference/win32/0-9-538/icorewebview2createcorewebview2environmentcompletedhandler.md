---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: c41da3c6f88c06d0642d00f38a8181acb079a009
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877405"
---
# <span data-ttu-id="41ff6-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="41ff6-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="41ff6-105">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="41ff6-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="41ff6-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="41ff6-106">Summary</span></span>

 <span data-ttu-id="41ff6-107">Ses</span><span class="sxs-lookup"><span data-stu-id="41ff6-107">Members</span></span>                        | <span data-ttu-id="41ff6-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="41ff6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="41ff6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="41ff6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="41ff6-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="41ff6-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="41ff6-111">Ses</span><span class="sxs-lookup"><span data-stu-id="41ff6-111">Members</span></span>

#### <span data-ttu-id="41ff6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="41ff6-112">Invoke</span></span> 

<span data-ttu-id="41ff6-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="41ff6-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="41ff6-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="41ff6-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

