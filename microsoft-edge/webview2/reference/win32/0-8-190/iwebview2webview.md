---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.8.355-WebView2 C++ Win32 IWebView2WebView
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 7ef58d19bc5284a3e71dc8be16f3865239047a10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878119"
---
# 0.8.355-interface IWebView2WebView 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2WebView
  : public IUnknown
```

WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | L’objet [IWebView2Settings](IWebView2Settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.
[get_Source](#get_source) | URI du document de niveau supérieur actuel.
[Rechercher](#navigate) | Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.
[MoveFocus](#movefocus) | Déplacer le focus sur le WebView.
[NavigateToString](#navigatetostring) | Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.
[add_NavigationStarting](#add_navigationstarting) | Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.
[add_DocumentStateChanged](#add_documentstatechanged) | Ajoutez un gestionnaire d’événements pour l’événement DocumentStateChanged.
[remove_DocumentStateChanged](#remove_documentstatechanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentStateChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.
[add_MoveFocusRequested](#add_movefocusrequested) | Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.
[add_GotFocus](#add_gotfocus) | Ajoutez un gestionnaire d’événements pour l’événement GotFocus.
[remove_GotFocus](#remove_gotfocus) | Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.
[add_LostFocus](#add_lostfocus) | Ajoutez un gestionnaire d’événements pour l’événement LostFocus.
[remove_LostFocus](#remove_lostfocus) | Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.
[add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated) | Cette API est déconseillée, utilisez la nouvelle API add_WebResourceRequested.
[remove_WebResourceRequested](#remove_webresourcerequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.
[add_PermissionRequested](#add_permissionrequested) | Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Supprimez le JavaScript correspondant ajouté par le biais de AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.
[CapturePreview](#capturepreview) | Capturez une image de l’affichage du WebView.
[Recharger](#reload) | Recharger la page active.
[get_Bounds](#get_bounds) | Les limites de l’affichage WebView.
[put_Bounds](#put_bounds) | Définissez la propriété Bounds.
[get_ZoomFactor](#get_zoomfactor) | Facteur de zoom pour la page active dans le WebView.
[put_ZoomFactor](#put_zoomfactor) | Définissez la propriété ZoomFactor.
[get_IsVisible](#get_isvisible) | La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.
[put_IsVisible](#put_isvisible) | Définissez la propriété IsVisible.
[PostWebMessageAsJson](#postwebmessageasjson) | Publiez le WebMessage spécifié dans le document de niveau supérieur de cette [IWebView2WebView]().
[PostWebMessageAsString](#postwebmessageasstring) | Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.
[Fermer](#close) | Ferme le WebView et nettoie l’instance de navigateur sous-jacente.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Appelez une méthode DevToolsProtocol asynchrone.
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | S’abonner à un événement DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.
[get_BrowserProcessId](#get_browserprocessid) | ID de processus du processus de navigation qui héberge le WebView.
[get_CanGoBack](#get_cangoback) | Peut parcourir le WebView vers la page précédente de l’historique de navigation.
[get_CanGoForward](#get_cangoforward) | Peut parcourir le WebView sur la page suivante de l’historique de navigation.
[GoBack](#goback) | Permet d’accéder à la page précédente de l’historique de navigation via le WebView.
[GoForward](#goforward) | Navigue vers la page suivante de l’historique de navigation du WebView.
[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) | Format d’image utilisé par la méthode [IWebView2WebView:: CapturePreview](#capturepreview) .
[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) | Type de boîte de dialogue JavaScript utilisée dans l’interface [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .
[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) | Type d’échec de processus utilisé dans l’interface [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .
[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) | Le type d’une demande d’autorisation.
[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) | Réponse à une demande d’autorisation.
[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) | Raison du déplacement du focus.
[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) | Valeurs d’état d’erreur pour les navigations Web.
[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) | Énum pour les contextes de demande de ressources Web.

## Événements de navigation

L’ordre normal des événements de navigation est NavigationStarting, DocumentStateChanged, puis NavigationCompleted.

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

Notez qu’il s’agit d’événements de navigation avec le même argument d’événement NavigationId. Les événements de navigation avec différents arguments d’événement NavigationId risquent de se chevaucher. Par exemple, si vous démarrez une navigation pour l’événement NavigationStarting, puis démarrez une autre navigation, vous verrez le NavigationStarting de la première navigation suivi par le NavigationStarting du deuxième navigation, suivi de l’NavigationCompleted de la première navigation, puis de tout le reste des événements de navigation appropriés pour la deuxième navigation. Dans les cas d’erreur, il est possible ou non qu’un événement DocumentStateChanged se poursuive sur une page d’erreur. Dans le cas d’une redirection HTTP, plusieurs événements NavigationStarting sont disponibles dans une ligne, avec les indicateurs IsRedirect définis dans le premier.

Dans le cas de sous-trames dans WebView, le seul événement de navigation déclenché est l’événement NavigationStarting qui donne à l’hôte la possibilité de bloquer les navigations de sous-bloc.

## Modèle de processus

WebView2 utilise le même modèle de processus que le navigateur Web Edge. Il existe un processus de navigateur Edge par répertoire de données utilisateur spécifié dans une session utilisateur qui traitera tout processus appelant WebView2 spécifiant ce répertoire de données utilisateur. Cela signifie qu’un processus de navigateur Edge est susceptible de traiter plusieurs processus d’appel et qu’un processus d’appel est susceptible d’utiliser plusieurs processus de navigation latérale.

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

Il y a un certain nombre de processus de convertisseur. Celles-ci sont créées autant de fois que nécessaire pour traiter plusieurs trames dans différents affichages. Le nombre de processus de rendu varie en fonction de la fonctionnalité du navigateur d’isolement de site et du nombre d’origines distantes distinctes affichées dans les webvues associées.

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

Vous pouvez réagir aux blocages et se bloquer dans ces processus de navigateur et de convertisseur à l’aide de l’événement ProcessFailure.

Vous pouvez arrêter en toute sécurité les processus de navigateur et de convertisseur associés à l’aide de la méthode Close.

## Modèle de threads

WebView2 doit être créé sur un thread d’interface utilisateur. Particulièrement un thread avec une pompe de messages. Tous les rappels se produiront sur ce thread et les appels dans le WebView doivent être effectués sur ce thread. Il n’est pas sûr d’utiliser le WebView à partir d’un autre thread.

Les rappels incluant des gestionnaires d’événements et des gestionnaires d’achèvement s’exécutent en série. Autrement dit, si vous disposez d’un gestionnaire d’événements et commencez une boucle de message, il n’y a pas de gestionnaires d’événements ou de rappels d’achèvement.

## Sécurité

Vérifiez toujours la propriété source de WebView avant d’utiliser ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString, ou toute autre méthode pour envoyer des informations dans le WebView. Le WebView peut avoir navigué vers une autre page par le biais de l’utilisateur final qui interagit avec la page ou le script de la page entraînant la navigation. De même, soyez prudent avec AddScriptToExecuteOnDocumentCreated. Toutes les futures navigations exécuteront ce script et, s’il donne accès à des informations destinées uniquement à un certain type d’origine, tous les documents HTML peuvent avoir accès.

Lorsque vous examinez le résultat d’un appel de méthode ExecuteScript, un événement WebMessageReceived, vérifie toujours la source de l’expéditeur ou tout autre mécanisme de réception d’informations à partir d’un document HTML dans un WebView valide l’URI du document HTML correspond à ce que vous attendez.

Lorsque vous construisez un message à envoyer dans un WebView, préférez utilisez PostWebMessageAsJson et construisez le paramètre de chaîne JSON à l’aide d’une bibliothèque JSON. Cela évite les accidents potentiels d’encoder des informations dans une chaîne ou un script JSON et garantir qu’aucune entrée contrôlée par l’attaquant ne peut modifier le reste du message JSON ou exécuter un script arbitraire.

## Types de chaîne

Les paramètres de type chaîne sont des chaînes de type LPWSTR nul terminées. Le l’appelant alloue la chaîne à l’aide de CoTaskMemAlloc. La propriété est transférée à l’appelant et il revient à l’appelant de libérer de la mémoire à l’aide de CoTaskMemFree.

La chaîne figurant dans les paramètres est LPCWSTRe des chaînes arrêtées null. L’appelant vérifie que la chaîne est valide pour la durée de l’appel de fonction synchrone. Si les appelants doivent conserver cette valeur à un certain point après la fin de l’appel de fonction, l’appelant doit allouer sa propre copie de la valeur de chaîne.

## D’analyse des URI et de JSON

Diverses méthodes fournissent ou acceptent des URI et JSON en tant que chaînes. Utilisez votre propre bibliothèque préférée pour analyser et générer ces chaînes.

Si WinRT est disponible pour votre application, vous pouvez l’utiliser `RuntimeClass_Windows_Data_Json_JsonObject` et `IJsonObjectStatics` analyser ou générer des chaînes JSON ou `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` analyser et générer des URI. Ces deux fonctions fonctionnent dans les applications Win32.

Si vous utilisez IUri et CreateUri pour analyser les URI, il est possible que vous souhaitiez utiliser les indicateurs de création d’URI suivants pour que le comportement CreateUri correspond plus étroitement à l’analyse d’URI dans le WebView: `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## Débogage

Ouvrez DevTools avec les raccourcis normaux: `F12` ou `Ctrl+Shift+I` . Vous pouvez utiliser le `--auto-open-devtools-for-tabs` commutateur d’argument de commande pour que la fenêtre devtools s’ouvre immédiatement lors de la création d’un WebView. Pour plus d’informations sur le processus de navigation, voir documentation CreateWebView. Consultez la clé de Registre LoaderOverride pour essayer différentes builds de WebView2 sans modifier votre application dans la documentation CreateWebView.

## Contrôle de version

Une fois que vous avez utilisé une version particulière du SDK pour générer votre application, l’exécution de votre application avec une version plus ancienne ou plus récente des fichiers binaires de navigateur installés sera terminée. Jusqu’à la version 1.0.0.0 de WebView2, des modifications peuvent être apportées lors des mises à jour qui empêchent votre SDK de fonctionner avec des versions différentes des fichiers binaires de navigateur installés. Après la version 1.0.0.0, vous pouvez utiliser les différentes versions du kit de développement logiciel (SDK) pour travailler avec les meilleures pratiques suivantes:

Pour prendre en compte les modifications apportées à l’API, veillez à vérifier l’échec lors de l’appel de la DLL d’exportation CreateWebView2Environment et lors de l’appel de QueryInterface sur un objet WebView2. La valeur de retour de E_NOINTERFACE peut indiquer que le kit de développement logiciel (SDK) n’est pas compatible avec les fichiers binaires de navigation Edge.

La vérification de l’échec de QueryInterface sera également comptabilisée dans les cas où le kit de développement logiciel (SDK) est plus récent que la version du navigateur Edge et que votre application tente d’utiliser une interface qui n’est pas compatible avec le navigateur Edge.

Lorsqu’une interface n’est pas disponible, vous pouvez envisager de désactiver la fonctionnalité associée le cas échéant ou d’informer l’utilisateur final qu’il doit mettre à jour son navigateur.

## Ses

#### get_Settings 

L’objet [IWebView2Settings](IWebView2Settings.md) contient différents paramètres modifiables pour le WebView en cours d’exécution.

> valeurs publiques HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) * *)

#### get_Source 

URI du document de niveau supérieur actuel.

> valeur publique HRESULT [get_Source](#get_source)(LPWSTR * URI)

Cette valeur peut changer dans le cadre du déclenchement de l’événement DocumentStateChanged, dans certains cas, par exemple, la navigation vers un site ou un fragment de navigation différent. Il restera identique pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### Rechercher 

Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.

> public HRESULT [Navigate](#navigate)(Uri LPCWSTR)

Pour plus d’informations, voir événements de navigation. Notez que cela démarre une navigation et que l’événement NavigationStarting correspondant est déclenché après la fin de l’appel.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### MoveFocus 

Déplacer le focus sur le WebView.

> public HRESULT [MoveFocus](#movefocus)([WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) raison)

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
            for (int i = 0; i < m_tabbableWindows.size(); i++)
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
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
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
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### NavigateToString 

Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.

> public HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)

Le paramètre htmlContent ne doit pas comporter plus de 2 Mo de caractères. L’origine de la nouvelle page va être vide.

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### add_NavigationStarting 

Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.

> [add_NavigationStarting](#add_navigationstarting)par le biais du[mot de passe](IWebView2NavigationStartingEventHandler.md)

NavigationStarting se déclenche lorsque le frame principal WebView demande une autorisation pour accéder à un URI différent. Cela se déclenche également pour les redirections.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### remove_NavigationStarting 

Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.

> [remove_NavigationStarting](#remove_navigationstarting)par le biais du mot-clé public HRESULT

#### add_DocumentStateChanged 

Ajoutez un gestionnaire d’événements pour l’événement DocumentStateChanged.

> [add_DocumentStateChanged](#add_documentstatechanged)par le biais du[mot de passe](IWebView2DocumentStateChangedEventHandler.md)

DocumentStateChanged est déclenché lorsqu’un nouveau contenu a commencé à se charger sur l’image principale du WebView ou si une même navigation de page se produit (par exemple par le biais des navigations par fragments ou de l’historique. pushState). Cela suit l’événement NavigationStarting et précède l’événement NavigationCompleted.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### remove_DocumentStateChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentStateChanged.

> [remove_DocumentStateChanged](#remove_documentstatechanged)par le biais du mot-clé public HRESULT

#### add_NavigationCompleted 

Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.

> [add_NavigationCompleted](#add_navigationcompleted)par le biais du[mot de passe](IWebView2NavigationCompletedEventHandler.md)

L’événement NavigationCompleted se déclenche lorsque le WebView est complètement chargé (le corps. OnLoad a été déclenché) ou que le chargement s’est arrêté avec une erreur.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### remove_NavigationCompleted 

Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.

> [remove_NavigationCompleted](#remove_navigationcompleted)par le biais du mot-clé public HRESULT

#### add_FrameNavigationStarting 

Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.

> [add_FrameNavigationStarting](#add_framenavigationstarting)par le biais du[mot de passe](IWebView2NavigationStartingEventHandler.md)

FrameNavigationStarting se déclenche quand une Frame enfant du WebView demande une autorisation pour accéder à un URI différent. Cela se déclenche également pour les redirections.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### remove_FrameNavigationStarting 

Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.

> [remove_FrameNavigationStarting](#remove_framenavigationstarting)par le biais du mot-clé public HRESULT

#### add_MoveFocusRequested 

Ajoutez un gestionnaire d’événements pour l’événement MoveFocusRequested.

> [add_MoveFocusRequested](#add_movefocusrequested)par le biais du[mot de passe](IWebView2MoveFocusRequestedEventHandler.md)

MoveFocusRequested est déclenché lorsque l’utilisateur tente d’accéder à l’onglet du WebView. Le focus du WebView n’a pas changé lors du déclenchement de cet événement.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
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

#### remove_MoveFocusRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_MoveFocusRequested.

> [remove_MoveFocusRequested](#remove_movefocusrequested)par le biais du mot-clé public HRESULT

#### add_GotFocus 

Ajoutez un gestionnaire d’événements pour l’événement GotFocus.

> [add_GotFocus](#add_gotfocus)par le biais du[mot de passe](IWebView2FocusChangedEventHandler.md)

GotFocus se déclenche lorsque WebView a le focus.

#### remove_GotFocus 

Supprimez un gestionnaire d’événements préalablement ajouté à add_GotFocus.

> [remove_GotFocus](#remove_gotfocus)par le biais du mot-clé public HRESULT

#### add_LostFocus 

Ajoutez un gestionnaire d’événements pour l’événement LostFocus.

> [add_LostFocus](#add_lostfocus)par le biais du[mot de passe](IWebView2FocusChangedEventHandler.md)

LostFocus se déclenche lorsque WebView perd le focus. Dans le cas où l’événement MoveFocusRequested est déclenché, le focus est toujours sur le WebView lors du déclenchement de l’événement MoveFocusRequested. Le focus perdu ne se déclenche que lorsque le code de l’application ou l’action par défaut de l’événement MoveFocusRequested a défini le focus hors du WebView.

#### remove_LostFocus 

Supprimez un gestionnaire d’événements préalablement ajouté à add_LostFocus.

> [remove_LostFocus](#remove_lostfocus)par le biais du mot-clé public HRESULT

#### add_WebResourceRequested_deprecated 

Cette API est déconseillée, utilisez la nouvelle API add_WebResourceRequested.

> valeur de HRESULT publique [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR * constante urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) * constante resourceContextFilter, size_t filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * EventHandler, EventRegistrationToken * jeton)

Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested. Se déclenche lorsque le WebView effectue une requête HTTP. Utilisez urlFilter pour transmettre une liste avec la taille filterLength d’URL à écouter. Chaque entrée d’URL prend également en charge les caractères génériques: ' * 'correspond à zéro, un ou plusieurs caractères et «?» correspond exactement à un caractère. Pour chaque entrée de urlFilter, fournissez un resourceContextFilter correspondant qui représente les types de ressources pour lesquels WebResourceRequested doit se déclencher. Si filterLength est 0, l’événement est déclenché pour toutes les requêtes réseau. Les contextes de ressources pris en charge sont les suivants: document, StyleSheet, image, multimédia, police, script, XHR, Fetch.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### remove_WebResourceRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.

> [remove_WebResourceRequested](#remove_webresourcerequested)par le biais du mot-clé public HRESULT

#### add_ScriptDialogOpening 

Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.

> [add_ScriptDialogOpening](#add_scriptdialogopening)par le biais du[mot de passe](IWebView2ScriptDialogOpeningEventHandler.md)

L’événement se déclenche quand une boîte de dialogue JavaScript (alerte, confirmation ou invite) s’affiche pour le WebView. Cet événement est déclenché uniquement si la propriété IWebView2Settings:: AreDefaultScriptDialogsEnabled est définie sur false.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### remove_ScriptDialogOpening 

Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.

> [remove_ScriptDialogOpening](#remove_scriptdialogopening)par le biais du mot-clé public HRESULT

#### add_ZoomFactorChanged 

Ajoutez un gestionnaire d’événements pour l’événement ZoomFactorChanged.

> [add_ZoomFactorChanged](#add_zoomfactorchanged)par le biais du[mot de passe](IWebView2ZoomFactorChangedEventHandler.md)

L’événement se déclenche lorsque la propriété ZoomFactor de l’élément WebView change. L’événement peut être déclenché en raison du fait que l’appelant a modifié la propriété ZoomFactor, ou en raison de l’utilisateur modifiant manuellement le zoom. Lorsqu’il est modifié par l’appelant par le biais de la propriété ZoomFactor, le facteur de zoom interne est mis à jour immédiatement et il n’y a pas d’événement ZoomFactorChanged. WebView associe le dernier facteur de zoom utilisé pour chaque site. Par conséquent, il est possible de modifier le facteur de zoom lorsque vous naviguez vers une autre page. Lorsque le facteur de zoom change en raison de cela, l’événement ZoomFactorChanged se déclenche immédiatement après l’événement DocumentStateChanged.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
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

#### remove_ZoomFactorChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_ZoomFactorChanged.

> [remove_ZoomFactorChanged](#remove_zoomfactorchanged)par le biais du mot-clé public HRESULT

#### add_PermissionRequested 

Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.

> [add_PermissionRequested](#add_permissionrequested)par le biais du[mot de passe](IWebView2PermissionRequestedEventHandler.md)

Se déclenche lorsque le contenu d’un WebView demande l’autorisation d’accéder à des ressources privilégiées.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.

> [remove_PermissionRequested](#remove_permissionrequested)par le biais du mot-clé public HRESULT

#### add_ProcessFailed 

Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.

> [add_ProcessFailed](#add_processfailed)par le biais du[mot de passe](IWebView2ProcessFailedEventHandler.md)

Se déclenche quand un processus WebView s’est arrêté de manière inattendue ou ne répond plus.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### remove_ProcessFailed 

Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.

> [remove_ProcessFailed](#remove_processfailed)par le biais du mot-clé public HRESULT

#### AddScriptToExecuteOnDocumentCreated 

Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.

> public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, gestionnaire[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) *)

Le script injecté s’applique à tous les futurs documents de niveau supérieur et navigation de Frame enfant jusqu’à sa suppression avec RemoveScriptToExecuteOnDocumentCreated. Cette opération est appliquée de manière asynchrone et vous devez attendre que le gestionnaire d’achèvement s’exécute avant de vérifier que le script est prêt à être exécuté sur de futurs navigations.

Notez que si un document HTML comporte un sandbox d’un type quelconque via les propriétés [sandbox](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) ou l' [en-tête HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , ce dernier affectera l’exécution du script. Par exemple, si le mot clé «allow-modaux» n’est pas défini, les appels à la `alert` fonction seront ignorés.

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### RemoveScriptToExecuteOnDocumentCreated 

Supprimez le JavaScript correspondant ajouté par le biais de AddScriptToExecuteOnDocumentCreated.

> public HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ID LPCWSTR)

#### ExecuteScript 

Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.

> public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, gestionnaire[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) *)

Cela s’exécute de manière asynchrone et, si un gestionnaire est fourni dans le paramètre ExecuteScriptCompletedHandler, sa méthode Invoke est appelée avec le résultat de l’évaluation du JavaScript fourni. La valeur de résultat est une chaîne codée au format JSON. Si le résultat n’est pas défini, contient un cycle de référence ou ne peut pas être encodé dans JSON, la valeur null JSON sera renvoyée comme chaîne «NULL». Notez qu’une fonction qui ne contient aucune valeur de retour explicite renvoie une valeur non définie. Si le script exécuté lève une exception non gérée, le résultat est également «null». Cette méthode est appliquée de manière asynchrone. Si l’appel est effectué alors que le WebView est sur un document et qu’une navigation se produit après la fin de l’appel, mais avant l’exécution du JavaScript, le script ne sera pas exécuté et le gestionnaire sera appelé avec E_FAIL pour son paramètre codeerreur. ExecuteScript fonctionne même si IsScriptEnabled est défini sur FALSe.

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<IWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### CapturePreview 

Capturez une image de l’affichage du WebView.

> public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream * ImageStream, gestionnaire[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) *)

Spécifiez le format de l’image avec le paramètre imageFormat. Les données binaires d’image obtenues sont écrites dans le paramètre imageStream fourni. Lorsque CapturePreview finit d’écrire dans le flux, la méthode Invoke du paramètre de gestionnaire fourni est appelée.

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### Recharger 

Recharger la page active.

> [rechargement](#reload)du HRESULT public ()

Il s’agit de la même façon que d’accéder à l’URI du document de niveau supérieur actuel, y compris tous les événements de navigation déclenchant et respectant les entrées dans le cache HTTP. Toutefois, l’historique en arrière-plan ne sera pas modifié.

#### get_Bounds 

Les limites de l’affichage WebView.

> [get_Boundss](#get_bounds)par le biais du public HRESULT

Les limites sont relatives au HWND parent. L’application peut positionner un WebView de deux manières:

1. Créer un HWND enfant qui est le HWND parent WebView. Positionnez cette fenêtre dans laquelle le WebView devrait être. Dans le cas présent, utilisez (0, 0) pour le coin supérieur gauche de la vue de Bound’s (offset).

1. Utilisez la plus grande fenêtre de l’application en tant que HWND parent d’affichage. Définissez le coin supérieur gauche de l’Bound’s WebView de sorte que le contrôle WebView soit correctement positionné dans l’application. Les valeurs de limites se trouvent dans l’espace de coordonnées de l’hôte.

#### put_Bounds 

Définissez la propriété Bounds.

> [put_Bounds](#put_bounds)par le biais du public HRESULT

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### get_ZoomFactor 

Facteur de zoom pour la page active dans le WebView.

> valeur publique HRESULT [get_ZoomFactor](#get_zoomfactor)(double * ZoomFactor)

Le facteur de zoom est conservé par site. Notez que la modification du facteur de zoom peut entraîner la modification de la `window.innerWidth/innerHeight` mise en page. Lorsque WebView accède à une page d’un site différent, le facteur de zoom défini pour la page précédente ne sera pas appliqué. Si l’application veut définir le facteur de zoom pour une page spécifique, l’emplacement le plus ancien est le dans le gestionnaire d’événements DocumentStateChanged. Notez que, si tel est le cas, il peut recevoir un événement ZoomFactorChanged pour le facteur de zoom persistant avant de recevoir l’événement ZoomFactorChanged pour le facteur de zoom spécifié. La spécification d’un zoomFactor inférieur ou égal à 0 n’est pas autorisée. WebView possède également une plage de facteur de zoom prise en charge interne. Lorsque le facteur de zoom spécifié est en dehors de cette plage, il est normalisé pour être dans la plage et un événement ZoomFactorChanged est déclenché pour le facteur de zoom réel appliqué. Lorsque cette situation se produit, la propriété ZoomFactor indique le facteur de zoom spécifié lors de la modification précédente de la propriété ZoomFactor jusqu’à ce que l’événement ZoomFactorChanged soit reçu lorsque WebView applique le facteur de zoom normalisé.

#### put_ZoomFactor 

Définissez la propriété ZoomFactor.

> [put_ZoomFactor](#put_zoomfactor)par le biais du public HRESULT (double ZoomFactor)

#### get_IsVisible 

La propriété IsVisible détermine s’il faut afficher ou masquer le WebView.

> valeur publique HRESULT [get_IsVisible](#get_isvisible)(bool * IsVisible)

Si la valeur de l’argument IsVisible est définie sur false, le WebView sera transparent et ne sera pas affiché. Toutefois, cela n’affecte pas la fenêtre qui contient le WebView (le paramètre HWND transmis à CreateWebView). Si vous souhaitez que cette fenêtre disparaisse également, appelez la fonction ShowWindow sur celle-ci directement en plus de modifier la propriété IsVisible. Le mode webaffichage sous forme de fenêtre enfant ne recevra pas de messages de fenêtre lorsque la fenêtre supérieure est réduite ou restaurée. Pour des raisons de performances, le développeur doit définir la propriété IsVisible du WebView sur false lorsque la fenêtre de l’application est réduite, puis revenir à la valeur true lorsque la fenêtre de l’application est restaurée. Pour cela, la fenêtre de l’application peut gérer les SC_MINIMIZE et de SC_RESTORE commande lors de la réception d’WM_SYSCOMMAND message.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
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
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### PostWebMessageAsJson 

Publiez le WebMessage spécifié dans le document de niveau supérieur de cette [IWebView2WebView]().

> public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Le document de niveau supérieur de la fenêtre du document. chrome. WebView est déclenché. JavaScript dans ce document est susceptible de s’abonner à l’événement et de s’en désabonner via la commande suivante: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 Les arguments d’événement sont une instance de `MessageEvent` . Le paramètre IWebView2Settings:: IsWebMessageEnabled doit avoir la valeur true, ou cette méthode échoue avec E_INVALIDARG. La propriété Data du arg est le paramètre de chaîne WebMessage électronique analysé comme chaîne JSON dans un objet JavaScript. La propriété source de l’objet Event est une référence à l' `window.chrome.webview` objet. Pour plus d’informations sur l’envoi de messages à partir du document HTML du WebView vers l’hôte, voir SetWebMessageReceivedEventHandler. Ce message est envoyé de manière asynchrone. Si une navigation se produit avant que le message ne soit publié sur la page, le message ne sera pas envoyé.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### PostWebMessageAsString 

Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.

> public HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)

Ce comportement se comporte exactement de la même façon que PostWebMessageAsJson, mais la `window.chrome.webview` propriété Data de arg du message est une chaîne ayant la même valeur que webMessageAsString. Utilisez cette fonction au lieu de PostWebMessageAsJson si vous souhaitez communiquer via des chaînes simples plutôt que des objets JSON.

#### add_WebMessageReceived 

Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .

> [add_WebMessageReceived](#add_webmessagereceived)par le biais[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) du public HRESULT

La fonction postMessage est l' `void postMessage(object)` emplacement de tout objet pris en charge par la conversion JSON.

```cpp
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```

 Lorsque postMessage est appelée, le [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) défini par le biais de cette méthode SetWebMessageReceivedEventHandler sera appelé avec le paramètre objet de PostMessage converti en chaîne JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### remove_WebMessageReceived 

Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.

> [remove_WebMessageReceived](#remove_webmessagereceived)par le biais du mot-clé public HRESULT

#### Fermer 

Ferme le WebView et nettoie l’instance de navigateur sous-jacente.

> valeur publique [HRESULT (](#close))

Le nettoyage de l’option de suppression de navigateur entraîne la mise à jour des ressources par le biais du WebView. L’instance du navigateur sera arrêtée s’il n’y a aucune autre WebView.

Après avoir appelé Close, tous les appels de méthode échouent et les gestionnaires d’événements cessent de se déclencher. Plus précisément, le WebView publie ses références à ses gestionnaires d’événements lorsque la méthode Close est appelée.

Close est appelé implicitement lorsque le WebView perd sa référence finale et est détruit. Mais il est conseillé d’appeler explicitement Close pour éviter tout cycle accidentel de références entre le WebView et le code de l’application. En particulier, si vous capturez une référence à WebView dans un gestionnaire d’événements, vous créerez un cycle de référence entre le WebView et le gestionnaire d’événements. La fermeture rompt ce cycle en libérant tous les gestionnaires d’événements. Néanmoins, pour éviter ce problème, il est préférable d’appeler explicitement la fermeture sur le WebView et de ne pas capturer de référence à WebView pour s’assurer que le WebView peut être nettoyé correctement.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### CallDevToolsProtocolMethod 

Appelez une méthode DevToolsProtocol asynchrone.

> public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR parametersAsJson, gestionnaire[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) *)

Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des méthodes disponibles. Le paramètre methodName est le nom complet de la méthode au format `{domain}.{method}` . Le paramètre parametersAsJson est une chaîne au format JSON contenant les paramètres de la méthode correspondante. La méthode Invoke du gestionnaire est appelée lorsque la méthode est terminée de manière asynchrone. Invoke sera appelé avec l’objet de retour de la méthode sous la forme d’une chaîne JSON.

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### add_DevToolsProtocolEventReceived 

S’abonner à un événement DevToolsProtocol.

> valeur de HRESULT publique [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR NomÉvénement, gestionnaire[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) *, jeton EventRegistrationToken *)

Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste et une description des événements disponibles. Le paramètre eventName est le nom complet de l’événement au format `{domain}.{event}` . La méthode Invoke du gestionnaire est appelée chaque fois que l’événement DevToolsProtocol correspondant est déclenché. Invoke sera appelé à l’aide d’un objet args d’événement contenant l’objet de paramètre de l’événement CDP en tant que chaîne JSON.

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### remove_DevToolsProtocolEventReceived 

Supprimez un gestionnaire d’événements préalablement ajouté à add_DevToolsProtocolEventReceived.

> [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)par le biais du public HRESULT, EventRegistrationToken jeton

#### get_BrowserProcessId 

ID de processus du processus de navigation qui héberge le WebView.

> valeur publique HRESULT [get_BrowserProcessId](#get_browserprocessid)(valeur UInt32 *)

#### get_CanGoBack 

Peut parcourir le WebView vers la page précédente de l’historique de navigation.

> valeur publique HRESULT [get_CanGoBack](#get_cangoback)(bool * CanGoBack)

get_CanGoBack modifier la valeur avec l’événement DocumentStateChanged.

#### get_CanGoForward 

Peut parcourir le WebView sur la page suivante de l’historique de navigation.

> valeur publique HRESULT [get_CanGoForward](#get_cangoforward)(bool * CanGoForward)

get_CanGoForward modifier la valeur avec l’événement DocumentStateChanged.

#### GoBack 

Permet d’accéder à la page précédente de l’historique de navigation via le WebView.

> public HRESULT [GoBack](#goback)()

#### GoForward 

Navigue vers la page suivante de l’historique de navigation du WebView.

> valeur publique HRESULT [GoForward](#goforward)()

#### WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Format d’image utilisé par la méthode [IWebView2WebView:: CapturePreview](#capturepreview) .

> énumération [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Format d’image PNG.
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Format d’image JPEG.

#### WEBVIEW2_SCRIPT_DIALOG_KIND 

Type de boîte de dialogue JavaScript utilisée dans l’interface [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .

> énumération [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Une boîte de dialogue appelée par le biais de la fonction JavaScript window. Alert.
WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Une boîte de dialogue appelée via la fonction de fenêtre. confirmer JavaScript.
WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Une boîte de dialogue appelée via la fonction JavaScript window. prompt.

#### WEBVIEW2_PROCESS_FAILED_KIND 

Type d’échec de processus utilisé dans l’interface [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .

> énumération [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Indique que le processus du navigateur s’est arrêté de manière inattendue.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Indique le processus de rendu arrêté de manière inattendue.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Indique que le processus de rendu ne répond pas.

#### WEBVIEW2_PERMISSION_TYPE 

Le type d’une demande d’autorisation.

> énumération [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION            | Autorisation inconnue.
WEBVIEW2_PERMISSION_TYPE_MICROPHONE            | Autorisation de capture audio.
WEBVIEW2_PERMISSION_TYPE_CAMERA            | Autorisation de capture vidéo.
WEBVIEW2_PERMISSION_TYPE_GEOLOCATION            | Autorisation d’accès à la géolocalisation.
WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS            | Autorisation d’envoyer des notifications Web.
WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS            | Autorisation d’accès au capteur générique.
WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ            | Autorisation de lecture du presse-papiers système sans mouvement utilisateur.

#### WEBVIEW2_PERMISSION_STATE 

Réponse à une demande d’autorisation.

> énumération [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_STATE_DEFAULT            | Utilisez le comportement par défaut du navigateur, qui invite en principe les utilisateurs à la décision.
WEBVIEW2_PERMISSION_STATE_ALLOW            | Accordez la demande d’autorisation.
WEBVIEW2_PERMISSION_STATE_DENY            | Refusez la demande d’autorisation.

#### WEBVIEW2_MOVE_FOCUS_REASON 

Raison du déplacement du focus.

> énumération [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Paramètre de code axé sur le WebView.
WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Déplacement du focus en raison d’une touche Tab.
WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Déplacement du focus en partant du haut de l’onglet.

#### WEBVIEW2_WEB_ERROR_STATUS 

Valeurs d’état d’erreur pour les navigations Web.

> énumération [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Une erreur inconnue s’est produite.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | Le nom usuel du certificat SSL ne correspond pas à l’adresse Web.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | Le certificat SSL a expiré.
WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | Le certificat client SSL comporte des erreurs.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | Le certificat SSL a été révoqué.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | Le certificat SSL n’est pas valide.
WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | L’hôte n’est pas joignable.
WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | La connexion a expiré.
WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | Le serveur a renvoyé une réponse non valide ou non reconnue.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | La connexion a été annulée.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | La connexion a été réinitialisée.
WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | La connexion Internet a été interrompue.
WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Connexion impossible à la destination.
WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Impossible de résoudre le nom d’hôte fourni.
WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | L’opération a été annulée.
WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Échec de la redirection de la requête.
WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Une erreur inattendue s’est produite.

#### WEBVIEW2_WEB_RESOURCE_CONTEXT 

Énum pour les contextes de demande de ressources Web.

> énumération [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Toutes les ressources.
WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Ressources de documents.
WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Des ressources CSS;
WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Ressources d’image.
WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Autres ressources multimédias telles que les vidéos.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Ressources de police.
WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Ressources de script.
WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | Requêtes HTTP XML.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Extraire la communication de l’API.
WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Ressources TextTrack.
WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Autres ressources.
