---
description: Découvrez comment déboguer des contrôles WebView2.
title: Débogage de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888580"
---
# <span data-ttu-id="b8ced-104">Comment déboguer avec WebView2</span><span class="sxs-lookup"><span data-stu-id="b8ced-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="b8ced-105">L’objectif du contrôle Microsoft Edge WebView2 combine les fonctionnalités de développement d’applications et les outils de développement d’applications Web et natives.</span><span class="sxs-lookup"><span data-stu-id="b8ced-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="b8ced-106">La page suivante décrit les différents outils à utiliser pour le développement de contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="b8ced-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="b8ced-107">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="b8ced-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="b8ced-108">Utilisez les [outils de développement Microsoft Edge (chrome)][DevtoolsMain] pour déboguer le contenu Web affiché dans les contrôles WebView2, de la même façon que si vous utilisiez Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b8ced-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsMain] to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="b8ced-109">Pour ouvrir le DevTools, positionnez le focus sur la fenêtre WebView, puis utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b8ced-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  

*   <span data-ttu-id="b8ced-110">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="b8ced-110">Select `F12`.</span></span>  
*   <span data-ttu-id="b8ced-111">Sélectionnez `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="b8ced-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="b8ced-112">Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) et sélectionnez `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="b8ced-112">Open the context menu \(right-click\) and select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Outils Microsoft Edge Dev" lightbox="../media/f12.png":::
   <span data-ttu-id="b8ced-114">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="b8ced-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!IMPORTANT]
> <span data-ttu-id="b8ced-115">Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.</span><span class="sxs-lookup"><span data-stu-id="b8ced-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="b8ced-116">Utilisez `Ctrl` + `Shift` + `I` , ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter cette situation.</span><span class="sxs-lookup"><span data-stu-id="b8ced-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

## <span data-ttu-id="b8ced-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b8ced-117">Visual Studio</span></span>  

<span data-ttu-id="b8ced-118">Vous pouvez utiliser Visual Studio pour développer le code de l’application et déboguer les scripts en même temps.</span><span class="sxs-lookup"><span data-stu-id="b8ced-118">You may use Visual Studio to develop application code and debug scripts at the same time.</span></span>  

<span data-ttu-id="b8ced-119">Gardez les points suivants à l’esprit.</span><span class="sxs-lookup"><span data-stu-id="b8ced-119">Keep the following things in mind.</span></span>  

*   <span data-ttu-id="b8ced-120">Visual Studio ne prend en charge que les scripts de débogage lors du lancement de l’application à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b8ced-120">Visual Studio only supports debugging scripts when the app is launched from within Visual Studio.</span></span>  <span data-ttu-id="b8ced-121">\ (L’attachement d’un processus actif pour le débogage n’est pas pris en charge. \)</span><span class="sxs-lookup"><span data-stu-id="b8ced-121">\(Attaching a running process for debugging is not supported.\)</span></span>  
*   <span data-ttu-id="b8ced-122">Le scénario de débogage WebView ciblé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b8ced-122">The targeted WebView debugging scenario is not supported.</span></span>  

<span data-ttu-id="b8ced-123">Utilisez le débogueur de script dans Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure pour déboguer votre script dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b8ced-123">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  

<span data-ttu-id="b8ced-124">Configurez le débogueur.</span><span class="sxs-lookup"><span data-stu-id="b8ced-124">Set up the debugger.</span></span>  

*   <span data-ttu-id="b8ced-125">Vérifiez que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.</span><span class="sxs-lookup"><span data-stu-id="b8ced-125">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  
    
    1.  <span data-ttu-id="b8ced-126">Accédez à **applications &** paramètres de fonctionnalités dans Windows.</span><span class="sxs-lookup"><span data-stu-id="b8ced-126">Navigate to **Apps & features** settings in Windows.</span></span>  <span data-ttu-id="b8ced-127">Recherchez-le à l’aide de la barre des tâches Windows.</span><span class="sxs-lookup"><span data-stu-id="b8ced-127">Search for it using the Windows task bar.</span></span>  
    1.  <span data-ttu-id="b8ced-128">Sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="b8ced-128">Choose **Modify**.</span></span>  
    1.  <span data-ttu-id="b8ced-129">Vérifiez que les cases à cocher **Diagnostics JavaScript** et **développement de bureau dans C++** sont activées.</span><span class="sxs-lookup"><span data-stu-id="b8ced-129">Verify the **Javascript diagnostics** and **Desktop Development in C++** checkboxes are selected.</span></span>  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Applications et fonctionnalités" lightbox="../media/appsandfeatures.png":::
           <span data-ttu-id="b8ced-131">Applications et fonctionnalités</span><span class="sxs-lookup"><span data-stu-id="b8ced-131">Apps & Features</span></span>  
        :::image-end:::  
        
*   <span data-ttu-id="b8ced-132">Activez le débogage de script WebView2.</span><span class="sxs-lookup"><span data-stu-id="b8ced-132">Enable WebView2 script debugging.</span></span>  
    1.  <span data-ttu-id="b8ced-133">Placez le pointeur de la souris sur votre projet, ouvrez le menu contextuel, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="b8ced-133">Hover on your project, open the context menu \(right-click\), and select **Properties**.</span></span>  
    1.  <span data-ttu-id="b8ced-134">Dans **Propriétés de configuration**, sélectionnez **débogage**.</span><span class="sxs-lookup"><span data-stu-id="b8ced-134">On **Configuration Properties**, select **Debugging**.</span></span>  
    1.  <span data-ttu-id="b8ced-135">Dans la propriété **type de débogueur** , recherchez la liste des options dans la liste, puis sélectionnez **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="b8ced-135">On the **Debugger Type** property, search the the list of options, and select **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Débogueur JavaScript Visual Studio" lightbox="../media/enbjs.png":::
           <span data-ttu-id="b8ced-137">Débogueur JavaScript Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b8ced-137">Visual Studio JavaScript Debugger</span></span>  
        :::image-end:::  
        
<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="b8ced-138">Vous êtes prêt à procéder au débogage.</span><span class="sxs-lookup"><span data-stu-id="b8ced-138">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="b8ced-139">Pour déboguer, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="b8ced-139">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="b8ced-140">Définir des points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="b8ced-140">Set Breakpoints</span></span>  
    *   <span data-ttu-id="b8ced-141">Ouvrez le fichier de script et définissez le point d’arrêt à l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="b8ced-141">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="b8ced-142">L’adaptateur de débogage JS/TS n’effectue pas le mappage de chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="b8ced-142">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="b8ced-143">Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.</span><span class="sxs-lookup"><span data-stu-id="b8ced-143">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="b8ced-144">Exécuter du code</span><span class="sxs-lookup"><span data-stu-id="b8ced-144">Run Code</span></span>  
    *   <span data-ttu-id="b8ced-145">Sélectionnez votre arôme de build et votre environnement d’exécution appropriés, puis démarrez le débogueur Windows local.</span><span class="sxs-lookup"><span data-stu-id="b8ced-145">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="b8ced-146">Afficher la console de débogage</span><span class="sxs-lookup"><span data-stu-id="b8ced-146">View Debug Console</span></span>  
    *   <span data-ttu-id="b8ced-147">Votre application s’exécute et le débogueur se connecte après la création du premier webview2.</span><span class="sxs-lookup"><span data-stu-id="b8ced-147">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="b8ced-148">Toute sortie de débogage en attente est affichée.</span><span class="sxs-lookup"><span data-stu-id="b8ced-148">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="b8ced-149">Cette méthode de débogage est actuellement limitée aux applications Win32 et aux compléments Office.</span><span class="sxs-lookup"><span data-stu-id="b8ced-149">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="b8ced-150">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="b8ced-150">Visual Studio Code</span></span>  

<span data-ttu-id="b8ced-151">Vous pouvez utiliser du code Visual Studio pour déboguer des scripts qui s’exécutent dans des contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="b8ced-151">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="b8ced-152">Pour plus d’informations, reportez-vous à la rubrique [applications WebView de Microsoft Edge (chrome)][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="b8ced-152">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="b8ced-153">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b8ced-153">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="b8ced-154">Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="b8ced-154">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="b8ced-155">Visitez le site de [Commentaires référentiel Samples][GithubMicrosoftedgeWebviewfeedback] pour envoyer des demandes de fonctionnalité ou des rapports de bogues.</span><span class="sxs-lookup"><span data-stu-id="b8ced-155">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedback] to submit feature requests or bug reports.</span></span>  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft Edge (chrome) applications WebView-débogueur de code VS pour Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
