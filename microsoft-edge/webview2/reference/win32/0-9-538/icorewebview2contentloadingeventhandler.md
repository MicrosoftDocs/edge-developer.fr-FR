---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: fb6e3cfabae0116ac746d6e8e5cc03efa0f1c1b6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877446"
---
# <span data-ttu-id="2ccd6-104">interface ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="2ccd6-104">interface ICoreWebView2ContentLoadingEventHandler</span></span> 

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="2ccd6-105">L’appelant implémente cette interface pour recevoir l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="2ccd6-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="2ccd6-106">Summary</span></span>

 <span data-ttu-id="2ccd6-107">Ses</span><span class="sxs-lookup"><span data-stu-id="2ccd6-107">Members</span></span>                        | <span data-ttu-id="2ccd6-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="2ccd6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ccd6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2ccd6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2ccd6-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2ccd6-111">Ses</span><span class="sxs-lookup"><span data-stu-id="2ccd6-111">Members</span></span>

#### <span data-ttu-id="2ccd6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2ccd6-112">Invoke</span></span> 

<span data-ttu-id="2ccd6-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="2ccd6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2ccd6-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2ccd6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

