---
description: Détermine si un objet possède ses propriétés indexées dans les données externes.
title: Fonction JsHasIndexedPropertiesExternalData | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e6395bacb15904bc3f2e74d22959844e8e0af373
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233474"
---
# <span data-ttu-id="ec2b3-103">JsHasIndexedPropertiesExternalData Function</span><span class="sxs-lookup"><span data-stu-id="ec2b3-103">JsHasIndexedPropertiesExternalData Function</span></span>

<span data-ttu-id="ec2b3-104">Détermine si un objet possède ses propriétés indexées dans les données externes.</span><span class="sxs-lookup"><span data-stu-id="ec2b3-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="ec2b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec2b3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="ec2b3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec2b3-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ec2b3-107">Objet.</span><span class="sxs-lookup"><span data-stu-id="ec2b3-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="ec2b3-108">Si l’objet possède ses propriétés indexées dans les données externes.</span><span class="sxs-lookup"><span data-stu-id="ec2b3-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="ec2b3-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ec2b3-109">Return Value</span></span>  
 <span data-ttu-id="ec2b3-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ec2b3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ec2b3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec2b3-111">Remarks</span></span>  
 <span data-ttu-id="ec2b3-112">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="ec2b3-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="ec2b3-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ec2b3-113">Requirements</span></span>  
 <span data-ttu-id="ec2b3-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ec2b3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ec2b3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec2b3-115">See Also</span></span>  
 [<span data-ttu-id="ec2b3-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ec2b3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
