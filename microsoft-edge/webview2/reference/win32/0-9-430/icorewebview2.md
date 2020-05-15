---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 77eb48773a963775e00d4dec50368564af5678b0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653679"
---
# interface ICoreWebView2 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.9.430. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface ICoreWebView2
  : public IUnknown
```

WebView2 vous permet d’héberger le contenu Web à l’aide de la technologie de navigateur Web la plus récente.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | L’objet ICoreWebView2Settings contient différents paramètres modifiables pour le WebView en cours d’exécution.
[get_Source](#get_source) | URI du document de niveau supérieur actuel.
[Rechercher](#navigate) | Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.
[NavigateToString](#navigatetostring) | Lance une navigation vers htmlContent en tant que code HTML source d’un nouveau document.
[add_NavigationStarting](#add_navigationstarting) | Ajoutez un gestionnaire d’événements pour l’événement NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationStarting.
[add_ContentLoading](#add_contentloading) | Ajoutez un gestionnaire d’événements pour l’événement ContentLoading.
[remove_ContentLoading](#remove_contentloading) | Supprimez un gestionnaire d’événements préalablement ajouté à add_ContentLoading.
[add_SourceChanged](#add_sourcechanged) | SourceChanged se déclenche lorsque la propriété source change.
[remove_SourceChanged](#remove_sourcechanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_SourceChanged.
[add_HistoryChanged](#add_historychanged) | Facturationmodifier écoutez la modification de l’historique de navigation du document de niveau supérieur.
[remove_HistoryChanged](#remove_historychanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_HistoryChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Supprimez un gestionnaire d’événements préalablement ajouté à add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Ajoutez un gestionnaire d’événements pour l’événement FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Supprimez un gestionnaire d’événements préalablement ajouté à add_FrameNavigationStarting.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Supprimez un gestionnaire d’événements préalablement ajouté à add_ScriptDialogOpening.
[add_PermissionRequested](#add_permissionrequested) | Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Supprimez un gestionnaire d’événements préalablement ajouté à add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Ajoutez le code JavaScript fourni à une liste de scripts qui doivent être exécutés après la création de l’objet global, mais avant l’analyse du document HTML et avant l’exécution de tout autre script fourni par le document HTML.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Supprimez le JavaScript correspondant ajouté par le biais de AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Exécutez le code JavaScript du paramètre JavaScript du document de niveau supérieur actuel affiché dans le WebView.
[CapturePreview](#capturepreview) | Capturez une image de l’affichage du WebView.
[Recharger](#reload) | Recharger la page active.
[PostWebMessageAsJson](#postwebmessageasjson) | Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Il s’agit d’un programme d’assistance pour publier un message qui est une chaîne simple plutôt qu’une représentation de chaîne JSON d’un objet JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Cet événement se déclenche lorsque le paramètre IsWebMessageEnabled est défini et au document de niveau supérieur des appels WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Supprimez un gestionnaire d’événements préalablement ajouté à add_WebMessageReceived.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Appelez une méthode DevToolsProtocol asynchrone.
[get_BrowserProcessId](#get_browserprocessid) | ID de processus du processus de navigation qui héberge le WebView.
[get_CanGoBack](#get_cangoback) | Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.
[get_CanGoForward](#get_cangoforward) | Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.
[GoBack](#goback) | Permet d’accéder à la page précédente de l’historique de navigation via le WebView.
[GoForward](#goforward) | Navigue vers la page suivante de l’historique de navigation du WebView.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.
[Stop](#stop) | Arrêtez toutes les navigations et les extractions de ressources en attente.
[add_NewWindowRequested](#add_newwindowrequested) | Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | Titre du document de niveau supérieur actuel.
[AddRemoteObject](#addremoteobject) | Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.
[RemoveRemoteObject](#removeremoteobject) | Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.
[OpenDevToolsWindow](#opendevtoolswindow) | Ouvre la fenêtre DevTools pour le document actif dans le WebView.
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Avertit en cas de modification de la propriété ContainsFullScreenElement.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Indique si le WebView contient un élément HTML fullscreen.
[add_WebResourceRequested](#add_webresourcerequested) | Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.
[remove_WebResourceRequested](#remove_webresourcerequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.
[add_WindowCloseRequested](#add_windowcloserequested) | Ajoutez un gestionnaire d’événements pour l’événement WindowCloseRequested.
[remove_WindowCloseRequested](#remove_windowcloserequested) | Supprimez un gestionnaire d’événements préalablement ajouté à add_WindowCloseRequested.
[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) | Format d’image utilisé par la méthode ICoreWebView2:: CapturePreview.
[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) | Type de boîte de dialogue JavaScript utilisée dans l’interface ICoreWebView2ScriptDialogOpeningEventHandler.
[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) | Type d’échec de processus utilisé dans l’interface ICoreWebView2ProcessFailedEventHandler.
[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) | Le type d’une demande d’autorisation.
[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) | Réponse à une demande d’autorisation.
[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) | Valeurs d’état d’erreur pour les navigations Web.
[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) | Énum pour les contextes de demande de ressources Web.

## Événements de navigation

L’ordre normal des événements de navigation est NavigationStarting, SourceChanged, ContentLoading, puis NavigationCompleted.

![dot-Inline-dotgraph-1. png](media/dot-inline-dotgraph-1.png)

Notez qu’il s’agit d’événements de navigation avec le même argument d’événement NavigationId. Les événements de navigation avec différents arguments d’événement NavigationId risquent de se chevaucher. Par exemple, si vous démarrez une navigation pour l’événement NavigationStarting, puis démarrez une autre navigation, vous verrez le NavigationStarting de la première navigation suivi par le NavigationStarting du deuxième navigation, suivi de l’NavigationCompleted de la première navigation, puis de tout le reste des événements de navigation appropriés pour la deuxième navigation. Dans les cas d’erreur, il est possible ou non qu’un événement ContentLoading se poursuive sur une page d’erreur. Dans le cas d’une redirection HTTP, plusieurs événements NavigationStarting sont disponibles dans une ligne, avec les indicateurs IsRedirect définis dans le premier.

Pour surveiller ou annuler les navigations dans les sous-cadres du WebView, utilisez FrameNavigationStarting.

## Modèle de processus

WebView2 utilise le même modèle de processus que le navigateur Web Edge. Il existe un processus de navigateur Edge par répertoire de données utilisateur spécifié dans une session utilisateur qui traitera tout processus appelant WebView2 spécifiant ce répertoire de données utilisateur. Cela signifie qu’un processus de navigateur Edge est susceptible de traiter plusieurs processus d’appel et qu’un processus d’appel est susceptible d’utiliser plusieurs processus de navigation latérale.

![dot-Inline-dotgraph-2. png](media/dot-inline-dotgraph-2.png)

Il y a un certain nombre de processus de convertisseur. Celles-ci sont créées autant de fois que nécessaire pour traiter plusieurs trames dans différents affichages. Le nombre de processus de rendu varie en fonction de la fonctionnalité du navigateur d’isolement de site et du nombre d’origines distantes distinctes affichées dans les webvues associées.

![dot-Inline-dotgraph-3. png](media/dot-inline-dotgraph-3.png)

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

Ouvrez DevTools avec les raccourcis normaux: `F12` ou `Ctrl+Shift+I` . Vous pouvez utiliser le `--auto-open-devtools-for-tabs` commutateur d’argument de commande pour que la fenêtre devtools s’ouvre immédiatement lors de la création d’un WebView. Pour plus d’informations sur le processus de navigation, voir documentation CreateCoreWebView2Host. Consultez la clé de Registre LoaderOverride pour essayer différentes builds de WebView2 sans modifier votre application dans la documentation CreateCoreWebView2Host.

## Contrôle de version

Une fois que vous avez utilisé une version particulière du SDK pour générer votre application, l’exécution de votre application avec une version plus ancienne ou plus récente des fichiers binaires de navigateur installés sera terminée. Jusqu’à la version 1.0.0.0 de WebView2, des modifications peuvent être apportées lors des mises à jour qui empêchent votre SDK de fonctionner avec des versions différentes des fichiers binaires de navigateur installés. Après la version 1.0.0.0, vous pouvez utiliser les différentes versions du kit de développement logiciel (SDK) pour travailler avec les meilleures pratiques suivantes:

Pour prendre en compte les modifications apportées à l’API, veillez à vérifier l’échec lors de l’appel de la DLL d’exportation CreateCoreWebView2Environment et lors de l’appel de QueryInterface sur un objet CoreWebView2. La valeur de retour de E_NOINTERFACE peut indiquer que le kit de développement logiciel (SDK) n’est pas compatible avec les fichiers binaires de navigation Edge.

La vérification de l’échec de QueryInterface sera également comptabilisée dans les cas où le kit de développement logiciel (SDK) est plus récent que la version du navigateur Edge et que votre application tente d’utiliser une interface qui n’est pas compatible avec le navigateur Edge.

Lorsqu’une interface n’est pas disponible, vous pouvez envisager de désactiver la fonctionnalité associée le cas échéant ou d’informer l’utilisateur final qu’il doit mettre à jour son navigateur.

## Ses

#### get_Settings 

L’objet ICoreWebView2Settings contient différents paramètres modifiables pour le WebView en cours d’exécution.

> valeurs publiques HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings * *)

#### get_Source 

URI du document de niveau supérieur actuel.

> valeur publique HRESULT [get_Source](#get_source)(LPWSTR * URI)

Cette valeur peut éventuellement changer dans le cadre du déclenchement de l’événement SourceChanged dans certains cas, par exemple pour accéder à un site ou à un fragment de navigation différent. Il restera identique pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active.

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### Rechercher 

Entraîner une navigation du document de niveau supérieur sur l’URI spécifié.

> public HRESULT [Navigate](#navigate)(Uri LPCWSTR)

Pour plus d’informations, voir événements de navigation. Notez que cela démarre une navigation et que l’événement NavigationStarting correspondant est déclenché après la fin de l’appel.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
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

> [add_NavigationStarting](#add_navigationstarting)par le biais du[mot de passe](ICoreWebView2NavigationStartingEventHandler.md)

NavigationStarting se déclenche lorsque le frame principal WebView demande une autorisation pour accéder à un URI différent. Cela se déclenche également pour les redirections.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
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

#### add_ContentLoading 

Ajoutez un gestionnaire d’événements pour l’événement ContentLoading.

> [add_ContentLoading](#add_contentloading)par le biais du[mot de passe](ICoreWebView2ContentLoadingEventHandler.md)

ContentLoading se déclenche avant le chargement du contenu, notamment les scripts ajoutés avec AddScriptToExecuteOnDocumentCreated ContentLoading ne se déclenchent pas si une même navigation de page se produit (par exemple par le biais des navigations ou de l’historique d’un fragment. pushState navigation). Cela suit les événements NavigationStarting et SourceChanged, ainsi que les événements HistoryChanged et NavigationCompleted.

#### remove_ContentLoading 

Supprimez un gestionnaire d’événements préalablement ajouté à add_ContentLoading.

> [remove_ContentLoading](#remove_contentloading)par le biais du mot-clé public HRESULT

#### add_SourceChanged 

SourceChanged se déclenche lorsque la propriété source change.

> [add_SourceChanged](#add_sourcechanged)par le biais du[mot de passe](ICoreWebView2SourceChangedEventHandler.md)

L’utilisation de l’fonction SourceChanged est déclenchée pour accéder à un site ou à un fragment de navigation différent. Il ne se déclenche pas pour les autres types de navigation, tels que les recharges de page ou l’historique. pushState avec la même URL que la page active. SourceChanged se déclenche avant ContentLoading pour la navigation vers un nouveau document. Ajoutez un gestionnaire d’événements pour l’événement SourceChanged. 

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### remove_SourceChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_SourceChanged.

> [remove_SourceChanged](#remove_sourcechanged)par le biais du mot-clé public HRESULT

#### add_HistoryChanged 

Facturationmodifier écoutez la modification de l’historique de navigation du document de niveau supérieur.

> [add_HistoryChanged](#add_historychanged)par le biais du[mot de passe](ICoreWebView2HistoryChangedEventHandler.md)

Utilisez Facturationmodifier pour vérifier si la valeur get_CanGoBack/get_CanGoForward a changé. HistoryChanged est également déclenché pour l’utilisation de GoBack/GoForward. HistoryChanged se déclenche après SourceChanged et ContentLoading. Ajoutez un gestionnaire d’événements pour l’événement HistoryChanged. 

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### remove_HistoryChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_HistoryChanged.

> [remove_HistoryChanged](#remove_historychanged)par le biais du mot-clé public HRESULT

#### add_NavigationCompleted 

Ajoutez un gestionnaire d’événements pour l’événement NavigationCompleted.

> [add_NavigationCompleted](#add_navigationcompleted)par le biais du[mot de passe](ICoreWebView2NavigationCompletedEventHandler.md)

L’événement NavigationCompleted se déclenche lorsque le WebView est complètement chargé (le corps. OnLoad a été déclenché) ou que le chargement s’est arrêté avec une erreur.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
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

> [add_FrameNavigationStarting](#add_framenavigationstarting)par le biais du[mot de passe](ICoreWebView2NavigationStartingEventHandler.md)

FrameNavigationStarting se déclenche quand une Frame enfant du WebView demande une autorisation pour accéder à un URI différent. Cela se déclenche également pour les redirections.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### add_ScriptDialogOpening 

Ajoutez un gestionnaire d’événements pour l’événement ScriptDialogOpening.

> [add_ScriptDialogOpening](#add_scriptdialogopening)par le biais du[mot de passe](ICoreWebView2ScriptDialogOpeningEventHandler.md)

L’événement se déclenche quand une boîte de dialogue JavaScript (alerte, confirmation ou invite) s’affiche pour le WebView. Cet événement est déclenché uniquement si la propriété ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled est définie sur false. L’événement ScriptDialogOpening peut être utilisé pour supprimer des boîtes de dialogue ou remplacer les boîtes de dialogue par défaut par des boîtes de dialogue personnalisées.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
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

#### add_PermissionRequested 

Ajoutez un gestionnaire d’événements pour l’événement PermissionRequested.

> [add_PermissionRequested](#add_permissionrequested)par le biais du[mot de passe](ICoreWebView2PermissionRequestedEventHandler.md)

Se déclenche lorsque le contenu d’un WebView demande l’autorisation d’accéder à des ressources privilégiées.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_PermissionRequested.

> [remove_PermissionRequested](#remove_permissionrequested)par le biais du mot-clé public HRESULT

#### add_ProcessFailed 

Ajoutez un gestionnaire d’événements pour l’événement ProcessFailed.

> [add_ProcessFailed](#add_processfailed)par le biais du[mot de passe](ICoreWebView2ProcessFailedEventHandler.md)

Se déclenche quand un processus WebView s’est arrêté de manière inattendue ou ne répond plus.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
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

> public HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript, gestionnaire[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) *)

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
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
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

> public HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript, gestionnaire[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) *)

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
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
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

> public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream * ImageStream, gestionnaire[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) *)

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
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

#### PostWebMessageAsJson 

Publier le WebMessage spécifié sur le document de niveau supérieur dans ce WebView.

> public HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Le document de niveau supérieur de la fenêtre du document. chrome. WebView est déclenché. JavaScript dans ce document est susceptible de s’abonner à l’événement et de s’en désabonner via la commande suivante: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 Les arguments d’événement sont une instance de `MessageEvent` . Le paramètre ICoreWebView2Settings:: IsWebMessageEnabled doit avoir la valeur true, ou cette méthode échoue avec E_INVALIDARG. La propriété Data du arg est le paramètre de chaîne WebMessage électronique analysé comme chaîne JSON dans un objet JavaScript. La propriété source de l’objet Event est une référence à l' `window.chrome.webview` objet. Pour plus d’informations sur l’envoi de messages à partir du document HTML du WebView vers l’hôte, voir SetWebMessageReceivedEventHandler. Ce message est envoyé de manière asynchrone. Si une navigation se produit avant que le message ne soit publié sur la page, le message ne sera pas envoyé.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

> [add_WebMessageReceived](#add_webmessagereceived)par le biais[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) du public HRESULT

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

 Lorsque postMessage est appelée, le [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) défini par le biais de cette méthode SetWebMessageReceivedEventHandler sera appelé avec le paramètre objet de PostMessage converti en chaîne JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

#### CallDevToolsProtocolMethod 

Appelez une méthode DevToolsProtocol asynchrone.

> public HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR parametersAsJson, gestionnaire[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) *)

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
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### get_BrowserProcessId 

ID de processus du processus de navigation qui héberge le WebView.

> valeur publique HRESULT [get_BrowserProcessId](#get_browserprocessid)(valeur UInt32 *)

#### get_CanGoBack 

Renvoie vrai si le WebView peut accéder à une page précédente de l’historique de navigation.

> valeur publique HRESULT [get_CanGoBack](#get_cangoback)(bool * CanGoBack)

L’événement HistoryChanged se déclenche si get_CanGoBack change de valeur.

#### get_CanGoForward 

Cette fonction renvoie la valeur vrai si le WebView peut accéder à une page suivante de l’historique de navigation.

> valeur publique HRESULT [get_CanGoForward](#get_cangoforward)(bool * CanGoForward)

L’événement HistoryChanged se déclenche si get_CanGoForward change de valeur.

#### GoBack 

Permet d’accéder à la page précédente de l’historique de navigation via le WebView.

> public HRESULT [GoBack](#goback)()

#### GoForward 

Navigue vers la page suivante de l’historique de navigation du WebView.

> valeur publique HRESULT [GoForward](#goforward)()

#### GetDevToolsProtocolEventReceiver 

Obtenez un destinataire d’événement de protocole DevTools qui vous permet de vous abonner à un événement de protocole DevTools.

> public HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR NomÉvénement;[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) * * Receiver)

Le paramètre eventName est le nom complet de l’événement au format `{domain}.{event}` . Voir la [visionneuse de protocoles devtools](https://aka.ms/DevToolsProtocolDocs) pour obtenir une liste des événements de protocole devtools et des arguments d’événement.

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
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### Stop 

Arrêtez toutes les navigations et les extractions de ressources en attente.

> point d' [arrêt](#stop)public HRESULT ()

Ne permet pas d’arrêter les scripts.

#### add_NewWindowRequested 

Ajoutez un gestionnaire d’événements pour l’événement NewWindowRequested.

> [add_NewWindowRequested](#add_newwindowrequested)par le biais du[mot de passe](ICoreWebView2NewWindowRequestedEventHandler.md)

Se déclenche lorsque le contenu à l’intérieur du WebView est demandé pour ouvrir une nouvelle fenêtre, par exemple via Window. Open. L’application peut transmettre un WebView cible qui sera considéré comme la fenêtre ouverte.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_NewWindowRequested.

> [remove_NewWindowRequested](#remove_newwindowrequested)par le biais du mot-clé public HRESULT

#### add_DocumentTitleChanged 

Ajoutez un gestionnaire d’événements pour l’événement DocumentTitleChanged.

> [add_DocumentTitleChanged](#add_documenttitlechanged)par le biais du[mot de passe](ICoreWebView2DocumentTitleChangedEventHandler.md)

L’événement se déclenche lorsque la propriété DocumentTitle de WebView change et qu’il est susceptible de se déclencher avant ou après l’événement NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Supprimez un gestionnaire d’événements préalablement ajouté à add_DocumentTitleChanged.

> [remove_DocumentTitleChanged](#remove_documenttitlechanged)par le biais du mot-clé public HRESULT

#### get_DocumentTitle 

Titre du document de niveau supérieur actuel.

> valeur publique HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR * title)

Si le document ne comporte pas de titre explicite ou s’il est vide, une valeur par défaut qui peut ou ne correspond pas à l’URI du document sera utilisée.

#### AddRemoteObject 

Ajoutez l’objet hôte fourni au script qui s’exécute sur le WebView avec le nom spécifié.

> public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR Name, variant * Object)

Les objets hôtes sont exposés en tant que proxy d’objets distants par le biais de `window.chrome.webview.remoteObjects.<name>` . Les proxys d’objets distants sont promet et sont résolus en objet représentant l’objet hôte. La promesse est refusée si l’application n’a pas ajouté d’objet portant le nom. Lorsque le code JavaScript accède à une propriété ou une méthode de l’objet, une promesse est renvoyée, qui est résolue en fonction de la valeur renvoyée par l’hôte de la propriété ou de la méthode, ou rejetée en cas d’erreur, comme il n’y a pas de propriété ou de méthode sur l’objet ou les paramètres ne sont pas valides. Par exemple, lorsque le code de l’application effectue les opérations suivantes: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 Le code JavaScript de l’affichage WebView sera en mesure d’accéder à appObject comme suit, puis d’accéder aux attributs et méthodes de appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Notez qu’en ce qui concerne les types simples, IDispatch et Array sont pris en charge, le type IUnknown, VT_DECIMAL ou VT_RECORD variant n’est pas pris en charge. Les objets JavaScript distants comme les fonctions de rappel sont représentés sous la forme d’un VT_DISPATCH VARIANT avec l’objet qui implémente IDispatch. La méthode de rappel JavaScript doit être appelée à l’aide de DISPID_VALUE pour le DISPID. Les tableaux imbriqués sont pris en charge jusqu’à une profondeur de 3. Les matrices de par types de référence ne sont pas prises en charge. VT_EMPTY et VT_NULL sont mappés dans JavaScript en tant que valeurs NULL. Dans JavaScript, les valeurs NULL et non définies sont mappées à VT_EMPTY.

De plus, tous les objets distants sont exposés en tant que `window.chrome.webview.remoteObjects.sync.<name>` . Ici, les objets hôtes sont exposés en tant que proxy d’objets distants synchrones. Celles-ci ne sont pas promesse et les appels de fonctions ou d’accès aux propriétés empêchent de manière synchrone l’exécution d’un script en attente de communication croisée pour que le code hôte s’exécute. En conséquence, cela peut entraîner des problèmes de fiabilité et nous vous conseillons d’utiliser l’API asynchrone basée sur la promesse `window.chrome.webview.remoteObjects.<name>` décrite ci-dessus.

Les proxys d’objets distants synchrones et les proxys d’objets distants asynchrones peuvent deux proxy sur le même objet distant. Les modifications distantes apportées par un proxy seront reflétées dans tous les autres proxy de ce même objet distant, qu’il s’agisse de proxys et synchrones ou asynchrones.

Si JavaScript est bloqué lors d’un appel asynchrone au code natif, ce code natif ne peut pas rappeler JavaScript. Les tentatives d’une telle opération échoueront avec HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Les proxys d’objets distants sont des objets proxy JavaScript qui interceptent l’ensemble des appels de propriété Get, de jeu de propriétés et de méthode. Les propriétés ou méthodes qui font partie du prototype de fonction ou d’objet sont exécutées localement. De plus, toute propriété ou méthode du tableau `chrome.webview.remoteObjects.options.forceLocalProperties` sera également exécutée localement. Par exemple, vous pouvez inclure des méthodes facultatives ayant une signification dans JavaScript comme `toJSON` et `Symbol.toPrimitive` . Vous pouvez en ajouter d’autres à ce tableau selon vos besoins.

Il existe une méthode `chrome.webview.remoteObjects.cleanupSome` qui consiste à utiliser au mieux le nettoyage de la mémoire proxy d’objets distants.

Les proxys d’objets distants présentent également les méthodes suivantes qui s’exécutent en local:

* applyRemote, getRemote, setRemote: effectue un appel de méthode, Get de propriété ou jeu de propriétés sur l’objet distant. Vous pouvez utiliser ces éléments pour forcer explicitement une méthode ou une propriété à s’exécuter à distance en cas de conflit entre une méthode locale ou une propriété. Par exemple, `proxy.toString()` exécute la méthode ToString locale sur l’objet proxy. Mais `proxy.applyRemote('toString')` s’exécute `toString` plutôt sur l’objet proxy distant.

* getLocal, setLocal: exécuter la propriété Get ou Property Set localement. Vous pouvez utiliser ces méthodes pour forcer l’affichage ou la définition d’une propriété sur le proxy d’objet distant lui-même plutôt que sur l’objet distant qu’elle représente. Par exemple, obtiendrez `proxy.unknownProperty` la propriété nommée `unknownProperty` de l’objet proxy distant. Toutefois `proxy.getLocal('unknownProperty')` , vous obtiendrez la valeur de la propriété `unknownProperty` sur l’objet proxy lui-même.

* synchronisation: les proxys d’objets distants asynchrones présentent une méthode de synchronisation qui renvoie une promesse de proxy d’objet distant synchrone pour le même objet distant. Par exemple, `chrome.webview.remoteObjects.sample.methodCall()` retourne un proxy asynchrone d’objet distant. Vous pouvez utiliser la `sync` méthode pour obtenir un proxy d’objet distant synchrone à la place: `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: les proxys d’objets distants synchrones présentent une méthode Async qui bloque et retourne un proxy d’objet distant asynchrone pour le même objet distant. Par exemple, `chrome.webview.remoteObjects.sync.sample.methodCall()` retourne un proxy d’objet distant synchrone. Appel de la `async` méthode sur ce bloc, puis retour d’un proxy d’objet distant asynchrone pour le même objet distant: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* ensuite: les proxys d’objets distants asynchrones ont une méthode Then. Cela leur permet d’être await. `then` renverra une promesse qui est résolue en une représentation de l’objet distant. Si le proxy représente un littéral JavaScript, une copie de celui-ci est renvoyée localement. Si le proxy représente une fonction, un proxy non-await est retourné. Si le proxy représente un objet JavaScript avec une combinaison de propriétés littérales et de propriétés de fonctions, une copie de l’objet est renvoyée avec des propriétés en tant que proxy d’objets distants.

Tous les autres appels de propriété et de méthode (autres que les méthodes de proxy d’objet distant, la liste forceLocalProperties et les propriétés des prototypes de fonction et d’objet) s’exécutent à distance. Les proxys d’objets distants asynchrones retournent une promesse qui représente la complétion asynchrone d’appeler la méthode à distance ou d’obtenir la propriété. La promesse se résout une fois les opérations distantes terminées et la promesse de la valeur de l’opération. Les proxys d’objets distants synchrones s’exécutent de la même façon, mais bloquent l’exécution JavaScript et attendez la fin de l’opération à distance.

La définition d’une propriété sur un proxy asynchrone d’objet distant fonctionne légèrement différemment. Le jeu renvoie immédiatement et la valeur de retour est la valeur qui sera définie. Il s’agit d’une condition requise de l’objet proxy JavaScript. Si vous avez besoin d’attendre que le jeu de propriétés soit terminé, utilisez la méthode setRemote qui renvoie une promesse comme décrit ci-dessus. La propriété du jeu de propriétés d’objet synchrone se bloque de manière synchrone tant que la propriété est définie.

Par exemple, supposons que vous disposiez d’un objet COM avec l’interface suivante.

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 Nous pouvons ajouter une instance de cette interface dans notre JavaScript avec `AddRemoteObject` . Dans le cas présent, vous nommerez ce message `sample` :

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 Ensuite, dans le document HTML, vous pouvez utiliser cet objet COM via `chrome.webview.remoteObjects.sample` :

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### RemoveRemoteObject 

Supprimez l’objet hôte spécifié par le nom afin qu’il ne soit plus accessible à partir du code JavaScript du WebView.

> public HRESULT [RemoveRemoteObject](#removeremoteobject)(nom LPCWSTR)

Même si de nouvelles tentatives d’accès seront refusées, si l’objet est déjà obtenu par le code JavaScript du WebView, le code JavaScript continuera à avoir accès à cet objet. Il n’est pas nécessaire d’appeler cette méthode pour un nom qui a déjà été supprimé ou n’ayant jamais été ajouté.

#### OpenDevToolsWindow 

Ouvre la fenêtre DevTools pour le document actif dans le WebView.

> public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Ne peut pas être appelé lorsque la fenêtre DevTools est déjà ouverte

#### add_ContainsFullScreenElementChanged 

Avertit en cas de modification de la propriété ContainsFullScreenElement.

> [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)par le biais du[mot de passe](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md)

Cela signifie qu’un élément HTML à l’intérieur du WebView est entré en plein écran jusqu’à la taille de l’affichage WebView ou en laissant le plein écran. Cet événement est utile, par exemple, lorsqu’un élément vidéo demande d’être placé en plein écran. L’écouteur de ContainsFullScreenElementChanged peut alors redimensionner le WebView en réponse.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Supprimez le gestionnaire d’événements précédemment ajouté avec la méthode d’événement add_ correspondante.

> [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)par le biais du mot-clé public HRESULT

#### get_ContainsFullScreenElement 

Indique si le WebView contient un élément HTML fullscreen.

> valeur publique HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Ajoutez un gestionnaire d’événements pour l’événement WebResourceRequested.

> [add_WebResourceRequested](#add_webresourcerequested)par le biais du[mot de passe](ICoreWebView2WebResourceRequestedEventHandler.md)

Se déclenche lorsque WebView effectue une requête HTTP à un filtre d’URL et de contexte de ressources correspondant qui a été ajouté à l’aide de AddWebResourceRequestedFilter. Au moins un filtre doit être ajouté pour que l’événement se déclenche.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
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

#### AddWebResourceRequestedFilter 

Ajoute un URI et un filtre de contexte de ressources à l’événement WebResourceRequested.

> public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) constante resourceContext)

Le paramètre URI peut être une chaîne de caractères génériques (' ': zéro ou plusieurs; '? ': exactement 1). nullptr est l’équivalent de L "". Pour plus d’détails sur les filtres de contexte de ressources, voir CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT Enum.

#### RemoveWebResourceRequestedFilter 

Supprime un filtre de ressources correspondant précédemment ajouté pour l’événement WebResourceRequested.

> public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) constante resourceContext)

Si le même filtre a été ajouté plusieurs fois, il doit être supprimé autant de fois que ce dernier a été ajouté pour que la suppression soit effective. Renvoie E_INVALIDARG pour un filtre qui n’a jamais été ajouté.

#### add_WindowCloseRequested 

Ajoutez un gestionnaire d’événements pour l’événement WindowCloseRequested.

> [add_WindowCloseRequested](#add_windowcloserequested)par le biais du[mot de passe](ICoreWebView2WindowCloseRequestedEventHandler.md)

Se déclenche lorsque le contenu à l’intérieur du WebView est requis pour fermer la fenêtre, par exemple, après l’appel de Window. Close. L’application doit fermer la fenêtre WebView et la fenêtre de l’application associée si cela est pertinent pour l’application.

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_WindowCloseRequested 

Supprimez un gestionnaire d’événements préalablement ajouté à add_WindowCloseRequested.

> [remove_WindowCloseRequested](#remove_windowcloserequested)par le biais du mot-clé public HRESULT

#### CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Format d’image utilisé par la méthode ICoreWebView2:: CapturePreview.

> énumération [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Format d’image PNG.
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Format d’image JPEG.

#### CORE_WEBVIEW2_SCRIPT_DIALOG_KIND 

Type de boîte de dialogue JavaScript utilisée dans l’interface ICoreWebView2ScriptDialogOpeningEventHandler.

> énumération [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Une boîte de dialogue appelée par le biais de la fonction JavaScript window. Alert.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Une boîte de dialogue appelée via la fonction de fenêtre. confirmer JavaScript.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Une boîte de dialogue appelée via la fonction JavaScript window. prompt.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD            | Une boîte de dialogue appelée via l’événement JavaScript beforeunload.

#### CORE_WEBVIEW2_PROCESS_FAILED_KIND 

Type d’échec de processus utilisé dans l’interface ICoreWebView2ProcessFailedEventHandler.

> énumération [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Indique que le processus du navigateur s’est arrêté de manière inattendue.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Indique le processus de rendu arrêté de manière inattendue.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Indique que le processus de rendu ne répond pas.

#### CORE_WEBVIEW2_PERMISSION_KIND 

Le type d’une demande d’autorisation.

> énumération [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION            | Autorisation inconnue.
CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE            | Autorisation de capture audio.
CORE_WEBVIEW2_PERMISSION_KIND_CAMERA            | Autorisation de capture vidéo.
CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION            | Autorisation d’accès à la géolocalisation.
CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS            | Autorisation d’envoyer des notifications Web.
CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS            | Autorisation d’accès au capteur générique.
CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ            | Autorisation de lecture du presse-papiers système sans mouvement utilisateur.

#### CORE_WEBVIEW2_PERMISSION_STATE 

Réponse à une demande d’autorisation.

> énumération [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT            | Utilisez le comportement par défaut du navigateur, qui invite en principe les utilisateurs à la décision.
CORE_WEBVIEW2_PERMISSION_STATE_ALLOW            | Accordez la demande d’autorisation.
CORE_WEBVIEW2_PERMISSION_STATE_DENY            | Refusez la demande d’autorisation.

#### CORE_WEBVIEW2_WEB_ERROR_STATUS 

Valeurs d’état d’erreur pour les navigations Web.

> énumération [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Une erreur inconnue s’est produite.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | Le nom usuel du certificat SSL ne correspond pas à l’adresse Web.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | Le certificat SSL a expiré.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | Le certificat client SSL comporte des erreurs.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | Le certificat SSL a été révoqué.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | Le certificat SSL n’est pas valide &ndash; cela peut signifier que le certificat ne correspond pas aux codes confidentiels de clé publique du nom d’hôte. le certificat est signé par une autorité non approuvée ou à l’aide d’un algorithme de signature faible, le certificat ayant revendiqué des noms DNS enfreignant les contraintes de nom, le certificat contient une clé faible, la période de validité du certificat est trop longue, l’absence de données de révocation ou du mécanisme de révocation, le [legacy Symantec root](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html)nom d’hôte non unique, l’absence de données de transparence de
CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | L’hôte n’est pas joignable.
CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | La connexion a expiré.
CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | Le serveur a renvoyé une réponse non valide ou non reconnue.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | La connexion a été annulée.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | La connexion a été réinitialisée.
CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | La connexion Internet a été interrompue.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Connexion impossible à la destination.
CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Impossible de résoudre le nom d’hôte fourni.
CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | L’opération a été annulée.
CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Échec de la redirection de la requête.
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Une erreur inattendue s’est produite.

#### CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT 

Énum pour les contextes de demande de ressources Web.

> énumération [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context)

 Doubl                         | Descriptions
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Toutes les ressources.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Ressources de documents.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Des ressources CSS;
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Ressources d’image.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Autres ressources multimédias telles que les vidéos.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Ressources de police.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Ressources de script.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | Requêtes HTTP XML.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Extraire la communication de l’API.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | Ressources TextTrack.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | Communication API EventSource.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | Communication de l’API WebSocket.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | Manifestes de l’application Web.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | Échange HTTP signé.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | Demandes ping.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | Rapports de violation des CSP.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Autres ressources.
