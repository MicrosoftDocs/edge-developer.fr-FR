---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, Core, WebView2, WebView, dotnet, WPF, WinForms, application, Edge, CoreWebView2, CoreWebView2Controller, contrôle de navigateur, Edge html, Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
ms.openlocfilehash: 9ce4c9c3f076d54f03295ffda84c5fb0f03b4166
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010900"
---
# <span data-ttu-id="85f7e-104">0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="85f7e-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="85f7e-105">Espace de noms: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="85f7e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="85f7e-106">Assemblage: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="85f7e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="85f7e-107">Il s’agit essentiellement d’un objet POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combiné.</span><span class="sxs-lookup"><span data-stu-id="85f7e-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="85f7e-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="85f7e-108">Summary</span></span>

 <span data-ttu-id="85f7e-109">Ses</span><span class="sxs-lookup"><span data-stu-id="85f7e-109">Members</span></span>                        | <span data-ttu-id="85f7e-110">Descriptions</span><span class="sxs-lookup"><span data-stu-id="85f7e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="85f7e-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="85f7e-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="85f7e-112">ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="85f7e-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="85f7e-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="85f7e-114">DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="85f7e-115">FrameId</span><span class="sxs-lookup"><span data-stu-id="85f7e-115">FrameId</span></span>](#frameid) | <span data-ttu-id="85f7e-116">FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="85f7e-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="85f7e-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="85f7e-118">HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="85f7e-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="85f7e-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="85f7e-120">HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="85f7e-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="85f7e-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="85f7e-122">HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="85f7e-123">InputData</span><span class="sxs-lookup"><span data-stu-id="85f7e-123">InputData</span></span>](#inputdata) | <span data-ttu-id="85f7e-124">InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="85f7e-125">État</span><span class="sxs-lookup"><span data-stu-id="85f7e-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="85f7e-126">Les inversions de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="85f7e-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="85f7e-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="85f7e-128">PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="85f7e-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="85f7e-129">PenMask</span></span>](#penmask) | <span data-ttu-id="85f7e-130">PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="85f7e-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="85f7e-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="85f7e-132">PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="85f7e-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="85f7e-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="85f7e-134">PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="85f7e-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="85f7e-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="85f7e-136">PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="85f7e-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="85f7e-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="85f7e-138">PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="85f7e-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="85f7e-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="85f7e-140">PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="85f7e-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="85f7e-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="85f7e-142">PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="85f7e-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="85f7e-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="85f7e-144">PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="85f7e-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="85f7e-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="85f7e-146">PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="85f7e-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="85f7e-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="85f7e-148">PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="85f7e-149">PointerId</span><span class="sxs-lookup"><span data-stu-id="85f7e-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="85f7e-150">PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="85f7e-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="85f7e-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="85f7e-152">PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="85f7e-153">Heure</span><span class="sxs-lookup"><span data-stu-id="85f7e-153">Time</span></span>](#time) | <span data-ttu-id="85f7e-154">Heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="85f7e-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="85f7e-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="85f7e-156">TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="85f7e-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="85f7e-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="85f7e-158">TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="85f7e-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="85f7e-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="85f7e-160">TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="85f7e-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="85f7e-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="85f7e-162">TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="85f7e-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="85f7e-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="85f7e-164">TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="85f7e-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="85f7e-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="85f7e-166">TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="85f7e-167">Ses</span><span class="sxs-lookup"><span data-stu-id="85f7e-167">Members</span></span>

#### <span data-ttu-id="85f7e-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="85f7e-168">ButtonChangeKind</span></span> 

<span data-ttu-id="85f7e-169">ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="85f7e-170">public ent [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="85f7e-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="85f7e-171">Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="85f7e-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="85f7e-172">Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="85f7e-173">DisplayRect</span></span> 

<span data-ttu-id="85f7e-174">DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="85f7e-175">public Rect [DisplayRect](#displayrect)</span><span class="sxs-lookup"><span data-stu-id="85f7e-175">public Rect [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="85f7e-176">FrameId</span><span class="sxs-lookup"><span data-stu-id="85f7e-176">FrameId</span></span> 

<span data-ttu-id="85f7e-177">FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="85f7e-178">public uint [FrameId](#frameid)</span><span class="sxs-lookup"><span data-stu-id="85f7e-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="85f7e-179">Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="85f7e-180">HimetricLocation</span></span> 

<span data-ttu-id="85f7e-181">HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="85f7e-182">Point public [HimetricLocation](#himetriclocation)</span><span class="sxs-lookup"><span data-stu-id="85f7e-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="85f7e-183">Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="85f7e-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="85f7e-185">HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="85f7e-186">Point public [HimetricLocationRaw](#himetriclocationraw)</span><span class="sxs-lookup"><span data-stu-id="85f7e-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="85f7e-187">Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="85f7e-188">HistoryCount</span></span> 

<span data-ttu-id="85f7e-189">HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="85f7e-190">public uint [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="85f7e-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="85f7e-191">Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-192">InputData</span><span class="sxs-lookup"><span data-stu-id="85f7e-192">InputData</span></span> 

<span data-ttu-id="85f7e-193">InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="85f7e-194">public ent [InputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="85f7e-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="85f7e-195">Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-196">État</span><span class="sxs-lookup"><span data-stu-id="85f7e-196">KeyStates</span></span> 

<span data-ttu-id="85f7e-197">Les inversions de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="85f7e-198">[KeyStates](#keystates) public uint</span><span class="sxs-lookup"><span data-stu-id="85f7e-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="85f7e-199">Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="85f7e-200">PenFlags</span></span> 

<span data-ttu-id="85f7e-201">PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="85f7e-202">public uint [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="85f7e-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="85f7e-203">Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="85f7e-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="85f7e-204">Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="85f7e-205">PenMask</span></span> 

<span data-ttu-id="85f7e-206">PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="85f7e-207">public uint [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="85f7e-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="85f7e-208">Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="85f7e-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="85f7e-209">Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="85f7e-210">PenPressure</span></span> 

<span data-ttu-id="85f7e-211">PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="85f7e-212">public uint [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="85f7e-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="85f7e-213">Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="85f7e-214">PenRotation</span></span> 

<span data-ttu-id="85f7e-215">PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="85f7e-216">public uint [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="85f7e-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="85f7e-217">Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="85f7e-218">PenTiltX</span></span> 

<span data-ttu-id="85f7e-219">PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="85f7e-220">public ent [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="85f7e-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="85f7e-221">Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="85f7e-222">PenTiltY</span></span> 

<span data-ttu-id="85f7e-223">PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="85f7e-224">public ent [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="85f7e-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="85f7e-225">Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="85f7e-226">PerformanceCount</span></span> 

<span data-ttu-id="85f7e-227">PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="85f7e-228">public ulong [PerformanceCount](#performancecount)</span><span class="sxs-lookup"><span data-stu-id="85f7e-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="85f7e-229">Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="85f7e-230">PixelLocation</span></span> 

<span data-ttu-id="85f7e-231">PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="85f7e-232">Point public [PixelLocation](#pixellocation)</span><span class="sxs-lookup"><span data-stu-id="85f7e-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="85f7e-233">Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="85f7e-234">PixelLocationRaw</span></span> 

<span data-ttu-id="85f7e-235">PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="85f7e-236">Point public [PixelLocationRaw](#pixellocationraw)</span><span class="sxs-lookup"><span data-stu-id="85f7e-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="85f7e-237">Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="85f7e-238">PointerDeviceRect</span></span> 

<span data-ttu-id="85f7e-239">PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="85f7e-240">public Rect [PointerDeviceRect](#pointerdevicerect)</span><span class="sxs-lookup"><span data-stu-id="85f7e-240">public Rect [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="85f7e-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="85f7e-241">PointerFlags</span></span> 

<span data-ttu-id="85f7e-242">PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="85f7e-243">public uint [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="85f7e-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="85f7e-244">Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="85f7e-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="85f7e-245">Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-246">PointerId</span><span class="sxs-lookup"><span data-stu-id="85f7e-246">PointerId</span></span> 

<span data-ttu-id="85f7e-247">PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="85f7e-248">public uint [PointerId](#pointerid)</span><span class="sxs-lookup"><span data-stu-id="85f7e-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="85f7e-249">Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="85f7e-250">PointerKind</span></span> 

<span data-ttu-id="85f7e-251">PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="85f7e-252">public uint [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="85f7e-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="85f7e-253">Cela correspond à la propriété pointerKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="85f7e-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="85f7e-254">Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="85f7e-255">Prend en charge les PT_PEN et les PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="85f7e-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="85f7e-256">Heure</span><span class="sxs-lookup"><span data-stu-id="85f7e-256">Time</span></span> 

<span data-ttu-id="85f7e-257">Heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="85f7e-258">[heure](#time) du public</span><span class="sxs-lookup"><span data-stu-id="85f7e-258">public uint [Time](#time)</span></span>

<span data-ttu-id="85f7e-259">Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="85f7e-260">TouchContact</span></span> 

<span data-ttu-id="85f7e-261">TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="85f7e-262">public Rect [TouchContact](#touchcontact)</span><span class="sxs-lookup"><span data-stu-id="85f7e-262">public Rect [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="85f7e-263">Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="85f7e-264">TouchContactRaw</span></span> 

<span data-ttu-id="85f7e-265">TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="85f7e-266">public Rect [TouchContactRaw](#touchcontactraw)</span><span class="sxs-lookup"><span data-stu-id="85f7e-266">public Rect [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="85f7e-267">Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="85f7e-268">TouchFlags</span></span> 

<span data-ttu-id="85f7e-269">TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="85f7e-270">public uint [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="85f7e-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="85f7e-271">Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="85f7e-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="85f7e-272">Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="85f7e-273">TouchMask</span></span> 

<span data-ttu-id="85f7e-274">TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="85f7e-275">public uint [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="85f7e-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="85f7e-276">Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="85f7e-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="85f7e-277">Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="85f7e-278">TouchOrientation</span></span> 

<span data-ttu-id="85f7e-279">TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="85f7e-280">public uint [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="85f7e-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="85f7e-281">Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="85f7e-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="85f7e-282">TouchPressure</span></span> 

<span data-ttu-id="85f7e-283">TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="85f7e-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="85f7e-284">public uint [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="85f7e-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="85f7e-285">Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="85f7e-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

