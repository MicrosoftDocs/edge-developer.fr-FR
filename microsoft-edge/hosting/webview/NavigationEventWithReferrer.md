---
description: Contient des informations de renvoi sur la navigation
title: Objet NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752125"
---
# <span data-ttu-id="37070-104">Objet NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="37070-104">NavigationEventWithReferrer object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="37070-105">Objet qui représente un événement déclenché lorsque la navigation est lancée et que la navigation contient un referer.</span><span class="sxs-lookup"><span data-stu-id="37070-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>  

## <span data-ttu-id="37070-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="37070-106">Properties</span></span>  

### <span data-ttu-id="37070-107">Referer</span><span class="sxs-lookup"><span data-stu-id="37070-107">referer</span></span>

<span data-ttu-id="37070-108">URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.</span><span class="sxs-lookup"><span data-stu-id="37070-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="37070-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="37070-109">This property is read-only.</span></span>  

#### <span data-ttu-id="37070-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="37070-110">Property value</span></span>  

<span data-ttu-id="37070-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="37070-111">Type: **DOMString**</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### <span data-ttu-id="37070-112">uri</span><span class="sxs-lookup"><span data-stu-id="37070-112">uri</span></span>  

<span data-ttu-id="37070-113">URI (Uniform Resource Identifier) de la destination de la navigation.</span><span class="sxs-lookup"><span data-stu-id="37070-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="37070-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="37070-114">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="37070-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="37070-115">Property value</span></span>  

<span data-ttu-id="37070-116">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="37070-116">Type: **DOMString**</span></span>  
