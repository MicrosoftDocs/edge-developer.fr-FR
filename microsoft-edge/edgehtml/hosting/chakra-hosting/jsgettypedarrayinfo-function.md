---
description: Obtient les propriétés fréquemment utilisées d’un tableau typé.
title: Fonction JsGetTypedArrayInfo | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: fdc9a05a2aebdabfd0c8e95c848d3bd5f97e580a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233341"
---
# <span data-ttu-id="7c30b-103">JsGetTypedArrayInfo Function</span><span class="sxs-lookup"><span data-stu-id="7c30b-103">JsGetTypedArrayInfo Function</span></span>

<span data-ttu-id="7c30b-104">Obtient les propriétés fréquemment utilisées d’un tableau typé.</span><span class="sxs-lookup"><span data-stu-id="7c30b-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="7c30b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c30b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="7c30b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c30b-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="7c30b-107">Instance de tableau typé.</span><span class="sxs-lookup"><span data-stu-id="7c30b-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="7c30b-108">Type du tableau.</span><span class="sxs-lookup"><span data-stu-id="7c30b-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="7c30b-109">`ArrayBuffer`Magasin du tableau.</span><span class="sxs-lookup"><span data-stu-id="7c30b-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="7c30b-110">Décalage en octets du début de arrayBuffer référencé par le tableau.</span><span class="sxs-lookup"><span data-stu-id="7c30b-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="7c30b-111">Nombre d’octets dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="7c30b-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="7c30b-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7c30b-112">Return Value</span></span>  
 <span data-ttu-id="7c30b-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7c30b-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7c30b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7c30b-114">Remarks</span></span>  
 <span data-ttu-id="7c30b-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="7c30b-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7c30b-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="7c30b-116">Requirements</span></span>  
 <span data-ttu-id="7c30b-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7c30b-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7c30b-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c30b-118">See Also</span></span>  
 [<span data-ttu-id="7c30b-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7c30b-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
