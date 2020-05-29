---
description: Crée une valeur booléenne à partir d’une `bool` valeur.
title: Fonction JsBoolToBoolean | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f795bdd02a2a21dc4a0c8948a76ef817d6e0fac6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565265"
---
# <span data-ttu-id="801a6-103">Fonction JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="801a6-103">JsBoolToBoolean Function</span></span>
<span data-ttu-id="801a6-104">Crée une valeur booléenne à partir d’une `bool` valeur.</span><span class="sxs-lookup"><span data-stu-id="801a6-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="801a6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="801a6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="801a6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="801a6-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="801a6-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="801a6-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="801a6-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="801a6-108">The converted value.</span></span>  
  
## <span data-ttu-id="801a6-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="801a6-109">Return Value</span></span>  
 <span data-ttu-id="801a6-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="801a6-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="801a6-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="801a6-111">Remarks</span></span>  
 <span data-ttu-id="801a6-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="801a6-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="801a6-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="801a6-113">Requirements</span></span>  
 <span data-ttu-id="801a6-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="801a6-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="801a6-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="801a6-115">See Also</span></span>  
 [<span data-ttu-id="801a6-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="801a6-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)