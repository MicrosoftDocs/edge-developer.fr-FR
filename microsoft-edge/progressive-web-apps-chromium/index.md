---
description: Les applications Web progressives (chrome) s’exécutent en mode natif sur Windows 10.  Voici ce que vous devez savoir en tant que développeur Web.
title: Applications Web progressives sur Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications Web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: a13f39dc3b3e0d47ad07b0e447556dc14093e71b
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231215"
---
# <span data-ttu-id="5efe8-105">Vue d’ensemble des applications Web progressivement sur Windows</span><span class="sxs-lookup"><span data-stu-id="5efe8-105">Progressive Web Apps on Windows overview</span></span>  

<span data-ttu-id="5efe8-106">Les [applications Web progressives][MDNApps] \(PWAS \) offrent un accès aux technologies Web ouvertes pour une interopérabilité multiplateforme et fournissent aux utilisateurs une interface native et de type application adaptée à leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="5efe8-106">[Progressive Web Apps][MDNApps] \(PWAs\) provide access to open web technologies for cross-platform interoperability and provide your users with a native, app-like experience customized for their devices.</span></span>  <span data-ttu-id="5efe8-107">Les PWAs sont des sites Web qui sont [progressivement améliorés][AListApartUnderstandingProgressiveEnhancement] pour fonctionner comme des applications natives sur les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="5efe8-107">PWAs are websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="5efe8-108">Les qualités d’une PWA combinent le meilleur des applications web et natives.</span><span class="sxs-lookup"><span data-stu-id="5efe8-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [<span data-ttu-id="5efe8-109">Détectable</span><span class="sxs-lookup"><span data-stu-id="5efe8-109">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="5efe8-110">Dans les résultats de recherche Web et les magasins d’applications de support</span><span class="sxs-lookup"><span data-stu-id="5efe8-110">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [<span data-ttu-id="5efe8-111">Installation correcte</span><span class="sxs-lookup"><span data-stu-id="5efe8-111">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="5efe8-112">Épingler et lancer à partir de l’écran d’accueil, du menu Démarrer, de la barre des tâches, etc.</span><span class="sxs-lookup"><span data-stu-id="5efe8-112">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [<span data-ttu-id="5efe8-113">Nouvelle installation</span><span class="sxs-lookup"><span data-stu-id="5efe8-113">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="5efe8-114">Envoyer des notifications de transmission, même lorsque l’application n’est pas active</span><span class="sxs-lookup"><span data-stu-id="5efe8-114">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [<span data-ttu-id="5efe8-115">Indépendant du réseau</span><span class="sxs-lookup"><span data-stu-id="5efe8-115">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="5efe8-116">Fonctionne hors ligne et dans des conditions de faible réseau</span><span class="sxs-lookup"><span data-stu-id="5efe8-116">Works offline and in low-network conditions</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [<span data-ttu-id="5efe8-117">Avantage</span><span class="sxs-lookup"><span data-stu-id="5efe8-117">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="5efe8-118">L’accès évolue vers le haut (ou vers le bas) avec les fonctionnalités de l’appareil</span><span class="sxs-lookup"><span data-stu-id="5efe8-118">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [<span data-ttu-id="5efe8-119">Approuvés</span><span class="sxs-lookup"><span data-stu-id="5efe8-119">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="5efe8-120">Fournit un point de terminaison sécurisé HTTPs et d’autres protections de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="5efe8-120">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [<span data-ttu-id="5efe8-121">Réactivité</span><span class="sxs-lookup"><span data-stu-id="5efe8-121">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="5efe8-122">S’adapte à la taille de l’écran ou à l’orientation de l’utilisateur et à la méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="5efe8-122">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [<span data-ttu-id="5efe8-123">Liens hypertexte</span><span class="sxs-lookup"><span data-stu-id="5efe8-123">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="5efe8-124">Partager et lancer à partir d’un lien hypertexte standard</span><span class="sxs-lookup"><span data-stu-id="5efe8-124">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


<span data-ttu-id="5efe8-125">Créez \(ou convertissez) votre site Web existant vers un site PWA pour améliorer vos engagements.</span><span class="sxs-lookup"><span data-stu-id="5efe8-125">Build \(or convert\) your existing website to a PWA to enhance your engagement with your users.</span></span>  <span data-ttu-id="5efe8-126">Les améliorations incluent les notifications de transmission, l’intégration de type application et la prise en charge hors connexion.</span><span class="sxs-lookup"><span data-stu-id="5efe8-126">Enhancements include push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="5efe8-127">Continuez à développer votre public sur le Web ouvert pour que les utilisateurs puissent découvrir votre PWA par le biais de la recherche et du partage de liens.</span><span class="sxs-lookup"><span data-stu-id="5efe8-127">Continue to build your audience on the open web for users to discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="5efe8-128">Mieux, votre application est mise à jour à l’aide de votre code serveur Web.</span><span class="sxs-lookup"><span data-stu-id="5efe8-128">Best of all, your app is updated in using your web server code.</span></span>  

## <span data-ttu-id="5efe8-129">PWAs sur Microsoft Edge (chrome)</span><span class="sxs-lookup"><span data-stu-id="5efe8-129">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="5efe8-130">Lorsque vous générez une API standard Web pour cibler une application Web, votre application peut être déployée sur différentes plateformes et appareils et tirer parti des fonctionnalités spécifiques à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="5efe8-130">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device-specific capabilities as available.</span></span>  <span data-ttu-id="5efe8-131">PWAs dans Microsoft Edge \(chrome \) ajoutez les avantages suivants à votre site Web.</span><span class="sxs-lookup"><span data-stu-id="5efe8-131">PWAs in Microsoft Edge \(Chromium\) add the following advantages to your website.</span></span>  

*   <span data-ttu-id="5efe8-132">Votre application est basée sur une plateforme Web standard.</span><span class="sxs-lookup"><span data-stu-id="5efe8-132">Your app is built on a standards-based web platform.</span></span>  
*   <span data-ttu-id="5efe8-133">Permet aux utilisateurs d’installer votre application directement à partir du navigateur.</span><span class="sxs-lookup"><span data-stu-id="5efe8-133">Enables your users to install your app directly from the browser.</span></span>  
*   <span data-ttu-id="5efe8-134">Permet à vos utilisateurs d’installer votre application sans déploiement ou inscription sur le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="5efe8-134">Enables your users to install your app without a Store-based deployment or registration.</span></span>  
    
<span data-ttu-id="5efe8-135">Les PWAs de bureau sont prises en charge sur n’importe quelle plateforme Microsoft Edge \(chrome \) est disponible.</span><span class="sxs-lookup"><span data-stu-id="5efe8-135">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available.</span></span> <span data-ttu-id="5efe8-136">Microsoft Edge \(chrome \) est disponible sur Windows 7, Windows 10 et macOS.</span><span class="sxs-lookup"><span data-stu-id="5efe8-136">Microsoft Edge \(Chromium\) is available on Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="5efe8-137">Les avantages suivants sont inclus.</span><span class="sxs-lookup"><span data-stu-id="5efe8-137">The following benefits are included.</span></span>  

*   <span data-ttu-id="5efe8-138">Les applications sont installées directement à partir du navigateur à l’aide de l’icône d' **installation** dans la barre de navigation.</span><span class="sxs-lookup"><span data-stu-id="5efe8-138">Applications may be installed directly from within the browser using the **Install** icon in the navigation bar.</span></span>  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Installer le menu volant et l’icône d’application" lightbox="./media/install_pwa_icon.png":::
       <span data-ttu-id="5efe8-140">Installer le menu volant et l’icône d’application</span><span class="sxs-lookup"><span data-stu-id="5efe8-140">Install application flyout and icon</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="5efe8-141">Les applications risquent également d’être installées, exécutées et  gérées dans le menu des  >  **applications** paramètres</span><span class="sxs-lookup"><span data-stu-id="5efe8-141">Applications may also be installed, run, and managed from the **Settings** > **Apps** menu</span></span>  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Éléments de menu de l’application sous paramètres" lightbox="./media/app_menus.png":::
       <span data-ttu-id="5efe8-143">Éléments de menu de l’application sous paramètres</span><span class="sxs-lookup"><span data-stu-id="5efe8-143">Application menu items under settings</span></span>  
    :::image-end:::  
    
*   <span data-ttu-id="5efe8-144">Les notifications Web sont intégrées dans le système de notification Windows</span><span class="sxs-lookup"><span data-stu-id="5efe8-144">Web Notifications are integrated into the Windows notification system</span></span>  
*   <span data-ttu-id="5efe8-145">Magasin de cookies partagés avec le profil de navigateur qui a installé l’application</span><span class="sxs-lookup"><span data-stu-id="5efe8-145">Shared cookie store with the browser profile that installed the app</span></span>  
*   <span data-ttu-id="5efe8-146">Accès à d’autres fonctionnalités de navigateur à l’aide du menu **paramètre et plus** \( `...` \), avec la validation de certificats, les autorisations de site, la protection contre le suivi et les extensions de navigateur</span><span class="sxs-lookup"><span data-stu-id="5efe8-146">Access to other browser features using the **Setting and more** \(`...`\) menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>  
*   <span data-ttu-id="5efe8-147">Un accès complet à [Microsoft Edge devtools][DevtoolsProgressiveWebApps] pour le débogage de votre application</span><span class="sxs-lookup"><span data-stu-id="5efe8-147">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  
    
> [!IMPORTANT]
> <span data-ttu-id="5efe8-148">Pour personnaliser PWAs en particulier pour les Windows 10 qui effectuent des demandes d’API WinRT en utilisant JavaScript, accédez à [documentation spécifique aux fonctionnalités de EdgeHTML PWA] [PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="5efe8-148">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, navigate to [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="5efe8-149">En savoir plus sur le test de votre PWA sur Windows 10 et son distribution dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="5efe8-149">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="5efe8-150">Pour plus d’informations sur les avantages, les fonctionnalités à venir et les courtes démonstrations de Project Web App, accédez à la [version 2020 de la session PWA][BuildVideo].</span><span class="sxs-lookup"><span data-stu-id="5efe8-150">For more information about PWA benefits, upcoming features, and short demos, navigate to [Build 2020 PWA session][BuildVideo].</span></span> 

## <span data-ttu-id="5efe8-151">Conditions requises</span><span class="sxs-lookup"><span data-stu-id="5efe8-151">Requirements</span></span>  

<span data-ttu-id="5efe8-152">Pour être exécuté en tant que PWA, votre application Web hébergée sur un serveur doit inclure la configuration minimale requise.</span><span class="sxs-lookup"><span data-stu-id="5efe8-152">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-153">HTTPS</span><span class="sxs-lookup"><span data-stu-id="5efe8-153">HTTPS</span></span>][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-154">Protège vos utilisateurs en fournissant une connexion sécurisée pour la communication avec le serveur ou l’application.</span><span class="sxs-lookup"><span data-stu-id="5efe8-154">Protects your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="5efe8-155">Les travailleurs de service et autres technologies PWA fonctionnent uniquement avec les ressources Web fournies par le biais d’une connexion sécurisée (ou à partir `localhost` de à des fins de débogage \).</span><span class="sxs-lookup"><span data-stu-id="5efe8-155">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-156">Worker du service</span><span class="sxs-lookup"><span data-stu-id="5efe8-156">Service Workers</span></span>][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-157">Utilise des threads de travail de service pour agir en tant que proxy réseau entre votre serveur et votre application cliente.</span><span class="sxs-lookup"><span data-stu-id="5efe8-157">Uses Service Worker threads to act as network proxies between your server and client app.</span></span>  <span data-ttu-id="5efe8-158">Les threads de travail en mode hors connexion, de mise en cache des ressources, de notifications de transmission, de synchronisation des données en arrière-plan et d’optimisation des performances de la page.</span><span class="sxs-lookup"><span data-stu-id="5efe8-158">Service Worker threads provide offline support, resource caching, push notifications, background data sync, and  page-load performance optimizations.</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-159">Manifeste de l’application Web</span><span class="sxs-lookup"><span data-stu-id="5efe8-159">Web App Manifest</span></span>][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-160">Fournit un fichier de métadonnées JSON qui décrit les informations clés relatives à votre application Web, de sorte que les plateformes Windows 10 et d’autres plateformes puissent offrir aux utilisateurs de Project Web App une environnement d’exécution de l’application, qui permet d’installer une application native.</span><span class="sxs-lookup"><span data-stu-id="5efe8-160">Provides a JSON-based metadata file that describes key information about your web app, so that Windows 10 and other host platforms provide your PWA users with an installable, native app-like experience.</span></span>  <span data-ttu-id="5efe8-161">Les informations clés incluent les icônes, la langue et le point d’entrée d’URL.</span><span class="sxs-lookup"><span data-stu-id="5efe8-161">Key information includes icons, language, and URL entry point.</span></span> 
   :::column-end:::
:::row-end:::  

<span data-ttu-id="5efe8-162">Pour être une bonne solution de Project Web App, votre application doit également présenter la configuration requise suivante.</span><span class="sxs-lookup"><span data-stu-id="5efe8-162">To be a great PWA, your app must also meet the following requirements.</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-163">Compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="5efe8-163">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-164">Assurez-vous que le contrôle PWA fonctionne en effectuant des [tests][MicrosoftDeveloperEdgeToolsRemote] dans différents navigateurs et environnements.</span><span class="sxs-lookup"><span data-stu-id="5efe8-164">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-165">Conception réactive</span><span class="sxs-lookup"><span data-stu-id="5efe8-165">Responsive design</span></span>][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-166">Utilise des dispositions fluides et des images flexibles.</span><span class="sxs-lookup"><span data-stu-id="5efe8-166">Employs fluid layouts and flexible images.</span></span>  <span data-ttu-id="5efe8-167">La conception réactive inclut les éléments suivants qui adaptent votre expérience utilisateur à l’appareil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5efe8-167">Responsive design includes the following elements that adapt your UX to your user's device.</span></span>  
      
      *   <span data-ttu-id="5efe8-168">[Grille][MDNCssGridLayout] CSS</span><span class="sxs-lookup"><span data-stu-id="5efe8-168">CSS [grid][MDNCssGridLayout]</span></span>  
      *   [<span data-ttu-id="5efe8-169">flexbox</span><span class="sxs-lookup"><span data-stu-id="5efe8-169">flexbox</span></span>][MDNCssFlexibleBoxLayout]  
      *   <span data-ttu-id="5efe8-170">[Grille][MDNCssGridLayout] CSS et [Flexbox][MDNCssFlexibleBoxLayout]</span><span class="sxs-lookup"><span data-stu-id="5efe8-170">CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout]</span></span>  
      *   [<span data-ttu-id="5efe8-171">requêtes multimédias</span><span class="sxs-lookup"><span data-stu-id="5efe8-171">media queries</span></span>][MDNMediaQueries]  
      *   [<span data-ttu-id="5efe8-172">images réactives</span><span class="sxs-lookup"><span data-stu-id="5efe8-172">responsive images</span></span>][MDNResponsiveImages]  
      
      <span data-ttu-id="5efe8-173">Utilise des [Outils d’émulation d’appareil][DevToolsGuideDeviceModeTestingOtherBrowsers] de votre navigateur pour le test en local, ou créez une session de débogage à distance sur [Windows][DevtoolsRemoteDebuggingWindows] ou [Android][DevtoolsRemoteDebuggingIndex] pour tester directement sur un appareil cible.</span><span class="sxs-lookup"><span data-stu-id="5efe8-173">Uses [device emulation tools][DevToolsGuideDeviceModeTestingOtherBrowsers] from your browser to locally test, or create a remote debugging session on [Windows][DevtoolsRemoteDebuggingWindows] or [Android][DevtoolsRemoteDebuggingIndex] to test directly on a target device.</span></span>
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-174">Liaison Poussée</span><span class="sxs-lookup"><span data-stu-id="5efe8-174">Deep linking</span></span>][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-175">Route chaque page de votre site vers une URL unique de sorte que les utilisateurs existants puissent vous aider à impliquer un public encore plus large via le partage de réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="5efe8-175">Routes each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-176">Pratiques en matière de validation et de test</span><span class="sxs-lookup"><span data-stu-id="5efe8-176">Validation and testing practices</span></span>][Webhint]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-177">Utilise des outils de qualité de code comme l’élément [webhint][Webhint] de type Lint pour optimiser l’efficacité, la robustesse, la sécurité et l’accessibilité de votre application.</span><span class="sxs-lookup"><span data-stu-id="5efe8-177">Uses code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="5efe8-178">Liste de vérification de Project Web App</span><span class="sxs-lookup"><span data-stu-id="5efe8-178">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="5efe8-179">Vérifie votre PWA par rapport à la liste de vérification de base sur Google Baseline.</span><span class="sxs-lookup"><span data-stu-id="5efe8-179">Verifies your PWA against the Google baseline PWA checklist.</span></span>  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> <span data-ttu-id="5efe8-180">Pour transformer votre emplacement PWA en application du [Microsoft Store][MicrosoftDeveloperStore] , accédez à [application Web applications (EdgeHTML) sur le Microsoft Store] [PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="5efe8-180">To turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, navigate to [Progressive Web Apps (EdgeHTML) in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  
  
## <span data-ttu-id="5efe8-181">Voir également</span><span class="sxs-lookup"><span data-stu-id="5efe8-181">See also</span></span>  

*   [<span data-ttu-id="5efe8-182">PWAs de combustion de mythe</span><span class="sxs-lookup"><span data-stu-id="5efe8-182">Myth Busting PWAs</span></span>][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [<span data-ttu-id="5efe8-183">Plan progressif de votre application Web progressive</span><span class="sxs-lookup"><span data-stu-id="5efe8-183">A Progressive Roadmap for your Progressive Web App</span></span>][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [<span data-ttu-id="5efe8-184">Billets hors ligne avec des applications Web progressives</span><span class="sxs-lookup"><span data-stu-id="5efe8-184">Offline POSTs with Progressive Web Apps</span></span>][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [<span data-ttu-id="5efe8-185">PWA Q&A</span><span class="sxs-lookup"><span data-stu-id="5efe8-185">PWA Q&A</span></span>][AaronGustafsonNotebookPwaQa]  
*   [<span data-ttu-id="5efe8-186">Paris sur le Web</span><span class="sxs-lookup"><span data-stu-id="5efe8-186">Betting on the Web</span></span>][JoretegBlogBettingWeb]  
*   [<span data-ttu-id="5efe8-187">Attribution d’un nom aux applications Web progressives</span><span class="sxs-lookup"><span data-stu-id="5efe8-187">Naming Progressive Web Apps</span></span>][Fberriman20170626NamingProgressiveWebApps]  
*   [<span data-ttu-id="5efe8-188">Conception et création d’une application Web progressive sans infrastructure (partie 1)</span><span class="sxs-lookup"><span data-stu-id="5efe8-188">Designing And Building A Progressive Web Application Without A Framework (Part 1)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [<span data-ttu-id="5efe8-189">Conception et création d’une application Web progressive sans infrastructure (partie 2)</span><span class="sxs-lookup"><span data-stu-id="5efe8-189">Designing And Building A Progressive Web Application Without A Framework (Part 2)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [<span data-ttu-id="5efe8-190">Conception et création d’une application Web progressive sans infrastructure (partie 3)</span><span class="sxs-lookup"><span data-stu-id="5efe8-190">Designing And Building A Progressive Web Application Without A Framework (Part 3)</span></span>][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Commencer à utiliser le débogage à distance des appareils Android | Documents Microsoft"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Commencer à utiliser le débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Émuler et tester d’autres navigateurs Documents Microsoft"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Déboguer des applications Web progressives | Documents Microsoft"  
<!--[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "What's new in EdgeHTML 17 | Microsoft Docs"  -->  
<!--[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "What's New in EdgeHTML 14 | Microsoft Docs"  -->  
[PwaEdgehtmlIndex]: .. /edgehtml/progressive-Web-Apps/index.MD "Web Apps (EdgeHTML) sur Windows | Documents Microsoft  
[PwaEdgehtmlMicrosoftStore]: .. /edgehtml/progressive-Web-Apps/Microsoft-Store.MD "application Web progressive dans le Microsoft Store | Documents Microsoft
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Vue d’ensemble des services de notifications de transmission Windows (WNS) Documents Microsoft"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Conception pour Xbox et télévision | Documents Microsoft"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Considérations relatives à l’interface utilisateur pour les appareils UWP | Documents Microsoft"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Qu’est-ce qu’une application de plateforme Windows universelle (UWP)? Documents Microsoft"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Prendre en charge votre application avec des tâches en arrière-plan | Documents Microsoft"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publier des applications et des jeux Windows | Documents Microsoft"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Ouverture d’un compte de développeur | Documents Microsoft"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Accueillir des applications Web progressives sur Microsoft Edge et Windows 10-blogs Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de synchronisation en arrière-plan-état de la plateforme Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifeste de l’application Web-État de la plateforme Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Tests instantanés"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Réalité mixte pour les développeurs"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Activation ou désactivation de l’assistance au focus dans Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Modifier les paramètres de notification dans Windows 10"  

[AaronGustafsonNotebookPwaQa]: https://www.aaron-gustafson.com/notebook/pwa-qa "PWA Q&A"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Présentation de l’amélioration progressive-liste séparée"  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "applications | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Cache | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Test de navigateur croisé | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Disposition de cadre flexible CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Disposition Grille CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "API Fetch | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Requêtes multimédias | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Avantages de la découverte-application Web progressive"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Avantages de l’installation de l’application Web progressive"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Avantages liés aux applications Web multidirectionnelle"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Avantages de l’application Web progressive en réseau"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Avantages de l’application Web progressive progressive"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Avantages de l’utilisation de l’application Web progressive"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Avantages de l’application Web progressivement réactif"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Avantages de l’application Web progressive en sécurité"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Images réactives | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Vidéo sur Project Web App"  

[CloudfourThinksProgressiveRoadmapYourWebApp]: https://cloudfour.com/thinks/a-progressive-roadmap-for-your-progressive-web-app "Plan progressif de votre application Web progressive"  

[Davrous20191018MythBustingPwasNewEdgeEdition]: https://www.davrous.com/2019/10/18/myth-busting-pwas-the-new-edge-edition "PWAs: la nouvelle version de Microsoft Edge"  

[Fberriman20170626NamingProgressiveWebApps]: https://fberriman.com/2017/06/26/naming-progressive-web-apps "Attribution d’un nom aux applications Web progressives"  

[JoretegBlogBettingWeb]: https://joreteg.com/blog/betting-on-the-web "Paris sur le Web"  

[MediumWebEdgeOfflinePostsProgressiveWebApps]: https://medium.com/web-on-the-edge/offline-posts-with-progressive-web-apps-fc2dc4ad895 "Billets hors ligne avec des applications Web progressives"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-1 "Conception et création d’une application Web progressive sans infrastructure (partie 1)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-2 "Conception et création d’une application Web progressive sans infrastructure (partie 2)"  

[Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]: https://www.smashingmagazine.com/2019/07/progressive-web-application-pwa-framework-part-3 "Conception et création d’une application Web progressive sans infrastructure (partie 3)"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Qu’est-ce qu’une application Web progressive? | Web. dev"  

[Webhint]: https://webhint.io "webhint"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Liaison Poussée-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPs-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Conception de site Web réactif-Wikipédia"  
