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
# Référence (Runtime JavaScript)  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Les API Runtime JavaScript (JsRT) vous permettent d’ajouter des fonctionnalités d’écriture de script aux applications de bureau et aux applications côté serveur qui s’exécutent sur Windows.  

Si vous envisagez d’incorporer [ChakraCore](https://github.com/Microsoft/ChakraCore) dans votre application, reportez-vous à la rubrique références de [CHAKRACORE wiki](https://aka.ms/corejsrtref) pour JSRT à la place.  

## Dans cette section  

Les typedefs, constantes et énumérations qui prennent en charge l’hébergement JsRT sont décrits ici:  
  
*   [Typedefs de runtime JavaScript, constantes et énumérations](./javascript-runtime-typedefs-constants-and-enumerations.md)  

Les fonctions suivantes permettent l’hébergement d’JsRT:  

*   [JsAddRef Function](./jsaddref-function.md)  
*   [JsBooleanToBool Function](./jsbooleantobool-function.md)  
*   [JsBoolToBoolean Function](./jsbooltoboolean-function.md)  
*   [JsCallFunction Function](./jscallfunction-function.md)  
*   [JsCollectGarbage Function](./jscollectgarbage-function.md)  
*   [JsConstructObject Function](./jsconstructobject-function.md)  
*   [JsConvertValueToBoolean Function](./jsconvertvaluetoboolean-function.md)  
*   [JsConvertValueToNumber Function](./jsconvertvaluetonumber-function.md)  
*   [JsConvertValueToObject Function](./jsconvertvaluetoobject-function.md)  
*   [JsConvertValueToString Function](./jsconvertvaluetostring-function.md)  
*   [JsCreateArray Function](./jscreatearray-function.md)  
*   [JsCreateArrayBuffer Function](./jscreatearraybuffer-function.md)  
*   [JsCreateContext Function](./jscreatecontext-function.md)  
*   [JsCreateDataView Function](./jscreatedataview-function.md)  
*   [JsCreateError Function](./jscreateerror-function.md)  
*   [JsCreateExternalArrayBuffer Function](./jscreateexternalarraybuffer-function.md)  
*   [JsCreateExternalObject Function](./jscreateexternalobject-function.md)  
*   [JsCreateFunction Function](./jscreatefunction-function.md)  
*   [JsCreateNamedFunction Function](./jscreatenamedfunction-function.md)  
*   [JsCreateObject Function](./jscreateobject-function.md)  
*   [JsCreateRangeError Function](./jscreaterangeerror-function.md)  
*   [JsCreateReferenceError Function](./jscreatereferenceerror-function.md)  
*   [JsCreateRuntime Function](./jscreateruntime-function.md)  
*   [JsCreateSymbol Function](./jscreatesymbol-function.md)  
*   [JsCreateSyntaxError Function](./jscreatesyntaxerror-function.md)  
*   [JsCreateTypeError Function](./jscreatetypeerror-function.md)  
*   [JsCreateTypedArray Function](./jscreatetypedarray-function.md)  
*   [JsCreateURIError Function](./jscreateurierror-function.md)  
*   [JsDefineProperty Function](./jsdefineproperty-function.md)  
*   [JsDeleteIndexedProperty Function](./jsdeleteindexedproperty-function.md)  
*   [JsDeleteProperty Function](./jsdeleteproperty-function.md)  
*   [JsDisableRuntimeExecution Function](./jsdisableruntimeexecution-function.md)  
*   [JsDisposeRuntime Function](./jsdisposeruntime-function.md)  
*   [JsDoubleToNumber Function](./jsdoubletonumber-function.md)  
*   [JsEnableRuntimeExecution Function](./jsenableruntimeexecution-function.md)  
*   [JsEnumerateHeap Function](./jsenumerateheap-function.md)  
*   [JsEquals Function](./jsequals-function.md)  
*   [JsGetAndClearException Function](./jsgetandclearexception-function.md)  
*   [JsGetArrayBufferStorage Function](./jsgetarraybufferstorage-function.md)  
*   [JsGetContextData Function](./jsgetcontextdata-function.md)  
*   [JsGetContextOfObject Function](./jsgetcontextofobject-function.md)  
*   [JsGetCurrentContext Function](./jsgetcurrentcontext-function.md)  
*   [JsGetDataViewStorage Function](./jsgetdataviewstorage-function.md)  
*   [JsGetExtensionAllowed Function](./jsgetextensionallowed-function.md)  
*   [JsGetExternalData Function](./jsgetexternaldata-function.md)  
*   [JsGetFalseValue Function](./jsgetfalsevalue-function.md)  
*   [JsGetGlobalObject Function](./jsgetglobalobject-function.md)  
*   [JsGetIndexedPropertiesExternalData Function](./jsgetindexedpropertiesexternaldata-function.md)  
*   [JsGetIndexedProperty Function](./jsgetindexedproperty-function.md)  
*   [JsGetNullValue Function](./jsgetnullvalue-function.md)  
*   [JsGetOwnPropertyDescriptor Function](./jsgetownpropertydescriptor-function.md)  
*   [JsGetOwnPropertyNames Function](./jsgetownpropertynames-function.md)  
*   [JsGetOwnPropertySymbols Function](./jsgetownpropertysymbols-function.md)  
*   [JsGetProperty Function](./jsgetproperty-function.md)  
*   [JsGetPropertyIdFromName Function](./jsgetpropertyidfromname-function.md)  
*   [JsGetPropertyIdFromSymbol Function](./jsgetpropertyidfromsymbol-function.md)  
*   [JsGetPropertyIdType Function](./jsgetpropertyidtype-function.md)  
*   [JsGetPropertyNameFromId Function](./jsgetpropertynamefromid-function.md)  
*   [JsGetPrototype Function](./jsgetprototype-function.md)  
*   [JsGetRuntime Function](./jsgetruntime-function.md)  
*   [JsGetRuntimeMemoryLimit Function](./jsgetruntimememorylimit-function.md)  
*   [JsGetRuntimeMemoryUsage Function](./jsgetruntimememoryusage-function.md)  
*   [JsGetStringLength Function](./jsgetstringlength-function.md)  
*   [JsGetSymbolFromPropertyId Function](./jsgetsymbolfrompropertyid-function.md)  
*   [JsGetTrueValue Function](./jsgettruevalue-function.md)  
*   [JsGetTypedArrayInfo Function](./jsgettypedarrayinfo-function.md)  
*   [JsGetTypedArrayStorage Function](./jsgettypedarraystorage-function.md)  
*   [JsGetUndefinedValue Function](./jsgetundefinedvalue-function.md)  
*   [JsGetValueType Function](./jsgetvaluetype-function.md)  
*   [JsHasException Function](./jshasexception-function.md)  
*   [JsHasExternalData Function](./jshasexternaldata-function.md)  
*   [JsHasIndexedPropertiesExternalData Function](./jshasindexedpropertiesexternaldata-function.md)  
*   [JsHasIndexedProperty Function](./jshasindexedproperty-function.md)  
*   [JsHasProperty Function](./jshasproperty-function.md)  
*   [JsIdle Function](./jsidle-function.md)  
*   [JsInspectableToObject Function](./jsinspectabletoobject-function.md)  
*   [JsInstanceOf Function](./jsinstanceof-function.md)  
*   [JsIntToNumber Function](./jsinttonumber-function.md)  
*   [JsIsEnumeratingHeap Function](./jsisenumeratingheap-function.md)  
*   [JsIsRuntimeExecutionDisabled Function](./jsisruntimeexecutiondisabled-function.md)  
*   [JsNumberToDouble Function](./jsnumbertodouble-function.md)  
*   [JsNumberToInt Function](./jsnumbertoint-function.md)  
*   [JsObjectToInspectable Function](./jsobjecttoinspectable-function.md)  
*   [JsParseScript Function](./jsparsescript-function.md)  
*   [JsParseSerializedScript Function](./jsparseserializedscript-function.md)  
*   [JsParseSerializedScriptWithCallback Function](./jsparseserializedscriptwithcallback-function.md)  
*   [JsPointerToString Function](./jspointertostring-function.md)  
*   [JsPreventExtension Function](./jspreventextension-function.md)  
*   [JsProjectWinRTNamespace Function](./jsprojectwinrtnamespace-function.md)  
*   [JsRelease Function](./jsrelease-function.md)  
*   [JsRunScript Function](./jsrunscript-function.md)  
*   [JsRunSerializedScript Function](./jsrunserializedscript-function.md)  
*   [JsRunSerializedScriptWithCallback Function](./jsrunserializedscriptwithcallback-function.md)  
*   [JsSerializeScript Function](./jsserializescript-function.md)  
*   [JsSetContextData Function](./jssetcontextdata-function.md)  
*   [JsSetCurrentContext Function](./jssetcurrentcontext-function.md)  
*   [JsSetException Function](./jssetexception-function.md)  
*   [JsSetExternalData Function](./jssetexternaldata-function.md)  
*   [JsSetIndexedPropertiesToExternalData Function](./jssetindexedpropertiestoexternaldata-function.md)  
*   [JsSetIndexedProperty Function](./jssetindexedproperty-function.md)  
*   [JsSetObjectBeforeCollectCallback Function](./jssetobjectbeforecollectcallback-function.md)  
*   [JsSetProjectionEnqueueCallback Function](./jssetprojectionenqueuecallback-function.md)  
*   [JsSetPromiseContinuationCallback Function](./jssetpromisecontinuationcallback-function.md)  
*   [JsSetProperty Function](./jssetproperty-function.md)  
*   [JsSetPrototype Function](./jssetprototype-function.md)  
*   [JsSetRuntimeBeforeCollectCallback Function](./jssetruntimebeforecollectcallback-function.md)  
*   [JsSetRuntimeMemoryAllocationCallback Function](./jssetruntimememoryallocationcallback-function.md)  
*   [JsSetRuntimeMemoryLimit Function](./jssetruntimememorylimit-function.md)  
*   [JsStartDebugging Function](./jsstartdebugging-function.md)  
*   [JsStartProfiling Function](./jsstartprofiling-function.md)  
*   [JsStopProfiling Function](./jsstopprofiling-function.md)  
*   [JsStrictEquals Function](./jsstrictequals-function.md)  
*   [JsStringToPointer Function](./jsstringtopointer-function.md)  
*   [JsValueToVariant Function](./jsvaluetovariant-function.md)  
*   [JsVariantToValue Function](./jsvarianttovalue-function.md)  

## Voir également  

*   [Héberger le runtime JavaScript](./hosting-the-javascript-runtime.md)  
*   [Hébergement du runtime JavaScript](../javascript-runtime-hosting.md)  
