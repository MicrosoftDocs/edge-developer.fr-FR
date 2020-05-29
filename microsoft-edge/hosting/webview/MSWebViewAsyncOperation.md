---
description: Indique si l’opération est réussie ou a échoué.
title: Objet MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: ebb89c0fc645ebcd97357af10af2be650d8218b9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565103"
---
# <span data-ttu-id="510b9-104">Objet MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="510b9-104">MSWebViewAsyncOperation object</span></span>

<span data-ttu-id="510b9-105">Indique si l’opération est réussie ou a échoué.</span><span class="sxs-lookup"><span data-stu-id="510b9-105">Exposes whether the operation completed successfully or failed.</span></span> 

## <span data-ttu-id="510b9-106">Événements</span><span class="sxs-lookup"><span data-stu-id="510b9-106">Events</span></span>

### <span data-ttu-id="510b9-107">achever</span><span class="sxs-lookup"><span data-stu-id="510b9-107">complete</span></span>

<span data-ttu-id="510b9-108">Indique que l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="510b9-108">Indicates that the operation completed.</span></span> 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### <span data-ttu-id="510b9-109">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="510b9-109">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="510b9-110">Interface</span><span class="sxs-lookup"><span data-stu-id="510b9-110">Interface</span></span>** | **<span data-ttu-id="510b9-111">Événement</span><span class="sxs-lookup"><span data-stu-id="510b9-111">Event</span></span>**
|**<span data-ttu-id="510b9-112">Synchrone</span><span class="sxs-lookup"><span data-stu-id="510b9-112">Synchronous</span></span>** |<span data-ttu-id="510b9-113">Oui</span><span class="sxs-lookup"><span data-stu-id="510b9-113">Yes</span></span> |    
|**<span data-ttu-id="510b9-114">BD</span><span class="sxs-lookup"><span data-stu-id="510b9-114">Bubbles</span></span>**     |<span data-ttu-id="510b9-115">Non</span><span class="sxs-lookup"><span data-stu-id="510b9-115">No</span></span> |   
|**<span data-ttu-id="510b9-116">Annulable</span><span class="sxs-lookup"><span data-stu-id="510b9-116">Cancelable</span></span>**  |<span data-ttu-id="510b9-117">Non</span><span class="sxs-lookup"><span data-stu-id="510b9-117">No</span></span> |        


### <span data-ttu-id="510b9-118">erreur</span><span class="sxs-lookup"><span data-stu-id="510b9-118">error</span></span>

<span data-ttu-id="510b9-119">Indique qu’il y a eu une erreur de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="510b9-119">Indicates that there was an error with the operation.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### <span data-ttu-id="510b9-120">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="510b9-120">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="510b9-121">Interface</span><span class="sxs-lookup"><span data-stu-id="510b9-121">Interface</span></span>** | **<span data-ttu-id="510b9-122">Événement</span><span class="sxs-lookup"><span data-stu-id="510b9-122">Event</span></span>**
|**<span data-ttu-id="510b9-123">Synchrone</span><span class="sxs-lookup"><span data-stu-id="510b9-123">Synchronous</span></span>** |<span data-ttu-id="510b9-124">Oui</span><span class="sxs-lookup"><span data-stu-id="510b9-124">Yes</span></span> |    
|**<span data-ttu-id="510b9-125">BD</span><span class="sxs-lookup"><span data-stu-id="510b9-125">Bubbles</span></span>**     |<span data-ttu-id="510b9-126">Non</span><span class="sxs-lookup"><span data-stu-id="510b9-126">No</span></span> |   
|**<span data-ttu-id="510b9-127">Annulable</span><span class="sxs-lookup"><span data-stu-id="510b9-127">Cancelable</span></span>**  |<span data-ttu-id="510b9-128">Non</span><span class="sxs-lookup"><span data-stu-id="510b9-128">No</span></span> |            


## <span data-ttu-id="510b9-129">Méthodes</span><span class="sxs-lookup"><span data-stu-id="510b9-129">Methods</span></span>

### <span data-ttu-id="510b9-130">start</span><span class="sxs-lookup"><span data-stu-id="510b9-130">start</span></span>

<span data-ttu-id="510b9-131">Appelée pour lancer la tâche asynchrone.</span><span class="sxs-lookup"><span data-stu-id="510b9-131">Called to start the async task.</span></span> 

```js
MSWebViewAsyncOperation.start();
```

### <span data-ttu-id="510b9-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="510b9-132">Parameters</span></span>

<span data-ttu-id="510b9-133">Cette méthode n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="510b9-133">This method does not have parameters.</span></span>

### <span data-ttu-id="510b9-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="510b9-134">Return value</span></span>

<span data-ttu-id="510b9-135">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="510b9-135">This method does not return a value.</span></span>

## <span data-ttu-id="510b9-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="510b9-136">Properties</span></span>

### <span data-ttu-id="510b9-137">erreur</span><span class="sxs-lookup"><span data-stu-id="510b9-137">error</span></span>

<span data-ttu-id="510b9-138">Erreur qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="510b9-138">The error that occured.</span></span>

<span data-ttu-id="510b9-139">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="510b9-139">This property is read-only.</span></span>

```js
var error = MSWebViewAsyncOperation.error;
```

#### <span data-ttu-id="510b9-140">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="510b9-140">Property value</span></span>
<span data-ttu-id="510b9-141">Type: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="510b9-141">Type: **DOMError**</span></span>

### <span data-ttu-id="510b9-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="510b9-142">oncomplete</span></span>

<span data-ttu-id="510b9-143">Le gestionnaire d’événements **complet** .</span><span class="sxs-lookup"><span data-stu-id="510b9-143">The **complete** event handler.</span></span> 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### <span data-ttu-id="510b9-144">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="510b9-144">Property value</span></span>
<span data-ttu-id="510b9-145">Type: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="510b9-145">Type: **EventHandler**</span></span>

### <span data-ttu-id="510b9-146">erreur</span><span class="sxs-lookup"><span data-stu-id="510b9-146">onerror</span></span>

<span data-ttu-id="510b9-147">Le gestionnaire d’événements d' **erreur** .</span><span class="sxs-lookup"><span data-stu-id="510b9-147">The **error** event handler.</span></span> 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### <span data-ttu-id="510b9-148">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="510b9-148">Property value</span></span>
<span data-ttu-id="510b9-149">Type: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="510b9-149">Type: **EventHandler**</span></span>

### <span data-ttu-id="510b9-150">readyState</span><span class="sxs-lookup"><span data-stu-id="510b9-150">readyState</span></span>

<span data-ttu-id="510b9-151">Décrit l’état prêt de l’objet.</span><span class="sxs-lookup"><span data-stu-id="510b9-151">Describes the ready state of the object.</span></span>

<span data-ttu-id="510b9-152">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="510b9-152">This property is read-only.</span></span>

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### <span data-ttu-id="510b9-153">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="510b9-153">Property value</span></span>
<span data-ttu-id="510b9-154">Type: **courte non signée**</span><span class="sxs-lookup"><span data-stu-id="510b9-154">Type: **unsigned short**</span></span>

### <span data-ttu-id="510b9-155">provoqué</span><span class="sxs-lookup"><span data-stu-id="510b9-155">result</span></span>

<span data-ttu-id="510b9-156">Résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="510b9-156">The result of the operation.</span></span>

<span data-ttu-id="510b9-157">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="510b9-157">This property is read-only.</span></span>

```js
var result = MSWebViewAsyncOperation.result;
```

#### <span data-ttu-id="510b9-158">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="510b9-158">Property value</span></span>
<span data-ttu-id="510b9-159">Tapez: tout</span><span class="sxs-lookup"><span data-stu-id="510b9-159">Type: any</span></span>

### <span data-ttu-id="510b9-160">target</span><span class="sxs-lookup"><span data-stu-id="510b9-160">target</span></span>

<span data-ttu-id="510b9-161">La cible de l’opération.</span><span class="sxs-lookup"><span data-stu-id="510b9-161">The target of the operation.</span></span> 

<span data-ttu-id="510b9-162">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="510b9-162">This property is read-only.</span></span>

```js
var target = MSWebViewAsyncOperation.target;
```

#### <span data-ttu-id="510b9-163">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="510b9-163">Property value</span></span>
<span data-ttu-id="510b9-164">Type: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="510b9-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>

### <span data-ttu-id="510b9-165">type</span><span class="sxs-lookup"><span data-stu-id="510b9-165">type</span></span>

<span data-ttu-id="510b9-166">Type de l’opération.</span><span class="sxs-lookup"><span data-stu-id="510b9-166">The type of the operation.</span></span>

<span data-ttu-id="510b9-167">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="510b9-167">This property is read-only.</span></span>

```js
var type = MSWebViewAsyncOperation.type;
```

#### <span data-ttu-id="510b9-168">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="510b9-168">Property value</span></span>
<span data-ttu-id="510b9-169">Type: **courte non signée**</span><span class="sxs-lookup"><span data-stu-id="510b9-169">Type: **unsigned short**</span></span>
