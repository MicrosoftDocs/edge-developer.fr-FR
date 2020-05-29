---
description: Représente un processus WebView.
title: Objet MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565102"
---
# <span data-ttu-id="a1dd8-104">Objet MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="a1dd8-104">MSWebViewProcess object</span></span>

<span data-ttu-id="a1dd8-105">Représente un processus [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="a1dd8-105">Represents a [webview](../webview.md) process.</span></span>

```js
var wvprocess = new MSWebViewProcess();
```

## <span data-ttu-id="a1dd8-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a1dd8-106">Properties</span></span>

### <span data-ttu-id="a1dd8-107">enterpriseId</span><span class="sxs-lookup"><span data-stu-id="a1dd8-107">enterpriseId</span></span>

<span data-ttu-id="a1dd8-108">ID entreprise du processus.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-108">The enterprise ID of the process.</span></span>

```js
var enterpriseId = wvprocess.enterpriseId;
```

<span data-ttu-id="a1dd8-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-109">This property is read-only.</span></span>

#### <span data-ttu-id="a1dd8-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="a1dd8-110">Property value</span></span>
<span data-ttu-id="a1dd8-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="a1dd8-111">Type: **DOMString**</span></span>

### <span data-ttu-id="a1dd8-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="a1dd8-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>

<span data-ttu-id="a1dd8-113">Obtient une valeur indiquant si le processus [WebView](../webview.md) possède la [déclaration des fonctionnalités](/windows/uwp/packaging/app-capability-declarations) des *réseaux privés (client & serveur)* qui est activée dans le manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

<span data-ttu-id="a1dd8-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-114">This property is read-only.</span></span>

#### <span data-ttu-id="a1dd8-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="a1dd8-115">Property value</span></span>
<span data-ttu-id="a1dd8-116">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="a1dd8-116">Type: **Boolean**</span></span>

## <span data-ttu-id="a1dd8-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a1dd8-117">Methods</span></span>

### <span data-ttu-id="a1dd8-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="a1dd8-118">CreateWebViewAsync</span></span>

<span data-ttu-id="a1dd8-119">Crée un [WebView](../webview.md) dans un processus spécifique.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-119">Creates a [webview](../webview.md) in a specific process.</span></span>

```js
wvprocess.createWebviewAsync();
```

#### <span data-ttu-id="a1dd8-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a1dd8-120">Return value</span></span>

<span data-ttu-id="a1dd8-121">Nouveau**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="a1dd8-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="a1dd8-122">GetWebViews</span><span class="sxs-lookup"><span data-stu-id="a1dd8-122">GetWebViews</span></span>

<span data-ttu-id="a1dd8-123">Retourne une séquence d’objets **MSWebViewProcess** hébergés dans le processus.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>

#### <span data-ttu-id="a1dd8-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a1dd8-124">Return value</span></span>

<span data-ttu-id="a1dd8-125">Nouveau**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="a1dd8-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="a1dd8-126">Contrat</span><span class="sxs-lookup"><span data-stu-id="a1dd8-126">Terminate</span></span>

<span data-ttu-id="a1dd8-127">Arrête le processus.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-127">Terminates the process.</span></span>

```js
wvprocess.terminate();
```

#### <span data-ttu-id="a1dd8-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a1dd8-128">Return value</span></span>

<span data-ttu-id="a1dd8-129">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="a1dd8-129">This method does not return a value.</span></span>
