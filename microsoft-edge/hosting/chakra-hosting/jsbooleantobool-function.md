---
description: Récupère la `bool` valeur d’une valeur booléenne.
title: Fonction JsBooleanToBool | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 55b0ef1278cbc73652fc8427e004cab002d76e5b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565267"
---
# <span data-ttu-id="4d364-103">Fonction JsBooleanToBool</span><span class="sxs-lookup"><span data-stu-id="4d364-103">JsBooleanToBool Function</span></span>
<span data-ttu-id="4d364-104">Récupère la `bool` valeur d’une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="4d364-104">Retrieves the `bool` value of a Boolean value.</span></span>  
  
## <span data-ttu-id="4d364-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4d364-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### <span data-ttu-id="4d364-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4d364-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="4d364-107">Valeur à convertir.</span><span class="sxs-lookup"><span data-stu-id="4d364-107">The value to be converted.</span></span>  
  
 `boolValue`  
 <span data-ttu-id="4d364-108">Valeur convertie.</span><span class="sxs-lookup"><span data-stu-id="4d364-108">The converted value.</span></span>  
  
## <span data-ttu-id="4d364-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4d364-109">Return Value</span></span>  
 <span data-ttu-id="4d364-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4d364-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4d364-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d364-111">Remarks</span></span>  
 <span data-ttu-id="4d364-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="4d364-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4d364-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d364-113">Requirements</span></span>  
 <span data-ttu-id="4d364-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4d364-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4d364-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d364-115">See Also</span></span>  
 [<span data-ttu-id="4d364-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4d364-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)