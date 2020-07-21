---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2CreateCoreWebView2HostCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 9c2b5568e6a276b07dc91bd639c730b2009aa9e5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884280"
---
# <span data-ttu-id="3ea13-104">0.9.430-interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="3ea13-104">0.9.430 - interface ICoreWebView2CreateCoreWebView2HostCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CreateCoreWebView2HostCompletedHandler
  : public IUnknown
```

<span data-ttu-id="3ea13-105">L’appelant implémente cette interface pour recevoir les CoreWebView2Host créées via CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="3ea13-105">The caller implements this interface to receive the CoreWebView2Host created via CreateCoreWebView2Host.</span></span>

## <span data-ttu-id="3ea13-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="3ea13-106">Summary</span></span>

 <span data-ttu-id="3ea13-107">Ses</span><span class="sxs-lookup"><span data-stu-id="3ea13-107">Members</span></span>                        | <span data-ttu-id="3ea13-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3ea13-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3ea13-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3ea13-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3ea13-110">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="3ea13-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="3ea13-111">Ses</span><span class="sxs-lookup"><span data-stu-id="3ea13-111">Members</span></span>

#### <span data-ttu-id="3ea13-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3ea13-112">Invoke</span></span> 

<span data-ttu-id="3ea13-113">Appelée pour fournir à l’implémenteur l’état d’achèvement et le résultat de l’appel de méthode asynchrone correspondant.</span><span class="sxs-lookup"><span data-stu-id="3ea13-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="3ea13-114">[appel](#invoke)HRESULT public (résultat HRESULT,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span><span class="sxs-lookup"><span data-stu-id="3ea13-114">public HRESULT [Invoke](#invoke)(HRESULT result,[ICoreWebView2Host](ICoreWebView2Host.md) \* created_host)</span></span>

