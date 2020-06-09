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
ms.openlocfilehash: ef0546c03e2d2ccc87677125772b1663f2ec6362
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698700"
---
# interface ICoreWebView2ExperimentalPointerInfo 

> [!NOTE]
> Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

Il s’agit essentiellement d’un objet POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combiné.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_ButtonChangeKind](#get_buttonchangekind) | Obtenez le ButtonChangeKind de l’événement de pointeur.
[get_DisplayRect](#get_displayrect) | Obtenez le DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).
[get_FrameId](#get_frameid) | Obtenez le FrameID de l’événement de pointeur.
[get_HimetricLocation](#get_himetriclocation) | Obtenez le HimetricLocation de l’événement de pointeur.
[get_HimetricLocationRaw](#get_himetriclocationraw) | Obtenez le HimetricLocationRaw de l’événement de pointeur.
[get_HistoryCount](#get_historycount) | Obtenez le HistoryCount de l’événement de pointeur.
[get_InputData](#get_inputdata) | Obtenez le InputData de l’événement de pointeur.
[get_KeyStates](#get_keystates) | Obtenez les États de début de l’événement de pointeur.
[get_PenFlags](#get_penflags) | Obtenez le PenFlags de l’événement de pointeur.
[get_PenMask](#get_penmask) | Obtenez le PenMask de l’événement de pointeur.
[get_PenPressure](#get_penpressure) | Obtenez le PenPressure de l’événement de pointeur.
[get_PenRotation](#get_penrotation) | Obtenez le PenRotation de l’événement de pointeur.
[get_PenTiltX](#get_pentiltx) | Obtenez le PenTiltX de l’événement de pointeur.
[get_PenTiltY](#get_pentilty) | Obtenez le PenTiltY de l’événement de pointeur.
[get_PerformanceCount](#get_performancecount) | Obtenez le PerformanceCount de l’événement de pointeur.
[get_PixelLocation](#get_pixellocation) | Obtenez le PixelLocation de l’événement de pointeur.
[get_PixelLocationRaw](#get_pixellocationraw) | Obtenez le PixelLocationRaw de l’événement de pointeur.
[get_PointerDeviceRect](#get_pointerdevicerect) | Obtenez le PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).
[get_PointerFlags](#get_pointerflags) | Obtenez le PointerFlags de l’événement de pointeur.
[get_PointerId](#get_pointerid) | Obtenez le PointerId de l’événement de pointeur.
[get_PointerKind](#get_pointerkind) | Obtenez le PointerKind de l’événement de pointeur.
[get_Time](#get_time) | Obtenez l’heure de l’événement de pointeur.
[get_TouchContact](#get_touchcontact) | Obtenez le TouchContact de l’événement de pointeur.
[get_TouchContactRaw](#get_touchcontactraw) | Obtenez le TouchContactRaw de l’événement de pointeur.
[get_TouchFlags](#get_touchflags) | Obtenez le TouchFlags de l’événement de pointeur.
[get_TouchMask](#get_touchmask) | Obtenez le TouchMask de l’événement de pointeur.
[get_TouchOrientation](#get_touchorientation) | Obtenez le TouchOrientation de l’événement de pointeur.
[get_TouchPressure](#get_touchpressure) | Obtenez le TouchPressure de l’événement de pointeur.
[put_ButtonChangeKind](#put_buttonchangekind) | Définissez la ButtonChangeKind de l’événement de pointeur.
[put_DisplayRect](#put_displayrect) | Définissez le DisplayRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).
[put_FrameId](#put_frameid) | Définissez la FrameID de l’événement de pointeur.
[put_HimetricLocation](#put_himetriclocation) | Définissez la HimetricLocation de l’événement de pointeur.
[put_HimetricLocationRaw](#put_himetriclocationraw) | Définissez la HimetricLocationRaw de l’événement de pointeur.
[put_HistoryCount](#put_historycount) | Définissez la HistoryCount de l’événement de pointeur.
[put_InputData](#put_inputdata) | Définissez la InputData de l’événement de pointeur.
[put_KeyStates](#put_keystates) | Définissez les KeyStates de l’événement de pointeur.
[put_PenFlags](#put_penflags) | Définissez la PenFlags de l’événement de pointeur.
[put_PenMask](#put_penmask) | Définissez la PenMask de l’événement de pointeur.
[put_PenPressure](#put_penpressure) | Définissez la PenPressure de l’événement de pointeur.
[put_PenRotation](#put_penrotation) | Définissez la PenRotation de l’événement de pointeur.
[put_PenTiltX](#put_pentiltx) | Définissez la PenTiltX de l’événement de pointeur.
[put_PenTiltY](#put_pentilty) | Définissez la PenTiltY de l’événement de pointeur.
[put_PerformanceCount](#put_performancecount) | Définissez la PerformanceCount de l’événement de pointeur.
[put_PixelLocation](#put_pixellocation) | Définissez la PixelLocation de l’événement de pointeur.
[put_PixelLocationRaw](#put_pixellocationraw) | Définissez la PixelLocationRaw de l’événement de pointeur.
[put_PointerDeviceRect](#put_pointerdevicerect) | Définissez le PointerDeviceRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).
[put_PointerFlags](#put_pointerflags) | Définissez la PointerFlags de l’événement de pointeur.
[put_PointerId](#put_pointerid) | Définissez la PointerId de l’événement de pointeur.
[put_PointerKind](#put_pointerkind) | Définissez la PointerKind de l’événement de pointeur.
[put_Time](#put_time) | Définissez l’heure de l’événement de pointeur.
[put_TouchContact](#put_touchcontact) | Définissez la TouchContact de l’événement de pointeur.
[put_TouchContactRaw](#put_touchcontactraw) | Définissez la TouchContactRaw de l’événement de pointeur.
[put_TouchFlags](#put_touchflags) | Définissez la TouchFlags de l’événement de pointeur.
[put_TouchMask](#put_touchmask) | Définissez la TouchMask de l’événement de pointeur.
[put_TouchOrientation](#put_touchorientation) | Définissez la TouchOrientation de l’événement de pointeur.
[put_TouchPressure](#put_touchpressure) | Définissez la TouchPressure de l’événement de pointeur.

Il accepte les champs des trois et exclut certains types de données spécifiques Win32 comme HWND et descripteur. Notez que sourceDevice est pris en compte, mais que nous attendons que PointerDeviceRect et DisplayRect couvrent les cas d’utilisation existants de sourceDevice. Une autre différence majeure réside dans le fait que l’un ou l’autre emplacement est censé être présent dans les coordonnées physiques de WebView. Il s’agit des coordonnées relatives à l’affichage WebView et à la mise à l’échelle DPI appliquée.

## Ses

#### get_ButtonChangeKind 

Obtenez le ButtonChangeKind de l’événement de pointeur.

> [get_ButtonChangeKind](#get_buttonchangekind)par le biais du public HRESULT

Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO. Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).

#### get_DisplayRect 

Obtenez le DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).

> valeur publique HRESULT [get_DisplayRect](#get_displayrect)(Rect * DisplayRect)

#### get_FrameId 

Obtenez le FrameID de l’événement de pointeur.

> valeur publique HRESULT [get_FrameId](#get_frameid)(UInt32 * FrameId)

Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_HimetricLocation 

Obtenez le HimetricLocation de l’événement de pointeur.

> valeur publique HRESULT [get_HimetricLocation](#get_himetriclocation)(point * HimetricLocation)

Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_HimetricLocationRaw 

Obtenez le HimetricLocationRaw de l’événement de pointeur.

> valeur publique HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(point * HimetricLocationRaw)

Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_HistoryCount 

Obtenez le HistoryCount de l’événement de pointeur.

> valeur publique HRESULT [get_HistoryCount](#get_historycount)(UInt32 * HistoryCount)

Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_InputData 

Obtenez le InputData de l’événement de pointeur.

> [get_InputData](#get_inputdata)par le biais du public HRESULT

Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_KeyStates 

Obtenez les États de début de l’événement de pointeur.

> valeur publique HRESULT [get_KeyStates](#get_keystates)(DWORD * KeyStates)

Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PenFlags 

Obtenez le PenFlags de l’événement de pointeur.

> valeur publique HRESULT [get_PenFlags](#get_penflags)(UInt32 * PenFlags)

Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO. Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).

#### get_PenMask 

Obtenez le PenMask de l’événement de pointeur.

> valeur publique HRESULT [get_PenMask](#get_penmask)(UInt32 * PenMask)

Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO. Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).

#### get_PenPressure 

Obtenez le PenPressure de l’événement de pointeur.

> valeur publique HRESULT [get_PenPressure](#get_penpressure)(UInt32 * PenPressure)

Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PenRotation 

Obtenez le PenRotation de l’événement de pointeur.

> valeur publique HRESULT [get_PenRotation](#get_penrotation)(UInt32 * PenRotation)

Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PenTiltX 

Obtenez le PenTiltX de l’événement de pointeur.

> [get_PenTiltX](#get_pentiltx)par le biais du public HRESULT

Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PenTiltY 

Obtenez le PenTiltY de l’événement de pointeur.

> [get_PenTiltY](#get_pentilty)par le biais du public HRESULT

Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PerformanceCount 

Obtenez le PerformanceCount de l’événement de pointeur.

> [get_PerformanceCounts](#get_performancecount)par le biais du public HRESULT

Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PixelLocation 

Obtenez le PixelLocation de l’événement de pointeur.

> valeur publique HRESULT [get_PixelLocation](#get_pixellocation)(point * PixelLocation)

Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PixelLocationRaw 

Obtenez le PixelLocationRaw de l’événement de pointeur.

> valeur publique HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(point * PixelLocationRaw)

Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PointerDeviceRect 

Obtenez le PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO, tel que défini dans le SDK Windows (winuser. h).

> valeur publique HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect * PointerDeviceRect)

#### get_PointerFlags 

Obtenez le PointerFlags de l’événement de pointeur.

> valeur publique HRESULT [get_PointerFlags](#get_pointerflags)(UInt32 * PointerFlags)

Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO. Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).

#### get_PointerId 

Obtenez le PointerId de l’événement de pointeur.

> valeur publique HRESULT [get_PointerId](#get_pointerid)(UInt32 * PointerId)

Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_PointerKind 

Obtenez le PointerKind de l’événement de pointeur.

> valeur publique HRESULT [get_PointerKind](#get_pointerkind)(DWORD * PointerKind)

Cela correspond à la propriété pointerKind de l’struct POINTER_INFO. Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h). Prend en charge les PT_PEN et les PT_TOUCH.

#### get_Time 

Obtenez l’heure de l’événement de pointeur.

> valeur de HRESULT publique [get_Time](#get_time)(DWORD * Time)

Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_TouchContact 

Obtenez le TouchContact de l’événement de pointeur.

> valeur publique HRESULT [get_TouchContact](#get_touchcontact)(Rect * TouchContact)

Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_TouchContactRaw 

Obtenez le TouchContactRaw de l’événement de pointeur.

> valeur publique HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect * TouchContactRaw)

Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_TouchFlags 

Obtenez le TouchFlags de l’événement de pointeur.

> valeur publique HRESULT [get_TouchFlags](#get_touchflags)(UInt32 * TouchFlags)

Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO. Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).

#### get_TouchMask 

Obtenez le TouchMask de l’événement de pointeur.

> valeur publique HRESULT [get_TouchMask](#get_touchmask)(UInt32 * TouchMask)

Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO. Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).

#### get_TouchOrientation 

Obtenez le TouchOrientation de l’événement de pointeur.

> valeur publique HRESULT [get_TouchOrientation](#get_touchorientation)(UInt32 * TouchOrientation)

Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### get_TouchPressure 

Obtenez le TouchPressure de l’événement de pointeur.

> valeur publique HRESULT [get_TouchPressure](#get_touchpressure)(UInt32 * TouchPressure)

Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_ButtonChangeKind 

Définissez la ButtonChangeKind de l’événement de pointeur.

> [put_ButtonChangeKind](#put_buttonchangekind)par le biais du public HRESULT

Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO. Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).

#### put_DisplayRect 

Définissez le DisplayRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

> valeur publique HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)

#### put_FrameId 

Définissez la FrameID de l’événement de pointeur.

> [put_FrameIds](#put_frameid)HRESULT publiques (UInt32 FrameId)

Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_HimetricLocation 

Définissez la HimetricLocation de l’événement de pointeur.

> [put_HimetricLocation](#put_himetriclocation)par le biais du message public HRESULT (point HimetricLocation)

Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_HimetricLocationRaw 

Définissez la HimetricLocationRaw de l’événement de pointeur.

> [put_HimetricLocationRaw](#put_himetriclocationraw)par le biais du message public HRESULT (point HimetricLocationRaw)

Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_HistoryCount 

Définissez la HistoryCount de l’événement de pointeur.

> [put_HistoryCounts](#put_historycount)HRESULT publiques (UInt32 HistoryCount)

Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_InputData 

Définissez la InputData de l’événement de pointeur.

> [put_InputData](#put_inputdata)par le biais du public HRESULT

Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_KeyStates 

Définissez les KeyStates de l’événement de pointeur.

> [put_KeyStates](#put_keystates)par le biais du public HRESULT

Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PenFlags 

Définissez la PenFlags de l’événement de pointeur.

> [put_PenFlagss](#put_penflags)HRESULT publiques (UInt32 PenFlags)

Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO. Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).

#### put_PenMask 

Définissez la PenMask de l’événement de pointeur.

> [put_PenMasks](#put_penmask)HRESULT publiques (UInt32 PenMask)

Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO. Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).

#### put_PenPressure 

Définissez la PenPressure de l’événement de pointeur.

> [put_PenPressures](#put_penpressure)HRESULT publiques (UInt32 PenPressure)

Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PenRotation 

Définissez la PenRotation de l’événement de pointeur.

> [put_PenRotations](#put_penrotation)HRESULT publiques (UInt32 PenRotation)

Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PenTiltX 

Définissez la PenTiltX de l’événement de pointeur.

> [put_PenTiltX](#put_pentiltx)par le biais du public HRESULT

Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PenTiltY 

Définissez la PenTiltY de l’événement de pointeur.

> [put_PenTiltY](#put_pentilty)par le biais du public HRESULT

Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PerformanceCount 

Définissez la PerformanceCount de l’événement de pointeur.

> [put_PerformanceCount](#put_performancecount)par le biais du public HRESULT

Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PixelLocation 

Définissez la PixelLocation de l’événement de pointeur.

> [put_PixelLocation](#put_pixellocation)par le biais du message public HRESULT (point PixelLocation)

Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PixelLocationRaw 

Définissez la PixelLocationRaw de l’événement de pointeur.

> [put_PixelLocationRaw](#put_pixellocationraw)par le biais du message public HRESULT (point PixelLocationRaw)

Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PointerDeviceRect 

Définissez le PointerDeviceRect de la propriété sourceDevice de l’struct de POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

> valeur publique HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)

#### put_PointerFlags 

Définissez la PointerFlags de l’événement de pointeur.

> [put_PointerFlagss](#put_pointerflags)HRESULT publiques (UInt32 PointerFlags)

Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO. Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).

#### put_PointerId 

Définissez la PointerId de l’événement de pointeur.

> [put_PointerIds](#put_pointerid)HRESULT publiques (UInt32 PointerId)

Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_PointerKind 

Définissez la PointerKind de l’événement de pointeur.

> [put_PointerKind](#put_pointerkind)par le biais du public HRESULT (DWORD PointerKind)

Cela correspond à la propriété pointerKind de l’struct POINTER_INFO. Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h). Prend en charge les PT_PEN et les PT_TOUCH.

#### put_Time 

Définissez l’heure de l’événement de pointeur.

> valeur de HRESULT publique [put_Time](#put_time)

Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_TouchContact 

Définissez la TouchContact de l’événement de pointeur.

> valeur publique HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)

Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_TouchContactRaw 

Définissez la TouchContactRaw de l’événement de pointeur.

> valeur publique HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)

Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_TouchFlags 

Définissez la TouchFlags de l’événement de pointeur.

> [put_TouchFlagss](#put_touchflags)HRESULT publiques (UInt32 TouchFlags)

Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO. Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).

#### put_TouchMask 

Définissez la TouchMask de l’événement de pointeur.

> [put_TouchMasks](#put_touchmask)HRESULT publiques (UInt32 TouchMask)

Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO. Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).

#### put_TouchOrientation 

Définissez la TouchOrientation de l’événement de pointeur.

> [put_TouchOrientations](#put_touchorientation)HRESULT publiques (UInt32 TouchOrientation)

Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### put_TouchPressure 

Définissez la TouchPressure de l’événement de pointeur.

> [put_TouchPressures](#put_touchpressure)HRESULT publiques (UInt32 TouchPressure)

Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

