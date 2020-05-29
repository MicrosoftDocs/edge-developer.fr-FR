---
description: Représente une demande différée d’autorisation utilisateur pour accéder aux fonctionnalités d’appareil
title: Objet DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 6013f20195fc0f5d4f33b871a9c1b01392bf023e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565112"
---
# <span data-ttu-id="1b62e-104">Objet DeferredPermissionRequest</span><span class="sxs-lookup"><span data-stu-id="1b62e-104">DeferredPermissionRequest object</span></span>

<span data-ttu-id="1b62e-105">Représente une requête différée par le contenu du [WebView](../webview.md) pour l’autorisation de l’utilisateur final pour accéder à des fonctionnalités d’appareil spécialisées (par exemple, géolocalisation ou verrouillage de pointeur).</span><span class="sxs-lookup"><span data-stu-id="1b62e-105">Represents a deferred request by the content of the [webview](../webview.md) for end-user permission to access specialized device functionality (such as geolocation, or pointer lock).</span></span>

```js
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```

## <span data-ttu-id="1b62e-106">Méthodes</span><span class="sxs-lookup"><span data-stu-id="1b62e-106">Methods</span></span>

### <span data-ttu-id="1b62e-107">verte</span><span class="sxs-lookup"><span data-stu-id="1b62e-107">allow</span></span>

<span data-ttu-id="1b62e-108">Autorise la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="1b62e-108">Allows the request for permission.</span></span>

```js
deferredPermissionRequest.allow();
```

#### <span data-ttu-id="1b62e-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="1b62e-109">Parameters</span></span>

<span data-ttu-id="1b62e-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1b62e-110">This method has no parameters.</span></span>

#### <span data-ttu-id="1b62e-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b62e-111">Return value</span></span>

<span data-ttu-id="1b62e-112">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b62e-112">This method does not return a value.</span></span>

### <span data-ttu-id="1b62e-113">deny</span><span class="sxs-lookup"><span data-stu-id="1b62e-113">deny</span></span>

<span data-ttu-id="1b62e-114">Refuse la demande d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="1b62e-114">Denies the request for permission.</span></span>

```js
deferredPermissionRequest.deny();
```

#### <span data-ttu-id="1b62e-115">Parameters</span><span class="sxs-lookup"><span data-stu-id="1b62e-115">Parameters</span></span>

<span data-ttu-id="1b62e-116">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="1b62e-116">This method has no parameters.</span></span>

#### <span data-ttu-id="1b62e-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1b62e-117">Return value</span></span>

<span data-ttu-id="1b62e-118">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="1b62e-118">This method does not return a value.</span></span>

## <span data-ttu-id="1b62e-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1b62e-119">Properties</span></span>

### <span data-ttu-id="1b62e-120">id</span><span class="sxs-lookup"><span data-stu-id="1b62e-120">id</span></span>

<span data-ttu-id="1b62e-121">ID unique qui peut être utilisé pour mettre en corrélation le DeferredPermissionRequest actuel avec un objet PermissionRequest à partir d’un événement MSWebViewPermissionRequested précédent.</span><span class="sxs-lookup"><span data-stu-id="1b62e-121">A unique ID that can be used to correlate the current DeferredPermissionRequest with a PermissionRequest object from a previous MSWebViewPermissionRequested event.</span></span> <span data-ttu-id="1b62e-122">Voir la méthode **PermissionRequested. Defer** .</span><span class="sxs-lookup"><span data-stu-id="1b62e-122">See the **PermissionRequested.defer** method.</span></span>

<span data-ttu-id="1b62e-123">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1b62e-123">This property is read-only.</span></span>

```js
var id = deferredPermissionRequest.id;
```

##### <span data-ttu-id="1b62e-124">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1b62e-124">Property value</span></span>

<span data-ttu-id="1b62e-125">Type: **longue non signée**</span><span class="sxs-lookup"><span data-stu-id="1b62e-125">Type: **Unsigned long**</span></span>

### <span data-ttu-id="1b62e-126">type</span><span class="sxs-lookup"><span data-stu-id="1b62e-126">type</span></span>

<span data-ttu-id="1b62e-127">Type d’autorisation demandée.</span><span class="sxs-lookup"><span data-stu-id="1b62e-127">The type of permission being requested.</span></span> <span data-ttu-id="1b62e-128">Il s’agit de l’une des valeurs de chaîne suivantes:</span><span class="sxs-lookup"><span data-stu-id="1b62e-128">This may be one of the following string values:</span></span>

- <span data-ttu-id="1b62e-129">**géolocalisation**: accès aux données d’emplacement par le biais de Navigator. géolocalisation.</span><span class="sxs-lookup"><span data-stu-id="1b62e-129">**geolocation**: access to location data via navigator.geolocation.</span></span>
- <span data-ttu-id="1b62e-130">**unlimitedIndexedDBQuota**: autoriser les API IndexedDB à ignorer la limite de taille des données stockées habituellement.</span><span class="sxs-lookup"><span data-stu-id="1b62e-130">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>
- <span data-ttu-id="1b62e-131">**média**: accès au microphone et à la caméra par le biais de Navigator. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="1b62e-131">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>
- <span data-ttu-id="1b62e-132">**pointerlock**: possibilité de verrouiller et de contrôler le pointeur de la souris via l’élément. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="1b62e-132">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>
- <span data-ttu-id="1b62e-133">**webnotifications**: possibilité d’afficher les notifications sur le bureau via une fenêtre. Message.</span><span class="sxs-lookup"><span data-stu-id="1b62e-133">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>
- <span data-ttu-id="1b62e-134">**écran**: possibilité de prendre des captures d’écran à l’aide de l’API de capture multimédia.</span><span class="sxs-lookup"><span data-stu-id="1b62e-134">**screen**: ability to take screen shots via the Media Capture API.</span></span>
- <span data-ttu-id="1b62e-135">**immersiveview**: possibilité de contrôler un affichage VR.</span><span class="sxs-lookup"><span data-stu-id="1b62e-135">**immersiveview**: ability to control a VR display.</span></span>

<span data-ttu-id="1b62e-136">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1b62e-136">This property is read-only.</span></span>

```js
var type = deferredPermissionRequest.type;
```

#### <span data-ttu-id="1b62e-137">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1b62e-137">Property value</span></span>

<span data-ttu-id="1b62e-138">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1b62e-138">Type: **String**</span></span>

### <span data-ttu-id="1b62e-139">uri</span><span class="sxs-lookup"><span data-stu-id="1b62e-139">uri</span></span>

<span data-ttu-id="1b62e-140">URI (Uniform Resource Identifier) du document demandant l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="1b62e-140">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>

<span data-ttu-id="1b62e-141">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1b62e-141">This property is read-only.</span></span>

```js
var uri = deferredPermissionRequest.uri;
```

##### <span data-ttu-id="1b62e-142">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1b62e-142">Property value</span></span>

<span data-ttu-id="1b62e-143">Type: **chaîne**</span><span class="sxs-lookup"><span data-stu-id="1b62e-143">Type: **String**</span></span>

## <span data-ttu-id="1b62e-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1b62e-144">Requirements</span></span>

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong><span data-ttu-id="1b62e-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b62e-145">Minimum supported client</span></span></strong> | <span data-ttu-id="1b62e-146">Windows 10 (applications du Windows Store uniquement)</span><span class="sxs-lookup"><span data-stu-id="1b62e-146">Windows 10 [Windows Store apps only]</span></span> |
| <strong><span data-ttu-id="1b62e-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b62e-147">Minimum supported server</span></span></strong> |            <span data-ttu-id="1b62e-148">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b62e-148">Not supported</span></span>             |
| <strong><span data-ttu-id="1b62e-149">Téléphone minimum pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b62e-149">Minimum supported phone</span></span></strong>  |            <span data-ttu-id="1b62e-150">Non pris en charge</span><span class="sxs-lookup"><span data-stu-id="1b62e-150">Not supported</span></span>             |
