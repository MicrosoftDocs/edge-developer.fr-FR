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
ms.openlocfilehash: c3f9b8bb9451d8364424db01ea19aecedb362d59
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697167"
---
# <span data-ttu-id="6e197-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6e197-104">Microsoft.Web.WebView2.Core.CoreWebView2NewWindowRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="6e197-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="6e197-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6e197-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="6e197-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="6e197-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6e197-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6e197-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="6e197-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6e197-109">Arguments d’événement pour l’événement NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="6e197-109">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="6e197-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="6e197-110">Summary</span></span>

 <span data-ttu-id="6e197-111">Ses</span><span class="sxs-lookup"><span data-stu-id="6e197-111">Members</span></span>                        | <span data-ttu-id="6e197-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6e197-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6e197-113">Handled</span><span class="sxs-lookup"><span data-stu-id="6e197-113">Handled</span></span>](#handled) | <span data-ttu-id="6e197-114">Si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="6e197-114">Whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="6e197-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6e197-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="6e197-116">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="6e197-116">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="6e197-117">NewWindow</span><span class="sxs-lookup"><span data-stu-id="6e197-117">NewWindow</span></span>](#newwindow) | <span data-ttu-id="6e197-118">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6e197-118">Gets the new window.</span></span>
[<span data-ttu-id="6e197-119">URI</span><span class="sxs-lookup"><span data-stu-id="6e197-119">Uri</span></span>](#uri) | <span data-ttu-id="6e197-120">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="6e197-120">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="6e197-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6e197-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="6e197-122">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="6e197-122">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

<span data-ttu-id="6e197-123">L’événement est déclenché lorsque le contenu de l’affichage WebView est demandé à une nouvelle fenêtre (via Window. Open () et ainsi de suite.)</span><span class="sxs-lookup"><span data-stu-id="6e197-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="6e197-124">Ses</span><span class="sxs-lookup"><span data-stu-id="6e197-124">Members</span></span>

#### <span data-ttu-id="6e197-125">Handled</span><span class="sxs-lookup"><span data-stu-id="6e197-125">Handled</span></span> 

<span data-ttu-id="6e197-126">Si NewWindowRequestedEvent est géré par Host.</span><span class="sxs-lookup"><span data-stu-id="6e197-126">Whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="6e197-127">propriété booléenne [gérée](#handled)</span><span class="sxs-lookup"><span data-stu-id="6e197-127">public bool [Handled](#handled)</span></span>

<span data-ttu-id="6e197-128">S’il s’agit d’une valeur false et qu’aucune NewWindow n’est définie, le WebView ouvrira une fenêtre contextuelle et sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="6e197-128">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="6e197-129">Si elle a la valeur true et qu’aucune propriété NewWindow n’est définie pour un appel Window. Open, le WindowProxy ouvert sera destiné à un objet Window factice et aucune fenêtre ne sera chargée.</span><span class="sxs-lookup"><span data-stu-id="6e197-129">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="6e197-130">La valeur par défaut est false.</span><span class="sxs-lookup"><span data-stu-id="6e197-130">Default is false.</span></span>

#### <span data-ttu-id="6e197-131">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6e197-131">IsUserInitiated</span></span> 

<span data-ttu-id="6e197-132">IsUserInitiated a la valeur true lorsque la nouvelle demande de fenêtre a été lancée par le biais d’un mouvement utilisateur, par exemple en cliquant sur une balise d’ancrage avec target.</span><span class="sxs-lookup"><span data-stu-id="6e197-132">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="6e197-133">public bool [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="6e197-133">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="6e197-134">NewWindow</span><span class="sxs-lookup"><span data-stu-id="6e197-134">NewWindow</span></span> 

<span data-ttu-id="6e197-135">Obtient la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6e197-135">Gets the new window.</span></span>

> <span data-ttu-id="6e197-136">public CoreWebView2 [NewWindow](#newwindow)</span><span class="sxs-lookup"><span data-stu-id="6e197-136">public CoreWebView2 [NewWindow](#newwindow)</span></span>

#### <span data-ttu-id="6e197-137">URI</span><span class="sxs-lookup"><span data-stu-id="6e197-137">Uri</span></span> 

<span data-ttu-id="6e197-138">URI cible du NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="6e197-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="6e197-139">[URI](#uri) de chaîne publique</span><span class="sxs-lookup"><span data-stu-id="6e197-139">public string [Uri](#uri)</span></span>

<span data-ttu-id="6e197-140">Le WebView cible ne doit pas être parcouru.</span><span class="sxs-lookup"><span data-stu-id="6e197-140">The target webview should not be navigated.</span></span> <span data-ttu-id="6e197-141">Si l’NewWindow est définie, sa fenêtre de niveau supérieur sera renvoyée en tant que WindowProxy ouverte.</span><span class="sxs-lookup"><span data-stu-id="6e197-141">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="6e197-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6e197-142">GetDeferral</span></span> 

<span data-ttu-id="6e197-143">Obtenez un objet CoreWebView2Deferral et placez l’événement dans un État différé.</span><span class="sxs-lookup"><span data-stu-id="6e197-143">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="6e197-144">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="6e197-144">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="6e197-145">Vous pouvez utiliser l’objet CoreWebView2Deferral pour terminer la requête d’ouverture de fenêtre ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="6e197-145">You can use the CoreWebView2Deferral object to complete the window open request at a later time.</span></span> <span data-ttu-id="6e197-146">Même si cet événement est différé, la fenêtre d’ouverture sera renvoyée en tant que WindowProxy dans une fenêtre sans navigation, ce qui vous permettra de naviguer à l’issue du report.</span><span class="sxs-lookup"><span data-stu-id="6e197-146">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

