---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: 3ecafb8181b04032bf121a93af3771cfcad8fa91
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011166"
---
# <span data-ttu-id="f537d-104">0.9.579-interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="f537d-104">0.9.579 - interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="f537d-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="f537d-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="f537d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f537d-106">Summary</span></span>

 <span data-ttu-id="f537d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f537d-107">Members</span></span>                        | <span data-ttu-id="f537d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f537d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f537d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f537d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f537d-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="f537d-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="f537d-111">Ses</span><span class="sxs-lookup"><span data-stu-id="f537d-111">Members</span></span>

#### <span data-ttu-id="f537d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f537d-112">Invoke</span></span> 

<span data-ttu-id="f537d-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="f537d-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="f537d-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="f537d-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

