---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 163ab3f16b6d835fc64aef4ea0fdff2883084faa
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010263"
---
# <span data-ttu-id="05441-104">0.9.579-interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="05441-104">0.9.579 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="05441-105">L’appelant implémente cette interface pour recevoir des événements DevToolsProtocolEventReceived du WebView.</span><span class="sxs-lookup"><span data-stu-id="05441-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="05441-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="05441-106">Summary</span></span>

 <span data-ttu-id="05441-107">Ses</span><span class="sxs-lookup"><span data-stu-id="05441-107">Members</span></span>                        | <span data-ttu-id="05441-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="05441-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="05441-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="05441-109">Invoke</span></span>](#invoke) | <span data-ttu-id="05441-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="05441-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="05441-111">Ses</span><span class="sxs-lookup"><span data-stu-id="05441-111">Members</span></span>

#### <span data-ttu-id="05441-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="05441-112">Invoke</span></span> 

<span data-ttu-id="05441-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="05441-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="05441-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="05441-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) \* args)</span></span>

