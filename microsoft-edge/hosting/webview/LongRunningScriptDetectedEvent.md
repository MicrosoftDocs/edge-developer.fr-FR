---
description: ''
title: Objet LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752150"
---
# <span data-ttu-id="c109f-103">Objet LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="c109f-103">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="c109f-104">Fournit des informations pour [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="c109f-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>  

## <span data-ttu-id="c109f-105">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c109f-105">Properties</span></span>  

### <span data-ttu-id="c109f-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="c109f-106">executionTime</span></span>  

<span data-ttu-id="c109f-107">Obtient le nombre de millisecondes pendant lesquelles l’élément [WebView](../webview.md) a exécuté un script de longue durée.</span><span class="sxs-lookup"><span data-stu-id="c109f-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <span data-ttu-id="c109f-108">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="c109f-108">Property value</span></span>  

<span data-ttu-id="c109f-109">Type: **long**</span><span class="sxs-lookup"><span data-stu-id="c109f-109">Type: **long**</span></span>  

### <span data-ttu-id="c109f-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="c109f-110">stopPageScriptExecution</span></span>  

<span data-ttu-id="c109f-111">Arrête l’exécution d’un script longue dans l’élément [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="c109f-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <span data-ttu-id="c109f-112">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="c109f-112">Property value</span></span>  

<span data-ttu-id="c109f-113">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="c109f-113">Type: **Boolean**</span></span>  
