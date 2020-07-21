---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.515-WebView2 C++ Win32 ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 8c0ed40c61344fe0a3177fd36d5629953f8801d7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885484"
---
# <span data-ttu-id="9b05c-104">0.9.515-interface ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="9b05c-104">0.9.515 - interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="9b05c-105">Il s’agit essentiellement d’un objet POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combiné.</span><span class="sxs-lookup"><span data-stu-id="9b05c-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="9b05c-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9b05c-106">Summary</span></span>

 <span data-ttu-id="9b05c-107">Ses</span><span class="sxs-lookup"><span data-stu-id="9b05c-107">Members</span></span>                        | <span data-ttu-id="9b05c-108">Descriptions</span><span class="sxs-lookup"><span data-stu-id="9b05c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9b05c-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="9b05c-110">Obtenez le ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="9b05c-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="9b05c-112">Obtenez le DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="9b05c-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="9b05c-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="9b05c-114">Obtenez le FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="9b05c-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="9b05c-116">Obtenez le HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="9b05c-118">Obtenez le HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="9b05c-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="9b05c-120">Obtenez le HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="9b05c-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="9b05c-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="9b05c-122">Obtenez le InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="9b05c-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="9b05c-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="9b05c-124">Obtenez les États de début de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="9b05c-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="9b05c-126">Obtenez le PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="9b05c-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="9b05c-128">Obtenez le PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="9b05c-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="9b05c-130">Obtenez le PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="9b05c-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="9b05c-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="9b05c-132">Obtenez le PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="9b05c-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="9b05c-134">Obtenez le PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="9b05c-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="9b05c-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="9b05c-136">Obtenez le PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="9b05c-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="9b05c-138">Obtenez le PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="9b05c-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="9b05c-140">Obtenez le PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="9b05c-142">Obtenez le PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="9b05c-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="9b05c-144">Obtenez le PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="9b05c-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="9b05c-146">Obtenez le PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="9b05c-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="9b05c-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="9b05c-148">Obtenez le PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="9b05c-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="9b05c-150">Obtenez le PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="9b05c-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="9b05c-151">get_Time</span></span>](#get_time) | <span data-ttu-id="9b05c-152">Obtenez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="9b05c-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="9b05c-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="9b05c-154">Obtenez le TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="9b05c-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="9b05c-156">Obtenez le TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="9b05c-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="9b05c-158">Obtenez le TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="9b05c-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="9b05c-160">Obtenez le TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="9b05c-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="9b05c-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="9b05c-162">Obtenez le TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="9b05c-164">Obtenez le TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="9b05c-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="9b05c-166">Définissez la ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="9b05c-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="9b05c-168">Définissez le DisplayRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="9b05c-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="9b05c-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="9b05c-170">Définissez la FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="9b05c-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="9b05c-172">Définissez la HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="9b05c-174">Définissez la HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="9b05c-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="9b05c-176">Définissez la HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="9b05c-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="9b05c-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="9b05c-178">Définissez la InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="9b05c-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="9b05c-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="9b05c-180">Définissez les KeyStates de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="9b05c-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="9b05c-182">Définissez la PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="9b05c-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="9b05c-184">Définissez la PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="9b05c-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="9b05c-186">Définissez la PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="9b05c-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="9b05c-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="9b05c-188">Définissez la PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="9b05c-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="9b05c-190">Définissez la PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="9b05c-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="9b05c-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="9b05c-192">Définissez la PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="9b05c-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="9b05c-194">Définissez la PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="9b05c-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="9b05c-196">Définissez la PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="9b05c-198">Définissez la PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="9b05c-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="9b05c-200">Définissez le PointerDeviceRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="9b05c-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="9b05c-202">Définissez la PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="9b05c-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="9b05c-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="9b05c-204">Définissez la PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="9b05c-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="9b05c-206">Définissez la PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="9b05c-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="9b05c-207">put_Time</span></span>](#put_time) | <span data-ttu-id="9b05c-208">Définissez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="9b05c-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="9b05c-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="9b05c-210">Définissez la TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="9b05c-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="9b05c-212">Définissez la TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="9b05c-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="9b05c-214">Définissez la TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="9b05c-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="9b05c-216">Définissez la TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="9b05c-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="9b05c-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="9b05c-218">Définissez la TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="9b05c-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="9b05c-220">Définissez la TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="9b05c-221">Il accepte les champs des trois et exclut certains types de données spécifiques Win32 comme HWND et descripteur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="9b05c-222">Notez que sourceDevice est pris en compte, mais que nous attendons que PointerDeviceRect et DisplayRect couvrent les cas d’utilisation existants de sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="9b05c-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="9b05c-223">Une autre différence majeure réside dans le fait que l’un ou l’autre emplacement est censé être présent dans les coordonnées physiques de WebView.</span><span class="sxs-lookup"><span data-stu-id="9b05c-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="9b05c-224">Il s’agit des coordonnées relatives à l’affichage WebView et à la mise à l’échelle DPI appliquée.</span><span class="sxs-lookup"><span data-stu-id="9b05c-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="9b05c-225">Ses</span><span class="sxs-lookup"><span data-stu-id="9b05c-225">Members</span></span>

#### <span data-ttu-id="9b05c-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="9b05c-227">Obtenez le ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="9b05c-228">[get_ButtonChangeKind](#get_buttonchangekind)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="9b05c-229">Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="9b05c-230">Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-231">get_DisplayRect</span></span> 

<span data-ttu-id="9b05c-232">Obtenez le DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="9b05c-233">valeur publique HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="9b05c-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="9b05c-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="9b05c-234">get_FrameId</span></span> 

<span data-ttu-id="9b05c-235">Obtenez le FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="9b05c-236">valeur publique HRESULT [get_FrameId](#get_frameid)(UInt32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="9b05c-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="9b05c-237">Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-238">get_HimetricLocation</span></span> 

<span data-ttu-id="9b05c-239">Obtenez le HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-240">valeur publique HRESULT [get_HimetricLocation](#get_himetriclocation)(point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="9b05c-241">Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="9b05c-243">Obtenez le HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="9b05c-244">valeur publique HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="9b05c-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="9b05c-245">Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-246">get_HistoryCount</span></span> 

<span data-ttu-id="9b05c-247">Obtenez le HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="9b05c-248">valeur publique HRESULT [get_HistoryCount](#get_historycount)(UInt32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="9b05c-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="9b05c-249">Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="9b05c-250">get_InputData</span></span> 

<span data-ttu-id="9b05c-251">Obtenez le InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="9b05c-252">[get_InputData](#get_inputdata)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="9b05c-253">Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="9b05c-254">get_KeyStates</span></span> 

<span data-ttu-id="9b05c-255">Obtenez les États de début de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="9b05c-256">valeur publique HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="9b05c-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="9b05c-257">Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-258">get_PenFlags</span></span> 

<span data-ttu-id="9b05c-259">Obtenez le PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="9b05c-260">valeur publique HRESULT [get_PenFlags](#get_penflags)(UInt32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="9b05c-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="9b05c-261">Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="9b05c-262">Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-263">get_PenMask</span></span> 

<span data-ttu-id="9b05c-264">Obtenez le PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="9b05c-265">valeur publique HRESULT [get_PenMask](#get_penmask)(UInt32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="9b05c-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="9b05c-266">Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="9b05c-267">Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-268">get_PenPressure</span></span> 

<span data-ttu-id="9b05c-269">Obtenez le PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="9b05c-270">valeur publique HRESULT [get_PenPressure](#get_penpressure)(UInt32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="9b05c-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="9b05c-271">Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="9b05c-272">get_PenRotation</span></span> 

<span data-ttu-id="9b05c-273">Obtenez le PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-274">valeur publique HRESULT [get_PenRotation](#get_penrotation)(UInt32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="9b05c-275">Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="9b05c-276">get_PenTiltX</span></span> 

<span data-ttu-id="9b05c-277">Obtenez le PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="9b05c-278">[get_PenTiltX](#get_pentiltx)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="9b05c-279">Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="9b05c-280">get_PenTiltY</span></span> 

<span data-ttu-id="9b05c-281">Obtenez le PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="9b05c-282">[get_PenTiltY](#get_pentilty)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="9b05c-283">Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-284">get_PerformanceCount</span></span> 

<span data-ttu-id="9b05c-285">Obtenez le PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="9b05c-286">[get_PerformanceCounts](#get_performancecount)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="9b05c-287">Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-288">get_PixelLocation</span></span> 

<span data-ttu-id="9b05c-289">Obtenez le PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-290">valeur publique HRESULT [get_PixelLocation](#get_pixellocation)(point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="9b05c-291">Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="9b05c-293">Obtenez le PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="9b05c-294">valeur publique HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="9b05c-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="9b05c-295">Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="9b05c-297">Obtenez le PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="9b05c-298">valeur publique HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="9b05c-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="9b05c-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-299">get_PointerFlags</span></span> 

<span data-ttu-id="9b05c-300">Obtenez le PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="9b05c-301">valeur publique HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="9b05c-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="9b05c-302">Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="9b05c-303">Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="9b05c-304">get_PointerId</span></span> 

<span data-ttu-id="9b05c-305">Obtenez le PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="9b05c-306">valeur publique HRESULT [get_PointerId](#get_pointerid)(UInt32 \* PointerId)</span><span class="sxs-lookup"><span data-stu-id="9b05c-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="9b05c-307">Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-308">get_PointerKind</span></span> 

<span data-ttu-id="9b05c-309">Obtenez le PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="9b05c-310">valeur publique HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="9b05c-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="9b05c-311">Cela correspond à la propriété pointerKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="9b05c-312">Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="9b05c-313">Prend en charge les PT_PEN et les PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="9b05c-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="9b05c-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="9b05c-314">get_Time</span></span> 

<span data-ttu-id="9b05c-315">Obtenez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="9b05c-316">valeur de HRESULT publique [get_Time](#get_time)(DWORD \* Time)</span><span class="sxs-lookup"><span data-stu-id="9b05c-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="9b05c-317">Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="9b05c-318">get_TouchContact</span></span> 

<span data-ttu-id="9b05c-319">Obtenez le TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="9b05c-320">valeur publique HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="9b05c-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="9b05c-321">Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="9b05c-323">Obtenez le TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="9b05c-324">valeur publique HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="9b05c-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="9b05c-325">Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-326">get_TouchFlags</span></span> 

<span data-ttu-id="9b05c-327">Obtenez le TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="9b05c-328">valeur publique HRESULT [get_TouchFlags](#get_touchflags)(UInt32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="9b05c-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="9b05c-329">Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="9b05c-330">Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-331">get_TouchMask</span></span> 

<span data-ttu-id="9b05c-332">Obtenez le TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="9b05c-333">valeur publique HRESULT [get_TouchMask](#get_touchmask)(UInt32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="9b05c-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="9b05c-334">Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="9b05c-335">Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="9b05c-336">get_TouchOrientation</span></span> 

<span data-ttu-id="9b05c-337">Obtenez le TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-338">valeur publique HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="9b05c-339">Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-340">get_TouchPressure</span></span> 

<span data-ttu-id="9b05c-341">Obtenez le TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="9b05c-342">valeur publique HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="9b05c-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="9b05c-343">Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="9b05c-345">Définissez la ButtonChangeKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="9b05c-346">[put_ButtonChangeKind](#put_buttonchangekind)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="9b05c-347">Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="9b05c-348">Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-349">put_DisplayRect</span></span> 

<span data-ttu-id="9b05c-350">Définissez le DisplayRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="9b05c-351">valeur publique HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="9b05c-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="9b05c-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="9b05c-352">put_FrameId</span></span> 

<span data-ttu-id="9b05c-353">Définissez la FrameID de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="9b05c-354">[put_FrameIds](#put_frameid)HRESULT publiques (UInt32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="9b05c-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="9b05c-355">Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-356">put_HimetricLocation</span></span> 

<span data-ttu-id="9b05c-357">Définissez la HimetricLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-358">[put_HimetricLocation](#put_himetriclocation)par le biais du message public HRESULT (point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="9b05c-359">Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="9b05c-361">Définissez la HimetricLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="9b05c-362">[put_HimetricLocationRaw](#put_himetriclocationraw)par le biais du message public HRESULT (point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="9b05c-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="9b05c-363">Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-364">put_HistoryCount</span></span> 

<span data-ttu-id="9b05c-365">Définissez la HistoryCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="9b05c-366">[put_HistoryCounts](#put_historycount)HRESULT publiques (UInt32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="9b05c-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="9b05c-367">Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="9b05c-368">put_InputData</span></span> 

<span data-ttu-id="9b05c-369">Définissez la InputData de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="9b05c-370">[put_InputData](#put_inputdata)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="9b05c-371">Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="9b05c-372">put_KeyStates</span></span> 

<span data-ttu-id="9b05c-373">Définissez les KeyStates de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="9b05c-374">[put_KeyStates](#put_keystates)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="9b05c-375">Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-376">put_PenFlags</span></span> 

<span data-ttu-id="9b05c-377">Définissez la PenFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="9b05c-378">[put_PenFlagss](#put_penflags)HRESULT publiques (UInt32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="9b05c-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="9b05c-379">Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="9b05c-380">Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-381">put_PenMask</span></span> 

<span data-ttu-id="9b05c-382">Définissez la PenMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="9b05c-383">[put_PenMasks](#put_penmask)HRESULT publiques (UInt32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="9b05c-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="9b05c-384">Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="9b05c-385">Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-386">put_PenPressure</span></span> 

<span data-ttu-id="9b05c-387">Définissez la PenPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="9b05c-388">[put_PenPressures](#put_penpressure)HRESULT publiques (UInt32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="9b05c-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="9b05c-389">Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="9b05c-390">put_PenRotation</span></span> 

<span data-ttu-id="9b05c-391">Définissez la PenRotation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-392">[put_PenRotations](#put_penrotation)HRESULT publiques (UInt32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="9b05c-393">Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="9b05c-394">put_PenTiltX</span></span> 

<span data-ttu-id="9b05c-395">Définissez la PenTiltX de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="9b05c-396">[put_PenTiltX](#put_pentiltx)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="9b05c-397">Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="9b05c-398">put_PenTiltY</span></span> 

<span data-ttu-id="9b05c-399">Définissez la PenTiltY de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="9b05c-400">[put_PenTiltY](#put_pentilty)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="9b05c-401">Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="9b05c-402">put_PerformanceCount</span></span> 

<span data-ttu-id="9b05c-403">Définissez la PerformanceCount de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="9b05c-404">[put_PerformanceCount](#put_performancecount)par le biais du public HRESULT</span><span class="sxs-lookup"><span data-stu-id="9b05c-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="9b05c-405">Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="9b05c-406">put_PixelLocation</span></span> 

<span data-ttu-id="9b05c-407">Définissez la PixelLocation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-408">[put_PixelLocation](#put_pixellocation)par le biais du message public HRESULT (point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="9b05c-409">Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="9b05c-411">Définissez la PixelLocationRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="9b05c-412">[put_PixelLocationRaw](#put_pixellocationraw)par le biais du message public HRESULT (point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="9b05c-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="9b05c-413">Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="9b05c-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="9b05c-415">Définissez le PointerDeviceRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="9b05c-416">valeur publique HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="9b05c-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="9b05c-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-417">put_PointerFlags</span></span> 

<span data-ttu-id="9b05c-418">Définissez la PointerFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="9b05c-419">[put_PointerFlagss](#put_pointerflags)HRESULT publiques (UInt32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="9b05c-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="9b05c-420">Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="9b05c-421">Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="9b05c-422">put_PointerId</span></span> 

<span data-ttu-id="9b05c-423">Définissez la PointerId de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="9b05c-424">[put_PointerIds](#put_pointerid)HRESULT publiques (UInt32 PointerId)</span><span class="sxs-lookup"><span data-stu-id="9b05c-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="9b05c-425">Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="9b05c-426">put_PointerKind</span></span> 

<span data-ttu-id="9b05c-427">Définissez la PointerKind de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="9b05c-428">[put_PointerKind](#put_pointerkind)par le biais du public HRESULT (DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="9b05c-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="9b05c-429">Cela correspond à la propriété pointerKind de l’struct POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="9b05c-430">Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="9b05c-431">Prend en charge les PT_PEN et les PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="9b05c-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="9b05c-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="9b05c-432">put_Time</span></span> 

<span data-ttu-id="9b05c-433">Définissez l’heure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="9b05c-434">valeur de HRESULT publique [put_Time](#put_time)</span><span class="sxs-lookup"><span data-stu-id="9b05c-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="9b05c-435">Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="9b05c-436">put_TouchContact</span></span> 

<span data-ttu-id="9b05c-437">Définissez la TouchContact de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="9b05c-438">valeur publique HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="9b05c-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="9b05c-439">Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="9b05c-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="9b05c-441">Définissez la TouchContactRaw de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="9b05c-442">valeur publique HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="9b05c-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="9b05c-443">Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="9b05c-444">put_TouchFlags</span></span> 

<span data-ttu-id="9b05c-445">Définissez la TouchFlags de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="9b05c-446">[put_TouchFlagss](#put_touchflags)HRESULT publiques (UInt32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="9b05c-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="9b05c-447">Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="9b05c-448">Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="9b05c-449">put_TouchMask</span></span> 

<span data-ttu-id="9b05c-450">Définissez la TouchMask de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="9b05c-451">[put_TouchMasks](#put_touchmask)HRESULT publiques (UInt32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="9b05c-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="9b05c-452">Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="9b05c-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="9b05c-453">Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="9b05c-454">put_TouchOrientation</span></span> 

<span data-ttu-id="9b05c-455">Définissez la TouchOrientation de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="9b05c-456">[put_TouchOrientations](#put_touchorientation)HRESULT publiques (UInt32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="9b05c-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="9b05c-457">Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="9b05c-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="9b05c-458">put_TouchPressure</span></span> 

<span data-ttu-id="9b05c-459">Définissez la TouchPressure de l’événement de pointeur.</span><span class="sxs-lookup"><span data-stu-id="9b05c-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="9b05c-460">[put_TouchPressures](#put_touchpressure)HRESULT publiques (UInt32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="9b05c-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="9b05c-461">Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).</span><span class="sxs-lookup"><span data-stu-id="9b05c-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

