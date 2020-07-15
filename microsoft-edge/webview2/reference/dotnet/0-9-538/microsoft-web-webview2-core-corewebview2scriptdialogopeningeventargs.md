---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: cbff39e9393026f51471bdfb3189600e2d7bf109
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879694"
---
# <span data-ttu-id="d9935-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="d9935-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

<span data-ttu-id="d9935-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d9935-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d9935-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d9935-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d9935-107">Arguments d’événement pour l’événement ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="d9935-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="d9935-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="d9935-108">Summary</span></span>

 <span data-ttu-id="d9935-109">Ses</span><span class="sxs-lookup"><span data-stu-id="d9935-109">Members</span></span>                        | <span data-ttu-id="d9935-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="d9935-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d9935-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="d9935-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="d9935-112">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9935-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="d9935-113">Types</span><span class="sxs-lookup"><span data-stu-id="d9935-113">Kind</span></span>](#kind) | <span data-ttu-id="d9935-114">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9935-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="d9935-115">Message</span><span class="sxs-lookup"><span data-stu-id="d9935-115">Message</span></span>](#message) | <span data-ttu-id="d9935-116">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9935-116">The message of the dialog box.</span></span>
[<span data-ttu-id="d9935-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="d9935-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="d9935-118">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="d9935-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="d9935-119">URI</span><span class="sxs-lookup"><span data-stu-id="d9935-119">Uri</span></span>](#uri) | <span data-ttu-id="d9935-120">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9935-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="d9935-121">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="d9935-121">Accept</span></span>](#accept) | <span data-ttu-id="d9935-122">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="d9935-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="d9935-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d9935-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d9935-124">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="d9935-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="d9935-125">Ses</span><span class="sxs-lookup"><span data-stu-id="d9935-125">Members</span></span>

#### <span data-ttu-id="d9935-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="d9935-126">DefaultText</span></span> 

<span data-ttu-id="d9935-127">Deuxième paramètre passé à la boîte de dialogue d’invite JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9935-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="d9935-128">[DefaultText](#defaulttext) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="d9935-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="d9935-129">Il s’agit de la valeur par défaut à utiliser pour le résultat de la fonction invites JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9935-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="d9935-130">Types</span><span class="sxs-lookup"><span data-stu-id="d9935-130">Kind</span></span> 

<span data-ttu-id="d9935-131">Type de boîte de dialogue JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d9935-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="d9935-132">[type](#kind) CoreWebView2ScriptDialogKind public</span><span class="sxs-lookup"><span data-stu-id="d9935-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="d9935-133">Accepter, confirmer, demander ou beforeunload.</span><span class="sxs-lookup"><span data-stu-id="d9935-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="d9935-134">Message</span><span class="sxs-lookup"><span data-stu-id="d9935-134">Message</span></span> 

<span data-ttu-id="d9935-135">Message de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9935-135">The message of the dialog box.</span></span>

> <span data-ttu-id="d9935-136">[message](#message) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="d9935-136">public string [Message](#message)</span></span>

<span data-ttu-id="d9935-137">JavaScript il s’agit du premier paramètre passé aux alertes, confirmation et invite, et est vide pour beforeunload.</span><span class="sxs-lookup"><span data-stu-id="d9935-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="d9935-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="d9935-138">ResultText</span></span> 

<span data-ttu-id="d9935-139">Valeur de retour de la fonction d’invite JavaScript si Accept est appelé.</span><span class="sxs-lookup"><span data-stu-id="d9935-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="d9935-140">[ResultText](#resulttext) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="d9935-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="d9935-141">Ceci est ignoré pour les types de boîte de dialogue autres que invite.</span><span class="sxs-lookup"><span data-stu-id="d9935-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="d9935-142">Si Accept n’est pas appelée, cette valeur est ignorée et false est renvoyée de prompt.</span><span class="sxs-lookup"><span data-stu-id="d9935-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="d9935-143">URI</span><span class="sxs-lookup"><span data-stu-id="d9935-143">Uri</span></span> 

<span data-ttu-id="d9935-144">URI de la page qui a demandé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="d9935-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="d9935-145">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="d9935-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="d9935-146">Accept (Accepter)</span><span class="sxs-lookup"><span data-stu-id="d9935-146">Accept</span></span> 

<span data-ttu-id="d9935-147">L’hôte est susceptible de vous appeler pour répondre avec OK pour confirmer, inviter et beforeunload des boîtes de dialogue, ou ne pas appeler cette méthode pour indiquer l’annulation.</span><span class="sxs-lookup"><span data-stu-id="d9935-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="d9935-148">public void [Accept](#accept)()</span><span class="sxs-lookup"><span data-stu-id="d9935-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="d9935-149">À partir de JavaScript, cela signifie que la fonction confirmer et beforeunload renvoie vrai si l’argument accepter est appelé.</span><span class="sxs-lookup"><span data-stu-id="d9935-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="d9935-150">Et pour la fonction prompt, elle renvoie la valeur de ResultText si Accept est appelé et renvoie false dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="d9935-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="d9935-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d9935-151">GetDeferral</span></span> 

<span data-ttu-id="d9935-152">GetDeferral peut être appelé pour retourner un objet CoreWebView2Deferral.</span><span class="sxs-lookup"><span data-stu-id="d9935-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="d9935-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="d9935-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="d9935-154">Vous pouvez l’utiliser pour remplir l’événement ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="d9935-154">You can use this to complete the event at a later time.</span></span>

