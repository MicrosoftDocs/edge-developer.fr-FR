---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
ms.openlocfilehash: e26d711c24758f82d42067fa28e71bc6ac1177ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877412"
---
# <span data-ttu-id="9bd18-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="9bd18-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="9bd18-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="9bd18-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="9bd18-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9bd18-106">Summary</span></span>

 <span data-ttu-id="9bd18-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9bd18-107">Members</span></span>                        | <span data-ttu-id="9bd18-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9bd18-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9bd18-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9bd18-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9bd18-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="9bd18-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="9bd18-111">Ses</span><span class="sxs-lookup"><span data-stu-id="9bd18-111">Members</span></span>

#### <span data-ttu-id="9bd18-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9bd18-112">Invoke</span></span> 

<span data-ttu-id="9bd18-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="9bd18-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="9bd18-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="9bd18-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

