---
description: Définit la propriété propre d’un nouvel objet à partir d’un descripteur de propriété.
title: Fonction JsDefineProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDefineProperty
helpviewer_keywords:
- JsDefineProperty function
ms.assetid: b2cf48d6-eb40-457c-aa8b-b16a50dc5d6a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c9641b4d00540670b44d1718a6aa2aca3b02de
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565209"
---
# <span data-ttu-id="54d1a-103">Fonction JsDefineProperty</span><span class="sxs-lookup"><span data-stu-id="54d1a-103">JsDefineProperty Function</span></span>
<span data-ttu-id="54d1a-104">Définit la propriété propre d’un nouvel objet à partir d’un descripteur de propriété.</span><span class="sxs-lookup"><span data-stu-id="54d1a-104">Defines a new object's own property from a property descriptor.</span></span>  
  
## <span data-ttu-id="54d1a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54d1a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDefineProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef propertyDescriptor,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="54d1a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54d1a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="54d1a-107">Objet qui comporte la propriété.</span><span class="sxs-lookup"><span data-stu-id="54d1a-107">The object that has the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="54d1a-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="54d1a-108">The ID of the property.</span></span>  
  
 `propertyDescriptor`  
 <span data-ttu-id="54d1a-109">Le descripteur de propriété.</span><span class="sxs-lookup"><span data-stu-id="54d1a-109">The property descriptor.</span></span>  
  
 `result`  
 <span data-ttu-id="54d1a-110">Si la propriété a été définie.</span><span class="sxs-lookup"><span data-stu-id="54d1a-110">Whether the property was defined.</span></span>  
  
## <span data-ttu-id="54d1a-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="54d1a-111">Return Value</span></span>  
 <span data-ttu-id="54d1a-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="54d1a-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="54d1a-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="54d1a-113">Remarks</span></span>  
 <span data-ttu-id="54d1a-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="54d1a-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="54d1a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54d1a-115">Requirements</span></span>  
 <span data-ttu-id="54d1a-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="54d1a-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="54d1a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54d1a-117">See Also</span></span>  
 [<span data-ttu-id="54d1a-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="54d1a-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)