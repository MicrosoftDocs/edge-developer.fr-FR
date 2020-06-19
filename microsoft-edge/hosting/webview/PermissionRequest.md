---
description: Fournit des informations sur une demande d’autorisation.
title: Objet PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: c769bf122c3ca116d5783b73d0ff4f183d2cd52d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752115"
---
# <span data-ttu-id="85035-104">Objet PermissionRequest</span><span class="sxs-lookup"><span data-stu-id="85035-104">PermissionRequest object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="85035-105">Fournit des informations sur une demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="85035-105">Provides information about a permission request.</span></span> <span data-ttu-id="85035-106">Cet objet est disponible à partir de la propriété permissionRequest des arguments d’événement à partir de l’événement WebView [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) .</span><span class="sxs-lookup"><span data-stu-id="85035-106">This object is available from the permissionRequest property of the event args from the [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) webview event.</span></span>  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});
```  

## <span data-ttu-id="85035-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="85035-107">Methods</span></span>  

### <span data-ttu-id="85035-108">verte</span><span class="sxs-lookup"><span data-stu-id="85035-108">allow</span></span>  

<span data-ttu-id="85035-109">Autorise la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="85035-109">Allows the request for permission.</span></span>  

#### <span data-ttu-id="85035-110">Parameters</span><span class="sxs-lookup"><span data-stu-id="85035-110">Parameters</span></span>  

<span data-ttu-id="85035-111">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="85035-111">This method has no parameters.</span></span>  

#### <span data-ttu-id="85035-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85035-112">Return value</span></span>  

<span data-ttu-id="85035-113">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="85035-113">This method does not return a value.</span></span>  

### <span data-ttu-id="85035-114">différer</span><span class="sxs-lookup"><span data-stu-id="85035-114">defer</span></span>  

<span data-ttu-id="85035-115">Si, au lieu de autoriser ou non une PermissionRequest de manière synchrone, vous avez besoin d’un temps pour interagir avec l’utilisateur ou effectuer une autre action asynchrone, appeler différer () sur le PermissionRequest.</span><span class="sxs-lookup"><span data-stu-id="85035-115">If instead of synchronously allowing or disallowing a PermissionRequest, you require time to interact with the user or take some other asynchronous action, call defer() on the PermissionRequest.</span></span>  <span data-ttu-id="85035-116">Le PermissionRequest sera désormais disponible en tant que DeferredPermissionRequest à partir de getDeferredPermissionRequests et d’getDeferredPermissionRequestById.</span><span class="sxs-lookup"><span data-stu-id="85035-116">The PermissionRequest will now be available as a DeferredPermissionRequest from getDeferredPermissionRequests and getDeferredPermissionRequestById.</span></span>  <span data-ttu-id="85035-117">Vous pouvez mettre en corrélation le PermissionRequest actif avec le DeferredPermissionRequest correspondant par le biais de la propriété ID correspondante.</span><span class="sxs-lookup"><span data-stu-id="85035-117">You can correlate the current PermissionRequest with the corresponding DeferredPermissionRequest via the matching id property.</span></span>  

#### <span data-ttu-id="85035-118">Parameters</span><span class="sxs-lookup"><span data-stu-id="85035-118">Parameters</span></span>  

<span data-ttu-id="85035-119">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="85035-119">This method has no parameters.</span></span>  

#### <span data-ttu-id="85035-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85035-120">Return value</span></span>  

<span data-ttu-id="85035-121">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="85035-121">This method does not return a value.</span></span>  

### <span data-ttu-id="85035-122">deny</span><span class="sxs-lookup"><span data-stu-id="85035-122">deny</span></span>  

<span data-ttu-id="85035-123">Refuse la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="85035-123">Denies the request for permission.</span></span>  

#### <span data-ttu-id="85035-124">Parameters</span><span class="sxs-lookup"><span data-stu-id="85035-124">Parameters</span></span>  

<span data-ttu-id="85035-125">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="85035-125">This method has no parameters.</span></span>  

#### <span data-ttu-id="85035-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="85035-126">Return value</span></span>  

<span data-ttu-id="85035-127">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="85035-127">This method does not return a value.</span></span>  

## <span data-ttu-id="85035-128">Propriétés</span><span class="sxs-lookup"><span data-stu-id="85035-128">Properties</span></span>  

### <span data-ttu-id="85035-129">id</span><span class="sxs-lookup"><span data-stu-id="85035-129">id</span></span>  

<span data-ttu-id="85035-130">ID unique qui peut être utilisé pour mettre en corrélation le PermissionRequest en cours avec un DeferredPermissionRequest correspondant si la méthode defer est utilisée.</span><span class="sxs-lookup"><span data-stu-id="85035-130">A unique ID that can be used to correlate the current PermissionRequest with a corresponding DeferredPermissionRequest if the defer method is used.</span></span>  <span data-ttu-id="85035-131">Voir la méthode defer.</span><span class="sxs-lookup"><span data-stu-id="85035-131">See the defer method.</span></span>  

<span data-ttu-id="85035-132">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85035-132">This property is read-only.</span></span>  

##### <span data-ttu-id="85035-133">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="85035-133">Property value</span></span>  

<span data-ttu-id="85035-134">Type: **longue non signée**</span><span class="sxs-lookup"><span data-stu-id="85035-134">Type: **Unsigned long**</span></span>  

### <span data-ttu-id="85035-135">traité</span><span class="sxs-lookup"><span data-stu-id="85035-135">state</span></span>  

<span data-ttu-id="85035-136">Renvoie «Unknown», «Defer», «Allow» ou «Deny» pour indiquer l’état actuel de la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="85035-136">Returns "unknown", "defer", "allow", or "deny" to indicate the current state of permission request.</span></span>  <span data-ttu-id="85035-137">La chaîne d’état correspond à la méthode Allow, Deny ou différ appelée Last ou «Unknown» si aucune des méthodes n’a été appelée.</span><span class="sxs-lookup"><span data-stu-id="85035-137">The state string will correspond to whichever method allow, deny, or defer was called last or "unknown" if none of the methods have been called.</span></span>  

<span data-ttu-id="85035-138">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85035-138">This property is read-only.</span></span>  

#### <span data-ttu-id="85035-139">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="85035-139">Property value</span></span>  

<span data-ttu-id="85035-140">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85035-140">Type: **String**</span></span>  

### <span data-ttu-id="85035-141">type</span><span class="sxs-lookup"><span data-stu-id="85035-141">type</span></span>  

<span data-ttu-id="85035-142">Type d’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="85035-142">The type of permission being requested.</span></span> <span data-ttu-id="85035-143">Il s’agit de l’une des valeurs de chaîne suivantes:</span><span class="sxs-lookup"><span data-stu-id="85035-143">This may be one of the following string values:</span></span>  

*   <span data-ttu-id="85035-144">**géolocalisation**: accès aux données d’emplacement par le biais de Navigator. géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="85035-144">**geolocation**: access to location data via navigator.geolocation.</span></span>  
*   <span data-ttu-id="85035-145">**unlimitedIndexedDBQuota**: autoriser les API IndexedDB à ignorer la limite de taille des données stockées habituellement.</span><span class="sxs-lookup"><span data-stu-id="85035-145">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>  
*   <span data-ttu-id="85035-146">**média**: accès au microphone et à la caméra par le biais de Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="85035-146">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>  
*   <span data-ttu-id="85035-147">**pointerlock**: possibilité de verrouiller et de contrôler le pointeur de la souris via l’élément. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="85035-147">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>  
*   <span data-ttu-id="85035-148">**webnotifications**: possibilité d’afficher les notifications sur le bureau via une fenêtre. Message.</span><span class="sxs-lookup"><span data-stu-id="85035-148">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>  
*   <span data-ttu-id="85035-149">**écran**: possibilité de prendre des captures d’écran à l’aide de l’API de capture multimédia.</span><span class="sxs-lookup"><span data-stu-id="85035-149">**screen**: ability to take screen shots via the Media Capture API.</span></span>  
*   <span data-ttu-id="85035-150">**immersiveview**: possibilité de contrôler un affichage VR.</span><span class="sxs-lookup"><span data-stu-id="85035-150">**immersiveview**: ability to control a VR display.</span></span>  

<span data-ttu-id="85035-151">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85035-151">This property is read-only.</span></span>  

#### <span data-ttu-id="85035-152">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="85035-152">Property value</span></span>  

<span data-ttu-id="85035-153">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85035-153">Type: **String**</span></span>  

### <span data-ttu-id="85035-154">uri</span><span class="sxs-lookup"><span data-stu-id="85035-154">uri</span></span>  

<span data-ttu-id="85035-155">URI (Uniform Resource Identifier) du document demandant l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="85035-155">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>  

<span data-ttu-id="85035-156">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="85035-156">This property is read-only.</span></span>  

#### <span data-ttu-id="85035-157">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="85035-157">Property value</span></span>  

<span data-ttu-id="85035-158">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="85035-158">Type: **String**</span></span>  
