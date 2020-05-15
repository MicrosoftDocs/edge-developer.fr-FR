---
description: Héberger le contenu Web dans votre application Win32 avec le contrôle Microsoft Edge WebView2
title: Applications Microsoft Edge WebView2 pour Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge
ms.openlocfilehash: 3c799e97f8e85927e1c11b30be747d7649faeca0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2020
ms.locfileid: "10653400"
---
# interface IWebView2Settings 

> [!NOTE]
> Cette interface peut être modifiée ou indisponible pour les versions ultérieures SDK version 0.8.355. Reportez-vous à [référence](../../../webview2-api-reference.md) pour la dernière référence d’API.

```
interface IWebView2Settings
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
[get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated) | Ce paramètre est déconseillé et renverra toujours false.
[put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated) | Ce paramètre est déconseillé et n’aura aucun effet.
[get_IsStatusBarEnabled](#get_isstatusbarenabled) | IsStatusBarEnabled vérifie si la barre d’État s’affiche.
[put_IsStatusBarEnabled](#put_isstatusbarenabled) | Définissez la propriété IsStatusBarEnabled.
[get_AreDevToolsEnabled](#get_aredevtoolsenabled) | AreDevToolsEnabled vérifie que l’utilisateur est en mesure d’utiliser le menu contextuel ou les raccourcis clavier pour ouvrir la fenêtre DevTools.
[put_AreDevToolsEnabled](#put_aredevtoolsenabled) | Définissez la propriété AreDevToolsEnabled.

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
    ComPtr<IWebView2Settings> settings;
    CHECK_FAILURE(m_webView->get_Settings(&settings));

    CHECK_FAILURE(settings->put_IsWebMessageEnabled(TRUE));
```

#### put_IsWebMessageEnabled 

Définissez la propriété IsWebMessageEnabled.

> [put_IsWebMessageEnabled](#put_iswebmessageenabled)de passe par le public HRESULT

#### get_AreDefaultScriptDialogsEnabled 

AreDefaultScriptDialogsEnabled est utilisé lors du chargement d’un nouveau document HTML.

> valeur publique HRESULT [get_AreDefaultScriptDialogsEnabled](#get_aredefaultscriptdialogsenabled)(bool * AreDefaultScriptDialogsEnabled)

Si cette valeur est définie sur false, le WebView n’affichera pas la boîte de dialogue JavaScript par défaut (en particulier, les fonctions d’alerte, de confirmation et de confirmation JavaScript). Au lieu de cela, si un gestionnaire d’événements est défini par SetScriptDialogOpeningEventHandler, WebView envoie un événement qui contient toutes les informations pour la boîte de dialogue et autorise l’application hôte à afficher sa propre interface utilisateur personnalisée.

#### put_AreDefaultScriptDialogsEnabled 

Définissez la propriété AreDefaultScriptDialogsEnabled.

> [put_AreDefaultScriptDialogsEnabled](#put_aredefaultscriptdialogsenabled)de passe par le public HRESULT

#### get_IsFullscreenAllowed_deprecated 

Ce paramètre est déconseillé et renverra toujours false.

> valeur publique HRESULT [get_IsFullscreenAllowed_deprecated](#get_isfullscreenallowed_deprecated)(bool * IsFullscreenAllowed)

Cela signifie que les éléments du WebView ne remplissent que les limites de la WebView. Cette propriété sera alors entièrement supprimée. À la place, écoutez l’événement ContainsFullScreenElementChanged.

Détermine si la commande plein écran est autorisée pour les éléments du WebView. Lorsqu’il est autorisé, le contenu Web tel qu’un élément vidéo dans le WebView est autorisé à s’afficher en mode plein écran. Lorsqu’il n’est pas autorisé, ce type d’élément remplit les limites du WebView lorsque l’élément est demandé en plein écran. C’est vrai par défaut.

#### put_IsFullscreenAllowed_deprecated 

Ce paramètre est déconseillé et n’aura aucun effet.

> [put_IsFullscreenAllowed_deprecated](#put_isfullscreenallowed_deprecated)de passe par le public HRESULT

À la place, écoutez l’événement ContainsFullScreenElementChanged.

Définissez la propriété IsFullscreenAllowed.

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

