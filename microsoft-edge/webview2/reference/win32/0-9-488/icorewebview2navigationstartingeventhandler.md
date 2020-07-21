---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2NavigationStartingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 35ca64bcfdae9d82a2f5b00ef69d36f367e22efe
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884056"
---
# <span data-ttu-id="d86ee-104">0.9.515-interface ICoreWebView2NavigationStartingEventHandler</span><span class="sxs-lookup"><span data-stu-id="d86ee-104">0.9.515 - interface ICoreWebView2NavigationStartingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventHandler
  : public IUnknown
```

<span data-ttu-id="d86ee-105">L’appelant implémente cette interface pour recevoir l’événement NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="d86ee-105">The caller implements this interface to receive the NavigationStarting event.</span></span>

## <span data-ttu-id="d86ee-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d86ee-106">Summary</span></span>

 <span data-ttu-id="d86ee-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d86ee-107">Members</span></span>                        | <span data-ttu-id="d86ee-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d86ee-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d86ee-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="d86ee-109">Invoke</span></span>](#invoke) | <span data-ttu-id="d86ee-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d86ee-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="d86ee-111">Ses</span><span class="sxs-lookup"><span data-stu-id="d86ee-111">Members</span></span>

#### <span data-ttu-id="d86ee-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="d86ee-112">Invoke</span></span> 

<span data-ttu-id="d86ee-113">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="d86ee-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="d86ee-114">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="d86ee-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2NavigationStartingEventArgs](icorewebview2navigationstartingeventargs.md) \* args)</span></span>

