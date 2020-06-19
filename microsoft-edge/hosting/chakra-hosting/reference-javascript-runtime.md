---
description: Les API Runtime JavaScript (JsRT) vous permettent d’ajouter des fonctionnalités d’écriture de script aux applications de bureau et aux applications côté serveur qui s’exécutent sur Windows.
title: Référence (Runtime JavaScript)
ms.date: 06/08/2020
ms.prod: microsoft-edge
ms.topic: article
ms.assetid: 0bfe50da-fd79-4e00-9458-bc667769b415
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
ms.openlocfilehash: 7166e6cd5d64060c2939d8404e1415dc34fce17b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752212"
---
# <span data-ttu-id="f2ea1-103">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f2ea1-103">Reference (JavaScript runtime)</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="f2ea1-104">Les API Runtime JavaScript (JsRT) vous permettent d’ajouter des fonctionnalités d’écriture de script aux applications de bureau et aux applications côté serveur qui s’exécutent sur Windows.</span><span class="sxs-lookup"><span data-stu-id="f2ea1-104">JavaScript Runtime (JsRT) APIs enable you to add scripting capabilities to desktop and server-side applications running on Windows.</span></span>  

<span data-ttu-id="f2ea1-105">Si vous envisagez d’incorporer [ChakraCore](https://github.com/Microsoft/ChakraCore) dans votre application, reportez-vous à la rubrique références de [CHAKRACORE wiki](https://aka.ms/corejsrtref) pour JSRT à la place.</span><span class="sxs-lookup"><span data-stu-id="f2ea1-105">If you intend to embed [ChakraCore](https://github.com/Microsoft/ChakraCore) in your application, please refer to [ChakraCore Wiki](https://aka.ms/corejsrtref) for JSRT references instead.</span></span>  

## <span data-ttu-id="f2ea1-106">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="f2ea1-106">In this section</span></span>  

<span data-ttu-id="f2ea1-107">Les typedefs, constantes et énumérations qui prennent en charge l’hébergement JsRT sont décrits ici:</span><span class="sxs-lookup"><span data-stu-id="f2ea1-107">Typedefs, constants, and enumerations that support JsRT hosting are described here:</span></span>  
  
*   [<span data-ttu-id="f2ea1-108">Typedefs de runtime JavaScript, constantes et énumérations</span><span class="sxs-lookup"><span data-stu-id="f2ea1-108">JavaScript Runtime Typedefs, Constants, and Enumerations</span></span>](./javascript-runtime-typedefs-constants-and-enumerations.md)  

<span data-ttu-id="f2ea1-109">Les fonctions suivantes permettent l’hébergement d’JsRT:</span><span class="sxs-lookup"><span data-stu-id="f2ea1-109">The following functions enable JsRT hosting:</span></span>  

*   [<span data-ttu-id="f2ea1-110">JsAddRef Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-110">JsAddRef Function</span></span>](./jsaddref-function.md)  
*   [<span data-ttu-id="f2ea1-111">JsBooleanToBool Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-111">JsBooleanToBool Function</span></span>](./jsbooleantobool-function.md)  
*   [<span data-ttu-id="f2ea1-112">JsBoolToBoolean Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-112">JsBoolToBoolean Function</span></span>](./jsbooltoboolean-function.md)  
*   [<span data-ttu-id="f2ea1-113">JsCallFunction Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-113">JsCallFunction Function</span></span>](./jscallfunction-function.md)  
*   [<span data-ttu-id="f2ea1-114">JsCollectGarbage Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-114">JsCollectGarbage Function</span></span>](./jscollectgarbage-function.md)  
*   [<span data-ttu-id="f2ea1-115">JsConstructObject Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-115">JsConstructObject Function</span></span>](./jsconstructobject-function.md)  
*   [<span data-ttu-id="f2ea1-116">JsConvertValueToBoolean Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-116">JsConvertValueToBoolean Function</span></span>](./jsconvertvaluetoboolean-function.md)  
*   [<span data-ttu-id="f2ea1-117">JsConvertValueToNumber Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-117">JsConvertValueToNumber Function</span></span>](./jsconvertvaluetonumber-function.md)  
*   [<span data-ttu-id="f2ea1-118">JsConvertValueToObject Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-118">JsConvertValueToObject Function</span></span>](./jsconvertvaluetoobject-function.md)  
*   [<span data-ttu-id="f2ea1-119">JsConvertValueToString Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-119">JsConvertValueToString Function</span></span>](./jsconvertvaluetostring-function.md)  
*   [<span data-ttu-id="f2ea1-120">JsCreateArray Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-120">JsCreateArray Function</span></span>](./jscreatearray-function.md)  
*   [<span data-ttu-id="f2ea1-121">JsCreateArrayBuffer Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-121">JsCreateArrayBuffer Function</span></span>](./jscreatearraybuffer-function.md)  
*   [<span data-ttu-id="f2ea1-122">JsCreateContext Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-122">JsCreateContext Function</span></span>](./jscreatecontext-function.md)  
*   [<span data-ttu-id="f2ea1-123">JsCreateDataView Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-123">JsCreateDataView Function</span></span>](./jscreatedataview-function.md)  
*   [<span data-ttu-id="f2ea1-124">JsCreateError Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-124">JsCreateError Function</span></span>](./jscreateerror-function.md)  
*   [<span data-ttu-id="f2ea1-125">JsCreateExternalArrayBuffer Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-125">JsCreateExternalArrayBuffer Function</span></span>](./jscreateexternalarraybuffer-function.md)  
*   [<span data-ttu-id="f2ea1-126">JsCreateExternalObject Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-126">JsCreateExternalObject Function</span></span>](./jscreateexternalobject-function.md)  
*   [<span data-ttu-id="f2ea1-127">JsCreateFunction Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-127">JsCreateFunction Function</span></span>](./jscreatefunction-function.md)  
*   [<span data-ttu-id="f2ea1-128">JsCreateNamedFunction Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-128">JsCreateNamedFunction Function</span></span>](./jscreatenamedfunction-function.md)  
*   [<span data-ttu-id="f2ea1-129">JsCreateObject Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-129">JsCreateObject Function</span></span>](./jscreateobject-function.md)  
*   [<span data-ttu-id="f2ea1-130">JsCreateRangeError Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-130">JsCreateRangeError Function</span></span>](./jscreaterangeerror-function.md)  
*   [<span data-ttu-id="f2ea1-131">JsCreateReferenceError Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-131">JsCreateReferenceError Function</span></span>](./jscreatereferenceerror-function.md)  
*   [<span data-ttu-id="f2ea1-132">JsCreateRuntime Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-132">JsCreateRuntime Function</span></span>](./jscreateruntime-function.md)  
*   [<span data-ttu-id="f2ea1-133">JsCreateSymbol Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-133">JsCreateSymbol Function</span></span>](./jscreatesymbol-function.md)  
*   [<span data-ttu-id="f2ea1-134">JsCreateSyntaxError Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-134">JsCreateSyntaxError Function</span></span>](./jscreatesyntaxerror-function.md)  
*   [<span data-ttu-id="f2ea1-135">JsCreateTypeError Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-135">JsCreateTypeError Function</span></span>](./jscreatetypeerror-function.md)  
*   [<span data-ttu-id="f2ea1-136">JsCreateTypedArray Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-136">JsCreateTypedArray Function</span></span>](./jscreatetypedarray-function.md)  
*   [<span data-ttu-id="f2ea1-137">JsCreateURIError Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-137">JsCreateURIError Function</span></span>](./jscreateurierror-function.md)  
*   [<span data-ttu-id="f2ea1-138">JsDefineProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-138">JsDefineProperty Function</span></span>](./jsdefineproperty-function.md)  
*   [<span data-ttu-id="f2ea1-139">JsDeleteIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-139">JsDeleteIndexedProperty Function</span></span>](./jsdeleteindexedproperty-function.md)  
*   [<span data-ttu-id="f2ea1-140">JsDeleteProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-140">JsDeleteProperty Function</span></span>](./jsdeleteproperty-function.md)  
*   [<span data-ttu-id="f2ea1-141">JsDisableRuntimeExecution Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-141">JsDisableRuntimeExecution Function</span></span>](./jsdisableruntimeexecution-function.md)  
*   [<span data-ttu-id="f2ea1-142">JsDisposeRuntime Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-142">JsDisposeRuntime Function</span></span>](./jsdisposeruntime-function.md)  
*   [<span data-ttu-id="f2ea1-143">JsDoubleToNumber Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-143">JsDoubleToNumber Function</span></span>](./jsdoubletonumber-function.md)  
*   [<span data-ttu-id="f2ea1-144">JsEnableRuntimeExecution Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-144">JsEnableRuntimeExecution Function</span></span>](./jsenableruntimeexecution-function.md)  
*   [<span data-ttu-id="f2ea1-145">JsEnumerateHeap Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-145">JsEnumerateHeap Function</span></span>](./jsenumerateheap-function.md)  
*   [<span data-ttu-id="f2ea1-146">JsEquals Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-146">JsEquals Function</span></span>](./jsequals-function.md)  
*   [<span data-ttu-id="f2ea1-147">JsGetAndClearException Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-147">JsGetAndClearException Function</span></span>](./jsgetandclearexception-function.md)  
*   [<span data-ttu-id="f2ea1-148">JsGetArrayBufferStorage Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-148">JsGetArrayBufferStorage Function</span></span>](./jsgetarraybufferstorage-function.md)  
*   [<span data-ttu-id="f2ea1-149">JsGetContextData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-149">JsGetContextData Function</span></span>](./jsgetcontextdata-function.md)  
*   [<span data-ttu-id="f2ea1-150">JsGetContextOfObject Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-150">JsGetContextOfObject Function</span></span>](./jsgetcontextofobject-function.md)  
*   [<span data-ttu-id="f2ea1-151">JsGetCurrentContext Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-151">JsGetCurrentContext Function</span></span>](./jsgetcurrentcontext-function.md)  
*   [<span data-ttu-id="f2ea1-152">JsGetDataViewStorage Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-152">JsGetDataViewStorage Function</span></span>](./jsgetdataviewstorage-function.md)  
*   [<span data-ttu-id="f2ea1-153">JsGetExtensionAllowed Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-153">JsGetExtensionAllowed Function</span></span>](./jsgetextensionallowed-function.md)  
*   [<span data-ttu-id="f2ea1-154">JsGetExternalData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-154">JsGetExternalData Function</span></span>](./jsgetexternaldata-function.md)  
*   [<span data-ttu-id="f2ea1-155">JsGetFalseValue Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-155">JsGetFalseValue Function</span></span>](./jsgetfalsevalue-function.md)  
*   [<span data-ttu-id="f2ea1-156">JsGetGlobalObject Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-156">JsGetGlobalObject Function</span></span>](./jsgetglobalobject-function.md)  
*   [<span data-ttu-id="f2ea1-157">JsGetIndexedPropertiesExternalData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-157">JsGetIndexedPropertiesExternalData Function</span></span>](./jsgetindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="f2ea1-158">JsGetIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-158">JsGetIndexedProperty Function</span></span>](./jsgetindexedproperty-function.md)  
*   [<span data-ttu-id="f2ea1-159">JsGetNullValue Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-159">JsGetNullValue Function</span></span>](./jsgetnullvalue-function.md)  
*   [<span data-ttu-id="f2ea1-160">JsGetOwnPropertyDescriptor Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-160">JsGetOwnPropertyDescriptor Function</span></span>](./jsgetownpropertydescriptor-function.md)  
*   [<span data-ttu-id="f2ea1-161">JsGetOwnPropertyNames Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-161">JsGetOwnPropertyNames Function</span></span>](./jsgetownpropertynames-function.md)  
*   [<span data-ttu-id="f2ea1-162">JsGetOwnPropertySymbols Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-162">JsGetOwnPropertySymbols Function</span></span>](./jsgetownpropertysymbols-function.md)  
*   [<span data-ttu-id="f2ea1-163">JsGetProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-163">JsGetProperty Function</span></span>](./jsgetproperty-function.md)  
*   [<span data-ttu-id="f2ea1-164">JsGetPropertyIdFromName Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-164">JsGetPropertyIdFromName Function</span></span>](./jsgetpropertyidfromname-function.md)  
*   [<span data-ttu-id="f2ea1-165">JsGetPropertyIdFromSymbol Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-165">JsGetPropertyIdFromSymbol Function</span></span>](./jsgetpropertyidfromsymbol-function.md)  
*   [<span data-ttu-id="f2ea1-166">JsGetPropertyIdType Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-166">JsGetPropertyIdType Function</span></span>](./jsgetpropertyidtype-function.md)  
*   [<span data-ttu-id="f2ea1-167">JsGetPropertyNameFromId Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-167">JsGetPropertyNameFromId Function</span></span>](./jsgetpropertynamefromid-function.md)  
*   [<span data-ttu-id="f2ea1-168">JsGetPrototype Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-168">JsGetPrototype Function</span></span>](./jsgetprototype-function.md)  
*   [<span data-ttu-id="f2ea1-169">JsGetRuntime Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-169">JsGetRuntime Function</span></span>](./jsgetruntime-function.md)  
*   [<span data-ttu-id="f2ea1-170">JsGetRuntimeMemoryLimit Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-170">JsGetRuntimeMemoryLimit Function</span></span>](./jsgetruntimememorylimit-function.md)  
*   [<span data-ttu-id="f2ea1-171">JsGetRuntimeMemoryUsage Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-171">JsGetRuntimeMemoryUsage Function</span></span>](./jsgetruntimememoryusage-function.md)  
*   [<span data-ttu-id="f2ea1-172">JsGetStringLength Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-172">JsGetStringLength Function</span></span>](./jsgetstringlength-function.md)  
*   [<span data-ttu-id="f2ea1-173">JsGetSymbolFromPropertyId Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-173">JsGetSymbolFromPropertyId Function</span></span>](./jsgetsymbolfrompropertyid-function.md)  
*   [<span data-ttu-id="f2ea1-174">JsGetTrueValue Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-174">JsGetTrueValue Function</span></span>](./jsgettruevalue-function.md)  
*   [<span data-ttu-id="f2ea1-175">JsGetTypedArrayInfo Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-175">JsGetTypedArrayInfo Function</span></span>](./jsgettypedarrayinfo-function.md)  
*   [<span data-ttu-id="f2ea1-176">JsGetTypedArrayStorage Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-176">JsGetTypedArrayStorage Function</span></span>](./jsgettypedarraystorage-function.md)  
*   [<span data-ttu-id="f2ea1-177">JsGetUndefinedValue Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-177">JsGetUndefinedValue Function</span></span>](./jsgetundefinedvalue-function.md)  
*   [<span data-ttu-id="f2ea1-178">JsGetValueType Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-178">JsGetValueType Function</span></span>](./jsgetvaluetype-function.md)  
*   [<span data-ttu-id="f2ea1-179">JsHasException Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-179">JsHasException Function</span></span>](./jshasexception-function.md)  
*   [<span data-ttu-id="f2ea1-180">JsHasExternalData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-180">JsHasExternalData Function</span></span>](./jshasexternaldata-function.md)  
*   [<span data-ttu-id="f2ea1-181">JsHasIndexedPropertiesExternalData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-181">JsHasIndexedPropertiesExternalData Function</span></span>](./jshasindexedpropertiesexternaldata-function.md)  
*   [<span data-ttu-id="f2ea1-182">JsHasIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-182">JsHasIndexedProperty Function</span></span>](./jshasindexedproperty-function.md)  
*   [<span data-ttu-id="f2ea1-183">JsHasProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-183">JsHasProperty Function</span></span>](./jshasproperty-function.md)  
*   [<span data-ttu-id="f2ea1-184">JsIdle Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-184">JsIdle Function</span></span>](./jsidle-function.md)  
*   [<span data-ttu-id="f2ea1-185">JsInspectableToObject Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-185">JsInspectableToObject Function</span></span>](./jsinspectabletoobject-function.md)  
*   [<span data-ttu-id="f2ea1-186">JsInstanceOf Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-186">JsInstanceOf Function</span></span>](./jsinstanceof-function.md)  
*   [<span data-ttu-id="f2ea1-187">JsIntToNumber Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-187">JsIntToNumber Function</span></span>](./jsinttonumber-function.md)  
*   [<span data-ttu-id="f2ea1-188">JsIsEnumeratingHeap Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-188">JsIsEnumeratingHeap Function</span></span>](./jsisenumeratingheap-function.md)  
*   [<span data-ttu-id="f2ea1-189">JsIsRuntimeExecutionDisabled Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-189">JsIsRuntimeExecutionDisabled Function</span></span>](./jsisruntimeexecutiondisabled-function.md)  
*   [<span data-ttu-id="f2ea1-190">JsNumberToDouble Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-190">JsNumberToDouble Function</span></span>](./jsnumbertodouble-function.md)  
*   [<span data-ttu-id="f2ea1-191">JsNumberToInt Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-191">JsNumberToInt Function</span></span>](./jsnumbertoint-function.md)  
*   [<span data-ttu-id="f2ea1-192">JsObjectToInspectable Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-192">JsObjectToInspectable Function</span></span>](./jsobjecttoinspectable-function.md)  
*   [<span data-ttu-id="f2ea1-193">JsParseScript Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-193">JsParseScript Function</span></span>](./jsparsescript-function.md)  
*   [<span data-ttu-id="f2ea1-194">JsParseSerializedScript Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-194">JsParseSerializedScript Function</span></span>](./jsparseserializedscript-function.md)  
*   [<span data-ttu-id="f2ea1-195">JsParseSerializedScriptWithCallback Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-195">JsParseSerializedScriptWithCallback Function</span></span>](./jsparseserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="f2ea1-196">JsPointerToString Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-196">JsPointerToString Function</span></span>](./jspointertostring-function.md)  
*   [<span data-ttu-id="f2ea1-197">JsPreventExtension Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-197">JsPreventExtension Function</span></span>](./jspreventextension-function.md)  
*   [<span data-ttu-id="f2ea1-198">JsProjectWinRTNamespace Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-198">JsProjectWinRTNamespace Function</span></span>](./jsprojectwinrtnamespace-function.md)  
*   [<span data-ttu-id="f2ea1-199">JsRelease Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-199">JsRelease Function</span></span>](./jsrelease-function.md)  
*   [<span data-ttu-id="f2ea1-200">JsRunScript Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-200">JsRunScript Function</span></span>](./jsrunscript-function.md)  
*   [<span data-ttu-id="f2ea1-201">JsRunSerializedScript Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-201">JsRunSerializedScript Function</span></span>](./jsrunserializedscript-function.md)  
*   [<span data-ttu-id="f2ea1-202">JsRunSerializedScriptWithCallback Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-202">JsRunSerializedScriptWithCallback Function</span></span>](./jsrunserializedscriptwithcallback-function.md)  
*   [<span data-ttu-id="f2ea1-203">JsSerializeScript Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-203">JsSerializeScript Function</span></span>](./jsserializescript-function.md)  
*   [<span data-ttu-id="f2ea1-204">JsSetContextData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-204">JsSetContextData Function</span></span>](./jssetcontextdata-function.md)  
*   [<span data-ttu-id="f2ea1-205">JsSetCurrentContext Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-205">JsSetCurrentContext Function</span></span>](./jssetcurrentcontext-function.md)  
*   [<span data-ttu-id="f2ea1-206">JsSetException Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-206">JsSetException Function</span></span>](./jssetexception-function.md)  
*   [<span data-ttu-id="f2ea1-207">JsSetExternalData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-207">JsSetExternalData Function</span></span>](./jssetexternaldata-function.md)  
*   [<span data-ttu-id="f2ea1-208">JsSetIndexedPropertiesToExternalData Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-208">JsSetIndexedPropertiesToExternalData Function</span></span>](./jssetindexedpropertiestoexternaldata-function.md)  
*   [<span data-ttu-id="f2ea1-209">JsSetIndexedProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-209">JsSetIndexedProperty Function</span></span>](./jssetindexedproperty-function.md)  
*   [<span data-ttu-id="f2ea1-210">JsSetObjectBeforeCollectCallback Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-210">JsSetObjectBeforeCollectCallback Function</span></span>](./jssetobjectbeforecollectcallback-function.md)  
*   [<span data-ttu-id="f2ea1-211">JsSetProjectionEnqueueCallback Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-211">JsSetProjectionEnqueueCallback Function</span></span>](./jssetprojectionenqueuecallback-function.md)  
*   [<span data-ttu-id="f2ea1-212">JsSetPromiseContinuationCallback Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-212">JsSetPromiseContinuationCallback Function</span></span>](./jssetpromisecontinuationcallback-function.md)  
*   [<span data-ttu-id="f2ea1-213">JsSetProperty Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-213">JsSetProperty Function</span></span>](./jssetproperty-function.md)  
*   [<span data-ttu-id="f2ea1-214">JsSetPrototype Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-214">JsSetPrototype Function</span></span>](./jssetprototype-function.md)  
*   [<span data-ttu-id="f2ea1-215">JsSetRuntimeBeforeCollectCallback Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-215">JsSetRuntimeBeforeCollectCallback Function</span></span>](./jssetruntimebeforecollectcallback-function.md)  
*   [<span data-ttu-id="f2ea1-216">JsSetRuntimeMemoryAllocationCallback Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-216">JsSetRuntimeMemoryAllocationCallback Function</span></span>](./jssetruntimememoryallocationcallback-function.md)  
*   [<span data-ttu-id="f2ea1-217">JsSetRuntimeMemoryLimit Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-217">JsSetRuntimeMemoryLimit Function</span></span>](./jssetruntimememorylimit-function.md)  
*   [<span data-ttu-id="f2ea1-218">JsStartDebugging Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-218">JsStartDebugging Function</span></span>](./jsstartdebugging-function.md)  
*   [<span data-ttu-id="f2ea1-219">JsStartProfiling Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-219">JsStartProfiling Function</span></span>](./jsstartprofiling-function.md)  
*   [<span data-ttu-id="f2ea1-220">JsStopProfiling Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-220">JsStopProfiling Function</span></span>](./jsstopprofiling-function.md)  
*   [<span data-ttu-id="f2ea1-221">JsStrictEquals Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-221">JsStrictEquals Function</span></span>](./jsstrictequals-function.md)  
*   [<span data-ttu-id="f2ea1-222">JsStringToPointer Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-222">JsStringToPointer Function</span></span>](./jsstringtopointer-function.md)  
*   [<span data-ttu-id="f2ea1-223">JsValueToVariant Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-223">JsValueToVariant Function</span></span>](./jsvaluetovariant-function.md)  
*   [<span data-ttu-id="f2ea1-224">JsVariantToValue Function</span><span class="sxs-lookup"><span data-stu-id="f2ea1-224">JsVariantToValue Function</span></span>](./jsvarianttovalue-function.md)  

## <span data-ttu-id="f2ea1-225">Voir également</span><span class="sxs-lookup"><span data-stu-id="f2ea1-225">See also</span></span>  

*   [<span data-ttu-id="f2ea1-226">Héberger le runtime JavaScript</span><span class="sxs-lookup"><span data-stu-id="f2ea1-226">Hosting the JavaScript Runtime</span></span>](./hosting-the-javascript-runtime.md)  
*   [<span data-ttu-id="f2ea1-227">Hébergement du runtime JavaScript</span><span class="sxs-lookup"><span data-stu-id="f2ea1-227">JavaScript Runtime Hosting</span></span>](../javascript-runtime-hosting.md)  
