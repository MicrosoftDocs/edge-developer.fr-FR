---
description: Obtient le stockage de mémoire sous-jacent utilisé par un ArrayBuffer.
title: Fonction JsGetArrayBufferStorage | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e8d265f3e81015ba9f5d0547b6b1c7246c23ce5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566330"
---
# <span data-ttu-id="dd70c-103">Fonction JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="dd70c-103">JsGetArrayBufferStorage Function</span></span>
<span data-ttu-id="dd70c-104">Obtient le stockage de mémoire sous-jacent utilisé par un `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="dd70c-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="dd70c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd70c-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="dd70c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd70c-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="dd70c-107">L’instance ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="dd70c-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="dd70c-108">Le tampon de l’ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="dd70c-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="dd70c-109">La durée de vie de la mémoire tampon renvoyée est identique à celle du `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="dd70c-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="dd70c-110">Le pointeur de tampon n’est pas compté en tant que référence à l' `ArrayBuffer` objectif du nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd70c-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="dd70c-111">Nombre d’octets de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="dd70c-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="dd70c-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd70c-112">Return Value</span></span>  
 <span data-ttu-id="dd70c-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="dd70c-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="dd70c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd70c-114">Remarks</span></span>  
 <span data-ttu-id="dd70c-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="dd70c-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="dd70c-116">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="dd70c-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="dd70c-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd70c-117">Requirements</span></span>  
 <span data-ttu-id="dd70c-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="dd70c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="dd70c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd70c-119">See Also</span></span>  
 [<span data-ttu-id="dd70c-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="dd70c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)