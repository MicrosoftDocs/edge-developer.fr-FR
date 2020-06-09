---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: a675bede2e1e509f3cfcc7490ac157da3f6d876c
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698667"
---
# <span data-ttu-id="021f1-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="021f1-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="021f1-105">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="021f1-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="021f1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="021f1-106">Summary</span></span>

 <span data-ttu-id="021f1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="021f1-107">Members</span></span>                        | <span data-ttu-id="021f1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="021f1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="021f1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="021f1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="021f1-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="021f1-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="021f1-111">Ses</span><span class="sxs-lookup"><span data-stu-id="021f1-111">Members</span></span>

#### <span data-ttu-id="021f1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="021f1-112">Invoke</span></span> 

<span data-ttu-id="021f1-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="021f1-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="021f1-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="021f1-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

