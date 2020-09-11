---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: f6c0037177843d65ce5fe7cc56f206d5661d4b2a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011999"
---
# <span data-ttu-id="72782-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="72782-104">interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="72782-105">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="72782-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="72782-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="72782-106">Summary</span></span>

 <span data-ttu-id="72782-107">Ses</span><span class="sxs-lookup"><span data-stu-id="72782-107">Members</span></span>                        | <span data-ttu-id="72782-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="72782-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="72782-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="72782-109">Invoke</span></span>](#invoke) | <span data-ttu-id="72782-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="72782-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="72782-111">Ses</span><span class="sxs-lookup"><span data-stu-id="72782-111">Members</span></span>

#### <span data-ttu-id="72782-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="72782-112">Invoke</span></span> 

<span data-ttu-id="72782-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="72782-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="72782-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="72782-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

