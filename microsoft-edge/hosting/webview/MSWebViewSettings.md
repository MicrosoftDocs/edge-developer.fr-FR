---
description: Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d’affichage WebView
title: Objet MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565100"
---
# <span data-ttu-id="d5ac6-104">Objet MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="d5ac6-104">MSWebViewSettings object</span></span>

<span data-ttu-id="d5ac6-105">Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d' [affichage WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="d5ac6-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>

## <span data-ttu-id="d5ac6-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d5ac6-106">Properties</span></span>

### <span data-ttu-id="d5ac6-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="d5ac6-107">isIndexedDBEnabled</span></span>

<span data-ttu-id="d5ac6-108">Obtient ou définit une valeur qui indique si l’utilisation de IndexedDB est autorisée dans le [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="d5ac6-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### <span data-ttu-id="d5ac6-109">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="d5ac6-109">Property value</span></span>
<span data-ttu-id="d5ac6-110">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="d5ac6-110">Type: **boolean**</span></span>

<span data-ttu-id="d5ac6-111">**True** si IndexedDB est autorisé dans le **WebView**; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d5ac6-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span> 

### <span data-ttu-id="d5ac6-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="d5ac6-112">isJavaScriptEnabled</span></span>

<span data-ttu-id="d5ac6-113">Obtient ou définit une valeur qui indique si l’utilisation de JavaScript est autorisée dans le [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="d5ac6-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### <span data-ttu-id="d5ac6-114">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="d5ac6-114">Property value</span></span>
<span data-ttu-id="d5ac6-115">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="d5ac6-115">Type: **boolean**</span></span>

<span data-ttu-id="d5ac6-116">**Vrai** JavaScript est autorisé dans le [WebView](../webview.md); Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d5ac6-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 

### <span data-ttu-id="d5ac6-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="d5ac6-117">isScriptNotifyAllowed</span></span>

<span data-ttu-id="d5ac6-118">Obtient ou définit une valeur qui indique si l’utilisation de [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisée dans le [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="d5ac6-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### <span data-ttu-id="d5ac6-119">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="d5ac6-119">Property value</span></span>
<span data-ttu-id="d5ac6-120">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="d5ac6-120">Type: **boolean**</span></span>

<span data-ttu-id="d5ac6-121">**Vrai** [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisé dans le [WebView](../webview.md); Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="d5ac6-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span> 
