---
description: Définit les propriétés indexées d’un objet sur des données externes. Les données externes seront utilisées comme magasin back pour les propriétés indexées de l’objet et consultées comme un tableau typé.
title: Fonction JsSetIndexedPropertiesToExternalData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c1aed6e194b1dc1c35f403626a7b6c02a7752ffb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566242"
---
# <span data-ttu-id="5cf53-104">Fonction JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="5cf53-104">JsSetIndexedPropertiesToExternalData Function</span></span>
<span data-ttu-id="5cf53-105">Définit les propriétés indexées d’un objet sur des données externes.</span><span class="sxs-lookup"><span data-stu-id="5cf53-105">Sets an object's indexed properties to external data.</span></span> <span data-ttu-id="5cf53-106">Les données externes seront utilisées comme magasin back pour les propriétés indexées de l’objet et consultées comme un tableau typé.</span><span class="sxs-lookup"><span data-stu-id="5cf53-106">The external data will be used as back store for the object's indexed properties and accessed like a typed array.</span></span>  
  
## <span data-ttu-id="5cf53-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5cf53-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### <span data-ttu-id="5cf53-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5cf53-108">Parameters</span></span>  
 `object`  
 <span data-ttu-id="5cf53-109">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="5cf53-109">The object to operate on.</span></span>  
  
 `data`  
 <span data-ttu-id="5cf53-110">Données externes à utiliser en tant que magasin back pour les propriétés indexées de l’objet.</span><span class="sxs-lookup"><span data-stu-id="5cf53-110">The external data to be used as back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="5cf53-111">Le type d’élément de tableau dans les données externes.</span><span class="sxs-lookup"><span data-stu-id="5cf53-111">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="5cf53-112">Nombre d’éléments de tableau de données externes.</span><span class="sxs-lookup"><span data-stu-id="5cf53-112">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="5cf53-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5cf53-113">Return Value</span></span>  
 <span data-ttu-id="5cf53-114">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5cf53-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5cf53-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="5cf53-115">Remarks</span></span>  
 <span data-ttu-id="5cf53-116">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="5cf53-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="5cf53-117">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="5cf53-117">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="5cf53-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cf53-118">Requirements</span></span>  
 <span data-ttu-id="5cf53-119">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5cf53-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5cf53-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cf53-120">See Also</span></span>  
 [<span data-ttu-id="5cf53-121">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5cf53-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)