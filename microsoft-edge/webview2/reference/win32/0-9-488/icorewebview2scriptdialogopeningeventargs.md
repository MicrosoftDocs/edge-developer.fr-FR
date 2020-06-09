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
ms.openlocfilehash: 33450805c7f5117806feb1fb561cd7e0c364f00e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698098"
---
# <span data-ttu-id="b92ff-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="b92ff-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b92ff-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b92ff-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b92ff-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="b92ff-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="b92ff-107">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="b92ff-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="b92ff-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b92ff-108">Summary</span></span>

 <span data-ttu-id="b92ff-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b92ff-109">Members</span></span>                        | <span data-ttu-id="b92ff-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b92ff-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b92ff-111">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="b92ff-111">Accept</span></span>](#accept) | <span data-ttu-id="b92ff-112">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="b92ff-112">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="b92ff-113">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="b92ff-113">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="b92ff-114">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b92ff-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="b92ff-115">get_Kind</span><span class="sxs-lookup"><span data-stu-id="b92ff-115">get_Kind</span></span>](#get_kind) | <span data-ttu-id="b92ff-116">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b92ff-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="b92ff-117">get_Message</span><span class="sxs-lookup"><span data-stu-id="b92ff-117">get_Message</span></span>](#get_message) | <span data-ttu-id="b92ff-118">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b92ff-118">The message of the dialog box.</span></span>
[<span data-ttu-id="b92ff-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="b92ff-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="b92ff-120">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="b92ff-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="b92ff-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b92ff-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b92ff-122">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b92ff-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="b92ff-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b92ff-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="b92ff-124">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b92ff-124">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="b92ff-125">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="b92ff-125">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="b92ff-126">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="b92ff-126">Set the ResultText property.</span></span>

## <span data-ttu-id="b92ff-127">Ses</span><span class="sxs-lookup"><span data-stu-id="b92ff-127">Members</span></span>

#### <span data-ttu-id="b92ff-128">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="b92ff-128">Accept</span></span> 

<span data-ttu-id="b92ff-129">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="b92ff-129">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="b92ff-130">[acceptation](#accept)publique HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="b92ff-130">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="b92ff-131">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="b92ff-131">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="b92ff-132">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="b92ff-132">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="b92ff-133">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="b92ff-133">get_DefaultText</span></span> 

<span data-ttu-id="b92ff-134">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b92ff-134">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="b92ff-135">valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="b92ff-135">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="b92ff-136">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b92ff-136">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="b92ff-137">get_Kind</span><span class="sxs-lookup"><span data-stu-id="b92ff-137">get_Kind</span></span> 

<span data-ttu-id="b92ff-138">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b92ff-138">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="b92ff-139">[get_Kinds](#get_kind)par valeur public HRESULT (COREWEBVIEW2_SCRIPT_DIALOG_KIND \* type)</span><span class="sxs-lookup"><span data-stu-id="b92ff-139">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="b92ff-140">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="b92ff-140">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="b92ff-141">get_Message</span><span class="sxs-lookup"><span data-stu-id="b92ff-141">get_Message</span></span> 

<span data-ttu-id="b92ff-142">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b92ff-142">The message of the dialog box.</span></span>

> <span data-ttu-id="b92ff-143">valeur publique HRESULT [get_Message](#get_message)(LPWSTR \* message)</span><span class="sxs-lookup"><span data-stu-id="b92ff-143">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="b92ff-144">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="b92ff-144">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="b92ff-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="b92ff-145">get_ResultText</span></span> 

<span data-ttu-id="b92ff-146">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="b92ff-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="b92ff-147">valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="b92ff-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="b92ff-148">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="b92ff-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="b92ff-149">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="b92ff-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="b92ff-150">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b92ff-150">get_Uri</span></span> 

<span data-ttu-id="b92ff-151">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="b92ff-151">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="b92ff-152">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="b92ff-152">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b92ff-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="b92ff-153">GetDeferral</span></span> 

<span data-ttu-id="b92ff-154">GetDeferral peut être appelé pour retourner un objet [ICoreWebView2Deferral](icorewebview2deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="b92ff-154">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="b92ff-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="b92ff-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="b92ff-156">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="b92ff-156">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="b92ff-157">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="b92ff-157">put_ResultText</span></span> 

<span data-ttu-id="b92ff-158">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="b92ff-158">Set the ResultText property.</span></span>

> <span data-ttu-id="b92ff-159">[put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="b92ff-159">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

