---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 28ed6db251095e2baf6474950c6839dc4a5a8633
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653692"
---
# <span data-ttu-id="0874f-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="0874f-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="0874f-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0874f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0874f-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="0874f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0874f-107">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="0874f-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="0874f-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="0874f-108">Summary</span></span>

 <span data-ttu-id="0874f-109">Ses</span><span class="sxs-lookup"><span data-stu-id="0874f-109">Members</span></span>                        | <span data-ttu-id="0874f-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="0874f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0874f-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="0874f-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="0874f-112">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="0874f-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="0874f-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="0874f-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="0874f-114">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="0874f-114">The transition state.</span></span>
[<span data-ttu-id="0874f-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="0874f-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="0874f-116">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="0874f-116">The context code.</span></span>
[<span data-ttu-id="0874f-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="0874f-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="0874f-118">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="0874f-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="0874f-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="0874f-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="0874f-120">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="0874f-120">The scan code.</span></span>
[<span data-ttu-id="0874f-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="0874f-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="0874f-122">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="0874f-122">The previous key state.</span></span>

<span data-ttu-id="0874f-123">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="0874f-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="0874f-124">Ses</span><span class="sxs-lookup"><span data-stu-id="0874f-124">Members</span></span>

#### <span data-ttu-id="0874f-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="0874f-125">IsExtendedKey</span></span> 

<span data-ttu-id="0874f-126">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="0874f-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="0874f-127">public ent [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="0874f-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="0874f-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="0874f-128">IsKeyReleased</span></span> 

<span data-ttu-id="0874f-129">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="0874f-129">The transition state.</span></span>

> <span data-ttu-id="0874f-130">public ent [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="0874f-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="0874f-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="0874f-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="0874f-132">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="0874f-132">The context code.</span></span>

> <span data-ttu-id="0874f-133">public ent [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="0874f-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="0874f-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="0874f-134">RepeatCount</span></span> 

<span data-ttu-id="0874f-135">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="0874f-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="0874f-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="0874f-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="0874f-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="0874f-137">ScanCode</span></span> 

<span data-ttu-id="0874f-138">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="0874f-138">The scan code.</span></span>

> <span data-ttu-id="0874f-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="0874f-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="0874f-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="0874f-140">WasKeyDown</span></span> 

<span data-ttu-id="0874f-141">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="0874f-141">The previous key state.</span></span>

> <span data-ttu-id="0874f-142">public ent [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="0874f-142">public int [WasKeyDown](#waskeydown)</span></span>

