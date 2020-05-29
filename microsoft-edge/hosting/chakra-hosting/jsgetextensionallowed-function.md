---
description: Renvoie une valeur qui indique si un objet est extensible ou non.
title: Fonction JsGetExtensionAllowed | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3baa6449294f7b055251d861a32095deb1bdfe9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565191"
---
# <span data-ttu-id="b6351-103">Fonction JsGetExtensionAllowed</span><span class="sxs-lookup"><span data-stu-id="b6351-103">JsGetExtensionAllowed Function</span></span>
<span data-ttu-id="b6351-104">Renvoie une valeur qui indique si un objet est extensible ou non.</span><span class="sxs-lookup"><span data-stu-id="b6351-104">Returns a value that indicates whether an object is extensible or not.</span></span>  
  
## <span data-ttu-id="b6351-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6351-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### <span data-ttu-id="b6351-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6351-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b6351-107">Objet à tester.</span><span class="sxs-lookup"><span data-stu-id="b6351-107">The object to test.</span></span>  
  
 `value`  
 <span data-ttu-id="b6351-108">Si l’objet est extensible ou non.</span><span class="sxs-lookup"><span data-stu-id="b6351-108">Whether the object is extensible or not.</span></span>  
  
## <span data-ttu-id="b6351-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b6351-109">Return Value</span></span>  
 <span data-ttu-id="b6351-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b6351-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b6351-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6351-111">Remarks</span></span>  
 <span data-ttu-id="b6351-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="b6351-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b6351-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6351-113">Requirements</span></span>  
 <span data-ttu-id="b6351-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b6351-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b6351-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6351-115">See Also</span></span>  
 [<span data-ttu-id="b6351-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b6351-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)