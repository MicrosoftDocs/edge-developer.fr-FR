---
description: Effectue un `instanceof` test d’opérateur JavaScript.
title: Fonction JsInstanceOf | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d8aec1d4512fe937d1fd48aa6f3e88294bf9850c
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233356"
---
# <span data-ttu-id="25c41-103">JsInstanceOf Function</span><span class="sxs-lookup"><span data-stu-id="25c41-103">JsInstanceOf Function</span></span>

<span data-ttu-id="25c41-104">Effectue un `instanceof` test d’opérateur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="25c41-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="25c41-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="25c41-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="25c41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="25c41-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="25c41-107">Objet à tester.</span><span class="sxs-lookup"><span data-stu-id="25c41-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="25c41-108">Fonction Constructor à tester.</span><span class="sxs-lookup"><span data-stu-id="25c41-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="25c41-109">La valeur de la propriété «Object instanceof Constructor».</span><span class="sxs-lookup"><span data-stu-id="25c41-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="25c41-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="25c41-110">Return Value</span></span>  
 <span data-ttu-id="25c41-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="25c41-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="25c41-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="25c41-112">Remarks</span></span>  
 <span data-ttu-id="25c41-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="25c41-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="25c41-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="25c41-114">Requirements</span></span>  
 <span data-ttu-id="25c41-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="25c41-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="25c41-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25c41-116">See Also</span></span>  
 [<span data-ttu-id="25c41-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="25c41-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
