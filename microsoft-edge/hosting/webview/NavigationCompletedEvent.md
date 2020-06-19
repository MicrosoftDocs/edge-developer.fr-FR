---
description: Contient des informations sur la navigation complète de WebView
title: Objet NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752136"
---
# <span data-ttu-id="42a5e-104">Objet NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="42a5e-104">NavigationCompletedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="42a5e-105">Objet qui représente un événement déclenché lorsque le [WebView](../webview.md) a fini de charger le contenu actuel ou en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="42a5e-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>  

## <span data-ttu-id="42a5e-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="42a5e-106">Properties</span></span>  

### <span data-ttu-id="42a5e-107">uri</span><span class="sxs-lookup"><span data-stu-id="42a5e-107">uri</span></span>  

<span data-ttu-id="42a5e-108">URI (Uniform Resource Identifier) de la navigation.</span><span class="sxs-lookup"><span data-stu-id="42a5e-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>  

<span data-ttu-id="42a5e-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="42a5e-109">This property is read-only.</span></span>  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### <span data-ttu-id="42a5e-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="42a5e-110">Property value</span></span>  

<span data-ttu-id="42a5e-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="42a5e-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="42a5e-112">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="42a5e-112">isSuccess</span></span>  

<span data-ttu-id="42a5e-113">Obtient une valeur qui indique si la navigation s’est déroulée correctement.</span><span class="sxs-lookup"><span data-stu-id="42a5e-113">Gets a value that indicates whether the navigation completed successfully.</span></span>  

<span data-ttu-id="42a5e-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="42a5e-114">This property is read-only.</span></span>  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### <span data-ttu-id="42a5e-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="42a5e-115">Property value</span></span>  

<span data-ttu-id="42a5e-116">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="42a5e-116">Type: **Boolean**</span></span>  

### <span data-ttu-id="42a5e-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="42a5e-117">webErrorStatus</span></span>  

<span data-ttu-id="42a5e-118">Si la navigation a échoué, obtient une valeur qui indique pourquoi.</span><span class="sxs-lookup"><span data-stu-id="42a5e-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>  

<span data-ttu-id="42a5e-119">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="42a5e-119">This property is read-only.</span></span>  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### <span data-ttu-id="42a5e-120">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="42a5e-120">Property value</span></span>  

<span data-ttu-id="42a5e-121">Type: **longue non signée**</span><span class="sxs-lookup"><span data-stu-id="42a5e-121">Type: **unsigned long**</span></span>  
