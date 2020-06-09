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
ms.openlocfilehash: 1d221498312959efbc16204097eb81db65fd2a7b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698660"
---
# interface ICoreWebView2Controller 

```
interface ICoreWebView2Controller
  : public IUnknown
```

Cette interface est le propriétaire de l’objet CoreWebView2 et prend en charge le redimensionnement, l’affichage et le masquage, le focus, ainsi que d’autres fonctionnalités relatives à la fenêtre et à la composition.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.
[add_GotFocus](#add_gotfocus) | Ajoutez un gestionnaire d’événements pour l’événement GotFocus.
[add_LostFocus](#add_lostfocus) | Ajoutez un gestionnaire d’événements pour l’événement LostFocus.
[add_MoveFocusRequested](#add_movefocusrequested) | Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.
[Fermer](#close) | Ferme le WebView et nettoie l’instance de navigateur sous-jacente.
[get_Bounds](#get_bounds) | Les limites de l’affichage WebView.
[get_CoreWebView2](#get_corewebview2) | Obtient le CoreWebView2 associé à cet CoreWebView2Controller.
[get_IsVisible](#get_isvisible) | La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.
[get_ParentWindow](#get_parentwindow) | Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.
[get_ZoomFactor](#get_zoomfactor) | Facteur de zoom pour le WebView.
[MoveFocus](#movefocus) | Déplacer le focus sur le WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Il s’agit d’une notification distincte des limites qui indiquent à WebView son parent (ou n’importe quel ancêtre) déplacé.
[put_Bounds](#put_bounds) | Définissez la propriété Bounds.
[put_IsVisible](#put_isvisible) | Définissez la propriété IsVisible.
[put_ParentWindow](#put_parentwindow) | Définissez la fenêtre parente pour le WebView.
[put_ZoomFactor](#put_zoomfactor) | Définissez la propriété ZoomFactor.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.
[remove_GotFocus](#remove_gotfocus) | Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.
[remove_LostFocus](#remove_lostfocus) | Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Mettez à jour les propriétés de limites et de ZoomFactor en même temps.

Le CoreWebView2Controller possède CoreWebView2, et si toutes les références au CoreWebView2Controller disparaissent, le WebView sera fermé.

## Ses

#### add_AcceleratorKeyPressed 

Ajoutez un gestionnaire d’événements pour l’événement AcceleratorKeyPressed.

> [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)par le biais du[mot de passe](icorewebview2acceleratorkeypressedeventhandler.md)

AcceleratorKeyPressed se déclenche quand une touche d’accès rapide ou une touche de raccourci est enfoncée ou relâche lorsque le WebView est ciblé. Un raccourci est considéré comme un accélérateur s’il s’agit de l’un des éléments suivants:

1. Ctrl ou Alt est en cours de conservation ou

1. la touche appuyée ne correspond pas à un caractère. Quelques touches spécifiques ne sont jamais considérées comme des accélérateurs, comme Shift. La touche Échap est toujours considérée comme un accélérateur.

Les événements de touches répétées déclenchés suite à la fermeture de la clé entraînent également le déclenchement de cet événement. Vous pouvez les filtrer en vérifiant les arguments d’événements «KeyEventLParam ou PhysicalKeyStatus.

En mode fenêtre, ce gestionnaire d’événements est appelé de manière synchrone. Tant que vous n’avez pas appelé handle () sur les arguments d’événement ou que le gestionnaire d’événements renvoie, le processus de navigateur sera bloqué et les appels COM entre processus entrants échoueront avec RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Toutes les méthodes de l’API CoreWebView2 fonctionneront toutefois.

En mode sans fenêtre, le gestionnaire d’événements est appelé de manière asynchrone. L’entrée supplémentaire n’atteint pas le navigateur tant que le gestionnaire d’événements n’a pas renvoyé ou que le gestionnaire d’événements n’est pas appelé, mais que le processus du navigateur proprement dit ne sera pas bloqué et que les appels COM sortants fonctionneront normalement.

Il est recommandé d’appeler handle (vrai) dès que vous en savez que vous voulez gérer la touche accélérateur.

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### add_GotFocus 

Ajoutez un gestionnaire d’événements pour l’événement GotFocus.

> [add_GotFocus](#add_gotfocus)par le biais du[mot de passe](icorewebview2focuschangedeventhandler.md)

GotFocus se déclenche lorsque WebView a le focus.

#### add_LostFocus 

Ajoutez un gestionnaire d’événements pour l’événement LostFocus.

> [add_LostFocus](#add_lostfocus)par le biais du[mot de passe](icorewebview2focuschangedeventhandler.md)

LostFocus se déclenche lorsque WebView perd le focus. Dans le cas où l’événement MoveFocusRequested est déclenché, le focus est toujours sur le WebView lors du déclenchement de l’événement MoveFocusRequested. Le focus perdu ne se déclenche que lorsque le code de l’application ou l’action par défaut de l’événement MoveFocusRequested a défini le focus hors du WebView.

#### add_MoveFocusRequested 

Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.

> [add_MoveFocusRequested](#add_movefocusrequested)par le biais du[mot de passe](icorewebview2movefocusrequestedeventhandler.md)

MoveFocusRequested est déclenché lorsque l’utilisateur tente d’accéder à l’onglet du WebView. Le focus du WebView n’a pas changé lors du déclenchement de cet événement.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### add_ZoomFactorChanged 

Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.

> [add_ZoomFactorChanged](#add_zoomfactorchanged)par le biais du[mot de passe](icorewebview2zoomfactorchangedeventhandler.md)

L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change. L’événement peut être déclenché en raison du fait que l’appelant a modifié la propriété ZoomFactor, ou en raison de l’utilisateur modifiant manuellement le zoom. Lorsqu’il est modifié par l’appelant par le biais de la propriété ZoomFactor, le facteur de zoom interne est mis à jour immédiatement et il n’y a pas d’événement ZoomFactorChanged. WebView associe le dernier facteur de zoom utilisé pour chaque site. Par conséquent, il est possible de modifier le facteur de zoom lorsque vous naviguez vers une autre page. Lorsque le facteur de zoom change en raison de cela, l’événement ZoomFactorChanged se déclenche immédiatement après l’événement ContentLoading.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### Fermer 

Ferme le WebView et nettoie l’instance de navigateur sous-jacente.

> valeur publique [HRESULT (](#close))

Le nettoyage de l’instance du navigateur entraîne la libération des ressources du WebView. L’instance du navigateur sera arrêtée s’il n’y a aucune autre WebView.

Après avoir appelé Close, tous les appels de méthode échouent et les gestionnaires d’événements cessent de se déclencher. Plus précisément, le WebView publie ses références à ses gestionnaires d’événements lorsque la méthode Close est appelée.

Close est appelé implicitement lorsque CoreWebView2Controller perd sa référence finale et est détruit. Mais il est conseillé d’appeler explicitement Close pour éviter tout cycle accidentel de références entre le WebView et le code de l’application. En particulier, si vous capturez une référence à WebView dans un gestionnaire d’événements, vous créerez un cycle de référence entre le WebView et le gestionnaire d’événements. L’appel de la fermeture rompt ce cycle en libérant tous les gestionnaires d’événements. Néanmoins, pour éviter ce problème, il est préférable d’appeler explicitement l’application WebView et de ne pas capturer de référence à WebView pour s’assurer que le WebView peut être nettoyé correctement.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/webview2/reference/win32/0-9-538/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### get_Bounds 

Les limites de l’affichage WebView.

> [get_Boundss](#get_bounds)par le biais du public HRESULT

Les limites sont relatives au HWND parent. L’application peut positionner un WebView de deux manières:

1. Créer un HWND enfant qui est le HWND parent WebView. Positionnez cette fenêtre dans laquelle le WebView devrait être. Dans le cas présent, utilisez (0, 0) pour le coin supérieur gauche de la vue de Bound’s (offset).

1. Utilisez la plus grande fenêtre de l’application en tant que HWND parent d’affichage. Définissez le coin supérieur gauche de l’Bound’s WebView de sorte que le contrôle WebView soit correctement positionné dans l’application. Les valeurs de limites se trouvent dans l’espace de coordonnées de l’hôte.

#### get_CoreWebView2 

Obtient le CoreWebView2 associé à cet CoreWebView2Controller.

> [get_CoreWebView2](#get_corewebview2)par le biais du public HRESULT ([ICoreWebView2](icorewebview2.md) * * CoreWebView2)

#### get_IsVisible 

La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.

> valeur publique HRESULT [get_IsVisible](#get_isvisible)(bool * IsVisible)

Si la valeur de l’argument IsVisible est définie sur false, le WebView sera transparent et ne sera pas affiché. Toutefois, cela n’affecte pas la fenêtre qui contient le WebView (le paramètre HWND transmis à CreateCoreWebView2Controller). Si vous souhaitez que cette fenêtre disparaisse également, appelez la fonction ShowWindow sur celle-ci directement en plus de modifier la propriété IsVisible. Le mode webaffichage sous forme de fenêtre enfant ne recevra pas de messages de fenêtre lorsque la fenêtre supérieure est réduite ou restaurée. Pour des raisons de performances, le développeur doit définir la propriété IsVisible du WebView sur false lorsque la fenêtre de l’application est réduite, puis revenir à la valeur true lorsque la fenêtre de l’application est restaurée. Pour cela, la fenêtre de l’application peut gérer les SC_MINIMIZE et de SC_RESTORE commande lors de la réception d’WM_SYSCOMMAND message.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### get_ParentWindow 

Fenêtre parent fournie par l’application utilisée par ce WebView pour afficher le contenu.

> valeur publique HRESULT [get_ParentWindow](#get_parentwindow)(HWND * topLevelWindow)

Cette API renvoie initialement la fenêtre transmise à CreateCoreWebView2Controller.

#### get_ZoomFactor 

Facteur de zoom pour le WebView.

> valeur publique HRESULT [get_ZoomFactor](#get_zoomfactor)(double * ZoomFactor)

Notez que la modification du facteur de zoom peut entraîner la modification de la `window.innerWidth/innerHeight` mise en page. Le facteur de zoom appliqué par l’hôte en appelant ZoomFactor devient le nouveau zoom par défaut de l’affichage WebView. Ce facteur de zoom s’applique aux différentes navigations et le facteur de zoom est renvoyé lorsque l’utilisateur appuie sur Ctrl + 0. Lorsque le facteur de zoom est modifié par l’utilisateur (ce qui permet à l’application de recevoir ZoomFactorChanged), ce zoom s’applique uniquement à la page active. Tout zoom appliqué à un utilisateur est réservé uniquement à la page active et est réinitialisé sur une navigation. La spécification d’un zoomFactor inférieur ou égal à 0 n’est pas autorisée. WebView possède également une plage de facteur de zoom prise en charge interne. Lorsque le facteur de zoom spécifié est en dehors de cette plage, il est normalisé pour être dans la plage et un événement ZoomFactorChanged est déclenché pour le facteur de zoom réel appliqué. Lorsque cette situation se produit, la propriété ZoomFactor indique le facteur de zoom spécifié lors de la modification précédente de la propriété ZoomFactor jusqu’à ce que l’événement ZoomFactorChanged soit reçu lorsque WebView applique le facteur de zoom normalisé.

#### MoveFocus 

Déplacer le focus sur le WebView.

> public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON raison)

WebView va mettre le focus et le focus sur l’élément correspondant dans la page hébergée dans le WebView. Pour des raisons de programmation, le focus est défini sur l’élément précédemment prioritaire ou l’élément par défaut s’il n’y a pas d’élément prioritaire auparavant. Pour une raison suivante, le focus est défini sur le premier élément. Pour une raison précédente, le focus est défini sur le dernier élément. Le mode webaffichage peut également mettre le focus sur une interaction utilisateur telle que cliquer sur le WebView ou sur Tab. Pour la fonction de tabulation, l’application peut appeler MoveFocus avec Next ou Previous pour s’aligner sur TAB et Maj + Tab lorsqu’elle décide que le WebView est l’élément tabbable suivant. Par exemple, l’application peut appeler IsDialogMessage dans le cadre de sa boucle de messages pour permettre à la plateforme de gérer automatiquement la tabulation. La plateforme est pivotée sur toutes les fenêtres avec WS_TABSTOP. Lorsque le WebView obtient le focus de IsDialogMessage, il positionne en interne le focus sur le premier ou le dernier élément de Tab et Maj + Tab respectivement.

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### NotifyParentWindowPositionChanged 

Il s’agit d’une notification distincte des limites qui indiquent à WebView son parent (ou n’importe quel ancêtre) déplacé.

> public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Cela est nécessaire pour l’accessibilité et certaines boîtes de dialogue dans WebView pour fonctionner correctement. 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### put_Bounds 

Définissez la propriété Bounds.

> [put_Bounds](#put_bounds)par le biais du public HRESULT

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### put_IsVisible 

Définissez la propriété IsVisible.

> valeur HRESULT publique [put_IsVisible](#put_isvisible)(bool IsVisible)

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### put_ParentWindow 

Définissez la fenêtre parente pour le WebView.

> [put_ParentWindow](#put_parentwindow)par le biais du public HRESULT

Cela a pour effet de refaire de la fenêtre de l’affichage de nouveau dans la fenêtre qui vient d’être fournie.

#### put_ZoomFactor 

Définissez la propriété ZoomFactor.

> [put_ZoomFactor](#put_zoomfactor)par le biais du public HRESULT (double ZoomFactor)

#### remove_AcceleratorKeyPressed 

Supprimez un gestionnaire d’événements préalablement ajouté à add_AcceleratorKeyPressed.

> [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)par le biais du mot-clé public HRESULT

#### remove_GotFocus 

Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.

> [remove_GotFocus](#remove_gotfocus)par le biais du mot-clé public HRESULT

#### remove_LostFocus 

Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.

> [remove_LostFocus](#remove_lostfocus)par le biais du mot-clé public HRESULT

#### remove_MoveFocusRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.

> [remove_MoveFocusRequested](#remove_movefocusrequested)par le biais du mot-clé public HRESULT

#### remove_ZoomFactorChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.

> [remove_ZoomFactorChanged](#remove_zoomfactorchanged)par le biais du mot-clé public HRESULT

#### SetBoundsAndZoomFactor 

Mettez à jour les propriétés de limites et de ZoomFactor en même temps.

> public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(limites de Rect, double ZoomFactor)

Cette opération est atomique du point de vue de l’hôte. Après avoir retourné la fonction, les limites et les propriétés ZoomFactor ont été mises à jour si la fonction est réussie, ou ne sont pas mises à jour en cas d’échec de la fonction. Si les limites et ZoomFactor sont toutes deux mises à jour par la même échelle (c’est-à-dire que les limites et ZoomFactor sont tous deux doublées), la page ne verra aucune modification apportée à Window. innerWidth/innerHeight et le WebView fera apparaître le contenu aux nouvelles tailles et zooms sans rendu intermédiaire. Cette fonction peut également être utilisée pour mettre à jour une seule de ZoomFactor ou de limites en passant la nouvelle valeur pour une et la valeur actuelle pour l’autre.

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```

