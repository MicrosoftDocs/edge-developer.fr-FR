---
description: Obtient le stockage de mémoire sous-jacent utilisé par un DataView.
title: Fonction JsGetDataViewStorage | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 55f357e4a94b1edbc417ebb14ab99db11083dff4
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233222"
---
# <span data-ttu-id="57031-103">JsGetDataViewStorage Function</span><span class="sxs-lookup"><span data-stu-id="57031-103">JsGetDataViewStorage Function</span></span>

<span data-ttu-id="57031-104">Obtient le stockage de mémoire sous-jacent utilisé par a `DataView` .</span><span class="sxs-lookup"><span data-stu-id="57031-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="57031-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57031-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="57031-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57031-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="57031-107">Instance DataView.</span><span class="sxs-lookup"><span data-stu-id="57031-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="57031-108">Tampon du DataView.</span><span class="sxs-lookup"><span data-stu-id="57031-108">The DataView's buffer.</span></span> <span data-ttu-id="57031-109">La durée de vie de la mémoire tampon renvoyée est identique à celle du `DataView` .</span><span class="sxs-lookup"><span data-stu-id="57031-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="57031-110">Le pointeur de tampon n’est pas compté en tant que référence à l' `DataView` objectif du nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="57031-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="57031-111">Nombre d’octets de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="57031-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="57031-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57031-112">Return Value</span></span>  
 <span data-ttu-id="57031-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="57031-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="57031-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="57031-114">Remarks</span></span>  
 <span data-ttu-id="57031-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="57031-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="57031-116">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="57031-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="57031-117">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="57031-117">Requirements</span></span>  
 <span data-ttu-id="57031-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="57031-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="57031-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="57031-119">See Also</span></span>  
 [<span data-ttu-id="57031-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="57031-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
