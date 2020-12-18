---
description: Sérialise un script analysé dans une mémoire tampon qu’il est possible de réutiliser.
title: Fonction JsSerializeScript | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 236cf40c91256e999d5390acd395b1e97fe538ad
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233484"
---
# <span data-ttu-id="dff20-103">JsSerializeScript Function</span><span class="sxs-lookup"><span data-stu-id="dff20-103">JsSerializeScript Function</span></span>

<span data-ttu-id="dff20-104">Sérialise un script analysé dans une mémoire tampon qu’il est possible de réutiliser.</span><span class="sxs-lookup"><span data-stu-id="dff20-104">Serializes a parsed script to a buffer than can be reused.</span></span>  
  
## <span data-ttu-id="dff20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dff20-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### <span data-ttu-id="dff20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dff20-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="dff20-107">Script à sérialiser.</span><span class="sxs-lookup"><span data-stu-id="dff20-107">The script to serialize.</span></span>  
  
 `buffer`  
 <span data-ttu-id="dff20-108">Mémoire tampon dans laquelle placer le script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="dff20-108">The buffer to put the serialized script into.</span></span> <span data-ttu-id="dff20-109">Peut être null.</span><span class="sxs-lookup"><span data-stu-id="dff20-109">Can be null.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="dff20-110">À l’entrée, la taille de la mémoire tampon, en octets; en sortie, la taille de la mémoire tampon, en octets, doit contenir le script sérialisé.</span><span class="sxs-lookup"><span data-stu-id="dff20-110">On entry, the size of the buffer, in bytes; on exit, the size of the buffer, in bytes, required to hold the serialized script.</span></span>  
  
## <span data-ttu-id="dff20-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dff20-111">Return Value</span></span>  
 <span data-ttu-id="dff20-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dff20-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dff20-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="dff20-113">Remarks</span></span>  
 `JsSerializeScript` <span data-ttu-id="dff20-114">analyse un script, puis stocke le formulaire analysé du script dans un format indépendant du Runtime.</span><span class="sxs-lookup"><span data-stu-id="dff20-114">parses a script and then stores the parsed form of the script in a runtime-independent format.</span></span> <span data-ttu-id="dff20-115">Le script sérialisé peut ensuite être désérialisé dans n’importe quel Runtime sans nécessiter de nouvelle analyse du script.</span><span class="sxs-lookup"><span data-stu-id="dff20-115">The serialized script then can be deserialized in any runtime without requiring the script to be re-parsed.</span></span>  
  
 <span data-ttu-id="dff20-116">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="dff20-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="dff20-117">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="dff20-117">Requirements</span></span>  
 <span data-ttu-id="dff20-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dff20-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dff20-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dff20-119">See Also</span></span>  
 [<span data-ttu-id="dff20-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dff20-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
