---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 4f2bb4e5077fea7583f7d9f9886923ea1867e1ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883679"
---
# <span data-ttu-id="4f5e8-104">0.9.515-interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="4f5e8-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="4f5e8-105">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="4f5e8-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="4f5e8-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="4f5e8-106">Summary</span></span>

 <span data-ttu-id="4f5e8-107">Ses</span><span class="sxs-lookup"><span data-stu-id="4f5e8-107">Members</span></span>                        | <span data-ttu-id="4f5e8-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4f5e8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4f5e8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="4f5e8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="4f5e8-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4f5e8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="4f5e8-111">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="4f5e8-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="4f5e8-112">Ses</span><span class="sxs-lookup"><span data-stu-id="4f5e8-112">Members</span></span>

#### <span data-ttu-id="4f5e8-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="4f5e8-113">Invoke</span></span> 

<span data-ttu-id="4f5e8-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="4f5e8-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4f5e8-115">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="4f5e8-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

