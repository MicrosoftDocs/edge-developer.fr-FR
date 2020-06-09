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
ms.openlocfilehash: bd63bda6b7835ff5edb30b8b1b22f877f4c96e14
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697594"
---
# <span data-ttu-id="3de05-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="3de05-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="3de05-105">Cette référence peut être modifiée ou indisponible pour les versions ultérieures au SDK version 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3de05-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3de05-106">Reportez-vous à la rubrique [référence d’API WebView2](../../../webview2-api-reference.md) pour obtenir les dernières références d’API.</span><span class="sxs-lookup"><span data-stu-id="3de05-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="3de05-107">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3de05-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3de05-108">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="3de05-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3de05-109">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="3de05-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="3de05-110">Résumé</span><span class="sxs-lookup"><span data-stu-id="3de05-110">Summary</span></span>

 <span data-ttu-id="3de05-111">Ses</span><span class="sxs-lookup"><span data-stu-id="3de05-111">Members</span></span>                        | <span data-ttu-id="3de05-112">Descriptions</span><span class="sxs-lookup"><span data-stu-id="3de05-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3de05-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="3de05-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="3de05-114">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="3de05-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="3de05-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="3de05-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="3de05-116">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="3de05-116">The transition state.</span></span>
[<span data-ttu-id="3de05-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="3de05-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="3de05-118">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="3de05-118">The context code.</span></span>
[<span data-ttu-id="3de05-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="3de05-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="3de05-120">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="3de05-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="3de05-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="3de05-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="3de05-122">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="3de05-122">The scan code.</span></span>
[<span data-ttu-id="3de05-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="3de05-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="3de05-124">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="3de05-124">The previous key state.</span></span>

<span data-ttu-id="3de05-125">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="3de05-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="3de05-126">Ses</span><span class="sxs-lookup"><span data-stu-id="3de05-126">Members</span></span>

#### <span data-ttu-id="3de05-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="3de05-127">IsExtendedKey</span></span> 

<span data-ttu-id="3de05-128">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="3de05-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="3de05-129">public ent [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="3de05-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="3de05-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="3de05-130">IsKeyReleased</span></span> 

<span data-ttu-id="3de05-131">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="3de05-131">The transition state.</span></span>

> <span data-ttu-id="3de05-132">public ent [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="3de05-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="3de05-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="3de05-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="3de05-134">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="3de05-134">The context code.</span></span>

> <span data-ttu-id="3de05-135">public ent [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="3de05-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="3de05-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="3de05-136">RepeatCount</span></span> 

<span data-ttu-id="3de05-137">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="3de05-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="3de05-138">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="3de05-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="3de05-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="3de05-139">ScanCode</span></span> 

<span data-ttu-id="3de05-140">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="3de05-140">The scan code.</span></span>

> <span data-ttu-id="3de05-141">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="3de05-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="3de05-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="3de05-142">WasKeyDown</span></span> 

<span data-ttu-id="3de05-143">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="3de05-143">The previous key state.</span></span>

> <span data-ttu-id="3de05-144">public ent [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="3de05-144">public int [WasKeyDown](#waskeydown)</span></span>

