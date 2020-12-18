---
description: Définit le contexte de script actuel sur le thread.
title: Fonction JsSetCurrentContext | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 60ec1760c582f1f6771a5af64f59c4a77b1a43f8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233134"
---
# <span data-ttu-id="9cf54-103">JsSetCurrentContext Function</span><span class="sxs-lookup"><span data-stu-id="9cf54-103">JsSetCurrentContext Function</span></span>

<span data-ttu-id="9cf54-104">Définit le contexte de script actuel sur le thread.</span><span class="sxs-lookup"><span data-stu-id="9cf54-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="9cf54-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9cf54-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="9cf54-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9cf54-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="9cf54-107">Contexte de script pour rendre active.</span><span class="sxs-lookup"><span data-stu-id="9cf54-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="9cf54-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9cf54-108">Return Value</span></span>  
 <span data-ttu-id="9cf54-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9cf54-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="9cf54-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="9cf54-110">Example</span></span>

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

## <span data-ttu-id="9cf54-111">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="9cf54-111">Requirements</span></span>  
 <span data-ttu-id="9cf54-112">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9cf54-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9cf54-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9cf54-113">See Also</span></span>  
 [<span data-ttu-id="9cf54-114">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9cf54-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
