---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878770"
---
# <span data-ttu-id="b9424-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="b9424-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="b9424-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b9424-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b9424-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b9424-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b9424-107">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="b9424-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="b9424-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b9424-108">Summary</span></span>

 <span data-ttu-id="b9424-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b9424-109">Members</span></span>                        | <span data-ttu-id="b9424-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b9424-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9424-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b9424-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="b9424-112">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="b9424-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="b9424-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b9424-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="b9424-114">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="b9424-114">The transition state.</span></span>
[<span data-ttu-id="b9424-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b9424-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="b9424-116">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="b9424-116">The context code.</span></span>
[<span data-ttu-id="b9424-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b9424-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="b9424-118">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="b9424-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="b9424-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b9424-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="b9424-120">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="b9424-120">The scan code.</span></span>
[<span data-ttu-id="b9424-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b9424-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="b9424-122">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="b9424-122">The previous key state.</span></span>

<span data-ttu-id="b9424-123">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="b9424-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="b9424-124">Ses</span><span class="sxs-lookup"><span data-stu-id="b9424-124">Members</span></span>

#### <span data-ttu-id="b9424-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b9424-125">IsExtendedKey</span></span> 

<span data-ttu-id="b9424-126">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="b9424-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="b9424-127">public ent [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="b9424-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="b9424-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b9424-128">IsKeyReleased</span></span> 

<span data-ttu-id="b9424-129">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="b9424-129">The transition state.</span></span>

> <span data-ttu-id="b9424-130">public ent [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="b9424-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="b9424-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b9424-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="b9424-132">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="b9424-132">The context code.</span></span>

> <span data-ttu-id="b9424-133">public ent [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="b9424-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="b9424-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b9424-134">RepeatCount</span></span> 

<span data-ttu-id="b9424-135">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="b9424-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="b9424-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="b9424-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="b9424-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b9424-137">ScanCode</span></span> 

<span data-ttu-id="b9424-138">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="b9424-138">The scan code.</span></span>

> <span data-ttu-id="b9424-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="b9424-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="b9424-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b9424-140">WasKeyDown</span></span> 

<span data-ttu-id="b9424-141">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="b9424-141">The previous key state.</span></span>

> <span data-ttu-id="b9424-142">public ent [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="b9424-142">public int [WasKeyDown](#waskeydown)</span></span>

