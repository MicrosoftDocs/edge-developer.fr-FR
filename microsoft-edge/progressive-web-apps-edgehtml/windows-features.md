---
description: Améliorer progressivement votre PWA pour Windows avec les fonctionnalités d’application natives
title: Personnaliser votre PWA pour Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, WinRT, UWP, EdgeHTML
ms.openlocfilehash: 5bad708db5b13517fd1887214a5e1d5457796ee2
ms.sourcegitcommit: e07de36ee9fbe20422ffc2c62b98839851e1b02b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2020
ms.locfileid: "10604010"
---
# <span data-ttu-id="5567c-104">Personnaliser votre PWA (EdgeHTML) pour Windows</span><span class="sxs-lookup"><span data-stu-id="5567c-104">Tailor your PWA (EdgeHTML) for Windows</span></span>  

<span data-ttu-id="5567c-105">PWAs installé sur Windows 10 Profitez de [tous les avantages de l'][PwaIndexWindows10] utilisation des applications de [plateforme Windows universelle (UWP)][WindowsUWPGetStartedGuide] , notamment la protection de l’application Windows en mode sandbox et un accès complet aux API [Windows Runtime \ (WinRT \))][UwpApiIndex] , notamment pour:</span><span class="sxs-lookup"><span data-stu-id="5567c-105">PWAs installed on Windows 10 enjoy [all the benefits][PwaIndexWindows10] of running as [Universal Windows Platform \(UWP\)][WindowsUWPGetStartedGuide] apps, including protection through Windows app sandboxing security and full access to [Windows Runtime \(WinRT\))][UwpApiIndex] APIs, including those for:</span></span>  

*   <span data-ttu-id="5567c-106">Contrôle des fonctionnalités du périphérique (par exemple, caméra, micro, GPS \)</span><span class="sxs-lookup"><span data-stu-id="5567c-106">Controlling device features \(such as camera, microphone, GPS\)</span></span>  
*   <span data-ttu-id="5567c-107">Accès aux ressources utilisateur \ (par exemple, calendrier, contacts, documents, musique \)</span><span class="sxs-lookup"><span data-stu-id="5567c-107">Accessing user resources \(such as calendar, contacts, documents, music\)</span></span>  
*   <span data-ttu-id="5567c-108">Lancement/déplacement de votre application par le biais des commandes vocales Cortana</span><span class="sxs-lookup"><span data-stu-id="5567c-108">Launching / navigating your app through Cortana voice commands</span></span>  
*   <span data-ttu-id="5567c-109">Intégration du système d’exploitation Windows \ (via le centre de notifications Windows, de la barre des tâches du bureau et des menus contextuels)</span><span class="sxs-lookup"><span data-stu-id="5567c-109">Integrating with the Windows OS \(through the Windows Action Center, desktop taskbar, and context menus\)</span></span>  

<span data-ttu-id="5567c-110">... et ce n’est que quelques-unes des possibilités ajoutées pour votre PWA \ (EdgeHTML \) sur Windows.</span><span class="sxs-lookup"><span data-stu-id="5567c-110">... and these are only a few of the added possibilities for your PWA \(EdgeHTML\) on Windows!</span></span>  

<span data-ttu-id="5567c-111">Ce guide décrit l’installation, l’exécution et l’amélioration de votre application PWA \ (EdgeHTML \) en tant qu’application Windows 10, tout en garantissant la compatibilité entre navigateur et multiplateforme.</span><span class="sxs-lookup"><span data-stu-id="5567c-111">This guide shows you how to install, run, and enhance your PWA \(EdgeHTML\) as a Windows 10 app, while still ensuring cross-browser and cross-platform compatibility.</span></span>  

## <span data-ttu-id="5567c-112">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="5567c-112">Prerequisites</span></span>  

*   <span data-ttu-id="5567c-113">Une application Web PWA (ou une application Web hébergée) existante, qui est un site Live ou localhost.</span><span class="sxs-lookup"><span data-stu-id="5567c-113">An existing PWA \(or hosted web app\), either a live or localhost site.</span></span>  <span data-ttu-id="5567c-114">Ce guide utilise l’exemple de PWA dans [prise en main des applications Web progressives][PwaGetStarted].</span><span class="sxs-lookup"><span data-stu-id="5567c-114">This guide uses the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted].</span></span>  
*   <span data-ttu-id="5567c-115">Téléchargez la [communauté 2017 Visual Studio Community][MicrosoftVisualStudio|::ref1::|].</span><span class="sxs-lookup"><span data-stu-id="5567c-115">Download the \(free\) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span></span>  <span data-ttu-id="5567c-116">Vous pouvez également utiliser les éditions professionnel, entreprise ou [preview][MicrosoftVisualStudioPreview] .</span><span class="sxs-lookup"><span data-stu-id="5567c-116">You are also able to use the Professional, Enterprise, or [Preview][MicrosoftVisualStudioPreview] editions.</span></span>  <span data-ttu-id="5567c-117">Dans le programme d’installation de Visual Studio, choisissez les charges de travail suivantes:</span><span class="sxs-lookup"><span data-stu-id="5567c-117">From the Visual Studio Installer, choose the following Workloads:</span></span>  
    *   **<span data-ttu-id="5567c-118">Développement de plateforme Windows universelle</span><span class="sxs-lookup"><span data-stu-id="5567c-118">Universal Windows Platform development</span></span>**  

## <span data-ttu-id="5567c-119">Configuration et exécution de votre application Windows universelle</span><span class="sxs-lookup"><span data-stu-id="5567c-119">Set up and run your Universal Windows app</span></span>  

<span data-ttu-id="5567c-120">Une application PWA \ (EdgeHTML \) installée en tant qu’application Windows 10 s’exécute en même temps que le navigateur, dans une fenêtre autonome \ ( `WWAHost.exe` processus \).</span><span class="sxs-lookup"><span data-stu-id="5567c-120">A PWA \(EdgeHTML\) installed as a Windows 10 app runs independently from the browser, in a standalone \(`WWAHost.exe` process\) window.</span></span>  <span data-ttu-id="5567c-121">Pour cela, il vous suffit de disposer d’un wrapper d’application léger qui contient votre application Web hébergée, que vous pouvez configurer rapidement à l’aide du modèle de projet Visual Studio `Progressive Web App (Universal Windows)` .</span><span class="sxs-lookup"><span data-stu-id="5567c-121">Enabling this simply requires a lightweight app wrapper that contains your hosted web app, which you are able to quickly set up using the Visual Studio `Progressive Web App (Universal Windows)` project template.</span></span>  <span data-ttu-id="5567c-122">\ (Toute la logique de votre application, y compris l’envoi de demandes d’API Windows Runtime natives, a toujours lieu dans le code de votre application Web d’origine. \)</span><span class="sxs-lookup"><span data-stu-id="5567c-122">\(All your app logic, including sending native Windows Runtime API requests, still happens in your original web app code.\)</span></span>  

<span data-ttu-id="5567c-123">Configurez votre environnement de développement d’applications Windows dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5567c-123">Set up your Windows app development environment in Visual Studio.</span></span>  

1.  <span data-ttu-id="5567c-124">Dans les paramètres Windows, activez le [mode développeur][WindowsUWPGetStartedEnable].</span><span class="sxs-lookup"><span data-stu-id="5567c-124">In your Windows Settings, turn on [Developer mode][WindowsUWPGetStartedEnable].</span></span>  <span data-ttu-id="5567c-125">\ (Tapez `developer mode` dans le Searchbar Windows pour le trouver. \)</span><span class="sxs-lookup"><span data-stu-id="5567c-125">\(Type `developer mode` in the Windows searchbar to find it.\)</span></span>  
1.  <span data-ttu-id="5567c-126">Lancez Visual Studio et **créez un projet...**</span><span class="sxs-lookup"><span data-stu-id="5567c-126">Launch Visual Studio and **Create a new project...**</span></span>  
1.  <span data-ttu-id="5567c-127">Sélectionnez le modèle de projet de création de **packages d’applications Windows** C#.</span><span class="sxs-lookup"><span data-stu-id="5567c-127">Select the C# **Windows Application Packaging Project** template.</span></span>  <span data-ttu-id="5567c-128">Si vous utilisez une version antérieure de Visual Studio, recherchez le modèle équivalent sous **application Web hébergée (Windows universel)** ou **application Web progressive (Windows universel)**.</span><span class="sxs-lookup"><span data-stu-id="5567c-128">If you are using a previous version of Visual Studio, find the equivalent template under **Hosted Web App (Universal Windows)** or **Progressive Web App (Universal Windows)**.</span></span>  
1.  <span data-ttu-id="5567c-129">Sélectionnez la version par défaut de Windows 10 `Target version` \ (version la plus récente \) et `Minimum version` \ (Build 10586 ou version ultérieure), puis cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="5567c-129">Select the default Windows 10 `Target version` \(most recent release\) and `Minimum version` \(build 10586 or higher\) and click **OK**.</span></span>  

    ![Boîte de dialogue de sélection Visual Studio pour les builds cibles de projet UWP](media/vs-target-min-version.png)  

    <span data-ttu-id="5567c-131">Votre nouveau projet se charge avec le concepteur package. appxmanifest ouvert.</span><span class="sxs-lookup"><span data-stu-id="5567c-131">Your new project loads with the package.appxmanifest designer open.</span></span>  <span data-ttu-id="5567c-132">C’est ici que vous configurez les détails de votre application, notamment l’identité du package, les dépendances du package, les fonctionnalités requises, les éléments visuels et les points d’extensibilité.</span><span class="sxs-lookup"><span data-stu-id="5567c-132">This is where you configure the details of your app, including package identity, package dependencies, required capabilities, visual elements, and extensibility points.</span></span>  <span data-ttu-id="5567c-133">Il s’agit d’une version temporaire facilement configurable du manifeste du package d’application utilisée lors du développement de l’application.</span><span class="sxs-lookup"><span data-stu-id="5567c-133">This is an easily configurable, temporary version of the app package manifest used during app development.</span></span>  
    <span data-ttu-id="5567c-134">Lorsque vous générez votre projet d’application, [Visual Studio génère un fichier AppxManifest. xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] à partir de ces métadonnées, qui est utilisé pour installer et exécuter votre application.</span><span class="sxs-lookup"><span data-stu-id="5567c-134">When you build your app project, [Visual Studio generates an AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] file from this metadata, which is used to install and run your app.</span></span>  <span data-ttu-id="5567c-135">Chaque fois que vous mettez à jour votre `package.appxmanifest` fichier, veillez à régénérer le projet afin que les deux apparaissent dans votre `AppxManifest.xml` Runtime.</span><span class="sxs-lookup"><span data-stu-id="5567c-135">Whenever you update your `package.appxmanifest` file, be sure to rebuild the project so both are reflected in your `AppxManifest.xml` at runtime.</span></span>  

1.  <span data-ttu-id="5567c-136">Dans le volet de l' **application** Project Designer, entrez l’URL de votre fichier `Start page` .</span><span class="sxs-lookup"><span data-stu-id="5567c-136">In the manifest designer **Application** panel, enter the URL of your PWA as the `Start page`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5567c-137">Les travailleurs de service sont pris en charge pour toutes les URL HTTPS \ (sécurisées \) spécifiées en tant que `StartPage` .</span><span class="sxs-lookup"><span data-stu-id="5567c-137">Service workers are supported for all https \(secure, remote\) urls specified as the `StartPage`.</span></span>  <span data-ttu-id="5567c-138">Par défaut, les travailleurs de services ne sont pas pris en charge pour les applications Web qui spécifient une page d’accueil locale.</span><span class="sxs-lookup"><span data-stu-id="5567c-138">Service workers are not supported by default for web apps that specify a local start page.</span></span>  <span data-ttu-id="5567c-139">Pour permettre la prise en charge du travailleur de service dans ces cas-là, ajoutez une entrée [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) explicite au manifeste, par exemple:</span><span class="sxs-lookup"><span data-stu-id="5567c-139">To enable service worker support for these cases, add an explicit [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) entry to the manifest, for example:</span></span> `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Panneau application de package. appxmanifest designer](media/vs-manifest-application.png)  
    
    <span data-ttu-id="5567c-141">Vous pouvez également modifier le `Display name` et `Description` comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="5567c-141">You are able to also modify the `Display name` and `Description` as you like.</span></span>  
1.  <span data-ttu-id="5567c-142">Enregistrez ce fichier \ (ou une autre image 512x512 de votre choix) sur votre ordinateur de bureau.</span><span class="sxs-lookup"><span data-stu-id="5567c-142">Save this file \(or another 512x512 image of your choosing\) to your desktop.</span></span>  
    <span data-ttu-id="5567c-143">Dans le panneau **composants visuels** du concepteur de manifeste, cliquez sur le `Source` bouton champ **...** , sélectionnez-le en tant que fichier source, puis cliquez sur **générer**.</span><span class="sxs-lookup"><span data-stu-id="5567c-143">Then, in the manifest designer **Visual Assets** panel, click on the `Source` field **...** button, select it as your source file, and click **Generate**.</span></span>  <span data-ttu-id="5567c-144">\ (Puis cliquez sur **OK** pour remplacer les images d’espaces réservés par défaut).</span><span class="sxs-lookup"><span data-stu-id="5567c-144">\(Then click **OK** to overwrite the default placeholder images\).</span></span>  
    
    ![Panneau de ressources visuelles de package. appxmanifest designer](media/vs-manifest-visual-assets.png)  
    
    <span data-ttu-id="5567c-146">Cela génère les ressources visuelles de base pour l’installation, l’exécution, le lancement et la distribution de votre application dans le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5567c-146">This generates the basic visual assets for installing, running, launching, and distributing your app in the store.</span></span>  
    <span data-ttu-id="5567c-147">Si vous voyez des erreurs rouges \ ( `X` \) indiquant des images manquantes, vous pouvez cliquer sur les boutons **...** pour sélectionner manuellement un fichier à partir des images générées.</span><span class="sxs-lookup"><span data-stu-id="5567c-147">If you see any red \(`X`\) errors indicating missing images, you are able to click on the **...** buttons to manually select a file from the generated images.</span></span>  
1.  <span data-ttu-id="5567c-148">Dans le volet des **URI de contenu** du concepteur de manifeste, remplacez `http://example.com` par l’emplacement de votre fichier `Rule`  =  `include` . `WinRT Access`  =  `All`</span><span class="sxs-lookup"><span data-stu-id="5567c-148">In the manifest designer **Content URIs** panel, replace `http://example.com` with the location of your PWA \(such that `Rule` = `include` and `WinRT Access` = `All`\).</span></span>  
    <span data-ttu-id="5567c-149">Cela octroie à votre accès à PWA l’autorisation d’envoyer des demandes d’API Windows Runtime Windows en natif lors de l’exécution en tant qu’application Windows 10, qui est abordée plus tard.</span><span class="sxs-lookup"><span data-stu-id="5567c-149">This grants your PWA permission to send native Windows Runtime \(WinRT\) API requests when running as a Windows 10 app, which is covered a bit later.</span></span>   <span data-ttu-id="5567c-150">Si votre application PWA réelle ne requiert pas l’accès WinRT, vous pouvez basculer la `WinRT Access` valeur vers `None` .</span><span class="sxs-lookup"><span data-stu-id="5567c-150">If your actual PWA does not require WinRT access, you are able to switch the `WinRT Access` value to `None`.</span></span>  <span data-ttu-id="5567c-151">Quelle que soit la méthode utilisée, veillez à désactiver la chaîne par défaut `http://example.com` avec l’URI de votre PWA ou votre application ne peut pas être chargée correctement au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="5567c-151">Either way, be sure to sub out the default `http://example.com` string with the URI of your PWA, or your app is not able to properly load at runtime.</span></span>  
    <span data-ttu-id="5567c-152">Vous pouvez exécuter et déboguer votre PWA en tant qu’application Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5567c-152">You are ready to run and debug your PWA as a Windows 10 app.</span></span>  <span data-ttu-id="5567c-153">Si vous utilisez un site localhost pour suivre ce guide, assurez-vous qu’il est en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="5567c-153">If you are using a localhost site to step through this guide, make sure it is running.</span></span>  <span data-ttu-id="5567c-154">Puis</span><span class="sxs-lookup"><span data-stu-id="5567c-154">Then,</span></span>  
1.  <span data-ttu-id="5567c-155">Créez \ ( `Ctrl` + `Shift` + `F5` \) et exécutez \ ( `F5` \) votre projet Project Web App.</span><span class="sxs-lookup"><span data-stu-id="5567c-155">Build \(`Ctrl`+`Shift`+`F5`\) and Run \(`F5`\) your PWA project.</span></span>  <span data-ttu-id="5567c-156">Votre site Web doit maintenant être lancé dans une fenêtre d’application autonome.</span><span class="sxs-lookup"><span data-stu-id="5567c-156">Your website should now launch in a standalone app window.</span></span>  <span data-ttu-id="5567c-157">Non seulement il s’agit d’une application Web hébergée; Il s’exécute en tant qu’application Web progressive installée sur Windows 10.</span><span class="sxs-lookup"><span data-stu-id="5567c-157">Not only is it a hosted web app; it is running as a Progressive Web App installed on Windows 10!</span></span>  

    ![PWA s’exécute dans une fenêtre WWAHost. exe](media/wwahost.png)  

## <span data-ttu-id="5567c-159">Déboguer votre PWA \ (EdgeHTML \) en tant qu’application Windows</span><span class="sxs-lookup"><span data-stu-id="5567c-159">Debug your PWA \(EdgeHTML\) as a Windows app</span></span>  

<span data-ttu-id="5567c-160">Dans la mesure où une application Web hébergée par le biais d’une application Web PWA est simplement améliorée, vous pouvez déboguer votre code côté serveur de la même manière que n’importe quelle application Web, à l’aide de votre IDE et de votre flux de travail habituels.</span><span class="sxs-lookup"><span data-stu-id="5567c-160">Because a PWA \(EdgeHTML\) is simply a progressively enhanced hosted web app, you are able to debug your server-side code the same as any web app, using your usual IDE and workflow.</span></span>  <span data-ttu-id="5567c-161">Les modifications que vous déployez en direct sont reflétées dans votre installation de Project Web App la prochaine fois que vous lancez l’application.</span><span class="sxs-lookup"><span data-stu-id="5567c-161">The changes you deploy live are reflected in your installed PWA the next time you launch it \(no need to redeploy your Universal Windows app package\).</span></span>

<span data-ttu-id="5567c-162">Pour le débogage côté client dans votre application Windows 10, vous devez disposer de l' `Microsoft Edge DevTools Preview` application.</span><span class="sxs-lookup"><span data-stu-id="5567c-162">For client-side debugging within your Windows 10 app, you must have the `Microsoft Edge DevTools Preview` app.</span></span>  <span data-ttu-id="5567c-163">Cette application autonome inclut toutes les fonctionnalités de la version d’origine du navigateur [Microsoft Edge devtools][DevToolsGuide] \ (y compris les [Outils PWA][DevToolsGuideServiceWorkers]\), ainsi que la prise en charge des fonctionnalités de [débogage à distance][DevToolsProtocol01ClientsEdgePreview] de base et un [Sélecteur de cibles de débogage][DevToolsGuideMicrosoftStoreApp] pour l’attachement à une instance en cours d’exécution du moteur EdgeHTML, y compris des compléments pour Office, Cortana</span><span class="sxs-lookup"><span data-stu-id="5567c-163">This standalone app includes all the functionality of the original in-browser [Microsoft Edge DevTools][DevToolsGuide] \(including [PWA tools][DevToolsGuideServiceWorkers]\), plus basic [remote debugging][DevToolsProtocol01ClientsEdgePreview] support and a [Debug Target chooser][DevToolsGuideMicrosoftStoreApp] for attaching to any running instance of the EdgeHTML engine, including add-ins for Office, Cortana, app webviews, and of course, PWAs running on Windows.</span></span>  

<span data-ttu-id="5567c-164">Voici la procédure à suivre pour configurer le débogage pour votre page PWA \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="5567c-164">Here is how to set up debugging for your PWA \(EdgeHTML\).</span></span>  

1.  <span data-ttu-id="5567c-165">Installez l’application [Microsoft Edge devtools Preview][MicrosoftStoreEdgeDevtoolsPreview] à partir du Microsoft Store si vous ne l’avez pas encore.</span><span class="sxs-lookup"><span data-stu-id="5567c-165">Install the [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] app from the Microsoft Store if you do not already have it.</span></span>  
1.  <span data-ttu-id="5567c-166">Une fois le site de PWA en service opérationnel, lancez l’application DevTools.</span><span class="sxs-lookup"><span data-stu-id="5567c-166">With your PWA site up and running, launch the DevTools app.</span></span>  
1.  <span data-ttu-id="5567c-167">Dans Visual Studio, lancez votre application Windows 10 avec la `Start Without Debugging` `Ctrl` + `F5` commande ().</span><span class="sxs-lookup"><span data-stu-id="5567c-167">From Visual Studio, launch your Windows 10 app with the `Start Without Debugging` (`Ctrl`+`F5`) command.</span></span>  <span data-ttu-id="5567c-168">\ (L’application DevTools n’est pas correctement jointe si le débogueur Visual Studio est actif. \)</span><span class="sxs-lookup"><span data-stu-id="5567c-168">\(The DevTools app does not attach properly if the Visual Studio debugger is active.\)</span></span>  
1.  <span data-ttu-id="5567c-169">Dans l’application DevTools, cliquez sur le bouton **Actualiser** du sélecteur de cibles de débogage local.</span><span class="sxs-lookup"><span data-stu-id="5567c-169">In the DevTools app, click the **Refresh** button in the Local debug target chooser.</span></span>  <span data-ttu-id="5567c-170">Votre site PWA \ (EdgeHTML \) doit maintenant être répertorié.</span><span class="sxs-lookup"><span data-stu-id="5567c-170">Your PWA \(EdgeHTML\) site should now be listed.</span></span>  <span data-ttu-id="5567c-171">\ (S’il s’exécute également dans une fenêtre de navigateur, il s’agit de la dernière instance de ce site dans la liste. \)</span><span class="sxs-lookup"><span data-stu-id="5567c-171">\(If it is also running in a browser window, it is the last instance of that site in the list.\)</span></span>  
1.  <span data-ttu-id="5567c-172">Cliquez sur votre annonce sur votre site Web (EdgeHTML \) pour ouvrir un nouvel onglet d’instance DevTools et démarrer le débogage.</span><span class="sxs-lookup"><span data-stu-id="5567c-172">Click on your PWA \(EdgeHTML\) site listing to open a new DevTools instance tab and start debugging.</span></span>  
    
    ![Sélecteur de cibles de débogage local dans l’application Microsoft Edge DevTools](media/devtools-local.png)  
    
1.  <span data-ttu-id="5567c-174">Vous pouvez vérifier que DevTools est attaché à votre application PWA-en tant que Windows.</span><span class="sxs-lookup"><span data-stu-id="5567c-174">You are able to verify that DevTools is attached to your PWA-running-as-Windows-app.</span></span>  <span data-ttu-id="5567c-175">Dans la **console**devtools, tapez:</span><span class="sxs-lookup"><span data-stu-id="5567c-175">In the DevTools **Console**, type:</span></span>  
    
    ```shell
    window.Windows
    ```  
    
    <span data-ttu-id="5567c-176">Cela renvoie l' `Windows Runtime` objet global contenant tous les [espaces de noms WinRT de niveau supérieur](#find-windows-runtime-winrt-apis).</span><span class="sxs-lookup"><span data-stu-id="5567c-176">This returns the global `Windows Runtime` object containing all of the [top-level WinRT namespaces](#find-windows-runtime-winrt-apis).</span></span>  <span data-ttu-id="5567c-177">Il s’agit de votre point d’entrée pour la [plateforme Windows universelle][WindowsUWPIndex]qui s’exécute sur votre ordinateur Windows 10, et n’est exposé qu’aux applications Web qui s’exécutent en tant qu’applications Windows 10 (exécutées en dehors du navigateur dans le cadre d’un `WWAHost.exe` processus).</span><span class="sxs-lookup"><span data-stu-id="5567c-177">This is your PWA \(EdgeHTML\) entrypoint to the [Universal Windows Platform][WindowsUWPIndex], and only exposed to web apps that run as Windows 10 apps (running outside the browser, in a `WWAHost.exe` process).</span></span>  
    
## <span data-ttu-id="5567c-178">Rechercher les API Windows Runtime \ (WinRT \)</span><span class="sxs-lookup"><span data-stu-id="5567c-178">Find Windows Runtime \(WinRT\) APIs</span></span>  

<span data-ttu-id="5567c-179">Dans le cas d’une application Windows installée, votre application [PWA \ (EdgeHTML \) dispose d’un accès complet aux API Windows Runtime natives][WindowsRuntime]; Déterminez ce que vous devez utiliser, obtenez les autorisations requises, puis utilisez la détection de fonctionnalités pour envoyer cette demande d’API dans les environnements pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5567c-179">As an installed Windows app, your [PWA \(EdgeHTML\) has full access to native Windows Runtime APIs][WindowsRuntime]; identify what you need to use, obtain the requisite permissions, and employ feature detection to send that API request on supported environments.</span></span>  <span data-ttu-id="5567c-180">Parcourez ce processus pour ajouter une amélioration progressive aux utilisateurs de bureau Windows de votre ordinateur de bureau Windows.</span><span class="sxs-lookup"><span data-stu-id="5567c-180">Walk through this process to add a progressive enhancement for Windows desktop users of your PWA.</span></span>  

<span data-ttu-id="5567c-181">Il existe de nombreuses façons d’identifier les API de plateforme Windows universelle dont vous avez besoin pour votre Windows PWA, y compris la recherche dans l’ensemble des API de la plateforme Windows sur le centre de développement Windows, et le téléchargement et l’exécution d' [exemples de code UWP](#uwp-code-samples) avec Visual Studio, ainsi que les extraits de code de navigation pour les tâches courantes pour PWAS sur Windows.</span><span class="sxs-lookup"><span data-stu-id="5567c-181">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for PWAs on Windows.</span></span>

<span data-ttu-id="5567c-182">Il existe de nombreuses façons d’identifier les API de plateforme Windows universelle dont vous avez besoin pour votre Windows PWA, y compris la recherche dans l’ensemble des API de la plateforme Windows sur le centre de développement Windows (UWP/API/), le téléchargement et l’exécution d' [exemples de code UWP](#uwp-code-samples) dans Visual Studio, et les extraits de code pour les tâches courantes pour [PWAS sur Windows 10 (EdgeHTML)][PwaIndexWindows10]</span><span class="sxs-lookup"><span data-stu-id="5567c-182">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for [PWAs on Windows 10 (EdgeHTML)][PwaIndexWindows10].</span></span>  

<span data-ttu-id="5567c-183">Le fonctionnement global des API WinRT dans JavaScript, de la même manière que dans C#, vous pouvez suivre la [documentation de la plateforme Windows universelle][WindowsUWPIndex] et la [référence d’API][UwpApiIndex] pour l’utilisation.</span><span class="sxs-lookup"><span data-stu-id="5567c-183">Overall, WinRT APIs work in JavaScript the same way they do in C#, so you may follow the general [Universal Windows Platform documentation][WindowsUWPIndex] and [API Reference][UwpApiIndex] for usage.</span></span>  <span data-ttu-id="5567c-184">Notez toutefois les différences suivantes:</span><span class="sxs-lookup"><span data-stu-id="5567c-184">However, please note the following differences:</span></span>  

*   <span data-ttu-id="5567c-185">Les fonctionnalités WinRT dans JavaScript utilisent [différentes conventions de casse][ScriptingJsinrtUsingWinRTCasingConventions]</span><span class="sxs-lookup"><span data-stu-id="5567c-185">WinRT features in JavaScript use  [different casing conventions][ScriptingJsinrtUsingWinRTCasingConventions]</span></span>  
*   <span data-ttu-id="5567c-186">[Les événements sont représentés sous forme de identificateurs de chaîne][ScriptingJsinrtHandlingWinRTEvents] transmis à des `addEventListener` / `removeEventListener` méthodes de classe.</span><span class="sxs-lookup"><span data-stu-id="5567c-186">[Events are represented as string identifiers][ScriptingJsinrtHandlingWinRTEvents] passed to class `addEventListener`/`removeEventListener` methods</span></span>  
*   <span data-ttu-id="5567c-187">Les [méthodes asynchrones][ScriptingJsinrtUsingWinRT] utilisent le modèle de promesse JavaScript</span><span class="sxs-lookup"><span data-stu-id="5567c-187">[Asynchronous methods][ScriptingJsinrtUsingWinRT] use the JavaScript Promise model</span></span>  
*   <span data-ttu-id="5567c-188">Les API dans l' `Windows.UI.Xaml` espace de noms ne sont pas prises en charge pour les applications JavaScript, qui utilisent plutôt la pile de rendu Web du moteur [EdgeHTML][DevGuideWhatsNew] \ (html, CSS \)</span><span class="sxs-lookup"><span data-stu-id="5567c-188">APIs in the `Windows.UI.Xaml` namespace are not supported for JavaScript apps, which instead use the [EdgeHTML][DevGuideWhatsNew] engine web rendering stack \(HTML, CSS\)</span></span>  

<span data-ttu-id="5567c-189">Pour plus d’informations, consultez [utilisation de Windows Runtime en JavaScript][WindowRuntimeUsingJavascript].</span><span class="sxs-lookup"><span data-stu-id="5567c-189">For more details, see [Using the Windows Runtime in JavaScript][WindowRuntimeUsingJavascript].</span></span>  

### <span data-ttu-id="5567c-190">Exemples de code UWP</span><span class="sxs-lookup"><span data-stu-id="5567c-190">UWP code samples</span></span>  

<span data-ttu-id="5567c-191">Consultez les exemples de code de la [plateforme Windows universelle (UWP \)][MicrosoftDeveloperWindowsSamples] référentiel samples pour parcourir les exemples JavaScript pour les scénarios d’application Windows 10 courants.</span><span class="sxs-lookup"><span data-stu-id="5567c-191">Check out the [Universal Windows Platform \(UWP\) Code Samples][MicrosoftDeveloperWindowsSamples] repo to browse JavaScript examples for common Windows 10 app scenarios.</span></span>  <span data-ttu-id="5567c-192">Bien que les versions JS de ces exemples utilisent la bibliothèque [WinJS][GithubWinjsWinjs] pour structurer le modèle d’exemple, WinJS n’est pas requis pour l’envoi des demandes d’API WinRT illustrées dans ces exemples.</span><span class="sxs-lookup"><span data-stu-id="5567c-192">Although the JS versions of these samples use the [WinJS][GithubWinjsWinjs] library to structure the sample template, WinJS is not required for sending the WinRT API requests demonstrated in these samples.</span></span>  

> [!NOTE]
> <span data-ttu-id="5567c-193">Si vous devez écouter l' [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] événement de l’application, vous pouvez le faire à l’aide de l’API WinRT Native suivante:</span><span class="sxs-lookup"><span data-stu-id="5567c-193">If you need to listen for the [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] event for the app, you are able to do this using the following native WinRT API:</span></span>  
> 
> **<span data-ttu-id="5567c-194">Utilisez cette</span><span class="sxs-lookup"><span data-stu-id="5567c-194">Use this</span></span>**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> <span data-ttu-id="5567c-195">... Contrairement à ce type de requête WinJS utilisée dans les exemples:</span><span class="sxs-lookup"><span data-stu-id="5567c-195">... as opposed this type of WinJS request used in the samples:</span></span>  
> 
> **<span data-ttu-id="5567c-196">Non</span><span class="sxs-lookup"><span data-stu-id="5567c-196">Not this</span></span>**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## <span data-ttu-id="5567c-197">Envoyer des demandes d’API WinRT à partir de votre PWA (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="5567c-197">Send WinRT API requests from your PWA (EdgeHTML)</span></span>  

<span data-ttu-id="5567c-198">À ce stade, imaginons que vous vouliez ajouter un menu contextuel personnalisé pour les utilisateurs Windows de notre PWA \ (EdgeHTML \) et avoir identifié les API dont vous avez besoin dans l’espace de noms [Windows. UI. Popup][UwpApiWindowsUiPopups] .</span><span class="sxs-lookup"><span data-stu-id="5567c-198">At this point, pretend you want to add a custom context menu for Windows users of our PWA \(EdgeHTML\) and have identified the APIs you need in the [Windows.UI.Popups][UwpApiWindowsUiPopups] namespace.</span></span>  

<span data-ttu-id="5567c-199">Pour envoyer des demandes d’API WinRT à partir de notre PWA \ (EdgeHTML \), vous devez tout d’abord [établir les autorisations requises](#set-application-content-uri-rules-acurs) (ou les règles URI de contenu de l’application \) dans le manifeste du package d’application Windows `.appxmanifest` .</span><span class="sxs-lookup"><span data-stu-id="5567c-199">In order to send any WinRT APIs requests from our PWA \(EdgeHTML\), you first need to [establish the requisite permissions](#set-application-content-uri-rules-acurs) \(or, Application Content URI Rules\) in your Windows app package manifest \(`.appxmanifest`\) file.</span></span>  

<span data-ttu-id="5567c-200">Si l’une de ces requêtes d’API implique l’accès à des ressources utilisateur telles que des images ou de la musique, ou à des fonctionnalités d’appareil comme la caméra ou le microphone, vous devez également ajouter des [déclarations de fonctionnalités d’application](#app-capability-declarations) au manifeste du package de l’application afin que Windows puisse lui demander une autorisation.</span><span class="sxs-lookup"><span data-stu-id="5567c-200">If any of these API requests involve access to user resources like pictures or music, or to device features like the camera or microphone, you also need to add [app capability declarations](#app-capability-declarations) to the app package manifest in order for Windows to prompt the user for permission.</span></span>  <span data-ttu-id="5567c-201">Par la suite, si vous publiez votre version d’Outlook. Outlook sur le Microsoft Store, les [autorisations d’application][MicrosoftSupportWindowsAppPermissions] requises sont également indiquées dans votre description dans le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5567c-201">If you later publish your PWA \(EdgeHTML\) to the Microsoft Store, these required [App permissions][MicrosoftSupportWindowsAppPermissions] are also noted in your store listing.</span></span>  

#### <span data-ttu-id="5567c-202">Définir les règles URI de contenu de l’application (règles acur)</span><span class="sxs-lookup"><span data-stu-id="5567c-202">Set Application Content URI Rules (ACURs)</span></span>  

<span data-ttu-id="5567c-203">Par le biais des règles acur, également appelées liste des URL autorisées, vous pouvez donner aux URL de votre PWA \ (EdgeHTML \) un accès direct aux API Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="5567c-203">Through ACURs, otherwise known as a URL allow list, you are able to give the URLs of your PWA \(EdgeHTML\) direct access to Windows Runtime APIs.</span></span>  <span data-ttu-id="5567c-204">Au niveau du système d’exploitation Windows, des limites de stratégie appropriées ont été définies pour autoriser le code hébergé sur votre serveur Web à envoyer des demandes d’API de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="5567c-204">At the Windows OS level, the right policy bounds are set to allow code hosted on your web server to directly send platform API requests.</span></span>  <span data-ttu-id="5567c-205">Vous définissez ces limites dans le fichier manifeste du package d’application quand vous spécifiez les URL de Project Web App `ApplicationContentUriRules` .</span><span class="sxs-lookup"><span data-stu-id="5567c-205">You define these bounds in the app package manifest file when you specify your PWA URLs as `ApplicationContentUriRules`.</span></span>  

<span data-ttu-id="5567c-206">Vos règles doivent inclure la page de démarrage de votre application et toutes les autres pages que vous souhaitez inclure en tant que pages de l’application.</span><span class="sxs-lookup"><span data-stu-id="5567c-206">Your rules should include the start page for your app and any other pages you want included as app pages.</span></span>  <span data-ttu-id="5567c-207">Si votre utilisateur navigue vers une URL qui n’est pas incluse dans vos règles, Windows ouvre l’URL cible dans le navigateur Microsoft Edge plutôt que la fenêtre autonome PWA \ (EdgeHTML \) `WWAHost.exe` .</span><span class="sxs-lookup"><span data-stu-id="5567c-207">If your user navigates to a URL that is not included in your rules, Windows opens the target URL in the Microsoft Edge browser rather than your standalone PWA \(EdgeHTML\) window \(`WWAHost.exe` process\).</span></span>  <span data-ttu-id="5567c-208">Vous pouvez également exclure des URL spécifiques.</span><span class="sxs-lookup"><span data-stu-id="5567c-208">You may also exclude specific URLs.</span></span>  

<span data-ttu-id="5567c-209">Il existe plusieurs façons de spécifier une URL `Match` dans vos règles:</span><span class="sxs-lookup"><span data-stu-id="5567c-209">There are several ways to specify a URL `Match` in your rules:</span></span>  

*   <span data-ttu-id="5567c-210">Nom d’hôte exact</span><span class="sxs-lookup"><span data-stu-id="5567c-210">An exact hostname</span></span>  
*   <span data-ttu-id="5567c-211">Nom d’hôte sur la base duquel inclure ou exclure tout URI contenant un sous-domaine de ce nom d’hôte.</span><span class="sxs-lookup"><span data-stu-id="5567c-211">A hostname for which a URI with any subdomain of that hostname is included or excluded</span></span>  
*   <span data-ttu-id="5567c-212">URI exact</span><span class="sxs-lookup"><span data-stu-id="5567c-212">An exact URI</span></span>  
*   <span data-ttu-id="5567c-213">URI exact contenant une propriété de requête</span><span class="sxs-lookup"><span data-stu-id="5567c-213">An exact URI containing a query property</span></span>  
*   <span data-ttu-id="5567c-214">Chemin d’accès partiel et caractère générique permettant d’indiquer une extension de fichier particulière pour une règle d’inclusion.</span><span class="sxs-lookup"><span data-stu-id="5567c-214">A partial path and a wildcard to indicate a particular file extension for an include rule</span></span>  
*   <span data-ttu-id="5567c-215">Chemins d’accès relatifs pour les règles d’exclusion</span><span class="sxs-lookup"><span data-stu-id="5567c-215">Relative paths for exclude rules</span></span>  

<span data-ttu-id="5567c-216">Voici quelques exemples de règles acur dans un `.appxmanifest` fichier:</span><span class="sxs-lookup"><span data-stu-id="5567c-216">Here are a few examples of ACURs in a `.appxmanifest` file:</span></span>  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

<span data-ttu-id="5567c-217">Les URL définies dans règles acur pour votre application peuvent être accordées à Windows Runtime par le biais de l' `WindowsRuntimeAccess` attribut, qui accepte les valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="5567c-217">URLs defined within the ACURs for your app are able to be granted permission to the Windows Runtime through the `WindowsRuntimeAccess` attribute, which accepts the following values:</span></span>  

*   `all`<span data-ttu-id="5567c-218">: Le code JavaScript distant dispose d’un accès à toutes les API WinRT et composants empaquetés locaux.</span><span class="sxs-lookup"><span data-stu-id="5567c-218">: Remote JavaScript code has access to all WinRT APIs and any local packaged components.</span></span>  <span data-ttu-id="5567c-219">L’espace de noms [Windows \ (WinRT \))][UwpApiIndex] est injecté et présent dans le moteur de script.</span><span class="sxs-lookup"><span data-stu-id="5567c-219">The [Windows \(WinRT\))][UwpApiIndex] namespace is injected and present in the script engine.</span></span>  
*   `allowForWeb`<span data-ttu-id="5567c-220">: L’accès au code JavaScript distant est limité aux composants empaquetés locaux, y compris aux composants C++/C # personnalisés.</span><span class="sxs-lookup"><span data-stu-id="5567c-220">: Remote JavaScript code access is limited to local packaged components, including custom C++/C# components.</span></span>  
*   `none`<span data-ttu-id="5567c-221">Définie.</span><span class="sxs-lookup"><span data-stu-id="5567c-221">: Default.</span></span>  <span data-ttu-id="5567c-222">L’URL spécifiée n’a pas d’accès à la plateforme.</span><span class="sxs-lookup"><span data-stu-id="5567c-222">The specified URL has no platform access.</span></span>  

<span data-ttu-id="5567c-223">Dans ce didacticiel, vous avez déjà défini la seule forme règles ACUR que vous avez besoin de l’étape 6 de la [configuration précédente et](#set-up-and-run-your-universal-windows-app) de l’exécution de la section \) pour votre application d’une seule page.</span><span class="sxs-lookup"><span data-stu-id="5567c-223">In this tutorial, you already set the only ACUR that you need \(Step 6 of the previous [Set up and run your app](#set-up-and-run-your-universal-windows-app) section\) for your single-page app.</span></span>  <span data-ttu-id="5567c-224">Vous pouvez confirmer cela dans le volet des **URI de contenu** du concepteur Visual Studio `package.appxmanifest` .</span><span class="sxs-lookup"><span data-stu-id="5567c-224">You are able to confirm this from the **Content URIs** panel of the Visual Studio `package.appxmanifest` designer.</span></span>  

![Panneau URI de contenu du concepteur Visual Studio appxmanifest](media/vs-appxmanifest-editor-acurs.png)  

<span data-ttu-id="5567c-226">Vous pouvez également afficher le code XML brut de votre manifeste en cliquant avec le bouton droit sur votre `package.appxmanifest` fichier dans l’Explorateur de solutions de Visual Studio et en sélectionnant **afficher le code** \ ( `F7` \).</span><span class="sxs-lookup"><span data-stu-id="5567c-226">You are also able to view the raw XML of your manifest by right-clicking your `package.appxmanifest` file in Visual Studio Solution Explorer and selecting **View Code** \(`F7`\).</span></span>  <span data-ttu-id="5567c-227">Pour basculer vers le mode concepteur, sélectionnez **afficher le concepteur** \ ( `Shift` + `F7` \).</span><span class="sxs-lookup"><span data-stu-id="5567c-227">To toggle back to the Designer view, select **View Designer** \(`Shift`+`F7`\).</span></span>  

#### <span data-ttu-id="5567c-228">Déclarations des fonctionnalités d’application</span><span class="sxs-lookup"><span data-stu-id="5567c-228">App capability declarations</span></span>  

<span data-ttu-id="5567c-229">Si votre application a besoin d’un accès par programme à des ressources utilisateur telles que des images ou de la musique, ou à des appareils tels qu’une caméra ou un microphone, vous devez inclure les [déclarations de fonctionnalités d’application][WindowsUwpPackagingAppCapabilities] correspondantes dans le fichier manifeste de votre package d’application.</span><span class="sxs-lookup"><span data-stu-id="5567c-229">If your app needs programmatic access to user resources like pictures or music, or to devices like a camera or a microphone, you must include the corresponding [App capability declarations][WindowsUwpPackagingAppCapabilities] in your app package manifest file.</span></span>  <span data-ttu-id="5567c-230">Il existe trois catégories de déclaration de fonctionnalités d’application:</span><span class="sxs-lookup"><span data-stu-id="5567c-230">There are three app capability declaration categories:</span></span>  

*   <span data-ttu-id="5567c-231">Les [fonctionnalités à usage général][WindowsUwpPackagingAppCapabilitiesGeneralUse] qui s’appliquent aux scénarios d’application les plus courants.</span><span class="sxs-lookup"><span data-stu-id="5567c-231">[General-use capabilities][WindowsUwpPackagingAppCapabilitiesGeneralUse] that apply to most common app scenarios.</span></span>  
*   <span data-ttu-id="5567c-232">Les [fonctionnalités d’appareil][WindowsUwpPackagingAppCapabilitiesDevice] qui permettent à votre application d’accéder à des périphériques et à des dispositifs internes.</span><span class="sxs-lookup"><span data-stu-id="5567c-232">[Device capabilities][WindowsUwpPackagingAppCapabilitiesDevice] that allow your app to access peripheral and internal devices.</span></span>  
*   <span data-ttu-id="5567c-233">[Fonctionnalités à usage spécial][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] qui prennent en charge les scénarios d’entreprise et qui nécessitent un compte d’entreprise Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5567c-233">[Special-use capabilities][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] that support enterprise scenarios and require a Microsoft Store company account.</span></span>  <span data-ttu-id="5567c-234">Pour plus d’informations sur les comptes d’entreprise, voir [Types de compte, emplacements et frais][WindowsUwpPublishAccountTypesLocationsFees].</span><span class="sxs-lookup"><span data-stu-id="5567c-234">For more info about company accounts, see [Account types, locations, and fees][WindowsUwpPublishAccountTypesLocationsFees].</span></span>

<span data-ttu-id="5567c-235">La page de votre application Microsoft Store répertorie toutes les fonctions que vous déclarez dans le manifeste de votre package d’application, vous devez donc spécifier uniquement les fonctionnalités utilisées réellement par votre application.</span><span class="sxs-lookup"><span data-stu-id="5567c-235">Your Microsoft Store app page lists all the capabilities you declare in your app package manifest, so be sure to only specify the capabilities that your app actually uses.</span></span>

<span data-ttu-id="5567c-236">Certaines fonctionnalités permettent aux applications d’accéder à des ressources sensibles.</span><span class="sxs-lookup"><span data-stu-id="5567c-236">Some capabilities provide apps access to sensitive resources.</span></span>  <span data-ttu-id="5567c-237">Ces ressources sont considérées comme «sensibles», car chacune peut accéder aux données personnelles de l’utilisateur ou coûter l’argent à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5567c-237">These resources are considered sensitive because each is able to access the user's personal data or cost the user money.</span></span>  <span data-ttu-id="5567c-238">Paramètres de confidentialité, gérés par l’application [paramètres][BingResultsWindows10Settings] Windows 10, permet à l’utilisateur de contrôler de façon dynamique l’accès aux ressources sensibles.</span><span class="sxs-lookup"><span data-stu-id="5567c-238">Privacy settings, managed by the Windows 10 [Settings][BingResultsWindows10Settings] app, let the user dynamically control access to sensitive resources.</span></span>  <span data-ttu-id="5567c-239">Par conséquent, il est important que votre application ne présume pas qu’une ressource sensible est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="5567c-239">Thus, it is important that your app does not assume a sensitive resource is always available.</span></span>  <span data-ttu-id="5567c-240">Pour plus d’informations sur l’accès aux ressources sensibles, voir [Recommandations en matière d’applications prenant en charge la confidentialité][WindowsUwp|::ref2::|Index].</span><span class="sxs-lookup"><span data-stu-id="5567c-240">For more info about accessing sensitive resources, see [Guidelines for privacy-aware apps][WindowsUwp|::ref2::|Index].</span></span>  

<span data-ttu-id="5567c-241">Vous pouvez demander l’accès en déclarant les fonctionnalités dans le manifeste du package de votre application.</span><span class="sxs-lookup"><span data-stu-id="5567c-241">You request access by declaring capabilities in the package manifest for your app.</span></span>  <span data-ttu-id="5567c-242">Dans Visual Studio, vous pouvez effectuer cette opération à partir du volet **capacités** du concepteur package. appxmanifest.</span><span class="sxs-lookup"><span data-stu-id="5567c-242">In Visual Studio, you are able to do this from the **Capabilities** panel of the package.appxmanifest designer.</span></span>  

![Panneau capacités du concepteur Visual Studio appxmanifest](media/vs-appxmanifest-editor-capabilities.png)  

<span data-ttu-id="5567c-244">Dans ce didacticiel, seule la fonctionnalité Internet (client) par défaut est requise, donc aucune action supplémentaire n’est requise.</span><span class="sxs-lookup"><span data-stu-id="5567c-244">In this tutorial, only the default Internet \(Client\) capability is required, so no further action is needed.</span></span>  

### <span data-ttu-id="5567c-245">Utiliser la détection de fonctionnalités pour appeler WinRT</span><span class="sxs-lookup"><span data-stu-id="5567c-245">Use feature detection to invoke WinRT</span></span>  

<span data-ttu-id="5567c-246">Pour garantir une connaissance de base de qualité pour votre public sur toutes les plateformes, vous améliorez progressivement votre utilisation de Project Web App à l’aide de la fonctionnalité de détection des fonctionnalités WinRT.</span><span class="sxs-lookup"><span data-stu-id="5567c-246">To ensure a quality baseline experience for your PWA audience across all platforms, you progressively enhance your PWA experience on Windows using WinRT feature detection.</span></span>  <span data-ttu-id="5567c-247">De cette façon, vous pouvez être sûr que votre code spécifique à Windows s’exécute uniquement dans un contexte où les API WinRT sont disponibles et applicables.</span><span class="sxs-lookup"><span data-stu-id="5567c-247">This way, you are able to be sure your Windows-specific code is only run in a context where WinRT APIs are available and applicable.</span></span>  

<span data-ttu-id="5567c-248">Pour détecter les fonctionnalités, il est possible de rechercher en tant qu' `Windows` objet \ (le point d’entrée vers l' [espace de noms WinRT][UwpApiIndex]\) comme suit:</span><span class="sxs-lookup"><span data-stu-id="5567c-248">Feature detection may be as simple as looking for the `Windows` object \(the entrypoint to the [WinRT namespace][UwpApiIndex]\) as below:</span></span>  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="5567c-249">Toutefois, étant donné que toutes les API Windows ne sont pas disponibles sur tous les [types d’appareils Windows 10][UwpExtensionSdkDeviceFamiliesOverview], il est généralement utile d’utiliser une détection de fonctionnalités plus spécifique pour qualifier davantage l’espace de noms de la requête d’API que vous envoyez:</span><span class="sxs-lookup"><span data-stu-id="5567c-249">However, given that not all Windows APIs are available on all [Windows 10 device types][UwpExtensionSdkDeviceFamiliesOverview], it is generally useful to use more specific feature detection to further qualify the namespace of the API request you are sending:</span></span>  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="5567c-250">Avec cet arrière-plan, vous pouvez ajouter du code WinRT pour implémenter un menu contextuel personnalisé.</span><span class="sxs-lookup"><span data-stu-id="5567c-250">With that background, you are ready to add some WinRT code to implement a custom context menu.</span></span>  <span data-ttu-id="5567c-251">Si vous utilisez l’exemple de Project Web App à partir de [prise en main des applications Web progressives][PwaGetStarted]:</span><span class="sxs-lookup"><span data-stu-id="5567c-251">If you are using the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted]:</span></span>

1.  <span data-ttu-id="5567c-252">Ouvrez Visual Studio pour votre projet de site Project Web App.</span><span class="sxs-lookup"><span data-stu-id="5567c-252">Open Visual Studio to your PWA site project.</span></span>

1.  <span data-ttu-id="5567c-253">Dans l’Explorateur de solutions, ouvrez le `views\layout.pug` fichier et ajoutez la ligne suivante, juste en dessous de la `script` référence de votre travailleur de service:</span><span class="sxs-lookup"><span data-stu-id="5567c-253">In Solution Explorer, open the `views\layout.pug` file and add the following line, right below the `script` reference for your service worker:</span></span>
    
    ```xml
    script(src='/javascripts/site.js')
    ```  

1.  <span data-ttu-id="5567c-254">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le `javascripts` dossier et **Ajoutez**  >  **nouveau fichier...**.</span><span class="sxs-lookup"><span data-stu-id="5567c-254">In Solution Explorer, right-click on the `javascripts` folder and **Add** > **New File...**.</span></span>

1.  <span data-ttu-id="5567c-255">Nommez votre fichier `site.js` , puis copiez-le dans le code suivant:</span><span class="sxs-lookup"><span data-stu-id="5567c-255">Name your file: `site.js`, and copy in the following code:</span></span>
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```

1.  <span data-ttu-id="5567c-256">Comparez le comportement du menu contextuel lors de l’exécution de votre PWA dans le navigateur \ ( `F5` à partir du projet de site PWA \) plutôt que dans la fenêtre de l’application Windows ( `F5` à partir de votre projet d’application Windows universelle \).</span><span class="sxs-lookup"><span data-stu-id="5567c-256">Compare the context menu behavior when you run your PWA in the browser \(`F5` from your PWA site project\) versus from inside the Windows app window \(`F5` from your Universal Windows app project\).</span></span>  <span data-ttu-id="5567c-257">Dans le navigateur, le fait de cliquer avec le bouton droit vous permet d’accéder au menu contextuel de Microsoft Edge par défaut, alors que dans le `WWAHost.exe` processus, votre menu personnalisé apparaît désormais.</span><span class="sxs-lookup"><span data-stu-id="5567c-257">In the browser, right-clicking gives you the Microsoft Edge default context menu, whereas in the `WWAHost.exe` process, your custom menu now appears.</span></span>  

    | <span data-ttu-id="5567c-258">MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="5567c-258">Microsoft Edge</span></span> | <span data-ttu-id="5567c-259">Application Windows 10</span><span class="sxs-lookup"><span data-stu-id="5567c-259">Windows 10 app</span></span> |  
    |:--- |:---- |  
    | ![Menu contextuel par défaut du navigateur](media/browser-context-menu.png) | ![Menu contextuel personnalisé de l’application](media/app-context-menu.png) |  

<span data-ttu-id="5567c-262">J’espère que vous avez à présent une base solide pour améliorer votre PWAs sur Windows.</span><span class="sxs-lookup"><span data-stu-id="5567c-262">Hopefully you now have a solid foundation for progressively enhancing your PWAs on Windows.</span></span>  <span data-ttu-id="5567c-263">Si vous rencontrez des questions ou quelque chose n’est pas clair, envoyez-nous un commentaire!</span><span class="sxs-lookup"><span data-stu-id="5567c-263">If you run into questions or anything is unclear, please send a comment!</span></span>  

## <span data-ttu-id="5567c-264">Aller plus loin</span><span class="sxs-lookup"><span data-stu-id="5567c-264">Going further</span></span>

<span data-ttu-id="5567c-265">Le [Centre de développement Windows][MicrosoftDeveloperWindowsApps] est votre référence complète pour toutes les phases du bâtiment d’applications Windows, de la [mise][MicrosoftDeveloperWindowsAppsGetStarted]en route à la [conception][MicrosoftDeveloperWindowsAppsDesign], du [développement][MicrosoftDeveloperWindowsAppsDevelop]et de la [publication][MicrosoftDeveloperStorePublishApps] sur le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5567c-265">The [Windows Dev Center][MicrosoftDeveloperWindowsApps] is your complete reference for all stages of Windows app building, from [getting started][MicrosoftDeveloperWindowsAppsGetStarted], to [designing][MicrosoftDeveloperWindowsAppsDesign], [developing][MicrosoftDeveloperWindowsAppsDevelop], and [publishing][MicrosoftDeveloperStorePublishApps] to the Microsoft Store.</span></span>  

<span data-ttu-id="5567c-266">Pour obtenir une vue d’ensemble générale de la plateforme Windows universelle (UWP) et de la manière de cibler différentes familles d’appareils Windows 10, voir [Présentation de la plateforme Windows universelle][WindowsUWPGetStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="5567c-266">For a general overview on the Universal Windows Platform \(UWP\) and how to target different Windows 10 device families, see [Intro to the Universal Windows Platform][WindowsUWPGetStartedGuide].</span></span>  

<span data-ttu-id="5567c-267">Lorsque vous êtes prêt, voici comment \ (et pourquoi! \) pour [transmettre votre document PWA au Microsoft Store](./microsoft-store.md).</span><span class="sxs-lookup"><span data-stu-id="5567c-267">And when you are ready, here is how \(and why!\) to [Submit your PWA to the Microsoft Store](./microsoft-store.md).</span></span>  

<!-- image links -->  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Découvrir les applications Web progressives"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs sur Windows 10 (EdgeHTML)-applications Web progressives sur Windows"  
[DevToolsGuide]: ../devtools-guide.md "Outils de développement Microsoft Edge (EdgeHTML)"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide.md#microsoft-store-app "Application Microsoft Store App-Microsoft Edge (EdgeHTML)-outils de développement"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Travailleurs de service"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clients du protocole Microsoft Edge DevTools Preview-DevTools"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Nouveautés de EdgeHTML"  
[WindowsRuntime]: ../windows-runtime/index.md "Windows Runtime (WinRT) pour JavaScript"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Utilisation de Windows Runtime en JavaScript"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Gestion des événements Windows Runtime en JavaScript"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Utilisation de méthodes asynchrones Windows Runtime"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Conventions de casse avec les fonctionnalités Windows Runtime-utilisation de Windows Runtime en JavaScript"  
[UwpApiIndex]: /uwp/api/index "Espaces de noms UWP Windows"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Espace de noms Windows. UI. Popup"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "Événement WebUIApplication. Activated"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Présentation de la famille d’appareils"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "Comment Visual Studio génère un manifeste de package d’application"  
[WindowsUWPIndex]: /windows/uwp/index "Documentation de la plateforme Windows universelle"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "Qu’est-ce qu’une application de plateforme Windows universelle (UWP)?"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Activer votre appareil pour le développement"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Sûreté"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Types de compte, emplacements et frais"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Fonctionnalités restreintes"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Fonctionnalités de l’appareil"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Fonctionnalités à usage général"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "Déclarations des fonctionnalités d’application"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "paramètres Windows 10-Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "winjs/winjs | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Publier des applications et des jeux Windows"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Documentation de la plateforme Windows universelle"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Concevoir et coder des applications Windows"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Développer des applications UWP"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Découvrir les applications Windows 10"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Exemples de code"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Microsoft Edge DevTools preview"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "Autorisations des applications"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Téléchargements"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Visual Studio preview"  
