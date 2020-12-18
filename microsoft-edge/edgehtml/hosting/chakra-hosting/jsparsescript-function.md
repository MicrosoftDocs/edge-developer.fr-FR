---
description: Analyse un script et retourne une fonction qui représente le script.
title: Fonction JsParseScript | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 656d9a992868a3cb892808775f160092b8eaf069
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233309"
---
# <span data-ttu-id="538ba-103">JsParseScript Function</span><span class="sxs-lookup"><span data-stu-id="538ba-103">JsParseScript Function</span></span>

<span data-ttu-id="538ba-104">Analyse un script et retourne une fonction qui représente le script.</span><span class="sxs-lookup"><span data-stu-id="538ba-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="538ba-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="538ba-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="538ba-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="538ba-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="538ba-107">Script à analyser.</span><span class="sxs-lookup"><span data-stu-id="538ba-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="538ba-108">Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.</span><span class="sxs-lookup"><span data-stu-id="538ba-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="538ba-109">Emplacement à partir duquel provient le script.</span><span class="sxs-lookup"><span data-stu-id="538ba-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="538ba-110">Fonction qui représente le code de script.</span><span class="sxs-lookup"><span data-stu-id="538ba-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="538ba-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="538ba-111">Return Value</span></span>  
 <span data-ttu-id="538ba-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="538ba-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="538ba-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="538ba-113">Remarks</span></span>  
 <span data-ttu-id="538ba-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="538ba-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="538ba-115">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="538ba-115">Requirements</span></span>  
 <span data-ttu-id="538ba-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="538ba-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="538ba-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="538ba-117">See Also</span></span>  
 [<span data-ttu-id="538ba-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="538ba-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
