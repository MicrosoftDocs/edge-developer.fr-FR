---
description: Découvrez comment déboguer des contrôles WebView2.
title: Commencer le débogage des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: dcdeeadc2c25bcf50834176706b8d181f06f994a
ms.sourcegitcommit: 6c7ededf8677fd7add5e4060e92f9ec4cfdb6952
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2020
ms.locfileid: "10927901"
---
# <span data-ttu-id="be45c-104">Commencer le débogage des applications WebView2</span><span class="sxs-lookup"><span data-stu-id="be45c-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="be45c-105">L’objectif du contrôle Microsoft Edge WebView2 est de combiner le meilleur des outils et des fonctionnalités de développement d’applications Web et natives.</span><span class="sxs-lookup"><span data-stu-id="be45c-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="be45c-106">Lorsque vous développez votre application WebView2, vous devez déboguer votre application.</span><span class="sxs-lookup"><span data-stu-id="be45c-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="be45c-107">Cet article présente les différents outils à utiliser pour déboguer votre code Web et votre code natif dans votre application WebView2.</span><span class="sxs-lookup"><span data-stu-id="be45c-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="be45c-108">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="be45c-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="be45c-109">Utilisez les [outils de développement Microsoft Edge (chrome)][DevtoolsGuideChromiumMain] pour déboguer le contenu Web affiché dans les contrôles WebView2, de la même façon que vous pouvez déboguer une autre page Web affichée dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="be45c-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="be45c-110">Pour ouvrir le DevTools, positionnez le focus sur le contrôle WebView, puis utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="be45c-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="be45c-111">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="be45c-111">Select `F12`.</span></span>  
*   <span data-ttu-id="be45c-112">Sélectionnez `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="be45c-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="be45c-113">Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) et sélectionnez `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="be45c-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="be45c-114">Pour plus d’informations, voir [vue d’ensemble de devtools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="be45c-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Débogage DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="be45c-116">Débogage DevTools</span><span class="sxs-lookup"><span data-stu-id="be45c-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="be45c-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="be45c-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="be45c-118">Visual Studio fournit différents outils de débogage pour le Web et le code natif dans les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="be45c-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="be45c-119">Dans la section Visual Studio, le focus est essentiellement au débogage de contrôles WebView, mais les autres méthodes de débogage dans Visual Studio sont disponibles comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="be45c-119">In the Visual Studio section, the primarily focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="be45c-120">Le processus suivant permet de déboguer du code Web et du code natif dans des applications Win32 ou des compléments Office uniquement.</span><span class="sxs-lookup"><span data-stu-id="be45c-120">Use the following process to debug web and native code in Win32 applications or Office add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="be45c-121">Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.</span><span class="sxs-lookup"><span data-stu-id="be45c-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="be45c-122">Sélectionnez `Ctrl` + `Shift` + `I` ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter la situation.</span><span class="sxs-lookup"><span data-stu-id="be45c-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="be45c-123">Avant de commencer, assurez-vous que les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="be45c-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="be45c-124">Pour déboguer les scripts, l’application doit être lancée à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="be45c-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="be45c-125">Vous ne pouvez pas attacher de débogueur à un processus WebView2 en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="be45c-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="be45c-126">Installez Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="be45c-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="be45c-127">Installez et configurez les outils de débogage de script dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="be45c-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="be45c-128">Procédez comme suit pour installer le composant **Diagnostics JavaScript** dans le **développement de bureau avec C++**.</span><span class="sxs-lookup"><span data-stu-id="be45c-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="be45c-129">Dans la barre de l’Explorateur Windows, tapez `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="be45c-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="be45c-130">Sélectionnez **programme d’installation de Visual Studio** pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="be45c-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="be45c-131">Dans le programme d’installation de Visual Studio, sur la version installée, sélectionnez le bouton **plus** , puis sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="be45c-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="be45c-132">Dans Visual Studio, sous **charges de travail**, choisissez le paramètre **développement de bureau en C++** .</span><span class="sxs-lookup"><span data-stu-id="be45c-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Écran modification de la charge de travail dans Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="be45c-134">Écran modification de la charge de travail dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="be45c-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="be45c-135">Choisissez **des composants individuels**.</span><span class="sxs-lookup"><span data-stu-id="be45c-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="be45c-136">Dans la zone de recherche, entrez `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="be45c-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="be45c-137">Sélectionnez le paramètre **Diagnostics JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="be45c-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="be45c-138">Sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="be45c-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Onglet de modification de composants individuels dans Visual Studio" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="be45c-140">Onglet de modification de composants individuels dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="be45c-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="be45c-141">Activez le débogage de script pour les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="be45c-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="be45c-142">Dans votre projet WebView2, ouvrez le menu contextuel, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="be45c-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="be45c-143">Sous les **Propriétés de configuration**, sélectionnez **débogage**.</span><span class="sxs-lookup"><span data-stu-id="be45c-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="be45c-144">Sous le **type de débogueur**, choisissez **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="be45c-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Propriété de configuration du débogage de Visual Studio" lightbox="./media/enbjs.png":::
           <span data-ttu-id="be45c-146">Propriété de configuration du **débogage** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="be45c-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="be45c-147">Effectuez les opérations suivantes pour déboguer votre application WebView2.</span><span class="sxs-lookup"><span data-stu-id="be45c-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="be45c-148">Pour définir un point d’arrêt dans votre code source, positionnez le curseur à gauche du numéro de ligne et choisissez de définir un point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="be45c-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="be45c-149">L’adaptateur de débogage JS/TS n’effectue pas le mappage de chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="be45c-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="be45c-150">Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.</span><span class="sxs-lookup"><span data-stu-id="be45c-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Ajouter un point d’arrêt dans Visual Studio" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="be45c-152">Ajouter un point d’arrêt dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="be45c-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="be45c-153">Pour exécuter le débogueur, choisissez la taille en bits de la plateforme, puis sélectionnez le bouton de lecture de couleur verte en regard du **débogueur Windows local**.</span><span class="sxs-lookup"><span data-stu-id="be45c-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="be45c-154">L’application s’exécute et le débogueur se connecte au premier processus WebView2 créé.</span><span class="sxs-lookup"><span data-stu-id="be45c-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Débogueur Windows de Visual Studio local" lightbox="./media/run.png"::: 
       <span data-ttu-id="be45c-156">**Débogueur Windows** de Visual Studio local</span><span class="sxs-lookup"><span data-stu-id="be45c-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="be45c-157">Dans la **console de débogage**, recherchez la sortie du débogueur.</span><span class="sxs-lookup"><span data-stu-id="be45c-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Console de débogage de Visual Studio" lightbox="./media/console.png"::: 
       <span data-ttu-id="be45c-159">Console de **débogage** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="be45c-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
* * *  

## <span data-ttu-id="be45c-160">Voir également</span><span class="sxs-lookup"><span data-stu-id="be45c-160">See also</span></span>  

*   <span data-ttu-id="be45c-161">Pour commencer à utiliser WebView2, voir [guides de mise en route de WebView2][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="be45c-161">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="be45c-162">Pour obtenir un exemple complet de fonctionnalités WebView2, consultez la référentiel Samples [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="be45c-162">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="be45c-163">Pour plus d’informations sur les API WebView2, voir informations de référence sur les [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="be45c-163">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="be45c-164">Pour plus d’informations sur WebView2, voir [ressources WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="be45c-164">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="be45c-165">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="be45c-165">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome)"  

[Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions classe | Documents Microsoft"  
[Webview2ReferenceWin3209538Webview2IdlParameters]: ../reference/win32/0-9-538/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-global | Documents Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
