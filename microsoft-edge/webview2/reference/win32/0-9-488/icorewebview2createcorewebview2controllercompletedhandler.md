---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 49b2baf825d65b97b4b1fa62d06b2f6d6b7bd26d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653535"
---
# <span data-ttu-id="87e20-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="87e20-104">interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler</span></span> 

```
interface ICoreWebView2CreateCoreWebView2ControllerCompletedHandler
  : public IUnknown
```

<span data-ttu-id="87e20-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Controller créées via CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="87e20-105">The caller implements this interface to receive the CoreWebView2Controller created via CreateCoreWebView2Controller.</span></span>

## <span data-ttu-id="87e20-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="87e20-106">Summary</span></span>

 <span data-ttu-id="87e20-107">Ses</span><span class="sxs-lookup"><span data-stu-id="87e20-107">Members</span></span>                        | <span data-ttu-id="87e20-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="87e20-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="87e20-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="87e20-109">Invoke</span></span>](#invoke) | <span data-ttu-id="87e20-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="87e20-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="87e20-111">Ses</span><span class="sxs-lookup"><span data-stu-id="87e20-111">Members</span></span>

#### <span data-ttu-id="87e20-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="87e20-112">Invoke</span></span> 

<span data-ttu-id="87e20-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="87e20-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="87e20-114">[appel](#invoke)HRESULT public (résultat HRESULT, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span><span class="sxs-lookup"><span data-stu-id="87e20-114">public HRESULT [Invoke](#invoke)(HRESULT result, [ICoreWebView2Controller](icorewebview2controller.md) \* createdController)</span></span>

