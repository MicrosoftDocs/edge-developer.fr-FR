---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 237179df5ef704fb88516780696f3a9c10c9a198
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884665"
---
# <span data-ttu-id="1c651-104">0.8.355-interface IWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1c651-104">0.8.355 - interface IWebView2ZoomFactorChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1c651-105">L’appelant implémente cette interface pour recevoir des événements ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="1c651-105">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="1c651-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="1c651-106">Summary</span></span>

 <span data-ttu-id="1c651-107">Ses</span><span class="sxs-lookup"><span data-stu-id="1c651-107">Members</span></span>                        | <span data-ttu-id="1c651-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="1c651-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1c651-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="1c651-109">Invoke</span></span>](#invoke) | <span data-ttu-id="1c651-110">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="1c651-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1c651-111">Utilisez la propriété IWebView2WebView. ZoomFactor pour obtenir le facteur de zoom modifié.</span><span class="sxs-lookup"><span data-stu-id="1c651-111">Use the IWebView2WebView.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="1c651-112">Ses</span><span class="sxs-lookup"><span data-stu-id="1c651-112">Members</span></span>

#### <span data-ttu-id="1c651-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="1c651-113">Invoke</span></span> 

<span data-ttu-id="1c651-114">Appelée pour fournir à l’implémenteur des arguments d’événement pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="1c651-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1c651-115">[appel](#invoke)vers un HRESULT public ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1c651-115">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="1c651-116">Il n’y a pas d’arguments d’événement et le paramètre args a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="1c651-116">There are no event args and the args parameter will be null.</span></span>

