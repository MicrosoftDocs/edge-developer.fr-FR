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
ms.openlocfilehash: 2f3effd612303d1532c7220d566791a800753b37
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653296"
---
# <span data-ttu-id="ac00e-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ac00e-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="ac00e-105">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="ac00e-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="ac00e-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="ac00e-106">Summary</span></span>

 <span data-ttu-id="ac00e-107">Ses</span><span class="sxs-lookup"><span data-stu-id="ac00e-107">Members</span></span>                        | <span data-ttu-id="ac00e-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ac00e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac00e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ac00e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ac00e-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ac00e-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="ac00e-111">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="ac00e-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="ac00e-112">Ses</span><span class="sxs-lookup"><span data-stu-id="ac00e-112">Members</span></span>

#### <span data-ttu-id="ac00e-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="ac00e-113">Invoke</span></span> 

<span data-ttu-id="ac00e-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="ac00e-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ac00e-115">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ac00e-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

