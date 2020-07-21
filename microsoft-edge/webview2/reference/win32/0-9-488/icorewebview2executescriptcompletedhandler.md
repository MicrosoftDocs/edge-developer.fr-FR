---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: da66c70724a6ce2c1102fcc2ef248963c11f0d1d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885302"
---
# <span data-ttu-id="77a01-104">0.9.515-interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="77a01-104">0.9.515 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="77a01-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="77a01-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="77a01-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="77a01-106">Summary</span></span>

 <span data-ttu-id="77a01-107">Ses</span><span class="sxs-lookup"><span data-stu-id="77a01-107">Members</span></span>                        | <span data-ttu-id="77a01-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="77a01-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="77a01-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="77a01-109">Invoke</span></span>](#invoke) | <span data-ttu-id="77a01-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="77a01-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="77a01-111">Ses</span><span class="sxs-lookup"><span data-stu-id="77a01-111">Members</span></span>

#### <span data-ttu-id="77a01-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="77a01-112">Invoke</span></span> 

<span data-ttu-id="77a01-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="77a01-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="77a01-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="77a01-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

