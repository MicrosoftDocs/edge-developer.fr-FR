---
description: Crée un `ArrayBuffer` objet JavaScript.
title: Fonction JsCreateArrayBuffer | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7e81c50317de5243fbcdf761c09c084f97a8e1e0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565246"
---
# <span data-ttu-id="c8421-103">Fonction JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="c8421-103">JsCreateArrayBuffer Function</span></span>
<span data-ttu-id="c8421-104">Crée un `ArrayBuffer` objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c8421-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="c8421-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8421-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="c8421-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8421-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="c8421-107">Nombre d’octets dans le ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="c8421-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="c8421-108">Nouvel objet ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="c8421-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="c8421-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c8421-109">Return Value</span></span>  
 <span data-ttu-id="c8421-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c8421-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c8421-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8421-111">Remarks</span></span>  
 <span data-ttu-id="c8421-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c8421-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c8421-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c8421-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="c8421-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8421-114">Requirements</span></span>  
 <span data-ttu-id="c8421-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c8421-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c8421-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8421-116">See Also</span></span>  
 [<span data-ttu-id="c8421-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c8421-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)