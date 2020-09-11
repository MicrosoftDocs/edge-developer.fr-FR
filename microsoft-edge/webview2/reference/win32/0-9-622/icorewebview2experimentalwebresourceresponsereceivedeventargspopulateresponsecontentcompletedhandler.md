---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6c97e0591d55570f4076f6a5c4f2eebc2cc7c5ad
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011836"
---
# <span data-ttu-id="70ea1-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="70ea1-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="70ea1-105">Gestionnaire d’achèvement de la méthode asynchrone PopulateResponseContent.</span><span class="sxs-lookup"><span data-stu-id="70ea1-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="70ea1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="70ea1-106">Summary</span></span>

 <span data-ttu-id="70ea1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="70ea1-107">Members</span></span>                        | <span data-ttu-id="70ea1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="70ea1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70ea1-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="70ea1-109">Invoke</span></span>](#invoke) | <span data-ttu-id="70ea1-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="70ea1-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="70ea1-111">Il est appelé lorsque le flux de contenu de la réponse à un événement WebResourceResponseReceieved est disponible.</span><span class="sxs-lookup"><span data-stu-id="70ea1-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="70ea1-112">Ses</span><span class="sxs-lookup"><span data-stu-id="70ea1-112">Members</span></span>

#### <span data-ttu-id="70ea1-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="70ea1-113">Invoke</span></span> 

<span data-ttu-id="70ea1-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="70ea1-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="70ea1-115">[appel](#invoke)HRESULT public (HRESULT codeerreur)</span><span class="sxs-lookup"><span data-stu-id="70ea1-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>

