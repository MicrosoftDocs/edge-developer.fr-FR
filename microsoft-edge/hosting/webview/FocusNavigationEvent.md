---
description: Objet dispatché d’un événement de focus contenant la raison et l’emplacement de la navigation
title: Objet FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565110"
---
# <span data-ttu-id="3db37-104">Objet FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="3db37-104">FocusNavigationEvent object</span></span>

<span data-ttu-id="3db37-105">Objet distribué de [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) contenant l' [**NavigationReason**](#navigationreason) et l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="3db37-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span> 

## <span data-ttu-id="3db37-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3db37-106">Methods</span></span>

### <span data-ttu-id="3db37-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="3db37-107">requestFocus</span></span>

<span data-ttu-id="3db37-108">Appelée pour déplacer le focus entre l’application et le WebView.</span><span class="sxs-lookup"><span data-stu-id="3db37-108">Called to move focus from the app to the webview.</span></span>

### <span data-ttu-id="3db37-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="3db37-109">Parameters</span></span>

<span data-ttu-id="3db37-110">Cette méthode n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="3db37-110">This method does not have parameters.</span></span>

### <span data-ttu-id="3db37-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3db37-111">Return value</span></span>

<span data-ttu-id="3db37-112">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="3db37-112">This method does not return a value.</span></span>

## <span data-ttu-id="3db37-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3db37-113">Properties</span></span>
    
### <span data-ttu-id="3db37-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="3db37-114">navigationReason</span></span>

<span data-ttu-id="3db37-115">Type **NavigationReason**: «gauche», «haut», «droite» ou «bas».</span><span class="sxs-lookup"><span data-stu-id="3db37-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span> 

<span data-ttu-id="3db37-116">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3db37-116">This property is read-only.</span></span>

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### <span data-ttu-id="3db37-117">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="3db37-117">Property value</span></span>
<span data-ttu-id="3db37-118">Type: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="3db37-118">Type: **NavigationReason**</span></span>

### <span data-ttu-id="3db37-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="3db37-119">originHeight</span></span>

<span data-ttu-id="3db37-120">Emplacement de la hauteur d’origine de l’élément à donner au focus.</span><span class="sxs-lookup"><span data-stu-id="3db37-120">The origin height location of the element to be given focus.</span></span>

<span data-ttu-id="3db37-121">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3db37-121">This property is read-only.</span></span>

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### <span data-ttu-id="3db37-122">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="3db37-122">Property value</span></span>
<span data-ttu-id="3db37-123">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="3db37-123">Type: **float**</span></span>

### <span data-ttu-id="3db37-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="3db37-124">originLeft</span></span>

<span data-ttu-id="3db37-125">Emplacement de gauche de l’élément à donner au focus.</span><span class="sxs-lookup"><span data-stu-id="3db37-125">The origin left location of the element to be given focus.</span></span>

<span data-ttu-id="3db37-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3db37-126">This property is read-only.</span></span>

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### <span data-ttu-id="3db37-127">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="3db37-127">Property value</span></span>
<span data-ttu-id="3db37-128">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="3db37-128">Type: **float**</span></span>

### <span data-ttu-id="3db37-129">originTop</span><span class="sxs-lookup"><span data-stu-id="3db37-129">originTop</span></span>

<span data-ttu-id="3db37-130">Emplacement supérieur d’origine de l’élément à donner le focus.</span><span class="sxs-lookup"><span data-stu-id="3db37-130">The origin top location of the element to be given focus.</span></span>

<span data-ttu-id="3db37-131">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3db37-131">This property is read-only.</span></span>

```js
var originTop = FocusNavigationEvent.originTop;
```

#### <span data-ttu-id="3db37-132">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="3db37-132">Property value</span></span>
<span data-ttu-id="3db37-133">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="3db37-133">Type: **float**</span></span>

### <span data-ttu-id="3db37-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="3db37-134">originWidth</span></span>

<span data-ttu-id="3db37-135">La largeur d’origine de l’élément à donner au focus.</span><span class="sxs-lookup"><span data-stu-id="3db37-135">The origin width location of the element to be given focus.</span></span>

<span data-ttu-id="3db37-136">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="3db37-136">This property is read-only.</span></span>

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### <span data-ttu-id="3db37-137">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="3db37-137">Property value</span></span>
<span data-ttu-id="3db37-138">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="3db37-138">Type: **float**</span></span>

