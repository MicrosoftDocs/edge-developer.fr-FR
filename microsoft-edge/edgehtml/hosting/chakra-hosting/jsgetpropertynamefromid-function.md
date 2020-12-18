---
description: Obtient le nom associé à l’ID de propriété.
title: Fonction JsGetPropertyNameFromId | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 42061ab54a70fed571740961a909a6da17fb0733
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233188"
---
# <span data-ttu-id="26f11-103">JsGetPropertyNameFromId Function</span><span class="sxs-lookup"><span data-stu-id="26f11-103">JsGetPropertyNameFromId Function</span></span>

<span data-ttu-id="26f11-104">Obtient le nom associé à l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="26f11-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="26f11-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26f11-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="26f11-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26f11-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="26f11-107">ID de propriété pour obtenir le nom de.</span><span class="sxs-lookup"><span data-stu-id="26f11-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="26f11-108">Nom associé à l’ID de propriété.</span><span class="sxs-lookup"><span data-stu-id="26f11-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="26f11-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="26f11-109">Return Value</span></span>  
 <span data-ttu-id="26f11-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="26f11-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="26f11-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="26f11-111">Remarks</span></span>  
 <span data-ttu-id="26f11-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="26f11-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="26f11-113">Le tampon renvoyé est valide tant que le runtime est actif et ne peut pas être utilisé une fois le runtime supprimé.</span><span class="sxs-lookup"><span data-stu-id="26f11-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="26f11-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="26f11-114">Requirements</span></span>  
 <span data-ttu-id="26f11-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="26f11-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="26f11-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26f11-116">See Also</span></span>  
 [<span data-ttu-id="26f11-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="26f11-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
