---
description: Héberger le contenu Web de votre application Win32 avec le contrôle WebView 2 de Microsoft Edge
title: Applications WebView 2 de Microsoft Edge 2 pour les applications Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Controller, contrôle de navigateur, html Edge
ms.openlocfilehash: 460364b0c93e80c0e3868c3b69e20ea9dcf6c129
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697195"
---
# <span data-ttu-id="33002-104">Mise en route de WebView2 (developer preview)</span><span class="sxs-lookup"><span data-stu-id="33002-104">Getting started with WebView2 (developer preview)</span></span>

<span data-ttu-id="33002-105">Cette procédure pas à pas décrit les fonctionnalités couramment utilisées de [WebView2 (developer preview)](https://aka.ms/webview) et vous permet de commencer à créer votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="33002-105">This walkthrough goes over the commonly used functionalities of [WebView2 (developer preview)](https://aka.ms/webview) and gets you started on creating your first WebView2 app.</span></span> <span data-ttu-id="33002-106">Pour en savoir plus sur les API individuelles, voir informations de référence sur les [API](../reference/win32/0-9-538-reference-webview2.md) .</span><span class="sxs-lookup"><span data-stu-id="33002-106">Visit [API reference](../reference/win32/0-9-538-reference-webview2.md) to learn more about individual APIs.</span></span>  

## <span data-ttu-id="33002-107">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="33002-107">Prerequisites</span></span>

* <span data-ttu-id="33002-108">[Microsoft Edge (chrome)](https://www.microsoftedgeinsider.com/download/) installé sur un système d’exploitation pris en charge (actuellement Windows 10, Windows 8,1 et Windows 7).</span><span class="sxs-lookup"><span data-stu-id="33002-108">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on supported OS (currently Windows 10, Windows 8.1, and Windows 7).</span></span> <span data-ttu-id="33002-109">**Nous vous recommandons d’utiliser le canal des Canaries et la version minimale requise est 82.0.488.0**.</span><span class="sxs-lookup"><span data-stu-id="33002-109">**We recommend using the Canary channel and the minimum required version is 82.0.488.0**.</span></span>
* <span data-ttu-id="33002-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 ou version ultérieure avec prise en charge C++ installée.</span><span class="sxs-lookup"><span data-stu-id="33002-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later with C++ support installed.</span></span>

## <span data-ttu-id="33002-111">Étape 1: créer une application Win32 de fenêtre unique</span><span class="sxs-lookup"><span data-stu-id="33002-111">Step 1 - Create a single window win32 app</span></span>

<span data-ttu-id="33002-112">Nous allons commencer par un projet de bureau de base contenant une seule fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="33002-112">We will start with a basic desktop project containing a single main window.</span></span> <span data-ttu-id="33002-113">Comme il ne s’agit pas du principal objectif de cette procédure pas à pas, nous allons utiliser un exemple de code modifié de la [procédure pas à pas: création d’une application de bureau Windows classique (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="33002-113">As this is not the main focus of this walkthrough, we will simply use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span> <span data-ttu-id="33002-114">[Téléchargez](https://aka.ms/HelloWebView) l’exemple modifié pour commencer.</span><span class="sxs-lookup"><span data-stu-id="33002-114">[Download](https://aka.ms/HelloWebView) the modified sample to get started.</span></span>

<span data-ttu-id="33002-115">Ouvrez **WebView2GettingStarted. sln** dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="33002-115">Open **WebView2GettingStarted.sln** in Visual Studio.</span></span> <span data-ttu-id="33002-116">Si vous utilisez une ancienne version de Visual Studio, cliquez avec le bouton droit sur le projet **WebView2GettingStarted** , puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="33002-116">If you are using an older version of Visual Studio, right click on the **WebView2GettingStarted** project and click **Properties**.</span></span> <span data-ttu-id="33002-117">Sous **Propriétés de configuration**  >  **générales**, modifiez la version et l' **ensemble d’outils de plateforme** du **SDK Windows** pour utiliser le kit de développement logiciel (SDK) Win10 et l’ensemble d’outils vs disponibles.</span><span class="sxs-lookup"><span data-stu-id="33002-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and VS toolset available to you.</span></span>

![outils-version](../media/tool-version.png)

<span data-ttu-id="33002-119">Visual Studio peut afficher des erreurs en raison d’un fichier d’en-tête WebView2 manquant, qui doit être placé une fois l’étape 2 terminée.</span><span class="sxs-lookup"><span data-stu-id="33002-119">Visual Studio may show some errors due to missing WebView2 header file, which should go away once Step 2 is completed.</span></span>

## <span data-ttu-id="33002-120">Étape 2: installer le SDK WebView2</span><span class="sxs-lookup"><span data-stu-id="33002-120">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="33002-121">À présent, nous allons ajouter le kit de développement logiciel (SDK) WebView2 au projet.</span><span class="sxs-lookup"><span data-stu-id="33002-121">Now let's add the WebView2 SDK into the project.</span></span> <span data-ttu-id="33002-122">Pour la version préliminaire du développeur, vous pouvez installer le kit de développement logiciel (SDK) Win32 via NuGet.</span><span class="sxs-lookup"><span data-stu-id="33002-122">For the developer preview, you can install the Win32 SDK via Nuget.</span></span>

1. <span data-ttu-id="33002-123">Cliquez avec le bouton droit sur le projet, puis cliquez sur **gérer les packages NuGet**.</span><span class="sxs-lookup"><span data-stu-id="33002-123">Right click the project and click **Manage Nuget Packages**.</span></span>

    ![Manage-NuGet-packages](../media/manage-nuget-packages.png)

2. <span data-ttu-id="33002-125">Entrez **Microsoft. Windows. ImplementationLibrary** dans la barre de recherche, cliquez sur **Microsoft. Windows. ImplementationLibrary** à partir des résultats, puis cliquez sur **installer** dans la fenêtre de droite, puis installez le SDK le plus récent.</span><span class="sxs-lookup"><span data-stu-id="33002-125">Enter **Microsoft.Windows.ImplementationLibrary** in the search bar, click **Microsoft.Windows.ImplementationLibrary** from the results, and click **Install** inthe right hand side window and install the latest SDK.</span></span> <span data-ttu-id="33002-126">NuGet télécharge le SDK sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="33002-126">Nuget will download the SDK to your machine.</span></span> <span data-ttu-id="33002-127">Bien que nous ayons recours à la [bibliothèque d’implémentation Windows](https://github.com/Microsoft/wil) et à la [bibliothèque de modèles C++ Windows Runtime](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) pour faciliter l’utilisation de com dans le cadre de cette procédure pas à pas, ces dernières sont entièrement facultatives.</span><span class="sxs-lookup"><span data-stu-id="33002-127">While we use [Windows Implementation Library](https://github.com/Microsoft/wil) and [Windows Runtime C++ Template Library](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) to make working with COM easier in this walkthrough, they are completely optional.</span></span>

    ![entendra](../media/wil.png)

3. <span data-ttu-id="33002-129">Entrez **Microsoft. Web. WebView2** dans la barre de recherche, cliquez sur **Microsoft. Web. WebView2** à partir des résultats, puis cliquez sur **installer** dans la fenêtre de droite, puis installez le SDK le plus récent.</span><span class="sxs-lookup"><span data-stu-id="33002-129">Enter **Microsoft.Web.WebView2** in the search bar, click **Microsoft.Web.WebView2** from the results, and click **Install** in the right hand side window and install the latest SDK.</span></span> <span data-ttu-id="33002-130">NuGet télécharge le SDK sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="33002-130">Nuget will download the SDK to your machine.</span></span>

    ![NuGet](../media/nuget.png)

4. <span data-ttu-id="33002-132">Incluez l’en-tête WebView2.</span><span class="sxs-lookup"><span data-stu-id="33002-132">Include the WebView2 header.</span></span> <span data-ttu-id="33002-133">Dans **HelloWebView. cpp**, ajoutez `#include "WebView2.h"` sous les lignes de `#include` s.</span><span class="sxs-lookup"><span data-stu-id="33002-133">In **HelloWebView.cpp**, add `#include "WebView2.h"` below the lines of `#include`s.</span></span>

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

<span data-ttu-id="33002-134">Vous êtes prêt à utiliser l’API WebView2 et à la générer.</span><span class="sxs-lookup"><span data-stu-id="33002-134">You are all set to use and build against the WebView2 API.</span></span> <span data-ttu-id="33002-135">Appuyez sur la touche F5 pour générer et exécuter l’exemple d’application.</span><span class="sxs-lookup"><span data-stu-id="33002-135">Press F5 to build and run the sample app.</span></span> <span data-ttu-id="33002-136">Une application doit afficher une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="33002-136">You should see an app displaying an empty window.</span></span>

![application vide](../media/empty-app.png)

## <span data-ttu-id="33002-138">Étape 3: créer un WebView unique dans la fenêtre parent</span><span class="sxs-lookup"><span data-stu-id="33002-138">Step 3 - Create a single WebView within the parent window</span></span>

<span data-ttu-id="33002-139">Ajoutons maintenant un WebView à la fenêtre principale.</span><span class="sxs-lookup"><span data-stu-id="33002-139">Now let's add a WebView to the main window.</span></span> <span data-ttu-id="33002-140">Nous allons utiliser `CreateCoreWebView2Environment` pour configurer l’environnement et rechercher le navigateur Microsoft Edge (chrome) qui alimente le contrôle.</span><span class="sxs-lookup"><span data-stu-id="33002-140">We'll use `CreateCoreWebView2Environment` to set up the environment and locate the Microsoft Edge (Chromium) browser powering the control.</span></span> <span data-ttu-id="33002-141">Vous pouvez également utiliser `CreateCoreWebView2EnvironmentWithOptions` si vous voulez spécifier l’emplacement du navigateur, le dossier utilisateur, les indicateurs du navigateur, etc., au lieu d’utiliser le paramètre par défaut.</span><span class="sxs-lookup"><span data-stu-id="33002-141">You can also use `CreateCoreWebView2EnvironmentWithOptions` if you want to specify browser location, user folder, browser flags, etc., instead of using the default setting.</span></span> <span data-ttu-id="33002-142">Lorsque `CreateCoreWebView2Environment` vous aurez terminé, vous serez en mesure d’appeler `ICoreWebView2Environment::CreateCoreWebView2Controller` le `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` rappel et d’appeler `ICoreWebView2Controller::get_CoreWebView2` pour obtenir le WebView associé.</span><span class="sxs-lookup"><span data-stu-id="33002-142">Upon the completion of `CreateCoreWebView2Environment`, you'll be able to call `ICoreWebView2Environment::CreateCoreWebView2Controller` inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and call `ICoreWebView2Controller::get_CoreWebView2` to get the associated WebView.</span></span>

<span data-ttu-id="33002-143">Dans le rappel, définissons également quelques paramètres, redimensionnez le WebView de sorte qu’il prenne 100% de la fenêtre parente, et naviguez jusqu’à Bing.</span><span class="sxs-lookup"><span data-stu-id="33002-143">In the callback, let's also set a few settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>

<span data-ttu-id="33002-144">Copiez le code suivant dans **HelloWebView. cpp** entre `// <-- WebView2 sample code starts here -->` et `// <-- WebView2 sample code ends here -->` .</span><span class="sxs-lookup"><span data-stu-id="33002-144">Copy the following code to **HelloWebView.cpp** between `// <-- WebView2 sample code starts here -->` and `// <-- WebView2 sample code ends here -->`.</span></span>

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
                // this is a redundant demo step as they are the default settings values
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

<span data-ttu-id="33002-145">Appuyez sur la touche F5 pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="33002-145">Press F5 to build and run the app.</span></span> <span data-ttu-id="33002-146">Maintenant, vous disposez d’une fenêtre WebView qui affiche Bing.</span><span class="sxs-lookup"><span data-stu-id="33002-146">Now you have a WebView window displaying Bing.</span></span>

![Bing-fenêtre](../media/bing-window.png)

## <span data-ttu-id="33002-148">Étape 4: événements de navigation</span><span class="sxs-lookup"><span data-stu-id="33002-148">Step 4 - Navigation events</span></span>

<span data-ttu-id="33002-149">Nous avons déjà parlé à l’adresse URL en utilisant `ICoreWebView2::Navigate` la dernière étape.</span><span class="sxs-lookup"><span data-stu-id="33002-149">We already covered navigating to URL using `ICoreWebView2::Navigate` in the last step.</span></span> <span data-ttu-id="33002-150">Pendant la navigation, WebView déclenche une séquence d’événements que l’hôte peut écouter,,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` et `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="33002-150">During navigation, WebView fires a sequence of events that the host can listen to - `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span> <span data-ttu-id="33002-151">Pour en savoir plus, cliquez [ici](../reference/win32/0-9-538/ICoreWebView2.md#navigation-events) .</span><span class="sxs-lookup"><span data-stu-id="33002-151">Click [here](../reference/win32/0-9-538/ICoreWebView2.md#navigation-events) to learn more.</span></span>

![navigation-événements](../media/navigation-events.png)

<span data-ttu-id="33002-153">Dans les cas d’erreur, il est possible, ou non `SourceChanged` , `ContentLoading` ou des `HistoryChanged` événements en fonction de la poursuite de la navigation sur une page d’erreur.</span><span class="sxs-lookup"><span data-stu-id="33002-153">In error cases there may or may not be `SourceChanged`, `ContentLoading`, or `HistoryChanged` event(s) depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="33002-154">Dans le cas d’une redirection HTTP, plusieurs événements sont présents `NavigationStarting` dans une ligne.</span><span class="sxs-lookup"><span data-stu-id="33002-154">In case of an HTTP redirect, there will be multiple `NavigationStarting` events in a row.</span></span>

<span data-ttu-id="33002-155">Pour savoir comment utiliser ces événements, nous allons enregistrer un gestionnaire pour `NavigationStarting` annuler toute demande non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="33002-155">As an example of utilizing those events, let's register a handler for `NavigationStarting` to cancel any non-https requests.</span></span> <span data-ttu-id="33002-156">Copiez le code suivant dans **HelloWebView. cpp** ci-dessous `// Step 4 - Navigation events` .</span><span class="sxs-lookup"><span data-stu-id="33002-156">Copy the following code to **HelloWebView.cpp** below `// Step 4 - Navigation events`.</span></span>

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

<span data-ttu-id="33002-157">À présent, l’application n’accède à aucun site non HTTPS.</span><span class="sxs-lookup"><span data-stu-id="33002-157">Now the app will not navigate to any non-https sites.</span></span> <span data-ttu-id="33002-158">Vous pouvez utiliser le même mécanisme pour effectuer d’autres tâches, comme limiter la navigation à l’intérieur de votre propre domaine.</span><span class="sxs-lookup"><span data-stu-id="33002-158">You can use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>

## <span data-ttu-id="33002-159">Étape 5: création de scripts</span><span class="sxs-lookup"><span data-stu-id="33002-159">Step 5 - Scripting</span></span>

<span data-ttu-id="33002-160">L’application d’hébergement peut également injecter JavaScript dans WebView.</span><span class="sxs-lookup"><span data-stu-id="33002-160">The hosting app can also inject JavaScript into WebView.</span></span> <span data-ttu-id="33002-161">Vous pouvez Task WebView pour exécuter du code JavaScript arbitraire ou ajouter des scripts d’initialisation.</span><span class="sxs-lookup"><span data-stu-id="33002-161">You can task WebView to execute arbitrary JavaScript or add initialization scripts.</span></span> <span data-ttu-id="33002-162">Les scripts d’initialisation ajoutés s’appliquent à tous les futurs documents de niveau supérieur et navigation de cadre enfant jusqu’à leur suppression, puis exécutés après la création de l’objet global et avant l’exécution de tout autre script fourni par le document HTML.</span><span class="sxs-lookup"><span data-stu-id="33002-162">Added initialization scripts apply to all future top level document and child frame navigation until removed, and run after the global object has been created and before any other script included by the HTML document is executed.</span></span>

<span data-ttu-id="33002-163">Copiez le code suivant `// Step 5 - Scripting` .</span><span class="sxs-lookup"><span data-stu-id="33002-163">Copy the following code below `// Step 5 - Scripting`.</span></span>

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

<span data-ttu-id="33002-164">Maintenant, WebView figera toujours l’objet objet et renverra le document page une seule fois.</span><span class="sxs-lookup"><span data-stu-id="33002-164">Now WebView will always freeze the Object object and return the page document once.</span></span>

**<span data-ttu-id="33002-165">Notez que ces API d’injection de script (et d’autres API WebView2) sont asynchrones, vous devez utiliser des rappels si le code doit être exécuté dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="33002-165">Note that these script injection APIs (and some other WebView2 APIs) are asynchronous, you should use callbacks if code is to be executed in a particular order.</span></span>**

## <span data-ttu-id="33002-166">Étape 6: communication entre l’hôte et le contenu Web</span><span class="sxs-lookup"><span data-stu-id="33002-166">Step 6 - Communication between host and web content</span></span>

<span data-ttu-id="33002-167">L’hôte et le contenu Web peuvent également communiquer entre eux `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="33002-167">The host and the web content can also communicate with each other through `postMessage`.</span></span> <span data-ttu-id="33002-168">Le contenu Web exécuté au sein d’un WebView peut être publié sur l’hôte `window.chrome.webview.postMessage` et le message est géré par tout inscrit `ICoreWebView2WebMessageReceivedEventHandler` sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="33002-168">The web content running within a WebView can post to the host through `window.chrome.webview.postMessage`, and the message would be handled by any registered `ICoreWebView2WebMessageReceivedEventHandler` on the host.</span></span> <span data-ttu-id="33002-169">De même, l’hôte peut afficher le contenu Web via `ICoreWebView2::PostWebMessageAsString` ou `ICoreWebView2::PostWebMessageAsJSON` , qui serait intercepté par des gestionnaires ajoutés `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="33002-169">Likewise, the host can message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON`, which would be caught by handlers added from `window.chrome.webview.addEventListener`.</span></span> <span data-ttu-id="33002-170">Le mécanisme de communication permet au contenu Web d’utiliser les fonctionnalités natives en passant des messages pour demander à l’hôte d’appeler des API natives.</span><span class="sxs-lookup"><span data-stu-id="33002-170">The communication mechanism allows the web content to utilize native capabilities by passing messages to ask the host to call native APIs.</span></span>

<span data-ttu-id="33002-171">Par exemple, pour comprendre le mécanisme, nous allons essayer d’imprimer l’URL du document dans WebView avec une petite présentation.</span><span class="sxs-lookup"><span data-stu-id="33002-171">As an example to understand the mechanism, let's try printing out the document URL in WebView with a little detour,</span></span>

1. <span data-ttu-id="33002-172">l’hôte inscrit un gestionnaire pour renvoyer le message reçu au contenu Web.</span><span class="sxs-lookup"><span data-stu-id="33002-172">the host registers a handler to return received message back to the web content</span></span>
2. <span data-ttu-id="33002-173">l’hôte injecte un script dans le contenu Web qui inscrit un gestionnaire pour imprimer le message à partir de l’hôte.</span><span class="sxs-lookup"><span data-stu-id="33002-173">the host injects a script to the web content that registers a handler to print message from the host</span></span>
3. <span data-ttu-id="33002-174">l’hôte injecte un script dans le contenu Web qui publie l’URL sur l’hôte.</span><span class="sxs-lookup"><span data-stu-id="33002-174">the host injects a script to the web content that posts the URL to the host</span></span>
4. <span data-ttu-id="33002-175">le gestionnaire de l’hôte est déclenché et renvoie le message (URL) du contenu Web.</span><span class="sxs-lookup"><span data-stu-id="33002-175">the host's handler is triggered and returns the message (the URL) to the web content</span></span>
5. <span data-ttu-id="33002-176">le gestionnaire du contenu Web est déclenché et imprime le message de l’hôte (URL)</span><span class="sxs-lookup"><span data-stu-id="33002-176">the web content's handler is triggered and prints the host's message (the URL)</span></span>

<span data-ttu-id="33002-177">Copiez le code suivant `// Step 6 - Communication between host and web content` ,</span><span class="sxs-lookup"><span data-stu-id="33002-177">Copy the following code below `// Step 6 - Communication between host and web content`,</span></span>

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

<span data-ttu-id="33002-178">Appuyez sur la touche F5 pour générer et exécuter l’application.</span><span class="sxs-lookup"><span data-stu-id="33002-178">Press F5 to build and run the app.</span></span> <span data-ttu-id="33002-179">Le message URL s’affiche alors avant de naviguer vers les pages.</span><span class="sxs-lookup"><span data-stu-id="33002-179">It will now show URLs before navigating to pages.</span></span>

![Show-URL](../media/show-url.png)

<span data-ttu-id="33002-181">Félicitations, vous venez de créer votre première application WebView2.</span><span class="sxs-lookup"><span data-stu-id="33002-181">Congratulations, you've just built your first WebView2 app!</span></span>

## <span data-ttu-id="33002-182">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="33002-182">Next Steps</span></span>

<span data-ttu-id="33002-183">Il existe de nombreuses fonctionnalités WebView2 non traitées dans cette procédure pas à pas.</span><span class="sxs-lookup"><span data-stu-id="33002-183">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>

<span data-ttu-id="33002-184">Pour en savoir plus:</span><span class="sxs-lookup"><span data-stu-id="33002-184">To learn more:</span></span>

* <span data-ttu-id="33002-185">Consultez l' [exemple d’API WebView2](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) pour obtenir un exemple complet de fonctionnalités WebView2's.</span><span class="sxs-lookup"><span data-stu-id="33002-185">Checkout [WebView2 API Sample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) for a comprehensive example of WebView2's capabilities.</span></span>
* <span data-ttu-id="33002-186">Extraire [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) une application créée à l’aide de WebView2.</span><span class="sxs-lookup"><span data-stu-id="33002-186">Checkout [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) an application built using WebView2.</span></span>
* <span data-ttu-id="33002-187">Pour plus d’informations sur notre API, consultez les informations de référence sur les [API](../reference/win32/0-9-538-reference-webview2.md) .</span><span class="sxs-lookup"><span data-stu-id="33002-187">Please explore [API reference](../reference/win32/0-9-538-reference-webview2.md) for detailed information about our API.</span></span>  

## <span data-ttu-id="33002-188">Contacter l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="33002-188">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="33002-189">Aidez-nous à créer une expérience WebView2 plus riche en partageant vos commentaires!</span><span class="sxs-lookup"><span data-stu-id="33002-189">Help us build a richer WebView2 experience by sharing your feedback!</span></span> <span data-ttu-id="33002-190">Consultez notre page de [Commentaires référentiel Samples](https://aka.ms/webviewfeedback) pour envoyer des demandes de fonctionnalité ou des rapports de bogues, ou pour rechercher des problèmes connus.</span><span class="sxs-lookup"><span data-stu-id="33002-190">Visit our [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>
