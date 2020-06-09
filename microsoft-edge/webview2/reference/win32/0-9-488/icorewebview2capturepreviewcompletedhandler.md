---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 6aaac0d062d0e97d3ec0c87bec243c5cf682ad6f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697048"
---
# <span data-ttu-id="49b4f-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="49b4f-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="49b4f-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="49b4f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="49b4f-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="49b4f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="49b4f-107">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="49b4f-107">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="49b4f-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="49b4f-108">Summary</span></span>

 <span data-ttu-id="49b4f-109">Ses</span><span class="sxs-lookup"><span data-stu-id="49b4f-109">Members</span></span>                        | <span data-ttu-id="49b4f-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="49b4f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49b4f-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="49b4f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="49b4f-112">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="49b4f-112">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="49b4f-113">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="49b4f-113">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="49b4f-114">Ses</span><span class="sxs-lookup"><span data-stu-id="49b4f-114">Members</span></span>

#### <span data-ttu-id="49b4f-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="49b4f-115">Invoke</span></span> 

<span data-ttu-id="49b4f-116">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="49b4f-116">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="49b4f-117">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="49b4f-117">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

