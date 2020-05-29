---
description: Crée un `ArrayBuffer` objet JavaScript pour accéder à la mémoire externe.
title: Fonction JsCreateExternalArrayBuffer | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565233"
---
# <span data-ttu-id="b4b17-103">Fonction JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="b4b17-103">JsCreateExternalArrayBuffer Function</span></span>
<span data-ttu-id="b4b17-104">Crée un `ArrayBuffer` objet JavaScript pour accéder à la mémoire externe.</span><span class="sxs-lookup"><span data-stu-id="b4b17-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="b4b17-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4b17-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="b4b17-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4b17-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="b4b17-107">Pointeur vers la mémoire externe.</span><span class="sxs-lookup"><span data-stu-id="b4b17-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="b4b17-108">Nombre d’octets de la mémoire externe.</span><span class="sxs-lookup"><span data-stu-id="b4b17-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="b4b17-109">Rappel lors de la finalisation de l’objet.</span><span class="sxs-lookup"><span data-stu-id="b4b17-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="b4b17-110">Est susceptible d’être null.</span><span class="sxs-lookup"><span data-stu-id="b4b17-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="b4b17-111">État fourni par l’utilisateur qui sera renvoyé à finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="b4b17-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="b4b17-112">Nouvel `ArrayBuffer` objet.</span><span class="sxs-lookup"><span data-stu-id="b4b17-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="b4b17-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b4b17-113">Return Value</span></span>  
 <span data-ttu-id="b4b17-114">Le code `JsNoError` en cas de réussite de l’opération, dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b4b17-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b4b17-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4b17-115">Remarks</span></span>  
 <span data-ttu-id="b4b17-116">Nécessite un contexte de script actif.</span><span class="sxs-lookup"><span data-stu-id="b4b17-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b4b17-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4b17-117">Requirements</span></span>  
 <span data-ttu-id="b4b17-118">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b4b17-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b4b17-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4b17-119">See Also</span></span>  
 [<span data-ttu-id="b4b17-120">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b4b17-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)