---
description: Indique si l’opération est réussie ou a échoué.
title: Objet MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: d6e03af2a0205938f19120076aa0ad622539d7e5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752122"
---
# <span data-ttu-id="08698-104">Objet MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="08698-104">MSWebViewAsyncOperation object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="08698-105">Indique si l’opération est réussie ou a échoué.</span><span class="sxs-lookup"><span data-stu-id="08698-105">Exposes whether the operation completed successfully or failed.</span></span>  

## <span data-ttu-id="08698-106">Événements</span><span class="sxs-lookup"><span data-stu-id="08698-106">Events</span></span>  

### <span data-ttu-id="08698-107">achever</span><span class="sxs-lookup"><span data-stu-id="08698-107">complete</span></span>  

<span data-ttu-id="08698-108">Indique que l’opération est terminée.</span><span class="sxs-lookup"><span data-stu-id="08698-108">Indicates that the operation completed.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### <span data-ttu-id="08698-109">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="08698-109">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="08698-110">Interface</span><span class="sxs-lookup"><span data-stu-id="08698-110">Interface</span></span>** | **<span data-ttu-id="08698-111">Événement</span><span class="sxs-lookup"><span data-stu-id="08698-111">Event</span></span>** |  
| **<span data-ttu-id="08698-112">Synchrone</span><span class="sxs-lookup"><span data-stu-id="08698-112">Synchronous</span></span>** |<span data-ttu-id="08698-113">Oui</span><span class="sxs-lookup"><span data-stu-id="08698-113">Yes</span></span> |  
| **<span data-ttu-id="08698-114">BD</span><span class="sxs-lookup"><span data-stu-id="08698-114">Bubbles</span></span>** |<span data-ttu-id="08698-115">Non</span><span class="sxs-lookup"><span data-stu-id="08698-115">No</span></span> |   
| **<span data-ttu-id="08698-116">Annulable</span><span class="sxs-lookup"><span data-stu-id="08698-116">Cancelable</span></span>** |<span data-ttu-id="08698-117">Non</span><span class="sxs-lookup"><span data-stu-id="08698-117">No</span></span> |  

### <span data-ttu-id="08698-118">erreur</span><span class="sxs-lookup"><span data-stu-id="08698-118">error</span></span>  

<span data-ttu-id="08698-119">Indique qu’il y a eu une erreur de fonctionnement.</span><span class="sxs-lookup"><span data-stu-id="08698-119">Indicates that there was an error with the operation.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### <span data-ttu-id="08698-120">Informations sur l’événement</span><span class="sxs-lookup"><span data-stu-id="08698-120">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="08698-121">Interface</span><span class="sxs-lookup"><span data-stu-id="08698-121">Interface</span></span>** | **<span data-ttu-id="08698-122">Événement</span><span class="sxs-lookup"><span data-stu-id="08698-122">Event</span></span>** |  
| **<span data-ttu-id="08698-123">Synchrone</span><span class="sxs-lookup"><span data-stu-id="08698-123">Synchronous</span></span>** | <span data-ttu-id="08698-124">Oui</span><span class="sxs-lookup"><span data-stu-id="08698-124">Yes</span></span> |  
| **<span data-ttu-id="08698-125">BD</span><span class="sxs-lookup"><span data-stu-id="08698-125">Bubbles</span></span>** | <span data-ttu-id="08698-126">Non</span><span class="sxs-lookup"><span data-stu-id="08698-126">No</span></span> |  
| **<span data-ttu-id="08698-127">Annulable</span><span class="sxs-lookup"><span data-stu-id="08698-127">Cancelable</span></span>** | <span data-ttu-id="08698-128">Non</span><span class="sxs-lookup"><span data-stu-id="08698-128">No</span></span> |  

## <span data-ttu-id="08698-129">Méthodes</span><span class="sxs-lookup"><span data-stu-id="08698-129">Methods</span></span>  

### <span data-ttu-id="08698-130">start</span><span class="sxs-lookup"><span data-stu-id="08698-130">start</span></span>  

<span data-ttu-id="08698-131">Appelée pour lancer la tâche asynchrone.</span><span class="sxs-lookup"><span data-stu-id="08698-131">Called to start the async task.</span></span>  

```javascript
MSWebViewAsyncOperation.start();
```  

### <span data-ttu-id="08698-132">Parameters</span><span class="sxs-lookup"><span data-stu-id="08698-132">Parameters</span></span>  

<span data-ttu-id="08698-133">Cette méthode n’a pas de paramètres.</span><span class="sxs-lookup"><span data-stu-id="08698-133">This method does not have parameters.</span></span>  

### <span data-ttu-id="08698-134">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="08698-134">Return value</span></span>  

<span data-ttu-id="08698-135">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="08698-135">This method does not return a value.</span></span>  

## <span data-ttu-id="08698-136">Propriétés</span><span class="sxs-lookup"><span data-stu-id="08698-136">Properties</span></span>  

### <span data-ttu-id="08698-137">erreur</span><span class="sxs-lookup"><span data-stu-id="08698-137">error</span></span>  

<span data-ttu-id="08698-138">Erreur qui s’est produite.</span><span class="sxs-lookup"><span data-stu-id="08698-138">The error that occurred.</span></span>  

<span data-ttu-id="08698-139">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="08698-139">This property is read-only.</span></span>  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### <span data-ttu-id="08698-140">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="08698-140">Property value</span></span>  

<span data-ttu-id="08698-141">Type: **DOMError**</span><span class="sxs-lookup"><span data-stu-id="08698-141">Type: **DOMError**</span></span>  

### <span data-ttu-id="08698-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="08698-142">oncomplete</span></span>  

<span data-ttu-id="08698-143">Le gestionnaire d’événements **complet** .</span><span class="sxs-lookup"><span data-stu-id="08698-143">The **complete** event handler.</span></span>  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### <span data-ttu-id="08698-144">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="08698-144">Property value</span></span>  

<span data-ttu-id="08698-145">Type: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="08698-145">Type: **EventHandler**</span></span>  

### <span data-ttu-id="08698-146">erreur</span><span class="sxs-lookup"><span data-stu-id="08698-146">onerror</span></span>  

<span data-ttu-id="08698-147">Le gestionnaire d’événements d' **erreur** .</span><span class="sxs-lookup"><span data-stu-id="08698-147">The **error** event handler.</span></span>  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### <span data-ttu-id="08698-148">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="08698-148">Property value</span></span>  

<span data-ttu-id="08698-149">Type: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="08698-149">Type: **EventHandler**</span></span>  

### <span data-ttu-id="08698-150">readyState</span><span class="sxs-lookup"><span data-stu-id="08698-150">readyState</span></span>  

<span data-ttu-id="08698-151">Décrit l’état prêt de l’objet.</span><span class="sxs-lookup"><span data-stu-id="08698-151">Describes the ready state of the object.</span></span>  

<span data-ttu-id="08698-152">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="08698-152">This property is read-only.</span></span>  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### <span data-ttu-id="08698-153">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="08698-153">Property value</span></span>  

<span data-ttu-id="08698-154">Type: **courte non signée**</span><span class="sxs-lookup"><span data-stu-id="08698-154">Type: **unsigned short**</span></span>  

### <span data-ttu-id="08698-155">provoqué</span><span class="sxs-lookup"><span data-stu-id="08698-155">result</span></span>  

<span data-ttu-id="08698-156">Résultat de l’opération.</span><span class="sxs-lookup"><span data-stu-id="08698-156">The result of the operation.</span></span>  

<span data-ttu-id="08698-157">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="08698-157">This property is read-only.</span></span>  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### <span data-ttu-id="08698-158">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="08698-158">Property value</span></span>  

<span data-ttu-id="08698-159">Tapez: tout</span><span class="sxs-lookup"><span data-stu-id="08698-159">Type: any</span></span>  

### <span data-ttu-id="08698-160">target</span><span class="sxs-lookup"><span data-stu-id="08698-160">target</span></span>  

<span data-ttu-id="08698-161">La cible de l’opération.</span><span class="sxs-lookup"><span data-stu-id="08698-161">The target of the operation.</span></span>  

<span data-ttu-id="08698-162">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="08698-162">This property is read-only.</span></span>  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### <span data-ttu-id="08698-163">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="08698-163">Property value</span></span>  

<span data-ttu-id="08698-164">Type: [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="08698-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>  

### <span data-ttu-id="08698-165">type</span><span class="sxs-lookup"><span data-stu-id="08698-165">type</span></span>  

<span data-ttu-id="08698-166">Type de l’opération.</span><span class="sxs-lookup"><span data-stu-id="08698-166">The type of the operation.</span></span>  

<span data-ttu-id="08698-167">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="08698-167">This property is read-only.</span></span>  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### <span data-ttu-id="08698-168">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="08698-168">Property value</span></span>  

<span data-ttu-id="08698-169">Type: **courte non signée**</span><span class="sxs-lookup"><span data-stu-id="08698-169">Type: **unsigned short**</span></span>  
