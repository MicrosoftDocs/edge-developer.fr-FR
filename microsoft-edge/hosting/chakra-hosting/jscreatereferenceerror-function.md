---
description: Crée un nouvel objet d’erreur ReferenceError JavaScript.
title: Fonction JsCreateReferenceError | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateReferenceError
helpviewer_keywords:
- JsCreateReferenceError function
ms.assetid: 1d0b2339-4bea-4dd0-a46a-4dcbf0be3bd8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 958af7111a233077aa7a2c2391b26666f55c634b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565224"
---
# <span data-ttu-id="c1d41-103">Fonction JsCreateReferenceError</span><span class="sxs-lookup"><span data-stu-id="c1d41-103">JsCreateReferenceError Function</span></span>
<span data-ttu-id="c1d41-104">Crée un nouvel objet d’erreur ReferenceError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c1d41-104">Creates a new JavaScript ReferenceError error object.</span></span>
  
## <span data-ttu-id="c1d41-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c1d41-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateReferenceError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="c1d41-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c1d41-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="c1d41-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c1d41-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="c1d41-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c1d41-108">The new error object.</span></span>  
  
## <span data-ttu-id="c1d41-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c1d41-109">Return Value</span></span>  
 <span data-ttu-id="c1d41-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c1d41-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c1d41-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1d41-111">Remarks</span></span>  
 <span data-ttu-id="c1d41-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c1d41-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="c1d41-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1d41-113">Requirements</span></span>  
 <span data-ttu-id="c1d41-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c1d41-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c1d41-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1d41-115">See Also</span></span>  
 [<span data-ttu-id="c1d41-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c1d41-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)