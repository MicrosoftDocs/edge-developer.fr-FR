---
description: Découvrez comment utiliser le protocole Chrome DevTools dans vos applications WebView2 à l’aide du package Microsoft Edge WebView2 Chromium DevTools Protocol NuGet
title: Utiliser le protocole Chrome DevTools dans WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/17/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: 86846ee195406f78d5fd7c369f375ed1e359101a
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536441"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a>Utiliser le protocole Chromium DevTools dans WebView2  

Le [Chromium DevTools fournit][GitHubChromedevtoolsDevtoolsProtocol] des API pour instrumenter, inspecter, déboguer et profiler Chromium navigateurs basés sur les navigateurs.  Le Chromium Protocole DevTools est la base de l’Microsoft Edge \(Chromium\) DevTools.  Utilisez le Chromium protocole DevTools pour les fonctionnalités qui ne sont pas implémentées dans la plateforme WebView2.  Pour plus d’informations sur Chromium fonctionnalités du protocole DevTools, accédez [Chromium protocole DevTools.][GitHubChromedevtoolsDevtoolsProtocol]  

> [!CAUTION]
> L Microsoft Edge WebView2 ne tient pas à jour ou ne prend pas en charge Chromium protocole DevTools.  Le Chromium protocole DevTools est maintenu par le projet d’Chromium open source.  
> 
> Pour envoyer vos suggestions pour les futures fonctionnalités de la plateforme WebView2, accédez aux commentaires [WebView][GithubMicrosoftedgeWebview2feedback] et soumettez un problème.  

Pour utiliser l Chromium API de protocole DevTools dans WebView2, utilisez l’une des actions suivantes.  

*   Installez et utilisez [Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package \(.NET\).  
*   Exécutez l’une des méthodes suivantes.  
    *   .NET :  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]  
    *   Win32 C/C++ :  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]  
    
## <a name="use-devtoolsprotocolhelper-preview"></a>Utiliser DevToolsProtocolHelper (Aperçu)

> [!NOTE]
> Le package [d’NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] est actuellement en prévisualisation technique.  Pendant la prévisualisation, évitez d’utiliser le package dans les applications de production.

[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension] est un package NuGet créé par l’équipe WebView2 qui fournit un accès facile aux fonctionnalités du protocole Chromium DevTools.  Les exemples suivants décrivent comment utiliser la fonctionnalité de géolocalisation dans Chromium protocole DevTools dans votre contrôle WebView2.  Vous pouvez suivre un modèle similaire pour utiliser d’Chromium fonctionnalités du protocole DevTools.  

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

1.  Pour créer une application WebView2, utilisez l’un des guides de mise en service suivants ou des exemples WebView2.  
    *   [Mise en place de WebView2 dans Windows formulaires][Webview2GettingstartedWinforms]  
    *   [Mise en place de WebView2 dans WPF][Webview2GettingstartedWpf]  
    *   [Exemples WebView2][GithubMicrosoftedgeWebview2samples]  
        
1.  Définissez la navigation initiale du contrôle WebView2 sur `geolocation.html` .  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  `geolocation.html`Assurez-vous que le fichier s’affiche dans votre application de contrôle WebView2.  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Afficher le geolocater.html dans votre application de contrôle WebView2" lightbox="./media/initial-geolocate.png":::
       Afficher le `geolocation.html` fichier dans votre application de contrôle WebView2  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a>Étape 3 : Installer le package d’NuGet DevToolsProtocolHelper  

Utilisez NuGet pour télécharger `Microsoft.Web.WebView2.DevToolsProtocolExtension` .  Pour installer le package, effectuer les actions suivantes.  

1.  Choose **Project**  >  **Manage NuGet Packages**  >  **Browse**.  
1.  Tapez `Microsoft.Web.WebView2.DevToolsProtocolExtension` et choisissez **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Assurez-vous que Microsoft.Web.WebView2.DevToolsProtocolExtension s’affiche dans le Visual Studio NuGet Gestionnaire de package" lightbox="./media/cdpnuget.png":::
   **Assurez-vous que Microsoft.Web.WebView2.DevToolsProtocolExtension** s’affiche dans le Visual Studio NuGet Gestionnaire de package  
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
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Afficher le .html dans un contrôle WebView2 avec les coordonnées de Paris" lightbox="./media/finallocation-cdp.png":::
       Afficher le `.html` fichier dans un contrôle WebView2 avec les coordonnées de Paris  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a>Fichier d’Chromium de protocole DevTools  

L’équipe WebView2 ne possède pas Chromium protocole DevTools.  

> [!IMPORTANT]
> Diriger les commentaires et les bogues vers le Chromium problèmes.  

Pour déposer un Chromium ou un problème du protocole DevTools, effectuer les actions suivantes.  

1.  Fichier [d’un rapport de bogues.][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]  
1.  Accédez [aux commentaires WebView][GithubMicrosoftedgeWebview2feedback] et ouvrez un nouveau problème.  
    
## <a name="see-also"></a>Voir également  

*   [Exemples WebView2][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GettingstartedWinforms]: /microsoft-edge/webview2/gettingstarted/winforms "Mise en place de WebView2 dans Windows Forms | Documents Microsoft"  
[Webview2GettingstartedWpf]: /microsoft-edge/webview2/gettingstarted/wpf "Mise en place de WebView2 dans WPF | Documents Microsoft"  

[DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]: /dotnet/api/microsoft.web.webview2.core.corewebview2.getdevtoolsprotocoleventreceiver?view=webview2-dotnet-1.0.774.44&preserve-view=true "Méthode CoreWebView2.GetDevToolsProtocolEventReceiver(String) | Documents Microsoft"  
[DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString]: /dotnet/api/microsoft.web.webview2.core.corewebview2.calldevtoolsprotocolmethodasync?view=webview2-dotnet-1.0.774.44&preserve-view=true#Microsoft_Web_WebView2_Core_CoreWebView2_CallDevToolsProtocolMethodAsync_System_String_System_String_ "Méthode CoreWebView2.CallDevToolsProtocolMethodAsync(String, String) | Documents Microsoft"  

[Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod]: /microsoft-edge/webview2/reference/win32/icorewebview2?view=webview2-1.0.774.44&preserve-view=true#calldevtoolsprotocolmethod "CallDevToolsProtocolMethod - interface ICoreWebView2 | Documents Microsoft"  
[Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]: /microsoft-edge/webview2/reference/win32/icorewebview2devtoolsprotocoleventreceiver?view=webview2-1.0.774.44&preserve-view=true "interface ICoreWebView2DevToolsProtocolEventReceiver | Documents Microsoft"  

[BingMaps]: https://www.bing.com/maps "Bing Cartes"  

[GitHubChromedevtoolsDevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Protocole Chrome DevTools | GitHub"  
[GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]: https://chromedevtools.github.io/devtools-protocol/tot/Emulation/#method-setGeolocationOverride "Emulation.setGeolocationOverride - Protocole Chrome DevTools | GitHub"  

[GithubMicrosoftedgeWebview2feedback]: https://github.com/MicrosoftEdge/WebView2Feedback "WebView Feedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples webView2 | GitHub"  

[ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]: https://bugs.chromium.org/p/chromium/issues/entry?components=Platform%3EDevTools%3EPlatform "Rapport de | Chromium Bogues"  

[NugetPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://www.nuget.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | NuGet Galerie QA"  
