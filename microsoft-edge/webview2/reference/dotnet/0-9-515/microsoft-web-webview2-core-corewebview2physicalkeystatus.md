---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: da7069fb4dad164720bb697a250a216a0bd452ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881199"
---
# <span data-ttu-id="e8a85-104">0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus struct</span><span class="sxs-lookup"><span data-stu-id="e8a85-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="e8a85-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e8a85-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e8a85-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="e8a85-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="e8a85-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e8a85-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e8a85-108">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e8a85-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e8a85-109">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="e8a85-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="e8a85-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="e8a85-110">Summary</span></span>

 <span data-ttu-id="e8a85-111">Ses</span><span class="sxs-lookup"><span data-stu-id="e8a85-111">Members</span></span>                        | <span data-ttu-id="e8a85-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="e8a85-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e8a85-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="e8a85-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="e8a85-114">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="e8a85-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="e8a85-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="e8a85-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="e8a85-116">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="e8a85-116">The transition state.</span></span>
[<span data-ttu-id="e8a85-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="e8a85-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="e8a85-118">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="e8a85-118">The context code.</span></span>
[<span data-ttu-id="e8a85-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="e8a85-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="e8a85-120">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="e8a85-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="e8a85-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="e8a85-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="e8a85-122">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="e8a85-122">The scan code.</span></span>
[<span data-ttu-id="e8a85-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="e8a85-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="e8a85-124">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="e8a85-124">The previous key state.</span></span>

<span data-ttu-id="e8a85-125">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="e8a85-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="e8a85-126">Ses</span><span class="sxs-lookup"><span data-stu-id="e8a85-126">Members</span></span>

#### <span data-ttu-id="e8a85-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="e8a85-127">IsExtendedKey</span></span> 

<span data-ttu-id="e8a85-128">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="e8a85-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="e8a85-129">public ent [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="e8a85-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="e8a85-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="e8a85-130">IsKeyReleased</span></span> 

<span data-ttu-id="e8a85-131">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="e8a85-131">The transition state.</span></span>

> <span data-ttu-id="e8a85-132">public ent [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="e8a85-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="e8a85-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="e8a85-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="e8a85-134">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="e8a85-134">The context code.</span></span>

> <span data-ttu-id="e8a85-135">public ent [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="e8a85-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="e8a85-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="e8a85-136">RepeatCount</span></span> 

<span data-ttu-id="e8a85-137">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="e8a85-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="e8a85-138">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="e8a85-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="e8a85-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="e8a85-139">ScanCode</span></span> 

<span data-ttu-id="e8a85-140">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="e8a85-140">The scan code.</span></span>

> <span data-ttu-id="e8a85-141">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="e8a85-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="e8a85-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="e8a85-142">WasKeyDown</span></span> 

<span data-ttu-id="e8a85-143">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="e8a85-143">The previous key state.</span></span>

> <span data-ttu-id="e8a85-144">public ent [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="e8a85-144">public int [WasKeyDown](#waskeydown)</span></span>

