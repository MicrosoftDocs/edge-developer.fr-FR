---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 845c3a3f0241fb66032ecf818c484b6110258327
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011990"
---
# <span data-ttu-id="cb60f-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="cb60f-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="cb60f-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="cb60f-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="cb60f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="cb60f-106">Summary</span></span>

 <span data-ttu-id="cb60f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="cb60f-107">Members</span></span>                        | <span data-ttu-id="cb60f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cb60f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cb60f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="cb60f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="cb60f-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="cb60f-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="cb60f-111">Ses</span><span class="sxs-lookup"><span data-stu-id="cb60f-111">Members</span></span>

#### <span data-ttu-id="cb60f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="cb60f-112">Invoke</span></span> 

<span data-ttu-id="cb60f-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="cb60f-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="cb60f-114">[appel](#invoke)HRESULT public (HRESULT codeerreur, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="cb60f-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

