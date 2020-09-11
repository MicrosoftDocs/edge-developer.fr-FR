---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ContainsFullScreenElementChangedEventHandler
ms.openlocfilehash: e1c51ee30a7b61d5a5638adb4130b1add3bddb23
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010557"
---
# <span data-ttu-id="795b6-104">0.9.579-interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="795b6-104">0.9.579 - interface ICoreWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="795b6-105">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="795b6-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="795b6-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="795b6-106">Summary</span></span>

 <span data-ttu-id="795b6-107">Ses</span><span class="sxs-lookup"><span data-stu-id="795b6-107">Members</span></span>                        | <span data-ttu-id="795b6-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="795b6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="795b6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="795b6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="795b6-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="795b6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="795b6-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="795b6-111">There are no event args for this event.</span></span>

## <span data-ttu-id="795b6-112">Ses</span><span class="sxs-lookup"><span data-stu-id="795b6-112">Members</span></span>

#### <span data-ttu-id="795b6-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="795b6-113">Invoke</span></span> 

<span data-ttu-id="795b6-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="795b6-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="795b6-115">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="795b6-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="795b6-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="795b6-116">There are no event args and the args parameter will be null.</span></span>

