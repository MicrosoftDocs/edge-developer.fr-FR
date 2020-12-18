---
description: Crée un objet de tableau typé JavaScript.
title: Fonction JsCreateTypedArray | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 62f62296d81dafe6515f69a990e33ff5c00730e1
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233328"
---
# <span data-ttu-id="75a53-103">JsCreateTypedArray Function</span><span class="sxs-lookup"><span data-stu-id="75a53-103">JsCreateTypedArray Function</span></span>

<span data-ttu-id="75a53-104">Crée un objet de tableau typé JavaScript.</span><span class="sxs-lookup"><span data-stu-id="75a53-104">Creates a JavaScript typed array object.</span></span>  
  
## <span data-ttu-id="75a53-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75a53-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="75a53-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75a53-106">Parameters</span></span>  
 `arrayType`  
 <span data-ttu-id="75a53-107">Type du tableau à créer.</span><span class="sxs-lookup"><span data-stu-id="75a53-107">The type of the array to create.</span></span>  
  
 `baseArray`  
 <span data-ttu-id="75a53-108">Tableau de base du nouveau tableau.</span><span class="sxs-lookup"><span data-stu-id="75a53-108">The base array of the new array.</span></span> <span data-ttu-id="75a53-109">Utilisez ce `JS_INVALID_REFERENCE` numéro si aucune matrice de base n’est utilisée.</span><span class="sxs-lookup"><span data-stu-id="75a53-109">Use `JS_INVALID_REFERENCE` if no base array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="75a53-110">Décalage en octets du début de `baseArray` () du `ArrayBuffer` tableau tapé pour le résultat à référencer.</span><span class="sxs-lookup"><span data-stu-id="75a53-110">The offset in bytes from the start of `baseArray` (`ArrayBuffer`) for result typed array to reference.</span></span> <span data-ttu-id="75a53-111">Applicable uniquement lorsqu' `baseArray` il s’agit d’un `ArrayBuffer` objet.</span><span class="sxs-lookup"><span data-stu-id="75a53-111">Only applicable when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="75a53-112">Doit être zéro dans le cas présent.</span><span class="sxs-lookup"><span data-stu-id="75a53-112">Must be 0 otherwise.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="75a53-113">Nombre d’éléments de la matrice.</span><span class="sxs-lookup"><span data-stu-id="75a53-113">The number of elements in the array.</span></span> <span data-ttu-id="75a53-114">Applicable uniquement lors de la création d’un tableau typé sans `baseArray` ( `baseArray` is `JS_INVALID_REFERENCE` ) ou lorsqu' `baseArray` il s’agit d’un `ArrayBuffer` objet.</span><span class="sxs-lookup"><span data-stu-id="75a53-114">Only applicable when creating a new typed array without `baseArray` (`baseArray` is `JS_INVALID_REFERENCE`) or when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="75a53-115">Doit être zéro dans le cas présent.</span><span class="sxs-lookup"><span data-stu-id="75a53-115">Must be 0 otherwise.</span></span>  
  
 `result`  
 <span data-ttu-id="75a53-116">Nouvel objet de tableau typé.</span><span class="sxs-lookup"><span data-stu-id="75a53-116">The new typed array object.</span></span>  
  
## <span data-ttu-id="75a53-117">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75a53-117">Return Value</span></span>  
 <span data-ttu-id="75a53-118">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="75a53-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="75a53-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="75a53-119">Remarks</span></span>  
 <span data-ttu-id="75a53-120">Il `baseArray` peut s’agir d’un, d’un `ArrayBuffer` autre tableau typé ou d’un code JavaScript `Array` .</span><span class="sxs-lookup"><span data-stu-id="75a53-120">The `baseArray` can be an `ArrayBuffer`, another typed array, or a JavaScript `Array`.</span></span> <span data-ttu-id="75a53-121">Le tableau typé retourné utilise le `baseArray` cas échéant `ArrayBuffer` , ou crée et utilise une copie du tableau source sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="75a53-121">The returned typed array will use the `baseArray` if it is an `ArrayBuffer`, or otherwise create and use a copy of the underlying source array.</span></span>  
  
 <span data-ttu-id="75a53-122">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="75a53-122">Requires an active script context.</span></span>  
  
 <span data-ttu-id="75a53-123">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="75a53-123">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="75a53-124">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="75a53-124">Requirements</span></span>  
 <span data-ttu-id="75a53-125">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="75a53-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="75a53-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="75a53-126">See Also</span></span>  
 [<span data-ttu-id="75a53-127">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="75a53-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
