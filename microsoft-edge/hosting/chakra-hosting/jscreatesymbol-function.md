---
description: Crée un symbole JavaScript.
title: Fonction JsCreateSymbol | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a4e634e6f0726ca32ad1056129186ce941edb77b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565218"
---
# <span data-ttu-id="9d59a-103">Fonction JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="9d59a-103">JsCreateSymbol Function</span></span>
<span data-ttu-id="9d59a-104">Crée un symbole JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9d59a-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="9d59a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d59a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="9d59a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d59a-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="9d59a-107">Description de la chaîne du symbole.</span><span class="sxs-lookup"><span data-stu-id="9d59a-107">The string description of the symbol.</span></span> <span data-ttu-id="9d59a-108">Peut être null.</span><span class="sxs-lookup"><span data-stu-id="9d59a-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="9d59a-109">Le nouveau symbole.</span><span class="sxs-lookup"><span data-stu-id="9d59a-109">The new symbol.</span></span>  
  
## <span data-ttu-id="9d59a-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d59a-110">Return Value</span></span>  
 <span data-ttu-id="9d59a-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9d59a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9d59a-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d59a-112">Remarks</span></span>  
 <span data-ttu-id="9d59a-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="9d59a-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9d59a-114">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9d59a-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="9d59a-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d59a-115">Requirements</span></span>  
 <span data-ttu-id="9d59a-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9d59a-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9d59a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d59a-117">See Also</span></span>  
 [<span data-ttu-id="9d59a-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9d59a-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)