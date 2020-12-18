---
description: Exécute un script.
title: Fonction JsRunScript | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: d61771991e1d22a9d71a928d785390b814a992a8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233472"
---
# <span data-ttu-id="7be55-103">JsRunScript Function</span><span class="sxs-lookup"><span data-stu-id="7be55-103">JsRunScript Function</span></span>

<span data-ttu-id="7be55-104">Exécute un script.</span><span class="sxs-lookup"><span data-stu-id="7be55-104">Executes a script.</span></span>  
  
## <span data-ttu-id="7be55-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7be55-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="7be55-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7be55-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="7be55-107">Script à exécuter.</span><span class="sxs-lookup"><span data-stu-id="7be55-107">The script to run.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="7be55-108">Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.</span><span class="sxs-lookup"><span data-stu-id="7be55-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="7be55-109">Emplacement à partir duquel provient le script.</span><span class="sxs-lookup"><span data-stu-id="7be55-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="7be55-110">Le résultat du script, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7be55-110">The result of the script, if any.</span></span> <span data-ttu-id="7be55-111">Ce paramètre peut être null.</span><span class="sxs-lookup"><span data-stu-id="7be55-111">This parameter can be null.</span></span>  
  
## <span data-ttu-id="7be55-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7be55-112">Return Value</span></span>  
 <span data-ttu-id="7be55-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="7be55-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7be55-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7be55-114">Remarks</span></span>  
 <span data-ttu-id="7be55-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="7be55-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="7be55-116">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="7be55-116">Requirements</span></span>  
 <span data-ttu-id="7be55-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7be55-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7be55-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7be55-118">See Also</span></span>  
 [<span data-ttu-id="7be55-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7be55-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
