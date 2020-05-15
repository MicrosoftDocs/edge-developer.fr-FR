---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: f9dcfa996058f4499daff03d8cad033ac61db4c9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653518"
---
# <span data-ttu-id="5f517-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5f517-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="5f517-105">L’appelant implémente cette méthode pour recevoir l’événement MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="5f517-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="5f517-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="5f517-106">Summary</span></span>

 <span data-ttu-id="5f517-107">Ses</span><span class="sxs-lookup"><span data-stu-id="5f517-107">Members</span></span>                        | <span data-ttu-id="5f517-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="5f517-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5f517-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5f517-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5f517-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="5f517-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="5f517-111">Ses</span><span class="sxs-lookup"><span data-stu-id="5f517-111">Members</span></span>

#### <span data-ttu-id="5f517-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5f517-112">Invoke</span></span> 

<span data-ttu-id="5f517-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="5f517-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5f517-114">[appel](#invoke)HRESULT public ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5f517-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

