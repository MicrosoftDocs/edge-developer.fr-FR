---
description: Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.
title: JsProjectionCallbackContext typedef | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 7742b0186a49e99f2738b81357b9e55cfe00042b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233299"
---
# <span data-ttu-id="bfd2c-103">Typedef JsProjectionCallbackContext</span><span class="sxs-lookup"><span data-stu-id="bfd2c-103">JsProjectionCallbackContext Typedef</span></span>

<span data-ttu-id="bfd2c-104">Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.</span><span class="sxs-lookup"><span data-stu-id="bfd2c-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="bfd2c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bfd2c-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="bfd2c-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="bfd2c-106">Remarks</span></span>  
 <span data-ttu-id="bfd2c-107">Nécessite l’appel `JsSetProjectionEnqueueCallback` pour recevoir des rappels.</span><span class="sxs-lookup"><span data-stu-id="bfd2c-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="bfd2c-108">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="bfd2c-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="bfd2c-109">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="bfd2c-109">Requirements</span></span>  
 <span data-ttu-id="bfd2c-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bfd2c-110">jsrt.h</span></span>  
  
## <span data-ttu-id="bfd2c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bfd2c-111">See Also</span></span>  
 [<span data-ttu-id="bfd2c-112">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bfd2c-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
