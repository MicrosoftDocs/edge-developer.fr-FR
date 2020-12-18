---
description: Obtient l’ID de propriété associé au nom.
title: Fonction JsGetPropertyIdFromName | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyIdFromName
helpviewer_keywords:
- JsGetPropertyIdFromName function
ms.assetid: 1674906f-746a-4c62-99cd-023276683a86
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: adc8de4d55fa0c74ad191b4621ceb3a54026d02d
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233326"
---
# <span data-ttu-id="bf780-103">JsGetPropertyIdFromName Function</span><span class="sxs-lookup"><span data-stu-id="bf780-103">JsGetPropertyIdFromName Function</span></span>

<span data-ttu-id="bf780-104">Obtient l’ID de propriété associé au nom.</span><span class="sxs-lookup"><span data-stu-id="bf780-104">Gets the property ID associated with the name.</span></span>  
  
## <span data-ttu-id="bf780-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf780-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyIdFromName(  
   _In_z_ const wchar_t *name,  
   _Out_ JsPropertyIdRef *propertyId  
);  
```  
  
#### <span data-ttu-id="bf780-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf780-106">Parameters</span></span>  
 `name`  
 <span data-ttu-id="bf780-107">Nom de l’ID de propriété à obtenir ou à créer.</span><span class="sxs-lookup"><span data-stu-id="bf780-107">The name of the property ID to get or create.</span></span> <span data-ttu-id="bf780-108">Le nom ne se compose que de chiffres.</span><span class="sxs-lookup"><span data-stu-id="bf780-108">The name may consist of only digits.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="bf780-109">ID de propriété dans ce Runtime pour le nom donné.</span><span class="sxs-lookup"><span data-stu-id="bf780-109">The property ID in this runtime for the given name.</span></span>  
  
## <span data-ttu-id="bf780-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bf780-110">Return Value</span></span>  
 <span data-ttu-id="bf780-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="bf780-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bf780-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf780-112">Remarks</span></span>  
 <span data-ttu-id="bf780-113">Les ID de propriété sont spécifiques à un contexte et ne peuvent pas être utilisés dans les contextes.</span><span class="sxs-lookup"><span data-stu-id="bf780-113">Property IDs are specific to a context and cannot be used across contexts.</span></span>  
  
 <span data-ttu-id="bf780-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="bf780-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bf780-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="bf780-115">Requirements</span></span>  
 <span data-ttu-id="bf780-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bf780-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bf780-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf780-117">See Also</span></span>  
 [<span data-ttu-id="bf780-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bf780-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
