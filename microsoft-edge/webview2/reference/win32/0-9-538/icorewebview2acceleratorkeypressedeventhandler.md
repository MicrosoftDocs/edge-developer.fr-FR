---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 104291f2bbf285737311a205188a1b549906becf
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011215"
---
# <span data-ttu-id="bd582-104">0.9.579-interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="bd582-104">0.9.579 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="bd582-105">L’appelant implémente cette interface pour recevoir l’événement AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="bd582-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="bd582-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="bd582-106">Summary</span></span>

 <span data-ttu-id="bd582-107">Ses</span><span class="sxs-lookup"><span data-stu-id="bd582-107">Members</span></span>                        | <span data-ttu-id="bd582-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="bd582-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bd582-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="bd582-109">Invoke</span></span>](#invoke) | <span data-ttu-id="bd582-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bd582-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="bd582-111">Ses</span><span class="sxs-lookup"><span data-stu-id="bd582-111">Members</span></span>

#### <span data-ttu-id="bd582-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="bd582-112">Invoke</span></span> 

<span data-ttu-id="bd582-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="bd582-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="bd582-114">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="bd582-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

