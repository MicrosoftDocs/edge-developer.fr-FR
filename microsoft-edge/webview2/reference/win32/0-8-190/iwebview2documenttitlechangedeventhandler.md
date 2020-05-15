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
ms.openlocfilehash: 69d8f410c7d9e7c4a8b1dc526babf535a372048f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653496"
---
# <span data-ttu-id="136ea-104">interface IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="136ea-104">interface IWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="136ea-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="136ea-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="136ea-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="136ea-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="136ea-107">L’appelant implémente cette interface pour recevoir des événements DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="136ea-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="136ea-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="136ea-108">Summary</span></span>

 <span data-ttu-id="136ea-109">Ses</span><span class="sxs-lookup"><span data-stu-id="136ea-109">Members</span></span>                        | <span data-ttu-id="136ea-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="136ea-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="136ea-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="136ea-111">Invoke</span></span>](#invoke) | <span data-ttu-id="136ea-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="136ea-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="136ea-113">Utilisez la propriété DocumentTitle pour obtenir le titre modifié.</span><span class="sxs-lookup"><span data-stu-id="136ea-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="136ea-114">Ses</span><span class="sxs-lookup"><span data-stu-id="136ea-114">Members</span></span>

#### <span data-ttu-id="136ea-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="136ea-115">Invoke</span></span> 

<span data-ttu-id="136ea-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="136ea-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="136ea-117">[appel](#invoke)vers un HRESULT public ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="136ea-117">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="136ea-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="136ea-118">There are no event args and the args parameter will be null.</span></span>

