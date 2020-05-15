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
ms.openlocfilehash: 1f7eb0237e43913ffcd147ff28dde0c14561643d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653640"
---
# <span data-ttu-id="ed6e9-104">interface ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ed6e9-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="ed6e9-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="ed6e9-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ed6e9-107">L’appelant implémente cette interface pour recevoir l’événement SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="ed6e9-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="ed6e9-108">Summary</span></span>

 <span data-ttu-id="ed6e9-109">Ses</span><span class="sxs-lookup"><span data-stu-id="ed6e9-109">Members</span></span>                        | <span data-ttu-id="ed6e9-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ed6e9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ed6e9-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="ed6e9-111">Invoke</span></span>](#invoke) | <span data-ttu-id="ed6e9-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ed6e9-113">Ses</span><span class="sxs-lookup"><span data-stu-id="ed6e9-113">Members</span></span>

#### <span data-ttu-id="ed6e9-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="ed6e9-114">Invoke</span></span> 

<span data-ttu-id="ed6e9-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ed6e9-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ed6e9-116">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ed6e9-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2SourceChangedEventArgs](ICoreWebView2SourceChangedEventArgs.md) \* args)</span></span>

