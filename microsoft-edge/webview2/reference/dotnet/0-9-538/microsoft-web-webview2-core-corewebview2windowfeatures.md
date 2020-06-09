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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698736"
---
# <span data-ttu-id="462a5-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="462a5-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="462a5-105">Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="462a5-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="462a5-106">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="462a5-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="462a5-107">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="462a5-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="462a5-108">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="462a5-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="462a5-109">Résumé</span><span class="sxs-lookup"><span data-stu-id="462a5-109">Summary</span></span>

 <span data-ttu-id="462a5-110">Ses</span><span class="sxs-lookup"><span data-stu-id="462a5-110">Members</span></span>                        | <span data-ttu-id="462a5-111">Descriptions</span><span class="sxs-lookup"><span data-stu-id="462a5-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="462a5-112">Height</span><span class="sxs-lookup"><span data-stu-id="462a5-112">Height</span></span>](#height) | <span data-ttu-id="462a5-113">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-113">The height of the window.</span></span>
[<span data-ttu-id="462a5-114">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="462a5-114">Left</span></span>](#left) | <span data-ttu-id="462a5-115">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-115">The left position of the window.</span></span>
[<span data-ttu-id="462a5-116">MenuBar</span><span class="sxs-lookup"><span data-stu-id="462a5-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="462a5-117">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="462a5-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="462a5-118">Barres</span><span class="sxs-lookup"><span data-stu-id="462a5-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="462a5-119">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="462a5-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="462a5-120">Statut</span><span class="sxs-lookup"><span data-stu-id="462a5-120">Status</span></span>](#status) | <span data-ttu-id="462a5-121">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="462a5-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="462a5-122">ToolBar</span><span class="sxs-lookup"><span data-stu-id="462a5-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="462a5-123">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="462a5-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="462a5-124">Top</span><span class="sxs-lookup"><span data-stu-id="462a5-124">Top</span></span>](#top) | <span data-ttu-id="462a5-125">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-125">The top position of the window.</span></span>
[<span data-ttu-id="462a5-126">Largeur</span><span class="sxs-lookup"><span data-stu-id="462a5-126">Width</span></span>](#width) | <span data-ttu-id="462a5-127">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-127">The width of the window.</span></span>
[<span data-ttu-id="462a5-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="462a5-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="462a5-129">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="462a5-129">Has specified left and top values.</span></span>
[<span data-ttu-id="462a5-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="462a5-130">HasSize</span></span>](#hassize) | <span data-ttu-id="462a5-131">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="462a5-131">Has specified height and width values.</span></span>

## <span data-ttu-id="462a5-132">Ses</span><span class="sxs-lookup"><span data-stu-id="462a5-132">Members</span></span>

#### <span data-ttu-id="462a5-133">Height</span><span class="sxs-lookup"><span data-stu-id="462a5-133">Height</span></span> 

<span data-ttu-id="462a5-134">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-134">The height of the window.</span></span>

> <span data-ttu-id="462a5-135">[hauteur](#height) publique uint</span><span class="sxs-lookup"><span data-stu-id="462a5-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="462a5-136">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="462a5-136">Left</span></span> 

<span data-ttu-id="462a5-137">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-137">The left position of the window.</span></span>

> <span data-ttu-id="462a5-138">public uint vers la [gauche](#left)</span><span class="sxs-lookup"><span data-stu-id="462a5-138">public uint [Left](#left)</span></span>

<span data-ttu-id="462a5-139">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="462a5-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="462a5-140">MenuBar</span><span class="sxs-lookup"><span data-stu-id="462a5-140">MenuBar</span></span> 

<span data-ttu-id="462a5-141">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="462a5-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="462a5-142">Barre de [menus](#menubar) publique ent</span><span class="sxs-lookup"><span data-stu-id="462a5-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="462a5-143">Barres</span><span class="sxs-lookup"><span data-stu-id="462a5-143">ScrollBars</span></span> 

<span data-ttu-id="462a5-144">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="462a5-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="462a5-145">Barres de [défilement](#scrollbars) public ent</span><span class="sxs-lookup"><span data-stu-id="462a5-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="462a5-146">Statut</span><span class="sxs-lookup"><span data-stu-id="462a5-146">Status</span></span> 

<span data-ttu-id="462a5-147">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="462a5-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="462a5-148">[État](#status) d’ent public</span><span class="sxs-lookup"><span data-stu-id="462a5-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="462a5-149">ToolBar</span><span class="sxs-lookup"><span data-stu-id="462a5-149">Toolbar</span></span> 

<span data-ttu-id="462a5-150">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="462a5-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="462a5-151">[barre d’outils](#toolbar) public ent</span><span class="sxs-lookup"><span data-stu-id="462a5-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="462a5-152">Top</span><span class="sxs-lookup"><span data-stu-id="462a5-152">Top</span></span> 

<span data-ttu-id="462a5-153">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-153">The top position of the window.</span></span>

> <span data-ttu-id="462a5-154">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="462a5-154">public uint [Top](#top)</span></span>

<span data-ttu-id="462a5-155">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="462a5-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="462a5-156">Largeur</span><span class="sxs-lookup"><span data-stu-id="462a5-156">Width</span></span> 

<span data-ttu-id="462a5-157">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="462a5-157">The width of the window.</span></span>

> <span data-ttu-id="462a5-158">[largeur](#width) publique uint</span><span class="sxs-lookup"><span data-stu-id="462a5-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="462a5-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="462a5-159">HasPosition</span></span> 

<span data-ttu-id="462a5-160">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="462a5-160">Has specified left and top values.</span></span>

> <span data-ttu-id="462a5-161">public ent [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="462a5-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="462a5-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="462a5-162">HasSize</span></span> 

<span data-ttu-id="462a5-163">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="462a5-163">Has specified height and width values.</span></span>

> <span data-ttu-id="462a5-164">public ent [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="462a5-164">public int [HasSize](#hassize)()</span></span>

