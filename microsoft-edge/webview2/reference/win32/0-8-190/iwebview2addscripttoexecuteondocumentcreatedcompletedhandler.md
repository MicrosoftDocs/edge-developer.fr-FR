---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 464192c119ddb7dd59ee7cb5981f172eb44dbb78
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885015"
---
# <span data-ttu-id="dee1f-104">0.8.355-interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="dee1f-104">0.8.355 - interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="dee1f-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="dee1f-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="dee1f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="dee1f-106">Summary</span></span>

 <span data-ttu-id="dee1f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="dee1f-107">Members</span></span>                        | <span data-ttu-id="dee1f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="dee1f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dee1f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="dee1f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dee1f-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="dee1f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="dee1f-111">Ses</span><span class="sxs-lookup"><span data-stu-id="dee1f-111">Members</span></span>

#### <span data-ttu-id="dee1f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="dee1f-112">Invoke</span></span> 

<span data-ttu-id="dee1f-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="dee1f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="dee1f-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="dee1f-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode,LPCWSTR id)</span></span>

