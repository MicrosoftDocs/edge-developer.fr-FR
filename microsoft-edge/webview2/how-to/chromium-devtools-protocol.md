---
description: Découvrez comment utiliser le protocole Chrome DevTools dans vos applications WebView2 à l’aide du package NuGet du protocole Chromium DevTools de Microsoft Edge WebView2
title: Utiliser le protocole Chrome DevTools dans WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: cd59bc0d177d17680222fcff8452c2cf8d56b195
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535912"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a>Utiliser le protocole Chromium DevTools dans WebView2  

Le [protocole Chromium DevTools][GitHubChromedevtoolsDevtoolsProtocol] fournit des API pour instrumenter, inspecter, déboguer et profiler les navigateurs basés sur Chromium.  Le protocole Chromium DevTools est la base de Microsoft Edge \(Chromium\) DevTools.  Utilisez le protocole Chromium DevTools pour les fonctionnalités qui ne sont pas implémentées dans la plateforme WebView2.  Pour plus d’informations sur la fonctionnalité de protocole Chromium DevTools, accédez au protocole [Chromium DevTools.][GitHubChromedevtoolsDevtoolsProtocol]  

> [!CAUTION]
> L’équipe Microsoft Edge WebView2 ne tient pas à jour ou ne prend pas en charge le protocole Chromium DevTools.  Le protocole Chromium DevTools est maintenu par le projet Chromium open source.  
> 
> Pour envoyer vos suggestions pour les futures fonctionnalités de la plateforme WebView2, accédez aux commentaires [WebView][GithubMicrosoftedgeWebview2feedback] et soumettez un problème.  

Pour utiliser l’API de protocole Chromium DevTools dans WebView2, utilisez l’une des actions suivantes.  

*   Installez et utilisez le package [NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] \(.NET\).  
*   Exécutez l’une des méthodes suivantes.  
    *   .NET :  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]  
    *   Win32 C/C++ :  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]  
    
## <a name="use-devtoolsprotocolhelper-preview"></a>Utiliser DevToolsProtocolHelper (Aperçu)

> [!NOTE]
> Le package [NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] est actuellement en prévisualisation technique.  Pendant la prévisualisation, évitez d’utiliser le package dans les applications de production.

[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] est un package NuGet créé par l’équipe WebView2 qui fournit un accès facile aux fonctionnalités du protocole Chromium DevTools.  Les exemples suivants décrivent comment utiliser la fonctionnalité de géolocalisation dans le protocole Chromium DevTools dans votre contrôle WebView2.  Vous pouvez suivre un modèle similaire pour utiliser d’autres fonctionnalités du protocole Chromium DevTools.  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a>Étape 1 : Créer une page web pour trouver votre géolocalisation  

Pour créer un `HTML file` pour trouver votre géolocalisation, terminez en suivant les actions.  

1.  Ouvrez Visual Studio Code \(ou un IDE de votre choix\).  
1.  Créez un `.html` fichier.  
1.  Copiez et collez l’extrait de code suivant dans votre nouveau `.html` fichier.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <title>Geolocation Finder</title>
    </head>
    <body>
        <button id="display">Display Location</button>
        <div id="message"></div>
    </body>
    
    <script>
        const btn = document.getElementById('display');
        // Find the user location.
        btn.addEventListener('click', function () {
            navigator.geolocation.getCurrentPosition(onSuccess, onError);
        });
        
        // Update message to display the latitude and longitude coordinates.
        function onSuccess(position) {
            const {latitude, longitude} = position.coords;
            message.textContent = `Your location: (${latitude},${longitude})`;
        }
        
        function onError() {
            message.textContent = `Operation Failed`;
        }
    </script>
    </html>
    ```  
    
1.  Enregistrez `.html` le fichier avec le nom de fichier `geolocation.html` .  
1.  Ouvrez MicrosoftEdge.  
1.  Ouvrez le fichier `geolocation.html`.  
1.  Pour afficher vos coordonnées de latitude et de longitude, choisissez le **bouton Emplacement d’affichage.**  Pour vérifier et comparer votre géolocalisation, copiez et collez vos coordonnées dans [https://www.bing.com/maps][BingMaps] .  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Afficher les coordonnées de géolocalisation de l’utilisateur dans Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       Afficher les coordonnées de géolocalisation de l’utilisateur dans Microsoft Edge  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a>Étape 2 : Afficher geolocation.html dans un contrôle WebView2  

1.  Pour créer une application WebView2, utilisez l’un des guides de prise en page suivants ou des exemples WebView2.  
    *   [Mise en place de WebView2 dans Windows Forms][Webview2GetStartedWinforms]  
    *   [Mise en place de WebView2 dans WPF][Webview2GetStartedWpf]  
    *   [Exemples WebView2][GithubMicrosoftedgeWebview2samples]  
        
1.  Définissez la navigation initiale du contrôle WebView2 sur `geolocation.html` .  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  `geolocation.html`Assurez-vous que le fichier s’affiche dans votre application de contrôle WebView2.  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Afficher le geolocater.html dans votre application de contrôle WebView2" lightbox="./media/initial-geolocate.png":::
       Afficher le `geolocation.html` fichier dans votre application de contrôle WebView2  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a>Étape 3 : Installer le package NuGet DevToolsProtocolHelper  

Utilisez NuGet pour télécharger `Microsoft.Web.WebView2.DevToolsProtocolExtension` .  Pour installer le package, effectuer les actions suivantes.  

1.  Choose **Project**  >  **Manage NuGet Packages**  >  **Browse**.  
1.  Tapez `Microsoft.Web.WebView2.DevToolsProtocolExtension` et choisissez **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.   
    
:::image type="complex" source="./media/cdp-nuget.png" alt-text="Assurez-vous que Microsoft.Web.WebView2.DevToolsProtocolExtension s’affiche dans la Visual Studio NuGet Gestionnaire de package" lightbox="./media/cdp-nuget.png":::
   **Assurez-vous que Microsoft.Web.WebView2.DevToolsProtocolExtension** s’affiche dans la Visual Studio NuGet Gestionnaire de package  
:::image-end:::    

## <a name="step-4-use-devtools-protocol-helper"></a>Étape 4 : Utiliser l’aide du protocole DevTools  

1.  Ajoutez `DevToolsProtocolExtension` l’espace de noms à votre projet.  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  Ins instantiate the `DevToolsProtocolHelper` object and navigate to `geolocation.html` .  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  Exécutez [la méthode setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]  Pour plus d’informations, accédez [à setGeolocationOverride.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webview.CoreWebView2.GetDevToolsProtocolHelper();
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
        
        // Latitude and longitude for Paris, France.
        double latitude = 48.857024082572565;  
        double longitude = 2.3161581601457386;  
        double accuracy = 1;
        await helper.Emulation.setGeolocationOverrideAsync(latitude, longitude, accuracy);
        
    }
    ```  
    
1.  Exécutez votre application.  
1.  Pour afficher les coordonnées de Paris, en France, sélectionnez le **bouton Emplacement d’affichage.**  
    
    :::image type="complex" source="./media/final-location-cdp.png" alt-text="Afficher le .html dans un contrôle WebView2 avec les coordonnées de Paris" lightbox="./media/final-location-cdp.png":::
       Afficher le `.html` fichier dans un contrôle WebView2 avec les coordonnées de Paris  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a>Fichier d’un bogue de protocole Chromium DevTools  

L’équipe WebView2 ne possède pas le protocole Chromium DevTools.  

> [!IMPORTANT]
> Direct feedback and bugs to the Chromium Issues repo.  

Pour déposer un bogue ou un problème de protocole Chromium DevTools, effectuer les actions suivantes.  

1.  Fichier [d’un rapport de bogues.][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]  
1.  Accédez [aux commentaires WebView][GithubMicrosoftedgeWebview2feedback] et ouvrez un nouveau problème.  
    
## <a name="see-also"></a>Voir également  

*   [Exemples WebView2][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GetStartedWinforms]: /microsoft-edge/webview2/get-started/winforms "Mise en place de WebView2 dans Windows Forms | Documents Microsoft"  
[Webview2GetStartedWpf]: /microsoft-edge/webview2/get-started/wpf "Mise en place de WebView2 dans WPF | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2.getdevtoolsprotocoleventreceiver?view=webview2-dotnet-1.0.774.44&preserve-view=true "Méthode CoreWebView2.GetDevToolsProtocolEventReceiver(String) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString]: /dotnet/api/microsoft.web.webview2.core.corewebview2.calldevtoolsprotocolmethodasync?view=webview2-dotnet-1.0.774.44&preserve-view=true#Microsoft_Web_WebView2_Core_CoreWebView2_CallDevToolsProtocolMethodAsync_System_String_System_String_ "Méthode CoreWebView2.CallDevToolsProtocolMethodAsync(String, String) | Documents Microsoft"  

[Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-1.0.774.44&preserve-view=true#calldevtoolsprotocolmethod "CallDevToolsProtocolMethod - interface ICoreWebView2 | Documents Microsoft"  
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-1.0.774.44&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  

[BingMaps]: https://www.bing.com/maps "Cartes Bing"  

[GitHubChromedevtoolsDevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Protocole Chrome DevTools | GitHub"  
[GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]: https://chromedevtools.github.io/devtools-protocol/tot/Emulation/#method-setGeolocationOverride "Emulation.setGeolocationOverride - Protocole Chrome DevTools | GitHub"  

[GithubMicrosoftedgeWebview2feedback]: https://github.com/MicrosoftEdge/WebView2Feedback "WebView Feedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples webView2 | GitHub"  

[ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]: https://bugs.chromium.org/p/chromium/issues/entry?components=Platform%3EDevTools%3EPlatform "Rapport de | Bogues Chromium"  

[NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://www.nuget.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | NuGet QA Gallery"  
