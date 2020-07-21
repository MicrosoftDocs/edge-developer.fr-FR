---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 70ecc1898f9a72656f12b912d103116c381d4218
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885673"
---
# <span data-ttu-id="893b0-104">0.8.355-interface IWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="893b0-104">0.8.355 - interface IWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="893b0-105">Se déclenche quand une requête HTTP est effectuée dans le WebView.</span><span class="sxs-lookup"><span data-stu-id="893b0-105">Fires when an HTTP request is made in the webview.</span></span>

## <span data-ttu-id="893b0-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="893b0-106">Summary</span></span>

 <span data-ttu-id="893b0-107">Ses</span><span class="sxs-lookup"><span data-stu-id="893b0-107">Members</span></span>                        | <span data-ttu-id="893b0-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="893b0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="893b0-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="893b0-109">Invoke</span></span>](#invoke) | <span data-ttu-id="893b0-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="893b0-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="893b0-111">L’hôte peut remplacer les requêtes, en-têtes de réponse et au contenu de la réponse.</span><span class="sxs-lookup"><span data-stu-id="893b0-111">The host can override request, response headers and response content.</span></span>

## <span data-ttu-id="893b0-112">Ses</span><span class="sxs-lookup"><span data-stu-id="893b0-112">Members</span></span>

#### <span data-ttu-id="893b0-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="893b0-113">Invoke</span></span> 

<span data-ttu-id="893b0-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="893b0-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="893b0-115">[appel](#invoke)HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="893b0-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2WebResourceRequestedEventArgs](IWebView2WebResourceRequestedEventArgs.md) \* args)</span></span>

