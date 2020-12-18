---
description: Crée une valeur numérique à partir d’une `int` valeur.
title: Fonction JsIntToNumber | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 1393c4ac-7189-4e9c-8e54-b0e041c22112
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 24e861d1535ae79843fb35de8a047031a479fe16
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233357"
---
# <span data-ttu-id="b037b-103">JsIntToNumber Function</span><span class="sxs-lookup"><span data-stu-id="b037b-103">JsIntToNumber Function</span></span>

<span data-ttu-id="b037b-104">Crée une valeur numérique à partir d’une `int` valeur.</span><span class="sxs-lookup"><span data-stu-id="b037b-104">Creates a number value from an `int` value.</span></span>  
  
## <span data-ttu-id="b037b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b037b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIntToNumber(  
   _In_ int intValue,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="b037b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b037b-106">Parameters</span></span>  
 `intValue`  
 <span data-ttu-id="b037b-107">La `int` valeur à convertir en nombre.</span><span class="sxs-lookup"><span data-stu-id="b037b-107">The `int` to convert to a number value.</span></span>  
  
 `value`  
 <span data-ttu-id="b037b-108">Nouvelle valeur du numéro.</span><span class="sxs-lookup"><span data-stu-id="b037b-108">The new number value.</span></span>  
  
## <span data-ttu-id="b037b-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b037b-109">Return Value</span></span>  
 <span data-ttu-id="b037b-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b037b-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b037b-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="b037b-111">Remarks</span></span>  
 <span data-ttu-id="b037b-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="b037b-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b037b-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="b037b-113">Requirements</span></span>  
 <span data-ttu-id="b037b-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b037b-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b037b-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b037b-115">See Also</span></span>  
 [<span data-ttu-id="b037b-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b037b-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
