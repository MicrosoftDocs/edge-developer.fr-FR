---
description: Ce guide vous donne une vue d’ensemble des notions de base et des outils de Project Web App pour créer des applications Web progressives sur Windows.
title: Découvrir les applications Web progressives
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, PWABuilder, le manifeste Web, le travailleur de service, l’émission
ms.date: 12/02/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 9a76399616ab7645b82242b94dd4757b73b37f60
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232796"
---
# <span data-ttu-id="00af1-104">Découvrir les applications Web progressives</span><span class="sxs-lookup"><span data-stu-id="00af1-104">Get started with Progressive Web Apps</span></span>  

<span data-ttu-id="00af1-105">Les applications Web progressives \(PWAs \) sont simplement des applications Web qui ont été [améliorées][WikiProgressiveEnhancement] avec les fonctionnalités de type application native sur la prise en charge des plateformes et des moteurs de navigateur, tels que les installations de lancement à partir de écran d’accueil, la prise en charge hors ligne et les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="00af1-105">Progressive Web Apps \(PWAs\) are simply web apps that are [progressively enhanced][WikiProgressiveEnhancement] with native app-like features on supporting platforms and browser engines, such as launch-from-homescreen installation, offline support, and push notifications.</span></span>  <span data-ttu-id="00af1-106">Sur Windows 10 avec le moteur Microsoft Edge \(EdgeHTML \), PWAs Profitez de l’avantage supplémentaire de s’exécuter indépendamment de la fenêtre du navigateur en tant qu’applications pour la [plateforme Windows universelle][WindowsUwpGetStartedWhat] .</span><span class="sxs-lookup"><span data-stu-id="00af1-106">On Windows 10 with the Microsoft Edge \(EdgeHTML\) engine, PWAs enjoy the added advantage of running independently of the browser window as [Universal Windows Platform][WindowsUwpGetStartedWhat] apps.</span></span>  

<span data-ttu-id="00af1-107">Ce guide vous donne une vue d’ensemble des concepts de base de la création d’une `localhost` application Web à l’aide de Microsoft Visual Studio et de certains utilitaires de création de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="00af1-107">This guide gives you an overview of PWA basics by building a simple `localhost` web app as a PWA using Microsoft Visual Studio and some PWA Builder utilities.</span></span>  <span data-ttu-id="00af1-108">Le produit fini fonctionne de la même manière dans tous les navigateurs qui prennent en charge PWAs.</span><span class="sxs-lookup"><span data-stu-id="00af1-108">The finished product works similarly across any browser that supports PWAs.</span></span>  

> [!TIP]
> <span data-ttu-id="00af1-109">Pour obtenir une méthode rapide de conversion d’un site existant dans un fichier PWA et de package pour Windows 10 et d’autres plateformes d’application, consultez le [Générateur PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="00af1-109">For a quick way to convert an existing site to a PWA and package it for Windows 10 and other app platforms, review [PWA Builder][PwaBuilder].</span></span>  

## <span data-ttu-id="00af1-110">Prérequis</span><span class="sxs-lookup"><span data-stu-id="00af1-110">Prerequisites</span></span>  

<span data-ttu-id="00af1-111">Vous pouvez générer PWAs avec n’importe quel éditeur de développement Web.</span><span class="sxs-lookup"><span data-stu-id="00af1-111">You may build PWAs with any web development IDE.</span></span>  <span data-ttu-id="00af1-112">Vous trouverez ci-après les conditions préalables pour ce guide, qui vous guident dans la prise en charge des outils de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="00af1-112">The following are only prerequisites for this guide, which walks you through PWA tooling support in the Windows developer ecosystem.</span></span>  

*   <span data-ttu-id="00af1-113">Téléchargez la [communauté 2017 Visual Studio Community][VisualStudioDownloads].</span><span class="sxs-lookup"><span data-stu-id="00af1-113">Download the \(free\) [Visual Studio Community 2017][VisualStudioDownloads].</span></span>  <span data-ttu-id="00af1-114">Vous pouvez également utiliser les éditions professionnel, entreprise ou [preview][VisualStudioPreview] .</span><span class="sxs-lookup"><span data-stu-id="00af1-114">You may also use the Professional, Enterprise, or [Preview][VisualStudioPreview] editions.</span></span>  <span data-ttu-id="00af1-115">Dans le programme d’installation de Visual Studio, choisissez les charges de travail suivantes.</span><span class="sxs-lookup"><span data-stu-id="00af1-115">From the Visual Studio Installer, choose the following Workloads.</span></span>  
    
    *   **<span data-ttu-id="00af1-116">Développement de plateforme Windows universelle</span><span class="sxs-lookup"><span data-stu-id="00af1-116">Universal Windows Platform development</span></span>**  
    *   **<span data-ttu-id="00af1-117">Développement Node.js</span><span class="sxs-lookup"><span data-stu-id="00af1-117">Node.js development</span></span>**  

## <span data-ttu-id="00af1-118">Configurer une application Web de base</span><span class="sxs-lookup"><span data-stu-id="00af1-118">Set up a basic web app</span></span>  

<span data-ttu-id="00af1-119">Par souci de simplicité, utilisez Visual StudioNode.js et le modèle d' [ application Express][VisualStudioNodeJsTutorial] pour créer `localhost` une application Web qui dessert une `index.html` page.</span><span class="sxs-lookup"><span data-stu-id="00af1-119">For the sake of simplicity, use the Visual Studio [Node.js and Express app][VisualStudioNodeJsTutorial] template to create `localhost` web app that serves up an `index.html` page.</span></span>  <span data-ttu-id="00af1-120">Imaginez qu’il s’agit d’un espace réservé pour l’application Web complète attrayante que vous développez en tant que PWA.</span><span class="sxs-lookup"><span data-stu-id="00af1-120">Imagine this as a placeholder for the compelling, full-featured web app that you are developing as a PWA.</span></span>  

1.  <span data-ttu-id="00af1-121">Lancez Visual Studio et démarrez un nouveau projet.</span><span class="sxs-lookup"><span data-stu-id="00af1-121">Launch Visual Studio, and start a new project.</span></span>  
    *   <span data-ttu-id="00af1-122">**Fichier**  >  **Nouvelle**  >  **Projet...**</span><span class="sxs-lookup"><span data-stu-id="00af1-122">**File** > **New** > **Project...**</span></span>  
    *   `Ctrl`+`Shift`+`N`  
1.  <span data-ttu-id="00af1-123">Sous **JavaScript**, sélectionnez l' **application Basic Node.js Express 4**.</span><span class="sxs-lookup"><span data-stu-id="00af1-123">Under **JavaScript**, select **Basic Node.js Express 4 Application**.</span></span>  <span data-ttu-id="00af1-124">Définissez le nom et l’emplacement, puis sélectionnez **OK**.</span><span class="sxs-lookup"><span data-stu-id="00af1-124">Set the name and location and choose **OK**.</span></span>  
    
    ![Sélection du modèle de projet Node.js Express 4 dans Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  <span data-ttu-id="00af1-126">Après le chargement de votre nouveau projet, sélectionnez **Build** \( `Ctrl` + `Shift` + `B` \) et **Démarrer le débogage** \( `F5` \).</span><span class="sxs-lookup"><span data-stu-id="00af1-126">Once your new project loads, choose **Build** \(`Ctrl`+`Shift`+`B`\) and **Start Debugging** \(`F5`\).</span></span>  <span data-ttu-id="00af1-127">Vérifiez que le `index.html` fichier est chargé lorsque vous naviguez vers `http://localhost:1337` .</span><span class="sxs-lookup"><span data-stu-id="00af1-127">Verify that your `index.html` file loads when you browse to `http://localhost:1337`.</span></span>  
    
    ![Exécution de votre nouveau site sur localhost][ImageVsNodejsExpressIndex]  

## <span data-ttu-id="00af1-129">Transformer votre application en PWA</span><span class="sxs-lookup"><span data-stu-id="00af1-129">Turn your app into a PWA</span></span>  

<span data-ttu-id="00af1-130">Maintenant, il est temps de vous connecter à la [Configuration minimale requise][PwaEdgehtmlIndexRequirements] de base pour votre application Web: manifeste de l' *application Web*, *https* et *travailleurs de service*.</span><span class="sxs-lookup"><span data-stu-id="00af1-130">Now it is time to wire up the basic [PWA requirements][PwaEdgehtmlIndexRequirements] for your web app: a *Web App Manifest*, *HTTPS* and *Service Workers*.</span></span>  

### <span data-ttu-id="00af1-131">Manifeste de l’application Web</span><span class="sxs-lookup"><span data-stu-id="00af1-131">Web App Manifest</span></span>  

<span data-ttu-id="00af1-132">Le [manifeste d’une application Web][MDNWebAppManifest] est un fichier de MÉTADONNÉEs JSON décrivant votre application, y compris le nom, l’auteur, l’URL de la page d’entrée et une ou plusieurs icônes.</span><span class="sxs-lookup"><span data-stu-id="00af1-132">A [Web App Manifest][MDNWebAppManifest] is a JSON metadata file describing your app, including the name, author, entry page URL, and one or more icons.</span></span>  <span data-ttu-id="00af1-133">Dans la mesure où il suit un [schéma normalisé][W3cWebAppManifest], vous devez uniquement fournir un manifeste de l’application Web unique pour le PWA que vous installez sur n’importe quelle plateforme, système d’exploitation et combinaison de périphériques prenant en charge PWAS.</span><span class="sxs-lookup"><span data-stu-id="00af1-133">Because it follows a [standards-based schema][W3cWebAppManifest], you must only supply a single web app manifest for the PWA that you are installing on any platform, OS, and device combination that supports PWAs.</span></span>  <span data-ttu-id="00af1-134">Dans l’écosystème Windows, le manifeste de votre application Web signale à l’indexeur Web de Bing qu’il est candidat pour une inclusion automatique dans le [Microsoft Store][PwaEdgehtmlMicrosoftStore], où il peut arriver qu’il atteigne près de 700 millions utilisateurs d’un mois actif dans le cadre d’une application Windows 10.</span><span class="sxs-lookup"><span data-stu-id="00af1-134">In the Windows ecosystem, your web app manifest signals to the Bing web indexer that your PWA is a candidate for automatic inclusion in the [Microsoft Store][PwaEdgehtmlMicrosoftStore], where it may reach nearly 700 million active monthly users as a Windows 10 app.</span></span>  

<span data-ttu-id="00af1-135">S’il s’agissait d’un site actif existant, vous pouvez générer un manifeste de l’application Web à l’aide du [Générateur PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="00af1-135">If this were an existing live site, you may generate a web app manifest using [PWA Builder][PwaBuilder].</span></span>  <span data-ttu-id="00af1-136">Dans la mesure où il s’agit toujours d’un projet non publié, copiez un exemple de manifeste.</span><span class="sxs-lookup"><span data-stu-id="00af1-136">Since it is still an unpublished project, copy a sample manifest.</span></span>  

1.  <span data-ttu-id="00af1-137">Dans l’Explorateur de *solutions*de Visual Studio, cliquez avec le bouton droit sur le dossier *public* , puis sélectionnez **Ajouter**  >  **un nouveau fichier...**, en spécifiant `manifest.json` le nom de l’élément.</span><span class="sxs-lookup"><span data-stu-id="00af1-137">In the Visual Studio *Solution Explorer*, right-click the *public* folder and select **Add** > **New File...**, specifying `manifest.json` as the item name.</span></span>  
1.  <span data-ttu-id="00af1-138">Dans le `manifest.json` fichier, copiez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="00af1-138">In the `manifest.json` file, copy the following code.</span></span>  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    <span data-ttu-id="00af1-139">Dans un espace de noms réel, l’étape suivante consiste à personnaliser le *nom*, le *start_url*, les *SHORT_NAME*, la *Description*et les *icônes* \(les icônes sont décrites dans l’étape suivante.).</span><span class="sxs-lookup"><span data-stu-id="00af1-139">In a real PWA, the next step is to customize *name*, *start_url*, *short_name*, *description*, and *icons* \(icons are covered in the next step\).</span></span>  
    
    <span data-ttu-id="00af1-140">Pour en savoir plus sur les différentes valeurs des membres et leurs objectifs associés, voir référence du manifeste de l' [application Web][MDNWebAppManifest] .</span><span class="sxs-lookup"><span data-stu-id="00af1-140">To learn more about the different member values and associated purposes, see the [Web App Manifest][MDNWebAppManifest] reference.</span></span>  
    
1.  <span data-ttu-id="00af1-141">Ensuite, remplissez le tableau vide `icons` avec des trajectoires d’image réelles à l’aide du générateur d’image de l’application Project Builder.</span><span class="sxs-lookup"><span data-stu-id="00af1-141">Next, fill in the empty `icons` array with actual image paths by using the PWA Builder App Image Generator.</span></span>  
    
    1.  <span data-ttu-id="00af1-142">À l’aide d’un navigateur Web, téléchargez cet [exemple d’image 512X512 PWA][ImagePwa].</span><span class="sxs-lookup"><span data-stu-id="00af1-142">Using a web browser, download this [sample 512x512 PWA image][ImagePwa].</span></span>  
    1.  <span data-ttu-id="00af1-143">Accédez au [Générateur d’image][PwaBuilderAppImageGenerator]de l’application concepteur PWA, puis sélectionnez l' `pwa.png` image que vous venez d’enregistrer en tant qu' **image d’entrée** , puis cliquez sur le bouton **Télécharger** .</span><span class="sxs-lookup"><span data-stu-id="00af1-143">Go to the PWA Builder [App Image Generator][PwaBuilderAppImageGenerator], and select the `pwa.png` image you just saved as the **Input Image** and then choose the **Download** button.</span></span>  
    1.  <span data-ttu-id="00af1-144">**Ouvrez** et **extrayez** le fichier zip.</span><span class="sxs-lookup"><span data-stu-id="00af1-144">**Open** and **Extract** the zip file.</span></span>  
    1.  <span data-ttu-id="00af1-145">Dans l’Explorateur de solutions de Visual Studio, cliquez avec le bouton droit sur le `public` dossier et **Ouvrez le dossier dans l’Explorateur de fichiers**.</span><span class="sxs-lookup"><span data-stu-id="00af1-145">In the Visual Studio Solution Explorer, right-click the `public` folder and **Open Folder in File Explorer**.</span></span>  <span data-ttu-id="00af1-146">Créer un **dossier** nommé `images` .</span><span class="sxs-lookup"><span data-stu-id="00af1-146">Create a **New folder** named `images`.</span></span>  
    1.  <span data-ttu-id="00af1-147">Copiez tous les dossiers de la plateforme \( `android` , `chrome` , `windows10` et ainsi de suite) à partir de votre code postal extrait dans le `images` dossier, puis fermez la fenêtre de l’Explorateur de fichiers.</span><span class="sxs-lookup"><span data-stu-id="00af1-147">Copy all of the platform folders \(`android`, `chrome`, `windows10`, and so on\) from your extracted zip to the `images` folder and close the file explorer window.</span></span>  <span data-ttu-id="00af1-148">Ajoutez les dossiers à votre projet Visual Studio, dans l’Explorateur de solutions, cliquez avec le bouton droit sur le `images` dossier, puis sélectionnez **Ajouter**un  >  **dossier existant...** pour chacun des dossiers \).</span><span class="sxs-lookup"><span data-stu-id="00af1-148">Add the folders to your Visual Studio project \(in Solution Explorer, right-click `images` folder and select **Add** > **Existing folder...** for each of the folders\).</span></span>  
    1.  <span data-ttu-id="00af1-149">Ouvrez \(avec Visual Studio ou n’importe quel éditeur) le `icons.json` fichier à partir du code postal extrait et copiez le `"icons": [...]` tableau dans le `manifest.json` fichier de votre projet.</span><span class="sxs-lookup"><span data-stu-id="00af1-149">Open \(with Visual Studio or any editor\) the `icons.json` file from the extracted zip and copy the `"icons": [...]` array into the `manifest.json` file of your project.</span></span>  

1.  <span data-ttu-id="00af1-150">Vous devez maintenant associer le manifeste de votre application Web à votre application.</span><span class="sxs-lookup"><span data-stu-id="00af1-150">Now you must associate your web app manifest with your app.</span></span>  <span data-ttu-id="00af1-151">Ouvrez le `layout.pug` fichier \(dans le `views` dossier \) pour le modifier, puis ajoutez cette ligne juste après le lien de la feuille de style.</span><span class="sxs-lookup"><span data-stu-id="00af1-151">Open the `layout.pug` file \(in `views` folder\) for editing, and add this line right after the stylesheet link.</span></span>  <span data-ttu-id="00af1-152">\(Il s’agit simplement du nœud [Pug][PugAttributes] de gabarit pour `<link rel='manifest' href='/manifest.json'>` \).</span><span class="sxs-lookup"><span data-stu-id="00af1-152">\(It is simply the Node [pug][PugAttributes] template shorthand for `<link rel='manifest' href='/manifest.json'>`\).</span></span>  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
<span data-ttu-id="00af1-153">Lorsque vous avez terminé, votre application Web utilise désormais une icône de manifeste et d’application écran d’accueil.</span><span class="sxs-lookup"><span data-stu-id="00af1-153">With all that in place, your web app is now serving up a manifest and homescreen-ready app icons!</span></span>  <span data-ttu-id="00af1-154">Essayez d’exécuter votre application \( `F5` \) et de charger le manifeste.</span><span class="sxs-lookup"><span data-stu-id="00af1-154">Try running your app \(`F5`\) and loading up the manifest.</span></span>  

![Chargement du manifeste de l’application Web à partir de localhost][ImageVsNodejsExpressManifest]  

<span data-ttu-id="00af1-156">Et l’une de vos icônes.</span><span class="sxs-lookup"><span data-stu-id="00af1-156">And one of your icons.</span></span>  

![Chargement du logo de l’application Square71x71Logo à partir de localhost][ImageVsNodejsExpressIcon]  

<span data-ttu-id="00af1-158">Si vous publiez l’application Live \(avec un `start_url` \), le moteur de recherche Bing le considère désormais comme un candidat pour [le Packaging automatique et la soumission à la boutique Microsoft][PwaEdgehtmlMicrosoftStore] en tant qu’application Windows 10 installable.</span><span class="sxs-lookup"><span data-stu-id="00af1-158">If you publish the app live \(with an actual `start_url`\), the Bing search engine now identifies it as a candidate for [automatic packaging and submission to the Microsoft Store][PwaEdgehtmlMicrosoftStore] as an installable Windows 10 app.</span></span>  <span data-ttu-id="00af1-159">Assurez-vous que votre manifest.jsdans le fichier inclut les [signaux de qualité pour les applications Web progressives][WindowsBlogsPwaEdge] pour lesquelles Bing analyse Bing, y compris les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="00af1-159">Ensure that your manifest.json file includes the [Quality signals for Progressive Web Apps][WindowsBlogsPwaEdge] for which Bing scans including the following items.</span></span>   

*   `name`  
*   `description`  
*   <span data-ttu-id="00af1-160">Au moins une icône 512px carré ou supérieur \(pour garantir la résolution de l’écran de démarrage de votre application dans le Windows Store, la description de votre application dans le Windows Store, l’image de la vignette, etc.).</span><span class="sxs-lookup"><span data-stu-id="00af1-160">At least one icon 512px square or larger \(to ensure an image source of sufficient resolution for auto-generating the splash screen of your app, store listing, tile image, and so on\).</span></span>  

<span data-ttu-id="00af1-161">Par ailleurs [, utilisez les](#https) [prestataires de services](#service-workers)et les politiques du Windows [Store][LegalWindowsAgrementsMicrosoftStorePolicies].</span><span class="sxs-lookup"><span data-stu-id="00af1-161">In addition, use [HTTPS](#https), [service workers](#service-workers), and comply with [Microsoft Store Policies][LegalWindowsAgrementsMicrosoftStorePolicies].</span></span>  

### <span data-ttu-id="00af1-162">HTTPS</span><span class="sxs-lookup"><span data-stu-id="00af1-162">HTTPS</span></span>  

<span data-ttu-id="00af1-163">[Les travailleurs de services][MDNServiceWorkerApi] et autres technologies PWA clés qui fonctionnent avec des travailleurs de service (par exemple, les API de synchronisation [en cache][MDNCache], de [transmission][MDNPushApi]et en [arrière-plan][MDNSyncManager] ) ne fonctionnent que sur des connexions sécurisées, ce qui signifie [https][WikiHttps] pour les sites dynamiques ou `localhost` à des fins de débogage.</span><span class="sxs-lookup"><span data-stu-id="00af1-163">[Service Workers][MDNServiceWorkerApi] and other key PWA technologies that work with service workers \(such as the [Cache][MDNCache], [Push][MDNPushApi], and [Background Sync][MDNSyncManager] APIs\) only work across secure connections, which means [HTTPS][WikiHttps] for live sites or `localhost` for debugging purposes.</span></span>  

<span data-ttu-id="00af1-164">Si vous [publiez cette application Web en tant que site actif][VisualStudioNodejsTutorialPublishAzureAppService] , vous devez vous assurer que votre [][AzureCreateFreeAccount]serveur est configuré pour la configuration de votre serveur pour http</span><span class="sxs-lookup"><span data-stu-id="00af1-164">If you [publish this web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="00af1-165">Si vous utilisez le [service Microsoft Azure App][AzureWebApps] pour héberger votre site, il est desservi par défaut par défaut.</span><span class="sxs-lookup"><span data-stu-id="00af1-165">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="00af1-166">Pour ce guide, continuez à utiliser `http://localhost` en tant qu’espace réservé pour un site actif `https://` .</span><span class="sxs-lookup"><span data-stu-id="00af1-166">For this guide, continue using `http://localhost` as a placeholder for a live site served over `https://`.</span></span>  

### <span data-ttu-id="00af1-167">Worker du service</span><span class="sxs-lookup"><span data-stu-id="00af1-167">Service Workers</span></span>  

<span data-ttu-id="00af1-168">Les travailleurs de service constituent la technologie clé en coulisse de PWAs.</span><span class="sxs-lookup"><span data-stu-id="00af1-168">Service Workers is the key technology behind PWAs.</span></span> <span data-ttu-id="00af1-169">Les travailleurs de service agissent en tant que proxy entre votre PWA et votre réseau pour permettre à votre site Web de fonctionner en tant qu’application native installée qui gère les scénarios hors connexion, répond aux notifications de transmission de serveur et exécute des tâches en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="00af1-169">Service Workers act as a proxy between your PWA and the network to enable your website to function as an installed native app that serves up offline scenarios, responds to server push notifications, and runs background tasks.</span></span>  <span data-ttu-id="00af1-170">Les travailleurs de service ouvrent également de nouvelles stratégies de performance.</span><span class="sxs-lookup"><span data-stu-id="00af1-170">Service workers also open up new performance strategies.</span></span>  <span data-ttu-id="00af1-171">Vous n’êtes pas tenu de mettre en œuvre une application Web complète pour utiliser le cache du travailleur du service pour améliorer les performances de chargement de page de votre site Web.</span><span class="sxs-lookup"><span data-stu-id="00af1-171">You are not required to implement a full web app to use the service worker cache for fine-tuned page load performance for your website.</span></span>  

<span data-ttu-id="00af1-172">Les travailleurs de service sont des threads d’arrière-plan pilotés par des événements qui s’exécutent à partir de fichiers JavaScript servis avec les scripts standard de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="00af1-172">Service workers are event-driven background threads that run from JavaScript files served up alongside the regular scripts that power your web app.</span></span>  <span data-ttu-id="00af1-173">Étant donné que les travailleurs de service ne s’exécutent pas sur le thread d’interface utilisateur principal, les travailleurs de service n’ont pas accès au DOM, même si le [thread d’interface utilisateur][MDNWorkerPrototypePostMessage] et un [thread de travail][MDNDedicatedWorkerGlobalScopePostMessage] sont en mesure de communiquer au moyen de `postMessage()` gestionnaires d’événements et de communication `onmessage` .</span><span class="sxs-lookup"><span data-stu-id="00af1-173">Because Service workers do not run on the main UI thread, service workers do not have DOM access, though the [UI thread][MDNWorkerPrototypePostMessage] and a [worker thread][MDNDedicatedWorkerGlobalScopePostMessage] is able to communicate using `postMessage()` and `onmessage` event handlers.</span></span>  

<span data-ttu-id="00af1-174">Pour associer un ouvrier de service à votre application, vous devez l’inscrire à l’adresse d’URL de votre site \(ou un chemin d’accès spécifié dans le fichier \).</span><span class="sxs-lookup"><span data-stu-id="00af1-174">You associate a service worker with your app by registering it to the URL origin of your site \(or a specified path within it\).</span></span>  <span data-ttu-id="00af1-175">Une fois inscrit, le fichier de travailleur de service est alors téléchargé, installé et activé sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="00af1-175">Once registered, the service worker file is then downloaded, installed, and activated on the user machine.</span></span>  <span data-ttu-id="00af1-176">Pour en savoir plus, MDN Web documentation dispose d’un guide complet sur [l’utilisation des travailleurs de services][MDNUsingServiceWorkers] et une référence d' [API de service][MDNServiceWorkerApi] détaillée.</span><span class="sxs-lookup"><span data-stu-id="00af1-176">For more, MDN web docs has a comprehensive guide on [Using Service Workers][MDNUsingServiceWorkers] and a detailed [Service Worker API][MDNServiceWorkerApi] reference.</span></span>  

<span data-ttu-id="00af1-177">Pour ce didacticiel, utilisez le script de travail de service de page en mode hors connexion dans le [Générateur PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="00af1-177">For this tutorial, use the Offline page service worker script on [PWA Builder][PwaBuilderServiceWorker].</span></span>  <span data-ttu-id="00af1-178">Commencez par personnaliser le script en fonction de vos besoins en matière de performances, de la bande passante réseau, etc.</span><span class="sxs-lookup"><span data-stu-id="00af1-178">Start by customizing the script with more functionality according to your performance requirements, network bandwidth, and so on.</span></span>  <span data-ttu-id="00af1-179">Consultez le livre de [recettes du travailleur][ServiceWorkerCookbook]  fourni par Mozilla pour un certain nombre d’idées mises en cache par des travailleurs de services utiles.</span><span class="sxs-lookup"><span data-stu-id="00af1-179">Review the [Service Worker Cookbook][ServiceWorkerCookbook]  provided by Mozilla for a number of useful service worker caching ideas.</span></span>  

1.  <span data-ttu-id="00af1-180">Ouvrez [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] et sélectionnez le travailleur de service de **page hors connexion** \(par défaut), puis cliquez sur le bouton **Télécharger le service ouvrier** .</span><span class="sxs-lookup"><span data-stu-id="00af1-180">Open [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] and select the \(default\) **Offline page** service worker and click the **Download service worker** button.</span></span>  
1.  <span data-ttu-id="00af1-181">Ouvrez le dossier de téléchargement et copiez les deux fichiers suivants.</span><span class="sxs-lookup"><span data-stu-id="00af1-181">Open the download folder and copy the following two files</span></span>  

    *   <span data-ttu-id="00af1-182">ServiceWorker1\pwabuilder-sw-register.js</span><span class="sxs-lookup"><span data-stu-id="00af1-182">ServiceWorker1\pwabuilder-sw-register.js</span></span>  
    *   <span data-ttu-id="00af1-183">ServiceWorker1\pwabuilder-sw.js</span><span class="sxs-lookup"><span data-stu-id="00af1-183">ServiceWorker1\pwabuilder-sw.js</span></span>  
    
    <span data-ttu-id="00af1-184">Enregistrez les fichiers dans le `public` dossier de votre projet Visual Studio Web App.</span><span class="sxs-lookup"><span data-stu-id="00af1-184">Save the files to the `public` folder of your Visual Studio web app project.</span></span>  <span data-ttu-id="00af1-185">\(Dans Visual Studio, utilisez `Ctrl` + `O` l’Explorateur de fichiers pour ouvrir l’Explorateur de fichiers et accédez au `public` dossier \).</span><span class="sxs-lookup"><span data-stu-id="00af1-185">\(From Visual Studio, use `Ctrl`+`O` to open file explorer to your project and navigate to the `public` folder\).</span></span>  
    
    <span data-ttu-id="00af1-186">Dans l’Explorateur de solutions, ouvrez le `public/pwabuilder-sw.js` fichier, puis changez la valeur de `offlineFallbackPage` to `offline.html` .</span><span class="sxs-lookup"><span data-stu-id="00af1-186">In Solution Explorer, open the `public/pwabuilder-sw.js` file, and change the value of `offlineFallbackPage` to `offline.html`.</span></span>  
    
    ```javascript
    const offlineFallbackPage = "offline.html";
    ```
    
    <span data-ttu-id="00af1-187">Il est important de revoir le code de ces deux fichiers afin d’obtenir le message d’enregistrement d’un ouvrier de service qui met en cache une page désignée \( `offline.html` \) et le remplit lorsqu’une extraction réseau échoue.</span><span class="sxs-lookup"><span data-stu-id="00af1-187">It is worth reviewing the code in both of these files, to get the gist of how to register a service worker that caches a designated page \(`offline.html`\) and serves it when a network fetch fails.</span></span>  <span data-ttu-id="00af1-188">Ensuite, créez une `offline.html` page simple en tant qu’espace réservé pour la fonctionnalité de votre application en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="00af1-188">Next, create a simple `offline.html` page as a placeholder for the offline functionality of your app.</span></span>  
    
1.  <span data-ttu-id="00af1-189">Dans l’Explorateur de solutions, ouvrez le `views/layout.pug` fichier, puis ajoutez la ligne suivante sous vos balises de lien.</span><span class="sxs-lookup"><span data-stu-id="00af1-189">In Solution Explorer, open the `views/layout.pug` file, and add the following line below your link tags.</span></span>  
    
    ```html
    script(src='/pwabuilder-sw-register.js' type='module')
    ```  
    
    <span data-ttu-id="00af1-190">Votre site charge et exécute le script d’inscription de votre travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="00af1-190">Your site loads and runs your service worker registration script.</span></span>  
    
1.  <span data-ttu-id="00af1-191">Dans l’Explorateur de solutions, cliquez avec le bouton droit sur le `public` dossier, puis sélectionnez **Ajouter**  >  **un nouveau fichier...**.  Nommez-le `offline.html` , puis ajoutez un `<title>` et du contenu du corps, par exemple le code suivant.</span><span class="sxs-lookup"><span data-stu-id="00af1-191">In Solution Explorer, right-click on the `public` folder and select **Add** > **New File...**.  Name it `offline.html`, and add a `<title>` and some body content, for example the following code.</span></span>  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    <span data-ttu-id="00af1-192">À ce stade, votre `public` dossier doit contenir trois nouveaux fichiers.</span><span class="sxs-lookup"><span data-stu-id="00af1-192">At this point, your `public` folder should have three new files.</span></span>  
    
    ![Fichiers ajoutés dans le dossier public de la solution][ImageVsNodejsExpressPublic]  
    
1.  <span data-ttu-id="00af1-194">Dans l’Explorateur de solutions, ouvrez le `routes\index.js` fichier et ajoutez le code suivant juste avant la commande finale \( `module.exports = router;` \).</span><span class="sxs-lookup"><span data-stu-id="00af1-194">In Solution Explorer, open the `routes\index.js` file, and add the following code just before the final command \(`module.exports = router;`\).</span></span>  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    <span data-ttu-id="00af1-195">Cela indique à votre application d’avoir le `offline.html` fichier \(lorsque le travailleur du service le récupère pour le cache hors connexion \).</span><span class="sxs-lookup"><span data-stu-id="00af1-195">This instructs your app to serve the `offline.html` file \(when your service worker fetches it for the offline cache\).</span></span>  
    
1.  <span data-ttu-id="00af1-196">Testez votre PWA.</span><span class="sxs-lookup"><span data-stu-id="00af1-196">Test out your PWA!</span></span>  <span data-ttu-id="00af1-197">Créez \( `Ctrl` + `Shift` + `B` \) et exécutez \( `F5` \) votre application Web pour lancer Microsoft Edge et ouvrir votre `localhost` page.</span><span class="sxs-lookup"><span data-stu-id="00af1-197">Build \(`Ctrl`+`Shift`+`B`\) and Run \(`F5`\) your web app to launch Microsoft Edge and open your `localhost` page.</span></span>  <span data-ttu-id="00af1-198">Procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="00af1-198">Then complete the following steps.</span></span>  
    
    1.  <span data-ttu-id="00af1-199">Ouvrez la **console** de devtools Edge \( `Ctrl` + `Shift` + `J` \) et vérifiez que le travailleur du service a été enregistré.</span><span class="sxs-lookup"><span data-stu-id="00af1-199">Open the Edge DevTools **Console** \(`Ctrl`+`Shift`+`J`\) and verify the Service worker was registered.</span></span>  
    1.  <span data-ttu-id="00af1-200">Dans le volet **débogueur** , développez le contrôle **travailleurs de service** , puis cliquez sur votre origine.</span><span class="sxs-lookup"><span data-stu-id="00af1-200">In the **Debugger** panel, expand the **Service Workers** control and click on your origin.</span></span>  <span data-ttu-id="00af1-201">Dans la **vue d’ensemble du travailleur de services**, vérifiez que votre travailleur de service est activé et en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="00af1-201">In the **Service Worker Overview**, verify your service worker is activated and running.</span></span>  
        
        ![Présentation du service d’DevTools Edge][ImageDevtoolsSwOverview]  
        
    1.  <span data-ttu-id="00af1-203">Développez le contrôle de **cache** et vérifiez que la `offline.html` page est mise en cache.</span><span class="sxs-lookup"><span data-stu-id="00af1-203">Expand the **Cache** control and verify that the `offline.html` page is cached.</span></span>  
        
        ![Cache du travailleur du service Edge DevTools][ImageDevtoolsSwCache]  
        
1.  <span data-ttu-id="00af1-205">Temps d’essayer votre application PWA en tant qu’application en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="00af1-205">Time to try your PWA as an offline app!</span></span>  <span data-ttu-id="00af1-206">Dans Visual Studio, **Arrêtez de déboguer** \( `Shift` + `F5` \) votre application Web, puis ouvrez Microsoft Edge \(ou actualisez) sur l’adresse localhost de votre site Web.</span><span class="sxs-lookup"><span data-stu-id="00af1-206">In Visual Studio, **Stop Debugging** \(`Shift`+`F5`\) your web app, then open Microsoft Edge \(or refresh\) to the localhost address of your website.</span></span>  <span data-ttu-id="00af1-207">Le chargement de la `offline.html` page \(par le biais de votre ouvrier de services et du cache hors connexion \) devrait désormais être chargé.</span><span class="sxs-lookup"><span data-stu-id="00af1-207">It should now load the `offline.html` page \(thanks to your service worker and offline cache\)!</span></span>  
    
    ![offline.html du http://localhost:1337 chargé dans Microsoft Edge][ImageOfflineHtml]  

## <span data-ttu-id="00af1-209">Ajouter des notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="00af1-209">Add push notifications</span></span>  

<span data-ttu-id="00af1-210">Rendez votre application Project de plus en plus proche en ajoutant une prise en charge côté client des notifications de transmission à l’aide de l' [API de transmission][MDNPushApi] pour vous abonner à un service de messagerie et l' [API notifications][MDNNotificationsApi] pour afficher un message Toast lors de la réception d’un message.</span><span class="sxs-lookup"><span data-stu-id="00af1-210">Make your PWA more app-like by adding client-side support for push notifications using the [Push API][MDNPushApi] to subscribe to a messaging service and the [Notifications API][MDNNotificationsApi] to display a toast message upon receiving a message.</span></span>  <span data-ttu-id="00af1-211">Comme pour les travailleurs de service, il s’agit d’API normalisées qui fonctionnent par le biais du navigateur, de sorte que vous n’avez à écrire le code qu’une seule fois pour le travail partout où PWAs est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="00af1-211">As with Service Workers, these are standards-based APIs that work cross-browser, so you only have to write the code once for it to work everywhere PWAs are supported.</span></span>  <span data-ttu-id="00af1-212">Sur le côté serveur, [Utilisez la bibliothèque open-source][NPMWebPush] pour gérer les différences inhérentes à la fourniture de messages de type pousser dans différents navigateurs.</span><span class="sxs-lookup"><span data-stu-id="00af1-212">On the server side, use the [Web-Push][NPMWebPush] open-source library to handle the differences involved in delivering push messages to various browsers.</span></span>  

<span data-ttu-id="00af1-213">Les solutions suivantes sont adaptées à partir du livre de [recettes de travail][ServiceWorkerCookbookPushRichDemo] complet fourni par Mozilla, qui est un bon d’examen pour un certain nombre d’autres recettes utiles sur les services Web et les employés.</span><span class="sxs-lookup"><span data-stu-id="00af1-213">The following is adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which is worth checking out for a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="00af1-214">Étape 1: installation de la bibliothèque Web NPM</span><span class="sxs-lookup"><span data-stu-id="00af1-214">Step 1 - Install the NPM web-push library</span></span>  

<span data-ttu-id="00af1-215">Dans l’Explorateur de solutions de Visual Studio, cliquez avec le bouton droit sur votre projet et **ouvrez Node.js fenêtre interactive...**.  Entrez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="00af1-215">In Visual Studio Solution Explorer, right-click your project and **Open Node.js Interactive Window...**.  In it, type the following code.</span></span>  

```javascript
.npm install web-push
```  

<span data-ttu-id="00af1-216">Cette opération installe la bibliothèque [de transmission Web][NPMWebPush] .</span><span class="sxs-lookup"><span data-stu-id="00af1-216">This installs the [Web-Push][NPMWebPush] library.</span></span>  <span data-ttu-id="00af1-217">Ensuite, ouvrez votre `index.js` fichier et ajoutez la ligne suivante en haut de votre fichier après les autres instructions.</span><span class="sxs-lookup"><span data-stu-id="00af1-217">Then, open up your `index.js` file, and add the following line to the top of your file after the other requirement statements.</span></span>  

```javascript
var webpush = require('web-push');
```  

### <span data-ttu-id="00af1-218">Étape 2: générer les clés VAPID pour votre serveur</span><span class="sxs-lookup"><span data-stu-id="00af1-218">Step 2 - Generate VAPID keys for your server</span></span>  

<span data-ttu-id="00af1-219">Ensuite, vous devez générer des clés VAPID \(d’identification involontaires du serveur d’application) pour que votre serveur envoie des messages de type pousser au client Project Web App.</span><span class="sxs-lookup"><span data-stu-id="00af1-219">Next you must generate VAPID \(Voluntary Application Server Identification\) keys for your server to send push messages to the PWA client.</span></span>  <span data-ttu-id="00af1-220">Pour cela, il vous suffit de le faire une fois \(autrement dit, votre serveur nécessite uniquement une seule paire de clés VAPID \).</span><span class="sxs-lookup"><span data-stu-id="00af1-220">You only have to do this once \(that is, your server only requires a single pair of VAPID keys\).</span></span>  <span data-ttu-id="00af1-221">Dans la fenêtre interactif du Node.js, tapez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="00af1-221">In the Node.js Interactive Window, type the following code.</span></span>  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

<span data-ttu-id="00af1-222">La sortie doit produire un objet JSON contenant une clé publique et privée, que vous copiez dans la logique de votre serveur.</span><span class="sxs-lookup"><span data-stu-id="00af1-222">The output should result in a JSON object containing a public and private key, which you copy into your server logic.</span></span>  

<span data-ttu-id="00af1-223">Dans votre `index.js` fichier, juste avant la fin de la `module.exports = router` ligne \(\), ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="00af1-223">In your `index.js` file, just before the final  \(`module.exports = router`\) line, add the following code.</span></span>  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

<span data-ttu-id="00af1-224">Copiez `publicKey` les `privateKey` valeurs et les valeurs que vous venez de générer.</span><span class="sxs-lookup"><span data-stu-id="00af1-224">Copy the `publicKey` and `privateKey` values that you just generated.</span></span>  <span data-ttu-id="00af1-225">N’hésitez pas à personnaliser l' `mailto` adresse également \(bien qu’il ne soit pas nécessaire pour exécuter cet exemple).</span><span class="sxs-lookup"><span data-stu-id="00af1-225">Feel free to customize the `mailto` address as well \(though it is not required in order to run this sample\).</span></span>  

<span data-ttu-id="00af1-226">Le [blog ingénierie des services Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] est doté d’un VAPID et de webpousser si vous êtes intéressé par le fonctionnement des coulisses.</span><span class="sxs-lookup"><span data-stu-id="00af1-226">The [Mozilla Services engineering blog][MozillaServicesSendingVapidWebPushNotificationsPush] has a nice explainer on VAPID and WebPush if you are interested in the details of how it works behind the scenes.</span></span>  

### <span data-ttu-id="00af1-227">Étape 3: gérer les demandes de serveur liées à l’émission</span><span class="sxs-lookup"><span data-stu-id="00af1-227">Step 3 - Handle push-related server requests</span></span>  

<span data-ttu-id="00af1-228">Configurez désormais des itinéraires pour gérer les demandes en relation poussée à partir du client de Project Web App, y compris la gestion de la clé publique VAPID et l’inscription du client pour recevoir des émission de type pousser.</span><span class="sxs-lookup"><span data-stu-id="00af1-228">Now set up routes for handling push-related requests from the PWA client, including serving up the VAPID public key and registering the client to receive pushes.</span></span>  

<span data-ttu-id="00af1-229">Dans un scénario réel, une notification de transmission peut provenir d’un événement dans votre logique serveur.</span><span class="sxs-lookup"><span data-stu-id="00af1-229">In a real scenario, a push notification likely originates from an event in your server logic.</span></span>  <span data-ttu-id="00af1-230">Pour simplifier les choses à ce stade, vous devez ajouter un bouton de **notification de transmission** à la page d’accueil de Project Web App pour générer des poussées à partir de notre serveur et un `/sendNotification` point de terminaison (itinéraire serveur \) pour la gestion de ces requêtes.</span><span class="sxs-lookup"><span data-stu-id="00af1-230">To simplify things here, you must add a **Push Notification** button to our PWA homepage for generating pushes from our server, and a `/sendNotification` endpoint \(server route\)for handling those requests.</span></span>  

<span data-ttu-id="00af1-231">Dans votre `index.js` fichier, ajoutez les itinéraires suivants juste après le code d’initialisation VAPID que vous avez ajouté dans [étape 2] [#step-2---Generate-VAPID-Keys-for-your-Server].</span><span class="sxs-lookup"><span data-stu-id="00af1-231">In your `index.js` file, append the following routes just after the VAPID initialization code you added in [Step 2][#step-2---generate-vapid-keys-for-your-server].</span></span>  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

<span data-ttu-id="00af1-232">Lorsque le code côté serveur est sur place, montez les notifications de transmission sur le client PWA.</span><span class="sxs-lookup"><span data-stu-id="00af1-232">With the server-side code in place, plumb in push notifications on the PWA client.</span></span>  

### <span data-ttu-id="00af1-233">Étape 4: s’abonner aux notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="00af1-233">Step 4 - Subscribe to push notifications</span></span>  

<span data-ttu-id="00af1-234">Dans le cadre de leur rôle de proxy réseau sur Project Web App, les travailleurs de services gèrent les événements d’émission et les interactions de notification Toast.</span><span class="sxs-lookup"><span data-stu-id="00af1-234">As part of their role as PWA network proxies, service workers handle push events and toast notification interactions.</span></span>  <span data-ttu-id="00af1-235">Toutefois, comme il s’agit de la première configuration de \(ou de l’enregistrement \) d’un travailleur de service, il est possible d’abonner les notifications de type «PWA» aux notifications de transmission du serveur sur le thread d’interface utilisateur principal de PWA et nécessite une connectivité réseau.</span><span class="sxs-lookup"><span data-stu-id="00af1-235">However, as it is with first setting up \(or registering\) a service worker, subscribing the PWA to server push notifications happens on the main UI thread of the PWA and requires network connectivity.</span></span>  <span data-ttu-id="00af1-236">S’abonner à des notifications d’émission nécessite l’inscription d’un employé de service actif, vous devez donc vérifier que votre travailleur de service est installé et actif avant d’essayer de s’abonner aux notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="00af1-236">Subscribing to push notifications requires an active service worker registration, so you must first verify that your service worker is installed and active before trying to subscribe it to push notifications.</span></span>  

<span data-ttu-id="00af1-237">Avant la création d’un nouvel abonnement envoyé, Microsoft Edge vérifie que l’utilisateur a accordé l’autorisation PWA de recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="00af1-237">Before a new push subscription is created, Microsoft Edge check if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="00af1-238">Si ce n’est pas le cas, l’utilisateur est invité par le navigateur à entrer une autorisation.</span><span class="sxs-lookup"><span data-stu-id="00af1-238">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="00af1-239">Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` lever a `DOMException` et doit donc être gérée.</span><span class="sxs-lookup"><span data-stu-id="00af1-239">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, so you must handle it.</span></span>  <span data-ttu-id="00af1-240">Pour plus d’informations sur la gestion des autorisations, voir [notifications de transmission dans Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="00af1-240">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="00af1-241">Dans votre `pwabuilder-sw-register.js` fichier, ajoutez le code suivant.</span><span class="sxs-lookup"><span data-stu-id="00af1-241">In your `pwabuilder-sw-register.js` file, append the following code.</span></span>  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
            });
        });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

<span data-ttu-id="00af1-242">Reportez-vous à la documentation MDN sur l’interface [PushManager][MDNPushManager] et NPM documents sur la bibliothèque de documents [Web][NPMWebPushUsage] pour plus d’informations sur le fonctionnement des API et sur diverses options associées.</span><span class="sxs-lookup"><span data-stu-id="00af1-242">Review the MDN documentation on the [PushManager][MDNPushManager] interface and NPM docs on the [Web-Push][NPMWebPushUsage] library for more details on how the APIs work and various related options.</span></span>  

### <span data-ttu-id="00af1-243">Étape 5: configurer les gestionnaires d’événements de type pousser et notificationclick</span><span class="sxs-lookup"><span data-stu-id="00af1-243">Step 5 - Set up push and notificationclick event handlers</span></span>  

<span data-ttu-id="00af1-244">Avec notre abonnement envoyé, le reste du travail intervient dans le travailleur de service.</span><span class="sxs-lookup"><span data-stu-id="00af1-244">With our push subscription set up, the remainder of the work happens in the service worker.</span></span>  <span data-ttu-id="00af1-245">Tout d’abord, vous devez configurer un gestionnaire pour les événements de transmission envoyés par le serveur et répondre avec une notification Toast \(si une autorisation a été accordée \) indiquant la charge utile des données de type pousser.</span><span class="sxs-lookup"><span data-stu-id="00af1-245">First you must set up a handler for server-sent push events, and respond with a toast notification \(if permission was granted\) displaying the push data payload.</span></span>  <span data-ttu-id="00af1-246">Ensuite, ajoutez un gestionnaire de Click pour le Toast afin d’ignorer la notification et de trier dans la liste des fenêtres actuellement ouvertes pour ouvrir, mettre au point, ou ouvrir et mettre le focus sur la page du client Project Web App prévue.</span><span class="sxs-lookup"><span data-stu-id="00af1-246">Next you add a click handler for the toast to dismiss the notification and sort through a list of currently open windows to open, focus, or open and focus the intended PWA client page.</span></span>  

<span data-ttu-id="00af1-247">Dans votre `pwabuilder-sw.js` fichier, ajoutez les gestionnaires suivants.</span><span class="sxs-lookup"><span data-stu-id="00af1-247">In your `pwabuilder-sw.js` file, append the following handlers.</span></span>  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### <span data-ttu-id="00af1-248">Étape 6: essayez-le</span><span class="sxs-lookup"><span data-stu-id="00af1-248">Step 6 - Try it out</span></span>  

<span data-ttu-id="00af1-249">Temps de test des notifications de transmission dans votre PWA</span><span class="sxs-lookup"><span data-stu-id="00af1-249">Time to test push notifications in your PWA!</span></span>  

1.  <span data-ttu-id="00af1-250">Exécutez \( `F5` \) votre PWA dans le navigateur.</span><span class="sxs-lookup"><span data-stu-id="00af1-250">Run \(`F5`\) your PWA in the browser.</span></span>  <span data-ttu-id="00af1-251">Étant donné que vous avez modifié le code de travailleur du service \( `pwabuilder-sw.js` \), vous devez ouvrir le débogueur de devtools \( `F12` \) dans le panneau de **vue d’ensemble des travailleurs de services** et **Annuler l’enregistrement** du travailleur de service, puis recharger \( `F5` \) la page pour le réenregistrer \(ou cliquer sur **mettre à jour**\).</span><span class="sxs-lookup"><span data-stu-id="00af1-251">Because you modified the service worker code \(`pwabuilder-sw.js`\), you must open the DevTools Debugger \(`F12`\) to the **Service Worker Overview** panel and **Unregister** the service worker and reload \(`F5`\) the page to re-register it \(or you click **Update**\).</span></span>  <span data-ttu-id="00af1-252">Dans un scénario de production, le navigateur vérifie régulièrement les mises à jour des travailleurs de services et installe les mises à jour en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="00af1-252">In a production scenario, the browser checks regularly check for service worker updates and install the updates in the background.</span></span>  <span data-ttu-id="00af1-253">Nous vous conseillons de le faire pour les résultats immédiats.</span><span class="sxs-lookup"><span data-stu-id="00af1-253">You should force it here for immediate results.</span></span>  
    
    <span data-ttu-id="00af1-254">Lorsque le travailleur de votre service est actif et tente de s’abonner à votre PWA pour les notifications de transmission, une boîte de dialogue d’autorisation apparaît en bas de la page.</span><span class="sxs-lookup"><span data-stu-id="00af1-254">As your service worker activates and attempts to subscribe your PWA to push notifications, you should see a permission dialog at the bottom of the page.</span></span>  
    
    ![Boîte de dialogue autorisation permettant d’activer les notifications][ImageNotificationPermission]  
    
    <span data-ttu-id="00af1-256">Cliquez sur **Oui** pour activer les notifications toast pour votre PWA.</span><span class="sxs-lookup"><span data-stu-id="00af1-256">Choose **Yes** to enable toast notifications for your PWA.</span></span>  
    
1.  <span data-ttu-id="00af1-257">Dans le volet vue d’ensemble des travailleurs de services, essayez de choisir le bouton  **transmission** .</span><span class="sxs-lookup"><span data-stu-id="00af1-257">From the Service Worker Overview pane, try choosing the  **Push** button.</span></span>  <span data-ttu-id="00af1-258">Une notification toast avec le message électronique de test «test de test» de DevTools "\) doit apparaître.</span><span class="sxs-lookup"><span data-stu-id="00af1-258">A toast notification with the \(hard-coded "Test push message from DevTools"\) payload should appear.</span></span>  
    
    ![Pousser une notification de DevTools][ImageDevtoolsPush]  
    
1.  <span data-ttu-id="00af1-260">Essayez ensuite de cliquer sur le bouton **Envoyer une notification** sur la page d’accueil de votre PWA.</span><span class="sxs-lookup"><span data-stu-id="00af1-260">Next try choosing the **Send Notification** button on the homepage of your PWA.</span></span>  <span data-ttu-id="00af1-261">Cette fois, un toast avec la charge utile de votre serveur s’affiche.</span><span class="sxs-lookup"><span data-stu-id="00af1-261">This time a toast with the payload from your server appears.</span></span>  
    
    ![Pousser une notification à partir du serveur PWA][ImagePwaPush]  
    
    <span data-ttu-id="00af1-263">Si vous ne cliquez pas sur \(ou activer) une notification Toast, elle est ignorée après quelques secondes, puis mise en file d’attente dans le centre de notifications Windows.</span><span class="sxs-lookup"><span data-stu-id="00af1-263">If you do not click \(or activate\) a toast notification, it is dismissed after several seconds and queue up in your Windows Action Center.</span></span>  
    
    ![Notifications dans le centre de notifications Windows][ImageWindowsActionCenter]  
    
    <span data-ttu-id="00af1-265">Vous avez les bases des notifications de transmission de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="00af1-265">You have the basics of PWA push notifications.</span></span>  <span data-ttu-id="00af1-266">Dans une application réelle, les étapes suivantes sont implémentées de manière à gérer et stocker les abonnements envoyés et à [chiffrer][NPMWebPushEncrypt] correctement les données de charge utile envoyées sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="00af1-266">In a real app, the next steps are implemented in a way to manage and store push subscriptions and to properly [encrypt][NPMWebPushEncrypt] payload data being sent across the wire.</span></span>  
    
## <span data-ttu-id="00af1-267">Aller plus loin</span><span class="sxs-lookup"><span data-stu-id="00af1-267">Going further</span></span>  

<span data-ttu-id="00af1-268">Ce guide a démontré l’anatomie de base d’une application Web progressive et des outils de développement de Microsoft Project Web App, dont Visual Studio, le concepteur PWA et DevTools Edge.</span><span class="sxs-lookup"><span data-stu-id="00af1-268">This guide demonstrated the basic anatomy of a Progressive Web App and Microsoft PWA development tools including Visual Studio, PWA Builder, and Edge DevTools.</span></span>  

<span data-ttu-id="00af1-269">Bien entendu, il y a beaucoup plus de choses à [faire][PwaEdgehtmlIndexRequirements] au-delà de ce que vous lisez ici, y compris la conception réactive, les liens hypertexte, les [Tests multinavigateurs][BrowserStackTestEdgeBrowser] et d’autres [pratiques recommandées][Webhint] (sans mentionner la fonctionnalité de votre application! \), mais j’espère que ce guide vous a donné une présentation solide des notions de base sur Project Web App</span><span class="sxs-lookup"><span data-stu-id="00af1-269">Of course, there is a lot more that goes into [making a great PWA][PwaEdgehtmlIndexRequirements] beyond what you read here, including responsive design, deep-linking, [cross-browser testing][BrowserStackTestEdgeBrowser] and other [best practices][Webhint] \(not to mention your app functionality!\), but hopefully this guide gave you a solid introduction of PWA basics and some ideas on getting started.</span></span>  <span data-ttu-id="00af1-270">Si vous avez d’autres questions sur le développement de Project Web App avec Windows ou Visual Studio, n’hésitez pas à nous laisser un commentaire!</span><span class="sxs-lookup"><span data-stu-id="00af1-270">If you have further questions on PWA development with Windows or with Visual Studio, please leave a comment!</span></span>  

<span data-ttu-id="00af1-271">Passez en revue les autres guides de Project Web App pour découvrir comment augmenter l’implication des clients et offrir une interface plus transparente et intégrée au système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="00af1-271">Review the other PWA guides to learn how to increase customer engagement and provide a more seamless, OS-integrated app experience.</span></span>  

*   <span data-ttu-id="00af1-272">[Personnalisation de Windows][PwaEdgehtmlWindowsFeatures].</span><span class="sxs-lookup"><span data-stu-id="00af1-272">[Windows tailoring][PwaEdgehtmlWindowsFeatures].</span></span> <span data-ttu-id="00af1-273">À l’aide d’une détection de fonctionnalités simple, vous pouvez améliorer progressivement vos clients Windows 10 par le biais des API Windows Runtime \(WinRT \) natives, telles que celles permettant de personnaliser les notifications par vignette du menu **Démarrer** de Windows et la barre des tâches JumpLists et \</span><span class="sxs-lookup"><span data-stu-id="00af1-273">Using simple feature detection, you may progressively enhance your PWA for Windows 10 customers through native Windows Runtime \(WinRT\) APIs, such as those for customizing Windows **Start** menu tile notifications and taskbar jumplists, and \(upon permission\) working with user resources, such as photos, music, and calendar.</span></span>  
*   <span data-ttu-id="00af1-274">[PWAS dans le Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="00af1-274">[PWAs in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  <span data-ttu-id="00af1-275">En savoir plus sur les avantages de la distribution de l’App Store et sur la soumission de votre PWA.</span><span class="sxs-lookup"><span data-stu-id="00af1-275">Learn more about the benefits of app store distribution and how to submit your PWA.</span></span>  

## <span data-ttu-id="00af1-276">Voir également</span><span class="sxs-lookup"><span data-stu-id="00af1-276">See also</span></span>  

*   <span data-ttu-id="00af1-277">Des [applications Web progressives sur MDN Web docs][MDNProgressiveWebApps] -excellent guide sur les applications Web progressives.</span><span class="sxs-lookup"><span data-stu-id="00af1-277">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="00af1-278">[Applications Web progressivement sur le Web. dev][WebDevProgressiveWebApps] -excellent guide sur les applications Web progressives.</span><span class="sxs-lookup"><span data-stu-id="00af1-278">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="00af1-279">[Applications Web progressives-présentation Rocks][ProgressiveWebApps] : exemples concrets de PWAS.</span><span class="sxs-lookup"><span data-stu-id="00af1-279">[Progressive Web Apps rocks][ProgressiveWebApps] - Showcases real-world examples of PWAs.</span></span>  
*   <span data-ttu-id="00af1-280">[Lecteurs de News malveillants: applications Web progressives][HackerNewsProgressiveWebApps] -compare les différents types d’infrastructure et de performance permettant d’implémenter un exemple de version de Project</span><span class="sxs-lookup"><span data-stu-id="00af1-280">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Configuration requise-applications Web progressives \(EdgeHTML \) sur Windows | Documents Microsoft"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps/microsoft-store.md "Applications Web progressives \(EdgeHTML \) sur le Microsoft Store | Documents Microsoft"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps/windows-features.md "Personnaliser votre PWA \(EdgeHTML \) pour Windows | Documents Microsoft"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Politiques du Microsoft Store | Documents Microsoft"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Didacticiel: créer un Node.js et une application rapide dans Visual Studio | Documents Microsoft"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Publier dans Azure App service-créer une Node.js et une application rapide dans Visual Studio | Documents Microsoft"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "Qu’est-ce qu’une application de plateforme Windows universelle (UWP)?  | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer un compte gratuit Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Applications Web | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Accueillir des applications Web progressives sur Microsoft Edge et Windows 10 | Blogs Windows"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications Web dans Microsoft Edge | Blogs Windows"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Téléchargements | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "Services de & de logiciels de développeur gratuits | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Visual Studio preview"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Tests gratuits du navigateur Microsoft Edge sur Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs de nouvelles pirates en application Web progressive"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. postMessage \(\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications Web progressives (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utiliser des travailleurs de service | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. prototype. postMessage \(\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoyer des notifications webtransmission identifiées par VAPID via le service pousser de Mozilla Services Mozilla"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Poussée | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Poussée | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation-Web-Poussée | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications Web progressives"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Attributs | Pug"  

[PwaBuilder]: https://www.pwabuilder.com "Générateur PWA"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "Générateur d’image d’application"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Travailleur de service | Générateur PWA"  

[ServiceWorkerCookbook]: https://serviceworke.rs "Livre de ServiceWorker"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Démonstration complète | Livre de ServiceWorker"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Manifeste de l’application Web | W3C"  

[Webhint]: https://sonarwhal.com "webhint, le moteur d’indicateurs pour les meilleures pratiques sur le Web" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Utilisation des travailleurs Web" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications Web progressives | Web. dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Wikipédia"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Amélioration progressive | Wikipédia"  
