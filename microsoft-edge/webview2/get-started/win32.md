---
description: Guide de mise en ligne avec WebView2 pour les applications Win32
title: Mise en place de WebView2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Controller, browser control, edge html
ms.openlocfilehash: 2714f9a6cffea3cb7d53f9a4128d64920fd02dce
ms.sourcegitcommit: 7713eec634264b0c44b1bb426f5b466c44b4e005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/26/2021
ms.locfileid: "11618385"
---
# <a name="get-started-with-webview2"></a><span data-ttu-id="b4bfb-104">Mise en place de WebView2</span><span class="sxs-lookup"><span data-stu-id="b4bfb-104">Get started with WebView2</span></span>  

<span data-ttu-id="b4bfb-105">Dans cet article, commencer à créer votre première application WebView2 et en savoir plus sur les principales fonctionnalités de [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span><span class="sxs-lookup"><span data-stu-id="b4bfb-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2][MicrosoftDeveloperMicrosoftEdgeWebview2].</span></span>  <span data-ttu-id="b4bfb-106">Pour plus d’informations sur les API WebView2 individuelles, accédez à la [référence d’API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="b4bfb-106">For more information about individual WebView2 APIs, navigate to [API reference][Webview2ReferenceWin32].</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="b4bfb-107">Prérequis</span><span class="sxs-lookup"><span data-stu-id="b4bfb-107">Prerequisites</span></span>  

<span data-ttu-id="b4bfb-108">Veillez à installer la liste des conditions préalables suivante avant de poursuivre.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-108">Ensure you install the following list of pre-requisites before proceeding.</span></span>  

*   <span data-ttu-id="b4bfb-109">[WebView2 Runtime][Webview2Installer] ou tout canal [Microsoft Edge (Chromium) non stable][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \(actuellement Windows 10, Windows 8.1 et Windows 7\).</span><span class="sxs-lookup"><span data-stu-id="b4bfb-109">[WebView2 Runtime][Webview2Installer] or any [Microsoft Edge (Chromium) non-stable channel][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
*   <span data-ttu-id="b4bfb-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 ou ultérieure avec la prise en charge de C++ installée.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  
    
## <a name="step-1---create-a-single-window-app"></a><span data-ttu-id="b4bfb-111">Étape 1 : créer une application à fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="b4bfb-111">Step 1 - Create a single-window app</span></span>  

<span data-ttu-id="b4bfb-112">Commencez par un projet de bureau de base qui contient une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-112">Start with a basic desktop project that contains a single main window.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b4bfb-113">Pour mieux concentrer la procédure pas à pas, utilisez l’exemple de code modifié de la procédure pas à pas : créer une application de bureau Windows classique [(C++)][CppWindowsWalkthroughCreatingDesktopApplication] pour votre exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-113">To better focus the walkthrough, use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="b4bfb-114">Pour télécharger l’exemple modifié et commencer, accédez à [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="b4bfb-114">To download the modified sample and get started, navigate to [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

1.  <span data-ttu-id="b4bfb-115">Dans Visual Studio, ouvrez `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="b4bfb-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  
    <span data-ttu-id="b4bfb-116">Si vous utilisez une version antérieure de Visual Studio, pointez sur le projet **WebView2GettingStarted,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="b4bfb-116">If you use an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and choose **Properties**.</span></span>  <span data-ttu-id="b4bfb-117">Sous **Propriétés**de configuration générales, modifiez Windows version du SDK et du jeu d’outils de plateforme pour utiliser le  >  \*\*\*\* SDK Win10 et Visual Studio’outils disponibles. \*\*\*\* \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="b4bfb-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset available to you.</span></span>  
    
:::image type="complex" source="../media/tool-version.png" alt-text="Version de l’outil" lightbox="../media/tool-version.png":::
   <span data-ttu-id="b4bfb-119">Version de l’outil</span><span class="sxs-lookup"><span data-stu-id="b4bfb-119">Tool version</span></span>  
:::image-end:::      

<span data-ttu-id="b4bfb-120">Visual Studio peut afficher des erreurs, car le fichier d’en-tête WebView2 manque dans votre projet.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-120">Visual Studio may display errors, because your project is missing the WebView2 header file.</span></span>  <span data-ttu-id="b4bfb-121">Les erreurs doivent être corrigées après [l’étape 2.](#step-2---install-webview2-sdk)</span><span class="sxs-lookup"><span data-stu-id="b4bfb-121">The errors should be fixed after [Step 2](#step-2---install-webview2-sdk).</span></span>  

## <a name="step-2---install-webview2-sdk"></a><span data-ttu-id="b4bfb-122">Étape 2 : installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="b4bfb-122">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="b4bfb-123">Ajoutez le SDK WebView2 au projet.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-123">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="b4bfb-124">Utilisez NuGet pour installer le SDK Win32.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-124">Use NuGet to install the Win32 SDK.</span></span>  

1.  <span data-ttu-id="b4bfb-125">Pointez sur le projet, ouvrez le menu contextuel \(clic droit\), puis choisissez **Gérer NuGet packages.**</span><span class="sxs-lookup"><span data-stu-id="b4bfb-125">Hover on the project, open the contextual menu \(right-click\), and choose **Manage NuGet Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Gérer des packages NuGet" lightbox="../media/manage-nuget-packages.png":::
       <span data-ttu-id="b4bfb-127">Gérer des packages NuGet</span><span class="sxs-lookup"><span data-stu-id="b4bfb-127">Manage NuGet packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="b4bfb-128">Installez la bibliothèque Windows d’implémentation de l’application.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-128">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="b4bfb-129">Dans la barre de recherche, `Microsoft.Windows.ImplementationLibrary` tapez > **choisissez Microsoft.Windows. ImplementationLibrary**.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-129">In the search bar, type `Microsoft.Windows.ImplementationLibrary` > choose **Microsoft.Windows.ImplementationLibrary**.</span></span>  
    1.  <span data-ttu-id="b4bfb-130">Dans la fenêtre de droite, choisissez **Installer.**</span><span class="sxs-lookup"><span data-stu-id="b4bfb-130">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="b4bfb-131">NuGet télécharge la bibliothèque sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-131">NuGet downloads the library to your machine.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="b4bfb-132">La [Windows d’implémentation et][GithubMicrosoftWilMain] Windows bibliothèque de modèles [C++ runtime][CppCxWrlTemplateLibraryVS2019] sont facultatives et facilitent l’exécution de COM pour l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-132">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Windows Bibliothèque d’implémentation" lightbox="../media/wil.png":::
           <span data-ttu-id="b4bfb-134">Windows Bibliothèque d’implémentation</span><span class="sxs-lookup"><span data-stu-id="b4bfb-134">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="b4bfb-135">Installez le SDK WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-135">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="b4bfb-136">Dans la barre de recherche, `Microsoft.Web.WebView2` tapez > **choisissez Microsoft.Web.WebView2**.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-136">In the search bar, type `Microsoft.Web.WebView2` > choose **Microsoft.Web.WebView2**.</span></span>  
    1.  <span data-ttu-id="b4bfb-137">Dans la fenêtre de droite, choisissez **Installer.**</span><span class="sxs-lookup"><span data-stu-id="b4bfb-137">In the right-hand side window, choose **Install**.</span></span>  <span data-ttu-id="b4bfb-138">NuGet télécharge le SDK sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-138">NuGet downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet Gestionnaire de package" lightbox="../media/nuget.png":::
           <span data-ttu-id="b4bfb-140">NuGet Gestionnaire de package</span><span class="sxs-lookup"><span data-stu-id="b4bfb-140">NuGet Package Manager</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="b4bfb-141">Ajoutez l’en-tête WebView2 à votre projet.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-141">Add WebView2 header to your project.</span></span>  
    
    :::row:::
       :::column span="1":::
          <span data-ttu-id="b4bfb-142">Dans le fichier, copiez l’extrait de code suivant et `HelloWebView.cpp` collez-le après la dernière `#include` ligne.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-142">In the `HelloWebView.cpp` file, copy the following code snippet and paste it after the last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="b4bfb-143">La section Include doit ressembler à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-143">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="b4bfb-144">Prêt à être utilisé et à créer avec l’API WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-144">Ready to use and build against the WebView2 API.</span></span>  

### <a name="build-your-empty-sample-app"></a><span data-ttu-id="b4bfb-145">Créer votre exemple d’application vide</span><span class="sxs-lookup"><span data-stu-id="b4bfb-145">Build your empty sample app</span></span>  

<span data-ttu-id="b4bfb-146">Pour créer et exécuter l’exemple d’application, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="b4bfb-146">To build and run the sample app, select `F5`.</span></span>  <span data-ttu-id="b4bfb-147">Votre application affiche une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-147">Your app displays an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Application vide" lightbox="../media/empty-app.png":::
   <span data-ttu-id="b4bfb-149">Application vide</span><span class="sxs-lookup"><span data-stu-id="b4bfb-149">Empty app</span></span>  
:::image-end:::    

## <a name="step-3---create-a-single-webview-within-the-parent-window"></a><span data-ttu-id="b4bfb-150">Étape 3 : créer un seul WebView dans la fenêtre parent</span><span class="sxs-lookup"><span data-stu-id="b4bfb-150">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="b4bfb-151">Ajoutez un WebView à la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-151">Add a WebView to the main window.</span></span>  

<span data-ttu-id="b4bfb-152">Utilisez la méthode pour configurer l’environnement et `CreateCoreWebView2Environment` localiser le navigateur Microsoft Edge \(Chromium\) sur le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-152">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="b4bfb-153">Vous pouvez également utiliser la méthode si vous souhaitez spécifier l’emplacement du navigateur, le dossier utilisateur, les indicateurs de navigateur, etc., au lieu d’utiliser le `CreateCoreWebView2EnvironmentWithOptions` paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-153">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="b4bfb-154">À la fin de la méthode, exécutez la méthode à l’intérieur du rappel et exécutez la méthode pour obtenir le `CreateCoreWebView2Environment` `ICoreWebView2Environment::CreateCoreWebView2Controller` `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` `ICoreWebView2Controller::get_CoreWebView2` WebView associé.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-154">Upon the completion of the `CreateCoreWebView2Environment` method, run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="b4bfb-155">Dans le rappel, définissez quelques paramètres de plus, resizez le WebView pour prendre 100 % de la fenêtre parente et accédez à Bing.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-155">In the callback, set a few more settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="b4bfb-156">Copiez l’extrait de code suivant et collez-le après `HelloWebView.cpp` le commentaire et avant le `// <-- WebView2 sample code starts here -->` `// <-- WebView2 sample code ends here -->` commentaire.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-156">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` comment and before the `// <-- WebView2 sample code ends here -->` comment.</span></span>  

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

### <a name="build-your-bing-sample-app"></a><span data-ttu-id="b4bfb-157">Créer votre exemple Bing application</span><span class="sxs-lookup"><span data-stu-id="b4bfb-157">Build your Bing sample app</span></span>  

<span data-ttu-id="b4bfb-158">Pour créer et exécuter l’application, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="b4bfb-158">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="b4bfb-159">Vous avez maintenant une fenêtre WebView qui affiche la Bing page.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-159">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Bing fenêtre" lightbox="../media/bing-window.png":::
   <span data-ttu-id="b4bfb-161">Bing fenêtre</span><span class="sxs-lookup"><span data-stu-id="b4bfb-161">Bing window</span></span>  
:::image-end:::    

## <a name="step-4---navigation-events"></a><span data-ttu-id="b4bfb-162">Étape 4 : événements de navigation</span><span class="sxs-lookup"><span data-stu-id="b4bfb-162">Step 4 - Navigation events</span></span>  

<span data-ttu-id="b4bfb-163">L’équipe WebView a déjà abordé la navigation vers l’URL à l’aide `ICoreWebView2::Navigate` de la méthode de la dernière étape.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-163">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="b4bfb-164">Lors de la navigation, WebView déclenche une séquence d’événements que l’hôte peut écouter.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-164">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   
    
<span data-ttu-id="b4bfb-165">Pour plus d’informations, accédez aux [événements de navigation.][Webview2ConceptsNavigationEvents]</span><span class="sxs-lookup"><span data-stu-id="b4bfb-165">For more information, navigate to [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation" lightbox="../media/navigation-events.png":::
   <span data-ttu-id="b4bfb-167">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="b4bfb-167">Navigation events</span></span>  
:::image-end:::    

<span data-ttu-id="b4bfb-168">Dans les cas d’erreur, un ou plusieurs des événements suivants peuvent se produire selon que la navigation se poursuit jusqu’à une page web d’erreur.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-168">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error webpage.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`
    
> [!NOTE]
> <span data-ttu-id="b4bfb-169">Si une redirection HTTP se produit, il existe plusieurs `NavigationStarting` événements dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-169">If an HTTP redirect occurs, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="b4bfb-170">À titre d’exemple d’utilisation des événements, inscrivez un responsable pour l’événement afin d’annuler les demandes `NavigationStarting` non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-170">As an example of using the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="b4bfb-171">Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="b4bfb-171">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="b4bfb-172">À présent, l’application ne navigue pas vers les sites non https.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-172">Now the app does not navigate to any non-https sites.</span></span>  <span data-ttu-id="b4bfb-173">Vous pouvez utiliser un mécanisme similaire pour accomplir d’autres tâches, telles que la limitation de la navigation à l’intérieur de votre propre domaine.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-173">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <a name="step-5---scripting"></a><span data-ttu-id="b4bfb-174">Étape 5 : écriture de scripts</span><span class="sxs-lookup"><span data-stu-id="b4bfb-174">Step 5 - Scripting</span></span>  

<span data-ttu-id="b4bfb-175">Vous pouvez utiliser des applications hôtes pour injecter du code JavaScript dans des contrôles WebView2 lors de l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-175">You may use host apps to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="b4bfb-176">Vous pouvez tâcher WebView pour exécuter du javaScript arbitraire ou ajouter des scripts d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-176">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="b4bfb-177">Le javaScript injecté s’applique à tous les nouveaux documents de niveau supérieur et aux images enfants jusqu’à ce que le JavaScript soit supprimé.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-177">The injected JavaScript applies to all new top-level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="b4bfb-178">Le javaScript injecté est exécuté avec un minutage spécifique.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-178">The injected JavaScript is run with specific timing.</span></span>  

*   <span data-ttu-id="b4bfb-179">Exécutez-le après la création de l’objet global.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-179">Run it after the creation of the global object.</span></span>  
*   <span data-ttu-id="b4bfb-180">Exécutez-le avant d’exécuter tout autre script inclus dans le document HTML.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-180">Run it before any other script included in the HTML document is run.</span></span>  
    
<span data-ttu-id="b4bfb-181">Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="b4bfb-181">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="b4bfb-182">À présent, WebView doit toujours figer `Object` l’objet et renvoie le document de page une seule fois.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-182">Now, WebView should always freeze the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="b4bfb-183">Les API d’injection de script \(et d’autres API WebView2\) sont asynchrones, vous devez utiliser des rappels si le code doit être exécuté dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-183">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <a name="step-6---communication-between-host-and-web-content"></a><span data-ttu-id="b4bfb-184">Étape 6 : communication entre le contenu hôte et le contenu web</span><span class="sxs-lookup"><span data-stu-id="b4bfb-184">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="b4bfb-185">L’hôte et le contenu web peuvent également communiquer entre eux par le biais de la `postMessage` méthode.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-185">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="b4bfb-186">Le contenu web en cours d’exécution dans un WebView peut publier sur l’hôte par le biais de la méthode, et le message est géré par tout le handler d’événement inscrit `window.chrome.webview.postMessage` `ICoreWebView2WebMessageReceivedEventHandler` sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-186">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="b4bfb-187">De même, l’hôte peut envoyer un message au contenu web par le biais d’une méthode ou d’une méthode, qui est capturée par les handlers ajoutés à partir de `ICoreWebView2::PostWebMessageAsString` `ICoreWebView2::PostWebMessageAsJSON` `window.chrome.webview.addEventListener` l’écoute.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-187">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="b4bfb-188">Le mécanisme de communication permet au contenu web d’utiliser des fonctionnalités natives en passant des messages pour demander à l’hôte d’exécuter des API natives.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-188">The communication mechanism allows the web content to use native capabilities by passing messages to ask the host to run native APIs.</span></span>  

<span data-ttu-id="b4bfb-189">Par exemple, pour comprendre le mécanisme, les étapes suivantes se produisent lorsque vous essayez d’afficher l’URL du document dans WebView.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-189">As an example to understand the mechanism, the following steps occur when you try to output the document URL in WebView.</span></span>  

1.  <span data-ttu-id="b4bfb-190">L’hôte inscrit un handler pour renvoyer le message reçu au contenu web</span><span class="sxs-lookup"><span data-stu-id="b4bfb-190">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="b4bfb-191">L’hôte injecte un script au contenu web qui inscrit un handler pour imprimer un message à partir de l’hôte</span><span class="sxs-lookup"><span data-stu-id="b4bfb-191">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="b4bfb-192">L’hôte injecte un script au contenu web qui publie l’URL sur l’hôte</span><span class="sxs-lookup"><span data-stu-id="b4bfb-192">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="b4bfb-193">Le handler de l’hôte est déclenché et renvoie le message \(l’URL\) au contenu web</span><span class="sxs-lookup"><span data-stu-id="b4bfb-193">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="b4bfb-194">Le handler du contenu web est déclenché et imprime le message à partir de l’hôte \(l’URL\)</span><span class="sxs-lookup"><span data-stu-id="b4bfb-194">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  
    
<span data-ttu-id="b4bfb-195">Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="b4bfb-195">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

### <a name="build-your-display-url-sample-app"></a><span data-ttu-id="b4bfb-196">Créer votre exemple d’application d’URL d’affichage</span><span class="sxs-lookup"><span data-stu-id="b4bfb-196">Build your display URL sample app</span></span>  

<span data-ttu-id="b4bfb-197">Pour créer et exécuter l’application, sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="b4bfb-197">To build and run the app, select `F5`.</span></span>  <span data-ttu-id="b4bfb-198">L’URL apparaît dans une fenêtre pop-up avant d’accéder à une page web.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-198">The URL appears in a pop-up window before navigating to a webpage.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Url d’affichage" lightbox="../media/show-url.png":::
   <span data-ttu-id="b4bfb-200">Url d’affichage</span><span class="sxs-lookup"><span data-stu-id="b4bfb-200">Display url</span></span>  
:::image-end:::    

<span data-ttu-id="b4bfb-201">Félicitations, vous avez créé votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-201">Congratulations, you built your first WebView2 app.</span></span>  

## <a name="next-steps"></a><span data-ttu-id="b4bfb-202">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="b4bfb-202">Next steps</span></span>  

<span data-ttu-id="b4bfb-203">Pour obtenir des fonctionnalités WebView2 supplémentaires qui ne sont pas couvertes dans cet article, examinez les ressources suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4bfb-203">For additional WebView2 functionality that isn't covered in this article, review the following resources.</span></span>  

*   <span data-ttu-id="b4bfb-204">Pour en savoir plus sur la création d’applications WebView2, accédez aux meilleures pratiques de développement [WebView2.][WV2BestPractices]</span><span class="sxs-lookup"><span data-stu-id="b4bfb-204">To learn more about building WebView2 applications, navigate to [WebView2 development best practices][WV2BestPractices].</span></span>  
*   <span data-ttu-id="b4bfb-205">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez à [l’exemple d’API WebView2.][GithubMicrosoftedgeWebview2samplesApisample]</span><span class="sxs-lookup"><span data-stu-id="b4bfb-205">For a comprehensive example of WebView2 capabilities, navigate to [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="b4bfb-206">Pour un exemple d’application créé à l’aide de WebView2, accédez [à WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="b4bfb-206">For a sample app built using WebView2, navigate to [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="b4bfb-207">Pour plus d’informations sur l’API WebView2, accédez à la référence [d’API.][Webview2ReferenceWin32]</span><span class="sxs-lookup"><span data-stu-id="b4bfb-207">For detailed information about the WebView2 API, navigate to [API reference][Webview2ReferenceWin32].</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="b4bfb-208">Entrer en contact avec l’Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="b4bfb-208">Getting in touch with the Microsoft Edge WebView team</span></span>  

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
