---
description: Analyse un script et retourne une fonction qui représente le script.
title: Fonction JsParseScript | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd224ef0e800f05e6e07580f545bc4af218b3498
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566284"
---
# <span data-ttu-id="4107b-103">Fonction JsParseScript</span><span class="sxs-lookup"><span data-stu-id="4107b-103">JsParseScript Function</span></span>
<span data-ttu-id="4107b-104">Analyse un script et retourne une fonction qui représente le script.</span><span class="sxs-lookup"><span data-stu-id="4107b-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="4107b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4107b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="4107b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4107b-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="4107b-107">Script à analyser.</span><span class="sxs-lookup"><span data-stu-id="4107b-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="4107b-108">Un cookie identifiant le script qui peut être utilisé par les contextes de script déboguables.</span><span class="sxs-lookup"><span data-stu-id="4107b-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="4107b-109">Emplacement à partir duquel provient le script.</span><span class="sxs-lookup"><span data-stu-id="4107b-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="4107b-110">Fonction qui représente le code de script.</span><span class="sxs-lookup"><span data-stu-id="4107b-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="4107b-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4107b-111">Return Value</span></span>  
 <span data-ttu-id="4107b-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4107b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4107b-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4107b-113">Remarks</span></span>  
 <span data-ttu-id="4107b-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="4107b-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4107b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4107b-115">Requirements</span></span>  
 <span data-ttu-id="4107b-116">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4107b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4107b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4107b-117">See Also</span></span>  
 [<span data-ttu-id="4107b-118">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4107b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)