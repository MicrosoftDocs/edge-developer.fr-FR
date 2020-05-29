---
description: Projet d’espace de noms WinRT.
title: Fonction JsProjectWinRTNamespace | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c4d63727b3d25bbb346fee7179ae0d942ae37008
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565139"
---
# <span data-ttu-id="f0fcb-103">Fonction JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="f0fcb-103">JsProjectWinRTNamespace Function</span></span>
<span data-ttu-id="f0fcb-104">Projet d’espace de noms WinRT.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="f0fcb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f0fcb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="f0fcb-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f0fcb-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="f0fcb-107">Espace de noms WinRT devant être projeté.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="f0fcb-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f0fcb-108">Return Value</span></span>  
 <span data-ttu-id="f0fcb-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f0fcb-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="f0fcb-110">Remarks</span></span>  
 <span data-ttu-id="f0fcb-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f0fcb-112">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="f0fcb-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="f0fcb-113">WinRT était le nom de la plateforme avant la plateforme Windows universelle (UWP).</span><span class="sxs-lookup"><span data-stu-id="f0fcb-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="f0fcb-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f0fcb-114">Requirements</span></span>  
 <span data-ttu-id="f0fcb-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f0fcb-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f0fcb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f0fcb-116">See Also</span></span>  
 [<span data-ttu-id="f0fcb-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f0fcb-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)