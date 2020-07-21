---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: 2672f2aac842fd475f6148c439dbecdacd7793ee
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885402"
---
# <span data-ttu-id="7d603-104">interface ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="7d603-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="7d603-105">Fonctionnalités de fenêtre pour une fenêtre contextuelle WebView.</span><span class="sxs-lookup"><span data-stu-id="7d603-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="7d603-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="7d603-106">Summary</span></span>

 <span data-ttu-id="7d603-107">Ses</span><span class="sxs-lookup"><span data-stu-id="7d603-107">Members</span></span>                        | <span data-ttu-id="7d603-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="7d603-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7d603-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="7d603-109">get_Height</span></span>](#get_height) | <span data-ttu-id="7d603-110">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-110">The height of the window.</span></span>
[<span data-ttu-id="7d603-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="7d603-111">get_Left</span></span>](#get_left) | <span data-ttu-id="7d603-112">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-112">The left position of the window.</span></span> <span data-ttu-id="7d603-113">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="7d603-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="7d603-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="7d603-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="7d603-115">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="7d603-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="7d603-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="7d603-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="7d603-117">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="7d603-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="7d603-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="7d603-118">get_Status</span></span>](#get_status) | <span data-ttu-id="7d603-119">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="7d603-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="7d603-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="7d603-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="7d603-121">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="7d603-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="7d603-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="7d603-122">get_Top</span></span>](#get_top) | <span data-ttu-id="7d603-123">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-123">The top position of the window.</span></span> <span data-ttu-id="7d603-124">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="7d603-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="7d603-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="7d603-125">get_Width</span></span>](#get_width) | <span data-ttu-id="7d603-126">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-126">The width of the window.</span></span>
[<span data-ttu-id="7d603-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="7d603-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="7d603-128">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="7d603-128">Has specified left and top values.</span></span>
[<span data-ttu-id="7d603-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="7d603-129">HasSize</span></span>](#hassize) | <span data-ttu-id="7d603-130">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="7d603-130">Has specified height and width values.</span></span>

<span data-ttu-id="7d603-131">Ces champs correspondent à la valeur «windowFeatures» transmise à Window. ouvrir comme spécifié dans[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="7d603-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="7d603-132">Ses</span><span class="sxs-lookup"><span data-stu-id="7d603-132">Members</span></span>

#### <span data-ttu-id="7d603-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="7d603-133">get_Height</span></span> 

<span data-ttu-id="7d603-134">Hauteur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-134">The height of the window.</span></span>

> <span data-ttu-id="7d603-135">valeur de HRESULT publique [get_Height](#get_height)(UInt32 \* Height)</span><span class="sxs-lookup"><span data-stu-id="7d603-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="7d603-136">La valeur minimale est 100.</span><span class="sxs-lookup"><span data-stu-id="7d603-136">Minimum value is 100.</span></span> <span data-ttu-id="7d603-137">Va échouer si HasSize est faux.</span><span class="sxs-lookup"><span data-stu-id="7d603-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="7d603-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="7d603-138">get_Left</span></span> 

<span data-ttu-id="7d603-139">Position gauche de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-139">The left position of the window.</span></span> <span data-ttu-id="7d603-140">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="7d603-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="7d603-141">valeur publique HRESULT [get_Left](#get_left)(UInt32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="7d603-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="7d603-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="7d603-142">get_MenuBar</span></span> 

<span data-ttu-id="7d603-143">Si vous souhaitez afficher la barre de menus.</span><span class="sxs-lookup"><span data-stu-id="7d603-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="7d603-144">[get_MenuBars](#get_menubar)par valeur HRESULT publiques (bool \* BarreMenus)</span><span class="sxs-lookup"><span data-stu-id="7d603-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="7d603-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="7d603-145">get_ScrollBars</span></span> 

<span data-ttu-id="7d603-146">Si les barres de défilement s’affichent ou non.</span><span class="sxs-lookup"><span data-stu-id="7d603-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="7d603-147">[get_ScrollBars](#get_scrollbars)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="7d603-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="7d603-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="7d603-148">get_Status</span></span> 

<span data-ttu-id="7d603-149">Si vous souhaitez ou non ajouter une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="7d603-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="7d603-150">valeur publique HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="7d603-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="7d603-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="7d603-151">get_Toolbar</span></span> 

<span data-ttu-id="7d603-152">Affichage de la barre d’outils du navigateur.</span><span class="sxs-lookup"><span data-stu-id="7d603-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="7d603-153">[get_Toolbars](#get_toolbar)par valeur de passe publiques (bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="7d603-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="7d603-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="7d603-154">get_Top</span></span> 

<span data-ttu-id="7d603-155">La position supérieure de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-155">The top position of the window.</span></span> <span data-ttu-id="7d603-156">Va échouer si HasPosition est faux.</span><span class="sxs-lookup"><span data-stu-id="7d603-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="7d603-157">valeur publique HRESULT [get_Top](#get_top)(UInt32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="7d603-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="7d603-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="7d603-158">get_Width</span></span> 

<span data-ttu-id="7d603-159">La largeur de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="7d603-159">The width of the window.</span></span>

> <span data-ttu-id="7d603-160">[get_Width](#get_width)des valeurs HRESULT publiques (UInt32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="7d603-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="7d603-161">La valeur minimale est 100.</span><span class="sxs-lookup"><span data-stu-id="7d603-161">Minimum value is 100.</span></span> <span data-ttu-id="7d603-162">Va échouer si HasSize est faux.</span><span class="sxs-lookup"><span data-stu-id="7d603-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="7d603-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="7d603-163">HasPosition</span></span> 

<span data-ttu-id="7d603-164">A spécifié les valeurs Left et Top.</span><span class="sxs-lookup"><span data-stu-id="7d603-164">Has specified left and top values.</span></span>

> <span data-ttu-id="7d603-165">public HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="7d603-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="7d603-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="7d603-166">HasSize</span></span> 

<span data-ttu-id="7d603-167">A spécifié des valeurs de hauteur et de largeur.</span><span class="sxs-lookup"><span data-stu-id="7d603-167">Has specified height and width values.</span></span>

> <span data-ttu-id="7d603-168">public HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="7d603-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

