---
description: Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d’affichage WebView
title: Objet MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752177"
---
# <span data-ttu-id="e1135-104">Objet MSWebViewSettings</span><span class="sxs-lookup"><span data-stu-id="e1135-104">MSWebViewSettings object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="e1135-105">Définit les propriétés permettant d’activer ou de désactiver les fonctionnalités d' [affichage WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="e1135-105">Defines properties that enable or disable [webview](../webview.md) features.</span></span>  

## <span data-ttu-id="e1135-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="e1135-106">Properties</span></span>  

### <span data-ttu-id="e1135-107">isIndexedDBEnabled</span><span class="sxs-lookup"><span data-stu-id="e1135-107">isIndexedDBEnabled</span></span>  

<span data-ttu-id="e1135-108">Obtient ou définit une valeur qui indique si l’utilisation de IndexedDB est autorisée dans le [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="e1135-108">Gets or sets a value that indicates whether the use of IndexedDB is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### <span data-ttu-id="e1135-109">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="e1135-109">Property value</span></span>  

<span data-ttu-id="e1135-110">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="e1135-110">Type: **boolean**</span></span>  

<span data-ttu-id="e1135-111">**True** si IndexedDB est autorisé dans le **WebView**; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e1135-111">**True** if IndexedDB is allowed in the **webview**; otherwise, **false**.</span></span>  

### <span data-ttu-id="e1135-112">isJavaScriptEnabled</span><span class="sxs-lookup"><span data-stu-id="e1135-112">isJavaScriptEnabled</span></span>  

<span data-ttu-id="e1135-113">Obtient ou définit une valeur qui indique si l’utilisation de JavaScript est autorisée dans le [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="e1135-113">Gets or sets a value that indicates whether the use of JavaScript is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### <span data-ttu-id="e1135-114">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="e1135-114">Property value</span></span>  

<span data-ttu-id="e1135-115">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="e1135-115">Type: **boolean**</span></span>  

<span data-ttu-id="e1135-116">**Vrai** JavaScript est autorisé dans le [WebView](../webview.md); Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e1135-116">**True** JavaScript is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  

### <span data-ttu-id="e1135-117">isScriptNotifyAllowed</span><span class="sxs-lookup"><span data-stu-id="e1135-117">isScriptNotifyAllowed</span></span>  

<span data-ttu-id="e1135-118">Obtient ou définit une valeur qui indique si l’utilisation de [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisée dans le [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="e1135-118">Gets or sets a value that indicates whether the use of [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md).</span></span>  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### <span data-ttu-id="e1135-119">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="e1135-119">Property value</span></span>  

<span data-ttu-id="e1135-120">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="e1135-120">Type: **boolean**</span></span>  

<span data-ttu-id="e1135-121">**Vrai** [ScriptNotifyEvent](ScriptNotifyEvent.md) est autorisé dans le [WebView](../webview.md); Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="e1135-121">**True** [ScriptNotifyEvent](ScriptNotifyEvent.md) is allowed in the [webview](../webview.md); otherwise, **false**.</span></span>  
