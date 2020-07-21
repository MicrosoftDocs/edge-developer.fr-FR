---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ExecuteScriptCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 9a96e18b8c0b56cd75d4f0fe7b0c90c0634fe68b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884196"
---
# <span data-ttu-id="ac354-104">0.9.430-interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ac354-104">0.9.430 - interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ac354-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="ac354-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="ac354-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ac354-106">Summary</span></span>

 <span data-ttu-id="ac354-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ac354-107">Members</span></span>                        | <span data-ttu-id="ac354-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ac354-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac354-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ac354-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ac354-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="ac354-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="ac354-111">Ses</span><span class="sxs-lookup"><span data-stu-id="ac354-111">Members</span></span>

#### <span data-ttu-id="ac354-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ac354-112">Invoke</span></span> 

<span data-ttu-id="ac354-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="ac354-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ac354-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="ac354-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR resultObjectAsJson)</span></span>

