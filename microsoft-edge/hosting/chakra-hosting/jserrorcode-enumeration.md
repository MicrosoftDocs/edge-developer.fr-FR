---
description: Code d’erreur retourné par une API d’hébergement Chakra.
title: Énumération JsErrorCode | Documents Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsErrorCode
helpviewer_keywords:
- JsErrorCode enumeration
ms.assetid: 4902f3f3-47a5-4e74-9c29-f96eeecbcda9
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3d1a319872ac69b2acaf19997f3c38f9c04597b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10566333"
---
# <span data-ttu-id="c0a8e-103">Énumération JsErrorCode</span><span class="sxs-lookup"><span data-stu-id="c0a8e-103">JsErrorCode Enumeration</span></span>
<span data-ttu-id="c0a8e-104">Code d’erreur retourné par une API d’hébergement Chakra.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-104">An error code returned from a Chakra hosting API.</span></span>  
  
## <span data-ttu-id="c0a8e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0a8e-105">Syntax</span></span>  
  
```cpp  
enum JsErrorCode : unsigned int;  
```  
  
## <span data-ttu-id="c0a8e-106">Ses</span><span class="sxs-lookup"><span data-stu-id="c0a8e-106">Members</span></span>  
  
### <span data-ttu-id="c0a8e-107">Doubl</span><span class="sxs-lookup"><span data-stu-id="c0a8e-107">Values</span></span>  
  
|<span data-ttu-id="c0a8e-108">Nom</span><span class="sxs-lookup"><span data-stu-id="c0a8e-108">Name</span></span>|<span data-ttu-id="c0a8e-109">Description</span><span class="sxs-lookup"><span data-stu-id="c0a8e-109">Description</span></span>|  
|----------|-----------------|  
|`JsErrorAlreadyDebuggingContext`|<span data-ttu-id="c0a8e-110">Le contexte ne peut pas être placé dans un état de débogage, car il est déjà dans un état de débogage.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-110">The context cannot be put into a debug state because it is already in a debug state.</span></span>|  
|`JsErrorAlreadyProfilingContext`|<span data-ttu-id="c0a8e-111">Le contexte ne peut pas démarrer le profilage, car il est déjà en cours de profilage.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-111">The context cannot start profiling because it is already profiling.</span></span>|  
|`JsErrorArgumentNotObject`|<span data-ttu-id="c0a8e-112">Une API d’hébergement qui fonctionne sur des valeurs d’objet a été appelée avec une valeur non Object.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-112">A hosting API that operates on object values was called with a non-object value.</span></span>|  
|`JsErrorBadSerializedScript`|<span data-ttu-id="c0a8e-113">Un script sérialisé incorrect a été utilisé ou le script sérialisé a été sérialisé par une autre version du moteur Chakra.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-113">A bad serialized script was used, or the serialized script was serialized by a different version of the Chakra engine.</span></span>|  
|`JsErrorCannotDisableExecution`|<span data-ttu-id="c0a8e-114">Le runtime ne prend pas en charge l’interruption du script fiable.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-114">Runtime does not support reliable script interruption.</span></span>|  
|`JsErrorCannotSerializeDebugScript`|<span data-ttu-id="c0a8e-115">Les scripts ne peuvent pas être sérialisés dans les contextes de débogage.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-115">Scripts cannot be serialized in debug contexts.</span></span>|  
|`JsErrorCategoryEngine`|<span data-ttu-id="c0a8e-116">Catégories d’erreurs liées à des erreurs se produisant dans le moteur lui-même.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-116">Category of errors that relates to errors occurring within the engine itself.</span></span>|  
|`JsErrorCategoryFatal`|<span data-ttu-id="c0a8e-117">Catégorie d’erreurs irrécupérable et signifiant échec du moteur.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-117">Category of errors that are fatal and signify failure of the engine.</span></span>|  
|`JsErrorCategoryScript`|<span data-ttu-id="c0a8e-118">Catégories d’erreurs liées aux erreurs dans un script.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-118">Category of errors that relates to errors in a script.</span></span>|  
|`JsErrorCategoryUsage`|<span data-ttu-id="c0a8e-119">Catégories d’erreurs liées à l’utilisation incorrecte de l’API elle-même.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-119">Category of errors that relates to incorrect usage of the API itself.</span></span>|  
|`JsErrorFatal`|<span data-ttu-id="c0a8e-120">Une erreur irrécupérable s’est produite dans le moteur.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-120">A fatal error in the engine has occurred.</span></span>|  
|`JsErrorHeapEnumInProgress`|<span data-ttu-id="c0a8e-121">Une énumération de tas est actuellement en cours dans le contexte de script.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-121">A heap enumeration is currently underway in the script context.</span></span>|  
|`JsErrorIdleNotEnabled`|<span data-ttu-id="c0a8e-122">Notification inactif fournie lorsque l’hôte n’a pas activé le traitement inactif.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-122">Idle notification given when the host did not enable idle processing.</span></span>|  
|`JsErrorInDisabledState`|<span data-ttu-id="c0a8e-123">Le runtime est dans un état désactivé.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-123">The runtime is in a disabled state.</span></span>|  
|`JsErrorInExceptionState`|<span data-ttu-id="c0a8e-124">Le moteur est dans un état d’exception et aucune API ne peut être appelée tant que l’exception n’est pas supprimée.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-124">The engine is in an exception state and no APIs can be called until the exception is cleared.</span></span>|  
|`JsErrorInObjectBeforeCollectCallback`|<span data-ttu-id="c0a8e-125">L’opération n’est pas prise en charge dans un objet avant la collecte du rappel.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-125">The operation is not supported in an object before collect callback.</span></span><br /><br /> <span data-ttu-id="c0a8e-126">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-126">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorInProfileCallback`|<span data-ttu-id="c0a8e-127">Un contexte de script se trouve au milieu d’un rappel de profil.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-127">A script context is in the middle of a profile callback.</span></span>|  
|`JsErrorInThreadServiceCallback`|<span data-ttu-id="c0a8e-128">Un rappel de service de thread est actuellement en cours.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-128">A thread service callback is currently underway.</span></span>|  
|`JsErrorInvalidArgument`|<span data-ttu-id="c0a8e-129">Un argument d’une API d’hébergement n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-129">An argument to a hosting API was invalid.</span></span>|  
|`JsErrorNoCurrentContext`|<span data-ttu-id="c0a8e-130">L’API d’hébergement exige qu’un contexte soit à jour, mais qu’il n’y ait aucun contexte actuel.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-130">The hosting API requires that a context be current, but there is no current context.</span></span>|  
|`JsErrorNotImplemented`|<span data-ttu-id="c0a8e-131">Une API d’hébergement n’est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-131">A hosting API is not yet implemented.</span></span>|  
|`JsErrorNullArgument`|<span data-ttu-id="c0a8e-132">Un argument pour une API d’hébergement a la valeur null dans un contexte pour lequel la valeur NULL n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-132">An argument to a hosting API was null in a context where null is not allowed.</span></span>|  
|`JsErrorObjectNotInspectable`|<span data-ttu-id="c0a8e-133">L’objet ne peut pas être ajusté au `IInspectable` pointeur.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-133">Object cannot be unwrapped to `IInspectable` pointer.</span></span><br /><br /> <span data-ttu-id="c0a8e-134">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-134">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorOutOfMemory`|<span data-ttu-id="c0a8e-135">Mémoire insuffisante pour le moteur Chakra.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-135">The Chakra engine has run out of memory.</span></span>|  
|`JsErrorPropertyNotSymbol`|<span data-ttu-id="c0a8e-136">Une API d’hébergement qui fonctionne sur les ID de propriété de symbole mais qui a été appelée avec un ID de propriété sans symbole. Le code d’erreur est retourné par `JsGetSymbolFromPropertyId` si la fonction est appelée avec un ID de propriété sans symbole.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-136">A hosting API that operates on symbol property ids but was called with a non-symbol property id. The error code is returned by `JsGetSymbolFromPropertyId` if the function is called with non-symbol property id.</span></span><br /><br /> <span data-ttu-id="c0a8e-137">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-137">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorPropertyNotString`|<span data-ttu-id="c0a8e-138">API d’hébergement qui fonctionne sur les ID de propriété de chaîne, mais qui a été appelée avec un ID de propriété autre qu’une chaîne. Le code d’erreur est retourné par existing `JsGetPropertyNamefromId` si la fonction est appelée avec un ID de propriété autre qu’une chaîne.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-138">A hosting API that operates on string property ids but was called with a non-string property id. The error code is returned by existing `JsGetPropertyNamefromId` if the function is called with non-string property id.</span></span><br /><br /> <span data-ttu-id="c0a8e-139">Cette valeur d’énumération est uniquement prise en charge en mode Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-139">This enumeration value is supported only in Microsoft Edge mode.</span></span>|  
|`JsErrorRuntimeInUse`|<span data-ttu-id="c0a8e-140">Un Runtime toujours en cours d’utilisation ne peut pas être supprimé.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-140">A runtime that is still in use cannot be disposed.</span></span>|  
|`JsErrorScriptCompile`|<span data-ttu-id="c0a8e-141">JavaScript n’a pas réussi à compiler.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-141">JavaScript failed to compile.</span></span>|  
|`JsErrorScriptEvalDisabled`|<span data-ttu-id="c0a8e-142">Un script a été arrêté car il a essayé d’utiliser `eval` ou `function` et eval a été désactivé.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-142">A script was terminated because it tried to use `eval` or `function` and eval was disabled.</span></span>|  
|`JsErrorScriptException`|<span data-ttu-id="c0a8e-143">Une exception JavaScript s’est produite lors de l’exécution d’un script.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-143">A JavaScript exception occurred while running a script.</span></span>|  
|`JsErrorScriptTerminated`|<span data-ttu-id="c0a8e-144">Un script a été arrêté en raison d’une demande de suspension d’un Runtime.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-144">A script was terminated due to a request to suspend a runtime.</span></span>|  
|`JsErrorWrongRuntime`|<span data-ttu-id="c0a8e-145">Une API d’hébergement a été appelée avec un objet créé sur un autre Runtime JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-145">A hosting API was called with object created on different JavaScript runtime.</span></span>|  
|`JsErrorWrongThread`|<span data-ttu-id="c0a8e-146">Une API d’hébergement a été appelée sur le thread incorrect.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-146">A hosting API was called on the wrong thread.</span></span>|  
|`JsNoError`|<span data-ttu-id="c0a8e-147">Code d’erreur de réussite.</span><span class="sxs-lookup"><span data-stu-id="c0a8e-147">Success error code.</span></span>|  
  
## <span data-ttu-id="c0a8e-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0a8e-148">Requirements</span></span>  
 <span data-ttu-id="c0a8e-149">**En-tête:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="c0a8e-149">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="c0a8e-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0a8e-150">See Also</span></span>  
 [<span data-ttu-id="c0a8e-151">Référence (Runtime JavaScript)</span><span class="sxs-lookup"><span data-stu-id="c0a8e-151">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)