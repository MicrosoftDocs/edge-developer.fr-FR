---
description: Crée un `DataView` objet JavaScript.
title: Fonction JsCreateDataView | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565239"
---
# <span data-ttu-id="1a896-103">Fonction JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="1a896-103">JsCreateDataView Function</span></span>
<span data-ttu-id="1a896-104">Crée un `DataView` objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1a896-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="1a896-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a896-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="1a896-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1a896-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="1a896-107">Objet existant `ArrayBuffer` à utiliser comme espace de stockage de l’objet de résultat `DataView` .</span><span class="sxs-lookup"><span data-stu-id="1a896-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="1a896-108">Le décalage en octets entre le début du `arrayBuffer` résultat `DataView` et la référence.</span><span class="sxs-lookup"><span data-stu-id="1a896-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="1a896-109">Nombre d’octets dans ArrayBuffer pour le DataView de résultats à référencer.</span><span class="sxs-lookup"><span data-stu-id="1a896-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="1a896-110">Nouvel objet DataView.</span><span class="sxs-lookup"><span data-stu-id="1a896-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="1a896-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="1a896-111">Return Value</span></span>  
 <span data-ttu-id="1a896-112">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1a896-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="1a896-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a896-113">Remarks</span></span>  
 <span data-ttu-id="1a896-114">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="1a896-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="1a896-115">Cette API est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="1a896-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="1a896-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a896-116">Requirements</span></span>  
 <span data-ttu-id="1a896-117">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1a896-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1a896-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a896-118">See Also</span></span>  
 [<span data-ttu-id="1a896-119">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1a896-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)