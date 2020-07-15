---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: dfd3383318daf94e8060ba62ef1511c9944efe54
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880212"
---
# <span data-ttu-id="4c0d1-104">0.9.430-interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="4c0d1-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4c0d1-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="4c0d1-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="4c0d1-107">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="4c0d1-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4c0d1-108">Summary</span></span>

 <span data-ttu-id="4c0d1-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4c0d1-109">Members</span></span>                        | <span data-ttu-id="4c0d1-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4c0d1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4c0d1-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4c0d1-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="4c0d1-112">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="4c0d1-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="4c0d1-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="4c0d1-114">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="4c0d1-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="4c0d1-115">get_Message</span></span>](#get_message) | <span data-ttu-id="4c0d1-116">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-116">The message of the dialog box.</span></span>
[<span data-ttu-id="4c0d1-117">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-117">Accept</span></span>](#accept) | <span data-ttu-id="4c0d1-118">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="4c0d1-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="4c0d1-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="4c0d1-120">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="4c0d1-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="4c0d1-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="4c0d1-122">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="4c0d1-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="4c0d1-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="4c0d1-124">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-124">Set the ResultText property.</span></span>
[<span data-ttu-id="4c0d1-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4c0d1-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4c0d1-126">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="4c0d1-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="4c0d1-127">Ses</span><span class="sxs-lookup"><span data-stu-id="4c0d1-127">Members</span></span>

#### <span data-ttu-id="4c0d1-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4c0d1-128">get_Uri</span></span> 

<span data-ttu-id="4c0d1-129">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="4c0d1-130">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="4c0d1-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="4c0d1-131">get_Kind</span></span> 

<span data-ttu-id="4c0d1-132">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="4c0d1-133">[get_Kinds](#get_kind)par valeur public HRESULT (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* type)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="4c0d1-134">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="4c0d1-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="4c0d1-135">get_Message</span></span> 

<span data-ttu-id="4c0d1-136">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-136">The message of the dialog box.</span></span>

> <span data-ttu-id="4c0d1-137">valeur publique HRESULT [get_Message](#get_message)(LPWSTR \* message)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="4c0d1-138">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="4c0d1-139">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-139">Accept</span></span> 

<span data-ttu-id="4c0d1-140">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="4c0d1-141">[acceptation](#accept)publique HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="4c0d1-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="4c0d1-142">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="4c0d1-143">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="4c0d1-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="4c0d1-144">get_DefaultText</span></span> 

<span data-ttu-id="4c0d1-145">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="4c0d1-146">valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="4c0d1-147">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="4c0d1-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="4c0d1-148">get_ResultText</span></span> 

<span data-ttu-id="4c0d1-149">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="4c0d1-150">valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="4c0d1-151">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="4c0d1-152">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="4c0d1-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="4c0d1-153">put_ResultText</span></span> 

<span data-ttu-id="4c0d1-154">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-154">Set the ResultText property.</span></span>

> <span data-ttu-id="4c0d1-155">[put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="4c0d1-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4c0d1-156">GetDeferral</span></span> 

<span data-ttu-id="4c0d1-157">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="4c0d1-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="4c0d1-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="4c0d1-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="4c0d1-159">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="4c0d1-159">You can use this to complete the event at a later time.</span></span>

