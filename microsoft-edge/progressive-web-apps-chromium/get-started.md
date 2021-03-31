---
description: Ce guide vous donne une vue d’ensemble des outils et des principes de base de PWA pour la création d’applications web progressives (Chromium) sur Windows.
title: Mise en place des applications web progressives (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: applications web progressives, PWA, Edge, Windows, PWABuilder, manifeste web, service de travail, push
ms.openlocfilehash: 6ff24b2e9219b2f3755bb2e8f6db137dc7a721ec
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398132"
---
# <a name="get-started-with-progressive-web-apps-chromium"></a><span data-ttu-id="84124-104">Mise en place des applications web progressives (Chromium)</span><span class="sxs-lookup"><span data-stu-id="84124-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="84124-105">Les applications web progressives \(PWAs\) sont des applications web qui sont [progressivement améliorées.][WikiProgressiveEnhancement]</span><span class="sxs-lookup"><span data-stu-id="84124-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="84124-106">Les améliorations progressives incluent des fonctionnalités de type application, telles que l’installation, la prise en charge hors connexion et les notifications Push.</span><span class="sxs-lookup"><span data-stu-id="84124-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="84124-107">Vous pouvez également packager votre PWA pour les magasins d’applications.</span><span class="sxs-lookup"><span data-stu-id="84124-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="84124-108">Les magasins d’applications possibles incluent le Microsoft Store, Google Play, l’App Store Mac, etc.</span><span class="sxs-lookup"><span data-stu-id="84124-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="84124-109">Le Microsoft Store est le magasin d’applications commerciales intégré à Windows 10.</span><span class="sxs-lookup"><span data-stu-id="84124-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="84124-110">Le guide suivant vous donne une vue d’ensemble des principes de base de PWA en créant une application web simple et en l’étendant en tant que PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="84124-111">Le projet terminé fonctionne dans les navigateurs modernes.</span><span class="sxs-lookup"><span data-stu-id="84124-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="84124-112">Vous pouvez utiliser [PWABuilder][PwaBuilder] pour créer un PWA, améliorer votre PWA existant ou créer un package PWA pour les magasins d’applications.</span><span class="sxs-lookup"><span data-stu-id="84124-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <a name="prerequisites"></a><span data-ttu-id="84124-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="84124-113">Prerequisites</span></span>  

*   <span data-ttu-id="84124-114">Utilisez [Visual Studio code pour][VisualstudioCodeMain] modifier votre code source PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="84124-115">Utilisez [Node.js][NodejsMain] comme serveur web local.</span><span class="sxs-lookup"><span data-stu-id="84124-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <a name="create-a-basic-web-app"></a><span data-ttu-id="84124-116">Créer une application web de base</span><span class="sxs-lookup"><span data-stu-id="84124-116">Create a basic web app</span></span>  

<span data-ttu-id="84124-117">Pour créer une application web vide, suivez les étapes du Générateur d’applications [Node Express][ExpressjsApplicationGenerator]et nommez votre `MySamplePwa` application.</span><span class="sxs-lookup"><span data-stu-id="84124-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="84124-118">Dans l’invite, exécutez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="84124-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="84124-119">Les commandes créent une application web vide et installent les dépendances.</span><span class="sxs-lookup"><span data-stu-id="84124-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="84124-120">Vous avez maintenant une application web simple et fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="84124-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="84124-121">Pour démarrer votre application web, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="84124-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="84124-122">À présent, `http://localhost:3000` recherchez l’affichage de votre nouvelle application web.</span><span class="sxs-lookup"><span data-stu-id="84124-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Exécution de votre nouveau PWA sur localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="84124-124">Exécution de votre nouveau PWA sur localhost</span><span class="sxs-lookup"><span data-stu-id="84124-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <a name="get-started-building-a-pwa"></a><span data-ttu-id="84124-125">Commencer à créer un PWA</span><span class="sxs-lookup"><span data-stu-id="84124-125">Get started building a PWA</span></span>  

<span data-ttu-id="84124-126">Maintenant que vous avez une application web simple, étendez-la en tant que PWA en ajoutant les trois conditions requises pour les applications PWA</span><span class="sxs-lookup"><span data-stu-id="84124-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="84124-127">: [HTTPS](#step-1---use-https), un [manifeste d’application web](#step-2---create-a-web-app-manifest)et un service de [travail](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="84124-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <a name="step-1---use-https"></a><span data-ttu-id="84124-128">Étape 1 : utiliser HTTPS</span><span class="sxs-lookup"><span data-stu-id="84124-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="84124-129">Les principales parties de la plateforme PWA, telles que les travailleurs du [service,][MDNServiceWorkerApi]nécessitent l’utilisation du protocole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="84124-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="84124-130">Lorsque votre PWA est en ligne, vous devez le publier sur une URL HTTPS.</span><span class="sxs-lookup"><span data-stu-id="84124-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="84124-131">À des fins de débogage, Microsoft Edge permet également d’utiliser `http://localhost` les API PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="84124-132">[Publiez votre application web en tant que site en direct,][VisualStudioNodejsTutorialPublishAzureAppService]mais assurez-vous que votre serveur est configuré pour HTTPS.</span><span class="sxs-lookup"><span data-stu-id="84124-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="84124-133">Par exemple, vous pouvez créer un [compte gratuit Azure.][AzureCreateFreeAccount]</span><span class="sxs-lookup"><span data-stu-id="84124-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="84124-134">Hébergez votre site sur [Microsoft Azure App Service][AzureWebApps] et il est servi sur HTTPS par défaut.</span><span class="sxs-lookup"><span data-stu-id="84124-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="84124-135">Le guide suivant, à `http://localhost` utiliser pour créer votre PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <a name="step-2---create-a-web-app-manifest"></a><span data-ttu-id="84124-136">Étape 2 : créer un manifeste d’application web</span><span class="sxs-lookup"><span data-stu-id="84124-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="84124-137">Un [manifeste d’application web][MDNWebAppManifest] est un fichier JSON contenant des métadonnées sur votre application, telles que le nom, la description, les icônes, etc.</span><span class="sxs-lookup"><span data-stu-id="84124-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="84124-138">Pour ajouter un manifeste d’application à l’application web :</span><span class="sxs-lookup"><span data-stu-id="84124-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="84124-139">In Visual Studio Code, choose **File**  >  **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span><span class="sxs-lookup"><span data-stu-id="84124-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="84124-140">Sélectionnez `Ctrl` + `N` pour créer un fichier et collez-le dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="84124-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  <span data-ttu-id="84124-141">Enregistrez le fichier sous `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="84124-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="84124-142">Ajoutez une image d’icône d’application 512 x 512 `icon512.png` nommée à `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="84124-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="84124-143">Vous pouvez utiliser [l’exemple d’image à][ImagePwa] des fins de test.</span><span class="sxs-lookup"><span data-stu-id="84124-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="84124-144">Dans Visual Studio code, ouvrez et ajoutez l’extrait de code suivant `/public/index.html` à l’intérieur de la `<head>` balise.</span><span class="sxs-lookup"><span data-stu-id="84124-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <a name="step-3---add-a-service-worker"></a><span data-ttu-id="84124-145">Étape 3 : ajouter un service de travail</span><span class="sxs-lookup"><span data-stu-id="84124-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="84124-146">Les travailleurs de service sont la technologie clé derrière les PPA, ce qui permet des scénarios tels que la prise en charge hors connexion, la mise en cache avancée et l’exécution de tâches en arrière-plan précédemment limitées aux applications natives.</span><span class="sxs-lookup"><span data-stu-id="84124-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="84124-147">Les employés de service sont des tâches en arrière-plan qui interceptent les demandes réseau de votre application web.</span><span class="sxs-lookup"><span data-stu-id="84124-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="84124-148">Les employés de service tentent d’effectuer des tâches, même lorsque votre PWA n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="84124-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="84124-149">Les tâches incluent les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="84124-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="84124-150">Service des ressources demandées à partir d’un cache</span><span class="sxs-lookup"><span data-stu-id="84124-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="84124-151">Envoi de notifications Push</span><span class="sxs-lookup"><span data-stu-id="84124-151">Sending push notifications</span></span>  
*   <span data-ttu-id="84124-152">Exécution de tâches de récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="84124-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="84124-153">Icônes de badging</span><span class="sxs-lookup"><span data-stu-id="84124-153">Badging icons</span></span>  
*   <span data-ttu-id="84124-154">et plus</span><span class="sxs-lookup"><span data-stu-id="84124-154">and more</span></span>  
    
<span data-ttu-id="84124-155">Les employés de service sont définis dans un fichier JavaScript spécial.</span><span class="sxs-lookup"><span data-stu-id="84124-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="84124-156">Pour plus d’informations, accédez à [Utilisation des travailleurs de service][MDNUsingServiceWorkers] et de [l’API de travail de service.][MDNServiceWorkerApi]</span><span class="sxs-lookup"><span data-stu-id="84124-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="84124-157">Pour créer un service de travail dans votre projet, utilisez la recette de travail de travail de service réseau mise en **cache** à partir du [Générateur PWA.][PwaBuilderServiceWorker]</span><span class="sxs-lookup"><span data-stu-id="84124-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="84124-158">Accédez [à pwabuilder.com/serviceworker,][PwaBuilderServiceWorker]sélectionnez le travail de service réseau mis **en cache** en premier, puis sélectionnez le bouton Télécharger. </span><span class="sxs-lookup"><span data-stu-id="84124-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="84124-159">Le fichier téléchargé contient les fichiers suivants :</span><span class="sxs-lookup"><span data-stu-id="84124-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="84124-160">Copiez les fichiers téléchargés dans le `public` dossier de votre projet d’application web.</span><span class="sxs-lookup"><span data-stu-id="84124-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="84124-161">Dans Visual Studio code, ouvrez et ajoutez l’extrait de code suivant `/public/index.html` à l’intérieur de la `<head>` balise.</span><span class="sxs-lookup"><span data-stu-id="84124-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="84124-162">Votre application web dispose désormais d’un service de travail qui utilise la stratégie de mise en cache en premier.</span><span class="sxs-lookup"><span data-stu-id="84124-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="84124-163">Le nouveau service de travail récupère d’abord les ressources du cache et du réseau uniquement si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="84124-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="84124-164">Les ressources mises en cache incluent les images, JavaScript, CSS et HTML.</span><span class="sxs-lookup"><span data-stu-id="84124-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="84124-165">Utilisez les étapes suivantes pour confirmer que votre service de travail s’exécute.</span><span class="sxs-lookup"><span data-stu-id="84124-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="84124-166">Accédez à votre application web à l’aide `http://localhost:3000` de .</span><span class="sxs-lookup"><span data-stu-id="84124-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="84124-167">Si votre application web n’est pas disponible, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="84124-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="84124-168">Dans Microsoft Edge, `F12` sélectionnez pour ouvrir Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="84124-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="84124-169">Sélectionnez **Application,** puis **Service Workers** pour afficher les travailleurs du service.</span><span class="sxs-lookup"><span data-stu-id="84124-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="84124-170">Si le service de travail n’est pas affiché, actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="84124-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Vue d’ensemble de Microsoft Edge DevTools Service Worker" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="84124-172">Vue d’ensemble de Microsoft Edge DevTools Service Worker</span><span class="sxs-lookup"><span data-stu-id="84124-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="84124-173">Affichez le cache de travail de service en développez le stockage **de cache** et sélectionnez **pwabuilder-precache**.</span><span class="sxs-lookup"><span data-stu-id="84124-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="84124-174">Toutes les ressources mises en cache par le service de travail doivent être affichées.</span><span class="sxs-lookup"><span data-stu-id="84124-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="84124-175">Les ressources mises en cache par le service comprennent l’icône de l’application, le manifeste de l’application, les fichiers CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="84124-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache de travail de service dans Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="84124-177">Cache de travail de service dans Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="84124-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="84124-178">Essayez votre application PWA en tant qu’application hors connexion.</span><span class="sxs-lookup"><span data-stu-id="84124-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="84124-179">In Microsoft Edge DevTools \( `F12` \), choose **Network** then change the **Online** status to **Offline**.</span><span class="sxs-lookup"><span data-stu-id="84124-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Définition de l’application en mode hors connexion dans Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="84124-181">Définition de l’application en mode hors connexion dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="84124-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="84124-182">Actualisez votre application et affichez le mécanisme hors connexion pour servir les ressources de votre application à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="84124-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA en cours d’exécution hors connexion" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="84124-184">PWA en cours d’exécution hors connexion</span><span class="sxs-lookup"><span data-stu-id="84124-184">PWA running offline</span></span>
    :::image-end:::
    
## <a name="add-push-notifications-to-your-pwa"></a><span data-ttu-id="84124-185">Ajouter des notifications Push à votre PWA</span><span class="sxs-lookup"><span data-stu-id="84124-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="84124-186">Vous pouvez créer des P.A.P. qui prendre en charge les notifications Push en effectuant les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="84124-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="84124-187">S’abonner à un service de messagerie à l’aide de [l’API Push][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="84124-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="84124-188">Afficher un message toast lorsqu’un message est reçu du service à l’aide de [l’API Notifications][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="84124-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="84124-189">Comme pour les travailleurs de service, les API de notification Push sont des API basées sur des normes.</span><span class="sxs-lookup"><span data-stu-id="84124-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="84124-190">Les API de notification Push fonctionnent dans tous les navigateurs. Votre code doit donc fonctionner partout où les PPA sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="84124-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="84124-191">Pour plus d’informations sur la livraison de messages Push à différents navigateurs sur votre serveur, accédez [à Web-Push][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="84124-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="84124-192">Les étapes suivantes ont été adaptées à partir du manuel de travail de démonstration enrichie Push in [Service][ServiceWorkerCookbookPushRichDemo] fourni par Mozilla, qui offre un certain nombre d’autres recettes utiles de travail de service et Web Push.</span><span class="sxs-lookup"><span data-stu-id="84124-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <a name="step-1---generate-vapid-keys"></a><span data-ttu-id="84124-193">Étape 1 : générer des clés VAPID</span><span class="sxs-lookup"><span data-stu-id="84124-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="84124-194">Les notifications Push nécessitent des clés VAPID \(Identification du serveur d’applications volontaires\) pour envoyer des messages push au client PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="84124-195">Plusieurs générateurs de clés VAPID sont disponibles en ligne [\(par exemple, vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="84124-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="84124-196">Après la génération, vous devez obtenir un objet JSON contenant une clé publique et privée.</span><span class="sxs-lookup"><span data-stu-id="84124-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="84124-197">Enregistrez les clés pour les étapes ultérieures dans le didacticiel suivant.</span><span class="sxs-lookup"><span data-stu-id="84124-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="84124-198">Pour plus d’informations sur VAPID et WebPush, accédez à Envoyer des [notifications WebPush identifiées par VAPID][MozillaServicesSendingVapidWebPushNotificationsPush]à l’aide du service Push Mozilla.</span><span class="sxs-lookup"><span data-stu-id="84124-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <a name="step-2---subscribe-to-push-notifications"></a><span data-ttu-id="84124-199">Étape 2 : s’abonner aux notifications Push</span><span class="sxs-lookup"><span data-stu-id="84124-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="84124-200">Les employés de service gèrent les événements Push et les interactions de notification toast dans votre PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="84124-201">Pour abonner PWA aux notifications Push du serveur, assurez-vous que les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="84124-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="84124-202">Votre PWA est installé, actif et inscrit</span><span class="sxs-lookup"><span data-stu-id="84124-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="84124-203">Votre code pour terminer la tâche d’abonnement se trouve sur le thread d’interface utilisateur principal de PWA</span><span class="sxs-lookup"><span data-stu-id="84124-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="84124-204">Vous avez une connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="84124-204">You have network connectivity</span></span>  
    
<span data-ttu-id="84124-205">Avant de créer un abonnement Push, Microsoft Edge vérifie si l’utilisateur a accordé l’autorisation PWA pour recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="84124-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="84124-206">Si ce n’est pas le cas, le navigateur demande l’autorisation à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84124-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="84124-207">Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` throws a `DOMException` , qui doit être gérée.</span><span class="sxs-lookup"><span data-stu-id="84124-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="84124-208">Pour plus d’informations sur la gestion des autorisations, accédez [à Notifications Push dans Microsoft Edge.][WindowsBlogsWebNotificationsEdge]</span><span class="sxs-lookup"><span data-stu-id="84124-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="84124-209">Dans votre `pwabuilder-sw-register.js` fichier,endez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="84124-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
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

<span data-ttu-id="84124-210">Pour plus d’informations, [accédez à PushManager][MDNPushManager] et [Web-Push.][NPMWebPushUsage]</span><span class="sxs-lookup"><span data-stu-id="84124-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <a name="step-3---listen-for-push-notifications"></a><span data-ttu-id="84124-211">Étape 3 : écouter les notifications Push</span><span class="sxs-lookup"><span data-stu-id="84124-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="84124-212">Une fois qu’un abonnement est créé dans votre PWA, ajoutez des handlers au service de travail pour répondre aux événements Push.</span><span class="sxs-lookup"><span data-stu-id="84124-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="84124-213">Les événements Push sont envoyés à partir du serveur pour afficher des notifications toast.</span><span class="sxs-lookup"><span data-stu-id="84124-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="84124-214">Les notifications toast affichent les données d’un message reçu.</span><span class="sxs-lookup"><span data-stu-id="84124-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="84124-215">Pour effectuer les tâches suivantes, vous devez ajouter `click` un handler.</span><span class="sxs-lookup"><span data-stu-id="84124-215">To complete the following tasks, you must add a `click` handler.</span></span>  

*   <span data-ttu-id="84124-216">Ignorer la notification toast</span><span class="sxs-lookup"><span data-stu-id="84124-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="84124-217">Ouvrir, mettre au point ou ouvrir et mettre au point toutes les fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="84124-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="84124-218">Ouvrir et mettre au point une nouvelle fenêtre pour afficher une page cliente PWA</span><span class="sxs-lookup"><span data-stu-id="84124-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="84124-219">Dans votre `pwabuilder-sw.js` fichier, ajoutez les handlers suivants.</span><span class="sxs-lookup"><span data-stu-id="84124-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This attempts to display the current notification if it is already open and then focuses on it.
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

### <a name="step-4---try-it-out"></a><span data-ttu-id="84124-220">Étape 4 : essayez</span><span class="sxs-lookup"><span data-stu-id="84124-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="84124-221">Pour tester les notifications Push pour votre PWA, complétez les étapes suivantes.</span><span class="sxs-lookup"><span data-stu-id="84124-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="84124-222">Accédez à votre PWA sur `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="84124-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="84124-223">Lorsque votre service de travail s’active et tente d’abonner votre PWA aux notifications Push, Microsoft Edge vous invite à autoriser votre PWA à afficher les notifications.</span><span class="sxs-lookup"><span data-stu-id="84124-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="84124-224">Sélectionnez **Autoriser**.</span><span class="sxs-lookup"><span data-stu-id="84124-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Boîte de dialogue d’autorisation pour l’activation des notifications" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="84124-226">Boîte de dialogue d’autorisation pour l’activation des notifications</span><span class="sxs-lookup"><span data-stu-id="84124-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="84124-227">Simulez une notification Push côté serveur.</span><span class="sxs-lookup"><span data-stu-id="84124-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="84124-228">Une fois votre PWA ouvert dans votre navigateur, sélectionnez `http://localhost:3000` `F12` devTools.</span><span class="sxs-lookup"><span data-stu-id="84124-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="84124-229">Choose **Application**  >  **Service Worker**  >  **Push** to send a test push notification to your PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="84124-230">Une notification Push doit s’afficher près de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="84124-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Envoyer une notification à partir de DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="84124-232">Envoyer une notification à partir de DevTools</span><span class="sxs-lookup"><span data-stu-id="84124-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="84124-233">Si vous ne sélectionnez pas \(ou n’activez pas\) une notification toast, le système la masque automatiquement après plusieurs secondes et la met en file d’attente dans votre Centre de notifications Windows.</span><span class="sxs-lookup"><span data-stu-id="84124-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notifications dans le Centre de notifications Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="84124-235">Notifications dans le Centre de notifications Windows</span><span class="sxs-lookup"><span data-stu-id="84124-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <a name="next-steps"></a><span data-ttu-id="84124-236">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="84124-236">Next steps</span></span>  

<span data-ttu-id="84124-237">Les étapes suivantes incluent des tâches supplémentaires pour vous aider à comprendre la création de P PWAs réels.</span><span class="sxs-lookup"><span data-stu-id="84124-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="84124-238">Gérer et stocker les abonnements Push</span><span class="sxs-lookup"><span data-stu-id="84124-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="84124-239">[Chiffrer les][NPMWebPushEncrypt] données de charge utile</span><span class="sxs-lookup"><span data-stu-id="84124-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="84124-240">Conception réactive</span><span class="sxs-lookup"><span data-stu-id="84124-240">Responsive design</span></span>  
*   <span data-ttu-id="84124-241">Liaisons profondes</span><span class="sxs-lookup"><span data-stu-id="84124-241">Deep-linking</span></span>  
*   [<span data-ttu-id="84124-242">Test entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="84124-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="84124-243">Implémenter des pratiques de validation et de test telles [que Webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="84124-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <a name="see-also"></a><span data-ttu-id="84124-244">Voir également</span><span class="sxs-lookup"><span data-stu-id="84124-244">See also</span></span>  

*   [<span data-ttu-id="84124-245">Applications web progressives sur des documents web MDN</span><span class="sxs-lookup"><span data-stu-id="84124-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="84124-246">Applications web progressives sur web.dev</span><span class="sxs-lookup"><span data-stu-id="84124-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="84124-247">[Lecteurs d’actualités][HackerNewsProgressiveWebApps] de piratage en tant qu’applications web progressives : compare les différentes infrastructure et modèles de performances pour l’implémentation d’un exemple \(Lecteur Actualités du pirate\) PWA.</span><span class="sxs-lookup"><span data-stu-id="84124-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="84124-248">#A0</span><span class="sxs-lookup"><span data-stu-id="84124-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="84124-249">Une feuille de route progressive pour votre application web progressive</span><span class="sxs-lookup"><span data-stu-id="84124-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="84124-250">Posts hors connexion avec applications web progressives</span><span class="sxs-lookup"><span data-stu-id="84124-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="84124-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="84124-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="84124-252">Se menter sur le Web</span><span class="sxs-lookup"><span data-stu-id="84124-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="84124-253">Attribution de noms aux applications web progressives</span><span class="sxs-lookup"><span data-stu-id="84124-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="84124-254">Conception et création d’une application Web progressive sans infrastructure (partie 1)</span><span class="sxs-lookup"><span data-stu-id="84124-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="84124-255">Conception et création d’une application Web progressive sans infrastructure (partie 2)</span><span class="sxs-lookup"><span data-stu-id="84124-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="84124-256">Conception et création d’une application Web progressive sans infrastructure (partie 3)</span><span class="sxs-lookup"><span data-stu-id="84124-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Déployer une application Node.js azure avec Visual Studio code | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer des comptes azure gratuits | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Web Apps | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications web dans Microsoft Edge | Windows Blogs"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Test gratuit du navigateur Microsoft Edge sur Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Une feuille de route progressive pour votre application web progressive"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "#A0 – Nouvelle édition Edge"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Générateur d’applications Express | Express" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Attribution de noms aux applications web progressives"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs d’actualités sur les pirates en tant qu’applications web progressives"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Se menter sur le Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notifications API | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications web progressives \(PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Api Push | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "| PushManager MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker API | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utilisation du service Workers | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Contenu du manifeste d’application | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Posts hors connexion avec applications web progressives"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoi de notifications WebPush identifiées par VAPID via le service Push de Mozilla | Mozilla Services"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "web-push | npm"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "encrypt(userPublicKey, userAuth, payload, contentEncoding) - web-push | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation - web-push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications web progressives"  

[PwaBuilder]: https://www.pwabuilder.com "Générateur PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Service Worker | Générateur PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push Rich Demo | ServiceWorker Cookbook"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Conception et création d’une application Web progressive sans infrastructure (partie 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Conception et création d’une application Web progressive sans infrastructure (partie 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Conception et création d’une application Web progressive sans infrastructure (partie 3)"  

[VapidkeysMain]: https://vapidkeys.com "Sécuriser le générateur de clés VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications web progressives | web.dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Améliorations progressives | Wikipedia"  
