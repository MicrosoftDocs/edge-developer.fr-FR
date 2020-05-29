---
description: Extrait les données d’un objet externe.
title: Fonction JsGetExternalData | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 469d28d47f89b06897e4b72d081baad34eb92a6c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565192"
---
# <span data-ttu-id="219e9-103">Fonction JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="219e9-103">JsGetExternalData Function</span></span>
<span data-ttu-id="219e9-104">Extrait les données d’un objet externe.</span><span class="sxs-lookup"><span data-stu-id="219e9-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="219e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="219e9-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="219e9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="219e9-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="219e9-107">Objet externe.</span><span class="sxs-lookup"><span data-stu-id="219e9-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="219e9-108">Données externes stockées dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="219e9-108">The external data stored in the object.</span></span> <span data-ttu-id="219e9-109">Peut être null si aucune donnée externe n’est stockée dans l’objet.</span><span class="sxs-lookup"><span data-stu-id="219e9-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="219e9-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="219e9-110">Return Value</span></span>  
 <span data-ttu-id="219e9-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="219e9-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="219e9-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="219e9-112">Remarks</span></span>  
 <span data-ttu-id="219e9-113">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="219e9-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="219e9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="219e9-114">Requirements</span></span>  
 <span data-ttu-id="219e9-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="219e9-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="219e9-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="219e9-116">See Also</span></span>  
 [<span data-ttu-id="219e9-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="219e9-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)