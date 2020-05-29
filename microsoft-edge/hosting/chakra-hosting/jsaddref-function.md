---
description: Ajoute une référence à un objet nettoyé.
title: Fonction JsAddRef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd02dded6dc2877228f22b4d2800e41a78163467
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565270"
---
# <span data-ttu-id="372b8-103">Fonction JsAddRef</span><span class="sxs-lookup"><span data-stu-id="372b8-103">JsAddRef Function</span></span>
<span data-ttu-id="372b8-104">Ajoute une référence à un objet nettoyé.</span><span class="sxs-lookup"><span data-stu-id="372b8-104">Adds a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="372b8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="372b8-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="372b8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="372b8-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="372b8-107">Objet auquel ajouter une référence.</span><span class="sxs-lookup"><span data-stu-id="372b8-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="372b8-108">Le nouveau nombre de références (peut être transmis à null).</span><span class="sxs-lookup"><span data-stu-id="372b8-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="372b8-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="372b8-109">Return Value</span></span>  
 <span data-ttu-id="372b8-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="372b8-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="372b8-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="372b8-111">Remarks</span></span>  
 <span data-ttu-id="372b8-112">Pour cela, il suffit d’appeler sur des `JsRef` Handles qui n’ont pas pu être stockés quelque part dans la pile.</span><span class="sxs-lookup"><span data-stu-id="372b8-112">This only needs to be called on `JsRef` handles that are not going to be stored somewhere on the stack.</span></span> <span data-ttu-id="372b8-113">L’appel `JsAddRef` vérifie que l’objet auquel le `JsRef` fait référence ne sera pas libéré tant qu' `JsRelease` il n’est pas appelé.</span><span class="sxs-lookup"><span data-stu-id="372b8-113">Calling `JsAddRef` ensures that the object the `JsRef` refers to will not be freed until `JsRelease` is called.</span></span>  
  
## <span data-ttu-id="372b8-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="372b8-114">Requirements</span></span>  
 <span data-ttu-id="372b8-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="372b8-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="372b8-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="372b8-116">See Also</span></span>  
 [<span data-ttu-id="372b8-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="372b8-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)