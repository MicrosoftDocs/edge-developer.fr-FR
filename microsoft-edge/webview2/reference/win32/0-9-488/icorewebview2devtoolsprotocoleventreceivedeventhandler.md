---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 1e59d8d830c3357fafd4f8315388ee5fff93a3d2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880807"
---
# <span data-ttu-id="21fb8-104">0.9.515-interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="21fb8-104">0.9.515 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="21fb8-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="21fb8-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="21fb8-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="21fb8-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="21fb8-107">L’appelant implémente cette interface pour recevoir des événements DevToolsProtocolEventReceived du WebView.</span><span class="sxs-lookup"><span data-stu-id="21fb8-107">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="21fb8-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="21fb8-108">Summary</span></span>

 <span data-ttu-id="21fb8-109">Ses</span><span class="sxs-lookup"><span data-stu-id="21fb8-109">Members</span></span>                        | <span data-ttu-id="21fb8-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="21fb8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21fb8-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="21fb8-111">Invoke</span></span>](#invoke) | <span data-ttu-id="21fb8-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="21fb8-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="21fb8-113">Ses</span><span class="sxs-lookup"><span data-stu-id="21fb8-113">Members</span></span>

#### <span data-ttu-id="21fb8-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="21fb8-114">Invoke</span></span> 

<span data-ttu-id="21fb8-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="21fb8-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="21fb8-116">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="21fb8-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

