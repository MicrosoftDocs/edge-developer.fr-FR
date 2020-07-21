---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: c021cfa866e55bfdf30185eeaf6015db1b523271
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886543"
---
# <span data-ttu-id="ee8b5-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="ee8b5-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="ee8b5-105">Gestionnaire d’achèvement de la méthode asynchrone PopulateResponseContent.</span><span class="sxs-lookup"><span data-stu-id="ee8b5-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="ee8b5-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ee8b5-106">Summary</span></span>

 <span data-ttu-id="ee8b5-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ee8b5-107">Members</span></span>                        | <span data-ttu-id="ee8b5-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ee8b5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ee8b5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ee8b5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ee8b5-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="ee8b5-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="ee8b5-111">Il est appelé lorsque le flux de contenu de la réponse à un événement WebResourceResponseReceieved est disponible.</span><span class="sxs-lookup"><span data-stu-id="ee8b5-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="ee8b5-112">Ses</span><span class="sxs-lookup"><span data-stu-id="ee8b5-112">Members</span></span>

#### <span data-ttu-id="ee8b5-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="ee8b5-113">Invoke</span></span> 

<span data-ttu-id="ee8b5-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="ee8b5-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="ee8b5-115">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="ee8b5-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

