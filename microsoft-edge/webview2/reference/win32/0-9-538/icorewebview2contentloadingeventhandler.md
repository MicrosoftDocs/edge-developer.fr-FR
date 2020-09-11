---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ContentLoadingEventHandler
ms.openlocfilehash: 906b09ad99d6d6d9e74c52c0582584b9e46f74ba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010536"
---
# <span data-ttu-id="42c70-104">0.9.579-interface ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="42c70-104">0.9.579 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="42c70-105">L’appelant implémente cette interface pour recevoir l’événement ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="42c70-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="42c70-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="42c70-106">Summary</span></span>

 <span data-ttu-id="42c70-107">Ses</span><span class="sxs-lookup"><span data-stu-id="42c70-107">Members</span></span>                        | <span data-ttu-id="42c70-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="42c70-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="42c70-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="42c70-109">Invoke</span></span>](#invoke) | <span data-ttu-id="42c70-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="42c70-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="42c70-111">Ses</span><span class="sxs-lookup"><span data-stu-id="42c70-111">Members</span></span>

#### <span data-ttu-id="42c70-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="42c70-112">Invoke</span></span> 

<span data-ttu-id="42c70-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="42c70-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="42c70-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="42c70-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

