---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: 0.9.430-WebView2 C++ Win32 ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 70ccef9e99b3649ceca49b736570ba416cf73ebd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883986"
---
# 0.9.430-interface ICoreWebView2Settings 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_IsScriptEnabled](#get_isscriptenabled) | Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.
[put_IsScriptEnabled](#put_isscriptenabled) | Définissez la propriété IsScriptEnabled.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Définissez la propriété IsWebMessageEnabled.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Définissez la propriété AreDefaultScriptDialogsEnabled.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled vérifie si la barre d’État s’affiche.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Définissez la propriété IsStatusBarEnabled.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Définissez la propriété AreDevToolsEnabled.
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Définissez la propriété AreDefaultContextMenusEnabled.
[get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed) | La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets distants sont accessibles à partir de la page dans WebView.
[put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed) | Définissez la propriété AreRemoteObjectsAllowed.
[get_IsZoomControlEnabled](#get_iszoomcontrolenabled) | La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.
[put_IsZoomControlEnabled](#put_iszoomcontrolenabled) | Définissez la propriété IsZoomControlEnabled.

Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.

## Ses

#### get_IsScriptEnabled 

Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.

> valeur publique HRESULT [get_IsScriptEnabled](#get_isscriptenabled)(bool * IsScriptEnabled)

Cela ne concerne que les scripts du document. les scripts injectés avec ExecuteScript s’exécutent même si le script est désactivé. C’est vrai par défaut.

```cpp
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
```

#### put_IsScriptEnabled 

Définissez la propriété IsScriptEnabled.

> [put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT

#### get_IsWebMessageEnabled 

La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.

> valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool * IsWebMessageEnabled)

Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations). La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations). Si elle est définie sur false, la communication n’est pas autorisée. PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur. C’est vrai par défaut.

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Définissez la propriété IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.

> valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool * AreDefaultScriptDialogsEnabled)

Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload). Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.

#### put_AreDefaultScriptDialogsEnabled 

Définissez la propriété AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT

#### get_IsStatusBarEnabled 

IsStatusBarEnabled vérifie si la barre d’État s’affiche.

> valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool * IsStatusBarEnabled)

La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations. C’est vrai par défaut.

#### put_IsStatusBarEnabled 

Définissez la propriété IsStatusBarEnabled.

> [put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT

#### get_AreDevToolsEnabled 

AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.

> valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool * AreDevToolsEnabled)

C’est vrai par défaut.

#### put_AreDevToolsEnabled 

Définissez la propriété AreDevToolsEnabled.

> [put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT

#### get_AreDefaultContextMenusEnabled 

La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.

> [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)publique HRESULT (bool * activé)

Par défaut, la valeur est TRUE.

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### put_AreDefaultContextMenusEnabled 

Définissez la propriété AreDefaultContextMenusEnabled.

> [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT

#### get_AreRemoteObjectsAllowed 

La propriété AreRemoteObjectsAllowed est utilisée pour contrôler si les objets distants sont accessibles à partir de la page dans WebView.

> valeur publique HRESULT [get_AreRemoteObjectsAllowed](#get_areremoteobjectsallowed)(bool * autorisé)

Par défaut, la valeur est TRUE.

```cpp
            BOOL allowRemoteObjects;
            CHECK_FAILURE(m_settings->get_AreRemoteObjectsAllowed(&allowRemoteObjects));
            if (allowRemoteObjects)
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to remote objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreRemoteObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to remote objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### put_AreRemoteObjectsAllowed 

Définissez la propriété AreRemoteObjectsAllowed.

> [put_AreRemoteObjectsAllowed](#put_areremoteobjectsallowed)publiques HRESULT

#### get_IsZoomControlEnabled 

La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.

> [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)publique HRESULT (bool * activé)

Par défaut, la valeur est TRUE. Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via une API de put_ZoomFactor.

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control is disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control is enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### put_IsZoomControlEnabled 

Définissez la propriété IsZoomControlEnabled.

> [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)publiques HRESULT

