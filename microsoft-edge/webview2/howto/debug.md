---
description: Découvrez comment déboguer des contrôles WebView2.
title: Débogage de WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: ad6f334e5796d2f22146f2853ae1ef1d854e329c
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894318"
---
# <span data-ttu-id="adb22-104">Comment déboguer avec WebView2</span><span class="sxs-lookup"><span data-stu-id="adb22-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="adb22-105">L’objectif du contrôle Microsoft Edge WebView2 combine les fonctionnalités de développement d’applications et les outils de développement d’applications Web et natives.</span><span class="sxs-lookup"><span data-stu-id="adb22-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="adb22-106">La page suivante décrit les différents outils à utiliser pour le développement de contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="adb22-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="adb22-107">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="adb22-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="adb22-108">Utilisez les [outils de développement Microsoft Edge (chrome)][DevtoolsGuideChromiumMain] pour déboguer du contenu Web affiché dans les contrôles WebView2, de la même façon que Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="adb22-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you use Microsoft Edge.</span></span>  <span data-ttu-id="adb22-109">Pour ouvrir le DevTools, positionnez le focus sur la fenêtre WebView, puis utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="adb22-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  
*   <span data-ttu-id="adb22-110">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="adb22-110">Select `F12`.</span></span>  
*   <span data-ttu-id="adb22-111">Sélectionnez `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="adb22-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="adb22-112">Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) > sélectionnez `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="adb22-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Outils Microsoft Edge Dev" lightbox="../media/f12.png":::
   <span data-ttu-id="adb22-114">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="adb22-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="adb22-115">Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, le fait d’appuyer sur `F12` risque de déclencher le débogueur natif au lieu des outils de développement.</span><span class="sxs-lookup"><span data-stu-id="adb22-115">When you debug your application in Visual Studio with the native debugger attached, pressing `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="adb22-116">Appuyez sur `Ctrl` + `Shift` + `I` , ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter cette situation.</span><span class="sxs-lookup"><span data-stu-id="adb22-116">Press `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

> [!NOTE]
> <span data-ttu-id="adb22-117">Vous pouvez utiliser l' `--auto-open-devtools-for-tabs` argument de la ligne de commande pour ouvrir une nouvelle fenêtre devtools lorsque vous créez un WebView pour la première fois.</span><span class="sxs-lookup"><span data-stu-id="adb22-117">You may use the `--auto-open-devtools-for-tabs` command-line argument to open a new DevTools window when you first create a WebView.</span></span>  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## <span data-ttu-id="adb22-118">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="adb22-118">Visual Studio</span></span>  

<span data-ttu-id="adb22-119">Utilisez le débogueur de script dans Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure pour déboguer votre script dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="adb22-119">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="adb22-120">Vérifiez que le composant de **Diagnostics JavaScript** du **développement de bureau avec charge de** travail en C++ est installé.</span><span class="sxs-lookup"><span data-stu-id="adb22-120">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Diagnostics JavaScript Visual Studio":::
   <span data-ttu-id="adb22-122">Diagnostics JavaScript Visual Studio</span><span class="sxs-lookup"><span data-stu-id="adb22-122">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="adb22-123">Pour activer le débogage de script WebView2, ouvrez le menu contextuel (cliquez avec le bouton droit sur \) dans votre projet > sélectionnez **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="adb22-123">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  

*   <span data-ttu-id="adb22-124">Dans **Propriétés de configuration**, sélectionnez **débogage**.</span><span class="sxs-lookup"><span data-stu-id="adb22-124">On **Configuration Properties**, select **Debugging**.</span></span>  
*   <span data-ttu-id="adb22-125">Dans la propriété **type de débogueur** , sélectionnez **JavaScript (WebView2)** dans la liste des options.</span><span class="sxs-lookup"><span data-stu-id="adb22-125">On the **Debugger Type** property, select **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Débogueur JavaScript Visual Studio":::
   <span data-ttu-id="adb22-127">Débogueur JavaScript Visual Studio</span><span class="sxs-lookup"><span data-stu-id="adb22-127">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="adb22-128">Vous êtes prêt à procéder au débogage.</span><span class="sxs-lookup"><span data-stu-id="adb22-128">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="adb22-129">Pour déboguer, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="adb22-129">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="adb22-130">Définir des points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="adb22-130">Set Breakpoints</span></span>  
    *   <span data-ttu-id="adb22-131">Ouvrez le fichier de script et définissez le point d’arrêt à l’emplacement souhaité.</span><span class="sxs-lookup"><span data-stu-id="adb22-131">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="adb22-132">L’adaptateur de débogage JS/TS n’effectue pas le mappage de chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="adb22-132">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="adb22-133">Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.</span><span class="sxs-lookup"><span data-stu-id="adb22-133">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="adb22-134">Exécuter du code</span><span class="sxs-lookup"><span data-stu-id="adb22-134">Run Code</span></span>  
    *   <span data-ttu-id="adb22-135">Sélectionnez votre arôme de build et votre environnement d’exécution appropriés, puis démarrez le débogueur Windows local.</span><span class="sxs-lookup"><span data-stu-id="adb22-135">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="adb22-136">Afficher la console de débogage</span><span class="sxs-lookup"><span data-stu-id="adb22-136">View Debug Console</span></span>  
    *   <span data-ttu-id="adb22-137">Votre application s’exécute et le débogueur se connecte après la création du premier webview2.</span><span class="sxs-lookup"><span data-stu-id="adb22-137">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="adb22-138">Toute sortie de débogage en attente est affichée.</span><span class="sxs-lookup"><span data-stu-id="adb22-138">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="adb22-139">Cette méthode de débogage est actuellement limitée aux applications Win32 et aux compléments Office.</span><span class="sxs-lookup"><span data-stu-id="adb22-139">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="adb22-140">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="adb22-140">Visual Studio Code</span></span>  

<span data-ttu-id="adb22-141">Vous pouvez utiliser du code Visual Studio pour déboguer des scripts qui s’exécutent dans des contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="adb22-141">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="adb22-142">Pour plus d’informations, reportez-vous à la rubrique [applications WebView de Microsoft Edge (chrome)][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="adb22-142">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="adb22-143">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="adb22-143">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="adb22-144">Aidez-vous à créer une expérience WebView2 plus riche en partageant vos commentaires.</span><span class="sxs-lookup"><span data-stu-id="adb22-144">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="adb22-145">Visitez le site de [Commentaires référentiel Samples][GithubMicrosoftedgeWebviewfeedbackMain] pour envoyer des demandes de fonctionnalité ou des rapports de bogues.</span><span class="sxs-lookup"><span data-stu-id="adb22-145">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedbackMain] to submit feature requests or bug reports.</span></span>  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome) et débogueur de code et de code-débogueur pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
