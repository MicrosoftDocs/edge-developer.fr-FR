---
description: Objet LongRunningScriptDetectedEvent
title: Objet LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/03/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: webview, applications Windows 10, uwp, edge
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5f5eb3230e46ee2cd7926b21f6526e512a7a0322
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397939"
---
# <a name="longrunningscriptdetectedevent-object"></a><span data-ttu-id="44699-104">Objet LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="44699-104">LongRunningScriptDetectedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="44699-105">Fournit des informations [pour MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="44699-105">Provides information for [MSWebViewLongRunningScriptDetected](../webview/index.md#mswebviewlongrunningscriptdetected).</span></span>  

## <a name="properties"></a><span data-ttu-id="44699-106">Propriétés</span><span class="sxs-lookup"><span data-stu-id="44699-106">Properties</span></span>  

### <a name="executiontime"></a><span data-ttu-id="44699-107">executionTime</span><span class="sxs-lookup"><span data-stu-id="44699-107">executionTime</span></span>  

<span data-ttu-id="44699-108">Obtient le nombre de millisecondes pendant combien de millisecondes l’élément [webview](../webview/index.md) a exécuté un script de longue durée.</span><span class="sxs-lookup"><span data-stu-id="44699-108">Gets the number of milliseconds that the [webview](../webview/index.md) element has been executing a long-running script.</span></span>  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### <a name="property-value"></a><span data-ttu-id="44699-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="44699-109">Property value</span></span>  

<span data-ttu-id="44699-110">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="44699-110">Type: **long**</span></span>  

### <a name="stoppagescriptexecution"></a><span data-ttu-id="44699-111">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="44699-111">stopPageScriptExecution</span></span>  

<span data-ttu-id="44699-112">Arrête l’exécution d’un script de longue durée dans [l’élément webview.](../webview/index.md)</span><span class="sxs-lookup"><span data-stu-id="44699-112">Stops a long-running script executing in the [webview](../webview/index.md) element.</span></span>  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### <a name="property-value"></a><span data-ttu-id="44699-113">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="44699-113">Property value</span></span>  

<span data-ttu-id="44699-114">Type : **Boolean**</span><span class="sxs-lookup"><span data-stu-id="44699-114">Type: **Boolean**</span></span>  
