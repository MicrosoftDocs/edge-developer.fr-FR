---
description: Découvrez comment lier statiquement la bibliothèque de chargeurs WebView2.
title: Comment lier statiquement la bibliothèque de chargeurs WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 8f48a4fde9e2960de6156fc14db8c84f87a49868
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535887"
---
# <a name="statically-link-the-webview2-loader-library"></a><span data-ttu-id="96ffc-104">Lier statiquement la bibliothèque de chargeurs WebView2</span><span class="sxs-lookup"><span data-stu-id="96ffc-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="96ffc-105">Vous pouvez distribuer votre application avec un seul fichier exécutable, au lieu d’un package de nombreux fichiers.</span><span class="sxs-lookup"><span data-stu-id="96ffc-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="96ffc-106">Pour créer un fichier exécutable unique ou pour réduire la taille de votre package, vous devez lier statiquement les fichiers WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="96ffc-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="96ffc-107">Le SDK WebView2 contient un fichier d’en-tête `WebView2Loader.dll` et le `IDL` fichier.</span><span class="sxs-lookup"><span data-stu-id="96ffc-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="96ffc-108">est un petit composant qui permet aux applications de localiser le Runtime WebView2, ou les canaux non stables de Microsoft Edge, sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="96ffc-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="96ffc-109">Pour les applications qui ne souhaitent pas expédier `WebView2Loader.dll` un , complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="96ffc-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="96ffc-110">Ouvrez le `.vcxproj` fichier de projet de votre application dans un éditeur de texte, tel que Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="96ffc-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="96ffc-111">Le fichier de projet peut être masqué, ce qui signifie qu’il `.vcproj` ne s’affiche pas Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="96ffc-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="96ffc-112">Utilisez la ligne de commande pour rechercher les fichiers masqués.</span><span class="sxs-lookup"><span data-stu-id="96ffc-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="96ffc-113">Recherchez la section dans le code où vous incluez les fichiers cibles NuGet package WebView2.</span><span class="sxs-lookup"><span data-stu-id="96ffc-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="96ffc-114">L’emplacement dans le code est mis en évidence dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="96ffc-114">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/insert-here.png" alt-text="Project Extrait de code de fichiers" lightbox="./media/insert-here.png":::
       <span data-ttu-id="96ffc-116">Project Extrait de code de fichiers</span><span class="sxs-lookup"><span data-stu-id="96ffc-116">Project Files code snippet</span></span>   
    :::image-end:::  
    
1.  <span data-ttu-id="96ffc-117">Copiez l’extrait de code suivant et collez-le là où `Microsoft.Web.WebView2.targets` il est inclus.</span><span class="sxs-lookup"><span data-stu-id="96ffc-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  
    
    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```  
    
    :::image type="complex" source="./media/static-lib.png" alt-text="Extrait de code inséré" lightbox="./media/static-lib.png":::
       <span data-ttu-id="96ffc-119">Extrait de code inséré</span><span class="sxs-lookup"><span data-stu-id="96ffc-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="96ffc-120">Modifiez les dépendances supplémentaires de la configuration de build pour votre application.</span><span class="sxs-lookup"><span data-stu-id="96ffc-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="96ffc-121">Pour commencer, recherchez toutes les `<AdditionalDependencies>` balises.</span><span class="sxs-lookup"><span data-stu-id="96ffc-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="96ffc-122">Pour chacun d’eux, `version.lib` ajoutez en tant que dépendance supplémentaire à chaque configuration de build dans le `.vcxproj` fichier.</span><span class="sxs-lookup"><span data-stu-id="96ffc-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/version-lib.png" alt-text="Ajout de version.lib à ItemDefinitionGroups" lightbox="./media/version-lib.png":::
       <span data-ttu-id="96ffc-124">Ajout `version.lib` à</span><span class="sxs-lookup"><span data-stu-id="96ffc-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="96ffc-125">L’équipe WebView2 a pour objectif d’automatiser l’ajout de dépendances supplémentaires dans les prochaines publication.</span><span class="sxs-lookup"><span data-stu-id="96ffc-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1.  <span data-ttu-id="96ffc-126">Compilez et exécutez votre application.</span><span class="sxs-lookup"><span data-stu-id="96ffc-126">Compile and run your app.</span></span>  
    
## <a name="getting-in-touch-with-the-webview2-team"></a><span data-ttu-id="96ffc-127">Entrer en contact avec l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="96ffc-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

## <a name="see-also"></a><span data-ttu-id="96ffc-128">Articles associés</span><span class="sxs-lookup"><span data-stu-id="96ffc-128">See also</span></span>  

*   <span data-ttu-id="96ffc-129">To get started using WebView2, navigate to [WebView2 Prise en main Guides][Webview2MainGetStarted].</span><span class="sxs-lookup"><span data-stu-id="96ffc-129">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span></span>  
*   <span data-ttu-id="96ffc-130">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez [à WebView2Samples][GithubMicrosoftedgeWebview2samples] GitHub.</span><span class="sxs-lookup"><span data-stu-id="96ffc-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="96ffc-131">Pour plus d’informations sur les API WebView2, accédez à la référence [d’API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="96ffc-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="96ffc-132">Pour plus d’informations sur WebView2, accédez [à Ressources WebView2.][Webview2MainNextSteps]</span><span class="sxs-lookup"><span data-stu-id="96ffc-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Microsoft Edge outils de développement (Chromium) | Documents Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Microsoft Edge Référence de l’API WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2MainGetStarted]: ../index.md#get-started "Get started - Introduction to Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires WebView - MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Nouveautés - Déboguer JavaScript pour Visual Studio Code - microsoft/vscode-js-debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge applications WebView (Chromium) - Visual Studio Code - Déboguer pour Microsoft Edge - microsoft/vscode-edge-debug2 | GitHub"  
