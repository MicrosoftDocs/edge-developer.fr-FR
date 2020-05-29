---
description: Obtient les propriétés fréquemment utilisées d’un tableau typé.
title: Fonction JsGetTypedArrayInfo | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b33b0c515733864c1849a08aa2f8dc6e884c22ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565167"
---
# <span data-ttu-id="ca24f-103">Fonction JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="ca24f-103">JsGetTypedArrayInfo Function</span></span>
<span data-ttu-id="ca24f-104">Obtient les propriétés fréquemment utilisées d’un tableau typé.</span><span class="sxs-lookup"><span data-stu-id="ca24f-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="ca24f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca24f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="ca24f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca24f-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="ca24f-107">Instance de tableau typé.</span><span class="sxs-lookup"><span data-stu-id="ca24f-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="ca24f-108">Type du tableau.</span><span class="sxs-lookup"><span data-stu-id="ca24f-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="ca24f-109">`ArrayBuffer`Magasin du tableau.</span><span class="sxs-lookup"><span data-stu-id="ca24f-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="ca24f-110">Décalage en octets du début de arrayBuffer référencé par le tableau.</span><span class="sxs-lookup"><span data-stu-id="ca24f-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="ca24f-111">Nombre d’octets dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="ca24f-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="ca24f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca24f-112">Return Value</span></span>  
 <span data-ttu-id="ca24f-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ca24f-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ca24f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca24f-114">Remarks</span></span>  
 <span data-ttu-id="ca24f-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ca24f-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ca24f-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca24f-116">Requirements</span></span>  
 <span data-ttu-id="ca24f-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ca24f-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ca24f-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca24f-118">See Also</span></span>  
 [<span data-ttu-id="ca24f-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ca24f-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)