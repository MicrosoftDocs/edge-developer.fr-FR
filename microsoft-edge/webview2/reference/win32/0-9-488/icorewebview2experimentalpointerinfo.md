---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 2141dff54b44fe6d9a2758f571e61b81877079da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653487"
---
# <span data-ttu-id="4a87a-104">interface ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="4a87a-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="4a87a-105">Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="4a87a-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="4a87a-106">Il s’agit essentiellement d’un objet POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combiné.</span><span class="sxs-lookup"><span data-stu-id="4a87a-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="4a87a-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="4a87a-107">Summary</span></span>

 <span data-ttu-id="4a87a-108">Ses</span><span class="sxs-lookup"><span data-stu-id="4a87a-108">Members</span></span>                        | <span data-ttu-id="4a87a-109">Descriptions</span><span class="sxs-lookup"><span data-stu-id="4a87a-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4a87a-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="4a87a-111">Obtenez le ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="4a87a-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="4a87a-113">Obtenez le DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="4a87a-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="4a87a-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="4a87a-115">Obtenez le FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="4a87a-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="4a87a-117">Obtenez le HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="4a87a-119">Obtenez le HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="4a87a-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="4a87a-121">Obtenez le HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="4a87a-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="4a87a-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="4a87a-123">Obtenez le InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="4a87a-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="4a87a-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="4a87a-125">Obtenez les États de début de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="4a87a-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="4a87a-127">Obtenez le PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="4a87a-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="4a87a-129">Obtenez le PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="4a87a-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="4a87a-131">Obtenez le PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="4a87a-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="4a87a-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="4a87a-133">Obtenez le PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="4a87a-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="4a87a-135">Obtenez le PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="4a87a-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="4a87a-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="4a87a-137">Obtenez le PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="4a87a-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="4a87a-139">Obtenez le PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="4a87a-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="4a87a-141">Obtenez le PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="4a87a-143">Obtenez le PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="4a87a-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="4a87a-145">Obtenez le PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="4a87a-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="4a87a-147">Obtenez le PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="4a87a-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="4a87a-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="4a87a-149">Obtenez le PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="4a87a-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="4a87a-151">Obtenez le PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="4a87a-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="4a87a-152">get_Time</span></span>](#get_time) | <span data-ttu-id="4a87a-153">Obtenez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="4a87a-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="4a87a-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="4a87a-155">Obtenez le TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="4a87a-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="4a87a-157">Obtenez le TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="4a87a-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="4a87a-159">Obtenez le TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="4a87a-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="4a87a-161">Obtenez le TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="4a87a-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="4a87a-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="4a87a-163">Obtenez le TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="4a87a-165">Obtenez le TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="4a87a-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="4a87a-167">Définissez la ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="4a87a-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="4a87a-169">Définissez le DisplayRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="4a87a-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="4a87a-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="4a87a-171">Définissez la FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="4a87a-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="4a87a-173">Définissez la HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="4a87a-175">Définissez la HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="4a87a-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="4a87a-177">Définissez la HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="4a87a-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="4a87a-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="4a87a-179">Définissez la InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="4a87a-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="4a87a-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="4a87a-181">Définissez les KeyStates de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="4a87a-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="4a87a-183">Définissez la PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="4a87a-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="4a87a-185">Définissez la PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="4a87a-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="4a87a-187">Définissez la PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="4a87a-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="4a87a-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="4a87a-189">Définissez la PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="4a87a-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="4a87a-191">Définissez la PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="4a87a-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="4a87a-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="4a87a-193">Définissez la PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="4a87a-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="4a87a-195">Définissez la PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="4a87a-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="4a87a-197">Définissez la PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="4a87a-199">Définissez la PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="4a87a-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="4a87a-201">Définissez le PointerDeviceRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="4a87a-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="4a87a-203">Définissez la PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="4a87a-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="4a87a-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="4a87a-205">Définissez la PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="4a87a-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="4a87a-207">Définissez la PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="4a87a-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="4a87a-208">put_Time</span></span>](#put_time) | <span data-ttu-id="4a87a-209">Définissez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="4a87a-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="4a87a-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="4a87a-211">Définissez la TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="4a87a-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="4a87a-213">Définissez la TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="4a87a-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="4a87a-215">Définissez la TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="4a87a-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="4a87a-217">Définissez la TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="4a87a-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="4a87a-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="4a87a-219">Définissez la TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="4a87a-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="4a87a-221">Définissez la TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="4a87a-222">Il accepte les champs des trois et exclut certains types de données spécifiques Win32 comme HWND et descripteur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="4a87a-223">Notez que sourceDevice est pris en compte, mais que nous attendons que PointerDeviceRect et DisplayRect couvrent les cas d’utilisation existants de sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="4a87a-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="4a87a-224">Une autre différence majeure réside dans le fait que l’un ou l’autre emplacement est censé être présent dans les coordonnées physiques de WebView.</span><span class="sxs-lookup"><span data-stu-id="4a87a-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="4a87a-225">Il s’agit des coordonnées relatives à l’affichage WebView et à la mise à l’échelle DPI appliquée.</span><span class="sxs-lookup"><span data-stu-id="4a87a-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="4a87a-226">Ses</span><span class="sxs-lookup"><span data-stu-id="4a87a-226">Members</span></span>

#### <span data-ttu-id="4a87a-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="4a87a-228">Obtenez le ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="4a87a-229">[get_ButtonChangeKind](#get_buttonchangekind)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="4a87a-230">Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="4a87a-231">Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-232">get_DisplayRect</span></span> 

<span data-ttu-id="4a87a-233">Obtenez le DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="4a87a-234">valeur publique HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="4a87a-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="4a87a-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="4a87a-235">get_FrameId</span></span> 

<span data-ttu-id="4a87a-236">Obtenez le FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="4a87a-237">valeur publique HRESULT [get_FrameId](#get_frameid)(UInt32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="4a87a-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="4a87a-238">Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-239">get_HimetricLocation</span></span> 

<span data-ttu-id="4a87a-240">Obtenez le HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-241">valeur publique HRESULT [get_HimetricLocation](#get_himetriclocation)(point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="4a87a-242">Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="4a87a-244">Obtenez le HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="4a87a-245">valeur publique HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="4a87a-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="4a87a-246">Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-247">get_HistoryCount</span></span> 

<span data-ttu-id="4a87a-248">Obtenez le HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="4a87a-249">valeur publique HRESULT [get_HistoryCount](#get_historycount)(UInt32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="4a87a-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="4a87a-250">Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="4a87a-251">get_InputData</span></span> 

<span data-ttu-id="4a87a-252">Obtenez le InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="4a87a-253">[get_InputData](#get_inputdata)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="4a87a-254">Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="4a87a-255">get_KeyStates</span></span> 

<span data-ttu-id="4a87a-256">Obtenez les États de début de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="4a87a-257">valeur publique HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="4a87a-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="4a87a-258">Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-259">get_PenFlags</span></span> 

<span data-ttu-id="4a87a-260">Obtenez le PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="4a87a-261">valeur publique HRESULT [get_PenFlags](#get_penflags)(UInt32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="4a87a-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="4a87a-262">Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="4a87a-263">Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-264">get_PenMask</span></span> 

<span data-ttu-id="4a87a-265">Obtenez le PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="4a87a-266">valeur publique HRESULT [get_PenMask](#get_penmask)(UInt32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="4a87a-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="4a87a-267">Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="4a87a-268">Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-269">get_PenPressure</span></span> 

<span data-ttu-id="4a87a-270">Obtenez le PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="4a87a-271">valeur publique HRESULT [get_PenPressure](#get_penpressure)(UInt32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="4a87a-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="4a87a-272">Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="4a87a-273">get_PenRotation</span></span> 

<span data-ttu-id="4a87a-274">Obtenez le PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-275">valeur publique HRESULT [get_PenRotation](#get_penrotation)(UInt32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="4a87a-276">Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="4a87a-277">get_PenTiltX</span></span> 

<span data-ttu-id="4a87a-278">Obtenez le PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="4a87a-279">[get_PenTiltX](#get_pentiltx)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="4a87a-280">Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="4a87a-281">get_PenTiltY</span></span> 

<span data-ttu-id="4a87a-282">Obtenez le PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="4a87a-283">[get_PenTiltY](#get_pentilty)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="4a87a-284">Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-285">get_PerformanceCount</span></span> 

<span data-ttu-id="4a87a-286">Obtenez le PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="4a87a-287">[get_PerformanceCounts](#get_performancecount)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="4a87a-288">Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-289">get_PixelLocation</span></span> 

<span data-ttu-id="4a87a-290">Obtenez le PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-291">valeur publique HRESULT [get_PixelLocation](#get_pixellocation)(point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="4a87a-292">Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="4a87a-294">Obtenez le PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="4a87a-295">valeur publique HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="4a87a-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="4a87a-296">Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="4a87a-298">Obtenez le PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="4a87a-299">valeur publique HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="4a87a-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="4a87a-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-300">get_PointerFlags</span></span> 

<span data-ttu-id="4a87a-301">Obtenez le PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="4a87a-302">valeur publique HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="4a87a-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="4a87a-303">Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="4a87a-304">Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="4a87a-305">get_PointerId</span></span> 

<span data-ttu-id="4a87a-306">Obtenez le PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="4a87a-307">valeur publique HRESULT [get_PointerId](#get_pointerid)(UInt32 \* PointerId)</span><span class="sxs-lookup"><span data-stu-id="4a87a-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="4a87a-308">Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-309">get_PointerKind</span></span> 

<span data-ttu-id="4a87a-310">Obtenez le PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="4a87a-311">valeur publique HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="4a87a-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="4a87a-312">Cela correspond à la propriété pointerKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="4a87a-313">Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="4a87a-314">Prend en charge les PT_PEN et les PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="4a87a-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="4a87a-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="4a87a-315">get_Time</span></span> 

<span data-ttu-id="4a87a-316">Obtenez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="4a87a-317">valeur de HRESULT publique [get_Time](#get_time)(DWORD \* Time)</span><span class="sxs-lookup"><span data-stu-id="4a87a-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="4a87a-318">Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="4a87a-319">get_TouchContact</span></span> 

<span data-ttu-id="4a87a-320">Obtenez le TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="4a87a-321">valeur publique HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="4a87a-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="4a87a-322">Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="4a87a-324">Obtenez le TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="4a87a-325">valeur publique HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="4a87a-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="4a87a-326">Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-327">get_TouchFlags</span></span> 

<span data-ttu-id="4a87a-328">Obtenez le TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="4a87a-329">valeur publique HRESULT [get_TouchFlags](#get_touchflags)(UInt32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="4a87a-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="4a87a-330">Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="4a87a-331">Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-332">get_TouchMask</span></span> 

<span data-ttu-id="4a87a-333">Obtenez le TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="4a87a-334">valeur publique HRESULT [get_TouchMask](#get_touchmask)(UInt32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="4a87a-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="4a87a-335">Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="4a87a-336">Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="4a87a-337">get_TouchOrientation</span></span> 

<span data-ttu-id="4a87a-338">Obtenez le TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-339">valeur publique HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="4a87a-340">Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-341">get_TouchPressure</span></span> 

<span data-ttu-id="4a87a-342">Obtenez le TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="4a87a-343">valeur publique HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="4a87a-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="4a87a-344">Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="4a87a-346">Définissez la ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="4a87a-347">[put_ButtonChangeKind](#put_buttonchangekind)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="4a87a-348">Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="4a87a-349">Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-350">put_DisplayRect</span></span> 

<span data-ttu-id="4a87a-351">Définissez le DisplayRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="4a87a-352">valeur publique HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="4a87a-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="4a87a-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="4a87a-353">put_FrameId</span></span> 

<span data-ttu-id="4a87a-354">Définissez la FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="4a87a-355">[put_FrameIds](#put_frameid)HRESULT publiques (UInt32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="4a87a-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="4a87a-356">Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-357">put_HimetricLocation</span></span> 

<span data-ttu-id="4a87a-358">Définissez la HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-359">[put_HimetricLocation](#put_himetriclocation)par le biais du message public HRESULT (point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="4a87a-360">Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="4a87a-362">Définissez la HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="4a87a-363">[put_HimetricLocationRaw](#put_himetriclocationraw)par le biais du message public HRESULT (point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="4a87a-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="4a87a-364">Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-365">put_HistoryCount</span></span> 

<span data-ttu-id="4a87a-366">Définissez la HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="4a87a-367">[put_HistoryCounts](#put_historycount)HRESULT publiques (UInt32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="4a87a-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="4a87a-368">Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="4a87a-369">put_InputData</span></span> 

<span data-ttu-id="4a87a-370">Définissez la InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="4a87a-371">[put_InputData](#put_inputdata)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="4a87a-372">Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="4a87a-373">put_KeyStates</span></span> 

<span data-ttu-id="4a87a-374">Définissez les KeyStates de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="4a87a-375">[put_KeyStates](#put_keystates)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="4a87a-376">Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-377">put_PenFlags</span></span> 

<span data-ttu-id="4a87a-378">Définissez la PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="4a87a-379">[put_PenFlagss](#put_penflags)HRESULT publiques (UInt32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="4a87a-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="4a87a-380">Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="4a87a-381">Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-382">put_PenMask</span></span> 

<span data-ttu-id="4a87a-383">Définissez la PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="4a87a-384">[put_PenMasks](#put_penmask)HRESULT publiques (UInt32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="4a87a-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="4a87a-385">Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="4a87a-386">Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-387">put_PenPressure</span></span> 

<span data-ttu-id="4a87a-388">Définissez la PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="4a87a-389">[put_PenPressures](#put_penpressure)HRESULT publiques (UInt32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="4a87a-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="4a87a-390">Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="4a87a-391">put_PenRotation</span></span> 

<span data-ttu-id="4a87a-392">Définissez la PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-393">[put_PenRotations](#put_penrotation)HRESULT publiques (UInt32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="4a87a-394">Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="4a87a-395">put_PenTiltX</span></span> 

<span data-ttu-id="4a87a-396">Définissez la PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="4a87a-397">[put_PenTiltX](#put_pentiltx)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="4a87a-398">Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="4a87a-399">put_PenTiltY</span></span> 

<span data-ttu-id="4a87a-400">Définissez la PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="4a87a-401">[put_PenTiltY](#put_pentilty)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="4a87a-402">Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="4a87a-403">put_PerformanceCount</span></span> 

<span data-ttu-id="4a87a-404">Définissez la PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="4a87a-405">[put_PerformanceCount](#put_performancecount)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="4a87a-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="4a87a-406">Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="4a87a-407">put_PixelLocation</span></span> 

<span data-ttu-id="4a87a-408">Définissez la PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-409">[put_PixelLocation](#put_pixellocation)par le biais du message public HRESULT (point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="4a87a-410">Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="4a87a-412">Définissez la PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="4a87a-413">[put_PixelLocationRaw](#put_pixellocationraw)par le biais du message public HRESULT (point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="4a87a-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="4a87a-414">Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="4a87a-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="4a87a-416">Définissez le PointerDeviceRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="4a87a-417">valeur publique HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="4a87a-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="4a87a-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-418">put_PointerFlags</span></span> 

<span data-ttu-id="4a87a-419">Définissez la PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="4a87a-420">[put_PointerFlagss](#put_pointerflags)HRESULT publiques (UInt32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="4a87a-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="4a87a-421">Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="4a87a-422">Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="4a87a-423">put_PointerId</span></span> 

<span data-ttu-id="4a87a-424">Définissez la PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="4a87a-425">[put_PointerIds](#put_pointerid)HRESULT publiques (UInt32 PointerId)</span><span class="sxs-lookup"><span data-stu-id="4a87a-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="4a87a-426">Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="4a87a-427">put_PointerKind</span></span> 

<span data-ttu-id="4a87a-428">Définissez la PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="4a87a-429">[put_PointerKind](#put_pointerkind)par le biais du public HRESULT (DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="4a87a-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="4a87a-430">Cela correspond à la propriété pointerKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="4a87a-431">Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="4a87a-432">Prend en charge les PT_PEN et les PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="4a87a-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="4a87a-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="4a87a-433">put_Time</span></span> 

<span data-ttu-id="4a87a-434">Définissez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="4a87a-435">valeur de HRESULT publique [put_Time](#put_time)</span><span class="sxs-lookup"><span data-stu-id="4a87a-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="4a87a-436">Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="4a87a-437">put_TouchContact</span></span> 

<span data-ttu-id="4a87a-438">Définissez la TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="4a87a-439">valeur publique HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="4a87a-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="4a87a-440">Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="4a87a-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="4a87a-442">Définissez la TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="4a87a-443">valeur publique HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="4a87a-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="4a87a-444">Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="4a87a-445">put_TouchFlags</span></span> 

<span data-ttu-id="4a87a-446">Définissez la TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="4a87a-447">[put_TouchFlagss](#put_touchflags)HRESULT publiques (UInt32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="4a87a-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="4a87a-448">Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="4a87a-449">Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="4a87a-450">put_TouchMask</span></span> 

<span data-ttu-id="4a87a-451">Définissez la TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="4a87a-452">[put_TouchMasks](#put_touchmask)HRESULT publiques (UInt32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="4a87a-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="4a87a-453">Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="4a87a-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="4a87a-454">Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="4a87a-455">put_TouchOrientation</span></span> 

<span data-ttu-id="4a87a-456">Définissez la TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="4a87a-457">[put_TouchOrientations](#put_touchorientation)HRESULT publiques (UInt32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="4a87a-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="4a87a-458">Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="4a87a-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="4a87a-459">put_TouchPressure</span></span> 

<span data-ttu-id="4a87a-460">Définissez la TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="4a87a-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="4a87a-461">[put_TouchPressures](#put_touchpressure)HRESULT publiques (UInt32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="4a87a-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="4a87a-462">Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="4a87a-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

