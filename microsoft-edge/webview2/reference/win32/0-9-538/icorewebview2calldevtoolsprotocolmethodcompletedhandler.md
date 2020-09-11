---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
ms.openlocfilehash: aed9cb6a748730e7bb7872b02e06233e97600e17
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010620"
---
# <span data-ttu-id="e95fa-104">0.9.579-interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="e95fa-104">0.9.579 - interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

<span data-ttu-id="e95fa-105">L’appelant implémente cette interface pour recevoir des résultats d’achèvement CallDevToolsProtocolMethod.</span><span class="sxs-lookup"><span data-stu-id="e95fa-105">The caller implements this interface to receive CallDevToolsProtocolMethod completion results.</span></span>

## <span data-ttu-id="e95fa-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="e95fa-106">Summary</span></span>

 <span data-ttu-id="e95fa-107">Ses</span><span class="sxs-lookup"><span data-stu-id="e95fa-107">Members</span></span>                        | <span data-ttu-id="e95fa-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e95fa-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e95fa-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="e95fa-109">Invoke</span></span>](#invoke) | <span data-ttu-id="e95fa-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="e95fa-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="e95fa-111">Ses</span><span class="sxs-lookup"><span data-stu-id="e95fa-111">Members</span></span>

#### <span data-ttu-id="e95fa-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="e95fa-112">Invoke</span></span> 

<span data-ttu-id="e95fa-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="e95fa-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="e95fa-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR returnObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e95fa-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR returnObjectAsJson)</span></span>

