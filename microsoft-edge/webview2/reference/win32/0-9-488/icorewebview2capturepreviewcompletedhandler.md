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
ms.openlocfilehash: 793dbde462e25ae0bfe0dc0bc475cc49e7237fb2
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653552"
---
# <span data-ttu-id="b188c-104">interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b188c-104">interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b188c-105">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="b188c-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="b188c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b188c-106">Summary</span></span>

 <span data-ttu-id="b188c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b188c-107">Members</span></span>                        | <span data-ttu-id="b188c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b188c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b188c-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b188c-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b188c-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b188c-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="b188c-111">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="b188c-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="b188c-112">Ses</span><span class="sxs-lookup"><span data-stu-id="b188c-112">Members</span></span>

#### <span data-ttu-id="b188c-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="b188c-113">Invoke</span></span> 

<span data-ttu-id="b188c-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="b188c-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b188c-115">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="b188c-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

