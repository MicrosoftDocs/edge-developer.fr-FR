---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: e526b723f111d7212a5da4b25840c89b69eb2e52
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011812"
---
# <span data-ttu-id="5bb45-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="5bb45-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="5bb45-105">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="5bb45-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="5bb45-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="5bb45-106">Summary</span></span>

 <span data-ttu-id="5bb45-107">Ses</span><span class="sxs-lookup"><span data-stu-id="5bb45-107">Members</span></span>                        | <span data-ttu-id="5bb45-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="5bb45-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5bb45-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5bb45-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5bb45-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="5bb45-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="5bb45-111">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="5bb45-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="5bb45-112">Ses</span><span class="sxs-lookup"><span data-stu-id="5bb45-112">Members</span></span>

#### <span data-ttu-id="5bb45-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="5bb45-113">Invoke</span></span> 

<span data-ttu-id="5bb45-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="5bb45-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="5bb45-115">[appel](#invoke)HRESULT public (HRESULT codeerreur)</span><span class="sxs-lookup"><span data-stu-id="5bb45-115">public HRESULT [Invoke](#invoke)(HRESULT errorCode)</span></span>

