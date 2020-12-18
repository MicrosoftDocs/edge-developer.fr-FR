---
description: Ce guide vous donne une vue d’ensemble des notions de base de Windows Store et des outils de création d’applications Web progressives (chrome) sur Windows.
title: Commencer à utiliser les applications Web progressives (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/02/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, PWABuilder, le manifeste Web, le travailleur de service, l’émission
ms.openlocfilehash: 7ad13f98f54c52891681d7591b21503c9d5825ff
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231222"
---
# <span data-ttu-id="193bb-104">Commencer à utiliser les applications Web progressives (chrome)</span><span class="sxs-lookup"><span data-stu-id="193bb-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="193bb-105">Les applications Web progressives \ (PWAs) sont des applications Web qui sont [progressivement améliorées][WikiProgressiveEnhancement].</span><span class="sxs-lookup"><span data-stu-id="193bb-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement].</span></span>  <span data-ttu-id="193bb-106">Les améliorations progressives incluent les fonctionnalités d’application, telles que l’installation, la prise en charge hors ligne et les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="193bb-106">The progressive enhancements include app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="193bb-107">Vous pouvez également empaqueter vos magasins d’applications PWA.</span><span class="sxs-lookup"><span data-stu-id="193bb-107">You may also package your PWA for app stores.</span></span>  <span data-ttu-id="193bb-108">Les magasins d’applications possibles incluent le Microsoft Store, Google Play, Mac App Store, etc.</span><span class="sxs-lookup"><span data-stu-id="193bb-108">Possible app stores include the Microsoft Store, Google Play, Mac App Store, and more.</span></span>  <span data-ttu-id="193bb-109">Le Microsoft Store est le magasin d’applications commercial intégré à Windows 10.</span><span class="sxs-lookup"><span data-stu-id="193bb-109">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="193bb-110">Le guide suivant vous donne une vue d’ensemble des concepts de base de la création de Project Web App et l’étend en tant que PWA.</span><span class="sxs-lookup"><span data-stu-id="193bb-110">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="193bb-111">Le projet finalisé fonctionne sur les navigateurs modernes.</span><span class="sxs-lookup"><span data-stu-id="193bb-111">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="193bb-112">Vous pouvez utiliser [PWABuilder][PwaBuilder] pour créer une nouvelle application Project Web App, améliorer votre version Web.</span><span class="sxs-lookup"><span data-stu-id="193bb-112">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="193bb-113">Prérequis</span><span class="sxs-lookup"><span data-stu-id="193bb-113">Prerequisites</span></span>  

*   <span data-ttu-id="193bb-114">Utilisez le [code Visual Studio][VisualstudioCodeMain] pour modifier votre code source PWA.</span><span class="sxs-lookup"><span data-stu-id="193bb-114">Use [Visual Studio Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="193bb-115">Utilisez [Node.js][NodejsMain] comme serveur Web local.</span><span class="sxs-lookup"><span data-stu-id="193bb-115">Use [Node.js][NodejsMain] as your local web server.</span></span>  
    
## <span data-ttu-id="193bb-116">Créer une application Web de base</span><span class="sxs-lookup"><span data-stu-id="193bb-116">Create a basic web app</span></span>  

<span data-ttu-id="193bb-117">Pour créer une application Web vide, suivez les étapes décrites dans l’article [Générateur d’applications de nœud][ExpressjsApplicationGenerator]et nommez votre application `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="193bb-117">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="193bb-118">Dans l’invite, exécutez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="193bb-118">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="193bb-119">Les commandes créent une application Web vide et installent des dépendances.</span><span class="sxs-lookup"><span data-stu-id="193bb-119">The commands create an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="193bb-120">Vous disposez maintenant d’une application Web simple et fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="193bb-120">You now have a simple, functional web app.</span></span>  <span data-ttu-id="193bb-121">Pour démarrer votre application Web, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="193bb-121">To start your web app, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="193bb-122">Rendez- `http://localhost:3000` vous sur pour afficher votre nouvelle application Web.</span><span class="sxs-lookup"><span data-stu-id="193bb-122">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Exécution de votre nouveau PWA sur localhost" lightbox="./media/vs-nodejs-express-index.png":::
   <span data-ttu-id="193bb-124">Exécution de votre nouveau PWA sur localhost</span><span class="sxs-lookup"><span data-stu-id="193bb-124">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="193bb-125">Commencer à créer un PWA</span><span class="sxs-lookup"><span data-stu-id="193bb-125">Get started building a PWA</span></span>  

<span data-ttu-id="193bb-126">À présent que vous disposez d’une application Web simple, étendez-la en tant que PWA en ajoutant les trois conditions requises pour PWAs</span><span class="sxs-lookup"><span data-stu-id="193bb-126">Now that you have a simple web app, extend it as a PWA by adding the three requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="193bb-127">: [Https](#step-1---use-https), manifeste d’une [application Web](#step-2---create-a-web-app-manifest)et [travailleur de service](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="193bb-127">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="193bb-128">Étape 1: utiliser HTTPs</span><span class="sxs-lookup"><span data-stu-id="193bb-128">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="193bb-129">Les principales parties de la plateforme PWA, telles que les [travailleurs de service][MDNServiceWorkerApi], nécessitent l’utilisation de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="193bb-129">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="193bb-130">Lorsque vous avez atteint la mise en service de Project Web App, vous devez la publier sur une URL HTTPs.</span><span class="sxs-lookup"><span data-stu-id="193bb-130">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="193bb-131">Pour le débogage, Microsoft Edge permet également `http://localhost` d’utiliser les API PWA.</span><span class="sxs-lookup"><span data-stu-id="193bb-131">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="193bb-132">[Publiez votre application Web en tant que site en ligne][VisualStudioNodejsTutorialPublishAzureAppService], mais assurez-vous que votre serveur est configuré pour HTTPS.</span><span class="sxs-lookup"><span data-stu-id="193bb-132">[Publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService], but ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="193bb-133">Par exemple, vous pouvez créer un [compte gratuit Azure][AzureCreateFreeAccount].</span><span class="sxs-lookup"><span data-stu-id="193bb-133">For example, you may create an [Azure free account][AzureCreateFreeAccount].</span></span>  <span data-ttu-id="193bb-134">Hébergez votre site sur le [service Microsoft Azure App][AzureWebApps] et il est desservi par défaut par le biais de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="193bb-134">Host your site on the [Microsoft Azure App Service][AzureWebApps] and it is served over HTTPS by default.</span></span>  

<span data-ttu-id="193bb-135">Le guide suivant, `http://localhost` qui vous permet de créer votre PWA.</span><span class="sxs-lookup"><span data-stu-id="193bb-135">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="193bb-136">Étape 2: créer un manifeste de l’application Web</span><span class="sxs-lookup"><span data-stu-id="193bb-136">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="193bb-137">Le [manifeste d’une application Web][MDNWebAppManifest] est un fichier JSON contenant les métadonnées relatives à votre application, telles que le nom, la description, les icônes, etc.</span><span class="sxs-lookup"><span data-stu-id="193bb-137">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="193bb-138">Pour ajouter un manifeste d’application à l’application Web:</span><span class="sxs-lookup"><span data-stu-id="193bb-138">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="193bb-139">Dans le code Visual Studio, choisissez **fichier**  >  **ouvrir le dossier** , puis sélectionnez le `MySamplePwa` répertoire que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="193bb-139">In Visual Studio Code, choose **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="193bb-140">Sélectionnez `Ctrl` + `N` pour créer un fichier, puis collez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="193bb-140">Select `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="193bb-141">Enregistrez le fichier sous `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="193bb-141">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="193bb-142">Ajoutez une image d’icône d’application 512x512 nommée `icon512.png` à `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="193bb-142">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="193bb-143">Vous pouvez utiliser l' [exemple d’image][ImagePwa] à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="193bb-143">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="193bb-144">Dans le code Visual Studio, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.</span><span class="sxs-lookup"><span data-stu-id="193bb-144">In Visual Studio Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="193bb-145">Étape 3: ajouter un travailleur de service</span><span class="sxs-lookup"><span data-stu-id="193bb-145">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="193bb-146">Les travailleurs de service sont la technologie clé de PWAs, qui permet de prendre en charge les scénarios tels que la prise en charge hors connexion, la mise en cache avancée et l’exécution des tâches en arrière-plan précédemment limitées</span><span class="sxs-lookup"><span data-stu-id="193bb-146">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="193bb-147">Les travailleurs de service sont des tâches en arrière-plan qui interceptent les requêtes réseau de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="193bb-147">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="193bb-148">Les travailleurs de service essaient d’exécuter des tâches, même si votre ordinateur n’est pas en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="193bb-148">Service workers attempt to complete tasks, even when your PWA is not running.</span></span>  <span data-ttu-id="193bb-149">Les tâches incluent les actions suivantes.</span><span class="sxs-lookup"><span data-stu-id="193bb-149">Tasks include the following actions.</span></span>  

*   <span data-ttu-id="193bb-150">Service des ressources demandées à partir d’un cache</span><span class="sxs-lookup"><span data-stu-id="193bb-150">Serving requested resources from a cache</span></span>  
*   <span data-ttu-id="193bb-151">Envoyer des notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="193bb-151">Sending push notifications</span></span>  
*   <span data-ttu-id="193bb-152">Exécution des tâches de récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="193bb-152">Running background fetch tasks</span></span>  
*   <span data-ttu-id="193bb-153">Icônes de badge</span><span class="sxs-lookup"><span data-stu-id="193bb-153">Badging icons</span></span>  
*   <span data-ttu-id="193bb-154">et bien plus encore</span><span class="sxs-lookup"><span data-stu-id="193bb-154">and more</span></span>  
    
<span data-ttu-id="193bb-155">Les travailleurs de service sont définis dans un fichier spécial JavaScript.</span><span class="sxs-lookup"><span data-stu-id="193bb-155">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="193bb-156">Pour plus d’informations, accédez à [utiliser les travailleurs de service][MDNUsingServiceWorkers] et les API du travailleur du [service][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="193bb-156">For more information, navigate to [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="193bb-157">Pour créer un Worker Worker dans votre projet, utilisez la recette du travailleur du service de première connexion de service de **mise en cache** du [Générateur PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="193bb-157">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="193bb-158">Accédez à [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], sélectionnez le travailleur **du service de premier réseau de mise en cache** , puis cliquez sur le bouton **Télécharger** .</span><span class="sxs-lookup"><span data-stu-id="193bb-158">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="193bb-159">Le fichier téléchargé contient les fichiers suivants:</span><span class="sxs-lookup"><span data-stu-id="193bb-159">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
        
1.  <span data-ttu-id="193bb-160">Copiez les fichiers téléchargés dans le `public` dossier de votre projet d’application Web.</span><span class="sxs-lookup"><span data-stu-id="193bb-160">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
1.  <span data-ttu-id="193bb-161">Dans le code Visual Studio, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.</span><span class="sxs-lookup"><span data-stu-id="193bb-161">In Visual Studio Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="193bb-162">Pour l’instant, votre application Web utilise un service d’assistance qui utilise la stratégie d’abord de cache.</span><span class="sxs-lookup"><span data-stu-id="193bb-162">Your web app now has a service worker that uses the cache-first strategy.</span></span>  <span data-ttu-id="193bb-163">Le nouveau travailleur de service extrait les ressources du cache en premier, et à partir du réseau uniquement selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="193bb-163">You new service worker fetches resources from the cache first, and from the network only as needed.</span></span>  <span data-ttu-id="193bb-164">Les ressources mises en cache incluent des images, JavaScript, CSS et HTML.</span><span class="sxs-lookup"><span data-stu-id="193bb-164">Cached resources include images, JavaScript, CSS, and HTML.</span></span>

<span data-ttu-id="193bb-165">Procédez comme suit pour vérifier que votre travailleur de service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="193bb-165">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="193bb-166">Accédez à votre application Web à l’aide de `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="193bb-166">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="193bb-167">Si votre application Web n’est pas disponible, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="193bb-167">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="193bb-168">Dans Microsoft Edge, sélectionnez `F12` pour ouvrir Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="193bb-168">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="193bb-169">Sélectionnez **application**, puis **travailleurs de service** pour afficher les travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="193bb-169">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="193bb-170">Si le travailleur de service n’est pas affiché, actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="193bb-170">If the service worker is not displayed, refresh the page.</span></span>  
    
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Vue d’ensemble des travailleurs de service Microsoft Edge DevTools" lightbox="./media/devtools-sw-overview.png":::
       <span data-ttu-id="193bb-172">Vue d’ensemble des travailleurs de service Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="193bb-172">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="193bb-173">Affichez le cache du travailleur de service en développant **stockage du cache** et sélectionnez **pwabuilder-cache**.</span><span class="sxs-lookup"><span data-stu-id="193bb-173">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="193bb-174">Toutes les ressources mises en cache par le travailleur de service doivent être affichées.</span><span class="sxs-lookup"><span data-stu-id="193bb-174">All of the resources cached by the service worker should be displayed.</span></span>  <span data-ttu-id="193bb-175">Les ressources mises en cache par le travailleur de service incluent l’icône d’application, le manifeste de l’application, les fichiers CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="193bb-175">The resources cached by the service worker include the app icon, app manifest, CSS, and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache du travailleur de service dans Microsoft Edge DevTools" lightbox="./media/devtools-cache.png":::
       <span data-ttu-id="193bb-177">Cache du travailleur de service dans Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="193bb-177">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="193bb-178">Essayez votre application PWA en tant qu’application en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="193bb-178">Try your PWA as an offline app.</span></span>  <span data-ttu-id="193bb-179">Dans Microsoft Edge DevTools \ ( `F12` \), cliquez sur **réseau** , puis \*\*\*\* définissez l’état de **connexion sur hors connexion**.</span><span class="sxs-lookup"><span data-stu-id="193bb-179">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Définir l’application en mode hors connexion dans Microsoft Edge DevTools" lightbox="./media/devtools-offline.png":::
       <span data-ttu-id="193bb-181">Définir l’application en mode hors connexion dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="193bb-181">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="193bb-182">Actualisez votre application pour qu’elle affiche le mécanisme hors connexion pour le service des ressources de votre application à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="193bb-182">Refresh your app and it should display the offline mechanism for serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA exécuté hors connexion" lightbox="./media/vs-nodejs-express-index.png":::
       <span data-ttu-id="193bb-184">PWA exécuté hors connexion</span><span class="sxs-lookup"><span data-stu-id="193bb-184">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="193bb-185">Ajouter des notifications de transmission à votre PWA</span><span class="sxs-lookup"><span data-stu-id="193bb-185">Add push notifications to your PWA</span></span>  

<span data-ttu-id="193bb-186">Vous pouvez créer des PWAs qui prennent en charge les notifications de transmission en effectuant les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="193bb-186">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="193bb-187">S’abonner à un service de messagerie à l’aide de l' [API de transmission][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="193bb-187">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="193bb-188">Afficher un message Toast lors de la réception d’un message du service à l’aide de l' [API notifications][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="193bb-188">Display a toast message when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  
    
<span data-ttu-id="193bb-189">Comme pour les travailleurs de service, les API de notifications de transmission d’API sont des API basées sur des normes.</span><span class="sxs-lookup"><span data-stu-id="193bb-189">Just like with Service Workers, the push notification APIs are standards-based APIs.</span></span>  <span data-ttu-id="193bb-190">Comme les API de notifications de transmission fonctionnent entre les navigateurs, votre code doit fonctionner partout où PWAs est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="193bb-190">The push notification APIs work across browsers, so your code should work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="193bb-191">Pour plus d’informations sur la distribution de messages de type pousser vers différents navigateurs sur votre serveur, accédez à la section [Web-Poussée][NPMWebPush].</span><span class="sxs-lookup"><span data-stu-id="193bb-191">For more information about delivering push messages to different browsers on your server, navigate to [Web-Push][NPMWebPush].</span></span>  

<span data-ttu-id="193bb-192">Les étapes ci-dessous ont été adaptées à partir du livre de recettes de travail complet du [travailleur de service][ServiceWorkerCookbookPushRichDemo] fourni par Mozilla, qui comporte un certain nombre d’autres recettes utiles pour les employés sur le Web et les services.</span><span class="sxs-lookup"><span data-stu-id="193bb-192">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="193bb-193">Étape 1: générer les clés de VAPID</span><span class="sxs-lookup"><span data-stu-id="193bb-193">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="193bb-194">Les notifications de transmission requièrent VAPID \ (application d’identification du serveur d’application) pour envoyer des messages envoyés au client de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="193bb-194">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="193bb-195">Plusieurs générateurs de clés VAPID sont disponibles en ligne (par exemple, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="193bb-195">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="193bb-196">Après la génération, vous devez obtenir un objet JSON contenant une clé publique et privée.</span><span class="sxs-lookup"><span data-stu-id="193bb-196">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="193bb-197">Enregistrez les clés pour les étapes ultérieures dans le didacticiel suivant.</span><span class="sxs-lookup"><span data-stu-id="193bb-197">Save the keys for later steps in the following tutorial.</span></span>  <span data-ttu-id="193bb-198">Pour plus d’informations sur VAPID et webpoussée, accédez à [Envoyer des notifications webtransmission identifiées par VAPID à l’aide du service Mozilla de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="193bb-198">For information about VAPID and WebPush, navigate to [Sending VAPID identified WebPush Notifications using the Mozilla Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="193bb-199">Étape 2: s’abonner aux notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="193bb-199">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="193bb-200">Les travailleurs de service gèrent les événements d’émission et les interactions de notification Toast dans votre PWA.</span><span class="sxs-lookup"><span data-stu-id="193bb-200">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="193bb-201">Pour abonner PWA aux notifications de transmission du serveur, assurez-vous que les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="193bb-201">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="193bb-202">Votre PWA est installé, actif et enregistré</span><span class="sxs-lookup"><span data-stu-id="193bb-202">Your PWA is installed, active, and registered</span></span>  
*   <span data-ttu-id="193bb-203">Votre code de réalisation de la tâche d’abonnement se trouve sur le thread d’interface utilisateur principal de PWA</span><span class="sxs-lookup"><span data-stu-id="193bb-203">Your code to complete the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="193bb-204">Vous avez une connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="193bb-204">You have network connectivity</span></span>  
    
<span data-ttu-id="193bb-205">Avant la création d’un nouvel abonnement envoyé, Microsoft Edge vérifie que l’utilisateur lui a accordé l’autorisation PWA de recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="193bb-205">Before a new push subscription is created, Microsoft Edge verifies if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="193bb-206">Si ce n’est pas le cas, l’utilisateur est invité par le navigateur à entrer une autorisation.</span><span class="sxs-lookup"><span data-stu-id="193bb-206">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="193bb-207">Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` lever a `DOMException` qui doit être gérée.</span><span class="sxs-lookup"><span data-stu-id="193bb-207">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="193bb-208">Pour plus d’informations sur la gestion des autorisations, accédez à [notifications de transmission dans Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="193bb-208">For more on permission management, navigate to [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="193bb-209">Dans votre `pwabuilder-sw-register.js` fichier, ajoutez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="193bb-209">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="193bb-210">Pour plus d’informations, accédez à [PushManager][MDNPushManager] et [Web-Poussée][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="193bb-210">For more information, navigate to [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="193bb-211">Étape 3: écouter les notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="193bb-211">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="193bb-212">Après avoir créé un abonnement dans votre PWA, ajoutez des gestionnaires au travailleur de service pour répondre aux événements de transmission.</span><span class="sxs-lookup"><span data-stu-id="193bb-212">After a subscription is created in your PWA, add handlers to the service worker to respond to push events.</span></span>  <span data-ttu-id="193bb-213">Un événement de type pousser est envoyé à partir du serveur pour afficher les notifications Toast.</span><span class="sxs-lookup"><span data-stu-id="193bb-213">Push event are sent from the server to display toast notifications.</span></span>  <span data-ttu-id="193bb-214">Notifications Toast affichent des données pour un message reçu.</span><span class="sxs-lookup"><span data-stu-id="193bb-214">Toast notifications display data for a received message.</span></span>  <span data-ttu-id="193bb-215">Pour effectuer les tâches suivantes, vous devez ajouter un gestionnaire de clic.</span><span class="sxs-lookup"><span data-stu-id="193bb-215">To complete the following tasks, you must add a click handler.</span></span>  

*   <span data-ttu-id="193bb-216">Ignorer la notification Toast</span><span class="sxs-lookup"><span data-stu-id="193bb-216">Dismiss the toast notification</span></span>  
*   <span data-ttu-id="193bb-217">Ouvrir, mettre au point ou ouvrir et sélectionner des fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="193bb-217">Open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="193bb-218">Ouvrir et focaliser une nouvelle fenêtre pour afficher une page client de Project Web App</span><span class="sxs-lookup"><span data-stu-id="193bb-218">Open and focus a new window to display a PWA client page</span></span>  
    
<span data-ttu-id="193bb-219">Dans votre `pwabuilder-sw.js` fichier, ajoutez les gestionnaires suivants.</span><span class="sxs-lookup"><span data-stu-id="193bb-219">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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

### <span data-ttu-id="193bb-220">Étape 4: testez-le</span><span class="sxs-lookup"><span data-stu-id="193bb-220">Step 4 - Try it out</span></span>  

<span data-ttu-id="193bb-221">Pour tester les notifications de transmission pour votre PWA, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="193bb-221">To test push notifications for your PWA, complete the following steps.</span></span>  

1.  <span data-ttu-id="193bb-222">Accédez à votre PWA à l’adresse `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="193bb-222">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="193bb-223">Lorsque le travailleur de votre service active et tente d’abonner votre PWA aux notifications de transmission, Microsoft Edge vous invite à autoriser votre PWA à afficher les notifications.</span><span class="sxs-lookup"><span data-stu-id="193bb-223">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="193bb-224">Sélectionnez **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="193bb-224">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Boîte de dialogue autorisation permettant d’activer les notifications" lightbox="./media/notification-permission.png":::
       <span data-ttu-id="193bb-226">Boîte de dialogue autorisation permettant d’activer les notifications</span><span class="sxs-lookup"><span data-stu-id="193bb-226">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="193bb-227">Simuler une notification de transmission côté serveur.</span><span class="sxs-lookup"><span data-stu-id="193bb-227">Simulate a server-side push notification.</span></span>  <span data-ttu-id="193bb-228">Avec votre PWA ouvert `http://localhost:3000` dans votre navigateur, sélectionnez `F12` pour ouvrir le devtools.</span><span class="sxs-lookup"><span data-stu-id="193bb-228">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="193bb-229">Sélectionnez \*\*\*\*  >  **Worker Worker Worker Worker**  >  \*\*\*\* pour envoyer une notification d’émission de test à votre application Project Web App.</span><span class="sxs-lookup"><span data-stu-id="193bb-229">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  
    
    :::row:::
       :::column span="":::
          <span data-ttu-id="193bb-230">Une notification de transmission doit s’afficher à proximité de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="193bb-230">A push notification should display near the taskbar.</span></span>  
          
          :::image type="complex" source="./media/devtools-push.png" alt-text="Pousser une notification de DevTools" lightbox="./media/devtools-push.png":::
             <span data-ttu-id="193bb-232">Pousser une notification de DevTools</span><span class="sxs-lookup"><span data-stu-id="193bb-232">Push a notification from DevTools</span></span>  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          <span data-ttu-id="193bb-233">Si vous ne sélectionnez pas \ (ou activer) une notification Toast, le système la ferme automatiquement après quelques secondes et la met en file d’attente dans votre centre de maintenance Windows.</span><span class="sxs-lookup"><span data-stu-id="193bb-233">If you do not select \(or activate\) a toast notification, the system automatically dismisses it after several seconds and queues it in your Windows Action Center.</span></span>  
          
          :::image type="complex" source="./media/windows-action-center.png" alt-text="Notifications dans le centre de notifications Windows" lightbox="./media/windows-action-center.png":::
             <span data-ttu-id="193bb-235">Notifications dans le centre de notifications Windows</span><span class="sxs-lookup"><span data-stu-id="193bb-235">Notifications in Windows Action Center</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::  
    
## <span data-ttu-id="193bb-236">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="193bb-236">Next steps</span></span>  

<span data-ttu-id="193bb-237">Les étapes suivantes incluent des tâches supplémentaires pour vous aider à comprendre la création de PWAss réalistes.</span><span class="sxs-lookup"><span data-stu-id="193bb-237">The following steps include additional tasks to help you understand building real-world PWAs.</span></span>  

*   <span data-ttu-id="193bb-238">Gérer et stocker des abonnements envoyés</span><span class="sxs-lookup"><span data-stu-id="193bb-238">Manage and store push subscriptions</span></span>  
*   <span data-ttu-id="193bb-239">[Chiffrer][NPMWebPushEncrypt] les données de charge utile</span><span class="sxs-lookup"><span data-stu-id="193bb-239">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*   <span data-ttu-id="193bb-240">Conception réactive</span><span class="sxs-lookup"><span data-stu-id="193bb-240">Responsive design</span></span>  
*   <span data-ttu-id="193bb-241">Liaison Poussée</span><span class="sxs-lookup"><span data-stu-id="193bb-241">Deep-linking</span></span>  
*   [<span data-ttu-id="193bb-242">Tests entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="193bb-242">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*   <span data-ttu-id="193bb-243">Mettre en œuvre des pratiques de validation et de test telles que [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="193bb-243">Implement validation and testing practices such as [Webhint][Webhint]</span></span>  
    
## <span data-ttu-id="193bb-244">Voir également</span><span class="sxs-lookup"><span data-stu-id="193bb-244">See also</span></span>  

*   [<span data-ttu-id="193bb-245">Applications Web progressives sur MDN Web docs</span><span class="sxs-lookup"><span data-stu-id="193bb-245">Progressive Web Apps on MDN web docs</span></span>][MDNProgressiveWebApps]  
*   [<span data-ttu-id="193bb-246">Applications Web progressives sur le Web. dev</span><span class="sxs-lookup"><span data-stu-id="193bb-246">Progressive Web Apps on web.dev</span></span>][WebDevProgressiveWebApps]  
*   <span data-ttu-id="193bb-247">[Lecteurs de News malveillants: applications Web progressives][HackerNewsProgressiveWebApps] -compare les différents types d’infrastructure et de performance permettant d’implémenter un exemple de version de Project</span><span class="sxs-lookup"><span data-stu-id="193bb-247">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  
*   [<span data-ttu-id="193bb-248">PWAs de combustion de mythe</span><span class="sxs-lookup"><span data-stu-id="193bb-248">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="193bb-249">Plan progressif de votre application Web progressive</span><span class="sxs-lookup"><span data-stu-id="193bb-249">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="193bb-250">Billets hors ligne avec des applications Web progressives</span><span class="sxs-lookup"><span data-stu-id="193bb-250">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="193bb-251">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="193bb-251">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="193bb-252">Paris sur le Web</span><span class="sxs-lookup"><span data-stu-id="193bb-252">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="193bb-253">Attribution d’un nom aux applications Web progressives</span><span class="sxs-lookup"><span data-stu-id="193bb-253">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="193bb-254">Conception et création d’une application Web progressive sans infrastructure (partie 1)</span><span class="sxs-lookup"><span data-stu-id="193bb-254">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="193bb-255">Conception et création d’une application Web progressive sans infrastructure (partie 2)</span><span class="sxs-lookup"><span data-stu-id="193bb-255">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="193bb-256">Conception et création d’une application Web progressive sans infrastructure (partie 3)</span><span class="sxs-lookup"><span data-stu-id="193bb-256">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Déploiement d’une application Node.js sur Azure avec du code Visual Studio | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer un compte gratuit Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Applications Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications Web dans Microsoft Edge | Blogs Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Tests gratuits du navigateur Microsoft Edge sur Windows 10 | BrowserStack"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Plan progressif de votre application Web progressive"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PWAs: la nouvelle version de Microsoft Edge"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Générateur d’application rapide | Explorer" 

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Attribution d’un nom aux applications Web progressives"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs de nouvelles pirates en application Web progressive"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Paris sur le Web"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications Web progressives (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utiliser des travailleurs de service | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Billets hors ligne avec des applications Web progressives"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoyer des notifications webtransmission identifiées par VAPID via le service pousser de Mozilla Services Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Poussée | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Poussée | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation-Web-Poussée | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications Web progressives"  

[PwaBuilder]: https://www.pwabuilder.com "Générateur PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Travailleur de service | Générateur PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Démonstration complète | Livre de ServiceWorker"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Conception et création d’une application Web progressive sans infrastructure (partie 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Conception et création d’une application Web progressive sans infrastructure (partie 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Conception et création d’une application Web progressive sans infrastructure (partie 3)"  

[VapidkeysMain]: https://vapidkeys.com "Générateur de clés sécurisées VAPID | VapidKeys" 

[Webhint]: https://webhint.io "webhint"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications Web progressives | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Amélioration progressive | Wikipédia"  
