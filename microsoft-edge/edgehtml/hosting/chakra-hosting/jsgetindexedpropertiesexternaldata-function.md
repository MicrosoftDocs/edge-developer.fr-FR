---
description: Récupère les informations externes d’un objet.
title: Fonction JsGetIndexedPropertiesExternalData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627aaef48def2e042927467e1cbb6d6b7c06a525
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232806"
---
# <span data-ttu-id="88d6b-103">JsGetIndexedPropertiesExternalData Function</span><span class="sxs-lookup"><span data-stu-id="88d6b-103">JsGetIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="88d6b-104">Récupère les informations externes d’un objet.</span><span class="sxs-lookup"><span data-stu-id="88d6b-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="88d6b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88d6b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="88d6b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88d6b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="88d6b-107">Objet.</span><span class="sxs-lookup"><span data-stu-id="88d6b-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="88d6b-108">Magasin de stockage de données externes pour les propriétés indexées de l’objet.</span><span class="sxs-lookup"><span data-stu-id="88d6b-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="88d6b-109">Le type d’élément de tableau dans les données externes.</span><span class="sxs-lookup"><span data-stu-id="88d6b-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="88d6b-110">Nombre d’éléments de tableau de données externes.</span><span class="sxs-lookup"><span data-stu-id="88d6b-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="88d6b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="88d6b-111">Return Value</span></span>  
 <span data-ttu-id="88d6b-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="88d6b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="88d6b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="88d6b-113">Remarks</span></span>  
 <span data-ttu-id="88d6b-114">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="88d6b-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="88d6b-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="88d6b-115">Requirements</span></span>  
 <span data-ttu-id="88d6b-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="88d6b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="88d6b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88d6b-117">See Also</span></span>  
 [<span data-ttu-id="88d6b-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="88d6b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
