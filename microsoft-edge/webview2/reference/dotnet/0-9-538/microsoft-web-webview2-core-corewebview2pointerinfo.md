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
# 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Espace de noms: Microsoft. Web. WebView2. Core \
Assemblage: Microsoft.Web.WebView2.Core.dll

Il s’agit essentiellement d’un objet POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO combiné.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[ButtonChangeKind](#buttonchangekind) | ButtonChangeKind de l’événement de pointeur.
[DisplayRect](#displayrect) | DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).
[FrameId](#frameid) | FrameID de l’événement de pointeur.
[HimetricLocation](#himetriclocation) | HimetricLocation de l’événement de pointeur.
[HimetricLocationRaw](#himetriclocationraw) | HimetricLocationRaw de l’événement de pointeur.
[HistoryCount](#historycount) | HistoryCount de l’événement de pointeur.
[InputData](#inputdata) | InputData de l’événement de pointeur.
[État](#keystates) | Les inversions de l’événement de pointeur.
[PenFlags](#penflags) | PenFlags de l’événement de pointeur.
[PenMask](#penmask) | PenMask de l’événement de pointeur.
[PenPressure](#penpressure) | PenPressure de l’événement de pointeur.
[PenRotation](#penrotation) | PenRotation de l’événement de pointeur.
[PenTiltX](#pentiltx) | PenTiltX de l’événement de pointeur.
[PenTiltY](#pentilty) | PenTiltY de l’événement de pointeur.
[PerformanceCount](#performancecount) | PerformanceCount de l’événement de pointeur.
[PixelLocation](#pixellocation) | PixelLocation de l’événement de pointeur.
[PixelLocationRaw](#pixellocationraw) | PixelLocationRaw de l’événement de pointeur.
[PointerDeviceRect](#pointerdevicerect) | PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).
[PointerFlags](#pointerflags) | PointerFlags de l’événement de pointeur.
[PointerId](#pointerid) | PointerId de l’événement de pointeur.
[PointerKind](#pointerkind) | PointerKind de l’événement de pointeur.
[Heure](#time) | Heure de l’événement de pointeur.
[TouchContact](#touchcontact) | TouchContact de l’événement de pointeur.
[TouchContactRaw](#touchcontactraw) | TouchContactRaw de l’événement de pointeur.
[TouchFlags](#touchflags) | TouchFlags de l’événement de pointeur.
[TouchMask](#touchmask) | TouchMask de l’événement de pointeur.
[TouchOrientation](#touchorientation) | TouchOrientation de l’événement de pointeur.
[TouchPressure](#touchpressure) | TouchPressure de l’événement de pointeur.

## Ses

#### ButtonChangeKind 

ButtonChangeKind de l’événement de pointeur.

> public ent [ButtonChangeKind](#buttonchangekind)

Cela correspond à la propriété ButtonChangeKind de l’struct POINTER_INFO. Les valeurs sont définies par l’énumération POINTER_BUTTON_CHANGE_KIND dans le SDK Windows (winuser. h).

#### DisplayRect 

DisplayRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

> public Rect [DisplayRect](#displayrect)

#### FrameId 

FrameID de l’événement de pointeur.

> public uint [FrameId](#frameid)

Cela correspond à la propriété frameId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### HimetricLocation 

HimetricLocation de l’événement de pointeur.

> Point public [HimetricLocation](#himetriclocation)

Cela correspond à la propriété ptHimetricLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### HimetricLocationRaw 

HimetricLocationRaw de l’événement de pointeur.

> Point public [HimetricLocationRaw](#himetriclocationraw)

Cela correspond à la propriété ptHimetricLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### HistoryCount 

HistoryCount de l’événement de pointeur.

> public uint [HistoryCount](#historycount)

Cela correspond à la propriété historyCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### InputData 

InputData de l’événement de pointeur.

> public ent [InputData](#inputdata)

Cela correspond à la propriété InputData de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### État 

Les inversions de l’événement de pointeur.

> [KeyStates](#keystates) public uint

Cela correspond à la propriété dwKeyStates de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### PenFlags 

PenFlags de l’événement de pointeur.

> public uint [PenFlags](#penflags)

Cela correspond à la propriété penFlags de l’struct POINTER_PEN_INFO. Les valeurs sont définies par les constantes PEN_FLAGS dans le SDK Windows (winuser. h).

#### PenMask 

PenMask de l’événement de pointeur.

> public uint [PenMask](#penmask)

Cela correspond à la propriété penMask de l’struct POINTER_PEN_INFO. Les valeurs sont définies par les constantes PEN_MASK dans le SDK Windows (winuser. h).

#### PenPressure 

PenPressure de l’événement de pointeur.

> public uint [PenPressure](#penpressure)

Cela correspond à la propriété de pression de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### PenRotation 

PenRotation de l’événement de pointeur.

> public uint [PenRotation](#penrotation)

Cela correspond à la propriété rotation du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### PenTiltX 

PenTiltX de l’événement de pointeur.

> public ent [PenTiltX](#pentiltx)

Cela correspond à la propriété tiltX de l’struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### PenTiltY 

PenTiltY de l’événement de pointeur.

> public ent [PenTiltY](#pentilty)

Cela correspond à la propriété inclinable du struct POINTER_PEN_INFO tel que défini dans le SDK Windows (winuser. h).

#### PerformanceCount 

PerformanceCount de l’événement de pointeur.

> public ulong [PerformanceCount](#performancecount)

Cela correspond à la propriété PerformanceCount de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### PixelLocation 

PixelLocation de l’événement de pointeur.

> Point public [PixelLocation](#pixellocation)

Cela correspond à la propriété ptPixelLocation de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### PixelLocationRaw 

PixelLocationRaw de l’événement de pointeur.

> Point public [PixelLocationRaw](#pixellocationraw)

Cela correspond à la propriété ptPixelLocationRaw de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### PointerDeviceRect 

PointerDeviceRect de la propriété sourceDevice de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

> public Rect [PointerDeviceRect](#pointerdevicerect)

#### PointerFlags 

PointerFlags de l’événement de pointeur.

> public uint [PointerFlags](#pointerflags)

Cela correspond à la propriété pointerFlags de l’struct POINTER_INFO. Les valeurs sont définies par les constantes POINTER_FLAGS dans le SDK Windows (winuser. h).

#### PointerId 

PointerId de l’événement de pointeur.

> public uint [PointerId](#pointerid)

Cela correspond à la propriété pointerId de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### PointerKind 

PointerKind de l’événement de pointeur.

> public uint [PointerKind](#pointerkind)

Cela correspond à la propriété pointerKind de l’struct POINTER_INFO. Les valeurs sont définies par l’énumération POINTER_INPUT_KIND dans le SDK Windows (winuser. h). Prend en charge les PT_PEN et les PT_TOUCH.

#### Heure 

Heure de l’événement de pointeur.

> [heure](#time) du public

Cela correspond à la propriété dwTime de l’struct POINTER_INFO tel que défini dans le SDK Windows (winuser. h).

#### TouchContact 

TouchContact de l’événement de pointeur.

> public Rect [TouchContact](#touchcontact)

Cela correspond à la propriété rcContact de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### TouchContactRaw 

TouchContactRaw de l’événement de pointeur.

> public Rect [TouchContactRaw](#touchcontactraw)

Cela correspond à la propriété rcContactRaw de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### TouchFlags 

TouchFlags de l’événement de pointeur.

> public uint [TouchFlags](#touchflags)

Cela correspond à la propriété touchFlags de l’struct POINTER_TOUCH_INFO. Les valeurs sont définies par les constantes TOUCH_FLAGS dans le SDK Windows (winuser. h).

#### TouchMask 

TouchMask de l’événement de pointeur.

> public uint [TouchMask](#touchmask)

Cela correspond à la propriété touchMask de l’struct POINTER_TOUCH_INFO. Les valeurs sont définies par les constantes TOUCH_MASK dans le SDK Windows (winuser. h).

#### TouchOrientation 

TouchOrientation de l’événement de pointeur.

> public uint [TouchOrientation](#touchorientation)

Cela correspond à la propriété orientation du struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

#### TouchPressure 

TouchPressure de l’événement de pointeur.

> public uint [TouchPressure](#touchpressure)

Cela correspond à la propriété de pression de l’struct POINTER_TOUCH_INFO tel que défini dans le SDK Windows (winuser. h).

