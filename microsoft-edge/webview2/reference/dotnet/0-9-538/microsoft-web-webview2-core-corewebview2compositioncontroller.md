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
ms.openlocfilehash: 33adcccc4174a4ebcbabe4a169cd430942ad8a5a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698728"
---
# Classe Microsoft. Web. WebView2. Core. CoreWebView2CompositionController 

> [!NOTE]
> Il s’agit d’une [API expérimentale](../../../concepts/versioning.md#experimental-apis) fournie avec notre version SDK version [0.9.538-préliminaire](../../../releasenotes.md#09538).

Espace de noms: Microsoft. Web. WebView2. Core \
Assembly: Microsoft. Web. WebView2. Core. dll

Cette classe est une extension de la classe CoreWebView2Controller pour prendre en charge l’hébergement visuel.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[Curseur](#cursor) | Le curseur actuel attendu par le WebView devrait être.
[CursorChanged](#cursorchanged) | L’événement se déclenche lorsque WebView considère que le curseur doit être modifié.
[RootVisualTarget](#rootvisualtarget) | Le RootVisualTarget est un élément visuel de l’arborescence visuelle de l’application hôte.
[UIAProvider](#uiaprovider) | Renvoie le fournisseur UI Automation pour le WebView.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Fonction d’assistance permettant de convertir un pointerId reçu du système en CoreWebView2ExperimentalPointerInfo.
[SendMouseInput](#sendmouseinput) | Si eventKind est CoreWebView2MouseEventKind. HorizontalWheel ou CoreWebView2MouseEventKind. Wheel, mouseData spécifie la valeur du mouvement de la roulette.
[SendPointerInput](#sendpointerinput) | SendPointerInput accepte les entrées de pointeur en forme d’effleurement ou de stylet définies dans CoreWebView2PointerEventKind.

## Ses

#### Curseur 

Le curseur actuel attendu par le WebView devrait être.

> [curseur](#cursor) IntPtr public

Le curseur doit être défini dans WM_SETCURSOR par le biais de mous. SetCursor ou défini sur le HWND parent/ancêtre correspondant du WebView via SetClassLongPtr. Le HCURSOR peut être retardée de sorte que CopyCursor/DestroyCursor est recommandé de conserver votre propre copie si vous ne faites pas immédiatement la définition du curseur.

#### CursorChanged 

L’événement se déclenche lorsque WebView considère que le curseur doit être modifié.

> événement public EventHandler< objet > [CursorChanged](#cursorchanged)

Par exemple, lorsque le curseur de la souris est actuellement le curseur par défaut, mais qu’il est alors déplacé sur du texte, il peut essayer de basculer vers le curseur IBeam.

#### RootVisualTarget 

Le RootVisualTarget est un élément visuel de l’arborescence visuelle de l’application hôte.

> [RootVisualTarget](#rootvisualtarget) d’objet public

Cet élément visuel est l’endroit où le WebView se connecte à son arborescence d’éléments visuels. L’application utilise cet élément visuel pour positionner le WebView dans l’application. L’application doit toujours utiliser la propriété Bounds pour redimensionner le WebView. La propriété RootVisualTarget peut être IDCompositionVisual ou Windows:: UI:: composition:: ContainerVisual. WebView va connecter son arborescence d’éléments visuels à l’élément visuel fourni avant de revenir à partir de la méthode setter de propriété. L’application doit valider sur son appareil définissant la propriété RootVisualTarget. La propriété RootVisualTarget prend en charge la valeur nullptr pour déconnecter le WebView de l’arborescence visuelle de l’application.

#### UIAProvider 

Renvoie le fournisseur UI Automation pour le WebView.

> [UIAProvider](#uiaprovider) d’objet public

#### CreateCoreWebView2PointerInfoFromPointerId 

Fonction d’assistance permettant de convertir un pointerId reçu du système en CoreWebView2ExperimentalPointerInfo.

> public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint PointerId, IntPtr FenêtreParent, Matrix4x4 Transform)

FenêtreParent est le HWND qui contient le WebView. Il peut s’agir d’un HWND de l’arborescence HWND qui contient le WebView. CoreWebView2Matrix4x4 est la transformation de ce HWND vers le WebView. Le CoreWebView2ExperimentalPointerInfo renvoyé est utilisé dans SendPointerInfo. Le type de pointeur doit être PEN ou Touch, ou la fonction échoue.

#### SendMouseInput 

Si eventKind est CoreWebView2MouseEventKind. HorizontalWheel ou CoreWebView2MouseEventKind. Wheel, mouseData spécifie la valeur du mouvement de la roulette.

> public void [SendMouseInput](#sendmouseinput)([CoreWebView2MouseEventKind](./namespace-microsoft-web-webview2-core.md) eventKind [CoreWebView2MouseEventVirtualKeys](./namespace-microsoft-web-webview2-core.md) VirtualKeys, uint mouseData, point point)

Valeur positive indiquant que la roue a été pivotée vers l’avant, en dehors de l’utilisateur; une valeur négative indique que la roue a été pivotée vers l’arrière, pour l’utilisateur. Un clic sur un seul volant définit en tant que WHEEL_DELTA, soit 120. Si eventKind est CoreWebView2MouseEventKind. XButtonDoubleClick CoreWebView2MouseEventKind. XButtonDown ou CoreWebView2MouseEventKind. XButtonUp, mouseData indique quels boutons X ont été pressés ou relâchements. Cette valeur doit être 1 si le premier bouton X est appuyé sur/officialisé et 2 si le second bouton X est enfoncé/officialisé. Si eventKind est CoreWebView2MouseEventKind. Leave, virtualKeys, mouseData et point doivent tous être zéro. Si eventKind est une autre valeur, mouseData doit être zéro. Le point est censé figurer dans l’espace de coordonnées client du WebView. Pour effectuer le suivi des événements de souris qui démarrent dans le WebView et qui peuvent être déplacés en dehors de l’application WebView et hôte, il est recommandé d’appeler SetCapture et ReleaseCapture. Pour faire disparaître les fenêtres de survol, il est également recommandé d’envoyer WM_MOUSELEAVE messages.

#### SendPointerInput 

SendPointerInput accepte les entrées de pointeur en forme d’effleurement ou de stylet définies dans CoreWebView2PointerEventKind.

> public void [SendPointerInput](#sendpointerinput)([CoreWebView2PointerEventKind](./namespace-microsoft-web-webview2-core.md) EventType; [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) pointerInfo)

Toute entrée de pointeur à partir du système doit d’abord être convertie en CoreWebView2ExperimentalPointerInfo.
