---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: cca15ccc5292f5eaf6f317ffb657f46fcd84b4a9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653630"
---
# <span data-ttu-id="cc26c-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cc26c-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

<span data-ttu-id="cc26c-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cc26c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cc26c-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="cc26c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cc26c-107">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="cc26c-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="cc26c-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="cc26c-108">Summary</span></span>

 <span data-ttu-id="cc26c-109">Ses</span><span class="sxs-lookup"><span data-stu-id="cc26c-109">Members</span></span>                        | <span data-ttu-id="cc26c-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="cc26c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cc26c-111">Handled</span><span class="sxs-lookup"><span data-stu-id="cc26c-111">Handled</span></span>](#handled) | <span data-ttu-id="cc26c-112">Si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="cc26c-112">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="cc26c-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cc26c-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="cc26c-114">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="cc26c-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="cc26c-115">NewWindow</span><span class="sxs-lookup"><span data-stu-id="cc26c-115">NewWindow</span></span>](#newwindow) | <span data-ttu-id="cc26c-116">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cc26c-116">Gets the new window.</span></span>
[<span data-ttu-id="cc26c-117">URI</span><span class="sxs-lookup"><span data-stu-id="cc26c-117">Uri</span></span>](#uri) | <span data-ttu-id="cc26c-118">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cc26c-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="cc26c-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cc26c-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="cc26c-120">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="cc26c-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="cc26c-121">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="cc26c-121">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="cc26c-122">Ses</span><span class="sxs-lookup"><span data-stu-id="cc26c-122">Members</span></span>

#### <span data-ttu-id="cc26c-123">Handled</span><span class="sxs-lookup"><span data-stu-id="cc26c-123">Handled</span></span> 

<span data-ttu-id="cc26c-124">Si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="cc26c-124">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="cc26c-125">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="cc26c-125">public bool [Handled](#handled)</span></span>

<span data-ttu-id="cc26c-126">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="cc26c-126">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="cc26c-127">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="cc26c-127">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="cc26c-128">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="cc26c-128">Default is false.</span></span>

#### <span data-ttu-id="cc26c-129">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cc26c-129">IsUserInitiated</span></span> 

<span data-ttu-id="cc26c-130">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="cc26c-130">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="cc26c-131">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="cc26c-131">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="cc26c-132">NewWindow</span><span class="sxs-lookup"><span data-stu-id="cc26c-132">NewWindow</span></span> 

<span data-ttu-id="cc26c-133">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="cc26c-133">Gets the new window.</span></span>

> <span data-ttu-id="cc26c-134">public CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="cc26c-134">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="cc26c-135">URI</span><span class="sxs-lookup"><span data-stu-id="cc26c-135">Uri</span></span> 

<span data-ttu-id="cc26c-136">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cc26c-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="cc26c-137">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="cc26c-137">public string [Uri](#uri)</span></span>

<span data-ttu-id="cc26c-138">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="cc26c-138">The target webview should not be navigated.</span></span> <span data-ttu-id="cc26c-139">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="cc26c-139">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="cc26c-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cc26c-140">GetDeferral</span></span> 

<span data-ttu-id="cc26c-141">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="cc26c-141">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="cc26c-142">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="cc26c-142">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="cc26c-143">Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="cc26c-143">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="cc26c-144">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="cc26c-144">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

