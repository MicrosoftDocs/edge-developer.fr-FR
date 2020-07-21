---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: d6d6f52456823488c07288c8ed07b9655a29883a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884436"
---
# <span data-ttu-id="6d2a0-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="6d2a0-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="6d2a0-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6d2a0-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6d2a0-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6d2a0-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6d2a0-107">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="6d2a0-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="6d2a0-108">Summary</span></span>

 <span data-ttu-id="6d2a0-109">Ses</span><span class="sxs-lookup"><span data-stu-id="6d2a0-109">Members</span></span>                        | <span data-ttu-id="6d2a0-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="6d2a0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6d2a0-111">Height</span><span class="sxs-lookup"><span data-stu-id="6d2a0-111">Height</span></span>](#height) | <span data-ttu-id="6d2a0-112">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-112">The height of the window.</span></span>
[<span data-ttu-id="6d2a0-113">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="6d2a0-113">Left</span></span>](#left) | <span data-ttu-id="6d2a0-114">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-114">The left position of the window.</span></span>
[<span data-ttu-id="6d2a0-115">MenuBar</span><span class="sxs-lookup"><span data-stu-id="6d2a0-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="6d2a0-116">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="6d2a0-117">Barres</span><span class="sxs-lookup"><span data-stu-id="6d2a0-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="6d2a0-118">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="6d2a0-119">Statut</span><span class="sxs-lookup"><span data-stu-id="6d2a0-119">Status</span></span>](#status) | <span data-ttu-id="6d2a0-120">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="6d2a0-121">ToolBar</span><span class="sxs-lookup"><span data-stu-id="6d2a0-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="6d2a0-122">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="6d2a0-123">Top</span><span class="sxs-lookup"><span data-stu-id="6d2a0-123">Top</span></span>](#top) | <span data-ttu-id="6d2a0-124">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-124">The top position of the window.</span></span>
[<span data-ttu-id="6d2a0-125">Largeur</span><span class="sxs-lookup"><span data-stu-id="6d2a0-125">Width</span></span>](#width) | <span data-ttu-id="6d2a0-126">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-126">The width of the window.</span></span>
[<span data-ttu-id="6d2a0-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="6d2a0-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="6d2a0-128">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-128">Has specified left and top values.</span></span>
[<span data-ttu-id="6d2a0-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="6d2a0-129">HasSize</span></span>](#hassize) | <span data-ttu-id="6d2a0-130">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-130">Has specified height and width values.</span></span>

## <span data-ttu-id="6d2a0-131">Ses</span><span class="sxs-lookup"><span data-stu-id="6d2a0-131">Members</span></span>

#### <span data-ttu-id="6d2a0-132">Height</span><span class="sxs-lookup"><span data-stu-id="6d2a0-132">Height</span></span> 

<span data-ttu-id="6d2a0-133">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-133">The height of the window.</span></span>

> <span data-ttu-id="6d2a0-134">[hauteur](#height) publique uint</span><span class="sxs-lookup"><span data-stu-id="6d2a0-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="6d2a0-135">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="6d2a0-135">Left</span></span> 

<span data-ttu-id="6d2a0-136">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-136">The left position of the window.</span></span>

> <span data-ttu-id="6d2a0-137">public uint vers la [gauche](#left)</span><span class="sxs-lookup"><span data-stu-id="6d2a0-137">public uint [Left](#left)</span></span>

<span data-ttu-id="6d2a0-138">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="6d2a0-139">MenuBar</span><span class="sxs-lookup"><span data-stu-id="6d2a0-139">MenuBar</span></span> 

<span data-ttu-id="6d2a0-140">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="6d2a0-141">Barre de [menus](#menubar) publique ent</span><span class="sxs-lookup"><span data-stu-id="6d2a0-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="6d2a0-142">Barres</span><span class="sxs-lookup"><span data-stu-id="6d2a0-142">ScrollBars</span></span> 

<span data-ttu-id="6d2a0-143">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="6d2a0-144">Barres de [défilement](#scrollbars) public ent</span><span class="sxs-lookup"><span data-stu-id="6d2a0-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="6d2a0-145">Statut</span><span class="sxs-lookup"><span data-stu-id="6d2a0-145">Status</span></span> 

<span data-ttu-id="6d2a0-146">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="6d2a0-147">[État](#status) d’ent public</span><span class="sxs-lookup"><span data-stu-id="6d2a0-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="6d2a0-148">ToolBar</span><span class="sxs-lookup"><span data-stu-id="6d2a0-148">Toolbar</span></span> 

<span data-ttu-id="6d2a0-149">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="6d2a0-150">[barre d’outils](#toolbar) public ent</span><span class="sxs-lookup"><span data-stu-id="6d2a0-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="6d2a0-151">Top</span><span class="sxs-lookup"><span data-stu-id="6d2a0-151">Top</span></span> 

<span data-ttu-id="6d2a0-152">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-152">The top position of the window.</span></span>

> <span data-ttu-id="6d2a0-153">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="6d2a0-153">public uint [Top](#top)</span></span>

<span data-ttu-id="6d2a0-154">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="6d2a0-155">Largeur</span><span class="sxs-lookup"><span data-stu-id="6d2a0-155">Width</span></span> 

<span data-ttu-id="6d2a0-156">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-156">The width of the window.</span></span>

> <span data-ttu-id="6d2a0-157">[largeur](#width) publique uint</span><span class="sxs-lookup"><span data-stu-id="6d2a0-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="6d2a0-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="6d2a0-158">HasPosition</span></span> 

<span data-ttu-id="6d2a0-159">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-159">Has specified left and top values.</span></span>

> <span data-ttu-id="6d2a0-160">public ent [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="6d2a0-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="6d2a0-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="6d2a0-161">HasSize</span></span> 

<span data-ttu-id="6d2a0-162">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="6d2a0-162">Has specified height and width values.</span></span>

> <span data-ttu-id="6d2a0-163">public ent [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="6d2a0-163">public int [HasSize](#hassize)()</span></span>

