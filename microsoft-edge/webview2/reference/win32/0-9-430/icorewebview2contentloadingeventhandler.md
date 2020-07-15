---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 7f227e3b2c45b1088b1ac678477cf1dac5ffed5f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881129"
---
# <span data-ttu-id="3808f-104">0.9.430-interface ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="3808f-104">0.9.430 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="3808f-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="3808f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="3808f-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="3808f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="3808f-107">L’appelant implémente cette interface pour recevoir l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="3808f-107">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="3808f-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="3808f-108">Summary</span></span>

 <span data-ttu-id="3808f-109">Ses</span><span class="sxs-lookup"><span data-stu-id="3808f-109">Members</span></span>                        | <span data-ttu-id="3808f-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3808f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3808f-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="3808f-111">Invoke</span></span>](#invoke) | <span data-ttu-id="3808f-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3808f-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3808f-113">Ses</span><span class="sxs-lookup"><span data-stu-id="3808f-113">Members</span></span>

#### <span data-ttu-id="3808f-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="3808f-114">Invoke</span></span> 

<span data-ttu-id="3808f-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="3808f-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3808f-116">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3808f-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span></span>

