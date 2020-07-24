---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Mise en route de WebView2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/07/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 7e35dc6ab84a32cfa7e020fa34ddfaa63818eda1
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895517"
---
# Mise en route de WebView2 (developer preview)  

Le contenu suivant vous présente les fonctionnalités fréquemment utilisées de [WebView2 (developer preview)][Webview2Index] et fournit un point de départ pour la création de votre première application WebView2.  Pour plus d’informations sur les API WebView2 individuelles, voir informations de référence sur les [API][Webview2ReferenceWin3209538].  

## Conditions préalables  

*   [Microsoft Edge (chrome)][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \ (actuellement Windows 10, Windows 8,1 et Windows 7 \).  
    
    > [!NOTE]
    > L’équipe WebView recommande d’utiliser le canal Canaries et la version minimale requise est 82.0.488.0.  
    
*   [Visual Studio][MicrosoftVisualstudioMain] 2015 ou version ultérieure avec prise en charge C++ installée.  

## Étape 1: créer une application Win32 de fenêtre unique  

Utiliser un projet de bureau de base contenant une seule fenêtre principale.  Pour mieux mettre au point la procédure pas à pas, vous utilisez un exemple de code modifié de la [procédure pas à pas: création d’une application de bureau Windows classique (C++)][CppWindowsWalkthroughCreatingDesktopApplication] pour votre exemple d’application.  Pour télécharger l’exemple modifié et commencer, voir [exemples de WebView2][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].  

Dans Visual Studio, ouvrez `WebView2GettingStarted.sln` .  Si vous utilisez une ancienne version de Visual Studio, pointez sur le projet **WebView2GettingStarted** , ouvrez le menu contextuel, puis cliquez sur **Propriétés**.  Sous **Propriétés de configuration**  >  **générales**, modifiez la version et l' **ensemble d’outils de plateforme** du **SDK Windows** pour utiliser le kit de développement logiciel (SDK) Win10 et l’ensemble d’outils Visual Studio (vs Tools) disponible.  

:::image type="complex" source="../media/tool-version.png" alt-text="Version de l’outil":::
   Version de l’outil  
:::image-end:::  

Visual Studio peut afficher des erreurs en raison d’un fichier d’en-tête WebView2 manquant, qui doit disparaître après l’exécution de l’étape 2.  

## Étape 2: installer le SDK WebView2  

Ajoutez le kit de développement logiciel (SDK) WebView2 au projet.  Pour la version préliminaire du développeur, vous pouvez installer le kit de développement logiciel (SDK) Win32 en utilisant NuGet.  

1.  Pointez sur le projet, ouvrez le menu contextuel, puis sélectionnez **gérer les packages NuGet**.  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Gérer les packages NuGet":::
       Gérer les packages NuGet  
    :::image-end:::  
    
1.  Installez la bibliothèque d’implémentation Windows.  
    1.  Entrez `Microsoft.Windows.ImplementationLibrary` dans la barre de recherche, sélectionnez **Microsoft. Windows. ImplementationLibrary** dans les résultats, puis sélectionnez **installer** dans la fenêtre de droite.  NuGet télécharge le SDK sur votre ordinateur.  
        
        > [!NOTE] 
        > La [bibliothèque d’implémentation Windows][GithubMicrosoftWilMain] et la [bibliothèque de modèles C++ Windows Runtime][CppCxWrlTemplateLibraryVS2019] sont facultatifs et ont été ajoutés pour faciliter l’utilisation de com.  
        
        :::image type="complex" source="../media/wil.png" alt-text="Bibliothèque d’implémentation Windows":::
           Bibliothèque d’implémentation Windows  
        :::image-end:::  
        
1.  Installez le kit de développement logiciel (SDK) WebView2.  
    1.  Entrez `Microsoft.Web.WebView2` dans la barre de recherche, sélectionnez **Microsoft. Web. WebView2** dans les résultats, puis sélectionnez **installer** dans la fenêtre de droite.  NuGet télécharge le SDK sur votre ordinateur.  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet":::
           NuGet
        :::image-end:::  
        
1.  Ajoutez WebView2 en-tête à votre projet.  
    :::row:::
       :::column span="1":::
          Ouvrez `HelloWebView.cpp` , copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` après la dernière `#include` ligne.  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          La section include doit ressembler à l’extrait de code suivant.  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
Vous êtes prêt à utiliser l’API WebView2 et à la générer.  

### Créer votre exemple d’application vide  

Appuyez `F5` pour générer et exécuter l’exemple d’application.  Une application doit afficher une fenêtre vide.  

:::image type="complex" source="../media/empty-app.png" alt-text="Application vide":::
   Application vide  
:::image-end:::  

## Étape 3: créer un WebView unique dans la fenêtre parent  

Ajoutez un WebView à la fenêtre principale.  Utilisez la `CreateCoreWebView2Environment` méthode de configuration de l’environnement et recherchez le navigateur Microsoft Edge \ (chrome \) qui alimente le contrôle.  Vous pouvez également utiliser la `CreateCoreWebView2EnvironmentWithOptions` méthode si vous souhaitez spécifier l’emplacement du navigateur, le dossier utilisateur, les indicateurs du navigateur, etc., au lieu d’utiliser le paramètre par défaut.  À l’issue de la `CreateCoreWebView2Environment` méthode, vous pouvez exécuter la `ICoreWebView2Environment::CreateCoreWebView2Controller` méthode dans le `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` rappel et exécuter la `ICoreWebView2Controller::get_CoreWebView2` méthode pour obtenir le WebView associé.  

Dans le rappel, définissez quelques paramètres supplémentaires, redimensionnez le WebView de sorte qu’il prenne 100% de la fenêtre parente, puis naviguez vers Bing.  

Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` l’après `// <-- WebView2 sample code starts here -->` et avant la `// <-- WebView2 sample code ends here -->` note.  

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


### Créer votre application Bing Sample  

Appuyez `F5` pour générer et exécuter l’application.  Vous disposez maintenant d’une fenêtre WebView affichant la page Bing.  

:::image type="complex" source="../media/bing-window.png" alt-text="Fenêtre Bing":::
   Fenêtre Bing  
:::image-end:::  

## Étape 4: événements de navigation  

L’équipe WebView a déjà abordé la navigation vers l’URL à l’aide `ICoreWebView2::Navigate` de la méthode de la dernière étape.  Dans le cadre de la navigation, WebView déclenche une séquence d’événements que l’hôte est susceptible d’écouter.  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

Pour plus d’informations, voir [événements de navigation][Webview2ConceptsNavigationEvents].  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   Événements de navigation  
:::image-end:::  

Dans les cas d’erreur, un ou plusieurs des événements suivants risquent de se produire selon que la navigation se poursuit sur une page d’erreur.  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

Dans le cas d’une redirection HTTP, il existe plusieurs `NavigationStarting` événements dans une ligne.  

En guise d’exemple d’utilisation des événements, inscrivez un gestionnaire pour l' `NavigationStarting` événement afin d’annuler toute demande non HTTPS.  Copiez l’extrait de code suivant, puis collez-le dans `HelloWebView.cpp` .  

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

À présent, l’application ne navigue pas vers des sites non HTTPS.  Vous pouvez utiliser le même mécanisme pour effectuer d’autres tâches, comme limiter la navigation à l’intérieur de votre propre domaine.  

## Étape 5: création de scripts  

L’application d’hébergement risque également d’injecter du JavaScript dans WebView.  Vous pouvez effectuer une tâche WebView pour exécuter du code JavaScript arbitraire ou ajouter des scripts d’initialisation.  Les scripts d’initialisation ajoutés s’appliquent à tous les futurs documents de niveau supérieur et navigation de cadre enfant jusqu’à leur suppression, puis exécutés après la création de l’objet global et avant l’exécution de tout autre script fourni par le document HTML.  

Copiez l’extrait de code suivant, puis collez-le dans `HelloWebView.cpp` .  

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

Le contrôle WebView devrait alors toujours figer l' `Object` objet et renvoyer le document de page une seule fois.  

> [!NOTE] 
> Les API d’injection de script \ (et certaines autres API WebView2 \) sont asynchrones, vous devez utiliser des rappels si le code doit être exécuté dans un ordre spécifique.  

## Étape 6: communication entre l’hôte et le contenu Web  

L’hôte et le contenu Web risquent également de communiquer entre eux par le biais de la `postMessage` méthode.  Le contenu Web exécuté au sein d’un WebView peut être publié sur l’hôte par le biais de la `window.chrome.webview.postMessage` méthode, et le message est géré par tout `ICoreWebView2WebMessageReceivedEventHandler` Gestionnaire d’événements enregistré sur l’hôte.  De même, l’hôte peut traiter le contenu Web via `ICoreWebView2::PostWebMessageAsString` ou la `ICoreWebView2::PostWebMessageAsJSON` méthode, qui est interceptée par des gestionnaires ajoutés de l' `window.chrome.webview.addEventListener` écouteur.  Le mécanisme de communication permet au contenu Web d’utiliser les fonctionnalités natives en passant des messages pour demander à l’hôte d’appeler des API natives.  

Pour comprendre le mécanisme, les étapes suivantes se produisent lorsque vous tentez d’imprimer l’URL du document dans WebView.  

1.  L’hôte inscrit un gestionnaire pour renvoyer le message reçu au contenu Web.  
1.  L’hôte injecte un script dans le contenu Web qui inscrit un gestionnaire pour imprimer le message à partir de l’hôte.  
1.  L’hôte injecte un script dans le contenu Web qui publie l’URL sur l’hôte.  
1.  Le gestionnaire de l’hôte est déclenché et renvoie le message \ (URL \) du contenu Web.  
1.  Le gestionnaire du contenu Web est déclenché et imprime le message de l’hôte \ (URL \)  

Copiez l’extrait de code suivant, puis collez-le dans `HelloWebView.cpp` .    

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

### Créer votre exemple d’application d’URL d’affichage  

Appuyez `F5` pour générer et exécuter l’application.  L’URL s’affiche dans une fenêtre contextuelle avant d’accéder à une page.  

:::image type="complex" source="../media/show-url.png" alt-text="Afficher l’URL":::
   Afficher l’URL  
:::image-end:::  

Félicitations, vous venez de créer votre première application WebView2.  

## Étapes suivantes  

La plupart des fonctionnalités WebView2 qui ne sont pas abordées sur cette page, la section suivante a fourni des ressources supplémentaires.  

### Voir également  

*   Pour obtenir un exemple complet de fonctionnalités WebView2, consultez l' [exemple d’API WebView2][GithubMicrosoftedgeWebview2samplesApisample].  
*   Pour obtenir un exemple d’application généré à l’aide de WebView2, voir [WebView2Browser][GithubMicrosoftedgeWebview2browser].  
*   Pour plus d’informations sur l’API WebView2, voir informations de référence sur les [API][Webview2ReferenceWin3209538].  

## Contacter l’équipe WebView2  

Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires!  Visitez le site de [Commentaires référentiel Samples][GithubMicrosoftedgeWebviewfeedback] sur GitHub pour envoyer des demandes de fonctionnalité ou des rapports de bogues, ou pour rechercher des problèmes connus.  

<!-- links -->  

[Webview2Index]: ../index.md "Introduction à Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Référence (WebView2) | Documents Microsoft"  
[Webview2ConceptsNavigationEvents]: ../concepts/navigation-events.md "Événements de navigation | Documents Microsoft"  

[CppCxWrlTemplateLibraryVS2019]: /cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019 "Bibliothèque de modèles C++ Windows Runtime (WRL) | Documents Microsoft"  
[CppWindowsWalkthroughCreatingDesktopApplication]: /cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019 "Procédure pas à pas: création d’une application de bureau Windows classique (C++) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2browser]: https://github.com/MicrosoftEdge/WebView2Browser "WebView2Browser-MicrosoftEdge/WebView2Browser | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample "Exemple d’API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesGettingStartedGuide]: https://github.com/MicrosoftEdge/WebView2Samples#1-getting-started-guide "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftWilMain]: https://github.com/Microsoft/wil "Bibliothèques d’implémentation Windows (WIL)-Microsoft/Wil | GitHub"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[MicrosoftVisualstudioMain]: https://visualstudio.microsoft.com "Visual Studio"  
