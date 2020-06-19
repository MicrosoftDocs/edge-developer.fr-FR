---
description: Événement déclenché lors de la tentative de requête HTTP.
title: Objet WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 3d2bb54cc5d60aec5391f0e3fdd427c8ba8a3dab
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751981"
---
# <span data-ttu-id="6da64-104">Objet WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="6da64-104">WebResourceRequestedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="6da64-105">Événement déclenché lors de la tentative de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="6da64-105">An event that is fired when an HTTP request is made.</span></span>  

## <span data-ttu-id="6da64-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6da64-106">Properties</span></span>  

### <span data-ttu-id="6da64-107">args</span><span class="sxs-lookup"><span data-stu-id="6da64-107">args</span></span>  

<span data-ttu-id="6da64-108">Informations sur la demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="6da64-108">Information about the resource request.</span></span>  <span data-ttu-id="6da64-109">Il s’agit d’un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="6da64-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>  

<span data-ttu-id="6da64-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="6da64-110">This property is read-only.</span></span>  

```javascript
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```  

#### <span data-ttu-id="6da64-111">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="6da64-111">Property value</span></span>  

<span data-ttu-id="6da64-112">Tapez: **tout**</span><span class="sxs-lookup"><span data-stu-id="6da64-112">Type: **any**</span></span>  
