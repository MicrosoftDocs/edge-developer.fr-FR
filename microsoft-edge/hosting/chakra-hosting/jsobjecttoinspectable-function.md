---
description: Détourne un objet JavaScript en `IInspectable` pointeur.
title: Fonction JsObjectToInspectable | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7127e1cf1372020e0df00b81ed172739379426f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566288"
---
# <span data-ttu-id="6b0e3-103">Fonction JsObjectToInspectable</span><span class="sxs-lookup"><span data-stu-id="6b0e3-103">JsObjectToInspectable Function</span></span>
<span data-ttu-id="6b0e3-104">Détourne un objet JavaScript en `IInspectable` pointeur.</span><span class="sxs-lookup"><span data-stu-id="6b0e3-104">Unwraps a JavaScript object to an `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="6b0e3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b0e3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### <span data-ttu-id="6b0e3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b0e3-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="6b0e3-107">Valeur JavaScript devant être projetée `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="6b0e3-107">A JavaScript value that should be projected to `IInspectable`.</span></span>  
  
 `inspectable`  
 <span data-ttu-id="6b0e3-108">`IInspectable`Valeur de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6b0e3-108">An `IInspectable` value of the object.</span></span>  
  
## <span data-ttu-id="6b0e3-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6b0e3-109">Return Value</span></span>  
 <span data-ttu-id="6b0e3-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="6b0e3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6b0e3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b0e3-111">Remarks</span></span>  
 <span data-ttu-id="6b0e3-112">Les hôtes sont chargés d’appliquer les règles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="6b0e3-112">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="6b0e3-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="6b0e3-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="6b0e3-114">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="6b0e3-114">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="6b0e3-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b0e3-115">Requirements</span></span>  
 <span data-ttu-id="6b0e3-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6b0e3-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6b0e3-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b0e3-117">See Also</span></span>  
 [<span data-ttu-id="6b0e3-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6b0e3-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)