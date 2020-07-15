---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: c991e9e9520bd696c579fdca379295afe253ba5d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877512"
---
# <span data-ttu-id="a5844-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="a5844-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="a5844-105">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="a5844-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="a5844-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="a5844-106">Summary</span></span>

 <span data-ttu-id="a5844-107">Ses</span><span class="sxs-lookup"><span data-stu-id="a5844-107">Members</span></span>                        | <span data-ttu-id="a5844-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="a5844-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a5844-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="a5844-109">Invoke</span></span>](#invoke) | <span data-ttu-id="a5844-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="a5844-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="a5844-111">Ses</span><span class="sxs-lookup"><span data-stu-id="a5844-111">Members</span></span>

#### <span data-ttu-id="a5844-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="a5844-112">Invoke</span></span> 

<span data-ttu-id="a5844-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="a5844-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="a5844-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="a5844-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

