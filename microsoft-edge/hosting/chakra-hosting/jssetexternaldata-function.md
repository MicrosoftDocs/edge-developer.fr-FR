---
description: Définit les données externes d’un objet externe.
title: Fonction JsSetExternalData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cc638905786a1baa0a3d5f79bfa3792a764f358f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566245"
---
# <span data-ttu-id="05982-103">Fonction JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="05982-103">JsSetExternalData Function</span></span>
<span data-ttu-id="05982-104">Définit les données externes d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="05982-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="05982-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="05982-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="05982-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="05982-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="05982-107">Objet externe.</span><span class="sxs-lookup"><span data-stu-id="05982-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="05982-108">Données externes stockées dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="05982-108">The external data stored in the object.</span></span> <span data-ttu-id="05982-109">Peut être null si aucune donnée externe n’est stockée dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="05982-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="05982-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="05982-110">Return Value</span></span>  
 <span data-ttu-id="05982-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="05982-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="05982-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="05982-112">Remarks</span></span>  
 <span data-ttu-id="05982-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="05982-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="05982-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05982-114">Requirements</span></span>  
 <span data-ttu-id="05982-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="05982-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="05982-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05982-116">See Also</span></span>  
 [<span data-ttu-id="05982-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="05982-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)