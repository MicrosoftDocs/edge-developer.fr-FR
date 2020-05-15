---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: f659e6de5cb5bf88593403fad77e56dd1bdcd976
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653619"
---
# <span data-ttu-id="e6bf0-104">interface IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="e6bf0-104">interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="e6bf0-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e6bf0-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="e6bf0-107">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-107">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="e6bf0-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="e6bf0-108">Summary</span></span>

 <span data-ttu-id="e6bf0-109">Ses</span><span class="sxs-lookup"><span data-stu-id="e6bf0-109">Members</span></span>                        | <span data-ttu-id="e6bf0-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e6bf0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e6bf0-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="e6bf0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="e6bf0-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="e6bf0-113">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-113">There are no event args for this event.</span></span>

## <span data-ttu-id="e6bf0-114">Ses</span><span class="sxs-lookup"><span data-stu-id="e6bf0-114">Members</span></span>

#### <span data-ttu-id="e6bf0-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="e6bf0-115">Invoke</span></span> 

<span data-ttu-id="e6bf0-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="e6bf0-117">[appel](#invoke)vers un HRESULT public ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="e6bf0-117">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="e6bf0-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="e6bf0-118">There are no event args and the args parameter will be null.</span></span>

