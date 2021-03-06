---
description: Utilisation des éléments pour Microsoft Edge (Chromium) à partir de Visual Studio Code
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
# <a name="microsoft-edge-devtools-for-visual-studio-code-extension"></a><span data-ttu-id="b7a26-104">Microsoft Edge DevTools pour l’extension Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="b7a26-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="b7a26-105">Utiliser</span><span class="sxs-lookup"><span data-stu-id="b7a26-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="b7a26-106">cette extension permet d’accéder dans Microsoft Edge DevTools à l’intérieur [de Microsoft Visual Studio Code][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="b7a26-106">this extension to access in Microsoft Edge DevTools inside [Microsoft Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="b7a26-107">Vous avez accès aux outils **d’éléments** **et** réseau dans Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b7a26-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="b7a26-108">Vous pouvez lancer ou attacher une instance de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b7a26-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="b7a26-109">Une fois connecté, vous pouvez afficher la structure HTML d’runtime, modifier la disposition, résoudre les problèmes de style et inspecter le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="b7a26-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <a name="elements-tool"></a><span data-ttu-id="b7a26-110">Outil Éléments</span><span class="sxs-lookup"><span data-stu-id="b7a26-110">Elements tool</span></span>  

<span data-ttu-id="b7a26-111">Par défaut, l’extension lance une instance de navigateur dans une fenêtre unique et vous offre la fonctionnalité **Éléments** de Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b7a26-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools pour Visual Studio code s’exécutant avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="b7a26-113">Microsoft Edge DevTools pour Visual Studio code s’exécutant avec une fenêtre de navigateur complète</span><span class="sxs-lookup"><span data-stu-id="b7a26-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="b7a26-114">Dans les paramètres d’extension, vous pouvez activer davantage de fonctionnalités telles que le **mode sans** tête et le **réseau.**</span><span class="sxs-lookup"><span data-stu-id="b7a26-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Activation (ou désactivation) du mode sans tête et de l’inspection du réseau dans les paramètres d’extension" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="b7a26-116">Activation du mode sans tête \(ou désactivation\) et inspection du réseau dans les paramètres d’extension</span><span class="sxs-lookup"><span data-stu-id="b7a26-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <a name="headless-mode"></a><span data-ttu-id="b7a26-117">Mode sans tête</span><span class="sxs-lookup"><span data-stu-id="b7a26-117">Headless Mode</span></span>  

<span data-ttu-id="b7a26-118">En mode sans en-tête, cette extension ne lance pas une instance de navigateur complète pour le débogage.</span><span class="sxs-lookup"><span data-stu-id="b7a26-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="b7a26-119">Il exécute une instance en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="b7a26-119">It runs an instance in the background.</span></span>  <span data-ttu-id="b7a26-120">Vous de devez peut-être rester à l’intérieur de l’éditeur et interagir avec le navigateur incorporé.</span><span class="sxs-lookup"><span data-stu-id="b7a26-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="b7a26-121">Une icône de navigateur supplémentaire ne s’affiche pas dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="b7a26-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools pour Visual Studio code s’exécutant sans en-tête" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="b7a26-123">Microsoft Edge DevTools pour Visual Studio code s’exécutant avec un navigateur sans en-tête</span><span class="sxs-lookup"><span data-stu-id="b7a26-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="b7a26-124">Sur macOS, vous devez activer le mode sans tête comme mode préféré.</span><span class="sxs-lookup"><span data-stu-id="b7a26-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="b7a26-125">L’utilisation du mode sans en-tête doit résoudre un problème dans lequel, si la fenêtre n’est pas visible, la fenêtre du navigateur signale qu’elle `Not Active` l’est.</span><span class="sxs-lookup"><span data-stu-id="b7a26-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <a name="network-tool"></a><span data-ttu-id="b7a26-126">Outil réseau</span><span class="sxs-lookup"><span data-stu-id="b7a26-126">Network tool</span></span>  

<span data-ttu-id="b7a26-127">Si vous souhaitez également inspecter le trafic réseau de votre application, ouvrez les paramètres et allumez **l’onglet** Réseau.</span><span class="sxs-lookup"><span data-stu-id="b7a26-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspection du réseau dans Microsoft Edge DevTools pour le Visual Studio code" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="b7a26-129">Inspection du réseau dans Microsoft Edge DevTools pour le Visual Studio code</span><span class="sxs-lookup"><span data-stu-id="b7a26-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <a name="launching-microsoft-edge-from-the-extension"></a><span data-ttu-id="b7a26-130">Lancement de Microsoft Edge à partir de l’extension</span><span class="sxs-lookup"><span data-stu-id="b7a26-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="b7a26-131">Accédez aux outils Microsoft Edge dans la **barre d’activité.**</span><span class="sxs-lookup"><span data-stu-id="b7a26-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="b7a26-132">En plus de l’endroit où il est indiqué **Outils Microsoft Edge** : Cibles, il existe un signe plus qui ouvre le navigateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="b7a26-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="b7a26-133">Si vous choisissez l’option **about:blank,** vous devez accéder à votre \*\*\*\* application web dans le navigateur pour qu’elle apparaisse dans le panneau Éléments dans Visual Studio Code.</span><span class="sxs-lookup"><span data-stu-id="b7a26-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <a name="launching-microsoft-edge-from-the-debug-view"></a><span data-ttu-id="b7a26-134">Lancement de Microsoft Edge à partir de l’affichage Débogage</span><span class="sxs-lookup"><span data-stu-id="b7a26-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="b7a26-135">Si vous êtes habitué à utiliser l’affichage Débogage dans Visual Studio Code, accédez à Microsoft Edge DevTools à partir de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="b7a26-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="b7a26-136">Dans Visual Studio code, accédez à l’affichage Débogage</span><span class="sxs-lookup"><span data-stu-id="b7a26-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="b7a26-137">Sélectionnez `Ctrl` + `Shift` + `D` sur Windows/Linux \( `Command` + `Shift` + `D` sur macOS\).</span><span class="sxs-lookup"><span data-stu-id="b7a26-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="b7a26-138">Si vous n’avez aucune configuration dans Visual Studio Code, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7a26-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="b7a26-139">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="b7a26-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="b7a26-140">Choisissez le **bouton Lire** \(vert\).</span><span class="sxs-lookup"><span data-stu-id="b7a26-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="b7a26-141">Dans ladown, choisissez **Edge** dans la dropdown.</span><span class="sxs-lookup"><span data-stu-id="b7a26-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="b7a26-142">Un fichier qui contient la configuration suivante doit `launch.json` être affiché.</span><span class="sxs-lookup"><span data-stu-id="b7a26-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
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
> <span data-ttu-id="b7a26-143">Une fois que vous avez chargé la configuration correcte, terminez l’action suivante.</span><span class="sxs-lookup"><span data-stu-id="b7a26-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="b7a26-144">Pour lancer **l’outil Éléments** à Visual Studio Code, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7a26-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="b7a26-145">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="b7a26-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="b7a26-146">Choisissez le **bouton Lire** \(vert\).</span><span class="sxs-lookup"><span data-stu-id="b7a26-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="b7a26-147">Vous pouvez maintenant faire les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7a26-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="b7a26-148">Accédez à une capture vidéo de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="b7a26-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="b7a26-149">Inspectez le DOM et le style des composants sur votre page.</span><span class="sxs-lookup"><span data-stu-id="b7a26-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <a name="attaching-to-microsoft-edge"></a><span data-ttu-id="b7a26-150">Attachement à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b7a26-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="b7a26-151">Pour ouvrir un navigateur et attacher l’instance à Visual Studio Code, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7a26-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="b7a26-152">Pour ouvrir une instance de Microsoft Edge \(Chromium\), copiez et exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="b7a26-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="b7a26-153">Après le lancement de l’instance, copiez et collez l’extrait de code suivant dans votre `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="b7a26-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
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
    
1.  <span data-ttu-id="b7a26-154">Dans Visual Studio Code, ouvrez \*\*\*\* le menu déroulant Débogger, choisissez Attacher à **Microsoft Edge et ouvrez les outils de développement.**</span><span class="sxs-lookup"><span data-stu-id="b7a26-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="b7a26-155">Pour lancer **l’outil Éléments** à Visual Studio Code, effectuer l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7a26-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="b7a26-156">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="b7a26-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="b7a26-157">Choisissez le **bouton Lire** \(vert\).</span><span class="sxs-lookup"><span data-stu-id="b7a26-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="b7a26-158">Vous pouvez maintenant faire les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7a26-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="b7a26-159">Accédez à une capture vidéo de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="b7a26-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="b7a26-160">Inspectez le DOM et le style des composants sur votre page.</span><span class="sxs-lookup"><span data-stu-id="b7a26-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-for-visual-studio-code-extension-team"></a><span data-ttu-id="b7a26-161">Mise en contact avec Microsoft Edge DevTools pour l Visual Studio d’extension de code</span><span class="sxs-lookup"><span data-stu-id="b7a26-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="b7a26-162">Envoyez vos commentaires en [classant un problème][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] par rapport au [référentiel GitHub][GithubMicrosoftVscodeEdgeDevtools] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="b7a26-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="b7a26-163">Si vous souhaitez vous aider à effectuer</span><span class="sxs-lookup"><span data-stu-id="b7a26-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="b7a26-164">Cette extension est préférable, vos contributions sont les bienvenues.</span><span class="sxs-lookup"><span data-stu-id="b7a26-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="b7a26-165">Recherchez tout ce dont vous avez besoin pour commencer dans le référentiel [GitHub][GithubMicrosoftVscodeEdgeDevtools] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="b7a26-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Visual Studio Code"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Visual Studio Code"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "microsoft/vscode-edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nouveau problème : microsoft/vscode-edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour Visual Studio code"  
