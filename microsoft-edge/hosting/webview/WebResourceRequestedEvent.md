---
description: Événement déclenché lors de la tentative de requête HTTP.
title: Objet WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564622"
---
# <span data-ttu-id="03a3f-104">Objet WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="03a3f-104">WebResourceRequestedEvent object</span></span>

<span data-ttu-id="03a3f-105">Événement déclenché lors de la tentative de requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="03a3f-105">An event that is fired when an HTTP request is made.</span></span>

## <span data-ttu-id="03a3f-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03a3f-106">Properties</span></span>

### <span data-ttu-id="03a3f-107">args</span><span class="sxs-lookup"><span data-stu-id="03a3f-107">args</span></span>

<span data-ttu-id="03a3f-108">Informations sur la demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="03a3f-108">Information about the resource request.</span></span> <span data-ttu-id="03a3f-109">Il s’agit d’un [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span><span class="sxs-lookup"><span data-stu-id="03a3f-109">This is a [Windows.Web.UI.WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).</span></span>

<span data-ttu-id="03a3f-110">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="03a3f-110">This property is read-only.</span></span>

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### <span data-ttu-id="03a3f-111">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="03a3f-111">Property value</span></span>
<span data-ttu-id="03a3f-112">Tapez: **tout**</span><span class="sxs-lookup"><span data-stu-id="03a3f-112">Type: **any**</span></span>

