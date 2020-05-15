---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 45c0a26fa424f87e692b243b43e7a3b189a2acd8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653675"
---
# <span data-ttu-id="8bc2d-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="8bc2d-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="8bc2d-105">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="8bc2d-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="8bc2d-106">Summary</span></span>

 <span data-ttu-id="8bc2d-107">Ses</span><span class="sxs-lookup"><span data-stu-id="8bc2d-107">Members</span></span>                        | <span data-ttu-id="8bc2d-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="8bc2d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8bc2d-109">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-109">Accept</span></span>](#accept) | <span data-ttu-id="8bc2d-110">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-110">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="8bc2d-111">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="8bc2d-111">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="8bc2d-112">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="8bc2d-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="8bc2d-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="8bc2d-114">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="8bc2d-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="8bc2d-115">get_Message</span></span>](#get_message) | <span data-ttu-id="8bc2d-116">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-116">The message of the dialog box.</span></span>
[<span data-ttu-id="8bc2d-117">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="8bc2d-117">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="8bc2d-118">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="8bc2d-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8bc2d-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="8bc2d-120">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="8bc2d-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8bc2d-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="8bc2d-122">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="8bc2d-122">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="8bc2d-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="8bc2d-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="8bc2d-124">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-124">Set the ResultText property.</span></span>

## <span data-ttu-id="8bc2d-125">Ses</span><span class="sxs-lookup"><span data-stu-id="8bc2d-125">Members</span></span>

#### <span data-ttu-id="8bc2d-126">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-126">Accept</span></span> 

<span data-ttu-id="8bc2d-127">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-127">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="8bc2d-128">[acceptation](#accept)publique HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="8bc2d-128">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="8bc2d-129">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-129">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="8bc2d-130">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-130">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="8bc2d-131">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="8bc2d-131">get_DefaultText</span></span> 

<span data-ttu-id="8bc2d-132">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-132">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="8bc2d-133">valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-133">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="8bc2d-134">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-134">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="8bc2d-135">get_Kind</span><span class="sxs-lookup"><span data-stu-id="8bc2d-135">get_Kind</span></span> 

<span data-ttu-id="8bc2d-136">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-136">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="8bc2d-137">[get_Kinds](#get_kind)par valeur public HRESULT (COREWEBVIEW2_SCRIPT_DIALOG_KIND \* type)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-137">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="8bc2d-138">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-138">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="8bc2d-139">get_Message</span><span class="sxs-lookup"><span data-stu-id="8bc2d-139">get_Message</span></span> 

<span data-ttu-id="8bc2d-140">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-140">The message of the dialog box.</span></span>

> <span data-ttu-id="8bc2d-141">valeur publique HRESULT [get_Message](#get_message)(LPWSTR \* message)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-141">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="8bc2d-142">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-142">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="8bc2d-143">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="8bc2d-143">get_ResultText</span></span> 

<span data-ttu-id="8bc2d-144">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-144">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="8bc2d-145">valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-145">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="8bc2d-146">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-146">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="8bc2d-147">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-147">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="8bc2d-148">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8bc2d-148">get_Uri</span></span> 

<span data-ttu-id="8bc2d-149">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-149">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="8bc2d-150">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-150">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="8bc2d-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8bc2d-151">GetDeferral</span></span> 

<span data-ttu-id="8bc2d-152">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="8bc2d-152">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="8bc2d-153">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-153">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="8bc2d-154">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-154">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="8bc2d-155">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="8bc2d-155">put_ResultText</span></span> 

<span data-ttu-id="8bc2d-156">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="8bc2d-156">Set the ResultText property.</span></span>

> <span data-ttu-id="8bc2d-157">[put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="8bc2d-157">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

