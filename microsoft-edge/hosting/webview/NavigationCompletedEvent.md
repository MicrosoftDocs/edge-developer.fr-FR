---
description: Contient des informations sur la navigation complète de WebView
title: Objet NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565099"
---
# <span data-ttu-id="1aa65-104">Objet NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="1aa65-104">NavigationCompletedEvent object</span></span>

<span data-ttu-id="1aa65-105">Objet qui représente un événement déclenché lorsque le [WebView](../webview.md) a fini de charger le contenu actuel ou en cas d’échec de la navigation.</span><span class="sxs-lookup"><span data-stu-id="1aa65-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>

## <span data-ttu-id="1aa65-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="1aa65-106">Properties</span></span>
    
### <span data-ttu-id="1aa65-107">uri</span><span class="sxs-lookup"><span data-stu-id="1aa65-107">uri</span></span>

<span data-ttu-id="1aa65-108">URI (Uniform Resource Identifier) de la navigation.</span><span class="sxs-lookup"><span data-stu-id="1aa65-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>

<span data-ttu-id="1aa65-109">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="1aa65-109">This property is read-only.</span></span>

```js
var uri = NavigationCompletedEvent.uri;
```

#### <span data-ttu-id="1aa65-110">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1aa65-110">Property value</span></span>
<span data-ttu-id="1aa65-111">Type: **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1aa65-111">Type: **DOMString**</span></span>

### <span data-ttu-id="1aa65-112">Propriétés IsSuccess</span><span class="sxs-lookup"><span data-stu-id="1aa65-112">isSuccess</span></span>

<span data-ttu-id="1aa65-113">Obtient une valeur qui indique si la navigation s’est déroulée correctement.</span><span class="sxs-lookup"><span data-stu-id="1aa65-113">Gets a value that indicates whether the navigation completed successfully.</span></span>

<span data-ttu-id="1aa65-114">Cette propriété est en lecture seule</span><span class="sxs-lookup"><span data-stu-id="1aa65-114">This property is read-only</span></span>

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### <span data-ttu-id="1aa65-115">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1aa65-115">Property value</span></span>
<span data-ttu-id="1aa65-116">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="1aa65-116">Type: **Boolean**</span></span>

### <span data-ttu-id="1aa65-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="1aa65-117">webErrorStatus</span></span>

<span data-ttu-id="1aa65-118">Si la navigation a échoué, obtient une valeur qui indique pourquoi.</span><span class="sxs-lookup"><span data-stu-id="1aa65-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>

<span data-ttu-id="1aa65-119">Cette propriété est en lecture seule</span><span class="sxs-lookup"><span data-stu-id="1aa65-119">This property is read-only</span></span>

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### <span data-ttu-id="1aa65-120">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="1aa65-120">Property value</span></span>
<span data-ttu-id="1aa65-121">Type: **longue non signée**</span><span class="sxs-lookup"><span data-stu-id="1aa65-121">Type: **unsigned long**</span></span>
