---
description: Obtient la liste de toutes les propriétés de l’objet.
title: Fonction JsGetOwnPropertyNames | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 4d00788b6ef581b923413e5c71a63bb27398a326
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232781"
---
# <span data-ttu-id="6bf34-103">JsGetOwnPropertyNames Function</span><span class="sxs-lookup"><span data-stu-id="6bf34-103">JsGetOwnPropertyNames Function</span></span>

<span data-ttu-id="6bf34-104">Obtient la liste de toutes les propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6bf34-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="6bf34-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bf34-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="6bf34-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bf34-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="6bf34-107">Objet à partir duquel obtenir les noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="6bf34-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="6bf34-108">Tableau de noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="6bf34-108">An array of property names.</span></span>  
  
## <span data-ttu-id="6bf34-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6bf34-109">Return Value</span></span>  
 <span data-ttu-id="6bf34-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6bf34-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6bf34-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6bf34-111">Remarks</span></span>  
 <span data-ttu-id="6bf34-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6bf34-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="6bf34-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="6bf34-113">Requirements</span></span>  
 <span data-ttu-id="6bf34-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6bf34-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6bf34-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bf34-115">See Also</span></span>  
 [<span data-ttu-id="6bf34-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6bf34-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
