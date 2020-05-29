---
description: Définit le contexte de script actuel sur le thread.
title: Fonction JsSetCurrentContext | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57620ad0e986034791ec07765d7cc115b958d661
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566250"
---
# <span data-ttu-id="1382a-103">Fonction JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="1382a-103">JsSetCurrentContext Function</span></span>
<span data-ttu-id="1382a-104">Définit le contexte de script actuel sur le thread.</span><span class="sxs-lookup"><span data-stu-id="1382a-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="1382a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1382a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="1382a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1382a-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="1382a-107">Contexte de script pour rendre active.</span><span class="sxs-lookup"><span data-stu-id="1382a-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="1382a-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1382a-108">Return Value</span></span>  
 <span data-ttu-id="1382a-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1382a-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="1382a-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="1382a-110">Example</span></span>

```cpp
JsRuntimeHandle runtime;
JsContextRef context;

// Create a runtime.
JsCreateRuntime(JsRuntimeAttributeNone, nullptr, &runtime);

// Create an execution context.
JsCreateContext(runtime, &context);

// Now set the current execution context.
JsSetCurrentContext(context);
```

## <span data-ttu-id="1382a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1382a-111">Requirements</span></span>  
 <span data-ttu-id="1382a-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1382a-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1382a-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1382a-113">See Also</span></span>  
 [<span data-ttu-id="1382a-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1382a-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)