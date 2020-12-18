---
description: Crée un nouvel objet d’erreur URIError JavaScript.
title: Fonction JsCreateURIError | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateURIError
helpviewer_keywords:
- JsCreateURIError function
ms.assetid: 711fd237-12a2-4ff0-b58a-ad74c91e79fb
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 88e6c1fc04607b3be088e297d1fa86f9374bcb03
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233113"
---
# <span data-ttu-id="70929-103">JsCreateURIError Function</span><span class="sxs-lookup"><span data-stu-id="70929-103">JsCreateURIError Function</span></span>

<span data-ttu-id="70929-104">Crée un nouvel objet d’erreur URIError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="70929-104">Creates a new JavaScript URIError error object.</span></span>  
  
## <span data-ttu-id="70929-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70929-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateURIError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="70929-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="70929-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="70929-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="70929-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="70929-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="70929-108">The new error object.</span></span>  
  
## <span data-ttu-id="70929-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="70929-109">Return Value</span></span>  
 <span data-ttu-id="70929-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="70929-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="70929-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="70929-111">Remarks</span></span>  
 <span data-ttu-id="70929-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="70929-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="70929-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="70929-113">Requirements</span></span>  
 <span data-ttu-id="70929-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="70929-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="70929-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70929-115">See Also</span></span>  
 [<span data-ttu-id="70929-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="70929-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
