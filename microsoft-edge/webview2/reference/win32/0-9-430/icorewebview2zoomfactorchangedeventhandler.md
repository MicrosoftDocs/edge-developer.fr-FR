---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: dd9365fb8fb0215b3090928c8edb59575c6247fe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653596"
---
# <span data-ttu-id="c848c-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c848c-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="c848c-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c848c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c848c-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="c848c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c848c-107">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="c848c-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="c848c-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="c848c-108">Summary</span></span>

 <span data-ttu-id="c848c-109">Ses</span><span class="sxs-lookup"><span data-stu-id="c848c-109">Members</span></span>                        | <span data-ttu-id="c848c-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="c848c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c848c-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="c848c-111">Invoke</span></span>](#invoke) | <span data-ttu-id="c848c-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c848c-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c848c-113">Utilisez la propriété ICoreWebView2Host. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="c848c-113">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="c848c-114">Ses</span><span class="sxs-lookup"><span data-stu-id="c848c-114">Members</span></span>

#### <span data-ttu-id="c848c-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="c848c-115">Invoke</span></span> 

<span data-ttu-id="c848c-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="c848c-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c848c-117">[appel](#invoke)de HRESULT public ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c848c-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="c848c-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="c848c-118">There are no event args and the args parameter will be null.</span></span>

