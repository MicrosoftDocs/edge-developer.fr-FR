---
description: Définit les données externes d’un objet externe.
title: Fonction JsSetExternalData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f2ebdce4448a14f145ce5aafe6ba412f7db26c17
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233290"
---
# <span data-ttu-id="5f9fb-103">JsSetExternalData Function</span><span class="sxs-lookup"><span data-stu-id="5f9fb-103">JsSetExternalData Function</span></span>

<span data-ttu-id="5f9fb-104">Définit les données externes d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="5f9fb-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="5f9fb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f9fb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="5f9fb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f9fb-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="5f9fb-107">Objet externe.</span><span class="sxs-lookup"><span data-stu-id="5f9fb-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="5f9fb-108">Données externes stockées dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="5f9fb-108">The external data stored in the object.</span></span> <span data-ttu-id="5f9fb-109">Peut être null si aucune donnée externe n’est stockée dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="5f9fb-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="5f9fb-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5f9fb-110">Return Value</span></span>  
 <span data-ttu-id="5f9fb-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="5f9fb-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="5f9fb-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="5f9fb-112">Remarks</span></span>  
 <span data-ttu-id="5f9fb-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="5f9fb-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="5f9fb-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="5f9fb-114">Requirements</span></span>  
 <span data-ttu-id="5f9fb-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5f9fb-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="5f9fb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f9fb-116">See Also</span></span>  
 [<span data-ttu-id="5f9fb-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5f9fb-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
