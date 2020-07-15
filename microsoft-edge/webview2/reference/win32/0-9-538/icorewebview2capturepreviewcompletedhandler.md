---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 013a7076648b93bf259d28422f418365d988a586
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877439"
---
# <span data-ttu-id="af5f8-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="af5f8-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="af5f8-105">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="af5f8-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="af5f8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="af5f8-106">Summary</span></span>

 <span data-ttu-id="af5f8-107">Ses</span><span class="sxs-lookup"><span data-stu-id="af5f8-107">Members</span></span>                        | <span data-ttu-id="af5f8-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="af5f8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af5f8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="af5f8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="af5f8-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="af5f8-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="af5f8-111">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="af5f8-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="af5f8-112">Ses</span><span class="sxs-lookup"><span data-stu-id="af5f8-112">Members</span></span>

#### <span data-ttu-id="af5f8-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="af5f8-113">Invoke</span></span> 

<span data-ttu-id="af5f8-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="af5f8-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="af5f8-115">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="af5f8-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

