---
description: Crée une valeur JavaScript qui est une projection du `IInspectable` pointeur transmis.
title: Fonction JsInspectableToObject | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565166"
---
# <span data-ttu-id="77c0b-103">Fonction JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="77c0b-103">JsInspectableToObject Function</span></span>
<span data-ttu-id="77c0b-104">Crée une valeur JavaScript qui est une projection du `IInspectable` pointeur transmis.</span><span class="sxs-lookup"><span data-stu-id="77c0b-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="77c0b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77c0b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="77c0b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77c0b-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="77c0b-107">A `IInspectable` à projeter.</span><span class="sxs-lookup"><span data-stu-id="77c0b-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="77c0b-108">Valeur JavaScript qui est une projection de la `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="77c0b-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="77c0b-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="77c0b-109">Return Value</span></span>  
 <span data-ttu-id="77c0b-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="77c0b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="77c0b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="77c0b-111">Remarks</span></span>  
 <span data-ttu-id="77c0b-112">La valeur projetée peut être utilisée par le script pour appeler un objet WinRT.</span><span class="sxs-lookup"><span data-stu-id="77c0b-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="77c0b-113">Les hôtes sont chargés d’appliquer les règles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="77c0b-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="77c0b-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="77c0b-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="77c0b-115">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="77c0b-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="77c0b-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77c0b-116">Requirements</span></span>  
 <span data-ttu-id="77c0b-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="77c0b-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="77c0b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77c0b-118">See Also</span></span>  
 [<span data-ttu-id="77c0b-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="77c0b-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)