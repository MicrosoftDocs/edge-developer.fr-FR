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
ms.openlocfilehash: 45ac3cf4728f8b09f9ce65a30b53506fc2829c9d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698657"
---
# <span data-ttu-id="87624-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="87624-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="87624-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="87624-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="87624-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="87624-106">Summary</span></span>

 <span data-ttu-id="87624-107">Ses</span><span class="sxs-lookup"><span data-stu-id="87624-107">Members</span></span>                        | <span data-ttu-id="87624-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="87624-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="87624-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="87624-109">Invoke</span></span>](#invoke) | <span data-ttu-id="87624-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="87624-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="87624-111">Ses</span><span class="sxs-lookup"><span data-stu-id="87624-111">Members</span></span>

#### <span data-ttu-id="87624-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="87624-112">Invoke</span></span> 

<span data-ttu-id="87624-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="87624-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="87624-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="87624-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

