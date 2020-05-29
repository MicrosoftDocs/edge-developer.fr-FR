---
description: Crée un nouvel objet d’erreur JavaScript.
title: Fonction JsCreateError | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateError
helpviewer_keywords:
- JsCreateError function
ms.assetid: dadbcac8-c56f-4f30-ba00-2d284daee191
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 33d70e3f077b085ccb4ab541d3246d777ea68978
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565237"
---
# <span data-ttu-id="0a9f6-103">Fonction JsCreateError</span><span class="sxs-lookup"><span data-stu-id="0a9f6-103">JsCreateError Function</span></span>
<span data-ttu-id="0a9f6-104">Crée un nouvel objet d’erreur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-104">Creates a new JavaScript error object.</span></span>  
  
## <span data-ttu-id="0a9f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a9f6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="0a9f6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a9f6-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="0a9f6-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="0a9f6-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-108">The new error object.</span></span>  
  
## <span data-ttu-id="0a9f6-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="0a9f6-109">Return Value</span></span>  
 <span data-ttu-id="0a9f6-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0a9f6-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="0a9f6-111">Remarks</span></span>  
 <span data-ttu-id="0a9f6-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="0a9f6-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="0a9f6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a9f6-113">Requirements</span></span>  
 <span data-ttu-id="0a9f6-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0a9f6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0a9f6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a9f6-115">See Also</span></span>  
 [<span data-ttu-id="0a9f6-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0a9f6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)