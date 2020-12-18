---
description: Obtient le stockage de mémoire sous-jacent utilisé par un tableau typé.
title: Fonction JsGetTypedArrayStorage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 442727228433368de14bac528ea416fcc2a95fa8
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232838"
---
# <span data-ttu-id="df197-103">JsGetTypedArrayStorage Function</span><span class="sxs-lookup"><span data-stu-id="df197-103">JsGetTypedArrayStorage Function</span></span>

<span data-ttu-id="df197-104">Obtient le stockage de mémoire sous-jacent utilisé par un tableau typé.</span><span class="sxs-lookup"><span data-stu-id="df197-104">Obtains the underlying memory storage used by a typed array.</span></span>  
  
## <span data-ttu-id="df197-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df197-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### <span data-ttu-id="df197-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df197-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="df197-107">Instance de tableau typé.</span><span class="sxs-lookup"><span data-stu-id="df197-107">The typed array instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="df197-108">Tampon du tableau.</span><span class="sxs-lookup"><span data-stu-id="df197-108">The array's buffer.</span></span> <span data-ttu-id="df197-109">La durée de vie de la mémoire tampon renvoyée est identique à la durée de vie de la matrice.</span><span class="sxs-lookup"><span data-stu-id="df197-109">The lifetime of the buffer returned is the same as the lifetime of the array.</span></span> <span data-ttu-id="df197-110">Le pointeur de tampon n’est pas considéré comme une référence au tableau à des fins de nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="df197-110">The buffer pointer does not count as a reference to the array for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="df197-111">Nombre d’octets de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="df197-111">The number of bytes in the buffer.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="df197-112">Type du tableau.</span><span class="sxs-lookup"><span data-stu-id="df197-112">The type of the array.</span></span>  
  
 `elementSize`  
 <span data-ttu-id="df197-113">Taille d’un élément du tableau.</span><span class="sxs-lookup"><span data-stu-id="df197-113">The size of an element of the array.</span></span>  
  
## <span data-ttu-id="df197-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df197-114">Return Value</span></span>  
 <span data-ttu-id="df197-115">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="df197-115">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="df197-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="df197-116">Remarks</span></span>  
 <span data-ttu-id="df197-117">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="df197-117">Requires an active script context.</span></span>  
  
 <span data-ttu-id="df197-118">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="df197-118">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="df197-119">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="df197-119">Requirements</span></span>  
 <span data-ttu-id="df197-120">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="df197-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="df197-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df197-121">See Also</span></span>  
 [<span data-ttu-id="df197-122">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="df197-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
