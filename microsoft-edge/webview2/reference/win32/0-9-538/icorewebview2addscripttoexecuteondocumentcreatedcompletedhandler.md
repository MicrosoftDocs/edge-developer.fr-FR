---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
ms.openlocfilehash: 81b2895f652646991102af37e4da7cd99e789e10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877513"
---
# <span data-ttu-id="dc5dd-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="dc5dd-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="dc5dd-105">L’appelant implémente cette interface pour recevoir le résultat de la méthode AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="dc5dd-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="dc5dd-106">Summary</span></span>

 <span data-ttu-id="dc5dd-107">Ses</span><span class="sxs-lookup"><span data-stu-id="dc5dd-107">Members</span></span>                        | <span data-ttu-id="dc5dd-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="dc5dd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc5dd-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc5dd-109">Invoke</span></span>](#invoke) | <span data-ttu-id="dc5dd-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="dc5dd-111">Ses</span><span class="sxs-lookup"><span data-stu-id="dc5dd-111">Members</span></span>

#### <span data-ttu-id="dc5dd-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="dc5dd-112">Invoke</span></span> 

<span data-ttu-id="dc5dd-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="dc5dd-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="dc5dd-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, ID LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="dc5dd-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

