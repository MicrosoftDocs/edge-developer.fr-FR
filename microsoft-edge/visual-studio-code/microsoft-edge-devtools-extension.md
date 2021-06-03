---
description: Comment utiliser des éléments pour Microsoft Edge (Chromium) à partir de Visual Studio Code
title: Éléments pour Microsoft Edge (Chromium) de Visual Studio Code
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, vs code, visual studio code, éléments
ms.openlocfilehash: 83bac187fa2a9b1766a52f3f2cd176f171846e02
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398454"
---
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a><span data-ttu-id="79602-104">Microsoft Edge DevTools pour l’extension Visual Studio Code de recherche</span><span class="sxs-lookup"><span data-stu-id="79602-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="79602-105">Utiliser</span><span class="sxs-lookup"><span data-stu-id="79602-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="79602-106">cette extension à accéder dans Microsoft Edge DevTools à [l’intérieur Microsoft Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="79602-106">this extension to access in Microsoft Edge DevTools inside [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="79602-107">Vous avez accès aux outils **éléments** **et** réseau dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="79602-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="79602-108">Vous pouvez lancer ou attacher une instance de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="79602-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="79602-109">Une fois connecté, vous pouvez afficher la structure HTML d’runtime, modifier la disposition, résoudre les problèmes de style et inspecter le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="79602-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <a name="elements-tool"></a><span data-ttu-id="79602-110">Outil Éléments</span><span class="sxs-lookup"><span data-stu-id="79602-110">Elements tool</span></span>  

<span data-ttu-id="79602-111">Par défaut, l’extension lance une instance de navigateur dans une fenêtre unique et vous offre la fonctionnalité **Elements** de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="79602-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools pour Visual Studio Code’exécution avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="79602-113">Microsoft Edge DevTools pour Visual Studio Code’exécution avec une fenêtre de navigateur complète</span><span class="sxs-lookup"><span data-stu-id="79602-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="79602-114">Dans les paramètres d’extension, vous pouvez activer davantage de fonctionnalités telles que le **mode sans** tête et le **réseau.**</span><span class="sxs-lookup"><span data-stu-id="79602-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Activation (ou désactivation) du mode sans tête et inspection du réseau dans les paramètres d’extension" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="79602-116">Activation du mode sans tête \(ou désactivation\) et inspection du réseau dans les paramètres d’extension</span><span class="sxs-lookup"><span data-stu-id="79602-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <a name="headless-mode"></a><span data-ttu-id="79602-117">Mode sans tête</span><span class="sxs-lookup"><span data-stu-id="79602-117">Headless Mode</span></span>  

<span data-ttu-id="79602-118">En mode sans en-tête, cette extension ne lance pas une instance de navigateur complète pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="79602-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="79602-119">Il exécute une instance en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="79602-119">It runs an instance in the background.</span></span>  <span data-ttu-id="79602-120">Vous de devez peut-être rester à l’intérieur de l’éditeur et interagir avec le navigateur incorporé.</span><span class="sxs-lookup"><span data-stu-id="79602-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="79602-121">Une icône de navigateur supplémentaire n’est pas affichée dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="79602-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools pour les Visual Studio Code’exécution sans en-tête" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="79602-123">Microsoft Edge DevTools pour les Visual Studio Code’exécution avec un navigateur sans en-tête</span><span class="sxs-lookup"><span data-stu-id="79602-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="79602-124">Sur macOS, vous devez activer le mode sans tête comme mode préféré.</span><span class="sxs-lookup"><span data-stu-id="79602-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="79602-125">L’utilisation du mode sans en-tête doit résoudre un problème dans lequel, si la fenêtre n’est pas visible, la fenêtre du navigateur signale qu’elle `Not Active` l’est.</span><span class="sxs-lookup"><span data-stu-id="79602-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <a name="network-tool"></a><span data-ttu-id="79602-126">Outil réseau</span><span class="sxs-lookup"><span data-stu-id="79602-126">Network tool</span></span>  

<span data-ttu-id="79602-127">Si vous souhaitez également inspecter le trafic réseau de votre application, ouvrez les paramètres et allumez **l’onglet** Réseau.</span><span class="sxs-lookup"><span data-stu-id="79602-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspection du réseau dans Microsoft Edge DevTools pour les Visual Studio Code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="79602-129">Inspection du réseau dans Microsoft Edge DevTools pour les Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="79602-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a><span data-ttu-id="79602-130">Lancement Microsoft Edge à partir de l’extension</span><span class="sxs-lookup"><span data-stu-id="79602-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="79602-131">Accédez à Microsoft Edge outils dans la **barre d’activité.**</span><span class="sxs-lookup"><span data-stu-id="79602-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="79602-132">À côté de **l’Microsoft Edge Outils** : Cibles, il existe un signe plus qui ouvre le navigateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="79602-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="79602-133">Si vous choisissez l’option **about:blank,** vous devez accéder à votre application web dans le navigateur pour qu’elle apparaisse dans le panneau **Éléments** dans Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="79602-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <a name="launching-microsoft-edge-from-the-debug-view"></a><span data-ttu-id="79602-134">Lancement Microsoft Edge à partir de la vue Débogage</span><span class="sxs-lookup"><span data-stu-id="79602-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="79602-135">Si vous avez l’habitude d’utiliser la vue Débogage dans Visual Studio Code, accédez à Microsoft Edge devTools à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="79602-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="79602-136">Dans Visual Studio Code, accédez à l’affichage Débogage</span><span class="sxs-lookup"><span data-stu-id="79602-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="79602-137">Sélectionnez `Ctrl` + `Shift` + `D` sur Windows/Linux \( `Command` + `Shift` + `D` sur macOS\).</span><span class="sxs-lookup"><span data-stu-id="79602-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="79602-138">Si vous n’avez aucune configuration dans Visual Studio Code, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="79602-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="79602-139">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="79602-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="79602-140">Choisissez le **bouton Lire** \(vert\).</span><span class="sxs-lookup"><span data-stu-id="79602-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="79602-141">Dans ladown, choisissez **Edge** dans la dropdown.</span><span class="sxs-lookup"><span data-stu-id="79602-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="79602-142">Un fichier qui contient la configuration suivante doit `launch.json` être affiché.</span><span class="sxs-lookup"><span data-stu-id="79602-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
>     
>     ```json
>     {
>       "version": "0.2.0",
>       "configurations": [
>         {
>           "name": "Launch Microsoft Edge and open the Edge DevTools",
>           "request": "launch",
>           "type": "vscode-edge-devtools.debug",
>           "url": "http://localhost:8080"
>         }
>       ]
>     }
>     ```  
>     
> <span data-ttu-id="79602-143">Une fois que vous avez chargé la configuration correcte, terminez l’action suivante.</span><span class="sxs-lookup"><span data-stu-id="79602-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="79602-144">Pour lancer l’outil **Éléments** à Visual Studio Code, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="79602-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="79602-145">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="79602-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="79602-146">Choisissez le **bouton Lire** \(vert\).</span><span class="sxs-lookup"><span data-stu-id="79602-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="79602-147">Vous pouvez maintenant faire les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="79602-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="79602-148">Accédez à une capture vidéo de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="79602-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="79602-149">Inspectez le DOM et le style des composants sur votre page.</span><span class="sxs-lookup"><span data-stu-id="79602-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="79602-150">Attachement à un Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="79602-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="79602-151">Pour ouvrir un navigateur et attacher l’instance à Visual Studio Code, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="79602-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="79602-152">Pour ouvrir une instance de Microsoft Edge \(Chromium\), copiez et exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="79602-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="79602-153">Après le lancement de l’instance, copiez et collez l’extrait de code suivant dans votre `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="79602-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
    ```json
    {
        "type": "vscode-edge-devtools.debug",
        "request": "attach",
        "name": "Attach to Microsoft Edge and open the developer tools",
        "url": "http://localhost:3000/",
        "webRoot": "${workspaceFolder}/out",
        "port": 9222
    }
    ```  
    
1.  <span data-ttu-id="79602-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span><span class="sxs-lookup"><span data-stu-id="79602-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="79602-155">Pour lancer l’outil **Éléments** à Visual Studio Code, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="79602-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="79602-156">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="79602-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="79602-157">Choisissez le **bouton Lire** \(vert\).</span><span class="sxs-lookup"><span data-stu-id="79602-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="79602-158">Vous pouvez maintenant faire les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="79602-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="79602-159">Accédez à une capture vidéo de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="79602-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="79602-160">Inspectez le DOM et le style des composants sur votre page.</span><span class="sxs-lookup"><span data-stu-id="79602-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a><span data-ttu-id="79602-161">Contacter l’équipe Microsoft Edge devTools pour Visual Studio Code extension</span><span class="sxs-lookup"><span data-stu-id="79602-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="79602-162">Envoyez vos commentaires en [classant un problème][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] par rapport [au GitHub de][GithubMicrosoftVscodeEdgeDevtools] l’extension.</span><span class="sxs-lookup"><span data-stu-id="79602-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="79602-163">Si vous souhaitez vous aider à effectuer</span><span class="sxs-lookup"><span data-stu-id="79602-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="79602-164">Cette extension est préférable, vos contributions sont les bienvenues.</span><span class="sxs-lookup"><span data-stu-id="79602-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="79602-165">Recherchez tout ce dont vous avez besoin pour commencer [dans le GitHub de][GithubMicrosoftVscodeEdgeDevtools] l’extension.</span><span class="sxs-lookup"><span data-stu-id="79602-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nouveau problème : microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Microsoft Edge Outils pour Visual Studio Code"  
