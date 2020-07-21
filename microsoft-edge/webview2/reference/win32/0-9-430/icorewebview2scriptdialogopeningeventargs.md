---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: cd8f96787d289ab0fe649244ce665445efdbcecf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884042"
---
# <span data-ttu-id="d9cd1-104">0.9.430-interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="d9cd1-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="d9cd1-105">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="d9cd1-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="d9cd1-106">Summary</span></span>

 <span data-ttu-id="d9cd1-107">Ses</span><span class="sxs-lookup"><span data-stu-id="d9cd1-107">Members</span></span>                        | <span data-ttu-id="d9cd1-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d9cd1-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9cd1-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d9cd1-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="d9cd1-110">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="d9cd1-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="d9cd1-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="d9cd1-112">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="d9cd1-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="d9cd1-113">get_Message</span></span>](#get_message) | <span data-ttu-id="d9cd1-114">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-114">The message of the dialog box.</span></span>
[<span data-ttu-id="d9cd1-115">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-115">Accept</span></span>](#accept) | <span data-ttu-id="d9cd1-116">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-116">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="d9cd1-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="d9cd1-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="d9cd1-118">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="d9cd1-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="d9cd1-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="d9cd1-120">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="d9cd1-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="d9cd1-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="d9cd1-122">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-122">Set the ResultText property.</span></span>
[<span data-ttu-id="d9cd1-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d9cd1-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d9cd1-124">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="d9cd1-124">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="d9cd1-125">Ses</span><span class="sxs-lookup"><span data-stu-id="d9cd1-125">Members</span></span>

#### <span data-ttu-id="d9cd1-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d9cd1-126">get_Uri</span></span> 

<span data-ttu-id="d9cd1-127">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="d9cd1-128">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="d9cd1-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="d9cd1-129">get_Kind</span></span> 

<span data-ttu-id="d9cd1-130">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="d9cd1-131">[get_Kinds](#get_kind)par valeur public HRESULT (CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* type)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-131">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="d9cd1-132">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-132">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="d9cd1-133">get_Message</span><span class="sxs-lookup"><span data-stu-id="d9cd1-133">get_Message</span></span> 

<span data-ttu-id="d9cd1-134">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-134">The message of the dialog box.</span></span>

> <span data-ttu-id="d9cd1-135">valeur publique HRESULT [get_Message](#get_message)(LPWSTR \* message)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-135">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="d9cd1-136">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-136">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="d9cd1-137">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-137">Accept</span></span> 

<span data-ttu-id="d9cd1-138">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-138">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="d9cd1-139">[acceptation](#accept)publique HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="d9cd1-139">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="d9cd1-140">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-140">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="d9cd1-141">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-141">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="d9cd1-142">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="d9cd1-142">get_DefaultText</span></span> 

<span data-ttu-id="d9cd1-143">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-143">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="d9cd1-144">valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-144">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="d9cd1-145">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-145">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="d9cd1-146">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="d9cd1-146">get_ResultText</span></span> 

<span data-ttu-id="d9cd1-147">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-147">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="d9cd1-148">valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-148">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="d9cd1-149">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-149">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="d9cd1-150">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-150">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="d9cd1-151">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="d9cd1-151">put_ResultText</span></span> 

<span data-ttu-id="d9cd1-152">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-152">Set the ResultText property.</span></span>

> <span data-ttu-id="d9cd1-153">[put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-153">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="d9cd1-154">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d9cd1-154">GetDeferral</span></span> 

<span data-ttu-id="d9cd1-155">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](ICoreWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="d9cd1-155">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="d9cd1-156">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="d9cd1-156">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="d9cd1-157">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d9cd1-157">You can use this to complete the event at a later time.</span></span>

