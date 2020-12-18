---
description: Crée un nouvel objet d’erreur TypeError JavaScript.
title: Fonction JsCreateTypeError | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 627dfdc6f01f0708366720a957b3784fc7bb59a4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233325"
---
# <span data-ttu-id="d0c98-103">JsCreateTypeError Function</span><span class="sxs-lookup"><span data-stu-id="d0c98-103">JsCreateTypeError Function</span></span>

<span data-ttu-id="d0c98-104">Crée un nouvel objet d’erreur TypeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d0c98-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="d0c98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d0c98-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="d0c98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d0c98-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="d0c98-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d0c98-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="d0c98-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d0c98-108">The new error object.</span></span>  
  
## <span data-ttu-id="d0c98-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d0c98-109">Return Value</span></span>  
 <span data-ttu-id="d0c98-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d0c98-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d0c98-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="d0c98-111">Remarks</span></span>  
 <span data-ttu-id="d0c98-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d0c98-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="d0c98-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="d0c98-113">Requirements</span></span>  
 <span data-ttu-id="d0c98-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d0c98-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d0c98-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0c98-115">See Also</span></span>  
 [<span data-ttu-id="d0c98-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d0c98-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
