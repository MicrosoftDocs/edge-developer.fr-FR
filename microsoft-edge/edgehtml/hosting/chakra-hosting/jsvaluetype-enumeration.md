---
description: Le type JavaScript d’un JsValueRef.
title: Énumération JsValueType | Documents Microsoft
ms.prod: microsoft-edge
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 840afcde86d4df80490d463921a74c73e42ddfc2
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11233124"
---
# <span data-ttu-id="f02d5-103">Énumération JsValueType</span><span class="sxs-lookup"><span data-stu-id="f02d5-103">JsValueType Enumeration</span></span>

<span data-ttu-id="f02d5-104">Le type JavaScript d’un JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="f02d5-104">The JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="f02d5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f02d5-105">Syntax</span></span>  
  
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
  
## <span data-ttu-id="f02d5-106">Ses</span><span class="sxs-lookup"><span data-stu-id="f02d5-106">Members</span></span>  
  
### <span data-ttu-id="f02d5-107">Doubl</span><span class="sxs-lookup"><span data-stu-id="f02d5-107">Values</span></span>  
  
|<span data-ttu-id="f02d5-108">Nom</span><span class="sxs-lookup"><span data-stu-id="f02d5-108">Name</span></span>|<span data-ttu-id="f02d5-109">Description</span><span class="sxs-lookup"><span data-stu-id="f02d5-109">Description</span></span>|  
|----------|-----------------|  
|`JsUndefined`|<span data-ttu-id="f02d5-110">La valeur est la `undefined` valeur.</span><span class="sxs-lookup"><span data-stu-id="f02d5-110">The value is the `undefined` value.</span></span>|  
|`JsNull`|<span data-ttu-id="f02d5-111">La valeur est la `null` valeur.</span><span class="sxs-lookup"><span data-stu-id="f02d5-111">The value is the `null` value.</span></span>|  
|`JsNumber`|<span data-ttu-id="f02d5-112">La valeur est une valeur numérique JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-112">The value is a JavaScript number value.</span></span>|  
|`JsString`|<span data-ttu-id="f02d5-113">La valeur est une valeur de chaîne JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-113">The value is a JavaScript string value.</span></span>|  
|`JsBoolean`|<span data-ttu-id="f02d5-114">La valeur est une valeur booléenne JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-114">The value is a JavaScript Boolean value.</span></span>|  
|`JsObject`|<span data-ttu-id="f02d5-115">La valeur est une valeur d’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-115">The value is a JavaScript object value.</span></span>|  
|`JsFunction`|<span data-ttu-id="f02d5-116">La valeur est une valeur d’objet fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-116">The value is a JavaScript function object value.</span></span>|  
|`JsError`|<span data-ttu-id="f02d5-117">La valeur est une valeur d’objet d’erreur JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-117">The value is a JavaScript error object value.</span></span>|  
|`JsArray`|<span data-ttu-id="f02d5-118">La valeur est une valeur d’objet de tableau JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-118">The value is a JavaScript array object value.</span></span>|  
|`JsSymbol`|<span data-ttu-id="f02d5-119">La valeur est une valeur de symbole JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-119">The value is a JavaScript symbol value.</span></span><br /><br /> <span data-ttu-id="f02d5-120">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f02d5-120">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsArrayBuffer`|<span data-ttu-id="f02d5-121">La valeur est une `ArrayBuffer` valeur d’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-121">The value is a JavaScript `ArrayBuffer` object value.</span></span><br /><br /> <span data-ttu-id="f02d5-122">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f02d5-122">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsTypedArray`|<span data-ttu-id="f02d5-123">La valeur est une valeur d’objet de tableau typé JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-123">The value is a JavaScript typed array object value.</span></span><br /><br /> <span data-ttu-id="f02d5-124">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f02d5-124">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsDataView`|<span data-ttu-id="f02d5-125">La valeur est une `DataView` valeur d’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f02d5-125">The value is a JavaScript `DataView` object value.</span></span><br /><br /> <span data-ttu-id="f02d5-126">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f02d5-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
  
## <span data-ttu-id="f02d5-127">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="f02d5-127">Requirements</span></span>  
 <span data-ttu-id="f02d5-128">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f02d5-128">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f02d5-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f02d5-129">See Also</span></span>  
 [<span data-ttu-id="f02d5-130">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f02d5-130">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)
