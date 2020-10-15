---
description: Découvrez comment déboguer des contrôles WebView2.
title: Commencer le débogage des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/14/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, applications Win32, Win32, Edge, ICoreWebView2, ICoreWebView2Host, contrôle de navigateur, html Edge
ms.openlocfilehash: 25a710796b499a78a43045266058029caa890b78
ms.sourcegitcommit: 61cc15d2fc89aee3e09cec48ef1e0e5bbf8d289a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/15/2020
ms.locfileid: "11119107"
---
# <span data-ttu-id="f1460-104">Commencer le débogage des applications WebView2</span><span class="sxs-lookup"><span data-stu-id="f1460-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="f1460-105">L’objectif du contrôle Microsoft Edge WebView2 est de combiner le meilleur des outils et des fonctionnalités de développement d’applications Web et natives.</span><span class="sxs-lookup"><span data-stu-id="f1460-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="f1460-106">Lorsque vous développez votre application WebView2, vous devez déboguer votre application.</span><span class="sxs-lookup"><span data-stu-id="f1460-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="f1460-107">Cet article présente les différents outils à utiliser pour déboguer votre code Web et votre code natif dans votre application WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="f1460-108">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="f1460-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="f1460-109">Utilisez les [outils de développement Microsoft Edge (chrome)][DevtoolsGuideChromiumMain] pour déboguer le contenu Web affiché dans les contrôles WebView2, de la même façon que vous pouvez déboguer une autre page Web affichée dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f1460-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="f1460-110">Pour ouvrir le DevTools, positionnez le focus sur le contrôle WebView, puis utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f1460-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="f1460-111">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="f1460-111">Select `F12`.</span></span>  
*   <span data-ttu-id="f1460-112">Sélectionnez `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="f1460-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="f1460-113">Ouvrez le menu contextuel (cliquez avec le bouton droit sur \) et sélectionnez `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="f1460-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="f1460-114">Pour plus d’informations, voir [vue d’ensemble de devtools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="f1460-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Débogage DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="f1460-116">Débogage DevTools</span><span class="sxs-lookup"><span data-stu-id="f1460-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="f1460-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="f1460-118">Visual Studio fournit différents outils de débogage pour le Web et le code natif dans les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="f1460-119">Dans la section Visual Studio, le focus principal est le débogage de contrôles WebView, mais les autres méthodes de débogage dans Visual Studio sont disponibles comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="f1460-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="f1460-120">Le processus suivant permet de déboguer du code Web et du code natif dans des applications Win32 ou des compléments Office uniquement.</span><span class="sxs-lookup"><span data-stu-id="f1460-120">Use the following process to debug web and native code in Win32 applications or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="f1460-121">Quand vous déboguez votre application dans Visual Studio avec le débogueur natif en pièce jointe, la sélection `F12` de l’application risque de déclencher le débogueur natif au lieu des outils de développement.</span><span class="sxs-lookup"><span data-stu-id="f1460-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="f1460-122">Sélectionnez `Ctrl` + `Shift` + `I` ou utilisez le menu contextuel (cliquez avec le bouton droit sur \) pour éviter la situation.</span><span class="sxs-lookup"><span data-stu-id="f1460-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="f1460-123">Avant de commencer, assurez-vous que les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="f1460-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="f1460-124">Pour déboguer les scripts, l’application doit être lancée à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f1460-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="f1460-125">Vous ne pouvez pas attacher de débogueur à un processus WebView2 en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="f1460-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="f1460-126">Installez Visual Studio 2019 version 16,4 Preview 2 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="f1460-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="f1460-127">Installez et configurez les outils de débogage de script dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f1460-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="f1460-128">Procédez comme suit pour installer le composant **Diagnostics JavaScript** dans le **développement de bureau avec C++**.</span><span class="sxs-lookup"><span data-stu-id="f1460-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="f1460-129">Dans la barre de l’Explorateur Windows, tapez `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="f1460-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="f1460-130">Sélectionnez **programme d’installation de Visual Studio** pour l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="f1460-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="f1460-131">Dans le programme d’installation de Visual Studio, sur la version installée, sélectionnez le bouton **plus** , puis sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="f1460-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="f1460-132">Dans Visual Studio, sous **charges de travail**, choisissez le paramètre **développement de bureau en C++** .</span><span class="sxs-lookup"><span data-stu-id="f1460-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Débogage DevTools" lightbox="./media/workloads.png":::
            <span data-ttu-id="f1460-134">Écran modification de la charge de travail dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="f1460-135">Choisissez **des composants individuels**.</span><span class="sxs-lookup"><span data-stu-id="f1460-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="f1460-136">Dans la zone de recherche, entrez `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="f1460-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="f1460-137">Sélectionnez le paramètre **Diagnostics JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="f1460-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="f1460-138">Sélectionnez **modifier**.</span><span class="sxs-lookup"><span data-stu-id="f1460-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Débogage DevTools" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="f1460-140">Onglet de modification de composants individuels dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f1460-141">Activez le débogage de script pour les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="f1460-142">Dans votre projet WebView2, ouvrez le menu contextuel, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="f1460-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="f1460-143">Sous les **Propriétés de configuration**, sélectionnez **débogage**.</span><span class="sxs-lookup"><span data-stu-id="f1460-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="f1460-144">Sous le **type de débogueur**, choisissez **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="f1460-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Débogage DevTools" lightbox="./media/enbjs.png":::
           <span data-ttu-id="f1460-146">Propriété de configuration du **débogage** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="f1460-147">Effectuez les opérations suivantes pour déboguer votre application WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="f1460-148">Pour définir un point d’arrêt dans votre code source, positionnez le curseur à gauche du numéro de ligne et choisissez de définir un point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f1460-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="f1460-149">L’adaptateur de débogage JS/TS n’effectue pas le mappage de chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="f1460-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="f1460-150">Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Débogage DevTools" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="f1460-152">Ajouter un point d’arrêt dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f1460-153">Pour exécuter le débogueur, choisissez la taille en bits de la plateforme, puis sélectionnez le bouton de lecture de couleur verte en regard du **débogueur Windows local**.</span><span class="sxs-lookup"><span data-stu-id="f1460-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="f1460-154">L’application s’exécute et le débogueur se connecte au premier processus WebView2 créé.</span><span class="sxs-lookup"><span data-stu-id="f1460-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text="Débogage DevTools" lightbox="./media/run.png"::: 
       <span data-ttu-id="f1460-156">**Débogueur Windows** de Visual Studio local</span><span class="sxs-lookup"><span data-stu-id="f1460-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="f1460-157">Dans la **console de débogage**, recherchez la sortie du débogueur.</span><span class="sxs-lookup"><span data-stu-id="f1460-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text="Débogage DevTools" lightbox="./media/console.png"::: 
       <span data-ttu-id="f1460-159">Console de **débogage** de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<span data-ttu-id="f1460-160">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="f1460-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="f1460-161">Utilisez le code Microsoft Visual Studio pour déboguer les scripts qui s’exécutent dans les contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="f1460-162">Dans le code Visual Studio, effectuez les actions suivantes pour déboguer votre code.</span><span class="sxs-lookup"><span data-stu-id="f1460-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="f1460-163">Un fichier est requis pour votre projet `launch.json` .</span><span class="sxs-lookup"><span data-stu-id="f1460-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="f1460-164">Si votre projet ne comporte pas de `launch.json` fichier, copiez l’extrait de code suivant et créez un `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="f1460-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
        
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",
        "env": {
            // Customize for your application location if needed
            "Path": "%path%;e:/path/to/your/application/location; "
        },
        "useWebView": true,
    ```  
        
1.  <span data-ttu-id="f1460-165">Pour définir un point d’arrêt dans votre code source, pointez sur la ligne, puis sélectionnez</span><span class="sxs-lookup"><span data-stu-id="f1460-165">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpointvs.png" alt-text="Débogage DevTools" lightbox="./media/breakpointvs.png":::
       <span data-ttu-id="f1460-167">Le point d’arrêt est défini dans le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-167">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
    > [!NOTE]
    > <span data-ttu-id="f1460-168">Dans la mesure où le code Visual Studio n’effectue pas le mappage source, assurez-vous de définir des points d’arrêt dans le même fichier que WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-168">Because Visual Studio Code does not perform source mapping, ensure you set breakpoints in the same file that WebView2 uses.</span></span>  <span data-ttu-id="f1460-169">Dans le cas contraire, le code Visual Studio n’interrompt pas le code en cours d’exécution au point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="f1460-169">If the paths do not match, Visual Studio Code does not pause the running code at the breakpoint.</span></span>  
    
1.  <span data-ttu-id="f1460-170">Exécutez le code.</span><span class="sxs-lookup"><span data-stu-id="f1460-170">Run the code.</span></span>  
    1.  <span data-ttu-id="f1460-171">Dans l’onglet **exécuter** , choisissez la configuration de lancement dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="f1460-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="f1460-172">Pour démarrer le débogage de votre application, sélectionnez Démarrer le débogage, qui est le triangle vert en regard de la liste déroulante de configuration de lancement.</span><span class="sxs-lookup"><span data-stu-id="f1460-172">To start debugging your application, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/runvs.png" alt-text="Débogage DevTools" lightbox="./media/runvs.png":::
           <span data-ttu-id="f1460-174">Onglet exécuter de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="f1460-175">Ouvrez la **console de débogage** pour afficher les erreurs et la sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="f1460-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/resultsvs.png" alt-text="Débogage DevTools" lightbox="./media/resultsvs.png":::
       <span data-ttu-id="f1460-177">Console de débogage de code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1460-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="f1460-178">**Paramètres avancés**:</span><span class="sxs-lookup"><span data-stu-id="f1460-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="f1460-179">Débogage WebView ciblé.</span><span class="sxs-lookup"><span data-stu-id="f1460-179">Targeted Webview debugging.</span></span> 

    <span data-ttu-id="f1460-180">Dans certaines applications WebView2, vous pouvez utiliser plusieurs contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-180">In some WebView2 applications, you may use more than one WebView2 control.</span></span> <span data-ttu-id="f1460-181">Pour sélectionner le contrôle WebView2 à déboguer dans cette situation, vous pouvez utiliser le débogage de WebView2 ciblé</span><span class="sxs-lookup"><span data-stu-id="f1460-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="f1460-182">Ouvrez `launch.json` et effectuez les actions suivantes pour utiliser le débogage d’affichage WebView ciblé.</span><span class="sxs-lookup"><span data-stu-id="f1460-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="f1460-183">Vérifiez que le `useWebview` paramètre est défini sur `true` .</span><span class="sxs-lookup"><span data-stu-id="f1460-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="f1460-184">Ajoutez le `urlFilter` paramètre.</span><span class="sxs-lookup"><span data-stu-id="f1460-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="f1460-185">Lorsque le contrôle WebView2 navigue vers une URL, la `urlFilter` valeur de paramètre est utilisée pour comparer les chaînes qui s’affichent dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="f1460-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
    
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="f1460-186">Lors du débogage de votre application, il est possible que vous deviez parcourir le code du début du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="f1460-186">When debugging your application, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="f1460-187">Si vous voulez afficher des pages Web sur des sites et que vous n’avez pas accès au code source, vous pouvez utiliser l' `?=value`  option, car les pages Web ignorent les paramètres non reconnus.</span><span class="sxs-lookup"><span data-stu-id="f1460-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="f1460-188">Une fois la première correspondance trouvée dans l’URL, le débogueur s’arrête.</span><span class="sxs-lookup"><span data-stu-id="f1460-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="f1460-189">Vous ne pouvez pas déboguer deux contrôles WebView2 en même temps, car le port CDP est partagé par tous les contrôles WebView2 et utilise un numéro de port unique.</span><span class="sxs-lookup"><span data-stu-id="f1460-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="f1460-190">Déboguer des processus en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="f1460-190">Debug running processes</span></span>  
    
    <span data-ttu-id="f1460-191">Il est possible que vous deviez joindre le débogueur pour exécuter les processus WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="f1460-192">Pour ce faire, dans `launch.json` , mettez à jour le `request` paramètre en `attach` .</span><span class="sxs-lookup"><span data-stu-id="f1460-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
        
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
        
    <span data-ttu-id="f1460-193">Votre contrôle WebView2 doit ouvrir le port CDP pour permettre le débogage du contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="f1460-194">Votre code doit être créé pour s’assurer qu’un seul contrôle WebView2 est ouvert par un port CDP (chrome Developer Protocol) avant de démarrer le débogueur.</span><span class="sxs-lookup"><span data-stu-id="f1460-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="f1460-195">Options de suivi de débogage</span><span class="sxs-lookup"><span data-stu-id="f1460-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="f1460-196">Ajoutez le `trace` paramètre à launch.jsactivé pour activer le suivi de débogage.</span><span class="sxs-lookup"><span data-stu-id="f1460-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="f1460-197">Ajouter un `trace` paramètre.</span><span class="sxs-lookup"><span data-stu-id="f1460-197">Add `trace` parameter.</span></span>  
        
 
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/application.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/tracelog.png" alt-text="Débogage DevTools" lightbox="./media/tracelog.png":::
                 <span data-ttu-id="f1460-199">Enregistrer la sortie de débogage dans un fichier journal</span><span class="sxs-lookup"><span data-stu-id="f1460-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text="Débogage DevTools" lightbox="./media/verbose.png":::
                 <span data-ttu-id="f1460-201">Sortie du débogage de code Visual Studio avec l’affichage suivi détaillé activé</span><span class="sxs-lookup"><span data-stu-id="f1460-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="f1460-202">Déboguer des compléments Office.</span><span class="sxs-lookup"><span data-stu-id="f1460-202">Debug Office Add-ins.</span></span>
    
    <span data-ttu-id="f1460-203">Si vous déboguez des compléments Office, ouvrez le code source du complément dans une instance distincte du code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f1460-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="f1460-204">Ouvrez launch.jsdans votre application WebView2, puis ajoutez l’extrait de code suivant pour joindre le débogueur au complément Office.</span><span class="sxs-lookup"><span data-stu-id="f1460-204">Open launch.json in your WebView2 application and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="f1460-205">Résoudre les problèmes du débogueur</span><span class="sxs-lookup"><span data-stu-id="f1460-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="f1460-206">Vous pouvez rencontrer les situations suivantes lors de l’utilisation du débogueur.</span><span class="sxs-lookup"><span data-stu-id="f1460-206">You may encounter the following scenarios when using the debugger.</span></span>  

    *   <span data-ttu-id="f1460-207">Le débogueur ne s’arrête pas au point d’arrêt et vous avez une sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="f1460-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="f1460-208">Pour résoudre ce problème, vérifiez que le fichier contenant le point d’arrêt est le même que celui utilisé par le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="f1460-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="f1460-209">Le débogueur n’effectue pas le mappage de chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="f1460-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="f1460-210">Vous ne pouvez pas attacher de processus en cours d’exécution et vous obtenez une erreur de temporisation.</span><span class="sxs-lookup"><span data-stu-id="f1460-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="f1460-211">Pour résoudre ce problème, vérifiez que le contrôle WebView2 a ouvert le port CDP.</span><span class="sxs-lookup"><span data-stu-id="f1460-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="f1460-212">Vérifiez que votre  `additionalBrowserArguments`  valeur dans le Registre est correcte ou que les options sont correctes.</span><span class="sxs-lookup"><span data-stu-id="f1460-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="f1460-213">Pour plus d’informations, consultez [additionalBrowserArguments pour dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] et [additionalBrowserArguments pour Win32][Webview2ReferenceWin32Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="f1460-213">For more information, see [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
    
* * *  


* * *  

## <span data-ttu-id="f1460-214">Voir également</span><span class="sxs-lookup"><span data-stu-id="f1460-214">See also</span></span>  

*   <span data-ttu-id="f1460-215">Pour commencer à utiliser WebView2, voir [guides de mise en route de WebView2][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="f1460-215">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="f1460-216">Pour obtenir un exemple complet de fonctionnalités WebView2, consultez la référentiel Samples [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="f1460-216">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="f1460-217">Pour plus d’informations sur les API WebView2, voir informations de référence sur les [API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="f1460-217">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="f1460-218">Pour plus d’informations sur WebView2, voir [ressources WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="f1460-218">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="f1460-219">Contacter l’équipe WebView de Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f1460-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome)"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriété CoreWebView2EnvironmentOptions. AdditionalBrowserArguments (Microsoft. Web. WebView2. Core) | Documents Microsoft"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment-global | Documents Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Référence sur l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Mise en route-présentation de Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "Commentaires sur le WebView-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "Exemples de WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Quelles sont les nouveautés? -Débogueur JavaScript pour le code Visual Studio-Microsoft/vscode-js-déboguer | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Applications WebView Microsoft Edge (chrome): débogueur de code Visual Studio pour Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
