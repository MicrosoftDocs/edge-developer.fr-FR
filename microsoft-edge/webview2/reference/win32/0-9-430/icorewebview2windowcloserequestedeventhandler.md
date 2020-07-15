---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WindowCloseRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 6a1b472a4a37c31d4914794784767f8e0b9b6b94
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877776"
---
# <span data-ttu-id="7fd98-104">0.9.430-interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7fd98-104">0.9.430 - interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="7fd98-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7fd98-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7fd98-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="7fd98-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="7fd98-107">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="7fd98-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="7fd98-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="7fd98-108">Summary</span></span>

 <span data-ttu-id="7fd98-109">Ses</span><span class="sxs-lookup"><span data-stu-id="7fd98-109">Members</span></span>                        | <span data-ttu-id="7fd98-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7fd98-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7fd98-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="7fd98-111">Invoke</span></span>](#invoke) | <span data-ttu-id="7fd98-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="7fd98-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7fd98-113">Ses</span><span class="sxs-lookup"><span data-stu-id="7fd98-113">Members</span></span>

#### <span data-ttu-id="7fd98-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="7fd98-114">Invoke</span></span> 

<span data-ttu-id="7fd98-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="7fd98-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7fd98-116">[appel](#invoke)de HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7fd98-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="7fd98-117">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="7fd98-117">There are no event args and the args parameter will be null.</span></span>

