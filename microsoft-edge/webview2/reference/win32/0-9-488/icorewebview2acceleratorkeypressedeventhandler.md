---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 8b0d6a4db4a4af6710df54e42b3cddee061a4040
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880961"
---
# <span data-ttu-id="581ee-104">0.9.515-interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="581ee-104">0.9.515 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="581ee-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="581ee-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="581ee-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="581ee-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="581ee-107">L’appelant implémente cette interface pour recevoir l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="581ee-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="581ee-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="581ee-108">Summary</span></span>

 <span data-ttu-id="581ee-109">Ses</span><span class="sxs-lookup"><span data-stu-id="581ee-109">Members</span></span>                        | <span data-ttu-id="581ee-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="581ee-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="581ee-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="581ee-111">Invoke</span></span>](#invoke) | <span data-ttu-id="581ee-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="581ee-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="581ee-113">Ses</span><span class="sxs-lookup"><span data-stu-id="581ee-113">Members</span></span>

#### <span data-ttu-id="581ee-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="581ee-114">Invoke</span></span> 

<span data-ttu-id="581ee-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="581ee-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="581ee-116">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="581ee-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

