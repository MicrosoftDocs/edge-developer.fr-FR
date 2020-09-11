---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 4b280a16c18c84641f91efd39407f93db968f69d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011984"
---
# <span data-ttu-id="b7fc4-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b7fc4-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="b7fc4-105">L’appelant implémente cette interface pour recevoir des événements DevToolsProtocolEventReceived du WebView.</span><span class="sxs-lookup"><span data-stu-id="b7fc4-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="b7fc4-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b7fc4-106">Summary</span></span>

 <span data-ttu-id="b7fc4-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b7fc4-107">Members</span></span>                        | <span data-ttu-id="b7fc4-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b7fc4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b7fc4-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b7fc4-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b7fc4-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="b7fc4-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b7fc4-111">Ses</span><span class="sxs-lookup"><span data-stu-id="b7fc4-111">Members</span></span>

#### <span data-ttu-id="b7fc4-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b7fc4-112">Invoke</span></span> 

<span data-ttu-id="b7fc4-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="b7fc4-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b7fc4-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="b7fc4-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

