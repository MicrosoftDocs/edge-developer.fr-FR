---
description: Crée un nouvel objet d’erreur SyntaxError JavaScript.
title: Fonction JsCreateSyntaxError | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7d6534bfa2b59cb2f6ab68c231d7a97c84876d62
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233329"
---
# <span data-ttu-id="c8a0d-103">JsCreateSyntaxError Function</span><span class="sxs-lookup"><span data-stu-id="c8a0d-103">JsCreateSyntaxError Function</span></span>

<span data-ttu-id="c8a0d-104">Crée un nouvel objet d’erreur SyntaxError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="c8a0d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8a0d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="c8a0d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8a0d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="c8a0d-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="c8a0d-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-108">The new error object.</span></span>  
  
## <span data-ttu-id="c8a0d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c8a0d-109">Return Value</span></span>  
 <span data-ttu-id="c8a0d-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c8a0d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8a0d-111">Remarks</span></span>  
 <span data-ttu-id="c8a0d-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c8a0d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c8a0d-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c8a0d-113">Requirements</span></span>  
 <span data-ttu-id="c8a0d-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c8a0d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c8a0d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8a0d-115">See Also</span></span>  
 [<span data-ttu-id="c8a0d-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c8a0d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
