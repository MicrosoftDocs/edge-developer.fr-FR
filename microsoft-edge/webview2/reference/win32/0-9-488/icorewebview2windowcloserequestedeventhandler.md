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
ms.openlocfilehash: 8d464202e224647c02953312810475b2755c530b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698112"
---
# <span data-ttu-id="9112a-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9112a-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="9112a-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="9112a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="9112a-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="9112a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="9112a-107">L’appelant implémente cette interface pour recevoir des événements NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="9112a-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="9112a-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="9112a-108">Summary</span></span>

 <span data-ttu-id="9112a-109">Ses</span><span class="sxs-lookup"><span data-stu-id="9112a-109">Members</span></span>                        | <span data-ttu-id="9112a-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9112a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9112a-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="9112a-111">Invoke</span></span>](#invoke) | <span data-ttu-id="9112a-112">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="9112a-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="9112a-113">Ses</span><span class="sxs-lookup"><span data-stu-id="9112a-113">Members</span></span>

#### <span data-ttu-id="9112a-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="9112a-114">Invoke</span></span> 

<span data-ttu-id="9112a-115">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="9112a-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9112a-116">[appel](#invoke)de HRESULT public ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="9112a-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="9112a-117">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="9112a-117">There are no event args and the args parameter will be null.</span></span>

