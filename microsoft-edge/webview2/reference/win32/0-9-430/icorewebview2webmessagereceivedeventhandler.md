---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: b59eae6966efb6c2ebfc018be5ec0a5d2d5334c7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653289"
---
# <span data-ttu-id="f1356-104">interface ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f1356-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f1356-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f1356-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f1356-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="f1356-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="f1356-107">L’appelant implémente cette interface pour recevoir l’événement WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="f1356-107">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="f1356-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f1356-108">Summary</span></span>

 <span data-ttu-id="f1356-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f1356-109">Members</span></span>                        | <span data-ttu-id="f1356-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f1356-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f1356-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f1356-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f1356-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f1356-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f1356-113">Ses</span><span class="sxs-lookup"><span data-stu-id="f1356-113">Members</span></span>

#### <span data-ttu-id="f1356-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f1356-114">Invoke</span></span> 

<span data-ttu-id="f1356-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="f1356-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f1356-116">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f1356-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebMessageReceivedEventArgs](ICoreWebView2WebMessageReceivedEventArgs.md) \* args)</span></span>

