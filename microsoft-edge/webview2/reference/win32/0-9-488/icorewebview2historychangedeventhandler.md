---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 5c4807a6f1772354f4448b25d49ea7ea86278f57
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880604"
---
# <span data-ttu-id="f3d89-104">0.9.515-interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f3d89-104">0.9.515 - interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f3d89-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f3d89-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f3d89-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="f3d89-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f3d89-107">L’appelant implémente cette interface pour recevoir l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="f3d89-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="f3d89-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f3d89-108">Summary</span></span>

 <span data-ttu-id="f3d89-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f3d89-109">Members</span></span>                        | <span data-ttu-id="f3d89-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f3d89-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f3d89-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f3d89-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f3d89-112">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f3d89-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="f3d89-113">Ses</span><span class="sxs-lookup"><span data-stu-id="f3d89-113">Members</span></span>

#### <span data-ttu-id="f3d89-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f3d89-114">Invoke</span></span> 

<span data-ttu-id="f3d89-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f3d89-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="f3d89-116">[appel](#invoke)vers un HRESULT public ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f3d89-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

