---
description: Libère une référence à un objet nettoyé.
title: Fonction JsRelease | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 46552a03dc56a10b1d258d8c33da1c533f38464a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232956"
---
# <span data-ttu-id="c0ed4-103">JsRelease Function</span><span class="sxs-lookup"><span data-stu-id="c0ed4-103">JsRelease Function</span></span>

<span data-ttu-id="c0ed4-104">Libère une référence à un objet nettoyé.</span><span class="sxs-lookup"><span data-stu-id="c0ed4-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="c0ed4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0ed4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="c0ed4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0ed4-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="c0ed4-107">Objet auquel ajouter une référence.</span><span class="sxs-lookup"><span data-stu-id="c0ed4-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="c0ed4-108">Le nouveau nombre de références (peut être transmis à null).</span><span class="sxs-lookup"><span data-stu-id="c0ed4-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="c0ed4-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c0ed4-109">Return Value</span></span>  
 <span data-ttu-id="c0ed4-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c0ed4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c0ed4-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0ed4-111">Remarks</span></span>  
 <span data-ttu-id="c0ed4-112">Supprime une référence à une `JsRef` poignée créée par `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="c0ed4-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="c0ed4-113">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c0ed4-113">Requirements</span></span>  
 <span data-ttu-id="c0ed4-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c0ed4-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c0ed4-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0ed4-115">See Also</span></span>  
 [<span data-ttu-id="c0ed4-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c0ed4-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
