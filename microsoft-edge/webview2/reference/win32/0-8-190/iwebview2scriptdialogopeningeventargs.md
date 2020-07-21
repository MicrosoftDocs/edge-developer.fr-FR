---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885792"
---
# <span data-ttu-id="f6b06-104">0.8.355-interface IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="f6b06-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="f6b06-105">Arguments d’événement pour l’événement [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="f6b06-105">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="f6b06-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f6b06-106">Summary</span></span>

 <span data-ttu-id="f6b06-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f6b06-107">Members</span></span>                        | <span data-ttu-id="f6b06-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f6b06-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f6b06-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f6b06-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f6b06-110">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f6b06-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="f6b06-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="f6b06-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="f6b06-112">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f6b06-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="f6b06-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="f6b06-113">get_Message</span></span>](#get_message) | <span data-ttu-id="f6b06-114">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f6b06-114">The message of the dialog box.</span></span>
[<span data-ttu-id="f6b06-115">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="f6b06-115">Accept</span></span>](#accept) | <span data-ttu-id="f6b06-116">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer et inviter les boîtes de dialogue ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="f6b06-116">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="f6b06-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="f6b06-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="f6b06-118">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f6b06-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="f6b06-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="f6b06-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="f6b06-120">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="f6b06-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="f6b06-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="f6b06-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="f6b06-122">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="f6b06-122">Set the ResultText property.</span></span>
[<span data-ttu-id="f6b06-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f6b06-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f6b06-124">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="f6b06-124">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="f6b06-125">Ses</span><span class="sxs-lookup"><span data-stu-id="f6b06-125">Members</span></span>

#### <span data-ttu-id="f6b06-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f6b06-126">get_Uri</span></span> 

<span data-ttu-id="f6b06-127">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f6b06-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="f6b06-128">valeur publique HRESULT [get_URI](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="f6b06-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f6b06-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="f6b06-129">get_Kind</span></span> 

<span data-ttu-id="f6b06-130">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f6b06-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="f6b06-131">[get_Kinds](#get_kind)par valeur public HRESULT (WEBVIEW2_SCRIPT_DIALOG_KIND \* type)</span><span class="sxs-lookup"><span data-stu-id="f6b06-131">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="f6b06-132">get_Message</span><span class="sxs-lookup"><span data-stu-id="f6b06-132">get_Message</span></span> 

<span data-ttu-id="f6b06-133">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="f6b06-133">The message of the dialog box.</span></span>

> <span data-ttu-id="f6b06-134">valeur publique HRESULT [get_Message](#get_message)(LPWSTR \* message)</span><span class="sxs-lookup"><span data-stu-id="f6b06-134">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="f6b06-135">À partir de JavaScript il s’agit du premier paramètre passé à alerte, confirmation et invite.</span><span class="sxs-lookup"><span data-stu-id="f6b06-135">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="f6b06-136">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="f6b06-136">Accept</span></span> 

<span data-ttu-id="f6b06-137">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer et inviter les boîtes de dialogue ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="f6b06-137">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="f6b06-138">[acceptation](#accept)publique HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="f6b06-138">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="f6b06-139">À partir de JavaScript cela signifie que la fonction confirmer retourne la valeur true si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="f6b06-139">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="f6b06-140">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f6b06-140">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="f6b06-141">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="f6b06-141">get_DefaultText</span></span> 

<span data-ttu-id="f6b06-142">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f6b06-142">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="f6b06-143">valeur publique HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="f6b06-143">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="f6b06-144">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f6b06-144">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="f6b06-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="f6b06-145">get_ResultText</span></span> 

<span data-ttu-id="f6b06-146">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="f6b06-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="f6b06-147">valeur publique HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="f6b06-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="f6b06-148">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="f6b06-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="f6b06-149">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="f6b06-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="f6b06-150">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="f6b06-150">put_ResultText</span></span> 

<span data-ttu-id="f6b06-151">Définissez la propriété ResultText.</span><span class="sxs-lookup"><span data-stu-id="f6b06-151">Set the ResultText property.</span></span>

> <span data-ttu-id="f6b06-152">[put_ResultText](#put_resulttext)par le biais du public HRESULT (LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="f6b06-152">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="f6b06-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f6b06-153">GetDeferral</span></span> 

<span data-ttu-id="f6b06-154">GetDeferral peut être appelé pour retourner un objet [IWebView2Deferral](IWebView2Deferral.md) .</span><span class="sxs-lookup"><span data-stu-id="f6b06-154">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="f6b06-155">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* Report)</span><span class="sxs-lookup"><span data-stu-id="f6b06-155">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f6b06-156">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="f6b06-156">You can use this to complete the event at a later time.</span></span>

