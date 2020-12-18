---
description: Obtient la liste de toutes les propriétés de symbole sur l’objet.
title: Fonction JsGetOwnPropertySymbols | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d44da140f61a17d4cdc3a959c8fa7d017cbab1cc
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233342"
---
# <span data-ttu-id="96967-103">JsGetOwnPropertySymbols Function</span><span class="sxs-lookup"><span data-stu-id="96967-103">JsGetOwnPropertySymbols Function</span></span>

<span data-ttu-id="96967-104">Obtient la liste de toutes les propriétés de symbole sur l’objet.</span><span class="sxs-lookup"><span data-stu-id="96967-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="96967-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96967-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="96967-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96967-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="96967-107">Objet à partir duquel obtenir les symboles de propriété.</span><span class="sxs-lookup"><span data-stu-id="96967-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="96967-108">Tableau de symboles de propriété.</span><span class="sxs-lookup"><span data-stu-id="96967-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="96967-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="96967-109">Return Value</span></span>  
 <span data-ttu-id="96967-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="96967-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="96967-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="96967-111">Remarks</span></span>  
 <span data-ttu-id="96967-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="96967-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="96967-113">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="96967-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="96967-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="96967-114">Requirements</span></span>  
 <span data-ttu-id="96967-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="96967-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="96967-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96967-116">See Also</span></span>  
 [<span data-ttu-id="96967-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="96967-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
