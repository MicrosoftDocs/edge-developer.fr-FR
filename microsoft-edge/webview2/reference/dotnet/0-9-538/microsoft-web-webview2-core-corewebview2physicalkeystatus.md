---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 17ed4a578234a056a7e6ff347829a12e39fa93bd
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010921"
---
# <span data-ttu-id="431b6-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus struct</span><span class="sxs-lookup"><span data-stu-id="431b6-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="431b6-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="431b6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="431b6-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="431b6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="431b6-107">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="431b6-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="431b6-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="431b6-108">Summary</span></span>

 <span data-ttu-id="431b6-109">Ses</span><span class="sxs-lookup"><span data-stu-id="431b6-109">Members</span></span>                        | <span data-ttu-id="431b6-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="431b6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="431b6-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="431b6-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="431b6-112">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="431b6-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="431b6-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="431b6-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="431b6-114">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="431b6-114">The transition state.</span></span>
[<span data-ttu-id="431b6-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="431b6-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="431b6-116">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="431b6-116">The context code.</span></span>
[<span data-ttu-id="431b6-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="431b6-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="431b6-118">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="431b6-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="431b6-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="431b6-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="431b6-120">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="431b6-120">The scan code.</span></span>
[<span data-ttu-id="431b6-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="431b6-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="431b6-122">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="431b6-122">The previous key state.</span></span>

<span data-ttu-id="431b6-123">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="431b6-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="431b6-124">Ses</span><span class="sxs-lookup"><span data-stu-id="431b6-124">Members</span></span>

#### <span data-ttu-id="431b6-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="431b6-125">IsExtendedKey</span></span> 

<span data-ttu-id="431b6-126">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="431b6-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="431b6-127">public ent [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="431b6-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="431b6-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="431b6-128">IsKeyReleased</span></span> 

<span data-ttu-id="431b6-129">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="431b6-129">The transition state.</span></span>

> <span data-ttu-id="431b6-130">public ent [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="431b6-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="431b6-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="431b6-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="431b6-132">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="431b6-132">The context code.</span></span>

> <span data-ttu-id="431b6-133">public ent [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="431b6-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="431b6-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="431b6-134">RepeatCount</span></span> 

<span data-ttu-id="431b6-135">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="431b6-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="431b6-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="431b6-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="431b6-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="431b6-137">ScanCode</span></span> 

<span data-ttu-id="431b6-138">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="431b6-138">The scan code.</span></span>

> <span data-ttu-id="431b6-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="431b6-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="431b6-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="431b6-140">WasKeyDown</span></span> 

<span data-ttu-id="431b6-141">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="431b6-141">The previous key state.</span></span>

> <span data-ttu-id="431b6-142">public ent [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="431b6-142">public int [WasKeyDown](#waskeydown)</span></span>

