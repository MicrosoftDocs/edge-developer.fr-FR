---
description: Crée un nouvel objet d’erreur JavaScript.
title: Fonction JsCreateError | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: cd2fd0172902cc6dc8a4dd169eef5947d0b25256
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232975"
---
# <span data-ttu-id="a6720-103">JsCreateError Function</span><span class="sxs-lookup"><span data-stu-id="a6720-103">JsCreateError Function</span></span>

<span data-ttu-id="a6720-104">Crée un nouvel objet d’erreur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a6720-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="a6720-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a6720-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="a6720-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a6720-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="a6720-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a6720-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="a6720-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="a6720-108">The new error object.</span></span>  
  
## <span data-ttu-id="a6720-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a6720-109">Return Value</span></span>  
 <span data-ttu-id="a6720-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a6720-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a6720-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a6720-111">Remarks</span></span>  
 <span data-ttu-id="a6720-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="a6720-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a6720-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="a6720-113">Requirements</span></span>  
 <span data-ttu-id="a6720-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a6720-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a6720-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a6720-115">See Also</span></span>  
 [<span data-ttu-id="a6720-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a6720-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
