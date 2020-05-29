---
description: Définit l’exécution du contexte actuel sur un état d’exception.
title: Fonction JsSetException | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566248"
---
# <span data-ttu-id="07bf0-103">Fonction JsSetException</span><span class="sxs-lookup"><span data-stu-id="07bf0-103">JsSetException Function</span></span>
<span data-ttu-id="07bf0-104">Définit l’exécution du contexte actuel sur un état d’exception.</span><span class="sxs-lookup"><span data-stu-id="07bf0-104">Sets the runtime of the current context to an exception state.</span></span>  
  
## <span data-ttu-id="07bf0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="07bf0-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### <span data-ttu-id="07bf0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="07bf0-106">Parameters</span></span>  
 `exception`  
 <span data-ttu-id="07bf0-107">Exception JavaScript à définir pour le runtime du contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="07bf0-107">The JavaScript exception to set for the runtime of the current context.</span></span>  
  
## <span data-ttu-id="07bf0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="07bf0-108">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="07bf0-109">Si le moteur a été défini comme état d’exception, il est contraire d’un code d’échec.</span><span class="sxs-lookup"><span data-stu-id="07bf0-109">if the engine was set into an exception state, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="07bf0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="07bf0-110">Remarks</span></span>  
 <span data-ttu-id="07bf0-111">Si le runtime du contexte actuel est déjà dans un état d’exception, cette API retourne `JsErrorInExceptionState` .</span><span class="sxs-lookup"><span data-stu-id="07bf0-111">If the runtime of the current context is already in an exception state, this API will return `JsErrorInExceptionState`.</span></span>  
  
 <span data-ttu-id="07bf0-112">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="07bf0-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="07bf0-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="07bf0-113">Requirements</span></span>  
 <span data-ttu-id="07bf0-114">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="07bf0-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="07bf0-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="07bf0-115">See Also</span></span>  
 [<span data-ttu-id="07bf0-116">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="07bf0-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)