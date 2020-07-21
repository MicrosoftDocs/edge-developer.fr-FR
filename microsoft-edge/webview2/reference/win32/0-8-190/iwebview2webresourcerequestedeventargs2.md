---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 7f710b4da71a4a4e61869f06e5d2a4a95a2d0891
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885708"
---
# <span data-ttu-id="9685d-104">0.8.355-interface IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="9685d-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="9685d-105">Arguments d’événement pour l’événement WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9685d-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9685d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9685d-106">Summary</span></span>

 <span data-ttu-id="9685d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9685d-107">Members</span></span>                        | <span data-ttu-id="9685d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9685d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9685d-109">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9685d-109">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="9685d-110">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9685d-110">The web resource request contexts.</span></span>

## <span data-ttu-id="9685d-111">Ses</span><span class="sxs-lookup"><span data-stu-id="9685d-111">Members</span></span>

#### <span data-ttu-id="9685d-112">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9685d-112">get_ResourceContext</span></span> 

<span data-ttu-id="9685d-113">Les contextes de requête de ressource Web.</span><span class="sxs-lookup"><span data-stu-id="9685d-113">The web resource request contexts.</span></span>

> <span data-ttu-id="9685d-114">[get_ResourceContext](#get_resourcecontext)par le biais du public HRESULT (WEBVIEW2_WEB_RESOURCE_CONTEXT \* Context)</span><span class="sxs-lookup"><span data-stu-id="9685d-114">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

