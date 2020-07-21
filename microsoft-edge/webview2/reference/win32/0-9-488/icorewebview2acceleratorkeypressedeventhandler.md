---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 13538c0ef14b9517a8a53e00d24ef93819adeb15
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883972"
---
# <span data-ttu-id="9aa63-104">0.9.515-interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9aa63-104">0.9.515 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="9aa63-105">L’appelant implémente cette interface pour recevoir l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="9aa63-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="9aa63-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9aa63-106">Summary</span></span>

 <span data-ttu-id="9aa63-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9aa63-107">Members</span></span>                        | <span data-ttu-id="9aa63-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9aa63-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9aa63-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9aa63-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9aa63-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="9aa63-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9aa63-111">Ses</span><span class="sxs-lookup"><span data-stu-id="9aa63-111">Members</span></span>

#### <span data-ttu-id="9aa63-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="9aa63-112">Invoke</span></span> 

<span data-ttu-id="9aa63-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="9aa63-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9aa63-114">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9aa63-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

