---
description: Incorporer des technologies Web (HTML, CSS et JavaScript) dans vos applications natives avec le contrôle Microsoft Edge WebView2
title: 0.9.579-WebView2 C++ Win32 ICoreWebView2Settings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge, ICoreWebView2Settings
ms.openlocfilehash: d17ab13deb9f26f2d7e29b5f8bb92d0aade727bc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010305"
---
# 0.9.579-interface ICoreWebView2Settings 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Settings
  : public IUnknown
```

Définit les propriétés permettant, de désactiver ou de modifier les fonctionnalités WebView.

## Résumé

 Ses                        | Descriptions
--------------------------------|---------------------------------------------
[get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled) | La propriété AreDefaultContextMenusEnabled est utilisée pour empêcher l’affichage des menus contextuels par défaut pour les utilisateurs dans WebView.
[get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled) | AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.
[get_AreHostObjectsAllowed](#get_arehostobjectsallowed) | La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.
[get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled) | La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.
[get_IsScriptEnabled](#get_isscriptenabled) | Déterminez si l’exécution JavaScript est activée dans les futures navigations du WebView.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled vérifie si la barre d’État s’affiche.
[get_IsWebMessageEnabled](#get_iswebmessageenabled) | La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.
[get_IsZoomControlEnabled](#get_iszoomcontrolenabled) | La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.
[put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled) | Définissez la propriété AreDefaultContextMenusEnabled.
[put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled) | Définissez la propriété AreDefaultScriptDialogsEnabled.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Définissez la propriété AreDevToolsEnabled.
[put_AreHostObjectsAllowed](#put_arehostobjectsallowed) | Définissez la propriété AreHostObjectsAllowed.
[put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled) | Définissez la propriété IsBuiltInErrorPageEnabled.
[put_IsScriptEnabled](#put_isscriptenabled) | Définissez la propriété IsScriptEnabled.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Définissez la propriété IsStatusBarEnabled.
[put_IsWebMessageEnabled](#put_iswebmessageenabled) | Définissez la propriété IsWebMessageEnabled.
[put_IsZoomControlEnabled](#put_iszoomcontrolenabled) | Définissez la propriété IsZoomControlEnabled.

Les modifications apportées après l’événement NavigationStarting ne s’appliquent pas tant que la navigation de niveau supérieur suivante n’est pas appliquée.

## Ses

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

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.

> valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool * AreDefaultScriptDialogsEnabled)

Si elle a la valeur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, celles qui sont affichées par l’alerte JavaScript, les fonctions confirmer, invites et événement beforeunload). Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.

#### get_AreDevToolsEnabled 

AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.

> valeur publique HRESULT [get_AreDevToolsEnabled](#get_aredevtoolsenabled)(bool * AreDevToolsEnabled)

C’est vrai par défaut.

#### get_AreHostObjectsAllowed 

La propriété AreHostObjectsAllowed est utilisée pour contrôler si les objets hôtes sont accessibles à partir de la page dans WebView.

> valeur publique HRESULT [get_AreHostObjectsAllowed](#get_arehostobjectsallowed)(bool * autorisé)

Par défaut, la valeur est TRUE.

```cpp
            BOOL allowHostObjects;
            CHECK_FAILURE(m_settings->get_AreHostObjectsAllowed(&allowHostObjects));
            if (allowHostObjects)
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(FALSE));
                MessageBox(
                    nullptr, L"Access to host objects will be denied after the next navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_AreHostObjectsAllowed(TRUE));
                MessageBox(
                    nullptr, L"Access to host objects will be allowed after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### get_IsBuiltInErrorPageEnabled 

La propriété IsBuiltInErrorPageEnabled est utilisée pour désactiver la page d’erreur intégrée à un échec de navigation et un échec de processus de rendu.

> [get_IsBuiltInErrorPageEnabled](#get_isbuiltinerrorpageenabled)publique HRESULT (bool * activé)

Par défaut, la valeur est TRUE. Lorsqu’elle est désactivée, une page vide s’affiche lorsque l’erreur associée se produit.

```cpp
            BOOL enabled;
            CHECK_FAILURE(m_settings->get_IsBuiltInErrorPageEnabled(&enabled));
            if (enabled)
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(FALSE));
                MessageBox(
                    nullptr, L"Built-in error page will be disabled for future navigation.",
                    L"Settings change", MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsBuiltInErrorPageEnabled(TRUE));
                MessageBox(
                    nullptr, L"Built-in error page will be enabled for future navigation.",
                    L"Settings change", MB_OK);
            }
```

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

#### get_IsStatusBarEnabled 

IsStatusBarEnabled vérifie si la barre d’État s’affiche.

> valeur publique HRESULT [get_IsStatusBarEnabled](#get_isstatusbarenabled)(bool * IsStatusBarEnabled)

La barre d’État est généralement affichée dans le coin inférieur gauche de l’affichage WebView et présente des éléments tels que l’URI d’un lien lorsque l’utilisateur pointe dessus et d’autres informations. C’est vrai par défaut.

#### get_IsWebMessageEnabled 

La propriété IsWebMessageEnabled est utilisée lors du chargement d’un nouveau document HTML.

> valeur publique HRESULT [get_IsWebMessageEnabled](#get_iswebmessageenabled)(bool * IsWebMessageEnabled)

Si elle a la valeur true, la communication de l’hôte vers le document HTML de niveau supérieur de l’hôte est autorisée via PostWebMessageAsJson, PostWebMessageAsString et Window. chrome. événement de message (voir la documentation PostWebMessageAsJson pour plus d’informations). La communication du document HTML de niveau supérieur d’un WebView à l’hôte est autorisée via la fonction postMessage de Window. chrome. WebView et la méthode SetWebMessageReceivedEventHandler (voir la documentation SetWebMessageReceivedEventHandler pour plus d’informations). Si elle est définie sur false, la communication n’est pas autorisée. PostWebMessageAsJson et PostWebMessageAsString échoueront avec E_ACCESSDENIED et Window. chrome. WebView. postMessage échoue en levant une instance d’objet d’erreur. C’est vrai par défaut.

```cpp
    ComPtr<ICoreWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### get_IsZoomControlEnabled 

La propriété IsZoomControlEnabled est utilisée pour empêcher l’utilisateur d’influer sur le zoom du WebView.

> [get_IsZoomControlEnabled](#get_iszoomcontrolenabled)publique HRESULT (bool * activé)

Par défaut, la valeur est TRUE. Lorsqu’il est désactivé, l’utilisateur ne peut pas effectuer un zoom à l’aide de Ctrl +/-ou Ctrl + molette, mais le zoom peut être défini via l’API ZoomFactor.

```cpp
            BOOL zoomControlEnabled;
            CHECK_FAILURE(m_settings->get_IsZoomControlEnabled(&zoomControlEnabled));
            if (zoomControlEnabled)
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(FALSE));
                MessageBox(
                    nullptr, L"Zoom control will be disabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
            else
            {
                CHECK_FAILURE(m_settings->put_IsZoomControlEnabled(TRUE));
                MessageBox(
                    nullptr, L"Zoom control will be enabled after the next navigation.", L"Settings change",
                    MB_OK);
            }
```

#### put_AreDefaultContextMenusEnabled 

Définissez la propriété AreDefaultContextMenusEnabled.

> [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)publiques HRESULT

#### put_AreDefaultScriptDialogsEnabled 

Définissez la propriété AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT

#### put_AreDevToolsEnabled 

Définissez la propriété AreDevToolsEnabled.

> [put_AreDevToolsEnabled](#put_aredevtoolsenabled)de passe par le public HRESULT

#### put_AreHostObjectsAllowed 

Définissez la propriété AreHostObjectsAllowed.

> [put_AreHostObjectsAllowed](#put_arehostobjectsallowed)publiques HRESULT

#### put_IsBuiltInErrorPageEnabled 

Définissez la propriété IsBuiltInErrorPageEnabled.

> [put_IsBuiltInErrorPageEnabled](#put_isbuiltinerrorpageenabled)publiques HRESULT

#### put_IsScriptEnabled 

Définissez la propriété IsScriptEnabled.

> [put_IsScriptEnabled](#put_isscriptenabled)de passe par le public HRESULT

#### put_IsStatusBarEnabled 

Définissez la propriété IsStatusBarEnabled.

> [put_IsStatusBarEnabled](#put_isstatusbarenabled)de passe par le public HRESULT

#### put_IsWebMessageEnabled 

Définissez la propriété IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT

#### put_IsZoomControlEnabled 

Définissez la propriété IsZoomControlEnabled.

> [put_IsZoomControlEnabled](#put_iszoomcontrolenabled)publiques HRESULT

