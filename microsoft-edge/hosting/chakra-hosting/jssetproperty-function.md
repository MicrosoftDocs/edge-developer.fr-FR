---
description: Place la propriété d’un objet.
title: Fonction JsSetProperty | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetProperty
helpviewer_keywords:
- JsSetProperty function
ms.assetid: 2c36bebf-ec86-425c-8131-2dd75fd30f40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2aba03a73f35284f79355a7d93161d9a9518012c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566234"
---
# <span data-ttu-id="3b27b-103">Fonction JsSetProperty</span><span class="sxs-lookup"><span data-stu-id="3b27b-103">JsSetProperty Function</span></span>
<span data-ttu-id="3b27b-104">Place la propriété d’un objet.</span><span class="sxs-lookup"><span data-stu-id="3b27b-104">Puts an object's property.</span></span>  
  
## <span data-ttu-id="3b27b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b27b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ JsValueRef value,  
   _In_ bool useStrictRules  
);  
```  
  
#### <span data-ttu-id="3b27b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3b27b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="3b27b-107">Objet qui contient la propriété.</span><span class="sxs-lookup"><span data-stu-id="3b27b-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="3b27b-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="3b27b-108">The ID of the property.</span></span>  
  
 `value`  
 <span data-ttu-id="3b27b-109">Nouvelle valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="3b27b-109">The new value of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="3b27b-110">Le jeu de propriétés doit suivre des règles en mode strict.</span><span class="sxs-lookup"><span data-stu-id="3b27b-110">The property set should follow strict mode rules.</span></span>  
  
## <span data-ttu-id="3b27b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3b27b-111">Return Value</span></span>  
 <span data-ttu-id="3b27b-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="3b27b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3b27b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="3b27b-113">Remarks</span></span>  
 <span data-ttu-id="3b27b-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="3b27b-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="3b27b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b27b-115">Requirements</span></span>  
 <span data-ttu-id="3b27b-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3b27b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3b27b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3b27b-117">See Also</span></span>  
 [<span data-ttu-id="3b27b-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3b27b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)