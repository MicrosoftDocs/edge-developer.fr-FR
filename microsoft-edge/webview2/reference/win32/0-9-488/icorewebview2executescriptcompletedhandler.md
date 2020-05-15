---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: da7b12d382776bb1755e90b0ce1c2728b555c8c8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653566"
---
# <span data-ttu-id="99a9a-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="99a9a-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="99a9a-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="99a9a-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="99a9a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="99a9a-106">Summary</span></span>

 <span data-ttu-id="99a9a-107">Ses</span><span class="sxs-lookup"><span data-stu-id="99a9a-107">Members</span></span>                        | <span data-ttu-id="99a9a-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="99a9a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="99a9a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="99a9a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="99a9a-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="99a9a-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="99a9a-111">Ses</span><span class="sxs-lookup"><span data-stu-id="99a9a-111">Members</span></span>

#### <span data-ttu-id="99a9a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="99a9a-112">Invoke</span></span> 

<span data-ttu-id="99a9a-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="99a9a-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="99a9a-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="99a9a-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

