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
ms.openlocfilehash: da49c1762ad7b7f3f366754bb9b05b7d16b861b7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653531"
---
# <span data-ttu-id="709c2-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="709c2-104">interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="709c2-105">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="709c2-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="709c2-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="709c2-106">Summary</span></span>

 <span data-ttu-id="709c2-107">Ses</span><span class="sxs-lookup"><span data-stu-id="709c2-107">Members</span></span>                        | <span data-ttu-id="709c2-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="709c2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="709c2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="709c2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="709c2-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="709c2-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="709c2-111">Ses</span><span class="sxs-lookup"><span data-stu-id="709c2-111">Members</span></span>

#### <span data-ttu-id="709c2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="709c2-112">Invoke</span></span> 

<span data-ttu-id="709c2-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="709c2-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="709c2-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="709c2-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Environment](icorewebview2environment.md) \* created_environment)</span></span>

