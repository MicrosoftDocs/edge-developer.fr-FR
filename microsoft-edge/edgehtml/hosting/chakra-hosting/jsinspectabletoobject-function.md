---
description: Crée une valeur JavaScript qui est une projection du `IInspectable` pointeur transmis.
title: Fonction JsInspectableToObject | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: a5d3d91b38c9db5de2eb8fb02526f6072f0f5147
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233358"
---
# <span data-ttu-id="d63bb-103">JsInspectableToObject Function</span><span class="sxs-lookup"><span data-stu-id="d63bb-103">JsInspectableToObject Function</span></span>

<span data-ttu-id="d63bb-104">Crée une valeur JavaScript qui est une projection du `IInspectable` pointeur transmis.</span><span class="sxs-lookup"><span data-stu-id="d63bb-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="d63bb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d63bb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="d63bb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d63bb-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="d63bb-107">A `IInspectable` à projeter.</span><span class="sxs-lookup"><span data-stu-id="d63bb-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="d63bb-108">Valeur JavaScript qui est une projection de la `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="d63bb-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="d63bb-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="d63bb-109">Return Value</span></span>  
 <span data-ttu-id="d63bb-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d63bb-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d63bb-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="d63bb-111">Remarks</span></span>  
 <span data-ttu-id="d63bb-112">La valeur projetée peut être utilisée par le script pour appeler un objet WinRT.</span><span class="sxs-lookup"><span data-stu-id="d63bb-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="d63bb-113">Les hôtes sont chargés d’appliquer les règles de thread COM.</span><span class="sxs-lookup"><span data-stu-id="d63bb-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="d63bb-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="d63bb-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d63bb-115">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d63bb-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="d63bb-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="d63bb-116">Requirements</span></span>  
 <span data-ttu-id="d63bb-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d63bb-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d63bb-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d63bb-118">See Also</span></span>  
 [<span data-ttu-id="d63bb-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d63bb-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
