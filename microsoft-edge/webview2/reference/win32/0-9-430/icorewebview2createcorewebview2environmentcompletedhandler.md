---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 5cc3ca23dcababc35a73b44a81c54439d0dbe1a3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884308"
---
# <span data-ttu-id="2f9ee-104">0.9.430-interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="2f9ee-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="2f9ee-105">L’appelant implémente cette interface pour recevoir les WebView2Environment créées via CreateCoreWebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="2f9ee-105">The caller implements this interface to receive the WebView2Environment created via CreateCoreWebView2Environment.</span></span>

## <span data-ttu-id="2f9ee-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="2f9ee-106">Summary</span></span>

 <span data-ttu-id="2f9ee-107">Ses</span><span class="sxs-lookup"><span data-stu-id="2f9ee-107">Members</span></span>                        | <span data-ttu-id="2f9ee-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2f9ee-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2f9ee-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2f9ee-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2f9ee-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="2f9ee-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="2f9ee-111">Ses</span><span class="sxs-lookup"><span data-stu-id="2f9ee-111">Members</span></span>

#### <span data-ttu-id="2f9ee-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2f9ee-112">Invoke</span></span> 

<span data-ttu-id="2f9ee-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="2f9ee-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="2f9ee-114">[appel](#invoke)HRESULT public (résultat HRESULT,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span><span class="sxs-lookup"><span data-stu-id="2f9ee-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Environment](ICoreWebView2Environment.md) \* created_environment)</span></span>

