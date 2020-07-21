---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: c08a851eb21947cae4af465a233dc4c49508c84c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884210"
---
# <span data-ttu-id="ea95f-104">0.9.430-interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ea95f-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="ea95f-105">L’appelant implémente cette interface pour recevoir des événements DevToolsProtocolEventReceived du WebView.</span><span class="sxs-lookup"><span data-stu-id="ea95f-105">The caller implements this interface to receive DevToolsProtocolEventReceived events from the WebView.</span></span>

## <span data-ttu-id="ea95f-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ea95f-106">Summary</span></span>

 <span data-ttu-id="ea95f-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ea95f-107">Members</span></span>                        | <span data-ttu-id="ea95f-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ea95f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea95f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ea95f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ea95f-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ea95f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ea95f-111">Ses</span><span class="sxs-lookup"><span data-stu-id="ea95f-111">Members</span></span>

#### <span data-ttu-id="ea95f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ea95f-112">Invoke</span></span> 

<span data-ttu-id="ea95f-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ea95f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ea95f-114">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ea95f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2DevToolsProtocolEventReceivedEventArgs](ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md) \* args)</span></span>

