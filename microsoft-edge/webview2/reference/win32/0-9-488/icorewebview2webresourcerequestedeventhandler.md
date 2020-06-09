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
ms.openlocfilehash: 622a7e93912a3380cc0d7dabae9293734cd3fcfa
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697937"
---
# <span data-ttu-id="e9d42-104">interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e9d42-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e9d42-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e9d42-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e9d42-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="e9d42-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="e9d42-107">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="e9d42-107">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="e9d42-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e9d42-108">Summary</span></span>

 <span data-ttu-id="e9d42-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e9d42-109">Members</span></span>                        | <span data-ttu-id="e9d42-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e9d42-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e9d42-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9d42-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e9d42-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e9d42-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e9d42-113">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="e9d42-113">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="e9d42-114">Ses</span><span class="sxs-lookup"><span data-stu-id="e9d42-114">Members</span></span>

#### <span data-ttu-id="e9d42-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="e9d42-115">Invoke</span></span> 

<span data-ttu-id="e9d42-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e9d42-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e9d42-117">[appel](#invoke)HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="e9d42-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

