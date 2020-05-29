---
description: Rappel de fonction.
title: JsNativeFunction typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565153"
---
# <span data-ttu-id="61550-103">JsNativeFunction typedef</span><span class="sxs-lookup"><span data-stu-id="61550-103">JsNativeFunction Typedef</span></span>
<span data-ttu-id="61550-104">Rappel de fonction.</span><span class="sxs-lookup"><span data-stu-id="61550-104">A function callback.</span></span>  
  
## <span data-ttu-id="61550-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61550-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="61550-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61550-106">Parameters</span></span>  
 <span data-ttu-id="61550-107">l ʼ</span><span class="sxs-lookup"><span data-stu-id="61550-107">callee</span></span>  
 <span data-ttu-id="61550-108">`Function`Objet qui représente la fonction appelée.</span><span class="sxs-lookup"><span data-stu-id="61550-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="61550-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="61550-109">isConstructCall</span></span>  
 <span data-ttu-id="61550-110">Indique s’il s’agit d’un appel régulier ou d’un nouvel appel.</span><span class="sxs-lookup"><span data-stu-id="61550-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="61550-111">arguments</span><span class="sxs-lookup"><span data-stu-id="61550-111">arguments</span></span>  
 <span data-ttu-id="61550-112">Les arguments de l’appel.</span><span class="sxs-lookup"><span data-stu-id="61550-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="61550-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="61550-113">argumentCount</span></span>  
 <span data-ttu-id="61550-114">Nombre d’arguments.</span><span class="sxs-lookup"><span data-stu-id="61550-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="61550-115">Valeur de propriété/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="61550-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="61550-116">Le résultat de l’appel, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="61550-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="61550-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="61550-117">Requirements</span></span>  
 <span data-ttu-id="61550-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="61550-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="61550-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="61550-119">See Also</span></span>  
 [<span data-ttu-id="61550-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="61550-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)