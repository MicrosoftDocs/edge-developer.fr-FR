---
description: Récupère les informations externes d’un objet.
title: Fonction JsGetIndexedPropertiesExternalData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 96fdcd4b6fe29ffc20a796983cc1de692c80a3f1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565186"
---
# <span data-ttu-id="56438-103">Fonction JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="56438-103">JsGetIndexedPropertiesExternalData Function</span></span>
<span data-ttu-id="56438-104">Récupère les informations externes d’un objet.</span><span class="sxs-lookup"><span data-stu-id="56438-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="56438-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56438-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="56438-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="56438-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="56438-107">Objet.</span><span class="sxs-lookup"><span data-stu-id="56438-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="56438-108">Magasin de stockage de données externes pour les propriétés indexées de l’objet.</span><span class="sxs-lookup"><span data-stu-id="56438-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="56438-109">Le type d’élément de tableau dans les données externes.</span><span class="sxs-lookup"><span data-stu-id="56438-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="56438-110">Nombre d’éléments de tableau de données externes.</span><span class="sxs-lookup"><span data-stu-id="56438-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="56438-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="56438-111">Return Value</span></span>  
 <span data-ttu-id="56438-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="56438-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="56438-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="56438-113">Remarks</span></span>  
 <span data-ttu-id="56438-114">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="56438-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="56438-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56438-115">Requirements</span></span>  
 <span data-ttu-id="56438-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="56438-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="56438-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56438-117">See Also</span></span>  
 [<span data-ttu-id="56438-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="56438-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)