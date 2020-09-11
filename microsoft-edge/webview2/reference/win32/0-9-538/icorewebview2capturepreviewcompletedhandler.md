---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 96fff3ab67331bf5a8cf8323af5dddbca04f9e0e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010564"
---
# <span data-ttu-id="512bf-104">0.9.579-interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="512bf-104">0.9.579 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="512bf-105">L’appelant implémente cette méthode pour recevoir le résultat de la méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="512bf-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="512bf-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="512bf-106">Summary</span></span>

 <span data-ttu-id="512bf-107">Ses</span><span class="sxs-lookup"><span data-stu-id="512bf-107">Members</span></span>                        | <span data-ttu-id="512bf-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="512bf-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="512bf-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="512bf-109">Invoke</span></span>](#invoke) | <span data-ttu-id="512bf-110">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="512bf-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="512bf-111">Le résultat est écrit dans le flux fourni lors de l’appel de méthode CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="512bf-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="512bf-112">Ses</span><span class="sxs-lookup"><span data-stu-id="512bf-112">Members</span></span>

#### <span data-ttu-id="512bf-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="512bf-113">Invoke</span></span> 

<span data-ttu-id="512bf-114">Appelée pour fournir à l’implémenteur l’état d’achèvement de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="512bf-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="512bf-115">[appel](#invoke)HRESULT public (résultat HRESULT)</span><span class="sxs-lookup"><span data-stu-id="512bf-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

