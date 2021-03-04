---
description: Microsoft Edge (Chromium) et Visual Studio
title: Visual Studio
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/18/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools, vs, visual studio, débogueur
ms.openlocfilehash: 562952ef238c05922e468501706ab75e1976273d
ms.sourcegitcommit: 661e8def3f27cea381c59ac38954789e736c18f4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/04/2021
ms.locfileid: "11387273"
---
# <a name="visual-studio"></a><span data-ttu-id="e3c90-104">Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-104">Visual Studio</span></span>  

<span data-ttu-id="e3c90-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] est un environnement de développement intégré \(IDE\).</span><span class="sxs-lookup"><span data-stu-id="e3c90-105">Microsoft [Visual Studio][MicrosoftVisualstudioVs] is an integrated development environment \(IDE\).</span></span>   <span data-ttu-id="e3c90-106">Utilisez-le pour modifier, déboguer, créer et publier vos applications web.</span><span class="sxs-lookup"><span data-stu-id="e3c90-106">Use it to edit, debug, build, and publish your web apps.</span></span>  <span data-ttu-id="e3c90-107">Il s’agit d’un programme riche en fonctionnalités qui peut être utilisé pour de nombreux aspects de votre développement web.</span><span class="sxs-lookup"><span data-stu-id="e3c90-107">It is a feature-rich program that may be used for many aspects of your web development.</span></span>  <span data-ttu-id="e3c90-108">Au-delà de l’éditeur et du débogger standard fournis par la plupart des ID, Visual Studio inclut les fonctionnalités suivantes pour faciliter votre processus de développement.</span><span class="sxs-lookup"><span data-stu-id="e3c90-108">Over and above the standard editor and debugger that most IDEs provide, Visual Studio includes the following features to ease your development process.</span></span>  

*   <span data-ttu-id="e3c90-109">compilateurs</span><span class="sxs-lookup"><span data-stu-id="e3c90-109">compilers</span></span>  
*   <span data-ttu-id="e3c90-110">outils d’achèvement du code</span><span class="sxs-lookup"><span data-stu-id="e3c90-110">code completion tools</span></span>  
*   <span data-ttu-id="e3c90-111">concepteurs graphiques</span><span class="sxs-lookup"><span data-stu-id="e3c90-111">graphical designers</span></span>  
*   <span data-ttu-id="e3c90-112">beaucoup plus</span><span class="sxs-lookup"><span data-stu-id="e3c90-112">many more</span></span>  
    
<span data-ttu-id="e3c90-113">Si vous n’utilisez pas déjà Visual Studio, accédez à Télécharger [Visual Studio][MicrosoftVisualstudioDownloads] télécharger.</span><span class="sxs-lookup"><span data-stu-id="e3c90-113">If you are not already using Visual Studio, navigate to [Download Visual Studio][MicrosoftVisualstudioDownloads] to download it.</span></span>  

<span data-ttu-id="e3c90-114">Actuellement, Visual Studio 2019 prend en charge le débogage de JavaScript dans Microsoft Edge pour ASP.NET Framework et ASP.NET applications principales.</span><span class="sxs-lookup"><span data-stu-id="e3c90-114">Currently, Visual Studio 2019 supports debugging JavaScript in Microsoft Edge for your ASP.NET Framework and ASP.NET Core apps.</span></span>  <span data-ttu-id="e3c90-115">Pour utiliser les Visual Studio déboguer Microsoft Edge, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="e3c90-115">Complete the following steps to use Visual Studio to debug Microsoft Edge.</span></span>  

## <a name="launch-microsoft-edge"></a><span data-ttu-id="e3c90-116">Lancer Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e3c90-116">Launch Microsoft Edge</span></span>  

<span data-ttu-id="e3c90-117">Visual Studio le flux de travail suivant à l’aide d’un seul bouton.</span><span class="sxs-lookup"><span data-stu-id="e3c90-117">Visual Studio completes the following workflow using a single button.</span></span>  

1.  <span data-ttu-id="e3c90-118">Crée votre application ASP.NET et ASP.NET core.</span><span class="sxs-lookup"><span data-stu-id="e3c90-118">Builds your ASP.NET and ASP.NET Core app.</span></span>  
1.  <span data-ttu-id="e3c90-119">Démarre votre serveur web.</span><span class="sxs-lookup"><span data-stu-id="e3c90-119">Starts your web server.</span></span>  
1.  <span data-ttu-id="e3c90-120">Lance Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e3c90-120">Launches Microsoft Edge.</span></span>  
1.  <span data-ttu-id="e3c90-121">Connecte le Visual Studio débogger.</span><span class="sxs-lookup"><span data-stu-id="e3c90-121">Connects the Visual Studio debugger.</span></span>  
    
<span data-ttu-id="e3c90-122">Le flux de travail simplifié vous permet de déboguer JavaScript qui s’exécute dans Microsoft Edge directement à partir de votre IDE.</span><span class="sxs-lookup"><span data-stu-id="e3c90-122">The simplified workflow allows you to debug JavaScript that run in Microsoft Edge directly from your IDE.</span></span>  

### <a name="create-a-new-aspnet-core-web-app"></a><span data-ttu-id="e3c90-123">Créer une application web ASP.NET core</span><span class="sxs-lookup"><span data-stu-id="e3c90-123">Create a new ASP.NET Core web app</span></span>  

<span data-ttu-id="e3c90-124">Ouvrez Visual Studio 2019 et choisissez **Créer un projet.**</span><span class="sxs-lookup"><span data-stu-id="e3c90-124">Open Visual Studio 2019 and choose **Create a new project**.</span></span>  <span data-ttu-id="e3c90-125">On the next screen, choose **ASP.NET Core Web app**  >  **Next**.</span><span class="sxs-lookup"><span data-stu-id="e3c90-125">On the next screen, choose **ASP.NET Core Web app** > **Next**.</span></span>  

:::image type="complex" source="./media/create-new-project.png" alt-text="Créer une application web ASP.NET core" lightbox="./media/create-new-project.png":::
   <span data-ttu-id="e3c90-127">Créer une application web ASP.NET core</span><span class="sxs-lookup"><span data-stu-id="e3c90-127">Create a new ASP.NET Core Web app</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-128">Fournissez **un nom de** projet pour votre nouveau projet et choisissez **Créer.**</span><span class="sxs-lookup"><span data-stu-id="e3c90-128">Provide a **Project name** for your new project and choose **Create**.</span></span>  <span data-ttu-id="e3c90-129">Pour les besoins de l’exemple, \*\* choisissezReact.js\*\* en tant que modèle, puis choisissez **Créer**.</span><span class="sxs-lookup"><span data-stu-id="e3c90-129">For the purposes of the example, choose **React.js** as the template, and choose **Create**.</span></span>  <span data-ttu-id="e3c90-130">Le **React.js** indique comment intégrer des React.js à une application ASP.NET Core.</span><span class="sxs-lookup"><span data-stu-id="e3c90-130">The **React.js** template specifies how to integrate React.js with an ASP.NET Core app.</span></span>  

### <a name="launch-microsoft-edge-from-visual-studio"></a><span data-ttu-id="e3c90-131">Lancer Microsoft Edge à partir de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-131">Launch Microsoft Edge from Visual Studio</span></span>  

<span data-ttu-id="e3c90-132">Après avoir créé votre projet, ouvrez `ClientApp/src/components/Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="e3c90-132">After you create your project, open `ClientApp/src/components/Counter.js`.</span></span>  <span data-ttu-id="e3c90-133">À présent, pour utiliser Visual Studio pour déboguer JavaScript, choisissez la zone de description en face du bouton **vert Lire** et **d’IIS Express**.</span><span class="sxs-lookup"><span data-stu-id="e3c90-133">Now, to use Visual Studio to debug JavaScript, choose the dropdown next to the green **Play** button and **IIS Express**.</span></span>  

:::image type="complex" source="./media/vs-dropdown.png" alt-text="La zone de détail en face du bouton vert Lire et d’IIS Express" lightbox="./media/vs-dropdown.png":::
   <span data-ttu-id="e3c90-135">La zone de détail en face du bouton **vert Lire** et **d’IIS Express**</span><span class="sxs-lookup"><span data-stu-id="e3c90-135">The dropdown next to the green **Play** button and **IIS Express**</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-136">Choose **Script Debugging**  >  **Enabled**.</span><span class="sxs-lookup"><span data-stu-id="e3c90-136">Choose **Script Debugging** > **Enabled**.</span></span>  

:::image type="complex" source="./media/enable-script-debugging.png" alt-text="Activer le débogage de script dans Visual Studio" lightbox="./media/enable-script-debugging.png":::
   <span data-ttu-id="e3c90-138">Activer le débogage de script dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-138">Turn on script debugging in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-139">Dans la même dropdown, choisissez navigateur **web** > le canal d’aperçu de Microsoft Edge que vous souhaitez que Visual Studio lance, tel que Microsoft Edge Canary, Dev ou Beta.</span><span class="sxs-lookup"><span data-stu-id="e3c90-139">In the same dropdown, choose **Web Browser** > the preview channel of Microsoft Edge that you want Visual Studio to launch, such as Microsoft Edge Canary, Dev, or Beta.</span></span>  <span data-ttu-id="e3c90-140">Si vous n’utilisez pas déjà l’un des canaux d’aperçu Microsoft Edge, accédez à Télécharger les canaux [Insider de Microsoft Edge][MicrosoftedgeinsiderDownload] pour en télécharger un.</span><span class="sxs-lookup"><span data-stu-id="e3c90-140">If you are not already using one of the Microsoft Edge preview channels, navigate to [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload] to download one.</span></span>  

:::image type="complex" source="./media/set-web-browser.png" alt-text="Choisissez le canal d’aperçu de Microsoft Edge que vous Visual Studio lancer" lightbox="./media/set-web-browser.png":::
   <span data-ttu-id="e3c90-142">Choisissez le canal d’aperçu de Microsoft Edge que vous Visual Studio lancer</span><span class="sxs-lookup"><span data-stu-id="e3c90-142">Choose the preview channel of Microsoft Edge that you want Visual Studio to launch</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e3c90-143">Si vous choisissez Microsoft Edge \(EdgeHTML\), Visual Studio le lance au lieu de Microsoft Edge \(Chromium\).</span><span class="sxs-lookup"><span data-stu-id="e3c90-143">If you choose Microsoft Edge \(EdgeHTML\), Visual Studio launches it instead of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="e3c90-144">Installez l’un des canaux d’aperçu de [Microsoft Edge][MicrosoftedgeinsiderDownload] ou assurez-vous que la version de Microsoft Edge installée sur votre ordinateur est Microsoft Edge \(Chromium\) et non Microsoft Edge \(EdgeHTML\).</span><span class="sxs-lookup"><span data-stu-id="e3c90-144">[Install the one of the preview channels of Microsoft Edge][MicrosoftedgeinsiderDownload] or ensure that the version of Microsoft Edge installed on your machine is Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  

<span data-ttu-id="e3c90-145">Maintenant que Visual Studio est correctement configuré, choisissez le bouton **Vert** Lire.</span><span class="sxs-lookup"><span data-stu-id="e3c90-145">Now that Visual Studio is correctly configured, choose the green **Play** button.</span></span>  <span data-ttu-id="e3c90-146">Visual Studio votre application, démarrez le serveur web, lancez Microsoft Edge et accédez à ou à n’importe quel `https://localhost:44362/` port spécifié dans `launchSettings.json` .</span><span class="sxs-lookup"><span data-stu-id="e3c90-146">Visual Studio builds your app, start the web server, launch Microsoft Edge, and navigate to `https://localhost:44362/` or whatever port is specified in `launchSettings.json`.</span></span>  

:::image type="complex" source="./media/edge-launch.png" alt-text="Lancement de Microsoft Edge à partir de Visual Studio" lightbox="./media/edge-launch.png":::
   <span data-ttu-id="e3c90-148">Lancement de Microsoft Edge à partir de Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-148">Microsoft Edge launches from Visual Studio</span></span>  
:::image-end:::  

### <a name="debug-javascript-running-in-microsoft-edge"></a><span data-ttu-id="e3c90-149">Débogage de JavaScript en cours d’exécution dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e3c90-149">Debug JavaScript running in Microsoft Edge</span></span>  

<span data-ttu-id="e3c90-150">Revenir à Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e3c90-150">Switch back to Visual Studio.</span></span>  <span data-ttu-id="e3c90-151">In `Counter.js` , to set a breakpoint on Line 13, choose the gutter next to the line.</span><span class="sxs-lookup"><span data-stu-id="e3c90-151">In `Counter.js`, to set a breakpoint on Line 13, choose the gutter next to the line.</span></span>  

:::image type="complex" source="./media/set-breakpoint.png" alt-text="Choisissez la caniveau en face de la ligne 13 Counter.js pour définir un point d’arrêt dans Visual Studio" lightbox="./media/set-breakpoint.png":::
   <span data-ttu-id="e3c90-153">Choisissez la caniveau en face de la ligne 13 `Counter.js` pour définir un point d’arrêt dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-153">Choose the gutter next to Line 13 in `Counter.js` to set a breakpoint in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-154">Revenir à l’instance de Microsoft Edge Visual Studio lancée.</span><span class="sxs-lookup"><span data-stu-id="e3c90-154">Now switch back to the instance of Microsoft Edge that Visual Studio launched.</span></span>  <span data-ttu-id="e3c90-155">Choisissez sur **Compteur** dans navMenu à gauche de la page web.</span><span class="sxs-lookup"><span data-stu-id="e3c90-155">Choose on **Counter** in the NavMenu on the left of the webpage.</span></span>  <span data-ttu-id="e3c90-156">Maintenant, choisissez **Incrément .**</span><span class="sxs-lookup"><span data-stu-id="e3c90-156">Now choose **Increment**.</span></span>  

:::image type="complex" source="./media/edge-counter.png" alt-text="Page Compteur dans notre application ASP.NET web principale" lightbox="./media/edge-counter.png":::
   <span data-ttu-id="e3c90-158">Page Compteur dans notre application ASP.NET web principale</span><span class="sxs-lookup"><span data-stu-id="e3c90-158">The Counter page in our ASP.NET Core web app</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-159">Le débogger JavaScript dans Visual Studio atteint le point d’arrêt que vous définissez dans `Counter.js` .</span><span class="sxs-lookup"><span data-stu-id="e3c90-159">The JavaScript debugger in Visual Studio hits the breakpoint you set in `Counter.js`.</span></span>  <span data-ttu-id="e3c90-160">Visual Studio suspend désormais l’exécution du javaScript exécuté dans Microsoft Edge et vous pouvez exécuter le script ligne par ligne.</span><span class="sxs-lookup"><span data-stu-id="e3c90-160">Visual Studio now pauses the runtime of the JavaScript running in Microsoft Edge and you may step through the script line-by-line.</span></span>  

:::image type="complex" source="./media/hit-breakpoint.png" alt-text="Visual Studio javaScript s’exécute dans Microsoft Edge" lightbox="./media/hit-breakpoint.png":::
   <span data-ttu-id="e3c90-162">Visual Studio javaScript s’exécute dans Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e3c90-162">Visual Studio pauses JavaScript running in Microsoft Edge</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-163">L’exemple n’était qu’une démonstration mineure des fonctionnalités disponibles dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e3c90-163">The example was just a minor demonstration of the functionality available in Visual Studio.</span></span>  <span data-ttu-id="e3c90-164">Pour plus d’informations sur les fonctionnalités Visual Studio 2019, accédez [à Visual Studio documentation.][VisualStudioWindowsIndex]</span><span class="sxs-lookup"><span data-stu-id="e3c90-164">For more information about the functionality in Visual Studio 2019, navigate to [Visual Studio documentation][VisualStudioWindowsIndex].</span></span>  

## <a name="attach-to-microsoft-edge"></a><span data-ttu-id="e3c90-165">Attacher à Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e3c90-165">Attach to Microsoft Edge</span></span>  

<span data-ttu-id="e3c90-166">Auparavant, vous deviez lancer Microsoft Edge à partir Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e3c90-166">Previously, you had to launch Microsoft Edge from Visual Studio.</span></span>  <span data-ttu-id="e3c90-167">À présent, vous pouvez attacher le débogger Visual Studio à une instance de Microsoft Edge déjà en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e3c90-167">Now, you are able to attach the Visual Studio debugger to an already running instance of Microsoft Edge.</span></span>  

<span data-ttu-id="e3c90-168">Tout d’abord, assurez-vous qu’il n’existe aucune instance en cours d’exécution de Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e3c90-168">First, ensure that there are no running instances of Microsoft Edge.</span></span>  <span data-ttu-id="e3c90-169">À présent, à partir de votre ligne de commande, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="e3c90-169">Now, from your command line, run the following command.</span></span>  

```console
start msedge –remote-debugging-port=9222
```  

<span data-ttu-id="e3c90-170">À Visual Studio, ouvrez le menu **Débogage** et choisissez **Attacher au** processus ou sélectionnez `Ctrl` + `Alt` + `P` .</span><span class="sxs-lookup"><span data-stu-id="e3c90-170">From Visual Studio, open the **Debug** menu and choose **Attach to Process** or select `Ctrl`+`Alt`+`P`.</span></span>  

:::image type="complex" source="./media/attach-to-process.png" alt-text="Choose Attach to Process in Visual Studio" lightbox="./media/attach-to-process.png":::
   <span data-ttu-id="e3c90-172">Choose **Attach to Process** in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-172">Choose **Attach to Process** in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-173">À partir de **la boîte de dialogue Attacher** au processus, définissez le **type** de connexion sur websocket de protocole **Chrome devtools (aucune authentification).**</span><span class="sxs-lookup"><span data-stu-id="e3c90-173">From the **Attach to Process** dialog, set **Connection type** to **Chrome devtools protocol websocket (no authentication)**.</span></span>  <span data-ttu-id="e3c90-174">Dans la **boîte de texte Cible** de connexion, `http://localhost:9222/` tapez et sélectionnez `Enter` .</span><span class="sxs-lookup"><span data-stu-id="e3c90-174">In the **Connecting target** textbox, type `http://localhost:9222/` and select `Enter`.</span></span>  <span data-ttu-id="e3c90-175">Examinez la liste des onglets ouverts que vous avez dans Microsoft Edge répertoriés dans la boîte de dialogue Attacher **au** processus.</span><span class="sxs-lookup"><span data-stu-id="e3c90-175">Review the list of open tabs you have in Microsoft Edge listed out in the **Attach to Process** dialog.</span></span>  

:::image type="complex" source="./media/attach-to-process-dialog.png" alt-text="Configurer la boîte de dialogue Attacher au processus dans Visual Studio" lightbox="./media/attach-to-process-dialog.png":::
   <span data-ttu-id="e3c90-177">Configurer la boîte **de dialogue Attacher au** processus dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-177">Configure the **Attach to Process** dialog in Visual Studio</span></span>  
:::image-end:::  

<span data-ttu-id="e3c90-178">**Sélectionnez...** > case à cocher en regard de **JavaScript (Microsoft Edge – Chromium).**</span><span class="sxs-lookup"><span data-stu-id="e3c90-178">Choose **Select...** > the checkbox next to **JavaScript (Microsoft Edge – Chromium)**.</span></span>  <span data-ttu-id="e3c90-179">Pour ajouter des onglets, accédez aux nouveaux onglets, fermez \*\*\*\* les onglets et affichez les modifications reflétées dans la boîte de dialogue Attacher au processus, sélectionnez **le bouton Actualiser.**</span><span class="sxs-lookup"><span data-stu-id="e3c90-179">To add tabs, navigate to new tabs, and close tabs and display the changes reflected in the **Attach to Process** dialog, choose the **Refresh** button.</span></span>  <span data-ttu-id="e3c90-180">Choisissez l’onglet que vous souhaitez déboguer et choisissez **Attacher.**</span><span class="sxs-lookup"><span data-stu-id="e3c90-180">Choose the tab you want to debug and choose **Attach**.</span></span>  

<span data-ttu-id="e3c90-181">Le débo Visual Studio est maintenant attaché à Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e3c90-181">The Visual Studio debugger is now attached to Microsoft Edge.</span></span>  <span data-ttu-id="e3c90-182">Vous pouvez suspendre l’exécution de JavaScript, définir des points d’arrêt et réviser des instructions directement dans la fenêtre Sortie `console.log()` de débogage Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e3c90-182">You may pause the running of JavaScript, set breakpoints, and review `console.log()` statements directly in the Debug Output window in Visual Studio.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-visual-studio-team"></a><span data-ttu-id="e3c90-183">Entrer en contact avec l’équipe microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-183">Getting in touch with the Microsoft Visual Studio team</span></span>  

<span data-ttu-id="e3c90-184">Les équipes Microsoft Visual Studio et Microsoft Edge souhaitent en savoir plus sur la façon dont vous travaillez avec JavaScript dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e3c90-184">The Microsoft Visual Studio and Microsoft Edge teams wants to learn more about how you work with JavaScript in Visual Studio.</span></span>  <span data-ttu-id="e3c90-185">Pour envoyer vos commentaires, sélectionnez l’icône Envoyer des commentaires Visual Studio ou tweetez-@VisualStudio [et @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools]. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="e3c90-185">To send your feedback, choose the **Send Feedback** icon in Visual Studio or tweet [@VisualStudio and @EdgeDevTools][TwitterIntentTweetViualstudioEdgdevtools].</span></span>  

:::image type="complex" source="./media/feedback-icon.png" alt-text="Icône Envoyer des commentaires dans Visual Studio" lightbox="./media/feedback-icon.png":::
   <span data-ttu-id="e3c90-187">Icône **Envoyer des commentaires** dans Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e3c90-187">The **Send Feedback** icon in Visual Studio</span></span>  
:::image-end:::  

<!-- links -->  

[VisualStudioWindowsIndex]: /visualstudio/windows/index "Visual Studio documentation | Documents Microsoft"  

[MicrosoftVisualstudioDownloads]: https://visualstudio.microsoft.com/downloads "Télécharger Visual Studio"  
[MicrosoftVisualstudioVs]: https://visualstudio.microsoft.com/vs "Visual Studio IDE"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Télécharger les canaux Microsoft Edge Insider"  

[TwitterIntentTweetViualstudioEdgdevtools]: https://twitter.com/intent/tweet?text=@VisualStudio+@EdgeDevTools "Tweet vers @VisualStudio et @EdgeDevTools | Twitter"  
