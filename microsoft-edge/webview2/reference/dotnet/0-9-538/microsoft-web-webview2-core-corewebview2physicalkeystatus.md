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
ms.openlocfilehash: e0fb3f9ff7114b0c4f2a42893adabfd72e9616de
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698596"
---
# <span data-ttu-id="b3bad-104">Struct Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="b3bad-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="b3bad-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b3bad-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b3bad-106">Assembly: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="b3bad-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b3bad-107">Structure représentant les informations contenues dans le LPARAM fourni à un événement de touche Win32.</span><span class="sxs-lookup"><span data-stu-id="b3bad-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="b3bad-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="b3bad-108">Summary</span></span>

 <span data-ttu-id="b3bad-109">Ses</span><span class="sxs-lookup"><span data-stu-id="b3bad-109">Members</span></span>                        | <span data-ttu-id="b3bad-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="b3bad-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3bad-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b3bad-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="b3bad-112">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="b3bad-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="b3bad-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b3bad-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="b3bad-114">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="b3bad-114">The transition state.</span></span>
[<span data-ttu-id="b3bad-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b3bad-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="b3bad-116">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="b3bad-116">The context code.</span></span>
[<span data-ttu-id="b3bad-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b3bad-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="b3bad-118">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="b3bad-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="b3bad-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b3bad-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="b3bad-120">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="b3bad-120">The scan code.</span></span>
[<span data-ttu-id="b3bad-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b3bad-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="b3bad-122">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="b3bad-122">The previous key state.</span></span>

<span data-ttu-id="b3bad-123">Pour plus d’informations, consultez la documentation de WM_KEYDOWN [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="b3bad-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="b3bad-124">Ses</span><span class="sxs-lookup"><span data-stu-id="b3bad-124">Members</span></span>

#### <span data-ttu-id="b3bad-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b3bad-125">IsExtendedKey</span></span> 

<span data-ttu-id="b3bad-126">Indique s’il s’agit d’une touche étendue.</span><span class="sxs-lookup"><span data-stu-id="b3bad-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="b3bad-127">public ent [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="b3bad-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="b3bad-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b3bad-128">IsKeyReleased</span></span> 

<span data-ttu-id="b3bad-129">État de la transition.</span><span class="sxs-lookup"><span data-stu-id="b3bad-129">The transition state.</span></span>

> <span data-ttu-id="b3bad-130">public ent [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="b3bad-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="b3bad-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b3bad-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="b3bad-132">Le code de contexte.</span><span class="sxs-lookup"><span data-stu-id="b3bad-132">The context code.</span></span>

> <span data-ttu-id="b3bad-133">public ent [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="b3bad-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="b3bad-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b3bad-134">RepeatCount</span></span> 

<span data-ttu-id="b3bad-135">Nombre répété pour le message actuel.</span><span class="sxs-lookup"><span data-stu-id="b3bad-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="b3bad-136">public uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="b3bad-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="b3bad-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b3bad-137">ScanCode</span></span> 

<span data-ttu-id="b3bad-138">Le code de numérisation.</span><span class="sxs-lookup"><span data-stu-id="b3bad-138">The scan code.</span></span>

> <span data-ttu-id="b3bad-139">public uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="b3bad-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="b3bad-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b3bad-140">WasKeyDown</span></span> 

<span data-ttu-id="b3bad-141">État de la clé précédente.</span><span class="sxs-lookup"><span data-stu-id="b3bad-141">The previous key state.</span></span>

> <span data-ttu-id="b3bad-142">public ent [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="b3bad-142">public int [WasKeyDown](#waskeydown)</span></span>

