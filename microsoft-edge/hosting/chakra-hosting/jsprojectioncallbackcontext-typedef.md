---
description: Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.
title: JsProjectionCallbackContext typedef | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565145"
---
# <span data-ttu-id="c851c-103">JsProjectionCallbackContext typedef</span><span class="sxs-lookup"><span data-stu-id="c851c-103">JsProjectionCallbackContext Typedef</span></span>
<span data-ttu-id="c851c-104">Le contexte transmis au rappel d’application, JsProjectionEnqueueCallback, de JsRT, puis de nouveau transmis à JsRT dans le rappel fourni, `JsProjectionCallback` par l’application sur le thread approprié.</span><span class="sxs-lookup"><span data-stu-id="c851c-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="c851c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c851c-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="c851c-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="c851c-106">Remarks</span></span>  
 <span data-ttu-id="c851c-107">Nécessite l’appel `JsSetProjectionEnqueueCallback` pour recevoir des rappels.</span><span class="sxs-lookup"><span data-stu-id="c851c-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="c851c-108">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="c851c-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="c851c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c851c-109">Requirements</span></span>  
 <span data-ttu-id="c851c-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c851c-110">jsrt.h</span></span>  
  
## <span data-ttu-id="c851c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c851c-111">See Also</span></span>  
 [<span data-ttu-id="c851c-112">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c851c-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)