---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 4866626111908eae9800da0baabec0356d5d4bf8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879652"
---
# <span data-ttu-id="06213-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="06213-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="06213-105">Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="06213-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="06213-106">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="06213-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="06213-107">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="06213-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="06213-108">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="06213-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="06213-109">Résumé</span><span class="sxs-lookup"><span data-stu-id="06213-109">Summary</span></span>

 <span data-ttu-id="06213-110">Ses</span><span class="sxs-lookup"><span data-stu-id="06213-110">Members</span></span>                        | <span data-ttu-id="06213-111">Descriptions</span><span class="sxs-lookup"><span data-stu-id="06213-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06213-112">Height</span><span class="sxs-lookup"><span data-stu-id="06213-112">Height</span></span>](#height) | <span data-ttu-id="06213-113">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-113">The height of the window.</span></span>
[<span data-ttu-id="06213-114">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="06213-114">Left</span></span>](#left) | <span data-ttu-id="06213-115">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-115">The left position of the window.</span></span>
[<span data-ttu-id="06213-116">MenuBar</span><span class="sxs-lookup"><span data-stu-id="06213-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="06213-117">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="06213-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="06213-118">Barres</span><span class="sxs-lookup"><span data-stu-id="06213-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="06213-119">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="06213-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="06213-120">Statut</span><span class="sxs-lookup"><span data-stu-id="06213-120">Status</span></span>](#status) | <span data-ttu-id="06213-121">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="06213-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="06213-122">ToolBar</span><span class="sxs-lookup"><span data-stu-id="06213-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="06213-123">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="06213-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="06213-124">Top</span><span class="sxs-lookup"><span data-stu-id="06213-124">Top</span></span>](#top) | <span data-ttu-id="06213-125">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-125">The top position of the window.</span></span>
[<span data-ttu-id="06213-126">Largeur</span><span class="sxs-lookup"><span data-stu-id="06213-126">Width</span></span>](#width) | <span data-ttu-id="06213-127">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-127">The width of the window.</span></span>
[<span data-ttu-id="06213-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="06213-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="06213-129">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="06213-129">Has specified left and top values.</span></span>
[<span data-ttu-id="06213-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="06213-130">HasSize</span></span>](#hassize) | <span data-ttu-id="06213-131">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="06213-131">Has specified height and width values.</span></span>

## <span data-ttu-id="06213-132">Ses</span><span class="sxs-lookup"><span data-stu-id="06213-132">Members</span></span>

#### <span data-ttu-id="06213-133">Height</span><span class="sxs-lookup"><span data-stu-id="06213-133">Height</span></span> 

<span data-ttu-id="06213-134">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-134">The height of the window.</span></span>

> <span data-ttu-id="06213-135">[hauteur](#height) publique uint</span><span class="sxs-lookup"><span data-stu-id="06213-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="06213-136">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="06213-136">Left</span></span> 

<span data-ttu-id="06213-137">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-137">The left position of the window.</span></span>

> <span data-ttu-id="06213-138">public uint vers la [gauche](#left)</span><span class="sxs-lookup"><span data-stu-id="06213-138">public uint [Left](#left)</span></span>

<span data-ttu-id="06213-139">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="06213-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="06213-140">MenuBar</span><span class="sxs-lookup"><span data-stu-id="06213-140">MenuBar</span></span> 

<span data-ttu-id="06213-141">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="06213-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="06213-142">Barre de [menus](#menubar) publique ent</span><span class="sxs-lookup"><span data-stu-id="06213-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="06213-143">Barres</span><span class="sxs-lookup"><span data-stu-id="06213-143">ScrollBars</span></span> 

<span data-ttu-id="06213-144">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="06213-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="06213-145">Barres de [défilement](#scrollbars) public ent</span><span class="sxs-lookup"><span data-stu-id="06213-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="06213-146">Statut</span><span class="sxs-lookup"><span data-stu-id="06213-146">Status</span></span> 

<span data-ttu-id="06213-147">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="06213-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="06213-148">[État](#status) d’ent public</span><span class="sxs-lookup"><span data-stu-id="06213-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="06213-149">ToolBar</span><span class="sxs-lookup"><span data-stu-id="06213-149">Toolbar</span></span> 

<span data-ttu-id="06213-150">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="06213-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="06213-151">[barre d’outils](#toolbar) public ent</span><span class="sxs-lookup"><span data-stu-id="06213-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="06213-152">Top</span><span class="sxs-lookup"><span data-stu-id="06213-152">Top</span></span> 

<span data-ttu-id="06213-153">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-153">The top position of the window.</span></span>

> <span data-ttu-id="06213-154">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="06213-154">public uint [Top](#top)</span></span>

<span data-ttu-id="06213-155">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="06213-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="06213-156">Largeur</span><span class="sxs-lookup"><span data-stu-id="06213-156">Width</span></span> 

<span data-ttu-id="06213-157">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="06213-157">The width of the window.</span></span>

> <span data-ttu-id="06213-158">[largeur](#width) publique uint</span><span class="sxs-lookup"><span data-stu-id="06213-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="06213-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="06213-159">HasPosition</span></span> 

<span data-ttu-id="06213-160">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="06213-160">Has specified left and top values.</span></span>

> <span data-ttu-id="06213-161">public ent [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="06213-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="06213-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="06213-162">HasSize</span></span> 

<span data-ttu-id="06213-163">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="06213-163">Has specified height and width values.</span></span>

> <span data-ttu-id="06213-164">public ent [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="06213-164">public int [HasSize](#hassize)()</span></span>

