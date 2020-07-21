---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 7a983d313e242cc163fb16a9c0d0068a9d6663d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883930"
---
# <span data-ttu-id="b8cf1-104">0.9.515-interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b8cf1-104">0.9.515 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b8cf1-105">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="b8cf1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b8cf1-106">Summary</span></span>

 <span data-ttu-id="b8cf1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b8cf1-107">Members</span></span>                        | <span data-ttu-id="b8cf1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b8cf1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b8cf1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b8cf1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b8cf1-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b8cf1-111">Ses</span><span class="sxs-lookup"><span data-stu-id="b8cf1-111">Members</span></span>

#### <span data-ttu-id="b8cf1-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b8cf1-112">Invoke</span></span> 

<span data-ttu-id="b8cf1-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b8cf1-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b8cf1-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="b8cf1-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

