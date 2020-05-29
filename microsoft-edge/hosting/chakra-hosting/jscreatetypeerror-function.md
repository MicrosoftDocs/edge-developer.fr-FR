---
description: Crée un nouvel objet d’erreur TypeError JavaScript.
title: Fonction JsCreateTypeError | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateTypeError
helpviewer_keywords:
- JsCreateTypeError function
ms.assetid: 8ef7bb77-2c98-482a-bccb-1f0fe2b826f5
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 302bf75af3668dfdd0b40336e940e3eef3a74bce
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565212"
---
# <span data-ttu-id="dd0e7-103">Fonction JsCreateTypeError</span><span class="sxs-lookup"><span data-stu-id="dd0e7-103">JsCreateTypeError Function</span></span>
<span data-ttu-id="dd0e7-104">Crée un nouvel objet d’erreur TypeError JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dd0e7-104">Creates a new JavaScript TypeError error object.</span></span>  
  
## <span data-ttu-id="dd0e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd0e7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypeError(  
   _In_ JsValueRef message,  
   _Out_ JsValueRef *error  
);  
```  
  
#### <span data-ttu-id="dd0e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd0e7-106">Parameters</span></span>  
 `message`  
 <span data-ttu-id="dd0e7-107">Message de l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dd0e7-107">Message for the error object.</span></span>  
  
 `error`  
 <span data-ttu-id="dd0e7-108">Nouvel objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="dd0e7-108">The new error object.</span></span>  
  
## <span data-ttu-id="dd0e7-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd0e7-109">Return Value</span></span>  
 <span data-ttu-id="dd0e7-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dd0e7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dd0e7-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd0e7-111">Remarks</span></span>  
 <span data-ttu-id="dd0e7-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="dd0e7-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dd0e7-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd0e7-113">Requirements</span></span>  
 <span data-ttu-id="dd0e7-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dd0e7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dd0e7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd0e7-115">See Also</span></span>  
 [<span data-ttu-id="dd0e7-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dd0e7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)