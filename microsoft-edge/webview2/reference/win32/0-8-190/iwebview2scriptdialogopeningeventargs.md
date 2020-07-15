---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 052f380caadf08814cc9364f3ccfbb5251fa7c7e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878196"
---
# <span data-ttu-id="ceb9b-104">0.8.355-interface IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="ceb9b-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="ceb9b-105">Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ceb9b-106">Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="ceb9b-107">Arguments d’événement pour l’événement [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="ceb9b-107">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="ceb9b-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="ceb9b-108">Summary</span></span>

 <span data-ttu-id="ceb9b-109">Ses</span><span class="sxs-lookup"><span data-stu-id="ceb9b-109">Members</span></span>                        | <span data-ttu-id="ceb9b-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ceb9b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ceb9b-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ceb9b-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="ceb9b-112">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="ceb9b-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="ceb9b-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="ceb9b-114">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="ceb9b-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="ceb9b-115">get_Message</span></span>](#get_message) | <span data-ttu-id="ceb9b-116">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-116">The message of the dialog box.</span></span>
[<span data-ttu-id="ceb9b-117">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-117">Accept</span></span>](#accept) | <span data-ttu-id="ceb9b-118">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer et inviter les boîtes de dialogue ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-118">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="ceb9b-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="ceb9b-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="ceb9b-120">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="ceb9b-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="ceb9b-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="ceb9b-122">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="ceb9b-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="ceb9b-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="ceb9b-124">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-124">Set the ResultText property.</span></span>
[<span data-ttu-id="ceb9b-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ceb9b-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ceb9b-126">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb9b-126">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="ceb9b-127">Ses</span><span class="sxs-lookup"><span data-stu-id="ceb9b-127">Members</span></span>

#### <span data-ttu-id="ceb9b-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="ceb9b-128">get_Uri</span></span> 

<span data-ttu-id="ceb9b-129">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="ceb9b-130">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="ceb9b-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="ceb9b-131">get_Kind</span></span> 

<span data-ttu-id="ceb9b-132">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="ceb9b-133">[get_Kinds](#get_kind)par valeur public HRESULT (WEBVIEW2_SCRIPT_DIALOG_KIND \* type)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-133">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="ceb9b-134">get_Message</span><span class="sxs-lookup"><span data-stu-id="ceb9b-134">get_Message</span></span> 

<span data-ttu-id="ceb9b-135">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-135">The message of the dialog box.</span></span>

> <span data-ttu-id="ceb9b-136">valeur publique HRESULT [get_Message](#get_message)(LPWSTR \* message)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-136">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="ceb9b-137">À partir de JavaScript il s’agit du premier paramètre passé à alerte, confirmation et invite.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="ceb9b-138">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-138">Accept</span></span> 

<span data-ttu-id="ceb9b-139">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer et inviter les boîtes de dialogue ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-139">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="ceb9b-140">[acceptation](#accept)publique HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="ceb9b-140">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="ceb9b-141">À partir de JavaScript cela signifie que la fonction confirmer retourne la valeur true si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-141">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="ceb9b-142">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-142">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="ceb9b-143">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="ceb9b-143">get_DefaultText</span></span> 

<span data-ttu-id="ceb9b-144">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-144">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="ceb9b-145">valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-145">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="ceb9b-146">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-146">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="ceb9b-147">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="ceb9b-147">get_ResultText</span></span> 

<span data-ttu-id="ceb9b-148">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-148">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="ceb9b-149">valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-149">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="ceb9b-150">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-150">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="ceb9b-151">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-151">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="ceb9b-152">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="ceb9b-152">put_ResultText</span></span> 

<span data-ttu-id="ceb9b-153">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-153">Set the ResultText property.</span></span>

> <span data-ttu-id="ceb9b-154">[put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-154">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="ceb9b-155">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ceb9b-155">GetDeferral</span></span> 

<span data-ttu-id="ceb9b-156">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="ceb9b-156">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="ceb9b-157">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="ceb9b-157">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="ceb9b-158">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="ceb9b-158">You can use this to complete the event at a later time.</span></span>

