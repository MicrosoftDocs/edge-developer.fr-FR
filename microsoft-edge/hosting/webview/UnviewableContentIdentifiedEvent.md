---
description: Indique que le WebView tente de télécharger un fichier non pris en charge.
title: Objet UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752012"
---
# <span data-ttu-id="1856e-104">Objet UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="1856e-104">UnviewableContentIdentifiedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="1856e-105">Indique que [WebView](../webview.md) tente d’accéder à un fichier d’un type de contenu non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1856e-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span>  

## <span data-ttu-id="1856e-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1856e-106">Properties</span></span>  

### <span data-ttu-id="1856e-107">Média</span><span class="sxs-lookup"><span data-stu-id="1856e-107">mediaType</span></span>  

<span data-ttu-id="1856e-108">Obtient le type de contenu du contenu non affiché.</span><span class="sxs-lookup"><span data-stu-id="1856e-108">Gets the content type of the unviewable content.</span></span>  

<span data-ttu-id="1856e-109">Cette propriété est en lecture seule</span><span class="sxs-lookup"><span data-stu-id="1856e-109">This property is read-only</span></span>  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### <span data-ttu-id="1856e-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1856e-110">Property value</span></span>  

<span data-ttu-id="1856e-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1856e-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="1856e-112">Referer</span><span class="sxs-lookup"><span data-stu-id="1856e-112">referer</span></span>  

<span data-ttu-id="1856e-113">URI (Uniform Resource Identifier) de la page du [WebView](../webview.md) demandant la navigation.</span><span class="sxs-lookup"><span data-stu-id="1856e-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="1856e-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1856e-114">This property is read-only.</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### <span data-ttu-id="1856e-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1856e-115">Property value</span></span>  

<span data-ttu-id="1856e-116">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1856e-116">Type: **DOMString**</span></span>  

### <span data-ttu-id="1856e-117">uri</span><span class="sxs-lookup"><span data-stu-id="1856e-117">uri</span></span>  

<span data-ttu-id="1856e-118">URI (Uniform Resource Identifier) de la destination de la navigation.</span><span class="sxs-lookup"><span data-stu-id="1856e-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="1856e-119">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1856e-119">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="1856e-120">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1856e-120">Property value</span></span>  

<span data-ttu-id="1856e-121">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1856e-121">Type: **DOMString**</span></span>  
