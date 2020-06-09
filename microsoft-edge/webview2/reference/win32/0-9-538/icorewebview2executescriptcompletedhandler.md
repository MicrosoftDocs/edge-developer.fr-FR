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
ms.openlocfilehash: a3dde4581692fb30cada16d9166bda62a0d69179
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698637"
---
# <span data-ttu-id="8b42b-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="8b42b-104">interface ICoreWebView2ExecuteScriptCompletedHandler</span></span> 

```
interface ICoreWebView2ExecuteScriptCompletedHandler
  : public IUnknown
```

<span data-ttu-id="8b42b-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode ExecuteScript.</span><span class="sxs-lookup"><span data-stu-id="8b42b-105">The caller implements this interface to receive the result of the ExecuteScript method.</span></span>

## <span data-ttu-id="8b42b-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8b42b-106">Summary</span></span>

 <span data-ttu-id="8b42b-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8b42b-107">Members</span></span>                        | <span data-ttu-id="8b42b-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8b42b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b42b-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8b42b-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8b42b-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="8b42b-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="8b42b-111">Ses</span><span class="sxs-lookup"><span data-stu-id="8b42b-111">Members</span></span>

#### <span data-ttu-id="8b42b-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8b42b-112">Invoke</span></span> 

<span data-ttu-id="8b42b-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="8b42b-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="8b42b-114">[appel](#invoke)HRESULT public (HRESULT CODEERREUR, LPCWSTR resultObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="8b42b-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR resultObjectAsJson)</span></span>

