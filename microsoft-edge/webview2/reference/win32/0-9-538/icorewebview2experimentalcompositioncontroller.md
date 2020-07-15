---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: WebView2 C++ Win32 ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2ExperimentalCompositionController
ms.openlocfilehash: e2b16cfd9095d43eb01d7e6233da2857c12a04ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880030"
---
# interface ICoreWebView2ExperimentalCompositionController 

> [!NOTE]
> Cette API expérimentale qui est fournie avec notre version bêta du SDK version 0.9.538.

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

Cette interface est une extension de l’interface ICoreWebView2Controller pour prendre en charge l’hébergement visuel.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[add_CursorChanged](#add_cursorchanged) | Ajoutez un gestionnaire d’événements pour l’événement CursorChanged.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Fonction d’assistance permettant de convertir un pointerId reçu du système en [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).
[get_Cursor](#get_cursor) | Le curseur actuel attendu par le WebView devrait être.
[get_RootVisualTarget](#get_rootvisualtarget) | Le RootVisualTarget est un élément visuel de l’arborescence visuelle de l’application hôte.
[get_UIAProvider](#get_uiaprovider) | Renvoie le fournisseur UI Automation pour le WebView.
[put_RootVisualTarget](#put_rootvisualtarget) | Définissez la propriété RootVisualTarget.
[remove_CursorChanged](#remove_cursorchanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_CursorChanged.
[SendMouseInput](#sendmouseinput) | Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData spécifie la quantité de mouvement du volant.
[SendPointerInput](#sendpointerinput) | SendPointerInput accepte les entrées de pointeur en forme d’effleurement ou de stylet définies dans COREWEBVIEW2_POINTER_EVENT_KIND.
[COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4) | Matrice qui représente une transformation 3D.
[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) | Type d’événement de souris utilisé par SendMouseInput pour transmettre le type d’événement de souris envoyé à WebView.
[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) | Touches virtuelles d’événement de souris associées à une COREWEBVIEW2_MOUSE_EVENT_KIND pour SendMouseInput.
[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) | Type d’événement de pointeur utilisé par SendPointerInput pour transmettre le type d’événement de pointeur envoyé à WebView.

Un objet qui implémente l’interface ICoreWebView2ExperimentalCompositionController implémente également ICoreWebView2Controller. Les appelants peuvent utiliser ICoreWebView2Controller pour le redimensionnement, la visibilité, le focus, etc., puis utiliser ICoreWebView2ExperimentalCompositionController pour se connecter à une arborescence de composition et fournir des entrées destinées au WebView.

## Ses

#### add_CursorChanged 

Ajoutez un gestionnaire d’événements pour l’événement CursorChanged.

> [add_CursorChanged](#add_cursorchanged)par le biais du[mot de passe](icorewebview2experimentalcursorchangedeventhandler.md)

L’événement se déclenche lorsque WebView considère que le curseur doit être modifié. Par exemple, lorsque le curseur de la souris est actuellement le curseur par défaut, mais qu’il est alors déplacé sur du texte, il peut essayer de basculer vers le curseur IBeam.

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                       IUnknown* args) -> HRESULT {
                    HCURSOR cursor;
                    CHECK_FAILURE(sender->get_Cursor(&cursor));
                    SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    return S_OK;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### CreateCoreWebView2PointerInfoFromPointerId 

Fonction d’assistance permettant de convertir un pointerId reçu du système en [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).

> public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND FenêtreParent, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

FenêtreParent est le HWND qui contient le WebView. Il peut s’agir d’un HWND de l’arborescence HWND qui contient le WebView. Le COREWEBVIEW2_MATRIX_4X4 est la transformation de ce HWND vers le WebView. Le [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) renvoyé est utilisé dans SendPointerInfo. Le type de pointeur doit être PEN ou Touch, ou la fonction échoue.



#### get_Cursor 

Le curseur actuel attendu par le WebView devrait être.

> valeur publique HRESULT [get_Cursor](#get_cursor)(HCURSOR * Cursor)

Le curseur doit être défini dans WM_SETCURSOR through:: SetCursor ou défini sur le HWND parent/ancêtre correspondant du WebView via:: SetClassLongPtr. Le HCURSOR peut être retardée de sorte que CopyCursor/DestroyCursor est recommandé de conserver votre propre copie si vous ne faites pas immédiatement la définition du curseur.

#### get_RootVisualTarget 

Le RootVisualTarget est un élément visuel de l’arborescence visuelle de l’application hôte.

> [get_RootVisualTarget](#get_rootvisualtarget)publiques HRESULT (IUnknown * * cible)

Cet élément visuel est l’endroit où le WebView se connecte à son arborescence d’éléments visuels. L’application utilise cet élément visuel pour positionner le WebView dans l’application. L’application doit toujours utiliser la propriété Bounds pour redimensionner le WebView. La propriété RootVisualTarget peut être IDCompositionVisual ou Windows:: UI:: composition:: ContainerVisual. WebView va connecter son arborescence d’éléments visuels à l’élément visuel fourni avant de revenir à partir de la méthode setter de propriété. L’application doit valider sur son appareil définissant la propriété RootVisualTarget. La propriété RootVisualTarget prend en charge la valeur nullptr pour déconnecter le WebView de l’arborescence visuelle de l’application. 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### get_UIAProvider 

Renvoie le fournisseur UI Automation pour le WebView.

> [get_UIAProvider](#get_uiaprovider)par le biais du service public HRESULT

#### put_RootVisualTarget 

Définissez la propriété RootVisualTarget.

> [put_RootVisualTarget](#put_rootvisualtarget)par le biais du public HRESULT

#### remove_CursorChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_CursorChanged.

> [remove_CursorChanged](#remove_cursorchanged)par le biais du mot-clé public HRESULT

#### SendMouseInput 

Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL ou COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData spécifie la quantité de mouvement du volant.

> public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) VIRTUALKEYS, UInt32 mouseData, point point)

Valeur positive indiquant que la roue a été pivotée vers l’avant, en dehors de l’utilisateur; une valeur négative indique que la roue a été pivotée vers l’arrière, pour l’utilisateur. Un clic sur un seul volant définit en tant que WHEEL_DELTA, soit 120. Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN ou COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, mouseData spécifie les boutons X ayant été pressés ou relâchements. Cette valeur doit être 1 si le premier bouton X est appuyé sur/officialisé et 2 si le second bouton X est enfoncé/officialisé. Si eventKind est COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, virtualKeys, mouseData et point doivent tous être zéro. Si eventKind est une autre valeur, mouseData doit être zéro. Le point est censé figurer dans l’espace de coordonnées client du WebView. Pour effectuer le suivi des événements de souris qui démarrent dans le WebView et qui peuvent être déplacés en dehors de l’application WebView et hôte, il est recommandé d’appeler SetCapture et ReleaseCapture. Pour faire disparaître les fenêtres de survol, il est également recommandé d’envoyer WM_MOUSELEAVE messages. 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### SendPointerInput 

SendPointerInput accepte les entrées de pointeur en forme d’effleurement ou de stylet définies dans COREWEBVIEW2_POINTER_EVENT_KIND.

> public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * pointerInfo)

Toute entrée de pointeur à partir du système doit d’abord être convertie en [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) .

#### COREWEBVIEW2_MATRIX_4X4 

Matrice qui représente une transformation 3D.

> [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4) typedef

Cette transformation est utilisée pour calculer les coordonnées correctes lors de l’appel de CreateCoreWebView2PointerInfoFromPointerId. Ceci équivaut à une D2D1_MATRIX_4X4_F

#### COREWEBVIEW2_MOUSE_EVENT_KIND 

Type d’événement de souris utilisé par SendMouseInput pour transmettre le type d’événement de souris envoyé à WebView.

> énumération [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL            | Événement de défilement de la molette horizontale de la souris, WM_MOUSEHWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK            | Double-cliquez sur le bouton gauche de la souris, WM_LBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN            | Bouton gauche de la souris, WM_LBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP            | Bouton gauche de la souris, WM_LBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE            | Événement de départ de la souris, WM_MOUSELEAVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK            | Bouton du milieu cliquez deux fois sur événement de souris, WM_MBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN            | Bouton du milieu de la souris, WM_MBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP            | Bouton du milieu de la souris, WM_MBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE            | Événement de déplacement de la souris, WM_MOUSEMOVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK            | Cliquez deux fois sur le bouton droit de la souris, WM_RBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN            | Bouton droit de la souris, WM_RBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP            | Cliquez sur le bouton droit de la souris, WM_RBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL            | Événement de défilement de la roulette de la souris, WM_MOUSEWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK            | Premier ou deuxième bouton X Cliquez deux fois sur événement de souris, WM_XBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN            | Premier ou deuxième X boutons de la souris, WM_XBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP            | Premier ou deuxième X boutons vers le haut, WM_XBUTTONUP.

Les valeurs de l’énumération sont alignées avec les messages de fenêtre WM_ * correspondants.

#### COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS 

Touches virtuelles d’événement de souris associées à une COREWEBVIEW2_MOUSE_EVENT_KIND pour SendMouseInput.

> énumération [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE            | Aucune touche supplémentaire enfoncée.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON            | Le bouton gauche de la souris est enfoncé, MK_LBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON            | Le bouton droit de la souris est en bas, MK_RBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT            | La touche Maj est enfoncée, MK_SHIFT.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL            | Touche CTRL enfoncée, MK_CONTROL.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON            | Le bouton du milieu de la souris est en bas, MK_MBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1            | Le premier bouton X est en bas, MK_XBUTTON1.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2            | Le deuxième bouton X est en bas, MK_XBUTTON2.

Ces valeurs peuvent être combinées en un indicateur de bit si plusieurs touches virtuelles sont utilisées pour l’événement. Les valeurs de l’énumération sont alignées avec les touches de souris et de MK_ correspondantes.

#### COREWEBVIEW2_POINTER_EVENT_KIND 

Type d’événement de pointeur utilisé par SendPointerInput pour transmettre le type d’événement de pointeur envoyé à WebView.

> énumération [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE            | Correspond à WM_POINTERACTIVATE.
COREWEBVIEW2_POINTER_EVENT_KIND_DOWN            | Correspond à WM_POINTERDOWN.
COREWEBVIEW2_POINTER_EVENT_KIND_ENTER            | Correspond à WM_POINTERENTER.
COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE            | Correspond à WM_POINTERLEAVE.
COREWEBVIEW2_POINTER_EVENT_KIND_UP            | Correspond à WM_POINTERUP.
COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE            | Correspond à WM_POINTERUPDATE.

Les valeurs de l’énumération sont alignées avec les messages de fenêtre WM_POINTER * correspondants.

