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
ms.openlocfilehash: 290d82666e5b9c5062132e1eb7515e39e2deb978
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698665"
---
# <span data-ttu-id="adb4c-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="adb4c-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="adb4c-105">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="adb4c-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="adb4c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="adb4c-106">Summary</span></span>

 <span data-ttu-id="adb4c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="adb4c-107">Members</span></span>                        | <span data-ttu-id="adb4c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="adb4c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="adb4c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="adb4c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="adb4c-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="adb4c-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="adb4c-111">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="adb4c-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="adb4c-112">Ses</span><span class="sxs-lookup"><span data-stu-id="adb4c-112">Members</span></span>

#### <span data-ttu-id="adb4c-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="adb4c-113">Invoke</span></span> 

<span data-ttu-id="adb4c-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="adb4c-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="adb4c-115">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="adb4c-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

