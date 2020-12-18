---
description: Crée un nouvel objet d’erreur RangeError JavaScript.
title: Fonction JsCreateRangeError | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRangeError
helpviewer_keywords:
- JsCreateRangeError function
ms.assetid: 0ab05de7-57af-4cfd-9aa5-0a69a893cc97
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 72cf882d5f9517f0f05d9e3367283f5f531dbdb3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233140"
---
# <span data-ttu-id="17c98-103">JsCreateRangeError Function</span><span class="sxs-lookup"><span data-stu-id="17c98-103">JsCreateRangeError Function</span></span>

<span data-ttu-id="17c98-104">Crée un nouvel objet d’erreur RangeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17c98-104">Creates a new JavaScript RangeError error object.</span></span>
  
## <span data-ttu-id="17c98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="17c98-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateRangeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="17c98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="17c98-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="17c98-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="17c98-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="17c98-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="17c98-108">The new error object.</span></span>  
  
## <span data-ttu-id="17c98-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="17c98-109">Return Value</span></span>  
 <span data-ttu-id="17c98-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="17c98-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="17c98-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="17c98-111">Remarks</span></span>  
 <span data-ttu-id="17c98-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="17c98-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="17c98-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="17c98-113">Requirements</span></span>  
 <span data-ttu-id="17c98-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="17c98-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="17c98-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17c98-115">See Also</span></span>  
 [<span data-ttu-id="17c98-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="17c98-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
