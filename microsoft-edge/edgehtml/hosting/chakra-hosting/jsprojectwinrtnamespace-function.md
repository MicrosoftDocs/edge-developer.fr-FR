---
description: Projet d’espace de noms WinRT.
title: Fonction JsProjectWinRTNamespace | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f781cf90aaec68b2bd305bf34c453fc663ad0187
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233541"
---
# <span data-ttu-id="e6dfa-103">JsProjectWinRTNamespace Function</span><span class="sxs-lookup"><span data-stu-id="e6dfa-103">JsProjectWinRTNamespace Function</span></span>

<span data-ttu-id="e6dfa-104">Projet d’espace de noms WinRT.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="e6dfa-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6dfa-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="e6dfa-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6dfa-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="e6dfa-107">Espace de noms WinRT devant être projeté.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="e6dfa-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e6dfa-108">Return Value</span></span>  
 <span data-ttu-id="e6dfa-109">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e6dfa-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6dfa-110">Remarks</span></span>  
 <span data-ttu-id="e6dfa-111">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e6dfa-112">Cette API est uniquement prise en charge en mode EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="e6dfa-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="e6dfa-113">WinRT était le nom de la plateforme avant la plateforme Windows universelle (UWP).</span><span class="sxs-lookup"><span data-stu-id="e6dfa-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="e6dfa-114">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="e6dfa-114">Requirements</span></span>  
 <span data-ttu-id="e6dfa-115">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e6dfa-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e6dfa-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6dfa-116">See Also</span></span>  
 [<span data-ttu-id="e6dfa-117">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e6dfa-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
