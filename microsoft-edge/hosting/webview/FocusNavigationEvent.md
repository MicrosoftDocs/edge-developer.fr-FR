---
description: Objet dispatché d’un événement de focus contenant la raison et l’emplacement de la navigation
title: Objet FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752163"
---
# <span data-ttu-id="aa62c-104">Objet FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="aa62c-104">FocusNavigationEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="aa62c-105">Objet distribué de [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) contenant l' [**NavigationReason**](#navigationreason) et l’emplacement.</span><span class="sxs-lookup"><span data-stu-id="aa62c-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span>  

## <span data-ttu-id="aa62c-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="aa62c-106">Methods</span></span>  

### <span data-ttu-id="aa62c-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="aa62c-107">requestFocus</span></span>  

<span data-ttu-id="aa62c-108">Appelée pour déplacer le focus entre l’application et le WebView.</span><span class="sxs-lookup"><span data-stu-id="aa62c-108">Called to move focus from the app to the webview.</span></span>  

### <span data-ttu-id="aa62c-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="aa62c-109">Parameters</span></span>  

<span data-ttu-id="aa62c-110">Cette méthode n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="aa62c-110">This method does not have parameters.</span></span>  

### <span data-ttu-id="aa62c-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aa62c-111">Return value</span></span>  

<span data-ttu-id="aa62c-112">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="aa62c-112">This method does not return a value.</span></span>  

## <span data-ttu-id="aa62c-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="aa62c-113">Properties</span></span>  

### <span data-ttu-id="aa62c-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="aa62c-114">navigationReason</span></span>  

<span data-ttu-id="aa62c-115">Type **NavigationReason**: «gauche», «haut», «droite» ou «bas».</span><span class="sxs-lookup"><span data-stu-id="aa62c-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span>  

<span data-ttu-id="aa62c-116">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aa62c-116">This property is read-only.</span></span>  

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### <span data-ttu-id="aa62c-117">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="aa62c-117">Property value</span></span>  

<span data-ttu-id="aa62c-118">Type: **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="aa62c-118">Type: **NavigationReason**</span></span>  

### <span data-ttu-id="aa62c-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="aa62c-119">originHeight</span></span>  

<span data-ttu-id="aa62c-120">Emplacement de la hauteur d’origine de l’élément à donner au focus.</span><span class="sxs-lookup"><span data-stu-id="aa62c-120">The origin height location of the element to be given focus.</span></span>  

<span data-ttu-id="aa62c-121">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aa62c-121">This property is read-only.</span></span>  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### <span data-ttu-id="aa62c-122">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="aa62c-122">Property value</span></span>  

<span data-ttu-id="aa62c-123">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="aa62c-123">Type: **float**</span></span>  

### <span data-ttu-id="aa62c-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="aa62c-124">originLeft</span></span>  

<span data-ttu-id="aa62c-125">Emplacement de gauche de l’élément à donner au focus.</span><span class="sxs-lookup"><span data-stu-id="aa62c-125">The origin left location of the element to be given focus.</span></span>  

<span data-ttu-id="aa62c-126">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aa62c-126">This property is read-only.</span></span>  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### <span data-ttu-id="aa62c-127">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="aa62c-127">Property value</span></span>  

<span data-ttu-id="aa62c-128">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="aa62c-128">Type: **float**</span></span>  

### <span data-ttu-id="aa62c-129">originTop</span><span class="sxs-lookup"><span data-stu-id="aa62c-129">originTop</span></span>  

<span data-ttu-id="aa62c-130">Emplacement supérieur d’origine de l’élément à donner le focus.</span><span class="sxs-lookup"><span data-stu-id="aa62c-130">The origin top location of the element to be given focus.</span></span>  

<span data-ttu-id="aa62c-131">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aa62c-131">This property is read-only.</span></span>  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### <span data-ttu-id="aa62c-132">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="aa62c-132">Property value</span></span>  

<span data-ttu-id="aa62c-133">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="aa62c-133">Type: **float**</span></span>  

### <span data-ttu-id="aa62c-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="aa62c-134">originWidth</span></span>  

<span data-ttu-id="aa62c-135">La largeur d’origine de l’élément à donner au focus.</span><span class="sxs-lookup"><span data-stu-id="aa62c-135">The origin width location of the element to be given focus.</span></span>  

<span data-ttu-id="aa62c-136">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="aa62c-136">This property is read-only.</span></span>  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### <span data-ttu-id="aa62c-137">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="aa62c-137">Property value</span></span>  

<span data-ttu-id="aa62c-138">Type: **float**</span><span class="sxs-lookup"><span data-stu-id="aa62c-138">Type: **float**</span></span>  
