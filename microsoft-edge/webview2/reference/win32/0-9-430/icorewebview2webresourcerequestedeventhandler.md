---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: d2b1aa9bbfc15aa44023a43425bb2fc939165cae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880156"
---
# <span data-ttu-id="e4848-104">0.9.430-interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e4848-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e4848-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="e4848-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="e4848-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="e4848-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e4848-107">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="e4848-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="e4848-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e4848-108">Summary</span></span>

 <span data-ttu-id="e4848-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e4848-109">Members</span></span>                        | <span data-ttu-id="e4848-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e4848-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e4848-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e4848-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e4848-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e4848-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e4848-113">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="e4848-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="e4848-114">Ses</span><span class="sxs-lookup"><span data-stu-id="e4848-114">Members</span></span>

#### <span data-ttu-id="e4848-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="e4848-115">Invoke</span></span> 

<span data-ttu-id="e4848-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e4848-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e4848-117">[appel](#invoke)HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e4848-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2WebResourceRequestedEventArgs](ICoreWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

