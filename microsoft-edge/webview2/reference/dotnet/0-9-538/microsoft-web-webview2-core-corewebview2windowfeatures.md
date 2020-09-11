---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 59e051c0537357fed89d6300db69ea479b656c7e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010515"
---
# <span data-ttu-id="504ec-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="504ec-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="504ec-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="504ec-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="504ec-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="504ec-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="504ec-107">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="504ec-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="504ec-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="504ec-108">Summary</span></span>

 <span data-ttu-id="504ec-109">Ses</span><span class="sxs-lookup"><span data-stu-id="504ec-109">Members</span></span>                        | <span data-ttu-id="504ec-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="504ec-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="504ec-111">Height</span><span class="sxs-lookup"><span data-stu-id="504ec-111">Height</span></span>](#height) | <span data-ttu-id="504ec-112">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-112">The height of the window.</span></span>
[<span data-ttu-id="504ec-113">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="504ec-113">Left</span></span>](#left) | <span data-ttu-id="504ec-114">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-114">The left position of the window.</span></span>
[<span data-ttu-id="504ec-115">MenuBar</span><span class="sxs-lookup"><span data-stu-id="504ec-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="504ec-116">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="504ec-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="504ec-117">Barres</span><span class="sxs-lookup"><span data-stu-id="504ec-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="504ec-118">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="504ec-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="504ec-119">Statut</span><span class="sxs-lookup"><span data-stu-id="504ec-119">Status</span></span>](#status) | <span data-ttu-id="504ec-120">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="504ec-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="504ec-121">ToolBar</span><span class="sxs-lookup"><span data-stu-id="504ec-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="504ec-122">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="504ec-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="504ec-123">Top</span><span class="sxs-lookup"><span data-stu-id="504ec-123">Top</span></span>](#top) | <span data-ttu-id="504ec-124">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-124">The top position of the window.</span></span>
[<span data-ttu-id="504ec-125">Largeur</span><span class="sxs-lookup"><span data-stu-id="504ec-125">Width</span></span>](#width) | <span data-ttu-id="504ec-126">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-126">The width of the window.</span></span>
[<span data-ttu-id="504ec-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="504ec-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="504ec-128">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="504ec-128">Has specified left and top values.</span></span>
[<span data-ttu-id="504ec-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="504ec-129">HasSize</span></span>](#hassize) | <span data-ttu-id="504ec-130">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="504ec-130">Has specified height and width values.</span></span>

## <span data-ttu-id="504ec-131">Ses</span><span class="sxs-lookup"><span data-stu-id="504ec-131">Members</span></span>

#### <span data-ttu-id="504ec-132">Height</span><span class="sxs-lookup"><span data-stu-id="504ec-132">Height</span></span> 

<span data-ttu-id="504ec-133">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-133">The height of the window.</span></span>

> <span data-ttu-id="504ec-134">[hauteur](#height) publique uint</span><span class="sxs-lookup"><span data-stu-id="504ec-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="504ec-135">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="504ec-135">Left</span></span> 

<span data-ttu-id="504ec-136">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-136">The left position of the window.</span></span>

> <span data-ttu-id="504ec-137">public uint vers la [gauche](#left)</span><span class="sxs-lookup"><span data-stu-id="504ec-137">public uint [Left](#left)</span></span>

<span data-ttu-id="504ec-138">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="504ec-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="504ec-139">MenuBar</span><span class="sxs-lookup"><span data-stu-id="504ec-139">MenuBar</span></span> 

<span data-ttu-id="504ec-140">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="504ec-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="504ec-141">Barre de [menus](#menubar) publique ent</span><span class="sxs-lookup"><span data-stu-id="504ec-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="504ec-142">Barres</span><span class="sxs-lookup"><span data-stu-id="504ec-142">ScrollBars</span></span> 

<span data-ttu-id="504ec-143">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="504ec-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="504ec-144">Barres de [défilement](#scrollbars) public ent</span><span class="sxs-lookup"><span data-stu-id="504ec-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="504ec-145">Statut</span><span class="sxs-lookup"><span data-stu-id="504ec-145">Status</span></span> 

<span data-ttu-id="504ec-146">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="504ec-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="504ec-147">[État](#status) d’ent public</span><span class="sxs-lookup"><span data-stu-id="504ec-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="504ec-148">ToolBar</span><span class="sxs-lookup"><span data-stu-id="504ec-148">Toolbar</span></span> 

<span data-ttu-id="504ec-149">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="504ec-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="504ec-150">[barre d’outils](#toolbar) public ent</span><span class="sxs-lookup"><span data-stu-id="504ec-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="504ec-151">Top</span><span class="sxs-lookup"><span data-stu-id="504ec-151">Top</span></span> 

<span data-ttu-id="504ec-152">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-152">The top position of the window.</span></span>

> <span data-ttu-id="504ec-153">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="504ec-153">public uint [Top](#top)</span></span>

<span data-ttu-id="504ec-154">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="504ec-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="504ec-155">Largeur</span><span class="sxs-lookup"><span data-stu-id="504ec-155">Width</span></span> 

<span data-ttu-id="504ec-156">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="504ec-156">The width of the window.</span></span>

> <span data-ttu-id="504ec-157">[largeur](#width) publique uint</span><span class="sxs-lookup"><span data-stu-id="504ec-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="504ec-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="504ec-158">HasPosition</span></span> 

<span data-ttu-id="504ec-159">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="504ec-159">Has specified left and top values.</span></span>

> <span data-ttu-id="504ec-160">public ent [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="504ec-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="504ec-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="504ec-161">HasSize</span></span> 

<span data-ttu-id="504ec-162">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="504ec-162">Has specified height and width values.</span></span>

> <span data-ttu-id="504ec-163">public ent [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="504ec-163">public int [HasSize](#hassize)()</span></span>

