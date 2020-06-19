---
description: Représente un processus WebView.
title: Objet MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752155"
---
# <span data-ttu-id="b4708-104">Objet MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="b4708-104">MSWebViewProcess object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="b4708-105">Représente un processus [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="b4708-105">Represents a [webview](../webview.md) process.</span></span>  

```javascript
var wvprocess = new MSWebViewProcess();
```  

## <span data-ttu-id="b4708-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4708-106">Properties</span></span>  

### <span data-ttu-id="b4708-107">enterpriseId</span><span class="sxs-lookup"><span data-stu-id="b4708-107">enterpriseId</span></span>  

<span data-ttu-id="b4708-108">ID entreprise du processus.</span><span class="sxs-lookup"><span data-stu-id="b4708-108">The enterprise ID of the process.</span></span>  

```js
var enterpriseId = wvprocess.enterpriseId;
```  

<span data-ttu-id="b4708-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b4708-109">This property is read-only.</span></span>  

#### <span data-ttu-id="b4708-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="b4708-110">Property value</span></span>  

<span data-ttu-id="b4708-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="b4708-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="b4708-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="b4708-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>  

<span data-ttu-id="b4708-113">Obtient une valeur indiquant si le processus [WebView](../webview.md) possède la [déclaration des fonctionnalités](/windows/uwp/packaging/app-capability-declarations) des *réseaux privés (client & serveur)* qui est activée dans le manifeste de l’application.</span><span class="sxs-lookup"><span data-stu-id="b4708-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>  

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

<span data-ttu-id="b4708-114">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="b4708-114">This property is read-only.</span></span>  

#### <span data-ttu-id="b4708-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="b4708-115">Property value</span></span>  

<span data-ttu-id="b4708-116">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="b4708-116">Type: **Boolean**</span></span>  

## <span data-ttu-id="b4708-117">Méthodes</span><span class="sxs-lookup"><span data-stu-id="b4708-117">Methods</span></span>  

### <span data-ttu-id="b4708-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="b4708-118">CreateWebViewAsync</span></span>  

<span data-ttu-id="b4708-119">Crée un [WebView](../webview.md) dans un processus spécifique.</span><span class="sxs-lookup"><span data-stu-id="b4708-119">Creates a [webview](../webview.md) in a specific process.</span></span>  

```javascript
wvprocess.createWebviewAsync();
```  

#### <span data-ttu-id="b4708-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4708-120">Return value</span></span>  

<span data-ttu-id="b4708-121">Nouveau**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="b4708-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="b4708-122">GetWebViews</span><span class="sxs-lookup"><span data-stu-id="b4708-122">GetWebViews</span></span>  

<span data-ttu-id="b4708-123">Retourne une séquence d’objets **MSWebViewProcess** hébergés dans le processus.</span><span class="sxs-lookup"><span data-stu-id="b4708-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>  

#### <span data-ttu-id="b4708-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4708-124">Return value</span></span>  

<span data-ttu-id="b4708-125">Nouveau**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="b4708-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="b4708-126">Contrat</span><span class="sxs-lookup"><span data-stu-id="b4708-126">Terminate</span></span>  

<span data-ttu-id="b4708-127">Arrête le processus.</span><span class="sxs-lookup"><span data-stu-id="b4708-127">Terminates the process.</span></span>  

```javascript
wvprocess.terminate();
```  

#### <span data-ttu-id="b4708-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4708-128">Return value</span></span>  

<span data-ttu-id="b4708-129">Cette méthode ne renvoie pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="b4708-129">This method does not return a value.</span></span>  
