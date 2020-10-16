---
description: Découvrez comment lier de manière statique la bibliothèque de chargeur WebView2.
title: Liaison statique de la bibliothèque de chargeur WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/15/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: a25bd85c8a6b17bdf8712c954eb7b7cc28738eb2
ms.sourcegitcommit: 442de63da52d00c6dc27fa08ccdb736534127566
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/16/2020
ms.locfileid: "11120070"
---
# <span data-ttu-id="7b717-104">Liaison statique de la bibliothèque de chargeur WebView2</span><span class="sxs-lookup"><span data-stu-id="7b717-104">How to Statically link the WebView2 loader library</span></span>  

## <span data-ttu-id="7b717-105">Contexte</span><span class="sxs-lookup"><span data-stu-id="7b717-105">Context</span></span>  

<span data-ttu-id="7b717-106">Qu’est-ce que le WebView2Loader.dll?</span><span class="sxs-lookup"><span data-stu-id="7b717-106">What is the WebView2Loader.dll?</span></span>  

*   <span data-ttu-id="7b717-107">Le kit de développement logiciel (SDK) WebView2 contient un fichier d’en-tête, `WebView2Loader.dll.` et le `IDL` fichier.</span><span class="sxs-lookup"><span data-stu-id="7b717-107">The WebView2 SDK contains a header file, `WebView2Loader.dll.`, and the `IDL` file.</span></span> `WebView2Loader.dll` <span data-ttu-id="7b717-108">est un petit composant qui aide les applications à localiser le runtime WebView2 (ou canaux Microsoft Edge non stables) sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7b717-108">is a small component that helps apps locate the WebView2 Runtime (or non-stable Microsoft Edge channels) on the device.</span></span>  

<span data-ttu-id="7b717-109">Pour les applications qui ont un seul Runtime et qui ne souhaitent pas expédier `WebView2Loader.dll` , procédez comme **Procedure** suit.</span><span class="sxs-lookup"><span data-stu-id="7b717-109">For apps that have a single runtime, and do not want to ship a `WebView2Loader.dll`, complete the following **Procedure** steps.</span></span>  

## <span data-ttu-id="7b717-110">Procédure</span><span class="sxs-lookup"><span data-stu-id="7b717-110">Procedure</span></span>  

1.  <span data-ttu-id="7b717-111">Ouvrez le `.vcxproj` fichier de projet de votre application dans un éditeur de texte, tel que le code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7b717-111">Open the `.vcxproj` project file for your app in a text editor, such as Visual Studio Code.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7b717-112">`.vcproj`Il peut s’agir d’un fichier caché, ce qui signifie qu’il n’est pas affiché dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7b717-112">The `.vcproj` project file may be a hidden file, meaning it does not display in Visual Studio.</span></span>  <span data-ttu-id="7b717-113">Pour rechercher un fichier masqué, utilisez la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="7b717-113">Use the command-line to find a hidden file.</span></span>  
    
1.  <span data-ttu-id="7b717-114">Recherchez la section dans le code où vous incluez les fichiers cibles de package NuGet WebView2.</span><span class="sxs-lookup"><span data-stu-id="7b717-114">Locate the section in the code where you include the WebView2 NuGet package target files.</span></span>  <span data-ttu-id="7b717-115">L’emplacement dans le code est surligné dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="7b717-115">The location in the code is highlighted in the following figure.</span></span>  
    
    :::image type="complex" source="./media/inserthere.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/inserthere.png"::: 
       <span data-ttu-id="7b717-117">Fragment de code de fichiers de projet</span><span class="sxs-lookup"><span data-stu-id="7b717-117">Project Files code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b717-118">Copiez l’extrait de code suivant et collez-le partout où `Microsoft.Web.WebView2.targets` est inclus.</span><span class="sxs-lookup"><span data-stu-id="7b717-118">Copy the following code snippet and paste it everywhere the `Microsoft.Web.WebView2.targets` is included.</span></span>  

    > [!NOTE]
    > <span data-ttu-id="7b717-119">Par exemple, incluez-le après le bloc de code suivant.</span><span class="sxs-lookup"><span data-stu-id="7b717-119">For example, include it after the following code block.</span></span>  
    > 
    > ```csharp
    > <Import Project="..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets" Condition="Exists('..\packages\Microsoft.Web.WebView2.0.9.579-prerelease\build\native\Microsoft.Web.WebView2.targets')" />
    > ```  
    
    ```csharp
    <PropertyGroup> <WebView2LoaderPreference>Static</WebView2LoaderPreference> </PropertyGroup>
    ```
    
    :::image type="complex" source="./media/staticlib.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/staticlib.png"::: 
       <span data-ttu-id="7b717-121">Extrait de code inséré</span><span class="sxs-lookup"><span data-stu-id="7b717-121">Inserted code snippet</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="7b717-122">Modifiez les dépendances supplémentaires de la configuration de build de votre application.</span><span class="sxs-lookup"><span data-stu-id="7b717-122">Edit the additional dependencies of the build configuration for your app.</span></span>  <span data-ttu-id="7b717-123">Pour commencer, recherchez toutes les `<AdditionalDependencies>` balises.</span><span class="sxs-lookup"><span data-stu-id="7b717-123">To begin, find all of the `<AdditionalDependencies>` tags.</span></span>  
1.  <span data-ttu-id="7b717-124">Ajoutez `version.lib` comme dépendance supplémentaire à chaque configuration de build différente dans le `.vcxproj` fichier de votre application.</span><span class="sxs-lookup"><span data-stu-id="7b717-124">Add `version.lib` as an additional dependency to every different build configuration in the `.vcxproj` file for your app.</span></span>  
    
    :::image type="complex" source="./media/versionlib.png" alt-text="Fragment de code de fichiers de projet" lightbox="./media/versionlib.png"::: 
       <span data-ttu-id="7b717-126">Ajout `version.lib` à</span><span class="sxs-lookup"><span data-stu-id="7b717-126">Adding `version.lib` to</span></span> `ItemDefinitionGroups`  
    :::image-end:::  
    
    > [!NOTE]
    > <span data-ttu-id="7b717-127">L’équipe WebView2 vise à automatiser l’étape de dépendance supplémentaire dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="7b717-127">The WebView2 team aims to automate the additional dependency step in future releases.</span></span>  
    
<span data-ttu-id="7b717-128">Compilez et déployez votre application.</span><span class="sxs-lookup"><span data-stu-id="7b717-128">Compile and deploy your app.</span></span>  <span data-ttu-id="7b717-129">Pris.</span><span class="sxs-lookup"><span data-stu-id="7b717-129">Success.</span></span>  

## <span data-ttu-id="7b717-130">Voir également</span><span class="sxs-lookup"><span data-stu-id="7b717-130">See also</span></span>  

*   <span data-ttu-id="7b717-131">Pour commencer à utiliser WebView2, accédez à [WebView2 guides de mise en route][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="7b717-131">To get started using WebView2, navigate to [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="7b717-132">Pour obtenir un exemple complet de fonctionnalités WebView2, accédez à [WebView2Samples][GithubMicrosoftedgeWebview2samples] dans github.</span><span class="sxs-lookup"><span data-stu-id="7b717-132">For a comprehensive example of WebView2 capabilities, navigate to [WebView2Samples][GithubMicrosoftedgeWebview2samples] on GitHub.</span></span>
*   <span data-ttu-id="7b717-133">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="7b717-133">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="7b717-134">Pour plus d’informations sur WebView2, accédez à [ressources WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="7b717-134">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="7b717-135">Contacter l’équipe WebView2</span><span class="sxs-lookup"><span data-stu-id="7b717-135">Getting in touch with the WebView2 team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
