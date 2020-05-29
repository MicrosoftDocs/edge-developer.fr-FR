---
description: Définit une fonction de rappel qui est appelée par le runtime avant le nettoyage de la mémoire d’un objet.
title: Fonction JsSetObjectBeforeCollectCallback | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566239"
---
# <span data-ttu-id="9fe07-103">Fonction JsSetObjectBeforeCollectCallback</span><span class="sxs-lookup"><span data-stu-id="9fe07-103">JsSetObjectBeforeCollectCallback Function</span></span>
<span data-ttu-id="9fe07-104">Définit une fonction de rappel qui est appelée par le runtime avant le nettoyage de la mémoire d’un objet.</span><span class="sxs-lookup"><span data-stu-id="9fe07-104">Sets a callback function that is called by the runtime before garbage collection of an object.</span></span>  
  
## <span data-ttu-id="9fe07-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9fe07-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### <span data-ttu-id="9fe07-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9fe07-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="9fe07-107">Objet pour lequel inscrire le rappel.</span><span class="sxs-lookup"><span data-stu-id="9fe07-107">The object for which to register the callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="9fe07-108">État fourni par l’utilisateur qui sera renvoyé au rappel.</span><span class="sxs-lookup"><span data-stu-id="9fe07-108">User-provided state that will be passed back to the callback.</span></span>  
  
 `objectBeforeCollectCallback`  
 <span data-ttu-id="9fe07-109">Fonction de rappel définie.</span><span class="sxs-lookup"><span data-stu-id="9fe07-109">The callback function being set.</span></span> <span data-ttu-id="9fe07-110">Utilisez la valeur null pour effacer le rappel enregistré précédemment.</span><span class="sxs-lookup"><span data-stu-id="9fe07-110">Use null to clear previously registered callback.</span></span>  
  
## <span data-ttu-id="9fe07-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9fe07-111">Return Value</span></span>  
 <span data-ttu-id="9fe07-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="9fe07-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9fe07-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="9fe07-113">Remarks</span></span>  
 <span data-ttu-id="9fe07-114">Le rappel est appelé sur le thread d’exécution du runtime actuel, donc l’exécution est bloquée jusqu’à ce que le rappel se termine.</span><span class="sxs-lookup"><span data-stu-id="9fe07-114">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="9fe07-115">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="9fe07-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="9fe07-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fe07-116">Requirements</span></span>  
 <span data-ttu-id="9fe07-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9fe07-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9fe07-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fe07-118">See Also</span></span>  
 [<span data-ttu-id="9fe07-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9fe07-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)