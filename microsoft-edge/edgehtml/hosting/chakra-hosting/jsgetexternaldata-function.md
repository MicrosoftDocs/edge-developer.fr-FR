---
description: Extrait les données d’un objet externe.
title: Fonction JsGetExternalData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d046b5c515b1a688cd527fdc0eb9cd173eb47570
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233220"
---
# <span data-ttu-id="90eab-103">JsGetExternalData Function</span><span class="sxs-lookup"><span data-stu-id="90eab-103">JsGetExternalData Function</span></span>

<span data-ttu-id="90eab-104">Extrait les données d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="90eab-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="90eab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90eab-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="90eab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90eab-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="90eab-107">Objet externe.</span><span class="sxs-lookup"><span data-stu-id="90eab-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="90eab-108">Données externes stockées dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="90eab-108">The external data stored in the object.</span></span> <span data-ttu-id="90eab-109">Peut être null si aucune donnée externe n’est stockée dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="90eab-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="90eab-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="90eab-110">Return Value</span></span>  
 <span data-ttu-id="90eab-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="90eab-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="90eab-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="90eab-112">Remarks</span></span>  
 <span data-ttu-id="90eab-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="90eab-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="90eab-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="90eab-114">Requirements</span></span>  
 <span data-ttu-id="90eab-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="90eab-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="90eab-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90eab-116">See Also</span></span>  
 [<span data-ttu-id="90eab-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="90eab-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
