---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 93e662088ae1561b5dcb33390f46a41c19ca0aaf
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698595"
---
# <span data-ttu-id="703b1-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="703b1-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

<span data-ttu-id="703b1-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="703b1-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="703b1-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="703b1-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="703b1-107">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="703b1-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="703b1-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="703b1-108">Summary</span></span>

 <span data-ttu-id="703b1-109">Ses</span><span class="sxs-lookup"><span data-stu-id="703b1-109">Members</span></span>                        | <span data-ttu-id="703b1-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="703b1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="703b1-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="703b1-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="703b1-112">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="703b1-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="703b1-113">Types</span><span class="sxs-lookup"><span data-stu-id="703b1-113">Kind</span></span>](#kind) | <span data-ttu-id="703b1-114">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="703b1-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="703b1-115">Message</span><span class="sxs-lookup"><span data-stu-id="703b1-115">Message</span></span>](#message) | <span data-ttu-id="703b1-116">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="703b1-116">The message of the dialog box.</span></span>
[<span data-ttu-id="703b1-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="703b1-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="703b1-118">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="703b1-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="703b1-119">URI</span><span class="sxs-lookup"><span data-stu-id="703b1-119">Uri</span></span>](#uri) | <span data-ttu-id="703b1-120">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="703b1-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="703b1-121">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="703b1-121">Accept</span></span>](#accept) | <span data-ttu-id="703b1-122">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="703b1-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="703b1-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="703b1-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="703b1-124">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="703b1-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="703b1-125">Ses</span><span class="sxs-lookup"><span data-stu-id="703b1-125">Members</span></span>

#### <span data-ttu-id="703b1-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="703b1-126">DefaultText</span></span> 

<span data-ttu-id="703b1-127">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="703b1-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="703b1-128">[DefaultText](#defaulttext) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="703b1-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="703b1-129">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="703b1-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="703b1-130">Types</span><span class="sxs-lookup"><span data-stu-id="703b1-130">Kind</span></span> 

<span data-ttu-id="703b1-131">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="703b1-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="703b1-132">[type](#kind) CoreWebView2ScriptDialogKind public</span><span class="sxs-lookup"><span data-stu-id="703b1-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="703b1-133">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="703b1-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="703b1-134">Message</span><span class="sxs-lookup"><span data-stu-id="703b1-134">Message</span></span> 

<span data-ttu-id="703b1-135">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="703b1-135">The message of the dialog box.</span></span>

> <span data-ttu-id="703b1-136">[message](#message) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="703b1-136">public string [Message](#message)</span></span>

<span data-ttu-id="703b1-137">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="703b1-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="703b1-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="703b1-138">ResultText</span></span> 

<span data-ttu-id="703b1-139">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="703b1-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="703b1-140">[ResultText](#resulttext) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="703b1-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="703b1-141">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="703b1-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="703b1-142">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="703b1-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="703b1-143">URI</span><span class="sxs-lookup"><span data-stu-id="703b1-143">Uri</span></span> 

<span data-ttu-id="703b1-144">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="703b1-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="703b1-145">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="703b1-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="703b1-146">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="703b1-146">Accept</span></span> 

<span data-ttu-id="703b1-147">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="703b1-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="703b1-148">public void [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="703b1-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="703b1-149">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="703b1-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="703b1-150">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="703b1-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="703b1-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="703b1-151">GetDeferral</span></span> 

<span data-ttu-id="703b1-152">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="703b1-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="703b1-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="703b1-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="703b1-154">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="703b1-154">You can use this to complete the event at a later time.</span></span>

