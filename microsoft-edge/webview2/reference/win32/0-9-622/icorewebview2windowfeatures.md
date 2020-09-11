---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2WindowFeatures
ms.openlocfilehash: 90b5a09a752250dc342e7eefad031c9b5b83d345
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011925"
---
# <span data-ttu-id="f3d64-104">interface ICoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="f3d64-104">interface ICoreWebView2WindowFeatures</span></span> 

```
interface ICoreWebView2WindowFeatures
  : public IUnknown
```

<span data-ttu-id="f3d64-105">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="f3d64-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="f3d64-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="f3d64-106">Summary</span></span>

 <span data-ttu-id="f3d64-107">Ses</span><span class="sxs-lookup"><span data-stu-id="f3d64-107">Members</span></span>                        | <span data-ttu-id="f3d64-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="f3d64-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f3d64-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="f3d64-109">get_Height</span></span>](#get_height) | <span data-ttu-id="f3d64-110">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-110">The height of the window.</span></span>
[<span data-ttu-id="f3d64-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="f3d64-111">get_Left</span></span>](#get_left) | <span data-ttu-id="f3d64-112">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-112">The left position of the window.</span></span> <span data-ttu-id="f3d64-113">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="f3d64-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="f3d64-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="f3d64-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="f3d64-115">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="f3d64-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="f3d64-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="f3d64-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="f3d64-117">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="f3d64-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="f3d64-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="f3d64-118">get_Status</span></span>](#get_status) | <span data-ttu-id="f3d64-119">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="f3d64-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="f3d64-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="f3d64-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="f3d64-121">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="f3d64-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="f3d64-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="f3d64-122">get_Top</span></span>](#get_top) | <span data-ttu-id="f3d64-123">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-123">The top position of the window.</span></span> <span data-ttu-id="f3d64-124">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="f3d64-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="f3d64-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="f3d64-125">get_Width</span></span>](#get_width) | <span data-ttu-id="f3d64-126">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-126">The width of the window.</span></span>
[<span data-ttu-id="f3d64-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="f3d64-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="f3d64-128">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="f3d64-128">Has specified left and top values.</span></span>
[<span data-ttu-id="f3d64-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="f3d64-129">HasSize</span></span>](#hassize) | <span data-ttu-id="f3d64-130">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="f3d64-130">Has specified height and width values.</span></span>

<span data-ttu-id="f3d64-131">Ces champs correspondent à la valeur «windowFeatures» transmise à Window. ouvrir comme spécifié dans [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="f3d64-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="f3d64-132">Ses</span><span class="sxs-lookup"><span data-stu-id="f3d64-132">Members</span></span>

#### <span data-ttu-id="f3d64-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="f3d64-133">get_Height</span></span> 

<span data-ttu-id="f3d64-134">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-134">The height of the window.</span></span>

> <span data-ttu-id="f3d64-135">valeur de HRESULT publique [get_Height](#get_height)(UInt32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="f3d64-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="f3d64-136">La valeur minimale est 100.</span><span class="sxs-lookup"><span data-stu-id="f3d64-136">Minimum value is 100.</span></span> <span data-ttu-id="f3d64-137">Va échouer si HasSize est faux.</span><span class="sxs-lookup"><span data-stu-id="f3d64-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="f3d64-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="f3d64-138">get_Left</span></span> 

<span data-ttu-id="f3d64-139">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-139">The left position of the window.</span></span> <span data-ttu-id="f3d64-140">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="f3d64-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="f3d64-141">valeur publique HRESULT [get_Left](#get_left)(UInt32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="f3d64-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="f3d64-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="f3d64-142">get_MenuBar</span></span> 

<span data-ttu-id="f3d64-143">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="f3d64-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="f3d64-144">[get_MenuBars](#get_menubar)par valeur HRESULT publiques (bool \* BarreMenus)</span><span class="sxs-lookup"><span data-stu-id="f3d64-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="f3d64-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="f3d64-145">get_ScrollBars</span></span> 

<span data-ttu-id="f3d64-146">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="f3d64-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="f3d64-147">[get_ScrollBars](#get_scrollbars)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="f3d64-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="f3d64-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="f3d64-148">get_Status</span></span> 

<span data-ttu-id="f3d64-149">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="f3d64-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="f3d64-150">valeur publique HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="f3d64-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="f3d64-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="f3d64-151">get_Toolbar</span></span> 

<span data-ttu-id="f3d64-152">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="f3d64-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="f3d64-153">[get_Toolbars](#get_toolbar)par valeur de passe publiques (bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="f3d64-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="f3d64-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="f3d64-154">get_Top</span></span> 

<span data-ttu-id="f3d64-155">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-155">The top position of the window.</span></span> <span data-ttu-id="f3d64-156">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="f3d64-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="f3d64-157">valeur publique HRESULT [get_Top](#get_top)(UInt32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="f3d64-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="f3d64-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="f3d64-158">get_Width</span></span> 

<span data-ttu-id="f3d64-159">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="f3d64-159">The width of the window.</span></span>

> <span data-ttu-id="f3d64-160">[get_Width](#get_width)des valeurs HRESULT publiques (UInt32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="f3d64-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="f3d64-161">La valeur minimale est 100.</span><span class="sxs-lookup"><span data-stu-id="f3d64-161">Minimum value is 100.</span></span> <span data-ttu-id="f3d64-162">Va échouer si HasSize est faux.</span><span class="sxs-lookup"><span data-stu-id="f3d64-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="f3d64-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="f3d64-163">HasPosition</span></span> 

<span data-ttu-id="f3d64-164">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="f3d64-164">Has specified left and top values.</span></span>

> <span data-ttu-id="f3d64-165">public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="f3d64-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="f3d64-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="f3d64-166">HasSize</span></span> 

<span data-ttu-id="f3d64-167">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="f3d64-167">Has specified height and width values.</span></span>

> <span data-ttu-id="f3d64-168">public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="f3d64-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

