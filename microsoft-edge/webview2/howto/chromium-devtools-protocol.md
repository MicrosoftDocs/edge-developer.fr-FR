---
description: Découvrez comment utiliser le protocole Chrome DevTools dans vos applications WebView2 à l’aide du package NuGet du protocole Chromium DevTools de Microsoft Edge WebView2
title: Utiliser le protocole Chrome DevTools dans WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/15/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, edge, ICoreWebView2, ICoreWebView2Controller, Chrome DevTools Protocol
ms.openlocfilehash: 0f7a2dd4bb3b1621e854cd4c0c5410e64d3c03ff
ms.sourcegitcommit: 0ef5bb3933cde8a466f2931b824f07b4995cfe5e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "11409311"
---
# <a name="use-chromium-devtools-protocol-in-webview2"></a><span data-ttu-id="b38fb-104">Utiliser le protocole Chromium DevTools dans WebView2</span><span class="sxs-lookup"><span data-stu-id="b38fb-104">Use Chromium DevTools Protocol in WebView2</span></span>  

<span data-ttu-id="b38fb-105">Le [protocole Chromium DevTools][GitHubChromedevtoolsDevtoolsProtocol] fournit des API pour instrumenter, inspecter, déboguer et profiler les navigateurs basés sur Chromium.</span><span class="sxs-lookup"><span data-stu-id="b38fb-105">The [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol] provides APIs to instrument, inspect, debug, and profile Chromium-based browsers.</span></span>  <span data-ttu-id="b38fb-106">Le protocole Chromium DevTools est la base de Microsoft Edge \(Chromium\) DevTools.</span><span class="sxs-lookup"><span data-stu-id="b38fb-106">The Chromium DevTools Protocol is the foundation for the Microsoft Edge \(Chromium\) DevTools.</span></span>  <span data-ttu-id="b38fb-107">Utilisez le protocole Chromium DevTools pour les fonctionnalités qui ne sont pas implémentées dans la plateforme WebView2.</span><span class="sxs-lookup"><span data-stu-id="b38fb-107">Use the Chromium DevTools Protocol for features that aren't implemented in the WebView2 platform.</span></span>  <span data-ttu-id="b38fb-108">Pour plus d’informations sur la fonctionnalité de protocole Chromium DevTools, accédez au protocole [Chromium DevTools.][GitHubChromedevtoolsDevtoolsProtocol]</span><span class="sxs-lookup"><span data-stu-id="b38fb-108">For more information about the Chromium DevTools Protocol functionality, navigate to [Chromium DevTools Protocol][GitHubChromedevtoolsDevtoolsProtocol].</span></span>  

> [!CAUTION]
> <span data-ttu-id="b38fb-109">L’équipe Microsoft Edge WebView2 ne tient pas à jour ou ne prend pas en charge le protocole Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="b38fb-109">The Microsoft Edge WebView2 team does not maintain or support the Chromium DevTools Protocol.</span></span>  <span data-ttu-id="b38fb-110">Le protocole Chromium DevTools est maintenu par le projet Chromium open source.</span><span class="sxs-lookup"><span data-stu-id="b38fb-110">The Chromium DevTools Protocol is maintained by the open source Chromium project.</span></span>  
> 
> <span data-ttu-id="b38fb-111">Pour envoyer vos suggestions pour les futures fonctionnalités de la plateforme WebView2, accédez aux commentaires [WebView][GithubMicrosoftedgeWebview2feedback] et soumettez un problème.</span><span class="sxs-lookup"><span data-stu-id="b38fb-111">To send your suggestions for future WebView2 platform features, navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and submit an issue.</span></span>  

<span data-ttu-id="b38fb-112">Pour utiliser l’API de protocole Chromium DevTools dans WebView2, utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b38fb-112">To use the Chromium DevTools Protocol API in WebView2, use either of the following actions.</span></span>  

*   <span data-ttu-id="b38fb-113">Installez et utilisez le package [NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] \(.NET\).</span><span class="sxs-lookup"><span data-stu-id="b38fb-113">Install and use the [Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package \(.NET\).</span></span>  
*   <span data-ttu-id="b38fb-114">Exécutez l’une des méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b38fb-114">Run one of the following methods.</span></span>  
    *   <span data-ttu-id="b38fb-115">.NET :  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span><span class="sxs-lookup"><span data-stu-id="b38fb-115">.NET:  [CallDevToolsProtocolAsync][DotnetApiMicrosoftWebWebview2CoreCorewebview2CalldevtoolsprotocolmethodasyncViewWebview2Dotnet1077444MicrosoftWebWebView2CoreCorewebview2CalldevtoolsprotocolmethodsyncSystemStringSystemString], [GetDevToolsProtocolEventReceiver][DotnetApiMicrosoftWebWebview2CoreCorewebview2GetdevtoolsprotocoleventreceiverViewWebview2Dotnet1077444]</span></span>  
    *   <span data-ttu-id="b38fb-116">Win32 C/C++ :  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span><span class="sxs-lookup"><span data-stu-id="b38fb-116">Win32 C/C++:  [CallDevToolsProtocolMethod][Webview2ReferenceWin32Icorewebview2ViewWebview21077444Calldevtoolsprotocolmethod], [ICoreWebView2DevToolsProtocolEventReceiver][Webview2ReferenceWin32Icorewebview2devtoolsprotocoleventreceiverViewWebview21077444]</span></span>  
    
## <a name="use-devtoolsprotocolhelper-preview"></a><span data-ttu-id="b38fb-117">Utiliser DevToolsProtocolHelper (Aperçu)</span><span class="sxs-lookup"><span data-stu-id="b38fb-117">Use DevToolsProtocolHelper (Preview)</span></span>

> [!NOTE]
> <span data-ttu-id="b38fb-118">Le package [NuGet Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] est actuellement en prévisualisation technique.</span><span class="sxs-lookup"><span data-stu-id="b38fb-118">The [Microsoft.Web.WebView2.DevToolsProtocolExtension][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] NuGet package is currently in technical preview.</span></span>  <span data-ttu-id="b38fb-119">Pendant la prévisualisation, évitez d’utiliser le package dans les applications de production.</span><span class="sxs-lookup"><span data-stu-id="b38fb-119">While in preview, refrain from using the package in production apps.</span></span>

<span data-ttu-id="b38fb-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] est un package NuGet créé par l’équipe WebView2 qui fournit un accès facile aux fonctionnalités du protocole Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="b38fb-120">[Microsoft.Web.WebView2.DevToolsProtocolExtension (Preview)][NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension] is a NuGet package created by the WebView2 team that provides easy access to Chromium DevTools Protocol features.</span></span>  <span data-ttu-id="b38fb-121">Les exemples suivants décrivent comment utiliser la fonctionnalité de géolocalisation dans le protocole Chromium DevTools dans votre contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="b38fb-121">The following examples describe how to use the geolocation functionality in Chromium DevTools Protocol in your WebView2 control.</span></span>  <span data-ttu-id="b38fb-122">Vous pouvez suivre un modèle similaire pour utiliser d’autres fonctionnalités du protocole Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="b38fb-122">You may follow a similar pattern to use other Chromium DevTools Protocol features.</span></span>  

## <a name="step-1-create-a-webpage-to-find-your-geolocation"></a><span data-ttu-id="b38fb-123">Étape 1 : Créer une page web pour trouver votre géolocalisation</span><span class="sxs-lookup"><span data-stu-id="b38fb-123">Step 1: Create a webpage to find your geolocation</span></span>  

<span data-ttu-id="b38fb-124">Pour créer un `HTML file` pour trouver votre géolocalisation, terminez en suivant les actions.</span><span class="sxs-lookup"><span data-stu-id="b38fb-124">To create an `HTML file` to find your geolocation, complete following the actions.</span></span>  

1.  <span data-ttu-id="b38fb-125">Ouvrez Visual Studio Code \(ou un IDE de votre choix\).</span><span class="sxs-lookup"><span data-stu-id="b38fb-125">Open Visual Studio Code \(or an IDE of your choice\).</span></span>  
1.  <span data-ttu-id="b38fb-126">Créez un `.html` fichier.</span><span class="sxs-lookup"><span data-stu-id="b38fb-126">Create a new `.html` file.</span></span>  
1.  <span data-ttu-id="b38fb-127">Copiez et collez l’extrait de code suivant dans votre nouveau `.html` fichier.</span><span class="sxs-lookup"><span data-stu-id="b38fb-127">Copy and paste the following code snippet in your new `.html` file.</span></span>  
    
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
    
1.  <span data-ttu-id="b38fb-128">Enregistrez `.html` le fichier avec le nom de fichier `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="b38fb-128">Save the `.html` file with the filename `geolocation.html`.</span></span>  
1.  <span data-ttu-id="b38fb-129">Ouvrez MicrosoftEdge.</span><span class="sxs-lookup"><span data-stu-id="b38fb-129">Open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="b38fb-130">Ouvrez le fichier `geolocation.html`.</span><span class="sxs-lookup"><span data-stu-id="b38fb-130">Open the `geolocation.html` file.</span></span>  
1.  <span data-ttu-id="b38fb-131">Pour afficher vos coordonnées de latitude et de longitude, choisissez le **bouton Emplacement d’affichage.**</span><span class="sxs-lookup"><span data-stu-id="b38fb-131">To display your latitude and longitude coordinates, choose the **Display Location** button.</span></span>  <span data-ttu-id="b38fb-132">Pour vérifier et comparer votre géolocalisation, copiez et collez vos coordonnées dans [https://www.bing.com/maps][BingMaps] .</span><span class="sxs-lookup"><span data-stu-id="b38fb-132">To verify and compare your geolocation, copy and paste your coordinates in [https://www.bing.com/maps][BingMaps].</span></span>  
    
    :::image type="complex" source="./media/geolocater-browser.png" alt-text="Afficher les coordonnées de géolocalisation de l’utilisateur dans Microsoft Edge" lightbox="./media/geolocater-browser.png":::
       <span data-ttu-id="b38fb-134">Afficher les coordonnées de géolocalisation de l’utilisateur dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b38fb-134">Display the geolocation coordinates of the user in Microsoft Edge</span></span>  
    :::image-end:::  
    
## <a name="step-2-display-geolocationhtml-in-a-webview2"></a><span data-ttu-id="b38fb-135">Étape 2 : Afficher geolocation.html dans un contrôle WebView2</span><span class="sxs-lookup"><span data-stu-id="b38fb-135">Step 2: Display geolocation.html in a WebView2</span></span>  

1.  <span data-ttu-id="b38fb-136">Pour créer une application WebView2, utilisez l’un des guides de mise en service suivants ou des exemples WebView2.</span><span class="sxs-lookup"><span data-stu-id="b38fb-136">To create a WebView2 app, use either of the following getting started guides or WebView2 samples.</span></span>  
    *   [<span data-ttu-id="b38fb-137">Mise en place de WebView2 dans Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b38fb-137">Getting Started with WebView2 in Windows Forms</span></span>][Webview2GettingstartedWinforms]  
    *   [<span data-ttu-id="b38fb-138">Mise en place de WebView2 dans WPF</span><span class="sxs-lookup"><span data-stu-id="b38fb-138">Getting Started with WebView2 in WPF</span></span>][Webview2GettingstartedWpf]  
    *   [<span data-ttu-id="b38fb-139">Exemples WebView2</span><span class="sxs-lookup"><span data-stu-id="b38fb-139">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
        
1.  <span data-ttu-id="b38fb-140">Définissez la navigation initiale du contrôle WebView2 sur `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="b38fb-140">Set the initial navigation of the WebView2 control to `geolocation.html`.</span></span>  
    
    ```csharp
    webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    ```  
    
1.  <span data-ttu-id="b38fb-141">`geolocation.html`Assurez-vous que le fichier s’affiche dans votre application de contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="b38fb-141">Ensure the `geolocation.html` file displays in your WebView2 control app.</span></span>  
    
    :::image type="complex" source="./media/initial-geolocate.png" alt-text="Afficher le geolocater.html dans votre application de contrôle WebView2" lightbox="./media/initial-geolocate.png":::
       <span data-ttu-id="b38fb-143">Afficher le `geolocation.html` fichier dans votre application de contrôle WebView2</span><span class="sxs-lookup"><span data-stu-id="b38fb-143">Display the `geolocation.html` file in your WebView2 control app</span></span>  
    :::image-end:::  
    
## <a name="step-3-install-the-devtoolsprotocolhelper-nuget-package"></a><span data-ttu-id="b38fb-144">Étape 3 : Installer le package NuGet DevToolsProtocolHelper</span><span class="sxs-lookup"><span data-stu-id="b38fb-144">Step 3: Install the DevToolsProtocolHelper NuGet package</span></span>  

<span data-ttu-id="b38fb-145">Utilisez NuGet pour télécharger `Microsoft.Web.WebView2.DevToolsProtocolExtension` .</span><span class="sxs-lookup"><span data-stu-id="b38fb-145">Use NuGet to download `Microsoft.Web.WebView2.DevToolsProtocolExtension`.</span></span>  <span data-ttu-id="b38fb-146">Pour installer le package, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b38fb-146">To install the package, complete the following actions.</span></span>  

1.  <span data-ttu-id="b38fb-147">Choose **Project**  >  **Manage NuGet Packages**  >  **Browse**.</span><span class="sxs-lookup"><span data-stu-id="b38fb-147">Choose **Project** > **Manage NuGet Packages** > **Browse**.</span></span>  
1.  <span data-ttu-id="b38fb-148">Tapez `Microsoft.Web.WebView2.DevToolsProtocolExtension` et choisissez **Microsoft.Web.WebView2.DevToolsProtocolExtension**  >  **Install**.</span><span class="sxs-lookup"><span data-stu-id="b38fb-148">Type `Microsoft.Web.WebView2.DevToolsProtocolExtension` and choose **Microsoft.Web.WebView2.DevToolsProtocolExtension** > **Install**.</span></span>   
    
:::image type="complex" source="./media/cdpnuget.png" alt-text="Assurez-vous que Microsoft.Web.WebView2.DevToolsProtocolExtension s’affiche dans la Visual Studio NuGet Gestionnaire de package" lightbox="./media/cdpnuget.png":::
   <span data-ttu-id="b38fb-150">**Assurez-vous que Microsoft.Web.WebView2.DevToolsProtocolExtension** s’affiche dans la Visual Studio NuGet Gestionnaire de package</span><span class="sxs-lookup"><span data-stu-id="b38fb-150">Ensure **Microsoft.Web.WebView2.DevToolsProtocolExtension** displays in the Visual Studio NuGet Package Manager</span></span>  
:::image-end:::  

## <a name="step-4-use-devtools-protocol-helper"></a><span data-ttu-id="b38fb-151">Étape 4 : Utiliser l’aide du protocole DevTools</span><span class="sxs-lookup"><span data-stu-id="b38fb-151">Step 4: Use DevTools Protocol Helper</span></span>  

1.  <span data-ttu-id="b38fb-152">Ajoutez `DevToolsProtocolExtension` l’espace de noms à votre projet.</span><span class="sxs-lookup"><span data-stu-id="b38fb-152">Add the `DevToolsProtocolExtension` namespace to your project.</span></span>  
    
    ```csharp
    using Microsoft.Web.WebView2.Core;
    using Microsoft.Web.WebView2.Core.DevToolsProtocolExtension;
    ```  
    
1.  <span data-ttu-id="b38fb-153">Inssérez `DevToolsProtocolHelper` l’objet et accédez à `geolocation.html` .</span><span class="sxs-lookup"><span data-stu-id="b38fb-153">Instantiate the `DevToolsProtocolHelper` object and navigate to `geolocation.html`.</span></span>  
    
    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        DevToolsProtocolHelper helper = webView.CoreWebView2.GetDevToolsProtocolHelper(); 
        
        webView.CoreWebView2.Navigate(@"C:\{path\to\file}\geolocation.html");
    }
    ```  
    
1.  <span data-ttu-id="b38fb-154">Exécutez [la méthode setGeoLocationOverrideAsync.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]</span><span class="sxs-lookup"><span data-stu-id="b38fb-154">Run the [setGeoLocationOverrideAsync][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride] method.</span></span>  <span data-ttu-id="b38fb-155">Pour plus d’informations, accédez [à setGeolocationOverride.][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride]</span><span class="sxs-lookup"><span data-stu-id="b38fb-155">For more information, navigate to [setGeolocationOverride][GithubChromedevtoolsDevtoolsProtocolTotEmulationMethodSetgeolocationoverride].</span></span>  
    
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
    
1.  <span data-ttu-id="b38fb-156">Exécutez votre application.</span><span class="sxs-lookup"><span data-stu-id="b38fb-156">Run your app.</span></span>  
1.  <span data-ttu-id="b38fb-157">Pour afficher les coordonnées de Paris, en France, sélectionnez le **bouton Emplacement d’affichage.**</span><span class="sxs-lookup"><span data-stu-id="b38fb-157">To display the coordinates of Paris, France, choose the **Display Location** button.</span></span>  
    
    :::image type="complex" source="./media/finallocation-cdp.png" alt-text="Afficher le fichier .html dans un contrôle WebView2 avec les coordonnées de Paris" lightbox="./media/finallocation-cdp.png":::
       <span data-ttu-id="b38fb-159">Afficher le `.html` fichier dans un contrôle WebView2 avec les coordonnées de Paris</span><span class="sxs-lookup"><span data-stu-id="b38fb-159">Display the `.html` file in a WebView2 control with the coordinates for Paris</span></span>  
    :::image-end:::  
    
## <a name="file-a-chromium-devtools-protocol-bug"></a><span data-ttu-id="b38fb-160">Fichier d’un bogue de protocole Chromium DevTools</span><span class="sxs-lookup"><span data-stu-id="b38fb-160">File a Chromium DevTools Protocol bug</span></span>  

<span data-ttu-id="b38fb-161">L’équipe WebView2 ne possède pas le protocole Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="b38fb-161">The WebView2 team doesn't own the Chromium DevTools Protocol.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b38fb-162">Diriger les commentaires et les bogues vers le repo Chromium Issues.</span><span class="sxs-lookup"><span data-stu-id="b38fb-162">Direct feedback and bugs to the Chromium Issues repo.</span></span>  

<span data-ttu-id="b38fb-163">Pour déposer un bogue ou un problème de protocole Chromium DevTools, effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b38fb-163">To file a Chromium DevTools Protocol bug or issue, complete the following actions.</span></span>  

1.  <span data-ttu-id="b38fb-164">Fichier [d’un rapport de bogues.][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform]</span><span class="sxs-lookup"><span data-stu-id="b38fb-164">File a [bug report][ChromiumBugsChromiumIssuesEntryComponentsPlatformDevtoolsPlatform].</span></span>  
1.  <span data-ttu-id="b38fb-165">Accédez [aux commentaires WebView][GithubMicrosoftedgeWebview2feedback] et ouvrez un nouveau problème.</span><span class="sxs-lookup"><span data-stu-id="b38fb-165">Navigate to [WebView Feedback][GithubMicrosoftedgeWebview2feedback] and open a new issue.</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="b38fb-166">Voir également</span><span class="sxs-lookup"><span data-stu-id="b38fb-166">See also</span></span>  

*   [<span data-ttu-id="b38fb-167">Exemples WebView2</span><span class="sxs-lookup"><span data-stu-id="b38fb-167">WebView2 samples</span></span>][GithubMicrosoftedgeWebview2samples]  
    
 <!-- links -->  

[Webview2GettingstartedWinforms]: /microsoft-edge/webview2/gettingstarted/winforms "Mise en place de WebView2 dans Windows Forms | Documents Microsoft"  
[Webview2GettingstartedWpf]: /microsoft-edge/webview2/gettingstarted/wpf "Mise en place de WebView2 dans WPF | Documents Microsoft"  

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

[NugettestIntPackagesMicrosoftWebWebView2DevToolsprotocolextension]: https://int.nugettest.org/packages/Microsoft.Web.WebView2.DevToolsProtocolExtension "Microsoft.Web.WebView2.DevToolsProtocolExtension | NuGet QA Gallery"  
