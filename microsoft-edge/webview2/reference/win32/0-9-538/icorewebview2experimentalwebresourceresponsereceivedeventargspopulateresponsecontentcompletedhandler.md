---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
ms.openlocfilehash: 6a854eb9ca73f45e366edfa144c273f780bcee94
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011411"
---
# <span data-ttu-id="0ba83-104">0.9.579-interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="0ba83-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler
  : public IUnknown
```

<span data-ttu-id="0ba83-105">Gestionnaire d’achèvement de la méthode asynchrone PopulateResponseContent.</span><span class="sxs-lookup"><span data-stu-id="0ba83-105">Completion handler for PopulateResponseContent async method.</span></span>

## <span data-ttu-id="0ba83-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="0ba83-106">Summary</span></span>

 <span data-ttu-id="0ba83-107">Ses</span><span class="sxs-lookup"><span data-stu-id="0ba83-107">Members</span></span>                        | <span data-ttu-id="0ba83-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0ba83-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0ba83-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ba83-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0ba83-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="0ba83-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="0ba83-111">Il est appelé lorsque le flux de contenu de la réponse à un événement WebResourceResponseReceieved est disponible.</span><span class="sxs-lookup"><span data-stu-id="0ba83-111">It's invoked when the Content stream of the Response of a WebResourceResponseReceieved event is available.</span></span>

## <span data-ttu-id="0ba83-112">Ses</span><span class="sxs-lookup"><span data-stu-id="0ba83-112">Members</span></span>

#### <span data-ttu-id="0ba83-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="0ba83-113">Invoke</span></span> 

<span data-ttu-id="0ba83-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="0ba83-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="0ba83-115">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="0ba83-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

