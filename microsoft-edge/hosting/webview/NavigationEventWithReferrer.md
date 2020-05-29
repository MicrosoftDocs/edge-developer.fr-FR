---
description: Contient des informations de renvoi sur la navigation
title: Objet NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565093"
---
# <span data-ttu-id="327b3-104">Objet NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="327b3-104">NavigationEventWithReferrer object</span></span>

<span data-ttu-id="327b3-105">Objet qui représente un événement déclenché lorsque la navigation est lancée et que la navigation contient un referer.</span><span class="sxs-lookup"><span data-stu-id="327b3-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>

## <span data-ttu-id="327b3-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="327b3-106">Properties</span></span>

### <span data-ttu-id="327b3-107">Referer</span><span class="sxs-lookup"><span data-stu-id="327b3-107">referer</span></span>

<span data-ttu-id="327b3-108">URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.</span><span class="sxs-lookup"><span data-stu-id="327b3-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="327b3-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="327b3-109">This property is read-only.</span></span>

#### <span data-ttu-id="327b3-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="327b3-110">Property value</span></span>
<span data-ttu-id="327b3-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="327b3-111">Type: **DOMString**</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

### <span data-ttu-id="327b3-112">uri</span><span class="sxs-lookup"><span data-stu-id="327b3-112">uri</span></span>

<span data-ttu-id="327b3-113">URI (Uniform Resource Identifier) de la destination de la navigation.</span><span class="sxs-lookup"><span data-stu-id="327b3-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="327b3-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="327b3-114">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="327b3-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="327b3-115">Property value</span></span>
<span data-ttu-id="327b3-116">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="327b3-116">Type: **DOMString**</span></span>
