---
description: Obtient la liste de toutes les propriétés de symbole sur l’objet.
title: Fonction JsGetOwnPropertySymbols | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7a7f4e88986a45fbccfae0c53e92ff2e5313991
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566317"
---
# <span data-ttu-id="e2738-103">Fonction JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="e2738-103">JsGetOwnPropertySymbols Function</span></span>
<span data-ttu-id="e2738-104">Obtient la liste de toutes les propriétés de symbole sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="e2738-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="e2738-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2738-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="e2738-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2738-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e2738-107">Objet à partir duquel obtenir les symboles de propriété.</span><span class="sxs-lookup"><span data-stu-id="e2738-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="e2738-108">Tableau de symboles de propriété.</span><span class="sxs-lookup"><span data-stu-id="e2738-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="e2738-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2738-109">Return Value</span></span>  
 <span data-ttu-id="e2738-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e2738-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e2738-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2738-111">Remarks</span></span>  
 <span data-ttu-id="e2738-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="e2738-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e2738-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e2738-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="e2738-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2738-114">Requirements</span></span>  
 <span data-ttu-id="e2738-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e2738-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e2738-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2738-116">See Also</span></span>  
 [<span data-ttu-id="e2738-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e2738-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)