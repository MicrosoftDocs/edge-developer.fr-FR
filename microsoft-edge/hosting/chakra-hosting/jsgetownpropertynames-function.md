---
description: Obtient la liste de toutes les propriétés de l’objet.
title: Fonction JsGetOwnPropertyNames | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5355caab864724d72fdb2c7abb3dc70e39662b55
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566316"
---
# <span data-ttu-id="6342c-103">Fonction JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="6342c-103">JsGetOwnPropertyNames Function</span></span>
<span data-ttu-id="6342c-104">Obtient la liste de toutes les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6342c-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="6342c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6342c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="6342c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6342c-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6342c-107">Objet à partir duquel obtenir les noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="6342c-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="6342c-108">Tableau de noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="6342c-108">An array of property names.</span></span>  
  
## <span data-ttu-id="6342c-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6342c-109">Return Value</span></span>  
 <span data-ttu-id="6342c-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6342c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6342c-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6342c-111">Remarks</span></span>  
 <span data-ttu-id="6342c-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6342c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6342c-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6342c-113">Requirements</span></span>  
 <span data-ttu-id="6342c-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6342c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6342c-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6342c-115">See Also</span></span>  
 [<span data-ttu-id="6342c-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6342c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)