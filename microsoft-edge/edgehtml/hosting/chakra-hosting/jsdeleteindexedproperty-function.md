---
description: Supprimez la valeur à l’index spécifié d’un objet.
title: Fonction JsDeleteIndexedProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 1340b0204d3845d4a9bd3f18a58ec125a82d2bc0
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233321"
---
# <span data-ttu-id="80a05-103">JsDeleteIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="80a05-103">JsDeleteIndexedProperty Function</span></span>

<span data-ttu-id="80a05-104">Supprimez la valeur à l’index spécifié d’un objet.</span><span class="sxs-lookup"><span data-stu-id="80a05-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="80a05-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80a05-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="80a05-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80a05-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="80a05-107">Objet sur lequel travailler.</span><span class="sxs-lookup"><span data-stu-id="80a05-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="80a05-108">Index à supprimer.</span><span class="sxs-lookup"><span data-stu-id="80a05-108">The index to delete.</span></span>  
  
## <span data-ttu-id="80a05-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="80a05-109">Return Value</span></span>  
 <span data-ttu-id="80a05-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="80a05-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="80a05-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="80a05-111">Remarks</span></span>  
 <span data-ttu-id="80a05-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="80a05-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="80a05-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="80a05-113">Requirements</span></span>  
 <span data-ttu-id="80a05-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="80a05-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="80a05-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80a05-115">See Also</span></span>  
 [<span data-ttu-id="80a05-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="80a05-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
