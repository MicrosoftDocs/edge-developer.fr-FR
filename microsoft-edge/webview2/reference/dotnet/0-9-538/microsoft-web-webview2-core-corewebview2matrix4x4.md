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
ms.openlocfilehash: e8563bdd77972945a1e4b81662071d07d1efeb02
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698623"
---
# <span data-ttu-id="ac856-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4</span><span class="sxs-lookup"><span data-stu-id="ac856-104">Microsoft.Web.WebView2.Core.CoreWebView2Matrix4x4 struct</span></span> 

> [!NOTE]
> <span data-ttu-id="ac856-105">Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="ac856-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="ac856-106">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ac856-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ac856-107">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="ac856-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ac856-108">Cette transformation est utilisée pour calculer les coordonnées correctes lors de l’appel de CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="ac856-108">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span>

## <span data-ttu-id="ac856-109">Résumé</span><span class="sxs-lookup"><span data-stu-id="ac856-109">Summary</span></span>

 <span data-ttu-id="ac856-110">Ses</span><span class="sxs-lookup"><span data-stu-id="ac856-110">Members</span></span>                        | <span data-ttu-id="ac856-111">Descriptions</span><span class="sxs-lookup"><span data-stu-id="ac856-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac856-112">_11</span><span class="sxs-lookup"><span data-stu-id="ac856-112">_11</span></span>](#_11) | <span data-ttu-id="ac856-113">Valeur de la première ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-113">The value in the first row and first column of the matrix.</span></span>
[<span data-ttu-id="ac856-114">_12</span><span class="sxs-lookup"><span data-stu-id="ac856-114">_12</span></span>](#_12) | <span data-ttu-id="ac856-115">Valeur de la première ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-115">The value in the first row and second column of the matrix.</span></span>
[<span data-ttu-id="ac856-116">_13</span><span class="sxs-lookup"><span data-stu-id="ac856-116">_13</span></span>](#_13) | <span data-ttu-id="ac856-117">Valeur de la première ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-117">The value in the first row and third column of the matrix.</span></span>
[<span data-ttu-id="ac856-118">_14</span><span class="sxs-lookup"><span data-stu-id="ac856-118">_14</span></span>](#_14) | <span data-ttu-id="ac856-119">Valeur de la première ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-119">The value in the first row and fourth column of the matrix.</span></span>
[<span data-ttu-id="ac856-120">_21</span><span class="sxs-lookup"><span data-stu-id="ac856-120">_21</span></span>](#_21) | <span data-ttu-id="ac856-121">Valeur de la deuxième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-121">The value in the second row and first column of the matrix.</span></span>
[<span data-ttu-id="ac856-122">_22</span><span class="sxs-lookup"><span data-stu-id="ac856-122">_22</span></span>](#_22) | <span data-ttu-id="ac856-123">Valeur de la deuxième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-123">The value in the second row and second column of the matrix.</span></span>
[<span data-ttu-id="ac856-124">_23</span><span class="sxs-lookup"><span data-stu-id="ac856-124">_23</span></span>](#_23) | <span data-ttu-id="ac856-125">Valeur de la deuxième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-125">The value in the second row and third column of the matrix.</span></span>
[<span data-ttu-id="ac856-126">_24</span><span class="sxs-lookup"><span data-stu-id="ac856-126">_24</span></span>](#_24) | <span data-ttu-id="ac856-127">Valeur de la deuxième ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-127">The value in the second row and fourth column of the matrix.</span></span>
[<span data-ttu-id="ac856-128">_31</span><span class="sxs-lookup"><span data-stu-id="ac856-128">_31</span></span>](#_31) | <span data-ttu-id="ac856-129">Valeur de la troisième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-129">The value in the third row and first column of the matrix.</span></span>
[<span data-ttu-id="ac856-130">_32</span><span class="sxs-lookup"><span data-stu-id="ac856-130">_32</span></span>](#_32) | <span data-ttu-id="ac856-131">Valeur de la troisième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-131">The value in the third row and second column of the matrix.</span></span>
[<span data-ttu-id="ac856-132">_33</span><span class="sxs-lookup"><span data-stu-id="ac856-132">_33</span></span>](#_33) | <span data-ttu-id="ac856-133">Valeur de la troisième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-133">The value in the third row and third column of the matrix.</span></span>
[<span data-ttu-id="ac856-134">_34</span><span class="sxs-lookup"><span data-stu-id="ac856-134">_34</span></span>](#_34) | <span data-ttu-id="ac856-135">Valeur de la troisième ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-135">The value in the third row and fourth column of the matrix.</span></span>
[<span data-ttu-id="ac856-136">_41</span><span class="sxs-lookup"><span data-stu-id="ac856-136">_41</span></span>](#_41) | <span data-ttu-id="ac856-137">Valeur de la quatrième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-137">The value in the fourth row and first column of the matrix.</span></span>
[<span data-ttu-id="ac856-138">_42</span><span class="sxs-lookup"><span data-stu-id="ac856-138">_42</span></span>](#_42) | <span data-ttu-id="ac856-139">Valeur de la quatrième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-139">The value in the fourth row and second column of the matrix.</span></span>
[<span data-ttu-id="ac856-140">_43</span><span class="sxs-lookup"><span data-stu-id="ac856-140">_43</span></span>](#_43) | <span data-ttu-id="ac856-141">Valeur de la quatrième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-141">The value in the fourth row and third column of the matrix.</span></span>
[<span data-ttu-id="ac856-142">_44</span><span class="sxs-lookup"><span data-stu-id="ac856-142">_44</span></span>](#_44) | <span data-ttu-id="ac856-143">Valeur de la quatrième ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-143">The value in the fourth row and fourth column of the matrix.</span></span>

<span data-ttu-id="ac856-144">Ceci équivaut à une D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="ac856-144">This is equivalent to a D2D1_MATRIX_4X4_F.</span></span>

## <span data-ttu-id="ac856-145">Ses</span><span class="sxs-lookup"><span data-stu-id="ac856-145">Members</span></span>

#### <span data-ttu-id="ac856-146">_11</span><span class="sxs-lookup"><span data-stu-id="ac856-146">_11</span></span> 

<span data-ttu-id="ac856-147">Valeur de la première ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-147">The value in the first row and first column of the matrix.</span></span>

> <span data-ttu-id="ac856-148">[_11](#_11) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-148">public Single [_11](#_11)</span></span>

#### <span data-ttu-id="ac856-149">_12</span><span class="sxs-lookup"><span data-stu-id="ac856-149">_12</span></span> 

<span data-ttu-id="ac856-150">Valeur de la première ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-150">The value in the first row and second column of the matrix.</span></span>

> <span data-ttu-id="ac856-151">[_12](#_12) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-151">public Single [_12](#_12)</span></span>

#### <span data-ttu-id="ac856-152">_13</span><span class="sxs-lookup"><span data-stu-id="ac856-152">_13</span></span> 

<span data-ttu-id="ac856-153">Valeur de la première ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-153">The value in the first row and third column of the matrix.</span></span>

> <span data-ttu-id="ac856-154">[_13](#_13) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-154">public Single [_13](#_13)</span></span>

#### <span data-ttu-id="ac856-155">_14</span><span class="sxs-lookup"><span data-stu-id="ac856-155">_14</span></span> 

<span data-ttu-id="ac856-156">Valeur de la première ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-156">The value in the first row and fourth column of the matrix.</span></span>

> <span data-ttu-id="ac856-157">[_14](#_14) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-157">public Single [_14](#_14)</span></span>

#### <span data-ttu-id="ac856-158">_21</span><span class="sxs-lookup"><span data-stu-id="ac856-158">_21</span></span> 

<span data-ttu-id="ac856-159">Valeur de la deuxième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-159">The value in the second row and first column of the matrix.</span></span>

> <span data-ttu-id="ac856-160">[_21](#_21) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-160">public Single [_21](#_21)</span></span>

#### <span data-ttu-id="ac856-161">_22</span><span class="sxs-lookup"><span data-stu-id="ac856-161">_22</span></span> 

<span data-ttu-id="ac856-162">Valeur de la deuxième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-162">The value in the second row and second column of the matrix.</span></span>

> <span data-ttu-id="ac856-163">[_22](#_22) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-163">public Single [_22](#_22)</span></span>

#### <span data-ttu-id="ac856-164">_23</span><span class="sxs-lookup"><span data-stu-id="ac856-164">_23</span></span> 

<span data-ttu-id="ac856-165">Valeur de la deuxième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-165">The value in the second row and third column of the matrix.</span></span>

> <span data-ttu-id="ac856-166">[_23](#_23) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-166">public Single [_23](#_23)</span></span>

#### <span data-ttu-id="ac856-167">_24</span><span class="sxs-lookup"><span data-stu-id="ac856-167">_24</span></span> 

<span data-ttu-id="ac856-168">Valeur de la deuxième ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-168">The value in the second row and fourth column of the matrix.</span></span>

> <span data-ttu-id="ac856-169">[_24](#_24) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-169">public Single [_24](#_24)</span></span>

#### <span data-ttu-id="ac856-170">_31</span><span class="sxs-lookup"><span data-stu-id="ac856-170">_31</span></span> 

<span data-ttu-id="ac856-171">Valeur de la troisième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-171">The value in the third row and first column of the matrix.</span></span>

> <span data-ttu-id="ac856-172">[_31](#_31) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-172">public Single [_31](#_31)</span></span>

#### <span data-ttu-id="ac856-173">_32</span><span class="sxs-lookup"><span data-stu-id="ac856-173">_32</span></span> 

<span data-ttu-id="ac856-174">Valeur de la troisième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-174">The value in the third row and second column of the matrix.</span></span>

> <span data-ttu-id="ac856-175">[_32](#_32) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-175">public Single [_32](#_32)</span></span>

#### <span data-ttu-id="ac856-176">_33</span><span class="sxs-lookup"><span data-stu-id="ac856-176">_33</span></span> 

<span data-ttu-id="ac856-177">Valeur de la troisième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-177">The value in the third row and third column of the matrix.</span></span>

> <span data-ttu-id="ac856-178">[_33](#_33) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-178">public Single [_33](#_33)</span></span>

#### <span data-ttu-id="ac856-179">_34</span><span class="sxs-lookup"><span data-stu-id="ac856-179">_34</span></span> 

<span data-ttu-id="ac856-180">Valeur de la troisième ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-180">The value in the third row and fourth column of the matrix.</span></span>

> <span data-ttu-id="ac856-181">[_34](#_34) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-181">public Single [_34](#_34)</span></span>

#### <span data-ttu-id="ac856-182">_41</span><span class="sxs-lookup"><span data-stu-id="ac856-182">_41</span></span> 

<span data-ttu-id="ac856-183">Valeur de la quatrième ligne et de la première colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-183">The value in the fourth row and first column of the matrix.</span></span>

> <span data-ttu-id="ac856-184">[_41](#_41) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-184">public Single [_41](#_41)</span></span>

#### <span data-ttu-id="ac856-185">_42</span><span class="sxs-lookup"><span data-stu-id="ac856-185">_42</span></span> 

<span data-ttu-id="ac856-186">Valeur de la quatrième ligne et de la deuxième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-186">The value in the fourth row and second column of the matrix.</span></span>

> <span data-ttu-id="ac856-187">[_42](#_42) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-187">public Single [_42](#_42)</span></span>

#### <span data-ttu-id="ac856-188">_43</span><span class="sxs-lookup"><span data-stu-id="ac856-188">_43</span></span> 

<span data-ttu-id="ac856-189">Valeur de la quatrième ligne et de la troisième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-189">The value in the fourth row and third column of the matrix.</span></span>

> <span data-ttu-id="ac856-190">[_43](#_43) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-190">public Single [_43](#_43)</span></span>

#### <span data-ttu-id="ac856-191">_44</span><span class="sxs-lookup"><span data-stu-id="ac856-191">_44</span></span> 

<span data-ttu-id="ac856-192">Valeur de la quatrième ligne et de la quatrième colonne de la matrice.</span><span class="sxs-lookup"><span data-stu-id="ac856-192">The value in the fourth row and fourth column of the matrix.</span></span>

> <span data-ttu-id="ac856-193">[_44](#_44) public unique</span><span class="sxs-lookup"><span data-stu-id="ac856-193">public Single [_44](#_44)</span></span>

