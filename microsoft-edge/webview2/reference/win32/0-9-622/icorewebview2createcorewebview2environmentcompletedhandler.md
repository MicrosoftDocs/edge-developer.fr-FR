---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
ms.openlocfilehash: 3f6b6b9a2d4df2a450b4589c351c3ea98f7cc28f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011989"
---
# <span data-ttu-id="6886f-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="6886f-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="6886f-105">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="6886f-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="6886f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="6886f-106">Summary</span></span>

 <span data-ttu-id="6886f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="6886f-107">Members</span></span>                        | <span data-ttu-id="6886f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6886f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6886f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="6886f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="6886f-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="6886f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="6886f-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6886f-111">Members</span></span>

#### <span data-ttu-id="6886f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="6886f-112">Invoke</span></span> 

<span data-ttu-id="6886f-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="6886f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="6886f-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span><span class="sxs-lookup"><span data-stu-id="6886f-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Environment](icorewebview2environment.md) \* createdEnvironment)</span></span>

