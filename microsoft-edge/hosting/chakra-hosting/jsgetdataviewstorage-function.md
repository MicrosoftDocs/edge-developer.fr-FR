---
description: Obtient le stockage de mémoire sous-jacent utilisé par un DataView.
title: Fonction JsGetDataViewStorage | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 54f8a91b6dea1e0997ad31d6585ea741fde8ba99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565194"
---
# <span data-ttu-id="f2e0a-103">Fonction JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="f2e0a-103">JsGetDataViewStorage Function</span></span>
<span data-ttu-id="f2e0a-104">Obtient le stockage de mémoire sous-jacent utilisé par a `DataView` .</span><span class="sxs-lookup"><span data-stu-id="f2e0a-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="f2e0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2e0a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="f2e0a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2e0a-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="f2e0a-107">Instance DataView.</span><span class="sxs-lookup"><span data-stu-id="f2e0a-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="f2e0a-108">Tampon du DataView.</span><span class="sxs-lookup"><span data-stu-id="f2e0a-108">The DataView's buffer.</span></span> <span data-ttu-id="f2e0a-109">La durée de vie de la mémoire tampon renvoyée est identique à celle du `DataView` .</span><span class="sxs-lookup"><span data-stu-id="f2e0a-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="f2e0a-110">Le pointeur de tampon n’est pas compté en tant que référence à l' `DataView` objectif du nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f2e0a-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="f2e0a-111">Nombre d’octets de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="f2e0a-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="f2e0a-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f2e0a-112">Return Value</span></span>  
 <span data-ttu-id="f2e0a-113">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f2e0a-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f2e0a-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2e0a-114">Remarks</span></span>  
 <span data-ttu-id="f2e0a-115">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="f2e0a-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="f2e0a-116">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f2e0a-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="f2e0a-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2e0a-117">Requirements</span></span>  
 <span data-ttu-id="f2e0a-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f2e0a-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f2e0a-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2e0a-119">See Also</span></span>  
 [<span data-ttu-id="f2e0a-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f2e0a-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)