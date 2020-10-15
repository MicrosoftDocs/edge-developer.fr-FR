---
description: Conventions d’API de WebView2 C++ Win32
title: Conventions d’API de WebView2 C++ Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications WPF, WPF, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 42f0b5c9970b2e4a6424eb70458c58a98ec8dbc7
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11118974"
---
# Conventions d’API de WebView2 C++ Win32  

## Méthodes Async  

Les méthodes asynchrones dans l’API C++ Win32 WebView2 utilisent une interface de délégué pour indiquer la fin de la méthode Async, le code de réussite ou d’échec, et pour some, le résultat de la méthode asynchrone.  Le paramètre final de toutes les méthodes asynchrones est un pointeur vers une interface de délégué qui vous permet de fournir une implémentation.  

L’interface du délégué dispose d’une `Invoke` méthode unique qui utilise comme premier paramètre un `HRESULT` Code de réussite ou d’échec.  Par ailleurs, il peut exister un second paramètre qui est le résultat de la méthode si la méthode a un résultat.  Par exemple, la méthode [ICoreWebView2:: CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] utilise le paramètre final comme `ICoreWebView2CapturePreviewCompletedHandler` pointeur.  Pour envoyer une `CapturePreview` demande de méthode, vous fournissez une instance du `ICoreWebView2CapturePreviewCompletedHandler` pointeur que vous implémentez.  L’extrait de code suivant utilise une méthode à implémenter.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Vous implémentez la `Invoke` méthode et `CoreWebView2` sollicitez votre `Invoke` méthode lorsque la requête est `CapturePreview` terminée.  Le paramètre unique décrit le `HRESULT` Code de réussite ou d’échec de la `CapturePreview` requête.  

Ou `ICoreWebView2::ExecuteScript` bien, vous fournissez une instance de `ICoreWebView2ExecuteScriptCompletedHandler` `Invoke` la méthode qui vous permet d’utiliser le code de réussite ou d’échec de la `ExecuteScript` requête, ainsi que le deuxième paramètre `resultObjectAsJson` qui est le paramètre JSON du résultat de l’exécution du script.  

Vous pouvez implémenter manuellement les `CompleteHandler` interfaces de délégué ou vous pouvez utiliser la [fonction de rappel WRL][CppCxWrlCallbackFunction].  La fonction callback est utilisée dans l’extrait de code WebView2 suivant.  

```cpp
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

## Événements  

Les événements de l’API C++ Win32 WebView2 utilisent `add_EventName` la `remove_EventName` paire de méthodes et vous abonner et vous désabonner des événements.  La `add_EventName` méthode prend une interface de délégué de gestionnaire d’événements et remet un `EventRegistrationToken` paramètre out en tant que paramètre out.  La `remove_EventName` méthode accepte un `EventRegistrationToken` et annule l’abonnement à l’événement correspondant.  

Les interfaces de délégué de gestionnaire d’événements fonctionnent de manière très similaire aux interfaces de délégué de gestionnaires terminés de méthode asynchrone.  Vous implémentez l’interface du délégué de gestionnaire d’événements et `CoreWebView2` envoyez un rappel chaque fois que l’événement se déclenche.  Chaque interface de délégué de gestionnaire d’événements possède une `Invoke` méthode unique qui a un paramètre sender suivi d’un paramètre d’arguments d’événement.  L’expéditeur est l’instance de l’objet sur lequel vous avez souscrit un abonnement à des événements.  Le paramètre args est une interface qui contient des informations sur l’événement actuellement en cours de déclenchement.  

Par exemple `NavigationCompleted` , l’événement sur `ICoreWebView2` a `ICoreWebView2::add_NavigationCompleted` la `ICoreWebView2::remove_NavigationCompleted` paire de méthodes et.  Lorsque vous demandez l’ajout, vous fournissez une instance de `ICoreWebView2NavigationCompletedEventHandler` la méthode que vous avez implémentée précédemment `Invoke` .  Lorsque l' `NavigationCompleted` événement est déclenché, votre `Invoke` méthode est sollicitée.  Le premier paramètre est le `ICoreWebView2` qui déclenche l' `NavigationCompleted` événement.  Le deuxième paramètre est le `ICoreWebView2NavigationCompletedEventArgs` qui contient des informations sur la réussite de la navigation et ainsi de suite.  

À l’instar de la méthode asynchrone, vous pouvez implémenter vous-même directement, ou vous pouvez utiliser la fonction de rappel WRL utilisée dans l’extrait de code WebView2 suivant.  

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
                COREWEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                if (webErrorStatus == COREWEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                {
                    // Do something here if you want to handle a specific error case.
                    // In most cases it is not necessary, because the WebView
                    // displays an error page automatically.
                }
            }
            m_toolbar->SetItemEnabled(Toolbar::Item_CancelButton, false);
            m_toolbar->SetItemEnabled(Toolbar::Item_ReloadButton, true);
            return S_OK;
        })
        .Get(),
    &m_navigationCompletedToken));
```  

## String  

Les paramètres de type chaîne se `LPWSTR` terminent par un caractère nul.  Le demandeur alloue la chaîne à l’aide de `CoTaskMemAlloc` .  La propriété est transférée à la demande et il appartient au demandeur de libérer de la mémoire en utilisant `CoTaskMemFree` .  

Les valeurs de chaîne dans les paramètres sont des `LPCWSTR` chaînes dont le caractère nul est terminé.  Le demandeur vérifie que la chaîne est valide pour la durée de la demande de fonction synchrone.  Si le destinataire doit conserver cette valeur à un certain point après la demande de la fonction, le destinataire doit allouer une copie associée de la valeur de chaîne.  

## D’analyse des URI et de JSON  

Diverses méthodes fournissent ou acceptent des URI et JSON en tant que chaînes.  Utilisez votre propre bibliothèque préférée pour analyser et générer les chaînes.  

Si WinRT est disponible pour votre application, vous pouvez utiliser les `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` méthodes et pour analyser ou générer des chaînes JSON ou `RuntimeClass_Windows_Foundation_Uri` des `IUriRuntimeClassFactory` méthodes pour analyser et générer des URI.  Les deux méthodes fonctionnent dans les applications Win32.  

Si vous utilisez `IUri` et que vous `CreateUri` souhaitez analyser les URI, vous pouvez utiliser les indicateurs de création d’URI suivants pour que le `CreateUri` comportement corresponde plus étroitement à l’analyse de l’URI dans le WebView.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

<!-- links -->  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview-interface ICoreWebView2 | Documents Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Fonction de rappel (WRL) | Documents Microsoft"  
