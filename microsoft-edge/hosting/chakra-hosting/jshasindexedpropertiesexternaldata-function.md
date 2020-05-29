---
description: Détermine si un objet possède ses propriétés indexées dans les données externes.
title: Fonction JsHasIndexedPropertiesExternalData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7f9f87b19016b3d837b637219eec936a11211e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566299"
---
# <span data-ttu-id="80665-103">Fonction JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="80665-103">JsHasIndexedPropertiesExternalData Function</span></span>
<span data-ttu-id="80665-104">Détermine si un objet possède ses propriétés indexées dans les données externes.</span><span class="sxs-lookup"><span data-stu-id="80665-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="80665-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80665-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="80665-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80665-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="80665-107">Objet.</span><span class="sxs-lookup"><span data-stu-id="80665-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="80665-108">Si l’objet possède ses propriétés indexées dans les données externes.</span><span class="sxs-lookup"><span data-stu-id="80665-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="80665-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="80665-109">Return Value</span></span>  
 <span data-ttu-id="80665-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="80665-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="80665-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="80665-111">Remarks</span></span>  
 <span data-ttu-id="80665-112">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="80665-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="80665-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80665-113">Requirements</span></span>  
 <span data-ttu-id="80665-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="80665-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="80665-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80665-115">See Also</span></span>  
 [<span data-ttu-id="80665-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="80665-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)