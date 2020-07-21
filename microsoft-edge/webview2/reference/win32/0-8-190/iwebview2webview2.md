---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884735"
---
# <span data-ttu-id="b2393-104">0.8.355-interface IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="b2393-104">0.8.355 - interface IWebView2WebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="b2393-105">Fonctionnalités supplémentaires implémentées par l’objet WebView principal.</span><span class="sxs-lookup"><span data-stu-id="b2393-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="b2393-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="b2393-106">Summary</span></span>

 <span data-ttu-id="b2393-107">Ses</span><span class="sxs-lookup"><span data-stu-id="b2393-107">Members</span></span>                        | <span data-ttu-id="b2393-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b2393-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b2393-109">Stop</span><span class="sxs-lookup"><span data-stu-id="b2393-109">Stop</span></span>](#stop) | <span data-ttu-id="b2393-110">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="b2393-110">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="b2393-111">Vous pouvez QueryInterface pour cette interface à partir de l’objet qui implémente [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="b2393-111">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="b2393-112">Pour plus d’informations, consultez l’interface [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="b2393-112">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="b2393-113">Ses</span><span class="sxs-lookup"><span data-stu-id="b2393-113">Members</span></span>

#### <span data-ttu-id="b2393-114">Stop</span><span class="sxs-lookup"><span data-stu-id="b2393-114">Stop</span></span> 

<span data-ttu-id="b2393-115">Arrêtez toutes les navigations et les extractions de ressources en attente.</span><span class="sxs-lookup"><span data-stu-id="b2393-115">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="b2393-116">point d' [arrêt](#stop)public HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="b2393-116">public HRESULT [Stop](#stop)()</span></span>

