---
description: Les applications web progressives (Chromium) s’exécutent en natif sur Windows 10.  Voici tout ce que vous devez savoir en tant que développeur web.
title: Applications web progressives sur Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/06/2021
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f1f5370af0710927f66c8231274fe307cb3ee2a4
ms.sourcegitcommit: 7f7922dbb6af87ecac1378d18359125770c5b8e5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2021
ms.locfileid: "11536808"
---
# <a name="progressive-web-apps-on-windows-overview"></a><span data-ttu-id="d7681-105">Vue d’ensemble des applications web progressives Windows web</span><span class="sxs-lookup"><span data-stu-id="d7681-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="d7681-106">[Les][MDNApps] applications web progressives \(PWAs\) permettent d’accéder aux technologies web ouvertes pour l’interopérabilité entre plateformes et offrent à vos utilisateurs une expérience native, de l’application, personnalisée pour leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="d7681-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="d7681-107">Les P PWA sont des sites web [qui][AListApartUnderstandingProgressiveEnhancement] sont progressivement améliorés pour fonctionner comme des applications natives sur les plateformes de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="d7681-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="d7681-108">Les qualités d’une PWA combinent le meilleur des applications web et natives.</span><span class="sxs-lookup"><span data-stu-id="d7681-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a><span data-ttu-id="d7681-109">[Découvrable][MDNPwaAdvantagesDiscoverable]</span><span class="sxs-lookup"><span data-stu-id="d7681-109">[Discoverable][MDNPwaAdvantagesDiscoverable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="installablemdnpwaadvantagesinstallable"></a><span data-ttu-id="d7681-110">[Installable][MDNPwaAdvantagesInstallable]</span><span class="sxs-lookup"><span data-stu-id="d7681-110">[Installable][MDNPwaAdvantagesInstallable]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a><span data-ttu-id="d7681-111">[Réentrable][MDNPwaAdvantagesReEngageable]</span><span class="sxs-lookup"><span data-stu-id="d7681-111">[Re-engageable][MDNPwaAdvantagesReEngageable]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="d7681-112">À partir des résultats de recherche web et des magasins d’applications de prise en charge</span><span class="sxs-lookup"><span data-stu-id="d7681-112">From web search results and supporting app stores</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="d7681-113">Épingler et lancer à partir de l’écran d’accueil, du menu Démarrer, de la barre des tâches, et ainsi de suite</span><span class="sxs-lookup"><span data-stu-id="d7681-113">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="d7681-114">Envoyer des notifications Push, même lorsque l’application n’est pas active</span><span class="sxs-lookup"><span data-stu-id="d7681-114">Send push notifications, even when the app is not active</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security-small.png":::  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a><span data-ttu-id="d7681-115">[Indépendant du réseau][MDNPwaAdvantagesNetworkIndependent]</span><span class="sxs-lookup"><span data-stu-id="d7681-115">[Network Independent][MDNPwaAdvantagesNetworkIndependent]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a><span data-ttu-id="d7681-116">[Progressive][MDNPwaAdvantagesProgressive]</span><span class="sxs-lookup"><span data-stu-id="d7681-116">[Progressive][MDNPwaAdvantagesProgressive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="safemdnpwaadvantagessafe"></a><span data-ttu-id="d7681-117">[Safe][MDNPwaAdvantagesSafe]</span><span class="sxs-lookup"><span data-stu-id="d7681-117">[Safe][MDNPwaAdvantagesSafe]</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="d7681-118">Fonctionne en mode hors connexion et dans des conditions de faible réseau</span><span class="sxs-lookup"><span data-stu-id="d7681-118">Works offline and in low-network conditions</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="d7681-119">L’expérience est étendue (ou réduite) avec les fonctionnalités de l’appareil</span><span class="sxs-lookup"><span data-stu-id="d7681-119">Experience scales up (or down) with device capabilities</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="d7681-120">Fournit un point de terminaison HTTPS sécurisé et d’autres protections utilisateur</span><span class="sxs-lookup"><span data-stu-id="d7681-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive-small.png":::  
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link-small.png":::  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        ### <a name="responsivemdnpwaadvantagesresponsive"></a><span data-ttu-id="d7681-121">[Réactivité][MDNPwaAdvantagesResponsive]</span><span class="sxs-lookup"><span data-stu-id="d7681-121">[Responsive][MDNPwaAdvantagesResponsive]</span></span>  
    :::column-end:::
    :::column:::
        ### <a name="linkablemdnpwaadvantageslinkable"></a><span data-ttu-id="d7681-122">[Linkable][MDNPwaAdvantagesLinkable]</span><span class="sxs-lookup"><span data-stu-id="d7681-122">[Linkable][MDNPwaAdvantagesLinkable]</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        <span data-ttu-id="d7681-123">S’adapte à la taille de l’écran ou à l’orientation et à la méthode d’entrée de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="d7681-123">Adapts to the user's screen size or orientation and input method</span></span>  
    :::column-end:::
    :::column:::
        <span data-ttu-id="d7681-124">Partager et lancer à partir d’un lien hypertexte standard</span><span class="sxs-lookup"><span data-stu-id="d7681-124">Share and launch from a standard hyperlink</span></span>  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  

<span data-ttu-id="d7681-125">Créez \(ou convertissez\) votre site web existant en un PWA pour améliorer votre engagement auprès de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="d7681-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="d7681-126">Les améliorations incluent les notifications Push, l’intégration de l’application et la prise en charge hors connexion.</span><span class="sxs-lookup"><span data-stu-id="d7681-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="d7681-127">Continuez à développer votre audience sur le web ouvert pour que les utilisateurs découvrent vos PWA par le biais de la recherche et du partage de liens.</span><span class="sxs-lookup"><span data-stu-id="d7681-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="d7681-128">Mieux encore, votre application est mise à jour à l’aide du code de votre serveur web.</span><span class="sxs-lookup"><span data-stu-id="d7681-128">Best of all, your app is updated in using your web server code.</span></span>  

## <a name="pwas-on-microsoft-edge-chromium"></a><span data-ttu-id="d7681-129">P PWAs sur Microsoft Edge (Chromium)</span><span class="sxs-lookup"><span data-stu-id="d7681-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="d7681-130">Lorsque vous créez une application web progressive ciblant des API web standard, votre application peut être déployée sur des plateformes et des appareils et tirer parti des fonctionnalités spécifiques de l’appareil, selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="d7681-130">When you build a Progressive Web App targeting web standard APIs, your app may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="d7681-131">Les P PWA dans Microsoft Edge \(Chromium\) ajoutent les avantages suivants à votre site web.</span><span class="sxs-lookup"><span data-stu-id="d7681-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="d7681-132">Votre application repose sur une plateforme web basée sur des normes.</span><span class="sxs-lookup"><span data-stu-id="d7681-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="d7681-133">Permet à vos utilisateurs d’installer votre application directement à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="d7681-133">Allows your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="d7681-134">Permet à vos utilisateurs d’installer votre application sans inscription ou déploiement basé sur le Store.</span><span class="sxs-lookup"><span data-stu-id="d7681-134">Allows your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="d7681-135">Les applications de bureau sont pris en charge sur l’une des plateformes Microsoft Edge \(Chromium\) est disponible.</span><span class="sxs-lookup"><span data-stu-id="d7681-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="d7681-136">Microsoft Edge \(Chromium\) est disponible sur Windows 7, Windows 10 et macOS.</span><span class="sxs-lookup"><span data-stu-id="d7681-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="d7681-137">Les avantages suivants sont inclus.</span><span class="sxs-lookup"><span data-stu-id="d7681-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="d7681-138">Les applications peuvent être installées directement à partir du navigateur à l’aide de l’icône **Installer** dans la barre de navigation.</span><span class="sxs-lookup"><span data-stu-id="d7681-138">Apps may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Installer le volant et l’icône de l’application" lightbox="./media/install-progressive-web-app-icon.png":::
       <span data-ttu-id="d7681-140">Installer le volant et l’icône de l’application</span><span class="sxs-lookup"><span data-stu-id="d7681-140">Install app flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="d7681-141">Les applications peuvent également être installées, exécutés et gérées à partir du menu **Paramètres**  >  **Applications**</span><span class="sxs-lookup"><span data-stu-id="d7681-141">Apps may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="Éléments de menu de l’application sous paramètres" lightbox="./media/app-menus.png":::
       <span data-ttu-id="d7681-143">Éléments de menu de l’application sous paramètres</span><span class="sxs-lookup"><span data-stu-id="d7681-143">App menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="d7681-144">Les notifications web sont intégrées dans le système de notification Windows’application</span><span class="sxs-lookup"><span data-stu-id="d7681-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="d7681-145">Magasin de cookies partagé avec le profil de navigateur qui a installé l’application</span><span class="sxs-lookup"><span data-stu-id="d7681-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="d7681-146">Accès à d’autres fonctionnalités de navigateur à l’aide du menu Paramètre et plus **\(** \), y compris la validation de certificat, les autorisations de site, la protection de suivi et les `...` extensions de navigateur</span><span class="sxs-lookup"><span data-stu-id="d7681-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="d7681-147">Accès total à [Microsoft Edge DevTools pour][DevtoolsProgressiveWebApps] le débogage de votre application</span><span class="sxs-lookup"><span data-stu-id="d7681-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!NOTE]
> <span data-ttu-id="d7681-148">Pour plus d’informations sur PWA avantages, les fonctionnalités à venir et les démonstrations courtes, accédez à build [2020 PWA session.][BuildVideo]</span><span class="sxs-lookup"><span data-stu-id="d7681-148">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <a name="requirements"></a><span data-ttu-id="d7681-149">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="d7681-149">Requirements</span></span>  

<span data-ttu-id="d7681-150">Pour s’exécuter en tant PWA, votre application web hébergée sur le serveur doit inclure les exigences minimales suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7681-150">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-151">HTTPS</span><span class="sxs-lookup"><span data-stu-id="d7681-151">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-152">Protège vos utilisateurs en fournissant une connexion sécurisée pour la communication entre le serveur ou l’application.</span><span class="sxs-lookup"><span data-stu-id="d7681-152">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="d7681-153">Les travailleurs de service et autres technologies PWA fonctionnent uniquement avec des ressources web servies sur une connexion sécurisée \(ou à partir de là à des fins `localhost` de débogage\).</span><span class="sxs-lookup"><span data-stu-id="d7681-153">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-154">Worker du service</span><span class="sxs-lookup"><span data-stu-id="d7681-154">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-155">Utilise les threads de travail de service pour agir en tant que proxys réseau entre votre serveur et votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="d7681-155">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="d7681-156">Les threads de travail de service assurent la prise en charge hors connexion, la mise en cache des ressources, les notifications Push, la synchronisation des données en arrière-plan et les optimisations des performances de chargement des pages.</span><span class="sxs-lookup"><span data-stu-id="d7681-156">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-157">Manifeste de l’application web</span><span class="sxs-lookup"><span data-stu-id="d7681-157">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-158">Fournit un fichier de métadonnées basé sur JSON qui décrit les informations clés sur votre application web, afin que Windows 10 et d’autres plateformes hôtes fournissent à vos utilisateurs PWA une expérience installable et native de l’application.</span><span class="sxs-lookup"><span data-stu-id="d7681-158">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="d7681-159">Les informations clés incluent les icônes, la langue et le point d’entrée d’URL.</span><span class="sxs-lookup"><span data-stu-id="d7681-159">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="d7681-160">Pour être une excellente PWA, votre application doit également répondre aux exigences suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7681-160">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-161">Compatibilité entre navigateurs</span><span class="sxs-lookup"><span data-stu-id="d7681-161">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-162">Assurez-vous que PWA fonctionne [en testant][MicrosoftDeveloperEdgeToolsRemote] dans différents navigateurs et environnements.</span><span class="sxs-lookup"><span data-stu-id="d7681-162">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-163">Conception réactive</span><span class="sxs-lookup"><span data-stu-id="d7681-163">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-164">Utilise des dispositions fluides et des images flexibles.</span><span class="sxs-lookup"><span data-stu-id="d7681-164">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="d7681-165">La conception réactive inclut les éléments suivants qui adaptent votre expérience utilisateur à l’appareil de votre utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d7681-165">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="d7681-166">Grille [CSS][MDNCssGridLayout]</span><span class="sxs-lookup"><span data-stu-id="d7681-166">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="d7681-167">flexbox</span><span class="sxs-lookup"><span data-stu-id="d7681-167">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="d7681-168">Grille CSS [et][MDNCssGridLayout] [flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="d7681-168">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="d7681-169">requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="d7681-169">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="d7681-170">images réactives</span><span class="sxs-lookup"><span data-stu-id="d7681-170">responsive images</span></span>][MDNResponsiveImages]  
          
      <span data-ttu-id="d7681-171">Utilise les outils d’émulation d’appareil de votre navigateur pour tester localement ou créer une session de débogage à distance sur [Windows][DevtoolsRemoteDebuggingWindows] ou [Android][DevtoolsRemoteDebuggingIndex] pour tester directement sur un appareil cible. [][DevToolsGuideDeviceModeTestingOtherBrowsers]</span><span class="sxs-lookup"><span data-stu-id="d7681-171">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-172">Liaisons profondes</span><span class="sxs-lookup"><span data-stu-id="d7681-172">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-173">Approvisionnement de chaque page de votre site vers une URL unique afin que les utilisateurs existants vous aident à impliquer un public encore plus large via le partage de réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="d7681-173">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-174">Pratiques de validation et de test</span><span class="sxs-lookup"><span data-stu-id="d7681-174">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-175">Utilise des outils de qualité du code tels que [le linter Webhint][Webhint] pour optimiser l’efficacité, la robustesse, la sécurité et l’accessibilité de votre application.</span><span class="sxs-lookup"><span data-stu-id="d7681-175">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="d7681-176">Chromium PWA liste de contrôle</span><span class="sxs-lookup"><span data-stu-id="d7681-176">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="d7681-177">Vérifie votre PWA par rapport à la liste de PWA de référence Google.</span><span class="sxs-lookup"><span data-stu-id="d7681-177">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="d7681-178">Pour transformer votre PWA en une application [Microsoft Store,][MicrosoftDeveloperStore] accédez à Applications web progressives [dans la Microsoft Store][PwaChromiumMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="d7681-178">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] app, navigate to [Progressive Web Apps in the Microsoft Store][PwaChromiumMicrosoftStore].</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d7681-179">Voir également</span><span class="sxs-lookup"><span data-stu-id="d7681-179">See also</span></span>  

*   [<span data-ttu-id="d7681-180">#A0</span><span class="sxs-lookup"><span data-stu-id="d7681-180">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="d7681-181">Une feuille de route progressive pour votre application web progressive</span><span class="sxs-lookup"><span data-stu-id="d7681-181">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="d7681-182">Posts hors connexion avec applications web progressives</span><span class="sxs-lookup"><span data-stu-id="d7681-182">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="d7681-183">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="d7681-183">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="d7681-184">Se menter sur le Web</span><span class="sxs-lookup"><span data-stu-id="d7681-184">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="d7681-185">Attribution de noms aux applications web progressives</span><span class="sxs-lookup"><span data-stu-id="d7681-185">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="d7681-186">Conception et création d’une application web progressive sans infrastructure (partie 1)</span><span class="sxs-lookup"><span data-stu-id="d7681-186">Designing And Building A Progressive Web App Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [<span data-ttu-id="d7681-187">Conception et création d’une application web progressive sans infrastructure (partie 2)</span><span class="sxs-lookup"><span data-stu-id="d7681-187">Designing And Building A Progressive Web App Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [<span data-ttu-id="d7681-188">Conception et création d’une application web progressive sans infrastructure (partie 3)</span><span class="sxs-lookup"><span data-stu-id="d7681-188">Designing And Building A Progressive Web App Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Prise en main le débogage à distance Windows 10 appareils | Documents Microsoft"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Émuler et tester d’autres navigateurs | Documents Microsoft"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Déboguer les applications web progressives | Documents Microsoft"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Publier votre application web progressive sur le Microsoft Store | Documents Microsoft"

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Windows Vue d’Notification Services (WNS) push | Documents Microsoft"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Conception pour xbox et télévision | Documents Microsoft"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Considérations sur l’interface utilisateur pour les appareils UWP | Documents Microsoft"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Qu’est-ce qu’une application de plateforme Windows universelle (UWP) ? | Documents Microsoft"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Prise en charge de votre application avec des tâches en arrière-plan | Documents Microsoft"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publier Windows applications et jeux | Documents Microsoft"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Ouverture d’un compte de développeur | Documents Microsoft"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Mise en place d’applications web progressives Microsoft Edge et Windows 10 - Windows blogs"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de synchronisation en arrière-plan - État Microsoft Edge plateforme"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifeste de l’application web : Microsoft Edge plateforme"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Test instantané"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Réalité mixte pour les développeurs"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau Microsoft Edge navigateur"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Activer ou désactiver l’assistance focus dans Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Modifier les paramètres de notification dans Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Understanding Progressive Enhancement - A List Apart"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "applications | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Test entre navigateurs | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Modèle de disposition de zone flexible CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Modèle de disposition de grille CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Récupérer les | API MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Requêtes multimédias | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notifications API | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "Api Push | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Découvrable : avantages de l’application web progressive"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Installable : avantages de l’application web progressive"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Linkable : avantages de l’application web progressive"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Indépendant du réseau : avantages de l’application web progressive"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Progressive : avantages de l’application web progressive"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Ré-engageable - Avantages progressifs de l’application web"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Réactive : avantages de l’application web progressive"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Sécurisé : avantages de l’application web progressive"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Images réactives | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "Service Worker API | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Contenu du manifeste d’application | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "PWA vidéo"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Une feuille de route progressive pour votre application web progressive"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "#A0 – Nouvelle édition Edge"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Attribution de noms aux applications web progressives"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Se menter sur le Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Posts hors connexion avec applications web progressives"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Conception et création d’une application Web progressive sans infrastructure (partie 1)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Conception et création d’une application Web progressive sans infrastructure (partie 2)"  

[Smashingmagazine201907ProgressiveWebAppFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Conception et création d’une application Web progressive sans infrastructure (partie 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Qu’est-ce qui rend une application web progressive | web.dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Liaison approfondie - Wikipedia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS - Wikipedia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Conception web réactive - Wikipedia"  
