---
description: 'Définit une fonction de rappel appelée par le runtime avant le nettoyage de la mémoire. '
title: Fonction JsSetRuntimeBeforeCollectCallback | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 94ad29fcfb778fc630d70664f917c6b5c2637dde
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232962"
---
# <span data-ttu-id="81fe3-103">JsSetRuntimeBeforeCollectCallback Function</span><span class="sxs-lookup"><span data-stu-id="81fe3-103">JsSetRuntimeBeforeCollectCallback Function</span></span>

<span data-ttu-id="81fe3-104">Définit une fonction de rappel appelée par le runtime avant le nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="81fe3-104">Sets a callback function that is called by the runtime before garbage collection.</span></span>  
  
## <span data-ttu-id="81fe3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81fe3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="81fe3-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81fe3-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="81fe3-107">Le runtime pour lequel inscrire le rappel d’allocation.</span><span class="sxs-lookup"><span data-stu-id="81fe3-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="81fe3-108">État fourni par l’utilisateur qui sera transmis au rappel.</span><span class="sxs-lookup"><span data-stu-id="81fe3-108">User provided state that will be passed back to the callback.</span></span>  
  
 `beforeCollectCallback`  
 <span data-ttu-id="81fe3-109">Fonction de rappel définie.</span><span class="sxs-lookup"><span data-stu-id="81fe3-109">The callback function being set.</span></span>  
  
## <span data-ttu-id="81fe3-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="81fe3-110">Return Value</span></span>  
 <span data-ttu-id="81fe3-111">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="81fe3-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="81fe3-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="81fe3-112">Remarks</span></span>  
 <span data-ttu-id="81fe3-113">Le rappel est appelé sur le thread d’exécution du runtime actuel, donc l’exécution est bloquée jusqu’à ce que le rappel se termine.</span><span class="sxs-lookup"><span data-stu-id="81fe3-113">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="81fe3-114">Le rappel peut être utilisé par des hôtes pour préparer le nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="81fe3-114">The callback can be used by hosts to prepare for garbage collection.</span></span> <span data-ttu-id="81fe3-115">Par exemple, en libérant les références inutiles sur les objets Chakra.</span><span class="sxs-lookup"><span data-stu-id="81fe3-115">For example, by releasing unnecessary references on Chakra objects.</span></span>  
  
## <span data-ttu-id="81fe3-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="81fe3-116">Requirements</span></span>  
 <span data-ttu-id="81fe3-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="81fe3-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="81fe3-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81fe3-118">See Also</span></span>  
 [<span data-ttu-id="81fe3-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="81fe3-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
