---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a12d8f08d16597b2201404931c2cd9edea8b3dbc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881185"
---
# <span data-ttu-id="38e2d-104">0.9.430-interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="38e2d-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="38e2d-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="38e2d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="38e2d-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="38e2d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="38e2d-107">L’appelant implémente cette interface pour recevoir l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="38e2d-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="38e2d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="38e2d-108">Summary</span></span>

 <span data-ttu-id="38e2d-109">Ses</span><span class="sxs-lookup"><span data-stu-id="38e2d-109">Members</span></span>                        | <span data-ttu-id="38e2d-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="38e2d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="38e2d-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="38e2d-111">Invoke</span></span>](#invoke) | <span data-ttu-id="38e2d-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="38e2d-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="38e2d-113">Ses</span><span class="sxs-lookup"><span data-stu-id="38e2d-113">Members</span></span>

#### <span data-ttu-id="38e2d-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="38e2d-114">Invoke</span></span> 

<span data-ttu-id="38e2d-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="38e2d-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="38e2d-116">[appel](#invoke)HRESULT public ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="38e2d-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

