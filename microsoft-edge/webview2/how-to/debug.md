---
description: Découvrez comment déboguer des contrôles WebView2.
title: Commencer à déboguer des applications WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, webview, win32 apps, win32, edge, ICoreWebView2, ICoreWebView2Host, browser control, edge html
ms.openlocfilehash: 01cd67897f7041bca0cedcee2cc3242f3ebcc962
ms.sourcegitcommit: 777b16ef10363f2dfd755f115ee2d4c81a8de46f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11535892"
---
# <a name="get-started-debugging-webview2-apps"></a><span data-ttu-id="28fb4-104">Commencer à déboguer des applications WebView2</span><span class="sxs-lookup"><span data-stu-id="28fb4-104">Get started debugging WebView2 apps</span></span>  

<span data-ttu-id="28fb4-105">L’objectif du contrôle Microsoft Edge WebView2 est de combiner les meilleurs outils et fonctionnalités de développement d’applications web et natives.</span><span class="sxs-lookup"><span data-stu-id="28fb4-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native app development features and tools.</span></span>  <span data-ttu-id="28fb4-106">Lorsque vous développez votre application WebView2, vous devez la déboguer.</span><span class="sxs-lookup"><span data-stu-id="28fb4-106">When you develop your WebView2 app, you should debug your app.</span></span>  <span data-ttu-id="28fb4-107">Cet article décrit les différents outils à utiliser pour déboguer votre code web et le code natif dans votre application WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 app.</span></span>  

## [<a name="microsoft-edge-devtools"></a><span data-ttu-id="28fb4-108">Outils Microsoft Edge Dev</span><span class="sxs-lookup"><span data-stu-id="28fb4-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="28fb4-109">Utilisez les outils de développement [Microsoft Edge (Chromium)][DevtoolsGuideChromiumMain] pour déboguer le contenu web affiché dans les contrôles WebView2, de la même manière que vous pouvez déboguer pour une autre page web affichée dans Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="28fb4-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="28fb4-110">Pour ouvrir DevTools, définissez le focus sur le contrôle WebView, puis utilisez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="28fb4-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="28fb4-111">Sélectionnez `F12` .</span><span class="sxs-lookup"><span data-stu-id="28fb4-111">Select `F12`.</span></span>  
*   <span data-ttu-id="28fb4-112">Sélectionnez `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="28fb4-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="28fb4-113">Ouvrez le menu contexto \(clic droit\) et choisissez `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="28fb4-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  
    
<span data-ttu-id="28fb4-114">Pour plus d’informations, accédez à la vue [d’ensemble de DevTools.][DevtoolsGuideChromiumMain]</span><span class="sxs-lookup"><span data-stu-id="28fb4-114">For more information, navigate to [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Débogage DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="28fb4-116">Débogage DevTools</span><span class="sxs-lookup"><span data-stu-id="28fb4-116">DevTools debugging</span></span>  
:::image-end:::    

## [<a name="visual-studio"></a><span data-ttu-id="28fb4-117">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="28fb4-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="28fb4-118">Visual Studio fournit différents outils de débogage pour le code web et le code natif dans les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-118">Visual Studio provides various debugging tools for web and native code in WebView2 apps.</span></span>  <span data-ttu-id="28fb4-119">Dans la section Visual Studio, le principal objectif est le débogage des contrôles WebView, mais les autres méthodes de débogage dans Visual Studio sont disponibles comme d’habitude.</span><span class="sxs-lookup"><span data-stu-id="28fb4-119">In the Visual Studio section, the primary focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="28fb4-120">Utilisez le processus suivant pour déboguer le code web et natif dans les applications Win32 ou les applications Office uniquement.</span><span class="sxs-lookup"><span data-stu-id="28fb4-120">Use the following process to debug web and native code in Win32 apps or Office Add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="28fb4-121">Lorsque vous déboguer votre application dans Visual Studio avec le déboguer natif attaché, la sélection peut déclencher le déboguer natif au lieu des outils `F12` de développement.</span><span class="sxs-lookup"><span data-stu-id="28fb4-121">When you debug your app in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="28fb4-122">Sélectionnez `Ctrl` + `Shift` + `I` ou utilisez le menu contexto \(clic droit\) pour éviter la situation.</span><span class="sxs-lookup"><span data-stu-id="28fb4-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="28fb4-123">Avant de commencer, assurez-vous que les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="28fb4-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="28fb4-124">Pour déboguer des scripts, l’application doit être lancée à partir de Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="28fb4-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="28fb4-125">Vous ne pouvez pas attacher un débompeur à un processus WebView2 en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="28fb4-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="28fb4-126">Installez Visual Studio version 2019 16.4 Preview 2 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="28fb4-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  
    
<span data-ttu-id="28fb4-127">Installez et installez les outils de débogger de script dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="28fb4-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="28fb4-128">Effectuer les actions suivantes pour installer le **composant de diagnostics JavaScript** dans le développement **de bureau avec C++**.</span><span class="sxs-lookup"><span data-stu-id="28fb4-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  
    1.  <span data-ttu-id="28fb4-129">Dans la barre de l’Explorateur Windows, tapez `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="28fb4-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1.  <span data-ttu-id="28fb4-130">Choisissez **Visual Studio installer pour** l’ouvrir.</span><span class="sxs-lookup"><span data-stu-id="28fb4-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1.  <span data-ttu-id="28fb4-131">Dans le Visual Studio installer, sur la version installée, choisissez le bouton **Plus,** puis choisissez **Modifier**.</span><span class="sxs-lookup"><span data-stu-id="28fb4-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1.  <span data-ttu-id="28fb4-132">Dans Visual Studio, sous **Charges de**travail, choisissez le paramètre **Développement de bureau en C++.**</span><span class="sxs-lookup"><span data-stu-id="28fb4-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Visual Studio écran Modification des charges de travail" lightbox="./media/workloads.png":::
            <span data-ttu-id="28fb4-134">Visual Studio écran Modification des charges de travail</span><span class="sxs-lookup"><span data-stu-id="28fb4-134">Visual Studio Modifying Workloads Screen</span></span>
        :::image-end:::  
        
    1.  <span data-ttu-id="28fb4-135">Choisissez **des composants individuels.**</span><span class="sxs-lookup"><span data-stu-id="28fb4-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="28fb4-136">Dans la zone de recherche, entrez `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="28fb4-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="28fb4-137">Choisissez le **paramètre de diagnostic JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="28fb4-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="28fb4-138">Choose **Modify**.</span><span class="sxs-lookup"><span data-stu-id="28fb4-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indiv-comp.png" alt-text="Visual Studio’onglet Modification des composants individuels" lightbox="./media/indiv-comp.png":::
           <span data-ttu-id="28fb4-140">Visual Studio’onglet Modification des composants individuels</span><span class="sxs-lookup"><span data-stu-id="28fb4-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="28fb4-141">Activez le débogage de script pour les applications WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-141">Enable script debugging for WebView2 apps.</span></span>  
    1.  <span data-ttu-id="28fb4-142">Dans votre projet WebView2, ouvrez le menu contexto \(clic droit\), puis choisissez **Propriétés.**</span><span class="sxs-lookup"><span data-stu-id="28fb4-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="28fb4-143">Sous les **propriétés de configuration,** choisissez **Débogage.**</span><span class="sxs-lookup"><span data-stu-id="28fb4-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="28fb4-144">Sous le **type de débogger,** choisissez **JavaScript (WebView2).**</span><span class="sxs-lookup"><span data-stu-id="28fb4-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enb-js.png" alt-text="Visual Studio configuration du débogage" lightbox="./media/enb-js.png":::
           <span data-ttu-id="28fb4-146">Visual Studio de **configuration de débogage**</span><span class="sxs-lookup"><span data-stu-id="28fb4-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="28fb4-147">Effectuer les actions suivantes pour déboguer votre application WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-147">Complete the following actions to debug your WebView2 app.</span></span>  

1.  <span data-ttu-id="28fb4-148">Pour définir un point d’arrêt dans votre code source, pointez sur la gauche du numéro de ligne et choisissez de définir un point d’arrêt.</span><span class="sxs-lookup"><span data-stu-id="28fb4-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="28fb4-149">L’adaptateur de débogage JS/TS n’effectue pas de mappage de chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="28fb4-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="28fb4-150">Vous devez ouvrir exactement le même chemin d’accès associé à votre WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Visual Studio ajouter un point d’arrêt" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="28fb4-152">Visual Studio ajouter un point d’arrêt</span><span class="sxs-lookup"><span data-stu-id="28fb4-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28fb4-153">Pour exécuter le débompeur, choisissez la taille de bits de la plateforme, puis choisissez le bouton de lecture vert en côté du débogger **Windows local.**</span><span class="sxs-lookup"><span data-stu-id="28fb4-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="28fb4-154">L’application s’exécute et le débogger se connecte au premier processus WebView2 créé.</span><span class="sxs-lookup"><span data-stu-id="28fb4-154">The app runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Visual Studio Local Windows Debugger" lightbox="./media/run.png"::: 
       <span data-ttu-id="28fb4-156">Visual Studio Local **Windows Debugger**</span><span class="sxs-lookup"><span data-stu-id="28fb4-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="28fb4-157">Dans la **console de débogage,** recherchez la sortie du déboguer.</span><span class="sxs-lookup"><span data-stu-id="28fb4-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Visual Studio console de débogage" lightbox="./media/console.png"::: 
       <span data-ttu-id="28fb4-159">Visual Studio console **de débogage**</span><span class="sxs-lookup"><span data-stu-id="28fb4-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
## [<a name="visual-studio-code"></a><span data-ttu-id="28fb4-160">VisualStudioCode</span><span class="sxs-lookup"><span data-stu-id="28fb4-160">Visual Studio Code</span></span>](#tab/visualstudiocode)  

<span data-ttu-id="28fb4-161">Utilisez Microsoft Visual Studio Code pour déboguer les scripts qui s’exécutent dans les contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-161">Use Microsoft Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <!--Ensure that you're using Visual Studio Code version [insert build here] or later.  -->  

<span data-ttu-id="28fb4-162">Dans Visual Studio code, effectuer les actions suivantes pour déboguer votre code.</span><span class="sxs-lookup"><span data-stu-id="28fb4-162">In Visual Studio Code, complete the following actions to debug your code.</span></span> 

1.  <span data-ttu-id="28fb4-163">Votre projet doit avoir un `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="28fb4-163">Your project is required to have a `launch.json` file.</span></span>  <span data-ttu-id="28fb4-164">Si votre projet ne comprend pas de fichier, copiez l’extrait de code suivant `launch.json` et créez un `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="28fb4-164">If your project doesn't have a `launch.json` file, copy the following code snippet and create a new `launch.json` file.</span></span>  
    
    ```json
        "name": "Hello debug world",
        "type": "pwa-msedge",
        "port": 9222, // The port value is optional, and the default value is 9222.
        "request": "launch",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",
        "env": {
            // Customize for your app location if needed
            "Path": "%path%;e:/path/to/your/app/location; "
        },
        "useWebView": true,
        // The following two lines setup source path mapping, where `url` is the start page of your app, and `webRoot` is the top level directory with all your code files.
        "url": "file:///${workspaceFolder}/path/to/your/toplevel/foo.html",
        "webRoot": "${workspaceFolder}/path/to/your/assets"
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="28fb4-165">Visual Studio mappage du chemin d’accès source du code nécessite désormais l’URL, de sorte que votre application reçoit désormais un paramètre de ligne de commande au démarrage.</span><span class="sxs-lookup"><span data-stu-id="28fb4-165">Visual Studio Code source path mapping now requires the URL, so your app now receives a command-line parameter when it starts.</span></span>  <span data-ttu-id="28fb4-166">Vous pouvez ignorer le paramètre en toute sécurité `url` si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="28fb4-166">You may safely ignore the `url` parameter if needed.</span></span>  
    
1.  <span data-ttu-id="28fb4-167">Pour définir un point d’arrêt dans votre code source, pointez sur la ligne, puis sélectionnez</span><span class="sxs-lookup"><span data-stu-id="28fb4-167">To set a breakpoint in your source code, hover on the line, and select</span></span> `F9`
    
    :::image type="complex" source="./media/breakpoint-vs.png" alt-text="Le point d’arrêt est Visual Studio Code" lightbox="./media/breakpoint-vs.png":::
       <span data-ttu-id="28fb4-169">Le point d’arrêt est Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="28fb4-169">Breakpoint is set in Visual Studio Code</span></span>  
    :::image-end:::
    
1.  <span data-ttu-id="28fb4-170">Exécutez le code.</span><span class="sxs-lookup"><span data-stu-id="28fb4-170">Run the code.</span></span>  
    1.  <span data-ttu-id="28fb4-171">Sous **l’onglet** Exécuter, choisissez la configuration de lancement dans le menu déroulant.</span><span class="sxs-lookup"><span data-stu-id="28fb4-171">On the **Run** tab, choose the launch configuration from the dropdown menu.</span></span>  
    1.  <span data-ttu-id="28fb4-172">Pour commencer à déboguer votre application, sélectionnez Démarrer le débogage, qui est le triangle vert à côté de la zone de configuration de lancement.</span><span class="sxs-lookup"><span data-stu-id="28fb4-172">To start debugging your app, choose Start Debugging, which is the green triangle next to the launch configuration drop down.</span></span>  
        
        :::image type="complex" source="./media/run-vs.png" alt-text=" Visual Studio’onglet Code Run" lightbox="./media/run-vs.png":::
           <span data-ttu-id="28fb4-174">Visual Studio’onglet Code Run</span><span class="sxs-lookup"><span data-stu-id="28fb4-174">Visual Studio Code Run tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="28fb4-175">Ouvrez **la Console de débogage** pour afficher la sortie et les erreurs de débogage.</span><span class="sxs-lookup"><span data-stu-id="28fb4-175">Open **Debug Console** to view the debug output and errors.</span></span>  
    
    :::image type="complex" source="./media/results-vs.png" alt-text=" Visual Studio console de débogage de code" lightbox="./media/results-vs.png":::
       <span data-ttu-id="28fb4-177">Visual Studio console de débogage de code</span><span class="sxs-lookup"><span data-stu-id="28fb4-177">Visual Studio Code Debug Console</span></span>  
    :::image-end:::  
    
<span data-ttu-id="28fb4-178">**Paramètres avancés**:</span><span class="sxs-lookup"><span data-stu-id="28fb4-178">**Advanced Settings**:</span></span>  

*   <span data-ttu-id="28fb4-179">Débogage Webview ciblé.</span><span class="sxs-lookup"><span data-stu-id="28fb4-179">Targeted Webview debugging.</span></span> 
    
    <span data-ttu-id="28fb4-180">Dans certaines applications WebView2, vous pouvez utiliser plusieurs contrôles WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-180">In some WebView2 apps, you may use more than one WebView2 control.</span></span> <span data-ttu-id="28fb4-181">Pour sélectionner le contrôle WebView2 à déboguer dans ce cas, vous pouvez utiliser le débogage webview2 ciblé</span><span class="sxs-lookup"><span data-stu-id="28fb4-181">To pick the WebView2 control to debug in this situation you can use targeted webview2 debugging</span></span> 
    
    <span data-ttu-id="28fb4-182">Ouvrez `launch.json` et terminez les actions suivantes pour utiliser le débogage Webview ciblé.</span><span class="sxs-lookup"><span data-stu-id="28fb4-182">Open `launch.json` and complete the following actions to use targeted Webview debugging.</span></span>  
    
    1.  <span data-ttu-id="28fb4-183">Confirmez que `useWebview` le paramètre est paramétrable sur `true` .</span><span class="sxs-lookup"><span data-stu-id="28fb4-183">Confirm that the `useWebview` parameter is set to `true`.</span></span>  
    1.  <span data-ttu-id="28fb4-184">Ajoutez le `urlFilter` paramètre.</span><span class="sxs-lookup"><span data-stu-id="28fb4-184">Add the `urlFilter` parameter.</span></span>  <span data-ttu-id="28fb4-185">Lorsque le contrôle WebView2 navigue vers une URL, la valeur du paramètre est utilisée pour comparer les chaînes qui apparaissent `urlFilter` dans l’URL.</span><span class="sxs-lookup"><span data-stu-id="28fb4-185">When the WebView2 control navigates to a URL, the `urlFilter` parameter value is used to compare strings that appear in the URL.</span></span>  
        
    ```json
    "useWebview": "true",
    "urlFilter": "*index.ts",
    
    // Other urlFilter options.
    
    urlFilter="*index.ts"    // Match any url that ends with index.ts, and ignore all leading characters. 
    urlFilter="*index*"      // Match any url that contains the string index anywhere in the URL.  
    urlFilter="file://C:/path/to/my/index.ts," // To match explicit file called index.ts.  
    ```  
    
    <span data-ttu-id="28fb4-186">Lors du débogage de votre application, vous devrez peut-être passer du code au début du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="28fb4-186">When debugging your app, you may need to step through the code from the beginning of the rendering process.</span></span> <span data-ttu-id="28fb4-187">Si vous rendez des pages web sur des sites et que vous n’avez pas accès au code source, vous pouvez utiliser cette option, car les pages web ignorent les `?=value`  paramètres non reconnus.</span><span class="sxs-lookup"><span data-stu-id="28fb4-187">If you are rendering webpages on sites and you don't have access to the source code, you can use the `?=value` option, because webpages ignore unrecognized parameters.</span></span>   
    
    > [!IMPORTANT]
    > <span data-ttu-id="28fb4-188">Une fois la première correspondance trouvée dans l’URL, le débogger s’arrête.</span><span class="sxs-lookup"><span data-stu-id="28fb4-188">After the first match is found in the URL, the debugger stops.</span></span>  <span data-ttu-id="28fb4-189">Vous ne pouvez pas déboguer deux contrôles WebView2 en même temps, car le port CDP est partagé par tous les contrôles WebView2 et utilise un numéro de port unique.</span><span class="sxs-lookup"><span data-stu-id="28fb4-189">You cannot debug two WebView2 controls at the same time because the CDP port is shared by all WebView2 controls, and uses a single port number.</span></span>  
    
*   <span data-ttu-id="28fb4-190">Débogage des processus en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="28fb4-190">Debug running processes</span></span>  
    
    <span data-ttu-id="28fb4-191">Vous devrez peut-être attacher le débogger aux processus WebView2 en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="28fb4-191">You may need to attach the debugger to running WebView2 processes.</span></span> <span data-ttu-id="28fb4-192">Pour ce faire, dans `launch.json` , mettez à jour le paramètre sur `request` `attach` .</span><span class="sxs-lookup"><span data-stu-id="28fb4-192">To do that, in `launch.json`, update the `request` parameter to `attach`.</span></span>
    
    ```json
        "name": "Hello debugging world",
        "type": "pwa-msedge",
        "port": 9222, 
        "request": "attach",
        "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
        "env": {
            "Path": "%path%;e:/path/to/your/build/location; "  
        },
        "useWebView": true
    ```  
    
    <span data-ttu-id="28fb4-193">Votre contrôle WebView2 doit ouvrir le port CDP pour autoriser le débogage du contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-193">Your WebView2 control must open the CDP port to allow debugging of the WebView2 control.</span></span>  <span data-ttu-id="28fb4-194">Votre code doit être créé pour vous assurer qu’un seul contrôle WebView2 dispose d’un port CDP (Chrome Developer Protocol) ouvert, avant de démarrer le débogger.</span><span class="sxs-lookup"><span data-stu-id="28fb4-194">Your code must be built to ensure that only one WebView2 control has a Chrome Developer Protocol (CDP) port open, before starting the debugger.</span></span>  
    
*   <span data-ttu-id="28fb4-195">Options de suivi du débogage</span><span class="sxs-lookup"><span data-stu-id="28fb4-195">Debug tracing options</span></span>  
    
    <span data-ttu-id="28fb4-196">Ajoutez `trace` le paramètre à launch.jsactivé pour activer le suivi du débogage.</span><span class="sxs-lookup"><span data-stu-id="28fb4-196">Add the `trace` parameter to launch.json to enable debug tracing.</span></span>  
    
    1.  <span data-ttu-id="28fb4-197">Ajouter un `trace` paramètre.</span><span class="sxs-lookup"><span data-stu-id="28fb4-197">Add `trace` parameter.</span></span>  
        
        :::row:::
           :::column span="":::
              ```json
                "name": "Hello debugging world",
                "type": "pwa-msedge",
                "port": 9222, 
                "request": "attach",
                "runtimeExecutable": "C:/path/to/your/webview2/app.exe",  
                "env": {
                "Path": "%path%;e:/path/to/your/build/location; "  
                },
                "useWebView": true
                ,"trace": true  // Turn on  debug tracing, and save the output to a log file.
              ```  
              
              :::image type="complex" source="./media/trace-log.png" alt-text=" Enregistrez la sortie de débogage dans un fichier journal." lightbox="./media/trace-log.png":::
                 <span data-ttu-id="28fb4-199">Enregistrer la sortie de débogage dans un fichier journal</span><span class="sxs-lookup"><span data-stu-id="28fb4-199">Save debug output to a log file</span></span>  
              :::image-end:::  
           :::column-end:::
           :::column span="":::
              ```json
              ,"trace": "verbose"  // Turn on verbose tracing in the Debug Output pane.
              ```  
              
              :::image type="complex" source="./media/verbose.png" alt-text=" Sortie détaillée" lightbox="./media/verbose.png":::
                 <span data-ttu-id="28fb4-201">Visual Studio sortie de débogage de code avec suivi détaillée est allumé</span><span class="sxs-lookup"><span data-stu-id="28fb4-201">Visual Studio Code Debug Output with verbose tracing turned on</span></span>  
              :::image-end:::  
           :::column-end:::
        :::row-end:::  
        
*   <span data-ttu-id="28fb4-202">Déboguer des add-ins Office.</span><span class="sxs-lookup"><span data-stu-id="28fb4-202">Debug Office Add-ins.</span></span>  
    
    <span data-ttu-id="28fb4-203">Si vous déboguer des add-ins Office, ouvrez le code source du Visual Studio code.</span><span class="sxs-lookup"><span data-stu-id="28fb4-203">If you're debugging Office Add-ins, open the add-in source code in a separate instance of Visual Studio Code.</span></span>  <span data-ttu-id="28fb4-204">Ouvrez launch.jsdans votre application WebView2 et ajoutez l’extrait de code suivant pour joindre le débogger au add-in Office.</span><span class="sxs-lookup"><span data-stu-id="28fb4-204">Open launch.json in your WebView2 app and add the following code snippet to attach the debugger to the Office add-in.</span></span>
    
    ```json
    ,"debugServer": 4711
    ```  
    
*   <span data-ttu-id="28fb4-205">Résolution des problèmes du débogger</span><span class="sxs-lookup"><span data-stu-id="28fb4-205">Troubleshooting the debugger</span></span>  
    
    <span data-ttu-id="28fb4-206">Vous pouvez rencontrer les scénarios suivants lors de l’utilisation du débogger.</span><span class="sxs-lookup"><span data-stu-id="28fb4-206">You may encounter the following scenarios when using the debugger.</span></span>  
    
    *   <span data-ttu-id="28fb4-207">Le déboguer ne s’arrête pas au point d’arrêt et vous avez une sortie de débogage.</span><span class="sxs-lookup"><span data-stu-id="28fb4-207">The debugger doesn't stop at the breakpoint, and you have debug output.</span></span>  <span data-ttu-id="28fb4-208">Pour résoudre le problème, confirmez que le fichier avec le point d’arrêt est le même fichier que celui utilisé par le contrôle WebView2.</span><span class="sxs-lookup"><span data-stu-id="28fb4-208">To solve the issue, confirm that the file with the breakpoint is the same file that's used by the WebView2 control.</span></span>  <span data-ttu-id="28fb4-209">Le débogger n’effectue pas de mappage de chemin d’accès source.</span><span class="sxs-lookup"><span data-stu-id="28fb4-209">The debugger doesn't perform source path mapping.</span></span>  
    *   <span data-ttu-id="28fb4-210">Vous ne pouvez pas vous attacher à un processus en cours d’exécution et vous obtenez une erreur de délai d’accès.</span><span class="sxs-lookup"><span data-stu-id="28fb4-210">You can't attach to a running process, and you get a timeout error.</span></span>  <span data-ttu-id="28fb4-211">Pour résoudre le problème, confirmez que le contrôle WebView2 a ouvert le port CDP.</span><span class="sxs-lookup"><span data-stu-id="28fb4-211">To solve the issue, confirm that the WebView2 control opened the CDP port.</span></span>  <span data-ttu-id="28fb4-212"> `additionalBrowserArguments` Assurez-vous que votre valeur dans le Registre est correcte ou que les options sont correctes.</span><span class="sxs-lookup"><span data-stu-id="28fb4-212">Ensure your `additionalBrowserArguments` value in the registry is correct, or the options are correct.</span></span>  <span data-ttu-id="28fb4-213">Pour plus d’informations, accédez à [additionalBrowserArguments pour dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] et [additionalBrowserArguments pour Win32][Webview2ReferenceWin32Webview2IdlParameters].</span><span class="sxs-lookup"><span data-stu-id="28fb4-213">For more information, navigate to [additionalBrowserArguments for dotnet][Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments] and [additionalBrowserArguments for Win32][Webview2ReferenceWin32Webview2IdlParameters].</span></span>  
        
* * *  

## <a name="see-also"></a><span data-ttu-id="28fb4-214">Voir également</span><span class="sxs-lookup"><span data-stu-id="28fb4-214">See also</span></span>  

*   <span data-ttu-id="28fb4-215">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span><span class="sxs-lookup"><span data-stu-id="28fb4-215">To get started using WebView2, navigate to [WebView2 Get Started Guides][Webview2MainGetStarted].</span></span>  
*   <span data-ttu-id="28fb4-216">Pour obtenir un exemple complet des fonctionnalités WebView2, accédez au référentiel [WebView2Samples][GithubMicrosoftedgeWebview2samples] sur GitHub.</span><span class="sxs-lookup"><span data-stu-id="28fb4-216">For a comprehensive example of WebView2 capabilities, navigate to the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="28fb4-217">Pour plus d’informations sur les API WebView2, accédez à la [référence d’API.][Webview2ApiReference]</span><span class="sxs-lookup"><span data-stu-id="28fb4-217">For more detailed information about WebView2 APIs, navigate to [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="28fb4-218">Pour plus d’informations sur WebView2, accédez à [Ressources WebView2.][Webview2MainNextSteps]</span><span class="sxs-lookup"><span data-stu-id="28fb4-218">For more information about WebView2, navigate to [WebView2 Resources][Webview2MainNextSteps].</span></span>
    
## <a name="getting-in-touch-with-the-microsoft-edge-webview-team"></a><span data-ttu-id="28fb4-219">Entrer en contact avec l’équipe Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="28fb4-219">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[Webview2ReferenceDotnetMicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: /dotnet/api/microsoft.web.webview2.core.corewebview2environmentoptions.additionalbrowserarguments "Propriété CoreWebView2EnvironmentOptions.AdditionalBrowserArguments (Microsoft.Web.WebView2.Core) | Documents Microsoft"  
[Webview2ReferenceWin32Webview2IdlParameters]: /microsoft-edge/webview2/reference/win32/webview2-idl#createcorewebview2environmentwithoptions  "CreateCoreWebView2Environment - Globals | Documents Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Référence de l’API Microsoft Edge WebView2 | Documents Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Étapes suivantes : présentation de Microsoft Edge WebView2 (prévisualisation) | Documents Microsoft"  
[Webview2MainGetStarted]: ../index.md#get-started "Get started - Introduction to Microsoft Edge WebView2 (Preview) | Documents Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples - MicrosoftEdge/WebView2Samples | GitHub"  
