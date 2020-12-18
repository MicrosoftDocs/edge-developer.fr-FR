---
description: Détourne un objet JavaScript en `IInspectable` pointeur.
title: Fonction JsObjectToInspectable | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 0d818f798805e2afad4dc87b308258464d31bf92
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233305"
---
# <span data-ttu-id="163e8-103">JsObjectToInspectable Function</span><span class="sxs-lookup"><span data-stu-id="163e8-103">JsObjectToInspectable Function</span></span>

<span data-ttu-id="163e8-104">Détourne un objet JavaScript en `IInspectable` pointeur.</span><span class="sxs-lookup"><span data-stu-id="163e8-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="163e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="163e8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="163e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="163e8-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="163e8-107">Valeur JavaScript devant être projetée `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="163e8-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="163e8-108">`IInspectable`Valeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="163e8-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="163e8-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="163e8-109">Return Value</span></span>  
 <span data-ttu-id="163e8-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="163e8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="163e8-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="163e8-111">Remarks</span></span>  
 <span data-ttu-id="163e8-112">Les hôtes sont chargés d’appliquer les règles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="163e8-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="163e8-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="163e8-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="163e8-114">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="163e8-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="163e8-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="163e8-115">Requirements</span></span>  
 <span data-ttu-id="163e8-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="163e8-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="163e8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="163e8-117">See Also</span></span>  
 [<span data-ttu-id="163e8-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="163e8-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
