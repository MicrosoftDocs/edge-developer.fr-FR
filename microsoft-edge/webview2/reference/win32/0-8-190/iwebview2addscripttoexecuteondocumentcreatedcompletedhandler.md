---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 903574f0372e9d077907b9e9d538007cb71f830f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878672"
---
# <span data-ttu-id="12df6-104">0.8.355-interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="12df6-104">0.8.355 - interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="12df6-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="12df6-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="12df6-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="12df6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="12df6-107">L’appelant implémente cette interface pour recevoir le résultat de la méthode AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="12df6-107">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="12df6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="12df6-108">Summary</span></span>

 <span data-ttu-id="12df6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="12df6-109">Members</span></span>                        | <span data-ttu-id="12df6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="12df6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="12df6-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="12df6-111">Invoke</span></span>](#invoke) | <span data-ttu-id="12df6-112">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="12df6-112">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="12df6-113">Ses</span><span class="sxs-lookup"><span data-stu-id="12df6-113">Members</span></span>

#### <span data-ttu-id="12df6-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="12df6-114">Invoke</span></span> 

<span data-ttu-id="12df6-115">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="12df6-115">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="12df6-116">[appel](#invoke)HRESULT public (HRESULT codeerreur, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="12df6-116">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>

