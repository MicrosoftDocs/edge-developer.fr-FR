---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 8a9e3c1c5d2e9b7053d09518e3086f9e038e181a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883923"
---
# <span data-ttu-id="524f6-104">0.9.515-interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="524f6-104">0.9.515 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="524f6-105">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="524f6-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="524f6-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="524f6-106">Summary</span></span>

 <span data-ttu-id="524f6-107">Ses</span><span class="sxs-lookup"><span data-stu-id="524f6-107">Members</span></span>                        | <span data-ttu-id="524f6-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="524f6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="524f6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="524f6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="524f6-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="524f6-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="524f6-111">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="524f6-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="524f6-112">Ses</span><span class="sxs-lookup"><span data-stu-id="524f6-112">Members</span></span>

#### <span data-ttu-id="524f6-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="524f6-113">Invoke</span></span> 

<span data-ttu-id="524f6-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="524f6-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="524f6-115">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="524f6-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

