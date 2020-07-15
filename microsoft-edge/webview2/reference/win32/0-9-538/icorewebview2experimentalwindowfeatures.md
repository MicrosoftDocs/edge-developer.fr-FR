---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: 8b56d16e9c78738e9aa61e8c4c5b841b7fe4932f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879904"
---
# <span data-ttu-id="e257e-104">interface ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="e257e-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="e257e-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="e257e-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="e257e-106">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="e257e-106">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="e257e-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="e257e-107">Summary</span></span>

 <span data-ttu-id="e257e-108">Ses</span><span class="sxs-lookup"><span data-stu-id="e257e-108">Members</span></span>                        | <span data-ttu-id="e257e-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e257e-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e257e-110">get_Height</span><span class="sxs-lookup"><span data-stu-id="e257e-110">get_Height</span></span>](#get_height) | <span data-ttu-id="e257e-111">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-111">The height of the window.</span></span>
[<span data-ttu-id="e257e-112">get_Left</span><span class="sxs-lookup"><span data-stu-id="e257e-112">get_Left</span></span>](#get_left) | <span data-ttu-id="e257e-113">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-113">The left position of the window.</span></span> <span data-ttu-id="e257e-114">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="e257e-114">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="e257e-115">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="e257e-115">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="e257e-116">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="e257e-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="e257e-117">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="e257e-117">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="e257e-118">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="e257e-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="e257e-119">get_Status</span><span class="sxs-lookup"><span data-stu-id="e257e-119">get_Status</span></span>](#get_status) | <span data-ttu-id="e257e-120">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="e257e-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="e257e-121">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="e257e-121">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="e257e-122">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="e257e-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="e257e-123">get_Top</span><span class="sxs-lookup"><span data-stu-id="e257e-123">get_Top</span></span>](#get_top) | <span data-ttu-id="e257e-124">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-124">The top position of the window.</span></span> <span data-ttu-id="e257e-125">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="e257e-125">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="e257e-126">get_Width</span><span class="sxs-lookup"><span data-stu-id="e257e-126">get_Width</span></span>](#get_width) | <span data-ttu-id="e257e-127">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-127">The width of the window.</span></span>
[<span data-ttu-id="e257e-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="e257e-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="e257e-129">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="e257e-129">Has specified left and top values.</span></span>
[<span data-ttu-id="e257e-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="e257e-130">HasSize</span></span>](#hassize) | <span data-ttu-id="e257e-131">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="e257e-131">Has specified height and width values.</span></span>

<span data-ttu-id="e257e-132">Ces champs correspondent à la valeur «windowFeatures» transmise à Window. ouvrir comme spécifié dans[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="e257e-132">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="e257e-133">Ses</span><span class="sxs-lookup"><span data-stu-id="e257e-133">Members</span></span>

#### <span data-ttu-id="e257e-134">get_Height</span><span class="sxs-lookup"><span data-stu-id="e257e-134">get_Height</span></span> 

<span data-ttu-id="e257e-135">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-135">The height of the window.</span></span>

> <span data-ttu-id="e257e-136">valeur de HRESULT publique [get_Height](#get_height)(UInt32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="e257e-136">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="e257e-137">La valeur minimale est 100.</span><span class="sxs-lookup"><span data-stu-id="e257e-137">Minimum value is 100.</span></span> <span data-ttu-id="e257e-138">Va échouer si HasSize est faux.</span><span class="sxs-lookup"><span data-stu-id="e257e-138">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="e257e-139">get_Left</span><span class="sxs-lookup"><span data-stu-id="e257e-139">get_Left</span></span> 

<span data-ttu-id="e257e-140">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-140">The left position of the window.</span></span> <span data-ttu-id="e257e-141">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="e257e-141">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="e257e-142">valeur publique HRESULT [get_Left](#get_left)(UInt32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="e257e-142">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="e257e-143">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="e257e-143">get_MenuBar</span></span> 

<span data-ttu-id="e257e-144">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="e257e-144">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="e257e-145">[get_MenuBars](#get_menubar)par valeur HRESULT publiques (bool \* BarreMenus)</span><span class="sxs-lookup"><span data-stu-id="e257e-145">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="e257e-146">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="e257e-146">get_ScrollBars</span></span> 

<span data-ttu-id="e257e-147">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="e257e-147">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="e257e-148">[get_ScrollBars](#get_scrollbars)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="e257e-148">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="e257e-149">get_Status</span><span class="sxs-lookup"><span data-stu-id="e257e-149">get_Status</span></span> 

<span data-ttu-id="e257e-150">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="e257e-150">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="e257e-151">valeur publique HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="e257e-151">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="e257e-152">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="e257e-152">get_Toolbar</span></span> 

<span data-ttu-id="e257e-153">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="e257e-153">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="e257e-154">[get_Toolbars](#get_toolbar)par valeur de passe publiques (bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="e257e-154">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="e257e-155">get_Top</span><span class="sxs-lookup"><span data-stu-id="e257e-155">get_Top</span></span> 

<span data-ttu-id="e257e-156">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-156">The top position of the window.</span></span> <span data-ttu-id="e257e-157">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="e257e-157">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="e257e-158">valeur publique HRESULT [get_Top](#get_top)(UInt32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="e257e-158">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="e257e-159">get_Width</span><span class="sxs-lookup"><span data-stu-id="e257e-159">get_Width</span></span> 

<span data-ttu-id="e257e-160">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="e257e-160">The width of the window.</span></span>

> <span data-ttu-id="e257e-161">[get_Width](#get_width)des valeurs HRESULT publiques (UInt32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="e257e-161">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="e257e-162">La valeur minimale est 100.</span><span class="sxs-lookup"><span data-stu-id="e257e-162">Minimum value is 100.</span></span> <span data-ttu-id="e257e-163">Va échouer si HasSize est faux.</span><span class="sxs-lookup"><span data-stu-id="e257e-163">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="e257e-164">HasPosition</span><span class="sxs-lookup"><span data-stu-id="e257e-164">HasPosition</span></span> 

<span data-ttu-id="e257e-165">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="e257e-165">Has specified left and top values.</span></span>

> <span data-ttu-id="e257e-166">public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="e257e-166">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="e257e-167">HasSize</span><span class="sxs-lookup"><span data-stu-id="e257e-167">HasSize</span></span> 

<span data-ttu-id="e257e-168">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="e257e-168">Has specified height and width values.</span></span>

> <span data-ttu-id="e257e-169">public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="e257e-169">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

