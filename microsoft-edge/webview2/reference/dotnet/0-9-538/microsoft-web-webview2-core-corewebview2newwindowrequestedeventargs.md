---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: 2a2934e1fef6c601155cb4002a0c97ca1629099e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878805"
---
# <span data-ttu-id="44298-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="44298-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="44298-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="44298-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="44298-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="44298-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="44298-107">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="44298-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="44298-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="44298-108">Summary</span></span>

 <span data-ttu-id="44298-109">Ses</span><span class="sxs-lookup"><span data-stu-id="44298-109">Members</span></span>                        | <span data-ttu-id="44298-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="44298-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="44298-111">Handled</span><span class="sxs-lookup"><span data-stu-id="44298-111">Handled</span></span>](#handled) | <span data-ttu-id="44298-112">Si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="44298-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="44298-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="44298-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="44298-114">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="44298-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="44298-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="44298-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="44298-116">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="44298-116">Gets the new window.</span></span>
[<span data-ttu-id="44298-117">URI</span><span class="sxs-lookup"><span data-stu-id="44298-117">Uri</span></span>](#uri) | <span data-ttu-id="44298-118">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="44298-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="44298-119">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="44298-119">WindowFeatures</span></span>](#windowfeatures) | <span data-ttu-id="44298-120">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="44298-120">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="44298-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="44298-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="44298-122">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="44298-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="44298-123">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="44298-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="44298-124">Ses</span><span class="sxs-lookup"><span data-stu-id="44298-124">Members</span></span>

#### <span data-ttu-id="44298-125">Handled</span><span class="sxs-lookup"><span data-stu-id="44298-125">Handled</span></span> 

<span data-ttu-id="44298-126">Si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="44298-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="44298-127">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="44298-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="44298-128">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="44298-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="44298-129">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="44298-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="44298-130">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="44298-130">Default is false.</span></span>

#### <span data-ttu-id="44298-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="44298-131">IsUserInitiated</span></span> 

<span data-ttu-id="44298-132">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="44298-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="44298-133">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="44298-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="44298-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="44298-134">NewWindow</span></span> 

<span data-ttu-id="44298-135">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="44298-135">Gets the new window.</span></span>

> <span data-ttu-id="44298-136">public CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="44298-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="44298-137">URI</span><span class="sxs-lookup"><span data-stu-id="44298-137">Uri</span></span> 

<span data-ttu-id="44298-138">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="44298-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="44298-139">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="44298-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="44298-140">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="44298-140">The target webview should not be navigated.</span></span> <span data-ttu-id="44298-141">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="44298-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="44298-142">WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="44298-142">WindowFeatures</span></span> 

<span data-ttu-id="44298-143">Fonctionnalités de fenêtre spécifiées par l’appel Window. Open.</span><span class="sxs-lookup"><span data-stu-id="44298-143">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="44298-144">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span><span class="sxs-lookup"><span data-stu-id="44298-144">public CoreWebView2WindowFeatures [WindowFeatures](#windowfeatures)</span></span>

<span data-ttu-id="44298-145">Ces fonctionnalités peuvent être envisagées pour le positionnement et le dimensionnement des nouvelles fenêtres WebView.</span><span class="sxs-lookup"><span data-stu-id="44298-145">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="44298-146">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="44298-146">GetDeferral</span></span> 

<span data-ttu-id="44298-147">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="44298-147">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="44298-148">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="44298-148">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="44298-149">Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="44298-149">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="44298-150">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="44298-150">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

