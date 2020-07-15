---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: b7071a312ce1fa3ca006a6805a1f712a51d0dab0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879113"
---
# <span data-ttu-id="98fa1-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="98fa1-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="98fa1-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="98fa1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="98fa1-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="98fa1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="98fa1-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="98fa1-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="98fa1-108">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="98fa1-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="98fa1-109">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="98fa1-109">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="98fa1-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="98fa1-110">Summary</span></span>

 <span data-ttu-id="98fa1-111">Ses</span><span class="sxs-lookup"><span data-stu-id="98fa1-111">Members</span></span>                        | <span data-ttu-id="98fa1-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="98fa1-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="98fa1-113">DefaultText</span><span class="sxs-lookup"><span data-stu-id="98fa1-113">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="98fa1-114">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98fa1-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="98fa1-115">Types</span><span class="sxs-lookup"><span data-stu-id="98fa1-115">Kind</span></span>](#kind) | <span data-ttu-id="98fa1-116">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98fa1-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="98fa1-117">Message</span><span class="sxs-lookup"><span data-stu-id="98fa1-117">Message</span></span>](#message) | <span data-ttu-id="98fa1-118">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="98fa1-118">The message of the dialog box.</span></span>
[<span data-ttu-id="98fa1-119">ResultText</span><span class="sxs-lookup"><span data-stu-id="98fa1-119">ResultText</span></span>](#resulttext) | <span data-ttu-id="98fa1-120">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="98fa1-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="98fa1-121">URI</span><span class="sxs-lookup"><span data-stu-id="98fa1-121">Uri</span></span>](#uri) | <span data-ttu-id="98fa1-122">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="98fa1-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="98fa1-123">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="98fa1-123">Accept</span></span>](#accept) | <span data-ttu-id="98fa1-124">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="98fa1-124">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="98fa1-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="98fa1-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="98fa1-126">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="98fa1-126">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="98fa1-127">Ses</span><span class="sxs-lookup"><span data-stu-id="98fa1-127">Members</span></span>

#### <span data-ttu-id="98fa1-128">DefaultText</span><span class="sxs-lookup"><span data-stu-id="98fa1-128">DefaultText</span></span> 

<span data-ttu-id="98fa1-129">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98fa1-129">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="98fa1-130">[DefaultText](#defaulttext) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="98fa1-130">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="98fa1-131">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98fa1-131">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="98fa1-132">Types</span><span class="sxs-lookup"><span data-stu-id="98fa1-132">Kind</span></span> 

<span data-ttu-id="98fa1-133">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="98fa1-133">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="98fa1-134">[type](#kind) CoreWebView2ScriptDialogKind public</span><span class="sxs-lookup"><span data-stu-id="98fa1-134">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="98fa1-135">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="98fa1-135">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="98fa1-136">Message</span><span class="sxs-lookup"><span data-stu-id="98fa1-136">Message</span></span> 

<span data-ttu-id="98fa1-137">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="98fa1-137">The message of the dialog box.</span></span>

> <span data-ttu-id="98fa1-138">[message](#message) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="98fa1-138">public string [Message](#message)</span></span>

<span data-ttu-id="98fa1-139">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="98fa1-139">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="98fa1-140">ResultText</span><span class="sxs-lookup"><span data-stu-id="98fa1-140">ResultText</span></span> 

<span data-ttu-id="98fa1-141">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="98fa1-141">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="98fa1-142">[ResultText](#resulttext) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="98fa1-142">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="98fa1-143">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="98fa1-143">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="98fa1-144">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="98fa1-144">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="98fa1-145">URI</span><span class="sxs-lookup"><span data-stu-id="98fa1-145">Uri</span></span> 

<span data-ttu-id="98fa1-146">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="98fa1-146">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="98fa1-147">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="98fa1-147">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="98fa1-148">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="98fa1-148">Accept</span></span> 

<span data-ttu-id="98fa1-149">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="98fa1-149">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="98fa1-150">public void [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="98fa1-150">public void [Accept](#accept)()</span></span>

<span data-ttu-id="98fa1-151">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="98fa1-151">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="98fa1-152">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="98fa1-152">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="98fa1-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="98fa1-153">GetDeferral</span></span> 

<span data-ttu-id="98fa1-154">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="98fa1-154">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="98fa1-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="98fa1-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="98fa1-156">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="98fa1-156">You can use this to complete the event at a later time.</span></span>

