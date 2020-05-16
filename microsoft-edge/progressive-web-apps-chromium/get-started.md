---
description: Ce guide vous donne une vue d’ensemble des notions de base et des outils de Project Web App pour créer des applications Web progressives sur Windows.
title: Commencer à utiliser les applications Web progressives (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: applications Web progressives, PWA, Edge, Windows, PWABuilder, le manifeste Web, le travailleur de service, l’émission
ms.openlocfilehash: 6c5fa5d6af8494f33e11a545d5dde1264604c787
ms.sourcegitcommit: 136642396bb8094a535e203067ee429e60d31d25
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/15/2020
ms.locfileid: "10659208"
---
# <span data-ttu-id="bf5da-104">Commencer à utiliser les applications Web progressives (chrome)</span><span class="sxs-lookup"><span data-stu-id="bf5da-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="bf5da-105">Les applications Web progressives (PWAs) sont des applications Web qui sont [progressivement améliorées][WikiProgressiveEnhancement] avec des fonctionnalités de type application, telles que l’installation, la prise en charge hors ligne et les notifications de transmission.</span><span class="sxs-lookup"><span data-stu-id="bf5da-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement] with app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="bf5da-106">Vous pouvez également empaqueter votre PWA pour les magasins d’applications, y compris le Microsoft Store ainsi que Google Play, Mac App Store et bien plus encore.</span><span class="sxs-lookup"><span data-stu-id="bf5da-106">You may also packaged your PWA for app stores, including the Microsoft Store as well as Google Play, Mac App Store and more.</span></span>  <span data-ttu-id="bf5da-107">Le Microsoft Store est le magasin d’applications commercial intégré à Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bf5da-107">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="bf5da-108">Le guide suivant vous donne une vue d’ensemble des concepts de base de la création de Project Web App et l’étend en tant que PWA.</span><span class="sxs-lookup"><span data-stu-id="bf5da-108">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="bf5da-109">Le projet finalisé fonctionne sur les navigateurs modernes.</span><span class="sxs-lookup"><span data-stu-id="bf5da-109">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="bf5da-110">Vous pouvez utiliser [PWABuilder][PwaBuilder] pour créer une nouvelle application Project Web App, améliorer votre version Web.</span><span class="sxs-lookup"><span data-stu-id="bf5da-110">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="bf5da-111">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="bf5da-111">Prerequisites</span></span>  

*   <span data-ttu-id="bf5da-112">Utilisez le [code vs][VisualstudioCodeMain] pour modifier votre code source PWA.</span><span class="sxs-lookup"><span data-stu-id="bf5da-112">Use [VS Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="bf5da-113">Utilisez [node. js][NodejsMain] comme serveur Web local.</span><span class="sxs-lookup"><span data-stu-id="bf5da-113">Use [Node.js][NodejsMain] as your local web server.</span></span>  

## <span data-ttu-id="bf5da-114">Configurer une application Web de base</span><span class="sxs-lookup"><span data-stu-id="bf5da-114">Set up a basic web app</span></span>  

<span data-ttu-id="bf5da-115">Pour créer une application Web vide, suivez les étapes décrites dans l’article [Générateur d’applications de nœud][ExpressjsApplicationGenerator]et nommez votre application `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="bf5da-115">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="bf5da-116">Dans l’invite, exécutez les commandes suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf5da-116">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="bf5da-117">Les commandes créent une application Web vide et installent des dépendances.</span><span class="sxs-lookup"><span data-stu-id="bf5da-117">The commands creates an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="bf5da-118">Vous disposez maintenant d’une application Web simple et fonctionnelle.</span><span class="sxs-lookup"><span data-stu-id="bf5da-118">Now you have a simple, functional web app.</span></span>  <span data-ttu-id="bf5da-119">Pour commencer, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="bf5da-119">To start it, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="bf5da-120">Rendez- `http://localhost:3000` vous sur pour afficher votre nouvelle application Web.</span><span class="sxs-lookup"><span data-stu-id="bf5da-120">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Exécution de votre nouveau PWA sur localhost":::
   <span data-ttu-id="bf5da-122">Exécution de votre nouveau PWA sur localhost</span><span class="sxs-lookup"><span data-stu-id="bf5da-122">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="bf5da-123">Commencer à créer un PWA</span><span class="sxs-lookup"><span data-stu-id="bf5da-123">Get started building a PWA</span></span>  

<span data-ttu-id="bf5da-124">À présent que vous disposez d’une application Web simple, étendez-la en tant que PWA en ajoutant les 3 conditions requises pour PWAs</span><span class="sxs-lookup"><span data-stu-id="bf5da-124">Now that you have a simple web app, extend it as a PWA by adding the 3 requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="bf5da-125">: [Https](#step-1---use-https), manifeste d’une [application Web](#step-2---create-a-web-app-manifest)et [travailleur de service](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="bf5da-125">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="bf5da-126">Étape 1: utiliser HTTPs</span><span class="sxs-lookup"><span data-stu-id="bf5da-126">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="bf5da-127">Les principales parties de la plateforme PWA, telles que les [travailleurs de service][MDNServiceWorkerApi], nécessitent l’utilisation de HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bf5da-127">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="bf5da-128">Lorsque vous avez atteint la mise en service de Project Web App, vous devez la publier sur une URL HTTPs.</span><span class="sxs-lookup"><span data-stu-id="bf5da-128">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="bf5da-129">Pour le débogage, Microsoft Edge permet également `http://localhost` d’utiliser les API PWA.</span><span class="sxs-lookup"><span data-stu-id="bf5da-129">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="bf5da-130">Si vous [publiez votre application Web en tant que site actif][VisualStudioNodejsTutorialPublishAzureAppService] (par exemple, en installant un [compte gratuit Azure][AzureCreateFreeAccount]), vous devez vous assurer que votre serveur est configuré pour HTTPS.</span><span class="sxs-lookup"><span data-stu-id="bf5da-130">If you [publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="bf5da-131">Si vous utilisez le [service Microsoft Azure App][AzureWebApps] pour héberger votre site, il est desservi par défaut par défaut.</span><span class="sxs-lookup"><span data-stu-id="bf5da-131">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="bf5da-132">Le guide suivant, `http://localhost` qui vous permet de créer votre PWA.</span><span class="sxs-lookup"><span data-stu-id="bf5da-132">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="bf5da-133">Étape 2: créer un manifeste de l’application Web</span><span class="sxs-lookup"><span data-stu-id="bf5da-133">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="bf5da-134">Le [manifeste d’une application Web][MDNWebAppManifest] est un fichier JSON contenant les métadonnées relatives à votre application, telles que le nom, la description, les icônes, etc.</span><span class="sxs-lookup"><span data-stu-id="bf5da-134">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="bf5da-135">Pour ajouter un manifeste d’application à l’application Web:</span><span class="sxs-lookup"><span data-stu-id="bf5da-135">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="bf5da-136">Dans le code vs, **File**accédez  >  au**dossier ouverture** du fichier et sélectionnez le `MySamplePwa` répertoire que vous avez créé précédemment.</span><span class="sxs-lookup"><span data-stu-id="bf5da-136">In VS Code, go **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="bf5da-137">Appuyez sur `Ctrl` + `N` pour créer un fichier, puis collez-le dans l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="bf5da-137">Press `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
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
    
1.  <span data-ttu-id="bf5da-138">Enregistrez le fichier sous `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="bf5da-138">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="bf5da-139">Ajoutez une image d’icône d’application 512x512 nommée `icon512.png` à `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="bf5da-139">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="bf5da-140">Vous pouvez utiliser l' [exemple d’image][ImagePwa] à des fins de test.</span><span class="sxs-lookup"><span data-stu-id="bf5da-140">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="bf5da-141">Dans le code VS, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.</span><span class="sxs-lookup"><span data-stu-id="bf5da-141">In VS Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="bf5da-142">Étape 3: ajouter un travailleur de service</span><span class="sxs-lookup"><span data-stu-id="bf5da-142">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="bf5da-143">Les travailleurs de service sont la technologie clé de PWAs, qui permet de prendre en charge les scénarios tels que la prise en charge hors connexion, la mise en cache avancée et l’exécution des tâches en arrière-plan précédemment limitées</span><span class="sxs-lookup"><span data-stu-id="bf5da-143">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="bf5da-144">Les travailleurs de service sont des tâches en arrière-plan qui interceptent les requêtes réseau de votre application Web.</span><span class="sxs-lookup"><span data-stu-id="bf5da-144">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="bf5da-145">Ces derniers effectuent des tâches, même lorsque votre PWA n’est pas en cours d’exécution, comme le service des ressources demandées à partir d’un cache, l’envoi de notifications de transmission, l’exécution de tâches de récupération en arrière-plan, d’icônes badge, etc.</span><span class="sxs-lookup"><span data-stu-id="bf5da-145">They perform tasks, even when your PWA is not running, such as serving requested resources from a cache, sending push notifications, running background fetch tasks, badging icons, and so on.</span></span>  <span data-ttu-id="bf5da-146">Les travailleurs de service sont définis dans un fichier spécial JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf5da-146">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="bf5da-147">Pour plus d’informations, voir [utilisation des travailleurs de service][MDNUsingServiceWorkers] et des API du travailleur du [service][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="bf5da-147">For more information, see [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="bf5da-148">Pour créer un Worker Worker dans votre projet, utilisez la recette du travailleur du service de première connexion de service de **mise en cache** du [Générateur PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="bf5da-148">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="bf5da-149">Accédez à [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], sélectionnez le travailleur **du service de premier réseau de mise en cache** , puis cliquez sur le bouton **Télécharger** .</span><span class="sxs-lookup"><span data-stu-id="bf5da-149">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="bf5da-150">Le fichier téléchargé contient les fichiers suivants:</span><span class="sxs-lookup"><span data-stu-id="bf5da-150">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  <span data-ttu-id="bf5da-151">Copiez les fichiers téléchargés dans le `public` dossier de votre projet d’application Web.</span><span class="sxs-lookup"><span data-stu-id="bf5da-151">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
    
1.  <span data-ttu-id="bf5da-152">Dans le code VS, ouvrez `/public/index.html` et ajoutez l’extrait de code suivant à l’intérieur de la `<head>` balise.</span><span class="sxs-lookup"><span data-stu-id="bf5da-152">In VS Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="bf5da-153">Votre application Web possède désormais un service Worker qui fait appel à la stratégie de mise en cache prioritaire, qui extrait d’abord les ressources telles que les images, JS, CSS et HTML du cache, et repasse au réseau selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="bf5da-153">Your web app now has a service worker that uses the cache-first strategy, which fetches resources like images, JS, CSS, and HTML from the cache first, and falls back to the network as needed.</span></span>  

<span data-ttu-id="bf5da-154">Procédez comme suit pour vérifier que votre travailleur de service s’exécute.</span><span class="sxs-lookup"><span data-stu-id="bf5da-154">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="bf5da-155">Accédez à votre application Web à l’aide de `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="bf5da-155">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="bf5da-156">Si votre application Web n’est pas disponible, exécutez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="bf5da-156">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="bf5da-157">Dans Microsoft Edge, sélectionnez `F12` pour ouvrir Microsoft Edge devtools.</span><span class="sxs-lookup"><span data-stu-id="bf5da-157">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="bf5da-158">Sélectionnez **application**, puis **travailleurs de service** pour afficher les travailleurs de service.</span><span class="sxs-lookup"><span data-stu-id="bf5da-158">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="bf5da-159">Si vous ne voyez pas le travailleur de service, il est possible que vous deviez actualiser la page.</span><span class="sxs-lookup"><span data-stu-id="bf5da-159">If you do not see the service worker, you may need to refresh the page.</span></span>  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Vue d’ensemble des travailleurs de service Microsoft Edge DevTools":::
       <span data-ttu-id="bf5da-161">Vue d’ensemble des travailleurs de service Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bf5da-161">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="bf5da-162">Affichez le cache du travailleur de service en développant **stockage du cache** et sélectionnez **pwabuilder-cache**.</span><span class="sxs-lookup"><span data-stu-id="bf5da-162">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="bf5da-163">Vous devez voir toutes les ressources mises en cache par le travailleur du service, telles que l’icône de l’application, le manifeste de l’application, les fichiers CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf5da-163">You should see all the resources cached by the service worker, such as the app icon, app manifest, CSS and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Cache du travailleur de service dans Microsoft Edge DevTools":::
       <span data-ttu-id="bf5da-165">Cache du travailleur de service dans Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="bf5da-165">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="bf5da-166">Essayez votre application PWA en tant qu’application en mode hors connexion.</span><span class="sxs-lookup"><span data-stu-id="bf5da-166">Try your PWA as an offline app.</span></span>  <span data-ttu-id="bf5da-167">Dans Microsoft Edge DevTools \ ( `F12` \), cliquez sur **réseau** , puis **Online** définissez l’état de **connexion sur hors connexion**.</span><span class="sxs-lookup"><span data-stu-id="bf5da-167">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Définir l’application en mode hors connexion dans Microsoft Edge DevTools":::
       <span data-ttu-id="bf5da-169">Définir l’application en mode hors connexion dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="bf5da-169">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="bf5da-170">Actualisez votre application pour pouvoir la voir travailler hors connexion en utilisant les ressources de votre application à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="bf5da-170">Refresh your app and you should see it working offline by serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA exécuté hors connexion":::
       <span data-ttu-id="bf5da-172">PWA exécuté hors connexion</span><span class="sxs-lookup"><span data-stu-id="bf5da-172">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="bf5da-173">Ajouter des notifications de transmission à votre PWA</span><span class="sxs-lookup"><span data-stu-id="bf5da-173">Add push notifications to your PWA</span></span>  

<span data-ttu-id="bf5da-174">Vous pouvez créer des PWAs qui prennent en charge les notifications de transmission en effectuant les tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf5da-174">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="bf5da-175">S’abonner à un service de messagerie à l’aide de l' [API de transmission][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="bf5da-175">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="bf5da-176">Afficher des messages toast lors de la réception d’un message du service à l’aide de l' [API notifications][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="bf5da-176">Display a toast messages when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  

<span data-ttu-id="bf5da-177">Comme pour les travailleurs de service, il s’agit d’API normalisées qui fonctionnent avec tous les navigateurs, de sorte que vous n’avez à écrire le code qu’une seule fois pour fonctionner partout où PWAs est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="bf5da-177">As with Service Workers, these are standards-based APIs that work across browsers, so you only have to write the code once for it to work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="bf5da-178">Pour plus d’informations sur la distribution de messages de type pousser vers différents navigateurs sur votre serveur, utilisez la bibliothèque open-source sur le [Web][NPMWebPush] .</span><span class="sxs-lookup"><span data-stu-id="bf5da-178">For more information on delivering push messages to different browsers on your server, use the [Web-Push][NPMWebPush] open-source library.</span></span>  

<span data-ttu-id="bf5da-179">Les étapes ci-dessous ont été adaptées à partir du livre de recettes de travail complet du [travailleur de service][ServiceWorkerCookbookPushRichDemo] fourni par Mozilla, qui comporte un certain nombre d’autres recettes utiles pour les employés sur le Web et les services.</span><span class="sxs-lookup"><span data-stu-id="bf5da-179">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="bf5da-180">Étape 1: générer les clés de VAPID</span><span class="sxs-lookup"><span data-stu-id="bf5da-180">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="bf5da-181">Les notifications de transmission requièrent VAPID \ (application d’identification du serveur d’application) pour envoyer des messages envoyés au client de Project Web App.</span><span class="sxs-lookup"><span data-stu-id="bf5da-181">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="bf5da-182">Plusieurs générateurs de clés VAPID sont disponibles en ligne (par exemple, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="bf5da-182">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="bf5da-183">Après la génération, vous devez obtenir un objet JSON contenant une clé publique et privée.</span><span class="sxs-lookup"><span data-stu-id="bf5da-183">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="bf5da-184">Enregistrez les clés pour les étapes suivantes dans le didacticiel suivant.</span><span class="sxs-lookup"><span data-stu-id="bf5da-184">Save the keys for subsequent steps in the following tutorial.</span></span>  <span data-ttu-id="bf5da-185">Pour plus d’informations sur le fonctionnement de VAPID et de webpousser, voir [envoi de notifications webtravers de Mozilla par le biais du service pousser de Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="bf5da-185">For information on how VAPID and WebPush works, see [Sending VAPID identified WebPush Notifications via Mozilla's Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="bf5da-186">Étape 2: s’abonner aux notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="bf5da-186">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="bf5da-187">Les travailleurs de service gèrent les événements d’émission et les interactions de notification Toast dans votre PWA.</span><span class="sxs-lookup"><span data-stu-id="bf5da-187">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="bf5da-188">Pour abonner PWA aux notifications de transmission du serveur, assurez-vous que les conditions suivantes sont remplies.</span><span class="sxs-lookup"><span data-stu-id="bf5da-188">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="bf5da-189">Votre PWA est installé, actif et inscrit</span><span class="sxs-lookup"><span data-stu-id="bf5da-189">Your PWA is installed, active and registered</span></span>  
*   <span data-ttu-id="bf5da-190">Votre code qui exécute la tâche d’abonnement se trouve sur le thread d’interface utilisateur principal de PWA.</span><span class="sxs-lookup"><span data-stu-id="bf5da-190">Your code that performs the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="bf5da-191">Vous avez une connectivité réseau</span><span class="sxs-lookup"><span data-stu-id="bf5da-191">You have network connectivity</span></span>  

<span data-ttu-id="bf5da-192">Avant de créer un nouvel abonnement envoyé, Microsoft Edge vérifie que l’utilisateur lui a accordé l’autorisation PWA pour recevoir des notifications.</span><span class="sxs-lookup"><span data-stu-id="bf5da-192">Before a new push subscription is created, Microsoft Edge checks if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="bf5da-193">Si ce n’est pas le cas, l’utilisateur est invité par le navigateur à entrer une autorisation.</span><span class="sxs-lookup"><span data-stu-id="bf5da-193">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="bf5da-194">Si l’autorisation est refusée, la demande de `registration.pushManager.subscribe` lever a `DOMException` qui doit être gérée.</span><span class="sxs-lookup"><span data-stu-id="bf5da-194">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="bf5da-195">Pour plus d’informations sur la gestion des autorisations, voir [notifications de transmission dans Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="bf5da-195">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="bf5da-196">Dans votre `pwabuilder-sw-register.js` fichier, ajoutez l’extrait de code suivant.</span><span class="sxs-lookup"><span data-stu-id="bf5da-196">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

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

<span data-ttu-id="bf5da-197">Pour plus d’informations, voir [PushManager][MDNPushManager] et [Web-Poussée][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="bf5da-197">For more information, see [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="bf5da-198">Étape 3: écouter les notifications de transmission</span><span class="sxs-lookup"><span data-stu-id="bf5da-198">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="bf5da-199">À présent qu’un abonnement est configuré dans votre PWA, ajoutez des gestionnaires au travailleur de service pour répondre aux événements de transmission \ (envoyés à partir du serveur \) pour afficher les notifications toast avec les données d’un message reçu.</span><span class="sxs-lookup"><span data-stu-id="bf5da-199">Now that a subscription is set up in your PWA, add handlers to the service worker to respond to push events \(sent from the server\) to display toast notifications with the data of a received message.</span></span>  <span data-ttu-id="bf5da-200">Vous devez ajouter un gestionnaire de Click pour effectuer l’une des tâches suivantes.</span><span class="sxs-lookup"><span data-stu-id="bf5da-200">You must add a click handler to perform the any of the following tasks.</span></span>  
*   <span data-ttu-id="bf5da-201">ignorer la notification Toast</span><span class="sxs-lookup"><span data-stu-id="bf5da-201">dismiss the toast notification</span></span>  
*   <span data-ttu-id="bf5da-202">ouvrir, mettre au point ou ouvrir et sélectionner des fenêtres ouvertes</span><span class="sxs-lookup"><span data-stu-id="bf5da-202">open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="bf5da-203">ouvrir et focaliser une nouvelle fenêtre pour afficher une page client de Project Web App</span><span class="sxs-lookup"><span data-stu-id="bf5da-203">open and focus a new window to display a PWA client page</span></span>  

<span data-ttu-id="bf5da-204">Dans votre `pwabuilder-sw.js` fichier, ajoutez les gestionnaires suivants.</span><span class="sxs-lookup"><span data-stu-id="bf5da-204">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

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
    
    // This looks to see if the current notification is already open and focuses it.
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

### <span data-ttu-id="bf5da-205">Étape 4: testez-le</span><span class="sxs-lookup"><span data-stu-id="bf5da-205">Step 4 - Try it out</span></span>  

<span data-ttu-id="bf5da-206">Suivez les étapes ci-dessous pour tester les notifications de transmission dans votre PWA.</span><span class="sxs-lookup"><span data-stu-id="bf5da-206">Perform the following steps to test push notifications in your PWA.</span></span>  

1.  <span data-ttu-id="bf5da-207">Accédez à votre PWA à l’adresse `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="bf5da-207">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="bf5da-208">Lorsque le travailleur de votre service active et tente d’abonner votre PWA aux notifications de transmission, Microsoft Edge vous invite à autoriser votre PWA à afficher les notifications.</span><span class="sxs-lookup"><span data-stu-id="bf5da-208">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="bf5da-209">Sélectionnez **autoriser**.</span><span class="sxs-lookup"><span data-stu-id="bf5da-209">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Boîte de dialogue autorisation permettant d’activer les notifications":::
       <span data-ttu-id="bf5da-211">Boîte de dialogue autorisation permettant d’activer les notifications</span><span class="sxs-lookup"><span data-stu-id="bf5da-211">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
    
1.  <span data-ttu-id="bf5da-212">Simuler une notification de transmission côté serveur.</span><span class="sxs-lookup"><span data-stu-id="bf5da-212">Simulate a server-side push notification.</span></span>  <span data-ttu-id="bf5da-213">Avec votre PWA ouvert `http://localhost:3000` dans votre navigateur, sélectionnez `F12` pour ouvrir le devtools.</span><span class="sxs-lookup"><span data-stu-id="bf5da-213">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="bf5da-214">Sélectionnez **Application**  >  **Worker Worker Worker Worker**  >  **Push** pour envoyer une notification d’émission de test à votre application Project Web App.</span><span class="sxs-lookup"><span data-stu-id="bf5da-214">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  <span data-ttu-id="bf5da-215">Une notification de transmission doit s’afficher à proximité de la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="bf5da-215">You should see a push notification appear near the taskbar.</span></span>  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Pousser une notification de DevTools":::
       <span data-ttu-id="bf5da-217">Pousser une notification de DevTools</span><span class="sxs-lookup"><span data-stu-id="bf5da-217">Push a notification from DevTools</span></span>
    :::image-end:::
     
    <span data-ttu-id="bf5da-218">Si vous ne sélectionnez pas \ (ou activer) une notification Toast, elle est ignorée après quelques secondes et est mise en file d’attente dans le centre de notifications Windows.</span><span class="sxs-lookup"><span data-stu-id="bf5da-218">If you do not select \(or activate\) a toast notification, it is dismissed after several seconds and queues up in your Windows Action Center.</span></span>  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Notifications dans le centre de notifications Windows":::
       <span data-ttu-id="bf5da-220">Notifications dans le centre de notifications Windows</span><span class="sxs-lookup"><span data-stu-id="bf5da-220">Notifications in Windows Action Center</span></span>
    :::image-end:::
    
    
## <span data-ttu-id="bf5da-221">Étapes suivantes</span><span class="sxs-lookup"><span data-stu-id="bf5da-221">Next steps</span></span>  

<span data-ttu-id="bf5da-222">Vous trouverez ci-dessous une liste de tâches supplémentaires à découvrir lors de la création de PWAss réalistes:</span><span class="sxs-lookup"><span data-stu-id="bf5da-222">The following is a list of additional tasks to learn when building real-world PWAs:</span></span>  

*  <span data-ttu-id="bf5da-223">Gérer et stocker des abonnements envoyés</span><span class="sxs-lookup"><span data-stu-id="bf5da-223">Manage and store push subscriptions</span></span>  
*  <span data-ttu-id="bf5da-224">[Chiffrer][NPMWebPushEncrypt] les données de charge utile</span><span class="sxs-lookup"><span data-stu-id="bf5da-224">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*  <span data-ttu-id="bf5da-225">Conception réactive</span><span class="sxs-lookup"><span data-stu-id="bf5da-225">Responsive design</span></span>  
*  <span data-ttu-id="bf5da-226">Liaison Poussée</span><span class="sxs-lookup"><span data-stu-id="bf5da-226">Deep-linking</span></span>  
*  [<span data-ttu-id="bf5da-227">Tests entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="bf5da-227">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*  <span data-ttu-id="bf5da-228">Mettre en œuvre des pratiques recommandées telles que [webhint][Webhint]</span><span class="sxs-lookup"><span data-stu-id="bf5da-228">Implement best practices such as [Webhint][Webhint]</span></span>  

## <span data-ttu-id="bf5da-229">Voir également</span><span class="sxs-lookup"><span data-stu-id="bf5da-229">See also</span></span>  

*   <span data-ttu-id="bf5da-230">[Applications Web progressives sur MDN Web docs][MDNProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="bf5da-230">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps].</span></span>  
*   <span data-ttu-id="bf5da-231">[Applications Web progressives sur le Web. dev][WebDevProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="bf5da-231">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps].</span></span>  
*   <span data-ttu-id="bf5da-232">[Lecteurs de News malveillants: applications Web progressives][HackerNewsProgressiveWebApps] -compare les différents types d’infrastructure et de performance permettant d’implémenter un exemple de version de Project</span><span class="sxs-lookup"><span data-stu-id="bf5da-232">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Publier sur le service d’application Azure-créez un nœud. js et une application rapide dans Visual Studio | Documents Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Créer un compte gratuit Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Applications Web | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Notifications Web dans Microsoft Edge | Blogs Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Code Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Tests gratuits du navigateur Microsoft Edge sur Windows 10 | BrowserStack"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Générateur d’application rapide | Explorer" 

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Lecteurs de nouvelles pirates en application Web progressive"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Applications Web progressives (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Utiliser des travailleurs de service | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Envoyer des notifications webtransmission identifiées par VAPID via le service pousser de Mozilla Services Mozilla"  

[NodejsMain]: https://nodejs.org "Node. js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "Web-Poussée | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, Payload, contentEncoding)-Web-Poussée | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Utilisation-Web-Poussée | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Applications Web progressives"  

[PwaBuilder]: https://www.pwabuilder.com "Générateur PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Travailleur de service | Générateur PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Démonstration complète | Livre de ServiceWorker"  

[VapidkeysMain]: https://vapidkeys.com "Générateur de clés sécurisées VAPID | VapidKeys" 

[Webhint]: https://sonarwhal.com "webhint, le moteur d’indicateurs pour les meilleures pratiques sur le Web"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Applications Web progressives | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Amélioration progressive | Wikipédia"  
