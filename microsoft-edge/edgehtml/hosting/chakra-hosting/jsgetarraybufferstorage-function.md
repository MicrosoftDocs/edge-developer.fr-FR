---
description: Obtient le stockage de mémoire sous-jacent utilisé par un ArrayBuffer.
title: Fonction JsGetArrayBufferStorage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 64b031a81506e68322759eff49da7467cac6f219
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233101"
---
# <span data-ttu-id="c7d9f-103">JsGetArrayBufferStorage Function</span><span class="sxs-lookup"><span data-stu-id="c7d9f-103">JsGetArrayBufferStorage Function</span></span>

<span data-ttu-id="c7d9f-104">Obtient le stockage de mémoire sous-jacent utilisé par un `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="c7d9f-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="c7d9f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7d9f-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="c7d9f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7d9f-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="c7d9f-107">L’instance ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="c7d9f-108">Le tampon de l’ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="c7d9f-109">La durée de vie de la mémoire tampon renvoyée est identique à celle du `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="c7d9f-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="c7d9f-110">Le pointeur de tampon n’est pas compté en tant que référence à l' `ArrayBuffer` objectif du nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="c7d9f-111">Nombre d’octets de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="c7d9f-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7d9f-112">Return Value</span></span>  
 <span data-ttu-id="c7d9f-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="c7d9f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7d9f-114">Remarks</span></span>  
 <span data-ttu-id="c7d9f-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="c7d9f-116">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c7d9f-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="c7d9f-117">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="c7d9f-117">Requirements</span></span>  
 <span data-ttu-id="c7d9f-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c7d9f-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c7d9f-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7d9f-119">See Also</span></span>  
 [<span data-ttu-id="c7d9f-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c7d9f-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
