---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
ms.openlocfilehash: 41ae506965067b478c3cb588eed0c8029704c4a3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011843"
---
# <span data-ttu-id="59116-104">Classe Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="59116-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

<span data-ttu-id="59116-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="59116-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="59116-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="59116-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="59116-107">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="59116-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="59116-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="59116-108">Summary</span></span>

 <span data-ttu-id="59116-109">Ses</span><span class="sxs-lookup"><span data-stu-id="59116-109">Members</span></span>                        | <span data-ttu-id="59116-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="59116-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="59116-111">Height</span><span class="sxs-lookup"><span data-stu-id="59116-111">Height</span></span>](#height) | <span data-ttu-id="59116-112">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-112">The height of the window.</span></span>
[<span data-ttu-id="59116-113">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="59116-113">Left</span></span>](#left) | <span data-ttu-id="59116-114">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-114">The left position of the window.</span></span>
[<span data-ttu-id="59116-115">MenuBar</span><span class="sxs-lookup"><span data-stu-id="59116-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="59116-116">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="59116-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="59116-117">Barres</span><span class="sxs-lookup"><span data-stu-id="59116-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="59116-118">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="59116-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="59116-119">Statut</span><span class="sxs-lookup"><span data-stu-id="59116-119">Status</span></span>](#status) | <span data-ttu-id="59116-120">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="59116-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="59116-121">ToolBar</span><span class="sxs-lookup"><span data-stu-id="59116-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="59116-122">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="59116-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="59116-123">Top</span><span class="sxs-lookup"><span data-stu-id="59116-123">Top</span></span>](#top) | <span data-ttu-id="59116-124">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-124">The top position of the window.</span></span>
[<span data-ttu-id="59116-125">Largeur</span><span class="sxs-lookup"><span data-stu-id="59116-125">Width</span></span>](#width) | <span data-ttu-id="59116-126">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-126">The width of the window.</span></span>
[<span data-ttu-id="59116-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="59116-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="59116-128">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="59116-128">Has specified left and top values.</span></span>
[<span data-ttu-id="59116-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="59116-129">HasSize</span></span>](#hassize) | <span data-ttu-id="59116-130">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="59116-130">Has specified height and width values.</span></span>

## <span data-ttu-id="59116-131">Ses</span><span class="sxs-lookup"><span data-stu-id="59116-131">Members</span></span>

#### <span data-ttu-id="59116-132">Height</span><span class="sxs-lookup"><span data-stu-id="59116-132">Height</span></span> 

<span data-ttu-id="59116-133">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-133">The height of the window.</span></span>

> <span data-ttu-id="59116-134">[hauteur](#height) publique uint</span><span class="sxs-lookup"><span data-stu-id="59116-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="59116-135">Vers la gauche</span><span class="sxs-lookup"><span data-stu-id="59116-135">Left</span></span> 

<span data-ttu-id="59116-136">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-136">The left position of the window.</span></span>

> <span data-ttu-id="59116-137">public uint vers la [gauche](#left)</span><span class="sxs-lookup"><span data-stu-id="59116-137">public uint [Left](#left)</span></span>

<span data-ttu-id="59116-138">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="59116-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="59116-139">MenuBar</span><span class="sxs-lookup"><span data-stu-id="59116-139">MenuBar</span></span> 

<span data-ttu-id="59116-140">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="59116-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="59116-141">Barre de [menus](#menubar) publique ent</span><span class="sxs-lookup"><span data-stu-id="59116-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="59116-142">Barres</span><span class="sxs-lookup"><span data-stu-id="59116-142">ScrollBars</span></span> 

<span data-ttu-id="59116-143">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="59116-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="59116-144">Barres de [défilement](#scrollbars) public ent</span><span class="sxs-lookup"><span data-stu-id="59116-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="59116-145">Statut</span><span class="sxs-lookup"><span data-stu-id="59116-145">Status</span></span> 

<span data-ttu-id="59116-146">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="59116-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="59116-147">[État](#status) d’ent public</span><span class="sxs-lookup"><span data-stu-id="59116-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="59116-148">ToolBar</span><span class="sxs-lookup"><span data-stu-id="59116-148">Toolbar</span></span> 

<span data-ttu-id="59116-149">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="59116-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="59116-150">[barre d’outils](#toolbar) public ent</span><span class="sxs-lookup"><span data-stu-id="59116-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="59116-151">Top</span><span class="sxs-lookup"><span data-stu-id="59116-151">Top</span></span> 

<span data-ttu-id="59116-152">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-152">The top position of the window.</span></span>

> <span data-ttu-id="59116-153">public uint [Top](#top)</span><span class="sxs-lookup"><span data-stu-id="59116-153">public uint [Top](#top)</span></span>

<span data-ttu-id="59116-154">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="59116-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="59116-155">Largeur</span><span class="sxs-lookup"><span data-stu-id="59116-155">Width</span></span> 

<span data-ttu-id="59116-156">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="59116-156">The width of the window.</span></span>

> <span data-ttu-id="59116-157">[largeur](#width) publique uint</span><span class="sxs-lookup"><span data-stu-id="59116-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="59116-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="59116-158">HasPosition</span></span> 

<span data-ttu-id="59116-159">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="59116-159">Has specified left and top values.</span></span>

> <span data-ttu-id="59116-160">public ent [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="59116-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="59116-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="59116-161">HasSize</span></span> 

<span data-ttu-id="59116-162">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="59116-162">Has specified height and width values.</span></span>

> <span data-ttu-id="59116-163">public ent [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="59116-163">public int [HasSize](#hassize)()</span></span>

