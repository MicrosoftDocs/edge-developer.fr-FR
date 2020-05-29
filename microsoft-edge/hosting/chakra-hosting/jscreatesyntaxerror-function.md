---
description: Crée un nouvel objet d’erreur SyntaxError JavaScript.
title: Fonction JsCreateSyntaxError | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateSyntaxError
helpviewer_keywords:
- JsCreateSyntaxError function
ms.assetid: 839845fc-60c4-4ffc-bfcc-fd7a8f06126f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 8f7459e8300df56aa8ccfaa78ef97ce2b6ec6fa0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565215"
---
# <span data-ttu-id="0d19d-103">Fonction JsCreateSyntaxError</span><span class="sxs-lookup"><span data-stu-id="0d19d-103">JsCreateSyntaxError Function</span></span>
<span data-ttu-id="0d19d-104">Crée un nouvel objet d’erreur SyntaxError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0d19d-104">Creates a new JavaScript SyntaxError error object.</span></span>  
  
## <span data-ttu-id="0d19d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d19d-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSyntaxError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="0d19d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0d19d-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="0d19d-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0d19d-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="0d19d-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0d19d-108">The new error object.</span></span>  
  
## <span data-ttu-id="0d19d-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0d19d-109">Return Value</span></span>  
 <span data-ttu-id="0d19d-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0d19d-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0d19d-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="0d19d-111">Remarks</span></span>  
 <span data-ttu-id="0d19d-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="0d19d-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0d19d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d19d-113">Requirements</span></span>  
 <span data-ttu-id="0d19d-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0d19d-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0d19d-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d19d-115">See Also</span></span>  
 [<span data-ttu-id="0d19d-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0d19d-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)