---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExecuteScriptCompletedHandler
ms.openlocfilehash: 0b257cef4ed4a85fcd41cd401ef00eea01a4d8b6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010228"
---
# <span data-ttu-id="358a0-104">0.9.579-interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="358a0-104">0.9.579 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="358a0-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="358a0-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="358a0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="358a0-106">Summary</span></span>

 <span data-ttu-id="358a0-107">Ses</span><span class="sxs-lookup"><span data-stu-id="358a0-107">Members</span></span>                        | <span data-ttu-id="358a0-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="358a0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="358a0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="358a0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="358a0-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="358a0-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="358a0-111">Ses</span><span class="sxs-lookup"><span data-stu-id="358a0-111">Members</span></span>

#### <span data-ttu-id="358a0-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="358a0-112">Invoke</span></span> 

<span data-ttu-id="358a0-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="358a0-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="358a0-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="358a0-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

