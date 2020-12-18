---
description: Découvrez comment lier de manière statique la bibliothèque de chargeur WebView2.
title: Liaison statique de la bibliothèque de chargeur WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 397c226eb958d1e656fb0ecb6dd8f1e2fe300746
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230928"
---
# <span data-ttu-id="e5a62-104">Liaison statique de la bibliothèque de chargeur WebView2</span><span class="sxs-lookup"><span data-stu-id="e5a62-104">Statically link the WebView2 loader library</span></span>  

<span data-ttu-id="e5a62-105">Vous pouvez distribuer votre application à l’aide d’un seul fichier exécutable au lieu d’un package de nombreux fichiers.</span><span class="sxs-lookup"><span data-stu-id="e5a62-105">You may want to distribute your application with a single executable file, instead of a package of many files.</span></span> <span data-ttu-id="e5a62-106">Pour créer un fichier exécutable unique ou pour réduire la taille de votre package, vous devez lier de manière statique les fichiers WebView2Loader.</span><span class="sxs-lookup"><span data-stu-id="e5a62-106">To create a single executable file, or to reduce the size of your package, you should statically link the WebView2Loader files.</span></span> <span data-ttu-id="e5a62-107">Le kit de développement logiciel (SDK) WebView2 contient un fichier d’en-tête, `WebView2Loader.dll` et le `IDL` fichier.</span><span class="sxs-lookup"><span data-stu-id="e5a62-107">The WebView2 SDK contains a header file, `WebView2Loader.dll`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="e5a62-108">est un petit composant qui aide les applications à localiser le runtime WebView2 ou les canaux non stables de Microsoft Edge sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e5a62-108">is a small component that helps apps locate the WebView2 Runtime, or non-stable channels of Microsoft Edge, on the device.</span></span>  

<span data-ttu-id="e5a62-109">Pour les applications qui ne souhaitent pas expédier `WebView2Loader.dll` , procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="e5a62-109">For apps that don't want to ship a `WebView2Loader.dll`, complete the following steps.</span></span>  

1.  <span data-ttu-id="e5a62-110">Ouvrez le `.vcxproj` fichier de projet de votre application dans un éditeur de texte, tel que le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e5a62-110">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="e5a62-111">`.vcproj`Il peut s’agir d’un fichier caché, ce qui signifie qu’il n’est pas affiché dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e5a62-111">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="e5a62-112">Utilisez la ligne de commande pour rechercher des fichiers cachés.</span><span class="sxs-lookup"><span data-stu-id="e5a62-112">Use the command-line to find hidden files.</span></span>  
    
1.  <span data-ttu-id="e5a62-113">Recherchez la section dans le code où vous incluez les fichiers cibles de package NuGet WebView2.</span><span class="sxs-lookup"><span data-stu-id="e5a62-113">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="e5a62-114">L’emplacement dans le code est surligné dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="e5a62-114">The location in the code is highlighted in the following figure.</span></span>  

    :::image type="complex" source="./media/inserthere.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/inserthere.png":::
       <span data-ttu-id="e5a62-116">Fragment de code de fichiers de projet</span><span class="sxs-lookup"><span data-stu-id="e5a62-116">Project Files code snippet</span></span>   
    :::image-end:::  
  
1.  <span data-ttu-id="e5a62-117">Copiez l’extrait de code suivant et collez-le là où il `Microsoft.Web.WebView2.targets` est inclus.</span><span class="sxs-lookup"><span data-stu-id="e5a62-117">Copy the following code snippet and paste it where the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    ```xaml
    <PropertyGroup> 
        <WebView2LoaderPreference>Static</WebView2LoaderPreference> 
    </PropertyGroup>
    ```
      
    :::image type="complex" source="./media/staticlib.png" alt-text="Extrait de code inséré" lightbox="./media/staticlib.png":::
       <span data-ttu-id="e5a62-119">Extrait de code inséré</span><span class="sxs-lookup"><span data-stu-id="e5a62-119">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e5a62-120">Modifiez les dépendances supplémentaires de la configuration de build de votre application.</span><span class="sxs-lookup"><span data-stu-id="e5a62-120">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="e5a62-121">Pour commencer, recherchez toutes les `<AdditionalDependencies>` balises.</span><span class="sxs-lookup"><span data-stu-id="e5a62-121">To begin, find all of the `<AdditionalDependencies>` tags.</span></span> <span data-ttu-id="e5a62-122">Pour chacun d’entre eux, ajoutez `version.lib` en tant que dépendance supplémentaire à chaque nouvelle configuration de build du `.vcxproj` fichier.</span><span class="sxs-lookup"><span data-stu-id="e5a62-122">For each, add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Ajouter version. lib à ItemDefinitionGroups" lightbox="./media/versionlib.png":::
       <span data-ttu-id="e5a62-124">Ajout `version.lib` à</span><span class="sxs-lookup"><span data-stu-id="e5a62-124">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="e5a62-125">L’équipe WebView2 vise à automatiser l’ajout de la dépendance supplémentaire dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="e5a62-125">The WebView2 team aims to automate adding the additional dependency in future releases.</span></span>  
    
1. <span data-ttu-id="e5a62-126">Compilez et exécutez l’application.</span><span class="sxs-lookup"><span data-stu-id="e5a62-126">Compile and run your app.</span></span>

### <span data-ttu-id="e5a62-127">Contacter l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="e5a62-127">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

### <span data-ttu-id="e5a62-128">Voir également</span><span class="sxs-lookup"><span data-stu-id="e5a62-128">See also</span></span>  

*   <span data-ttu-id="e5a62-129">Pour commencer à utiliser WebView2, accédez à [WebView2 guides de mise en route][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="e5a62-129">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="e5a62-130">Pour obtenir un exemple complet de fonctionnalités WebView2, accédez à [WebView2Samples][GithubMicrosoftedgeWebview2samples] dans github.</span><span class="sxs-lookup"><span data-stu-id="e5a62-130">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="e5a62-131">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="e5a62-131">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="e5a62-132">Pour plus d’informations sur WebView2, accédez à [ressources WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="e5a62-132">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
