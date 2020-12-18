---
description: Supprime la propriété d’un objet.
title: Fonction JsDeleteProperty | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteProperty
helpviewer_keywords:
- JsDeleteProperty function
ms.assetid: 0f6ac6a7-3576-42f5-98d0-1c06542c8149
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55089bd4cff7ef4d58bcce1d7531d4ca1c7381ae
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232807"
---
# <span data-ttu-id="ce44b-103">JsDeleteProperty Function</span><span class="sxs-lookup"><span data-stu-id="ce44b-103">JsDeleteProperty Function</span></span>

<span data-ttu-id="ce44b-104">Supprime la propriété d’un objet.</span><span class="sxs-lookup"><span data-stu-id="ce44b-104">Deletes an object's property.</span></span>  
  
## <span data-ttu-id="ce44b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce44b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteProperty(  
   _In_ JsValueRef object,  
   _In_ JsPropertyIdRef propertyId,  
   _In_ bool useStrictRules,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ce44b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce44b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="ce44b-107">Objet qui contient la propriété.</span><span class="sxs-lookup"><span data-stu-id="ce44b-107">The object that contains the property.</span></span>  
  
 `propertyId`  
 <span data-ttu-id="ce44b-108">ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ce44b-108">The ID of the property.</span></span>  
  
 `useStrictRules`  
 <span data-ttu-id="ce44b-109">Le jeu de propriétés doit suivre des règles en mode strict.</span><span class="sxs-lookup"><span data-stu-id="ce44b-109">The property set should follow strict mode rules.</span></span>  
  
 `result`  
 <span data-ttu-id="ce44b-110">L’état de suppression de la propriété.</span><span class="sxs-lookup"><span data-stu-id="ce44b-110">Whether the property was deleted.</span></span>  
  
## <span data-ttu-id="ce44b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="ce44b-111">Return Value</span></span>  
 <span data-ttu-id="ce44b-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ce44b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ce44b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="ce44b-113">Remarks</span></span>  
 <span data-ttu-id="ce44b-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="ce44b-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ce44b-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="ce44b-115">Requirements</span></span>  
 <span data-ttu-id="ce44b-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ce44b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ce44b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ce44b-117">See Also</span></span>  
 [<span data-ttu-id="ce44b-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ce44b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
