---
description: Conventions de l’API Win32 C++ WebView2
title: Conventions de l’API Win32 C++ WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, wpf apps, wpf, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: b5a86751bfe3386058812ca166fa7cf9e0e201dc
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535642"
---
# <a name="win32-c-webview2-api-conventions"></a>Conventions de l’API WebView2 Win32 C++  

:::row:::
   :::column span="1":::
      Plateformes pris en charge :
   :::column-end:::
   :::column span="2":::
      Win32
   :::column-end:::
:::row-end:::  

## <a name="prerequisites"></a>Conditions préalables  

*   Expérience d’utilisation de l’API Win32  

## <a name="async-methods"></a>Méthodes async  

Les méthodes asynchrones dans l’API WebView2 Win32 C++ utilisent une interface déléguée pour vous contacter pour les raisons suivantes.  

*   La méthode async est terminée.  
*   Code de réussite ou d’échec.  
*   Résultat de la méthode asynchrone.  

Le dernier paramètre de toutes les méthodes asynchrones est un pointeur vers une interface déléguée dont vous fournissez une implémentation.  

L’interface déléguée possède une méthode unique qui prend comme premier paramètre un code de réussite `Invoke` `HRESULT` ou d’échec.  En outre, il peut y avoir un deuxième paramètre qui est le résultat de la méthode si la méthode a un résultat.  Par exemple, la [méthode ICoreWebView2::CapturePreview][Webview2ReferenceWin32Icorewebview2CapturePreview] prend comme paramètre final un `ICoreWebView2CapturePreviewCompletedHandler` pointeur.  Pour envoyer une `CapturePreview` demande de méthode, vous fournissez une instance du `ICoreWebView2CapturePreviewCompletedHandler` pointeur que vous implémentez.  L’extrait de code suivant utilise une méthode pour implémenter.  

```cpp
HRESULT Invoke(HRESULT result)
```  

Vous implémentez `Invoke` la méthode et demandez votre méthode lorsque la demande est `CoreWebView2` `Invoke` `CapturePreview` terminée.  Le paramètre unique est le code de réussite ou `HRESULT` d’échec de la `CapturePreview` demande.  

Vous pouvez également fournir une instance qui dispose d’une méthode qui vous fournit le code de réussite ou `ICoreWebView2::ExecuteScript` `Invoke` d’échec de la `ExecuteScript` demande.  Fournissez également le deuxième paramètre qui est le JSON du résultat de l’exécution du script.  

Vous pouvez implémenter manuellement les interfaces déléguées, ou vous pouvez utiliser la fonction de rappel `CompleteHandler` [(WRL).][CppCxWrlCallbackFunction]  La [fonction de rappel (WRL)][CppCxWrlCallbackFunction] est utilisée dans l’extrait de code WebView2 suivant.  

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

## <a name="events"></a>Événements  

Les événements dans l’API C++ Win32 WebView2 utilisent la paire méthode et abonnement pour s’abonner à des événements et `add_EventName` `remove_EventName` s’en désabonner.  La `add_EventName` méthode prend une interface déléguée de gestion d’événements et retourne un `EventRegistrationToken` jeton en tant que paramètre de sortie.  La `remove_EventName` méthode prend un `EventRegistrationToken` jeton et désabonner l’abonnement à l’événement correspondant.  

Les interfaces déléguées du handler d’événements fonctionnent de la même manière que les interfaces déléguées de la méthode async terminées.  Vous implémentez l’interface déléguée du handler d’événements et envoyez un rappel chaque `CoreWebView2` fois que l’événement s’exécute.  Chaque interface déléguée du handler d’événements possède une seule méthode qui possède un paramètre d’expéditeur suivi d’un paramètre `Invoke` d’rgs d’événement.  L’expéditeur est l’instance de l’objet auquel vous vous êtes abonné pour les événements.  Le paramètre args d’événement est une interface qui contient des informations sur l’événement en cours de tir.  

Par exemple, `NavigationCompleted` l’événement sur a la paire méthode et la `ICoreWebView2` `ICoreWebView2::add_NavigationCompleted` `ICoreWebView2::remove_NavigationCompleted` paire.  Lorsque vous envoyez une demande, vous fournissez une instance dans laquelle `ICoreWebView2NavigationCompletedEventHandler` vous avez précédemment implémenté la `Invoke` méthode.  Lorsque `NavigationCompleted` l’événement s’exécute, `Invoke` votre méthode est demandée.  Le premier paramètre exécute `NavigationCompleted` l’événement.  Le deuxième paramètre contient des informations sur la réussite de la navigation, etc.  

À l’exemple de l’interface déléguée de handler terminée de la méthode async, utilisez l’une des actions suivantes pour la configurer.  

*   Implémentez-le directement.  
*   Utilisez la [fonction WRL (Callback function)][CppCxWrlCallbackFunction] qui est utilisée dans l’extrait de code WebView2 suivant.  

<!-- todo:  what is async method completed handler delegate interface?  Is there a shorter name for it?  -->  

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

## <a name="strings"></a>Chaînes  

Les paramètres de sortie de chaîne `LPWSTR` sont des chaînes terminées par null.  Le demandeur fournit la chaîne à l’aide `CoTaskMemAlloc` de .  La propriété est transférée au demandeur et c’est au demandeur de libérer la mémoire à l’aide `CoTaskMemFree` de .  

Les paramètres d’entrée de chaîne `LPCWSTR` sont des chaînes terminées par null.  Le demandeur s’assure que la chaîne est valide pour la durée de la demande de fonction synchrone.  Si le récepteur doit stocker la valeur à un certain point une fois la demande de fonction terminée, le récepteur doit fournir une copie associée de la valeur de chaîne.  

## <a name="uri-and-json-parsing"></a>URI et l’doncsiation JSON  

Diverses méthodes fournissent ou acceptent des URS et JSON en tant que chaînes.  Utilisez votre bibliothèque préférée pour l’utilisation et la génération des chaînes.  

Si WinRT est disponible pour votre application, vous pouvez utiliser les méthodes et les méthodes pour parer ou produire des chaînes ou des méthodes JSON pour l' `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` URIS.  Les deux méthodes fonctionnent dans les applications Win32.  

Si vous utilisez et pour l’URI, vous pouvez utiliser les indicateurs de création d’URI suivants pour que le comportement corresponde plus étroitement à l’URI de l’URI dans `IUri` `CreateUri` `CreateUri` WebView.  

```json
Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO
```  

## <a name="see-also"></a>Voir également  

*   To get started using WebView2 Win32 C/C++, navigate to [Get started with WebView2][Webview2IndexGetStarted] guides.  
*   Pour plus d’informations sur les API WebView2, accédez à la référence [d’API.][DotnetApiMicrosoftWebWebview2WpfWebview2]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[Webview2GetStartedWin32]: ../get-started/win32.md "Commencer à prendre en | WebView2 Documents Microsoft"  

[Webview2ReferenceWin32Icorewebview2CapturePreview]: /microsoft-edge/webview2/reference/win32/icorewebview2#capturepreview "CapturePreview - interface ICoreWebView2 | Documents Microsoft"  

[CppCxWrlCallbackFunction]: /cpp/cppcx/wrl/callback-function-wrl "Callback Function (WRL) | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2WpfWebview2]: /dotnet/api/microsoft.web.webview2.wpf.webview2 "Classe WebView2 | Documents Microsoft"  
