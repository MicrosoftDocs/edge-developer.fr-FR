---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884588"
---
# <span data-ttu-id="4f746-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus struct</span><span class="sxs-lookup"><span data-stu-id="4f746-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="4f746-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4f746-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4f746-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="4f746-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4f746-107">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="4f746-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="4f746-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="4f746-108">Summary</span></span>

 <span data-ttu-id="4f746-109">Ses</span><span class="sxs-lookup"><span data-stu-id="4f746-109">Members</span></span>                        | <span data-ttu-id="4f746-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4f746-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4f746-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="4f746-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="4f746-112">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="4f746-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="4f746-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="4f746-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="4f746-114">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="4f746-114">The transition state.</span></span>
[<span data-ttu-id="4f746-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="4f746-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="4f746-116">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="4f746-116">The context code.</span></span>
[<span data-ttu-id="4f746-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="4f746-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="4f746-118">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="4f746-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="4f746-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="4f746-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="4f746-120">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="4f746-120">The scan code.</span></span>
[<span data-ttu-id="4f746-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="4f746-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="4f746-122">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="4f746-122">The previous key state.</span></span>

<span data-ttu-id="4f746-123">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="4f746-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="4f746-124">Ses</span><span class="sxs-lookup"><span data-stu-id="4f746-124">Members</span></span>

#### <span data-ttu-id="4f746-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="4f746-125">IsExtendedKey</span></span> 

<span data-ttu-id="4f746-126">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="4f746-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="4f746-127">public ent [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="4f746-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="4f746-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="4f746-128">IsKeyReleased</span></span> 

<span data-ttu-id="4f746-129">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="4f746-129">The transition state.</span></span>

> <span data-ttu-id="4f746-130">public ent [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="4f746-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="4f746-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="4f746-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="4f746-132">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="4f746-132">The context code.</span></span>

> <span data-ttu-id="4f746-133">public ent [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="4f746-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="4f746-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="4f746-134">RepeatCount</span></span> 

<span data-ttu-id="4f746-135">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="4f746-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="4f746-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="4f746-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="4f746-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="4f746-137">ScanCode</span></span> 

<span data-ttu-id="4f746-138">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="4f746-138">The scan code.</span></span>

> <span data-ttu-id="4f746-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="4f746-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="4f746-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="4f746-140">WasKeyDown</span></span> 

<span data-ttu-id="4f746-141">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="4f746-141">The previous key state.</span></span>

> <span data-ttu-id="4f746-142">public ent [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="4f746-142">public int [WasKeyDown](#waskeydown)</span></span>

