---
description: Utiliser des éléments pour Microsoft Edge (chrome) à partir de code Visual Studio
title: Éléments de Microsoft Edge (chrome) issus du code Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, code vs, code Visual Studio, éléments
ms.openlocfilehash: 81488c08a76a16b80a415cbd17cd0617df916f54
ms.sourcegitcommit: 1cfcf2c8970a6c2221cfbf09a23d36b08bd60690
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2020
ms.locfileid: "11135484"
---
# <span data-ttu-id="f6928-104">Extension de code Microsoft Edge DevTools pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f6928-104">Microsoft Edge DevTools for Visual Studio Code extension</span></span>  

<span data-ttu-id="f6928-105">Utiliser</span><span class="sxs-lookup"><span data-stu-id="f6928-105">Use</span></span> <!--the [Microsoft Edge DevTools for Visual Studio Code][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] --><span data-ttu-id="f6928-106">pour accéder à cette extension dans Microsoft Edge DevTools dans le [code Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="f6928-106">this extension to access in Microsoft Edge DevTools inside [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="f6928-107">Vous avez accès aux **éléments** et aux outils **réseau** dans Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="f6928-107">You have access to the **Elements** and **Network** tools in Microsoft Edge DevTools.</span></span>  <span data-ttu-id="f6928-108">Vous pouvez lancer une instance de Microsoft Edge ou l’attacher à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="f6928-108">You may either launch or attach to an instance of Microsoft Edge.</span></span>  <span data-ttu-id="f6928-109">Après vous être connecté, vous pouvez afficher la structure HTML d’exécution, modifier la disposition, résoudre les problèmes de style et inspecter le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="f6928-109">After you connect you may display the runtime HTML structure, alter the layout, fix styling issues, and inspect network traffic.</span></span>  

## <span data-ttu-id="f6928-110">Outil éléments</span><span class="sxs-lookup"><span data-stu-id="f6928-110">Elements tool</span></span>  

<span data-ttu-id="f6928-111">Par défaut, l’extension lance une instance de navigateur dans une fenêtre unique et vous donne les fonctionnalités d' **éléments** de Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="f6928-111">By default, the extension launches a browser instance in a unique window and gives you the **Elements** functionality of Microsoft Edge DevTools.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-windowed.png" alt-text="Microsoft Edge DevTools pour le code Visual Studio exécuté avec une fenêtre de navigateur complète" lightbox="./media/edge-devtools-for-vscode-windowed.png":::
   <span data-ttu-id="f6928-113">Microsoft Edge DevTools pour le code Visual Studio exécuté avec une fenêtre de navigateur complète</span><span class="sxs-lookup"><span data-stu-id="f6928-113">Microsoft Edge DevTools for Visual Studio Code running with a full browser window</span></span>  
:::image-end:::  

<span data-ttu-id="f6928-114">Dans les paramètres de l’extension, vous pouvez activer davantage de fonctionnalités telles que le **mode** sans affichage et le **réseau**.</span><span class="sxs-lookup"><span data-stu-id="f6928-114">In the extension settings, you may enable more functionality like **Headless Mode** and **Network**.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-settings.png" alt-text="Activer (ou désactiver) le mode Headless et l’inspection réseau dans les paramètres d’extension" lightbox="./media/edge-devtools-for-vscode-settings.png":::
   <span data-ttu-id="f6928-116">Activation du mode sans affichage et de l’inspection du réseau dans les paramètres d’extension</span><span class="sxs-lookup"><span data-stu-id="f6928-116">Enabling \(or disabling\) headless mode and Network inspection in the extension settings</span></span>  
:::image-end:::  

## <span data-ttu-id="f6928-117">Mode headless</span><span class="sxs-lookup"><span data-stu-id="f6928-117">Headless Mode</span></span>  

<span data-ttu-id="f6928-118">En mode Headless, cette extension ne lance pas une instance de navigateur complète à déboguer.</span><span class="sxs-lookup"><span data-stu-id="f6928-118">In headless mode, this extension does not launch a full browser instance to debug.</span></span>  <span data-ttu-id="f6928-119">Il exécute une instance en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="f6928-119">It runs an instance in the background.</span></span>  <span data-ttu-id="f6928-120">Il est possible que vous deviez rester à l’intérieur de l’éditeur et interagir avec le navigateur intégré.</span><span class="sxs-lookup"><span data-stu-id="f6928-120">You may have to stay inside the editor and interact with the embedded browser.</span></span>  <span data-ttu-id="f6928-121">Une icône de navigateur supplémentaire ne s’affiche pas dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="f6928-121">An extra browser icon is not be displayed in your task bar.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-headless.png" alt-text="Microsoft Edge DevTools pour le code Visual Studio exécuté avec un service headless" lightbox="./media/edge-devtools-for-vscode-headless.png":::
   <span data-ttu-id="f6928-123">Microsoft Edge DevTools pour le code Visual Studio exécuté à l’aide d’un navigateur headless</span><span class="sxs-lookup"><span data-stu-id="f6928-123">Microsoft Edge DevTools for Visual Studio Code running with a headless browser</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="f6928-124">Sur macOS, vous devez activer le mode headless comme mode préféré.</span><span class="sxs-lookup"><span data-stu-id="f6928-124">On macOS, you should turn on headless mode as your preferred mode.</span></span>  <span data-ttu-id="f6928-125">L’utilisation du mode headless doit résoudre un problème à l’endroit où, si la fenêtre n’est pas visible, la fenêtre du navigateur indique son état `Not Active` .</span><span class="sxs-lookup"><span data-stu-id="f6928-125">Using headless mode should solve an issue where, if the window is not visible, the browser window reports that it is `Not Active`.</span></span>  

## <span data-ttu-id="f6928-126">Outil réseau</span><span class="sxs-lookup"><span data-stu-id="f6928-126">Network tool</span></span>  

<span data-ttu-id="f6928-127">Si vous voulez également examiner le trafic réseau de votre application, vous pouvez ouvrir les paramètres et activer l’onglet **réseau** .</span><span class="sxs-lookup"><span data-stu-id="f6928-127">If you also want to inspect the network traffic of your application, open the settings and turn on the **Network** tab.</span></span>  

:::image type="complex" source="./media/edge-devtools-for-vscode-network.png" alt-text="Inspection du réseau dans Microsoft Edge DevTools pour le code Visual Studio" lightbox="./media/edge-devtools-for-vscode-network.png":::
    <span data-ttu-id="f6928-129">Inspection du réseau dans Microsoft Edge DevTools pour le code Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f6928-129">Network inspection in Microsoft Edge DevTools for Visual Studio Code</span></span>  
:::image-end:::  

## <span data-ttu-id="f6928-130">Lancement de Microsoft Edge à partir de l’extension</span><span class="sxs-lookup"><span data-stu-id="f6928-130">Launching Microsoft Edge From the extension</span></span>  

<span data-ttu-id="f6928-131">Accédez à outils Microsoft Edge dans la **barre d’activité**.</span><span class="sxs-lookup"><span data-stu-id="f6928-131">Navigate to Microsoft Edge Tools in the **Activity Bar**.</span></span>  <span data-ttu-id="f6928-132">À côté de l’emplacement du message « **outils Microsoft Edge: cibles»,** il existe un signe plus qui ouvre le navigateur de votre application.</span><span class="sxs-lookup"><span data-stu-id="f6928-132">Next to where it says **Microsoft Edge Tools: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="f6928-133">Si vous choisissez l’option **à propos** de, vous devez accéder à votre application Web dans le navigateur pour qu’elle apparaisse dans le panneau **éléments** du code Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f6928-133">If you choose the **about:blank** option, you must navigate to your web app in the browser for it to appear in the **Elements** panel in Visual Studio Code.</span></span>  

## <span data-ttu-id="f6928-134">Lancement de Microsoft Edge à partir de la vue de débogage</span><span class="sxs-lookup"><span data-stu-id="f6928-134">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="f6928-135">Si vous avez l’habitude d’utiliser le mode débogage dans le code Visual Studio, accédez à DevTools Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f6928-135">If you are accustomed to using the Debug view in Visual Studio Code, access Microsoft Edge DevTools from it.</span></span>  

1.  <span data-ttu-id="f6928-136">Dans le code Visual Studio, accédez à la vue de débogage.</span><span class="sxs-lookup"><span data-stu-id="f6928-136">In Visual Studio Code, navigate to the Debug view</span></span> 
    *   <span data-ttu-id="f6928-137">Sélectionnez `Ctrl` + `Shift` + `D` Windows/Linux \ ( `Command` + `Shift` + `D` sur MacOS \).</span><span class="sxs-lookup"><span data-stu-id="f6928-137">Select `Ctrl`+`Shift`+`D` on Windows/Linux  \(`Command`+`Shift`+`D` on macOS\).</span></span>  

<!--TODO:  Is this section intended to be optional  -->  
> [!NOTE]
> 1.  <span data-ttu-id="f6928-138">Si vous n’avez pas de configurations dans le code Visual Studio, effectuez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6928-138">If you do not have any configurations in Visual Studio Code, complete one of the following actions.</span></span>  
>     *   <span data-ttu-id="f6928-139">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="f6928-139">Select `F5`.</span></span>  
>     *   <span data-ttu-id="f6928-140">Cliquez sur le bouton **lire** \ (Green \).</span><span class="sxs-lookup"><span data-stu-id="f6928-140">Choose the **Play** \(green\) button.</span></span>  
> 1.  <span data-ttu-id="f6928-141">Dans la liste déroulante, sélectionnez **Edge** dans la liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="f6928-141">In the dropdown, choose **Edge** in the dropdown.</span></span>  
> 1.  <span data-ttu-id="f6928-142">Un `launch.json` fichier doit être affiché pour contenir la configuration suivante.</span><span class="sxs-lookup"><span data-stu-id="f6928-142">A `launch.json` file should be displayed that contains the following configuration.</span></span>  
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
> <span data-ttu-id="f6928-143">Une fois la configuration correcte chargée, effectuez l’opération suivante.</span><span class="sxs-lookup"><span data-stu-id="f6928-143">After you load the correct configuration, complete the following action.</span></span>  

1.  <span data-ttu-id="f6928-144">Pour lancer l’outil **éléments** à partir du code Visual Studio, effectuez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6928-144">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="f6928-145">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="f6928-145">Select `F5`.</span></span>  
    *   <span data-ttu-id="f6928-146">Cliquez sur le bouton **lire** \ (Green \).</span><span class="sxs-lookup"><span data-stu-id="f6928-146">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="f6928-147">À présent, vous pouvez effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6928-147">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="f6928-148">Accédez à la vidéo de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="f6928-148">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="f6928-149">Inspectez le DOM et le style des composants de votre page.</span><span class="sxs-lookup"><span data-stu-id="f6928-149">Inspect the DOM and the styling of the components on your page.</span></span>  

## <span data-ttu-id="f6928-150">Joindre à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f6928-150">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="f6928-151">Pour ouvrir un navigateur et joindre l’instance au code Visual Studio, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="f6928-151">To open a browser and attach the instance to Visual Studio Code, complete the following steps.</span></span> 

1.  <span data-ttu-id="f6928-152">Pour ouvrir une instance de Microsoft Edge \ (chrome \), copiez et exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="f6928-152">To open an instance of Microsoft Edge \(Chromium\), copy and run the following command.</span></span>  
    
    ```shell
    start msedge --remote-debugging-port=9222
    ```  
    
1.  <span data-ttu-id="f6928-153">Après le lancement de l’instance, copiez et collez l’extrait de code suivant dans votre `launch.json` fichier.</span><span class="sxs-lookup"><span data-stu-id="f6928-153">After the instance launches, copy and paste the following code snippet into your `launch.json` file.</span></span>  
    
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
    
1.  <span data-ttu-id="f6928-154">Dans le code Visual Studio, ouvrez le menu déroulant **débogueur** et sélectionnez **joindre à Microsoft Edge, puis ouvrez les outils de développement**.</span><span class="sxs-lookup"><span data-stu-id="f6928-154">In Visual Studio Code, open the **Debugger** drop-down menu and choose **Attach to Microsoft Edge and open the developer tools**.</span></span>  
1.  <span data-ttu-id="f6928-155">Pour lancer l’outil **éléments** à partir du code Visual Studio, effectuez l’une des actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6928-155">To launch the **Elements** tool from Visual Studio Code, complete one of the following actions.</span></span> 
    *   <span data-ttu-id="f6928-156">Sélectionnez `F5` .</span><span class="sxs-lookup"><span data-stu-id="f6928-156">Select `F5`.</span></span>  
    *   <span data-ttu-id="f6928-157">Cliquez sur le bouton **lire** \ (Green \).</span><span class="sxs-lookup"><span data-stu-id="f6928-157">Choose the **Play** \(green\) button.</span></span>  
         
<span data-ttu-id="f6928-158">À présent, vous pouvez effectuer les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="f6928-158">Now, you may do the following actions.</span></span>  

*   <span data-ttu-id="f6928-159">Accédez à la vidéo de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="f6928-159">Access a screencast of your browser.</span></span>  
*   <span data-ttu-id="f6928-160">Inspectez le DOM et le style des composants de votre page.</span><span class="sxs-lookup"><span data-stu-id="f6928-160">Inspect the DOM and the styling of the components on your page.</span></span>  
    
## <span data-ttu-id="f6928-161">Contacter l’équipe de l’extension de code Microsoft Edge DevTools pour Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f6928-161">Getting in touch with the Microsoft Edge DevTools for Visual Studio Code extension team</span></span>  

<span data-ttu-id="f6928-162">Envoyez vos commentaires en envoyant [un problème][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] à l’aide de la [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="f6928-162">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="f6928-163">Si vous voulez apporter des informations</span><span class="sxs-lookup"><span data-stu-id="f6928-163">If you want to help make</span></span> <!--the Microsoft Edge DevTools for Visual Studio Code --><span data-ttu-id="f6928-164">C’est encore plus de plus de plaisirs.</span><span class="sxs-lookup"><span data-stu-id="f6928-164">this extension better, your contributions are welcome.</span></span>  <span data-ttu-id="f6928-165">Trouvez tout ce dont vous avez besoin pour commencer à utiliser le [GitHub référentiel Samples][GithubMicrosoftVscodeEdgeDevtools] de l’extension.</span><span class="sxs-lookup"><span data-stu-id="f6928-165">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!--links -->  

[VisualstudioCode]: https://code.visualstudio.com "Code Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Documentation | Code Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Nouveau problème-Microsoft/vscode-Edge-devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Outils Microsoft Edge pour le code VS"  
