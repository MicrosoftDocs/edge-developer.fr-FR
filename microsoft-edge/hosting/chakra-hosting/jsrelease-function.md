---
description: Libère une référence à un objet nettoyé.
title: Fonction JsRelease | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 134ba16509b6c2f0c232214d7efba4d8c8915d43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566272"
---
# <span data-ttu-id="a3cd3-103">Fonction JsRelease</span><span class="sxs-lookup"><span data-stu-id="a3cd3-103">JsRelease Function</span></span>
<span data-ttu-id="a3cd3-104">Libère une référence à un objet nettoyé.</span><span class="sxs-lookup"><span data-stu-id="a3cd3-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="a3cd3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3cd3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="a3cd3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3cd3-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="a3cd3-107">Objet auquel ajouter une référence.</span><span class="sxs-lookup"><span data-stu-id="a3cd3-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="a3cd3-108">Le nouveau nombre de références (peut être transmis à null).</span><span class="sxs-lookup"><span data-stu-id="a3cd3-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="a3cd3-109">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a3cd3-109">Return Value</span></span>  
 <span data-ttu-id="a3cd3-110">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="a3cd3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a3cd3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3cd3-111">Remarks</span></span>  
 <span data-ttu-id="a3cd3-112">Supprime une référence à une `JsRef` poignée créée par `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="a3cd3-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="a3cd3-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a3cd3-113">Requirements</span></span>  
 <span data-ttu-id="a3cd3-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a3cd3-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a3cd3-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3cd3-115">See Also</span></span>  
 [<span data-ttu-id="a3cd3-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a3cd3-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)