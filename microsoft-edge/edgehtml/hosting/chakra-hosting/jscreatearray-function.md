---
description: Crée un objet tableau JavaScript.
title: Fonction JsCreateArray | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateArray
helpviewer_keywords:
- JsCreateArray function
ms.assetid: a119949a-e427-4349-9d00-5ec20fb9319c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 34ce07055fa3d4d24188d7edbcedc3f08973e233
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232977"
---
# <span data-ttu-id="ca1e8-103">JsCreateArray Function</span><span class="sxs-lookup"><span data-stu-id="ca1e8-103">JsCreateArray Function</span></span>

<span data-ttu-id="ca1e8-104">Crée un objet tableau JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ca1e8-104">Creates a Javascript array object.</span></span>  
  
## <span data-ttu-id="ca1e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ca1e8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArray(  
   _In_ unsigned int length,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ca1e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ca1e8-106">Parameters</span></span>  
 `length`  
 <span data-ttu-id="ca1e8-107">Longueur initiale de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ca1e8-107">The initial length of the array.</span></span>  
  
 `result`  
 <span data-ttu-id="ca1e8-108">Nouvel objet tableau.</span><span class="sxs-lookup"><span data-stu-id="ca1e8-108">The new array object.</span></span>  
  
## <span data-ttu-id="ca1e8-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ca1e8-109">Return Value</span></span>  
 <span data-ttu-id="ca1e8-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ca1e8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ca1e8-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ca1e8-111">Remarks</span></span>  
 <span data-ttu-id="ca1e8-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ca1e8-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ca1e8-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ca1e8-113">Requirements</span></span>  
 <span data-ttu-id="ca1e8-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ca1e8-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ca1e8-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ca1e8-115">See Also</span></span>  
 [<span data-ttu-id="ca1e8-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ca1e8-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
