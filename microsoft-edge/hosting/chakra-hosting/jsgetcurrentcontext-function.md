---
description: Obtient le contexte de script actuel sur le thread.
title: Fonction JsGetCurrentContext | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetCurrentContext
helpviewer_keywords:
- JsGetCurrentContext function
ms.assetid: dd5fe0fa-d1e5-4af6-809e-e655a27519b5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 78f04674aab8783c43f22516903669e0f9b7543b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565195"
---
# <span data-ttu-id="2a5a9-103">Fonction JsGetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="2a5a9-103">JsGetCurrentContext Function</span></span>
<span data-ttu-id="2a5a9-104">Obtient le contexte de script actuel sur le thread.</span><span class="sxs-lookup"><span data-stu-id="2a5a9-104">Gets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="2a5a9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2a5a9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetCurrentContext(  
   _Out_ JsContextRef *currentContext  
);  
```  
  
#### <span data-ttu-id="2a5a9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2a5a9-106">Parameters</span></span>  
 `currentContext`  
 <span data-ttu-id="2a5a9-107">Contexte de script actuel sur le thread, null s’il n’y a aucun contexte de script actuel.</span><span class="sxs-lookup"><span data-stu-id="2a5a9-107">The current script context on the thread, null if there is no current script context.</span></span>  
  
## <span data-ttu-id="2a5a9-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2a5a9-108">Return Value</span></span>  
 <span data-ttu-id="2a5a9-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="2a5a9-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2a5a9-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2a5a9-110">Requirements</span></span>  
 <span data-ttu-id="2a5a9-111">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2a5a9-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2a5a9-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2a5a9-112">See Also</span></span>  
 [<span data-ttu-id="2a5a9-113">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2a5a9-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)