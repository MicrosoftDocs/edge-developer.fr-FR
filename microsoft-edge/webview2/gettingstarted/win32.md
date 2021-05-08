---
description: Guide de mise en place avec WebView2 pour les applications Win32
title: Mise en place de WebView2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/29/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 47f24b160797ce0ab7a7cb6a656c4f6b4e5696ac
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536465"
---
# <a name="getting-started-with-webview2"></a>Mise en place de WebView2  

Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].  Pour plus d’informations sur les API WebView2 individuelles, accédez à la [référence d’API.][Webview2ReferenceWin32]  

## <a name="prerequisites"></a>Conditions préalables  

Veillez à installer la liste des conditions préalables suivante avant de poursuivre.  

*   [WebView2 Runtime][Webview2Installer] ou tout canal [Microsoft Edge (Chromium) non stable][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \(actuellement Windows 10, Windows 8.1 et Windows 7\).  
    
    > [!NOTE]
    > L’équipe WebView recommande d’utiliser le canal Canary et la version minimale requise est 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 ou ultérieure avec la prise en charge de C++ installée.  
    
## <a name="step-1---create-a-single-window-app"></a>Étape 1 : créer une application à fenêtre unique  

Commencez par un projet de bureau de base qui contient une seule fenêtre principale.  

> [!IMPORTANT]
> Pour mieux concentrer la procédure pas à pas, utilisez l’exemple de code modifié de la procédure pas à pas : créer une application de bureau Windows classique [(C++)][CppWindowsWalkthroughCreatingDesktopApplication] pour votre exemple d’application.  Pour télécharger l’exemple modifié et commencer, accédez [à WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

1.  Dans Visual Studio, ouvrez `WebView2GettingStarted.sln` .  
    Si vous utilisez une version antérieure de Visual Studio, pointez sur le projet **WebView2GettingStarted,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Propriétés.**  Sous **Propriétés**de configuration générales, modifiez Windows version du SDK et du jeu d’outils de plateforme pour utiliser le  >  **** SDK Win10 et Visual Studio’outils disponibles. **** ****  

:::image type="complex" source="../media/tool-version.png" alt-text="Version de l’outil" lightbox="../media/tool-version.png":::
   Version de l’outil  
:::image-end:::  

Visual Studio peut afficher des erreurs, car le fichier d’en-tête WebView2 manque dans votre projet.  Les erreurs doivent être corrigées après [l’étape 2.](#step-2---install-webview2-sdk)  

## <a name="step-2---install-webview2-sdk"></a>Étape 2 : installer le SDK WebView2  

Ajoutez le SDK WebView2 au projet.  Utilisez NuGet pour installer le SDK Win32.  

1.  Pointez sur le projet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Gérer NuGet packages.**  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Gérer des packages NuGet" lightbox="../media/manage-nuget-packages.png":::
       Gérer des packages NuGet  
    :::image-end:::  
    
1.  Installez la bibliothèque Windows d’implémentation de l’application.  
    1.  Dans la barre de recherche, `Microsoft.Windows.ImplementationLibrary` tapez > **choisissez Microsoft.Windows. ImplementationLibrary**.  
    1.  Dans la fenêtre de droite, choisissez **Installer.**  NuGet télécharge la bibliothèque sur votre ordinateur.  
        
        > [!NOTE]
        > La [Windows d’implémentation et][GithubMicrosoftWilMain] Windows bibliothèque de modèles [C++ runtime][CppCxWrlTemplateLibraryVS2019] sont facultatives et facilitent l’exécution de COM pour l’exemple.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows Bibliothèque d’implémentation" lightbox="../media/wil.png":::
           Windows Bibliothèque d’implémentation  
        :::image-end:::  
        
1.  Installez le SDK WebView2.  
    1.  Dans la barre de recherche, `Microsoft.Web.WebView2` tapez > **choisissez Microsoft.Web.WebView2**.  
    1.  Dans la fenêtre de droite, choisissez **Installer.**  NuGet télécharge le SDK sur votre ordinateur.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Gestionnaire de package" lightbox="../media/nuget.png":::
           NuGet Gestionnaire de package
        :::image-end:::  
        
1.  Ajoutez l’en-tête WebView2 à votre projet.  
    :::row:::
       :::column span="1":::
          Dans le fichier, copiez l’extrait de code suivant et `HelloWebView.cpp` collez-le après la dernière `#include` ligne.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          La section Include doit ressembler à l’extrait de code suivant.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Prêt à être utilisé et à créer avec l’API WebView2.  

### <a name="build-your-empty-sample-app"></a>Créer votre exemple d’application vide  

Pour créer et exécuter l’exemple d’application, sélectionnez `F5` .  Votre application affiche une fenêtre vide.  

:::image type="complex" source="../media/empty-app.png" alt-text="Application vide" lightbox="../media/empty-app.png":::
   Application vide  
:::image-end:::  

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a>Étape 3 : créer un seul WebView dans la fenêtre parent  

Ajoutez un WebView à la fenêtre principale.  

 Utilisez la méthode pour configurer l’environnement et localiser Microsoft Edge navigateur `CreateCoreWebView2Environment` \(Chromium\) sur le contrôle.  Vous pouvez également utiliser la méthode si vous souhaitez spécifier l’emplacement du navigateur, le dossier utilisateur, les indicateurs de navigateur, etc., au lieu d’utiliser `CreateCoreWebView2EnvironmentWithOptions` le paramètre par défaut.  À la fin de la méthode, exécutez la méthode à l’intérieur du rappel et exécutez la méthode pour obtenir le `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` WebView associé.  

Dans le rappel, définissez quelques paramètres de plus, resizez le WebView pour prendre 100 % de la fenêtre parente et accédez à Bing.  

Copiez l’extrait de code suivant et collez-le après `HelloWebView.cpp` le commentaire et avant le `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` commentaire.  

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {
        
            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }
                
                // Add a few settings for the webview
                // The demo step is redundant since the values are the default settings
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);
                
                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);
                
                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");
                
                // Step 4 - Navigation events
                
                // Step 5 - Scripting
                
                // Step 6 - Communication between host and web content
                
                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```  

### <a name="build-your-bing-sample-app"></a>Créer votre exemple Bing application  

Pour créer et exécuter l’application, sélectionnez `F5` .  Vous avez maintenant une fenêtre WebView qui affiche la Bing page.  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing fenêtre" lightbox="../media/bing-window.png":::
   Bing fenêtre  
:::image-end:::  

## <a name="step-4---navigation-events"></a>Étape 4 : événements de navigation  

L’équipe WebView a déjà abordé la navigation vers l’URL à l’aide `ICoreWebView2::Navigate` de la méthode de la dernière étape.  Lors de la navigation, WebView déclenche une séquence d’événements que l’hôte peut écouter.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Pour plus d’informations, accédez aux [événements de navigation.][Webview2ConceptsNavigationEvents]  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation" lightbox="../media/navigation-events.png":::
   Événements de navigation  
:::image-end:::  

Dans les cas d’erreur, un ou plusieurs des événements suivants peuvent se produire selon que la navigation se poursuit jusqu’à une page web d’erreur.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

> [!NOTE]
> Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.  

À titre d’exemple d’utilisation des événements, inscrivez un responsable pour l’événement afin d’annuler les demandes `NavigationStarting` non HTTPS.  Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` .  

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```  

À présent, l’application ne navigue pas vers les sites non https.  Vous pouvez utiliser un mécanisme similaire pour accomplir d’autres tâches, telles que la limitation de la navigation à l’intérieur de votre propre domaine.  

## <a name="step-5---scripting"></a>Étape 5 : scripts  

Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.  Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.  Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.  Le javaScript injecté est exécuté avec un minutage spécifique.  

*   Exécutez-le après la création de l’objet global.  
*   Exécutez-le avant tout autre script inclus dans le document HTML.  

Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` .  

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```  

À présent, WebView doit toujours figer `Object` l’objet et renvoie le document de page une seule fois.  

> [!NOTE] 
> Les API d’injection de script \(et d’autres API WebView2\) sont asynchrones, vous devez utiliser des rappels si le code doit être exécuté dans un ordre spécifique.  

## <a name="step-6---communication-between-host-and-web-content"></a>Étape 6 : communication entre le contenu hôte et le contenu web  

L’hôte et le contenu web peuvent également communiquer entre eux par le biais de la `postMessage` méthode.  Le contenu web en cours d’exécution dans un WebView peut publier sur l’hôte par le biais de la méthode, et le message est géré par tout le handler d’événement inscrit `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` sur l’hôte.  De même, l’hôte peut envoyer un message au contenu web par le biais d’une méthode ou d’une méthode, qui est capturée par les handlers ajoutés à partir de `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` `window.chrome.webview.addEventListener` l’écoute.  Le mécanisme de communication permet au contenu web d’utiliser des fonctionnalités natives en passant des messages pour demander à l’hôte d’exécuter des API natives.  

Par exemple, pour comprendre le mécanisme, les étapes suivantes se produisent lorsque vous essayez d’afficher l’URL du document dans WebView.  

1.  L’hôte inscrit un handler pour renvoyer le message reçu au contenu web  
1.  L’hôte injecte un script au contenu web qui inscrit un handler pour imprimer un message à partir de l’hôte  
1.  L’hôte injecte un script au contenu web qui publie l’URL sur l’hôte  
1.  Le handler de l’hôte est déclenché et renvoie le message \(l’URL\) au contenu web  
1.  Le handler du contenu web est déclenché et imprime le message à partir de l’hôte \(l’URL\)  

Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` .  

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```  

### <a name="build-your-display-url-sample-app"></a>Créer votre exemple d’application d’URL d’affichage  

Pour créer et exécuter l’application, sélectionnez `F5` .  L’URL apparaît dans une fenêtre pop-up avant d’accéder à une page web.  

:::image type="complex" source="../media/show-url.png" alt-text="Url d’affichage" lightbox="../media/show-url.png":::
   Url d’affichage  
:::image-end:::  

Félicitations, vous avez créé votre première application WebView2.  

## <a name="next-steps"></a>Étapes suivantes  

Pour obtenir des fonctionnalités WebView2 supplémentaires qui ne sont pas couvertes dans cet article, examinez les ressources suivantes.  

*   Pour en savoir plus sur la création d’applications WebView2, accédez aux meilleures pratiques de développement [WebView2.][WV2BestPractices]  
*   Pour obtenir un exemple complet des fonctionnalités WebView2, accédez à [l’exemple d’API WebView2.][GithubMicrosoftedgeWebview2samplesApisample]  
*   Pour un exemple d’application créé à l’aide de WebView2, accédez [à WebView2Browser][GithubMicrosoftedgeWebview2browser].  
*   Pour plus d’informations sur l’API WebView2, accédez à la référence [d’API.][Webview2ReferenceWin32]  

## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a>Entrer en contact avec l’équipe web Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[WV2BestPractices]: ../concepts/developer-guide.md "Meilleures pratiques en matière de développement WebView2 | Documents Microsoft"  
[MicrosoftDeveloperMicrosoftEdgeWebview2]: https://developer.microsoft.com/microsoft-edge/webview2 "WebView2 | Microsoft Edge Développeur"  

[Webview2ReferenceWin32]: /microsoft-edge/webview2/reference/win32 "Référence WebView2 Win32 C++ | Documents Microsoft"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019&preserve-view=true "Windows Modèles WRL (Runtime C++ Template Library) | Documents Microsoft"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019&preserve-view=true "Walkthrough: Create a traditional Windows Desktop application (C++) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser - MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/blob/master/SampleApps/WebView2APISample/README.md "Exemple d’API WebView2 - MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Windows Bibliothèques d’implémentation (WIL) : microsoft/wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Programme d’installation WebView2"  
