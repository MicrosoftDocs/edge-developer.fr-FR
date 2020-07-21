---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ContainsFullScreenElementChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: b1d0bf7ea5f472d5a1c3682c2cbef564947ee54b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886184"
---
# <span data-ttu-id="55d51-104">0.8.355-interface IWebView2ContainsFullScreenElementChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="55d51-104">0.8.355 - interface IWebView2ContainsFullScreenElementChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ContainsFullScreenElementChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="55d51-105">L’appelant implémente cette méthode pour recevoir les événements ContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="55d51-105">The caller implements this method to receive the ContainsFullScreenElementChanged events.</span></span>

## <span data-ttu-id="55d51-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="55d51-106">Summary</span></span>

 <span data-ttu-id="55d51-107">Ses</span><span class="sxs-lookup"><span data-stu-id="55d51-107">Members</span></span>                        | <span data-ttu-id="55d51-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="55d51-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="55d51-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="55d51-109">Invoke</span></span>](#invoke) | <span data-ttu-id="55d51-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="55d51-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="55d51-111">Il n’existe aucun argument d’événement pour cet événement.</span><span class="sxs-lookup"><span data-stu-id="55d51-111">There are no event args for this event.</span></span>

## <span data-ttu-id="55d51-112">Ses</span><span class="sxs-lookup"><span data-stu-id="55d51-112">Members</span></span>

#### <span data-ttu-id="55d51-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="55d51-113">Invoke</span></span> 

<span data-ttu-id="55d51-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="55d51-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="55d51-115">[appel](#invoke)vers un HRESULT public ([IWebView2WebView5](IWebView2WebView5.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="55d51-115">public HRESULT [Invoke](#invoke)([IWebView2WebView5](IWebView2WebView5.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="55d51-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="55d51-116">There are no event args and the args parameter will be null.</span></span>

