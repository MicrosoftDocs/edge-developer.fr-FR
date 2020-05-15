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
ms.openlocfilehash: 8fd3533d8f479866989f719be6e48c437fae4ddb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653605"
---
# <span data-ttu-id="f9c76-104">interface ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f9c76-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="f9c76-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f9c76-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f9c76-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="f9c76-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="f9c76-107">L’appelant implémente cette interface pour recevoir l’événement HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="f9c76-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="f9c76-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="f9c76-108">Summary</span></span>

 <span data-ttu-id="f9c76-109">Ses</span><span class="sxs-lookup"><span data-stu-id="f9c76-109">Members</span></span>                        | <span data-ttu-id="f9c76-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f9c76-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f9c76-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="f9c76-111">Invoke</span></span>](#invoke) | <span data-ttu-id="f9c76-112">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f9c76-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="f9c76-113">Ses</span><span class="sxs-lookup"><span data-stu-id="f9c76-113">Members</span></span>

#### <span data-ttu-id="f9c76-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="f9c76-114">Invoke</span></span> 

<span data-ttu-id="f9c76-115">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="f9c76-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="f9c76-116">[appel](#invoke)vers un HRESULT public ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="f9c76-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>

