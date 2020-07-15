---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: e4969ecbb5068f634eeb9a10f4de07277051ef45
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878000"
---
# <span data-ttu-id="16e28-104">0.8.355-interface IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="16e28-104">0.8.355 - interface IWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="16e28-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="16e28-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="16e28-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="16e28-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="16e28-107">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="16e28-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="16e28-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="16e28-108">Summary</span></span>

 <span data-ttu-id="16e28-109">Ses</span><span class="sxs-lookup"><span data-stu-id="16e28-109">Members</span></span>                        | <span data-ttu-id="16e28-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="16e28-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="16e28-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="16e28-111">Invoke</span></span>](#invoke) | <span data-ttu-id="16e28-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="16e28-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="16e28-113">Utilisez la propriété IWebView2WebView. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="16e28-113">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="16e28-114">Ses</span><span class="sxs-lookup"><span data-stu-id="16e28-114">Members</span></span>

#### <span data-ttu-id="16e28-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="16e28-115">Invoke</span></span> 

<span data-ttu-id="16e28-116">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="16e28-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="16e28-117">[appel](#invoke)vers un HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="16e28-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="16e28-118">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="16e28-118">There are no event args and the args parameter will be null.</span></span>

