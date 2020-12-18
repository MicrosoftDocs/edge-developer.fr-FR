---
description: Rappel de fonction.
title: JsNativeFunction typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 891fe55f776e8519a5d3c187104b2bc326336482
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232797"
---
# <span data-ttu-id="d45a1-103">Typedef JsNativeFunction</span><span class="sxs-lookup"><span data-stu-id="d45a1-103">JsNativeFunction Typedef</span></span>

<span data-ttu-id="d45a1-104">Rappel de fonction.</span><span class="sxs-lookup"><span data-stu-id="d45a1-104">A function callback.</span></span>  
  
## <span data-ttu-id="d45a1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d45a1-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="d45a1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d45a1-106">Parameters</span></span>  
 <span data-ttu-id="d45a1-107">l ʼ</span><span class="sxs-lookup"><span data-stu-id="d45a1-107">callee</span></span>  
 <span data-ttu-id="d45a1-108">`Function`Objet qui représente la fonction appelée.</span><span class="sxs-lookup"><span data-stu-id="d45a1-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="d45a1-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="d45a1-109">isConstructCall</span></span>  
 <span data-ttu-id="d45a1-110">Indique s’il s’agit d’un appel régulier ou d’un nouvel appel.</span><span class="sxs-lookup"><span data-stu-id="d45a1-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="d45a1-111">arguments</span><span class="sxs-lookup"><span data-stu-id="d45a1-111">arguments</span></span>  
 <span data-ttu-id="d45a1-112">Les arguments de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d45a1-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="d45a1-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="d45a1-113">argumentCount</span></span>  
 <span data-ttu-id="d45a1-114">Nombre d’arguments.</span><span class="sxs-lookup"><span data-stu-id="d45a1-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="d45a1-115">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="d45a1-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="d45a1-116">Le résultat de l’appel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="d45a1-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="d45a1-117">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="d45a1-117">Requirements</span></span>  
 <span data-ttu-id="d45a1-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d45a1-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d45a1-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d45a1-119">See Also</span></span>  
 [<span data-ttu-id="d45a1-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d45a1-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
