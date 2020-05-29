---
description: Indique que le WebView tente de télécharger un fichier non pris en charge.
title: Objet UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564625"
---
# <span data-ttu-id="cedd3-104">Objet UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="cedd3-104">UnviewableContentIdentifiedEvent object</span></span>

<span data-ttu-id="cedd3-105">Indique que [WebView](../webview.md) tente d’accéder à un fichier d’un type de contenu non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="cedd3-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span> 

## <span data-ttu-id="cedd3-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="cedd3-106">Properties</span></span>

### <span data-ttu-id="cedd3-107">Média</span><span class="sxs-lookup"><span data-stu-id="cedd3-107">mediaType</span></span>

<span data-ttu-id="cedd3-108">Obtient le type de contenu du contenu non affiché.</span><span class="sxs-lookup"><span data-stu-id="cedd3-108">Gets the content type of the unviewable content.</span></span>

<span data-ttu-id="cedd3-109">Cette propriété est en lecture seule</span><span class="sxs-lookup"><span data-stu-id="cedd3-109">This property is read-only</span></span>

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### <span data-ttu-id="cedd3-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="cedd3-110">Property value</span></span>
<span data-ttu-id="cedd3-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="cedd3-111">Type: **DOMString**</span></span>

### <span data-ttu-id="cedd3-112">Referer</span><span class="sxs-lookup"><span data-stu-id="cedd3-112">referer</span></span>

<span data-ttu-id="cedd3-113">URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.</span><span class="sxs-lookup"><span data-stu-id="cedd3-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="cedd3-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cedd3-114">This property is read-only.</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

#### <span data-ttu-id="cedd3-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="cedd3-115">Property value</span></span>
<span data-ttu-id="cedd3-116">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="cedd3-116">Type: **DOMString**</span></span>

### <span data-ttu-id="cedd3-117">uri</span><span class="sxs-lookup"><span data-stu-id="cedd3-117">uri</span></span>

<span data-ttu-id="cedd3-118">URI (Uniform Resource Identifier) de la destination de la navigation.</span><span class="sxs-lookup"><span data-stu-id="cedd3-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="cedd3-119">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="cedd3-119">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="cedd3-120">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="cedd3-120">Property value</span></span>
<span data-ttu-id="cedd3-121">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="cedd3-121">Type: **DOMString**</span></span>
