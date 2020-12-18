---
description: Crée un `ArrayBuffer` objet JavaScript.
title: Fonction JsCreateArrayBuffer | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 3bee44d77f78bd35705211c598db78ab09000c71
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232973"
---
# <span data-ttu-id="17a20-103">JsCreateArrayBuffer Function</span><span class="sxs-lookup"><span data-stu-id="17a20-103">JsCreateArrayBuffer Function</span></span>

<span data-ttu-id="17a20-104">Crée un `ArrayBuffer` objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17a20-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="17a20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17a20-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="17a20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17a20-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="17a20-107">Nombre d’octets dans le ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="17a20-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="17a20-108">Nouvel objet ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="17a20-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="17a20-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="17a20-109">Return Value</span></span>  
 <span data-ttu-id="17a20-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="17a20-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="17a20-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="17a20-111">Remarks</span></span>  
 <span data-ttu-id="17a20-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="17a20-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="17a20-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="17a20-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="17a20-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="17a20-114">Requirements</span></span>  
 <span data-ttu-id="17a20-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="17a20-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="17a20-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17a20-116">See Also</span></span>  
 [<span data-ttu-id="17a20-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="17a20-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
