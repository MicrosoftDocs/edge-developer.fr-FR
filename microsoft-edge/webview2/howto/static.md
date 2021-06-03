---
description: Découvrez comment lier statiquement la bibliothèque de chargeurs WebView2.
title: Comment lier statiquement la bibliothèque de chargeurs WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: e3cd336c9448277e0dde3b9da1521b5cbc7c44d2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536404"
---
# <a name="statically-link-the-webview2-loader-library"></a><span data-ttu-id="a9e8d-104">Lier statiquement la bibliothèque de chargeurs WebView2</span><span class="sxs-lookup"><span data-stu-id="a9e8d-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="a9e8d-105">Vous pouvez distribuer votre application avec un seul fichier exécutable, au lieu d’un package de nombreux fichiers.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="a9e8d-106">Pour créer un fichier exécutable unique ou pour réduire la taille de votre package, vous devez lier statiquement les fichiers WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="a9e8d-107">Le SDK WebView2 contient un fichier d’en-tête `WebView2Loader.dll` et le `IDL` fichier.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="a9e8d-108">est un petit composant qui permet aux applications de localiser le Runtime WebView2, ou les canaux non stables de Microsoft Edge, sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="a9e8d-109">Pour les applications qui ne souhaitent pas expédier `WebView2Loader.dll` un , complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="a9e8d-110">Ouvrez le `.vcxproj` fichier de projet de votre application dans un éditeur de texte, tel que Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a9e8d-111">Le fichier de projet peut être masqué, ce qui signifie qu’il `.vcproj` ne s’affiche pas Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="a9e8d-112">Utilisez la ligne de commande pour rechercher les fichiers masqués.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="a9e8d-113">Recherchez la section dans le code où vous incluez les fichiers cibles NuGet package WebView2.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="a9e8d-114">L’emplacement dans le code est mis en évidence dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-114">The location in the code is highlighted in the following figure.</span></span>  

    :::image type="complex" source="./media/inserthere.png" alt-text="Project Extrait de code de fichiers" lightbox="./media/inserthere.png":::
       <span data-ttu-id="a9e8d-116">Project Extrait de code de fichiers</span><span class="sxs-lookup"><span data-stu-id="a9e8d-116">Project Files code snippet</span></span>   
    :::image-end:::  
  
1.  <span data-ttu-id="a9e8d-117">Copiez l’extrait de code suivant et collez-le là où `Microsoft.Web.WebView2.targets` il est inclus.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Extrait de code inséré" lightbox="./media/staticlib.png":::
       <span data-ttu-id="a9e8d-119">Extrait de code inséré</span><span class="sxs-lookup"><span data-stu-id="a9e8d-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a9e8d-120">Modifiez les dépendances supplémentaires de la configuration de build pour votre application.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="a9e8d-121">Pour commencer, recherchez toutes les `<AdditionalDependencies>` balises.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="a9e8d-122">Pour chacun d’eux, `version.lib` ajoutez en tant que dépendance supplémentaire à chaque configuration de build dans le `.vcxproj` fichier.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Ajout de version.lib à ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       <span data-ttu-id="a9e8d-124">Ajout `version.lib` à</span><span class="sxs-lookup"><span data-stu-id="a9e8d-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="a9e8d-125">L’équipe WebView2 a pour objectif d’automatiser l’ajout de dépendances supplémentaires dans les prochaines publication.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1. <span data-ttu-id="a9e8d-126">Compilez et exécutez votre application.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-126">Compile and run your app.</span></span>

### <a name="getting-in-touch-with-the-webview2-team"></a><span data-ttu-id="a9e8d-127">Entrer en contact avec l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="a9e8d-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <a name="see-also"></a><span data-ttu-id="a9e8d-128">Articles associés</span><span class="sxs-lookup"><span data-stu-id="a9e8d-128">See also</span></span>  

*   <span data-ttu-id="a9e8d-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="a9e8d-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="a9e8d-130">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez [à WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="a9e8d-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="a9e8d-131">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="a9e8d-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="a9e8d-132">Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2MainNextSteps]</span><span class="sxs-lookup"><span data-stu-id="a9e8d-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Référence de l’API WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en place : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Nouveautés - Déboguer JavaScript pour Visual Studio Code - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge applications WebView (Chromium) - Visual Studio Code - Déboguer pour Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
