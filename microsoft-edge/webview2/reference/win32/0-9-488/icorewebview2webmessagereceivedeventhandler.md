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
ms.openlocfilehash: 73af2e217ca645536623eca18ceafad3270529cd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653549"
---
# <span data-ttu-id="70ac8-104">interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="70ac8-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="70ac8-105">L’appelant implémente cette interface pour recevoir l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="70ac8-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="70ac8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="70ac8-106">Summary</span></span>

 <span data-ttu-id="70ac8-107">Ses</span><span class="sxs-lookup"><span data-stu-id="70ac8-107">Members</span></span>                        | <span data-ttu-id="70ac8-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="70ac8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70ac8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="70ac8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="70ac8-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="70ac8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="70ac8-111">Ses</span><span class="sxs-lookup"><span data-stu-id="70ac8-111">Members</span></span>

#### <span data-ttu-id="70ac8-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="70ac8-112">Invoke</span></span> 

<span data-ttu-id="70ac8-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="70ac8-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="70ac8-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="70ac8-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

