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
# <span data-ttu-id="d66f1-104">Mise en route de WebView2 (developer preview)</span><span class="sxs-lookup"><span data-stu-id="d66f1-104">Getting started with WebView2 (developer preview)</span></span>  

<span data-ttu-id="d66f1-105">Le contenu suivant vous présente les fonctionnalités fréquemment utilisées de [WebView2 (developer preview)][Webview2Index] et fournit un point de départ pour la création de votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="d66f1-105">The following content walks you through the commonly used functionalities of [WebView2 (developer preview)][Webview2Index] and provides a starting  point for creating your first WebView2 app.</span></span>  <span data-ttu-id="d66f1-106">Pour plus d’informations sur les API WebView2 individuelles, voir informations de référence sur les [API][Webview2ReferenceWin3209538].</span><span class="sxs-lookup"><span data-stu-id="d66f1-106">For more information about individual WebView2 APIs, see [API reference][Webview2ReferenceWin3209538].</span></span>  

## <span data-ttu-id="d66f1-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="d66f1-107">Prerequisites</span></span>  

*   <span data-ttu-id="d66f1-108">[Microsoft Edge (chrome)][MicrosoftedgeinsiderDownload] installé sur le système d’exploitation pris en charge \ (actuellement Windows 10, Windows 8,1 et Windows 7 \).</span><span class="sxs-lookup"><span data-stu-id="d66f1-108">[Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] installed on supported OS \(currently Windows 10, Windows 8.1, and Windows 7\).</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="d66f1-109">L’équipe WebView recommande d’utiliser le canal Canaries et la version minimale requise est 82.0.488.0.</span><span class="sxs-lookup"><span data-stu-id="d66f1-109">The WebView team recommends using the Canary channel and the minimum required version is 82.0.488.0.</span></span>  
    
*   <span data-ttu-id="d66f1-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 ou version ultérieure avec prise en charge C++ installée.</span><span class="sxs-lookup"><span data-stu-id="d66f1-110">[Visual Studio][MicrosoftVisualstudioMain] 2015 or later with C++ support installed.</span></span>  

## <span data-ttu-id="d66f1-111">Étape 1: créer une application Win32 de fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="d66f1-111">Step 1 - Create a single window win32 app</span></span>  

<span data-ttu-id="d66f1-112">Utiliser un projet de bureau de base contenant une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="d66f1-112">Start with a basic desktop project containing a single main window.</span></span>  <span data-ttu-id="d66f1-113">Pour mieux mettre au point la procédure pas à pas, vous utilisez un exemple de code modifié de la [procédure pas à pas: création d’une application de bureau Windows classique (C++)][CppWindowsWalkthroughCreatingDesktopApplication] pour votre exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="d66f1-113">To better focus the walkthrough, you are using modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)][CppWindowsWalkthroughCreatingDesktopApplication] for your sample app.</span></span>  <span data-ttu-id="d66f1-114">Pour télécharger l’exemple modifié et commencer, voir [exemples de WebView2][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="d66f1-114">To download the modified sample and get started, see [WebView2 Samples][GithubMicrosoftedgeWebview2samplesGettingStartedGuide].</span></span>  

<span data-ttu-id="d66f1-115">Dans Visual Studio, ouvrez `WebView2GettingStarted.sln` .</span><span class="sxs-lookup"><span data-stu-id="d66f1-115">In Visual Studio, open `WebView2GettingStarted.sln`.</span></span>  <span data-ttu-id="d66f1-116">Si vous utilisez une ancienne version de Visual Studio, pointez sur le projet **WebView2GettingStarted** , ouvrez le menu contextuel, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-116">If you are using an older version of Visual Studio, hover on the **WebView2GettingStarted** project, open the contextual menu \(right-click\), and select **Properties**.</span></span>  <span data-ttu-id="d66f1-117">Sous **Propriétés de configuration**  >  **générales**, modifiez la version et l' **ensemble d’outils de plateforme** du **SDK Windows** pour utiliser le kit de développement logiciel (SDK) Win10 et l’ensemble d’outils Visual Studio (vs Tools) disponible.</span><span class="sxs-lookup"><span data-stu-id="d66f1-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and Visual Studio toolset \(VS toolset\) available to you.</span></span>  

:::image type="complex" source="../media/tool-version.png" alt-text="Version de l’outil":::
   <span data-ttu-id="d66f1-119">Version de l’outil</span><span class="sxs-lookup"><span data-stu-id="d66f1-119">Tool version</span></span>  
:::image-end:::  

<span data-ttu-id="d66f1-120">Visual Studio peut afficher des erreurs en raison d’un fichier d’en-tête WebView2 manquant, qui doit disparaître après l’exécution de l’étape 2.</span><span class="sxs-lookup"><span data-stu-id="d66f1-120">Visual Studio may show some errors due to missing WebView2 header file, which should go away after Step 2 is completed.</span></span>  

## <span data-ttu-id="d66f1-121">Étape 2: installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="d66f1-121">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="d66f1-122">Ajoutez le kit de développement logiciel (SDK) WebView2 au projet.</span><span class="sxs-lookup"><span data-stu-id="d66f1-122">Add the WebView2 SDK into the project.</span></span>  <span data-ttu-id="d66f1-123">Pour la version préliminaire du développeur, vous pouvez installer le kit de développement logiciel (SDK) Win32 en utilisant NuGet.</span><span class="sxs-lookup"><span data-stu-id="d66f1-123">For the developer preview, you may install the Win32 SDK using Nuget.</span></span>  

1.  <span data-ttu-id="d66f1-124">Pointez sur le projet, ouvrez le menu contextuel, puis sélectionnez **gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="d66f1-124">Hover on the project, open the contextual menu \(right-click\), and select **Manage Nuget Packages**.</span></span>  
    
    :::image type="complex" source="../media/manage-nuget-packages.png" alt-text="Gérer les packages NuGet":::
       <span data-ttu-id="d66f1-126">Gérer les packages NuGet</span><span class="sxs-lookup"><span data-stu-id="d66f1-126">Manage Nuget packages</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d66f1-127">Installez la bibliothèque d’implémentation Windows.</span><span class="sxs-lookup"><span data-stu-id="d66f1-127">Install the Windows Implementation Library.</span></span>  
    1.  <span data-ttu-id="d66f1-128">Entrez `Microsoft.Windows.ImplementationLibrary` dans la barre de recherche, sélectionnez **Microsoft. Windows. ImplementationLibrary** dans les résultats, puis sélectionnez **installer** dans la fenêtre de droite.</span><span class="sxs-lookup"><span data-stu-id="d66f1-128">Enter `Microsoft.Windows.ImplementationLibrary` in the search bar, select **Microsoft.Windows.ImplementationLibrary** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="d66f1-129">NuGet télécharge le SDK sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d66f1-129">Nuget downloads the SDK to your machine.</span></span>  
        
        > [!NOTE] 
        > <span data-ttu-id="d66f1-130">La [bibliothèque d’implémentation Windows][GithubMicrosoftWilMain] et la [bibliothèque de modèles C++ Windows Runtime][CppCxWrlTemplateLibraryVS2019] sont facultatifs et ont été ajoutés pour faciliter l’utilisation de com.</span><span class="sxs-lookup"><span data-stu-id="d66f1-130">The [Windows Implementation Library][GithubMicrosoftWilMain] and [Windows Runtime C++ Template Library][CppCxWrlTemplateLibraryVS2019] are optional and were added to make working with COM easier for the example.</span></span>  
        
        :::image type="complex" source="../media/wil.png" alt-text="Bibliothèque d’implémentation Windows":::
           <span data-ttu-id="d66f1-132">Bibliothèque d’implémentation Windows</span><span class="sxs-lookup"><span data-stu-id="d66f1-132">Windows Implementation Library</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="d66f1-133">Installez le kit de développement logiciel (SDK) WebView2.</span><span class="sxs-lookup"><span data-stu-id="d66f1-133">Install the WebView2 SDK.</span></span>  
    1.  <span data-ttu-id="d66f1-134">Entrez `Microsoft.Web.WebView2` dans la barre de recherche, sélectionnez **Microsoft. Web. WebView2** dans les résultats, puis sélectionnez **installer** dans la fenêtre de droite.</span><span class="sxs-lookup"><span data-stu-id="d66f1-134">Enter `Microsoft.Web.WebView2` in the search bar, select **Microsoft.Web.WebView2** from the results, and select **Install** in the right-hand side window.</span></span>  <span data-ttu-id="d66f1-135">NuGet télécharge le SDK sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d66f1-135">Nuget downloads the SDK to your machine.</span></span>  
        
        :::image type="complex" source="../media/nuget.png" alt-text="NuGet":::
           <span data-ttu-id="d66f1-137">NuGet</span><span class="sxs-lookup"><span data-stu-id="d66f1-137">Nuget</span></span>
        :::image-end:::  
        
1.  <span data-ttu-id="d66f1-138">Ajoutez WebView2 en-tête à votre projet.</span><span class="sxs-lookup"><span data-stu-id="d66f1-138">Add WebView2 header to your project.</span></span>  
    :::row:::
       :::column span="1":::
          <span data-ttu-id="d66f1-139">Ouvrez `HelloWebView.cpp` , copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` après la dernière `#include` ligne.</span><span class="sxs-lookup"><span data-stu-id="d66f1-139">Open `HelloWebView.cpp`, copy the following code snippet and paste into `HelloWebView.cpp` after last `#include` line.</span></span>  
          
          ```cpp
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
       :::column span="1":::
          <span data-ttu-id="d66f1-140">La section include doit ressembler à l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="d66f1-140">The include section should look similar to the following code snippet.</span></span>  
          
          ```cpp
          ...
          #include <wrl.h>
          #include <wil/com.h>
          // include WebView2 header
          #include "WebView2.h"
          ```  
       :::column-end:::
    :::row-end:::
    
<span data-ttu-id="d66f1-141">Vous êtes prêt à utiliser l’API WebView2 et à la générer.</span><span class="sxs-lookup"><span data-stu-id="d66f1-141">You are all set to use and build against the WebView2 API.</span></span>  

### <span data-ttu-id="d66f1-142">Créer votre exemple d’application vide</span><span class="sxs-lookup"><span data-stu-id="d66f1-142">Build your empty sample app</span></span>  

<span data-ttu-id="d66f1-143">Appuyez `F5` pour générer et exécuter l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="d66f1-143">Press `F5` to build and run the sample app.</span></span>  <span data-ttu-id="d66f1-144">Une application doit afficher une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="d66f1-144">You should see an app displaying an empty window.</span></span>  

:::image type="complex" source="../media/empty-app.png" alt-text="Application vide":::
   <span data-ttu-id="d66f1-146">Application vide</span><span class="sxs-lookup"><span data-stu-id="d66f1-146">Empty app</span></span>  
:::image-end:::  

## <span data-ttu-id="d66f1-147">Étape 3: créer un WebView unique dans la fenêtre parent</span><span class="sxs-lookup"><span data-stu-id="d66f1-147">Step 3 - Create a single WebView within the parent window</span></span>  

<span data-ttu-id="d66f1-148">Ajoutez un WebView à la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="d66f1-148">Add a WebView to the main window.</span></span>  <span data-ttu-id="d66f1-149">Utilisez la `CreateCoreWebView2Environment` méthode de configuration de l’environnement et recherchez le navigateur Microsoft Edge \ (chrome \) qui alimente le contrôle.</span><span class="sxs-lookup"><span data-stu-id="d66f1-149">Use the `CreateCoreWebView2Environment` method to set up the environment and locate the Microsoft Edge \(Chromium\) browser powering the control.</span></span>  <span data-ttu-id="d66f1-150">Vous pouvez également utiliser la `CreateCoreWebView2EnvironmentWithOptions` méthode si vous souhaitez spécifier l’emplacement du navigateur, le dossier utilisateur, les indicateurs du navigateur, etc., au lieu d’utiliser le paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="d66f1-150">You may also use the `CreateCoreWebView2EnvironmentWithOptions` method if you want to specify browser location, user folder, browser flags, and so on, instead of using the default setting.</span></span>  <span data-ttu-id="d66f1-151">À l’issue de la `CreateCoreWebView2Environment` méthode, vous pouvez exécuter la `ICoreWebView2Environment::CreateCoreWebView2Controller` méthode dans le `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` rappel et exécuter la `ICoreWebView2Controller::get_CoreWebView2` méthode pour obtenir le WebView associé.</span><span class="sxs-lookup"><span data-stu-id="d66f1-151">Upon the completion of the `CreateCoreWebView2Environment` method, you are able to run the `ICoreWebView2Environment::CreateCoreWebView2Controller` method inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and run the `ICoreWebView2Controller::get_CoreWebView2` method to get the associated WebView.</span></span>  

<span data-ttu-id="d66f1-152">Dans le rappel, définissez quelques paramètres supplémentaires, redimensionnez le WebView de sorte qu’il prenne 100% de la fenêtre parente, puis naviguez vers Bing.</span><span class="sxs-lookup"><span data-stu-id="d66f1-152">In the callback, set a few additional settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>  

<span data-ttu-id="d66f1-153">Copiez l’extrait de code suivant et collez-le dans `HelloWebView.cpp` l’après `// <-- WebView2 sample code starts here -->` et avant la `// <-- WebView2 sample code ends here -->` note.</span><span class="sxs-lookup"><span data-stu-id="d66f1-153">Copy the following code snippet and paste into `HelloWebView.cpp` after the `// <-- WebView2 sample code starts here -->` note and before the `// <-- WebView2 sample code ends here -->` note.</span></span>  

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


### <span data-ttu-id="d66f1-154">Créer votre application Bing Sample</span><span class="sxs-lookup"><span data-stu-id="d66f1-154">Build your Bing sample app</span></span>  

<span data-ttu-id="d66f1-155">Appuyez `F5` pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="d66f1-155">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="d66f1-156">Vous disposez maintenant d’une fenêtre WebView affichant la page Bing.</span><span class="sxs-lookup"><span data-stu-id="d66f1-156">Now you have a WebView window displaying the Bing page.</span></span>  

:::image type="complex" source="../media/bing-window.png" alt-text="Fenêtre Bing":::
   <span data-ttu-id="d66f1-158">Fenêtre Bing</span><span class="sxs-lookup"><span data-stu-id="d66f1-158">Bing window</span></span>  
:::image-end:::  

## <span data-ttu-id="d66f1-159">Étape 4: événements de navigation</span><span class="sxs-lookup"><span data-stu-id="d66f1-159">Step 4 - Navigation events</span></span>  

<span data-ttu-id="d66f1-160">L’équipe WebView a déjà abordé la navigation vers l’URL à l’aide `ICoreWebView2::Navigate` de la méthode de la dernière étape.</span><span class="sxs-lookup"><span data-stu-id="d66f1-160">The WebView team already covered navigating to URL using the `ICoreWebView2::Navigate` method in the last step.</span></span>  <span data-ttu-id="d66f1-161">Dans le cadre de la navigation, WebView déclenche une séquence d’événements que l’hôte est susceptible d’écouter.</span><span class="sxs-lookup"><span data-stu-id="d66f1-161">During navigation, WebView fires a sequence of events to which the host may listen.</span></span>  

1.  `NavigationStarting`  
1.  `SourceChanged`  
1.  `ContentLoading`  
1.  `HistoryChanged`   
1.  `NavigationCompleted`   

<span data-ttu-id="d66f1-162">Pour plus d’informations, voir [événements de navigation][Webview2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="d66f1-162">For more information, see [Navigation events][Webview2ConceptsNavigationEvents].</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="Événements de navigation":::
   <span data-ttu-id="d66f1-164">Événements de navigation</span><span class="sxs-lookup"><span data-stu-id="d66f1-164">Navigation events</span></span>  
:::image-end:::  

<span data-ttu-id="d66f1-165">Dans les cas d’erreur, un ou plusieurs des événements suivants risquent de se produire selon que la navigation se poursuit sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="d66f1-165">In error cases, one or more of the following events may occur depending on whether the navigation is continued to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`

<span data-ttu-id="d66f1-166">Dans le cas d’une redirection HTTP, il existe plusieurs `NavigationStarting` événements dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="d66f1-166">In case of an HTTP redirect, there are multiple `NavigationStarting` events in a row.</span></span>  

<span data-ttu-id="d66f1-167">En guise d’exemple d’utilisation des événements, inscrivez un gestionnaire pour l' `NavigationStarting` événement afin d’annuler toute demande non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-167">As an example of utilizing the events, register a handler for the `NavigationStarting` event to cancel any non-https requests.</span></span>  <span data-ttu-id="d66f1-168">Copiez l’extrait de code suivant, puis collez-le dans `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="d66f1-168">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="d66f1-169">À présent, l’application ne navigue pas vers des sites non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="d66f1-169">Now the app is not navigating to any non-https sites.</span></span>  <span data-ttu-id="d66f1-170">Vous pouvez utiliser le même mécanisme pour effectuer d’autres tâches, comme limiter la navigation à l’intérieur de votre propre domaine.</span><span class="sxs-lookup"><span data-stu-id="d66f1-170">You may use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>  

## <span data-ttu-id="d66f1-171">Étape 5: création de scripts</span><span class="sxs-lookup"><span data-stu-id="d66f1-171">Step 5 - Scripting</span></span>  

<span data-ttu-id="d66f1-172">L’application d’hébergement risque également d’injecter du JavaScript dans WebView.</span><span class="sxs-lookup"><span data-stu-id="d66f1-172">The hosting app may also inject JavaScript into WebView.</span></span>  <span data-ttu-id="d66f1-173">Vous pouvez effectuer une tâche WebView pour exécuter du code JavaScript arbitraire ou ajouter des scripts d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="d66f1-173">You may task WebView to run arbitrary JavaScript or add initialization scripts.</span></span>  <span data-ttu-id="d66f1-174">Les scripts d’initialisation ajoutés s’appliquent à tous les futurs documents de niveau supérieur et navigation de cadre enfant jusqu’à leur suppression, puis exécutés après la création de l’objet global et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="d66f1-174">Added initialization scripts apply to all future top level document and child frame navigation until removed, and run after the global object has been created and before any other script included by the HTML document is run.</span></span>  

<span data-ttu-id="d66f1-175">Copiez l’extrait de code suivant, puis collez-le dans `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="d66f1-175">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>  

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

<span data-ttu-id="d66f1-176">Le contrôle WebView devrait alors toujours figer l' `Object` objet et renvoyer le document de page une seule fois.</span><span class="sxs-lookup"><span data-stu-id="d66f1-176">Now WebView should always freezes the `Object` object and returns the page document once.</span></span>  

> [!NOTE] 
> <span data-ttu-id="d66f1-177">Les API d’injection de script \ (et certaines autres API WebView2 \) sont asynchrones, vous devez utiliser des rappels si le code doit être exécuté dans un ordre spécifique.</span><span class="sxs-lookup"><span data-stu-id="d66f1-177">The script injection APIs \(and some other WebView2 APIs\) are asynchronous, you should use callbacks if code is must be run in a specific order.</span></span>  

## <span data-ttu-id="d66f1-178">Étape 6: communication entre l’hôte et le contenu Web</span><span class="sxs-lookup"><span data-stu-id="d66f1-178">Step 6 - Communication between host and web content</span></span>  

<span data-ttu-id="d66f1-179">L’hôte et le contenu Web risquent également de communiquer entre eux par le biais de la `postMessage` méthode.</span><span class="sxs-lookup"><span data-stu-id="d66f1-179">The host and the web content may also communicate with each other through the `postMessage` method.</span></span>  <span data-ttu-id="d66f1-180">Le contenu Web exécuté au sein d’un WebView peut être publié sur l’hôte par le biais de la `window.chrome.webview.postMessage` méthode, et le message est géré par tout `ICoreWebView2WebMessageReceivedEventHandler` Gestionnaire d’événements enregistré sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d66f1-180">The web content running within a WebView may post to the host through the `window.chrome.webview.postMessage` method, and the message is handled by any registered the `ICoreWebView2WebMessageReceivedEventHandler` event handler on the host.</span></span>  <span data-ttu-id="d66f1-181">De même, l’hôte peut traiter le contenu Web via `ICoreWebView2::PostWebMessageAsString` ou la `ICoreWebView2::PostWebMessageAsJSON` méthode, qui est interceptée par des gestionnaires ajoutés de l' `window.chrome.webview.addEventListener` écouteur.</span><span class="sxs-lookup"><span data-stu-id="d66f1-181">Likewise, the host may message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON` method, which is caught by handlers added from `window.chrome.webview.addEventListener` listener.</span></span>  <span data-ttu-id="d66f1-182">Le mécanisme de communication permet au contenu Web d’utiliser les fonctionnalités natives en passant des messages pour demander à l’hôte d’appeler des API natives.</span><span class="sxs-lookup"><span data-stu-id="d66f1-182">The communication mechanism allows the web content to utilize native capabilities by passing messages to ask the host to call native APIs.</span></span>  

<span data-ttu-id="d66f1-183">Pour comprendre le mécanisme, les étapes suivantes se produisent lorsque vous tentez d’imprimer l’URL du document dans WebView.</span><span class="sxs-lookup"><span data-stu-id="d66f1-183">As an example to understand the mechanism, the following steps occur when you try printing out the document URL in WebView.</span></span>  

1.  <span data-ttu-id="d66f1-184">L’hôte inscrit un gestionnaire pour renvoyer le message reçu au contenu Web.</span><span class="sxs-lookup"><span data-stu-id="d66f1-184">The host registers a handler to return received message back to the web content</span></span>  
1.  <span data-ttu-id="d66f1-185">L’hôte injecte un script dans le contenu Web qui inscrit un gestionnaire pour imprimer le message à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d66f1-185">The host injects a script to the web content that registers a handler to print message from the host</span></span>  
1.  <span data-ttu-id="d66f1-186">L’hôte injecte un script dans le contenu Web qui publie l’URL sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="d66f1-186">The host injects a script to the web content that posts the URL to the host</span></span>  
1.  <span data-ttu-id="d66f1-187">Le gestionnaire de l’hôte est déclenché et renvoie le message \ (URL \) du contenu Web.</span><span class="sxs-lookup"><span data-stu-id="d66f1-187">The handler of the host is triggered and returns the message \(the URL\) to the web content</span></span>  
1.  <span data-ttu-id="d66f1-188">Le gestionnaire du contenu Web est déclenché et imprime le message de l’hôte \ (URL \)</span><span class="sxs-lookup"><span data-stu-id="d66f1-188">The handler of the web content is triggered and prints message from the host \(the URL\)</span></span>  

<span data-ttu-id="d66f1-189">Copiez l’extrait de code suivant, puis collez-le dans `HelloWebView.cpp` .</span><span class="sxs-lookup"><span data-stu-id="d66f1-189">Copy the following code snippet and paste into `HelloWebView.cpp`.</span></span>    

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

### <span data-ttu-id="d66f1-190">Créer votre exemple d’application d’URL d’affichage</span><span class="sxs-lookup"><span data-stu-id="d66f1-190">Build your show URL sample app</span></span>  

<span data-ttu-id="d66f1-191">Appuyez `F5` pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="d66f1-191">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="d66f1-192">L’URL s’affiche dans une fenêtre contextuelle avant d’accéder à une page.</span><span class="sxs-lookup"><span data-stu-id="d66f1-192">You should see the URL in a pop-up window prior to navigating to a page.</span></span>  

:::image type="complex" source="../media/show-url.png" alt-text="Afficher l’URL":::
   <span data-ttu-id="d66f1-194">Afficher l’URL</span><span class="sxs-lookup"><span data-stu-id="d66f1-194">Show url</span></span>  
:::image-end:::  

<span data-ttu-id="d66f1-195">Félicitations, vous venez de créer votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="d66f1-195">Congratulations, you just built your first WebView2 app!</span></span>  

## <span data-ttu-id="d66f1-196">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="d66f1-196">Next steps</span></span>  

<span data-ttu-id="d66f1-197">La plupart des fonctionnalités WebView2 qui ne sont pas abordées sur cette page, la section suivante a fourni des ressources supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="d66f1-197">Many of the WebView2 functionalities that are not covered on this page, the following section provided additional resources.</span></span>  

### <span data-ttu-id="d66f1-198">Voir également</span><span class="sxs-lookup"><span data-stu-id="d66f1-198">See also</span></span>  

*   <span data-ttu-id="d66f1-199">Pour obtenir un exemple complet de fonctionnalités WebView2, consultez l' [exemple d’API WebView2][GithubMicrosoftedgeWebview2samplesApisample].</span><span class="sxs-lookup"><span data-stu-id="d66f1-199">For a comprehensive example of WebView2 capabilities, see [WebView2 API Sample][GithubMicrosoftedgeWebview2samplesApisample].</span></span>  
*   <span data-ttu-id="d66f1-200">Pour obtenir un exemple d’application généré à l’aide de WebView2, voir [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span><span class="sxs-lookup"><span data-stu-id="d66f1-200">For a sample application built using WebView2, see [WebView2Browser][GithubMicrosoftedgeWebview2browser].</span></span>  
*   <span data-ttu-id="d66f1-201">Pour plus d’informations sur l’API WebView2, voir informations de référence sur les [API][Webview2ReferenceWin3209538].</span><span class="sxs-lookup"><span data-stu-id="d66f1-201">For detailed information about the WebView2 API, see [API reference][Webview2ReferenceWin3209538].</span></span>  

## <span data-ttu-id="d66f1-202">Contacter l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="d66f1-202">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="d66f1-203">Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires!</span><span class="sxs-lookup"><span data-stu-id="d66f1-203">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="d66f1-204">Visitez le site de [Commentaires référentiel Samples][GithubMicrosoftedgeWebviewfeedback] sur GitHub pour envoyer des demandes de fonctionnalité ou des rapports de bogues, ou pour rechercher des problèmes connus.</span><span class="sxs-lookup"><span data-stu-id="d66f1-204">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedback] on GitHub to submit feature requests or bug reports or search for known issues.</span></span>  

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
