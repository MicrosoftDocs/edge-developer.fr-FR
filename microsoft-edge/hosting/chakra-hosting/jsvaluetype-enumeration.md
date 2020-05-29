---
description: Le type JavaScript d’un JsValueRef.
title: Énumération JsValueType | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c42231525b55b49f0931a2ace33b373e0d4ae441
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565127"
---
# <span data-ttu-id="b945e-103">Énumération JsValueType</span><span class="sxs-lookup"><span data-stu-id="b945e-103">JsValueType Enumeration</span></span>
<span data-ttu-id="b945e-104">Le type JavaScript d’un JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="b945e-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="b945e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b945e-105">Syntax</span></span>  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## <span data-ttu-id="b945e-106">Ses</span><span class="sxs-lookup"><span data-stu-id="b945e-106">Members</span></span>  
  
### <span data-ttu-id="b945e-107">Doubl</span><span class="sxs-lookup"><span data-stu-id="b945e-107">Values</span></span>  
  
|<span data-ttu-id="b945e-108">Nom</span><span class="sxs-lookup"><span data-stu-id="b945e-108">Name</span></span>|<span data-ttu-id="b945e-109">Description</span><span class="sxs-lookup"><span data-stu-id="b945e-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="b945e-110">La valeur est la `undefined` valeur.</span><span class="sxs-lookup"><span data-stu-id="b945e-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="b945e-111">La valeur est la `null` valeur.</span><span class="sxs-lookup"><span data-stu-id="b945e-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="b945e-112">La valeur est une valeur numérique JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="b945e-113">La valeur est une valeur de chaîne JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="b945e-114">La valeur est une valeur booléenne JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="b945e-115">La valeur est une valeur d’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="b945e-116">La valeur est une valeur d’objet fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="b945e-117">La valeur est une valeur d’objet d’erreur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="b945e-118">La valeur est une valeur d’objet de tableau JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="b945e-119">La valeur est une valeur de symbole JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="b945e-120">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b945e-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="b945e-121">La valeur est une `ArrayBuffer` valeur d’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="b945e-122">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b945e-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="b945e-123">La valeur est une valeur d’objet de tableau typé JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="b945e-124">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b945e-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="b945e-125">La valeur est une `DataView` valeur d’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b945e-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="b945e-126">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b945e-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="b945e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b945e-127">Requirements</span></span>  
 <span data-ttu-id="b945e-128">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b945e-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b945e-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b945e-129">See Also</span></span>  
 [<span data-ttu-id="b945e-130">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b945e-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)