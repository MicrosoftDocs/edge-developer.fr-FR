---
description: ''
title: Objet LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, applications Windows 10, UWP, Edge
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565109"
---
# <span data-ttu-id="03c10-103">Objet LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="03c10-103">LongRunningScriptDetectedEvent object</span></span>

<span data-ttu-id="03c10-104">Fournit des informations pour [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span><span class="sxs-lookup"><span data-stu-id="03c10-104">Provides information for [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).</span></span>

## <span data-ttu-id="03c10-105">Propriétés</span><span class="sxs-lookup"><span data-stu-id="03c10-105">Properties</span></span>

### <span data-ttu-id="03c10-106">executionTime</span><span class="sxs-lookup"><span data-stu-id="03c10-106">executionTime</span></span>

<span data-ttu-id="03c10-107">Obtient le nombre de millisecondes pendant lesquelles l’élément [WebView](../webview.md) a exécuté un script de longue durée.</span><span class="sxs-lookup"><span data-stu-id="03c10-107">Gets the number of milliseconds that the [webview](../webview.md) element has been executing a long-running script.</span></span>

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### <span data-ttu-id="03c10-108">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="03c10-108">Property value</span></span>
<span data-ttu-id="03c10-109">Type: **long**</span><span class="sxs-lookup"><span data-stu-id="03c10-109">Type: **long**</span></span>

### <span data-ttu-id="03c10-110">stopPageScriptExecution</span><span class="sxs-lookup"><span data-stu-id="03c10-110">stopPageScriptExecution</span></span>
<span data-ttu-id="03c10-111">Arrête l’exécution d’un script longue dans l’élément [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="03c10-111">Stops a long-running script executing in the [webview](../webview.md) element.</span></span>

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### <span data-ttu-id="03c10-112">Valeur de propriété</span><span class="sxs-lookup"><span data-stu-id="03c10-112">Property value</span></span>
<span data-ttu-id="03c10-113">Type: **booléen**</span><span class="sxs-lookup"><span data-stu-id="03c10-113">Type: **Boolean**</span></span>