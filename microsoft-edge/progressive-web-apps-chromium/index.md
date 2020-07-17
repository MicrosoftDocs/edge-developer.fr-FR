---
description: Les applications Web progressives s’exécutent en mode natif sur Windows 10.  Voici ce que vous devez savoir en tant que développeur Web.
title: Applications Web progressives sur Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications Web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 90740bac07ebfd74f89e2524e6955621e1b09b05
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882806"
---
# <span data-ttu-id="9d357-105">Applications Web progressives sur Windows</span><span class="sxs-lookup"><span data-stu-id="9d357-105">Progressive Web Apps on Windows</span></span>  

<span data-ttu-id="9d357-106">Grâce aux [applications Web progressives][MDNApps] \ (ou simplement à PWAS \), il n’est pas nécessaire de décider de l’utilisation d’une interface Web ouverte pour l’interopérabilité entre les plateformes et de fournir aux utilisateurs une interface utilisateur de type application adaptée à leurs appareils.</span><span class="sxs-lookup"><span data-stu-id="9d357-106">With [Progressive Web Apps][MDNApps] \(or simply PWAs\), you do not have to decide between using open web technologies for cross-platform interoperability and providing your users with a native app-like experience customized for their devices.</span></span>  <span data-ttu-id="9d357-107">Les PWAs sont des sites Web qui sont [progressivement améliorés][AListApartUnderstandingProgressiveEnhancement] pour fonctionner comme des applications natives sur les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="9d357-107">PWAs are just websites that are [progressively enhanced][AListApartUnderstandingProgressiveEnhancement] to function like native apps on supporting platforms.</span></span>  <span data-ttu-id="9d357-108">Les qualités d’une PWA combinent le meilleur des applications web et natives.</span><span class="sxs-lookup"><span data-stu-id="9d357-108">The qualities of a PWA combine the best of the web and native apps.</span></span>  

:::row:::
    :::column:::
        ![Icône détectable][ImageISearch]
        ### [<span data-ttu-id="9d357-110">Détectable</span><span class="sxs-lookup"><span data-stu-id="9d357-110">Discoverable</span></span>][MDNPwaAdvantagesDiscoverable]
        <span data-ttu-id="9d357-111">Dans les résultats de recherche Web et les magasins d’applications de support</span><span class="sxs-lookup"><span data-stu-id="9d357-111">From web search results and supporting app stores</span></span>
    :::column-end:::
    :::column:::
        ![Icône installer][ImageIPackage]
        ### [<span data-ttu-id="9d357-113">Installation correcte</span><span class="sxs-lookup"><span data-stu-id="9d357-113">Installable</span></span>][MDNPwaAdvantagesInstallable]
        <span data-ttu-id="9d357-114">Épingler et lancer à partir de l’écran d’accueil, du menu Démarrer, de la barre des tâches, etc.</span><span class="sxs-lookup"><span data-stu-id="9d357-114">Pin and launch from the home screen, Start Menu, Taskbar, and so on</span></span>
    :::column-end:::
    :::column:::
        ![Icône de réinstallation][ImageIPushNotification]
        ### [<span data-ttu-id="9d357-116">Nouvelle installation</span><span class="sxs-lookup"><span data-stu-id="9d357-116">Re-engageable</span></span>][MDNPwaAdvantagesReEngageable]
        <span data-ttu-id="9d357-117">Envoyer des notifications de transmission, même lorsque l’application n’est pas active</span><span class="sxs-lookup"><span data-stu-id="9d357-117">Send push notifications, even when the app is not active</span></span>
    :::column-end:::
    :::column:::
        ![Icône indépendante du réseau][ImageIOffline]
        ### [<span data-ttu-id="9d357-119">Indépendant du réseau</span><span class="sxs-lookup"><span data-stu-id="9d357-119">Network Independent</span></span>][MDNPwaAdvantagesNetworkIndependent]
        <span data-ttu-id="9d357-120">Fonctionne hors ligne et dans des conditions de faible réseau</span><span class="sxs-lookup"><span data-stu-id="9d357-120">Works offline and in low-network conditions</span></span>
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Icône progressif][ImageIProgressive]
        ### [<span data-ttu-id="9d357-122">Avantage</span><span class="sxs-lookup"><span data-stu-id="9d357-122">Progressive</span></span>][MDNPwaAdvantagesProgressive]
        <span data-ttu-id="9d357-123">L’accès évolue vers le haut (ou vers le bas) avec les fonctionnalités de l’appareil</span><span class="sxs-lookup"><span data-stu-id="9d357-123">Experience scales up (or down) with device capabilities</span></span>
    :::column-end:::
    :::column:::
        ![Icône sûr][ImageISecurity]
        ### [<span data-ttu-id="9d357-125">Approuvés</span><span class="sxs-lookup"><span data-stu-id="9d357-125">Safe</span></span>][MDNPwaAdvantagesSafe]
        <span data-ttu-id="9d357-126">Fournit un point de terminaison sécurisé HTTPs et d’autres protections de l’utilisateur</span><span class="sxs-lookup"><span data-stu-id="9d357-126">Provides a secure HTTPS endpoint and other user safeguards</span></span>
    :::column-end:::
    :::column:::
        ![Icône réactive][ImageIResponsive]
        ### [<span data-ttu-id="9d357-128">Réactivité</span><span class="sxs-lookup"><span data-stu-id="9d357-128">Responsive</span></span>][MDNPwaAdvantagesResponsive]
        <span data-ttu-id="9d357-129">S’adapte à la taille de l’écran ou à l’orientation de l’utilisateur et à la méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="9d357-129">Adapts to the user's screen size or orientation and input method</span></span>
    :::column-end:::
    :::column:::
        ![Icône de liaison][ImageILink]
        ### [<span data-ttu-id="9d357-131">Liens hypertexte</span><span class="sxs-lookup"><span data-stu-id="9d357-131">Linkable</span></span>][MDNPwaAdvantagesLinkable]
        <span data-ttu-id="9d357-132">Partager et lancer à partir d’un lien hypertexte standard</span><span class="sxs-lookup"><span data-stu-id="9d357-132">Share and launch from a standard hyperlink</span></span>
    :::column-end:::
:::row-end:::

<span data-ttu-id="9d357-133">En construisant ou en convertissant votre site existant vers une application Project Web App, vous vous engagez à améliorer la qualité de votre public grâce à des notifications de transmission, une intégration de type application et une prise en charge hors connexion.</span><span class="sxs-lookup"><span data-stu-id="9d357-133">By building or converting your existing site to a PWA, you engage better with your existing audience using push notifications, app-like integration, and offline support.</span></span>  <span data-ttu-id="9d357-134">En même temps, vous devez continuer à créer votre public sur le Web ouvert, car les utilisateurs découvrent votre PWA par le biais de la recherche et du partage de liens.</span><span class="sxs-lookup"><span data-stu-id="9d357-134">At the same time, you should continue to build your audience on the open web, as users discover your PWA through search and link-sharing.</span></span>  <span data-ttu-id="9d357-135">Mieux, vous pouvez mettre à jour votre application en mettant simplement à jour votre code serveur Web.</span><span class="sxs-lookup"><span data-stu-id="9d357-135">Best of all, you may update your app by simply updating your web server code.</span></span>  

## <span data-ttu-id="9d357-136">PWAs sur Microsoft Edge (chrome)</span><span class="sxs-lookup"><span data-stu-id="9d357-136">PWAs on Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="9d357-137">Lorsque vous générez une API standard Web pour cibler une application Web, votre application peut être déployée sur différentes plateformes et appareils et tirer parti des fonctionnalités spécifiques à l’appareil disponibles.</span><span class="sxs-lookup"><span data-stu-id="9d357-137">When you build a Progressive Web App targeting web standard APIs, your application may be deployed across platforms and devices and take advantage of the device specific capabilities as available.</span></span>  <span data-ttu-id="9d357-138">PWAs dans Microsoft Edge \ (chrome \) sont entièrement conformes aux normes du point de vue de la plateforme Web et permettent aux utilisateurs d’installer l’application directement à partir du navigateur sans nécessiter de déploiement ou d’inscription sur le Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9d357-138">PWAs in Microsoft Edge \(Chromium\) are completely standards-based from a web platform perspective and enable users to install the app directly from within the browser without the need for Store-based deployment or registration.</span></span>  <span data-ttu-id="9d357-139">Les PWAs de bureau sont prises en charge sur n’importe quelle plate-forme Microsoft Edge \ (chrome \) est disponible, y compris Windows 7, Windows 10 et macOS.</span><span class="sxs-lookup"><span data-stu-id="9d357-139">Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is available, including Windows 7, Windows 10, and macOS.</span></span>  <span data-ttu-id="9d357-140">Voici d’autres avantages:</span><span class="sxs-lookup"><span data-stu-id="9d357-140">Other benefits include:</span></span>  

*   <span data-ttu-id="9d357-141">Les applications sont installées directement à partir du navigateur à l’aide de l’icône d' **installation** dans la barre de navigation.</span><span class="sxs-lookup"><span data-stu-id="9d357-141">Applications may be installed directly from within the browser via the **Install** icon in the navigation bar.</span></span>  
    
    ![Installer le menu volant et l’icône d’application][ImageInstallPwa]  
    
*   <span data-ttu-id="9d357-143">Les applications pourront également être installées, exécutées et gérées à partir du menu **paramètres**des  >  **applications**</span><span class="sxs-lookup"><span data-stu-id="9d357-143">Applications may also be installed, run and managed from the **Settings** > **Apps** menu</span></span>  
    
    ![Éléments de menu de l’application sous paramètres][ImageAppMenus]  

*   <span data-ttu-id="9d357-145">Les notifications Web sont intégrées dans le système de notification Windows</span><span class="sxs-lookup"><span data-stu-id="9d357-145">Web Notifications are integrated into the Windows notification system</span></span>
*   <span data-ttu-id="9d357-146">Magasin de cookies partagés avec le profil de navigateur qui a installé l’application</span><span class="sxs-lookup"><span data-stu-id="9d357-146">Shared cookie store with the browser profile that installed the app</span></span>
*   <span data-ttu-id="9d357-147">Accès à d’autres fonctionnalités de navigateur via le `...` menu, notamment la validation de certificats, les autorisations de site, la protection contre le suivi et les extensions de navigateur</span><span class="sxs-lookup"><span data-stu-id="9d357-147">Access to other browser features via the `...` menu including certificate validation, site permissions, tracking protection, and browser extensions</span></span>
*   <span data-ttu-id="9d357-148">Un accès complet à [Microsoft Edge devtools][DevtoolsProgressiveWebApps] pour le débogage de votre application</span><span class="sxs-lookup"><span data-stu-id="9d357-148">Full access to [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] for debugging your app</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="9d357-149">Pour personnaliser PWAs en particulier pour Windows 10 qui effectue des demandes d’API WinRT en utilisant JavaScript, voir la [documentation spécifique aux fonctionnalités de EdgeHTML de Project Web App][PwaEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="9d357-149">To tailor PWAs specifically for Windows 10 that make WinRT API requests using JavaScript, see the [documentation specific to the EdgeHTML PWA features][PwaEdgehtmlIndex].</span></span>  <span data-ttu-id="9d357-150">En savoir plus sur le test de votre PWA sur Windows 10 et son distribution dans le Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9d357-150">Learn more about testing your PWA on Windows 10 and distributing it in the Microsoft Store.</span></span>  

> [!NOTE]
> <span data-ttu-id="9d357-151">Pour obtenir une vue d’ensemble des avantages de Project Web App, des fonctionnalités à venir et des courtes démonstrations, consultez la [session de création 2020][BuildVideo] .</span><span class="sxs-lookup"><span data-stu-id="9d357-151">Check out the [Build 2020 PWA session][BuildVideo] for an overview of PWA benefits, upcoming features and short demos.</span></span> 

## <span data-ttu-id="9d357-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d357-152">Requirements</span></span>  

<span data-ttu-id="9d357-153">Pour être exécuté en tant que PWA, votre application Web hébergée sur un serveur doit inclure la configuration minimale requise.</span><span class="sxs-lookup"><span data-stu-id="9d357-153">To run as a PWA, your server-hosted web app should include following minimum requirements.</span></span>  

| <span data-ttu-id="9d357-154">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d357-154">Requirement</span></span> | <span data-ttu-id="9d357-155">Détails</span><span class="sxs-lookup"><span data-stu-id="9d357-155">Details</span></span> | 
|:--- |:--- |  
| [<span data-ttu-id="9d357-156">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9d357-156">HTTPS</span></span>][WikiHttps] | <span data-ttu-id="9d357-157">Protégez vos utilisateurs en fournissant une connexion sécurisée pour la communication avec le serveur ou l’application.</span><span class="sxs-lookup"><span data-stu-id="9d357-157">Protect your users by providing a secure connection for server or app communication.</span></span>  <span data-ttu-id="9d357-158">Les travailleurs de service et autres technologies PWA fonctionnent uniquement avec les ressources Web fournies par le biais d’une connexion sécurisée (ou à partir `localhost` de à des fins de débogage \).</span><span class="sxs-lookup"><span data-stu-id="9d357-158">Service Workers and other PWA technologies only work with web resources served over a secure connection \(or from `localhost` for debugging purposes\).</span></span>  |  
| [<span data-ttu-id="9d357-159">Worker du service</span><span class="sxs-lookup"><span data-stu-id="9d357-159">Service Workers</span></span>][MDNServiceWorkerApi] | <span data-ttu-id="9d357-160">Les threads de travail de service permettent de faire office de proxy réseau entre votre serveur et votre application cliente afin de fournir une prise en charge hors connexion, une mise en cache de ressources, des notifications de transmission, une synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="9d357-160">Use Service Worker threads to act as network proxies between your server and client app in order to provide offline support, resource caching, push notifications, background data sync, and  page load perf optimizations.</span></span>  |  
| [<span data-ttu-id="9d357-161">Manifeste de l’application Web</span><span class="sxs-lookup"><span data-stu-id="9d357-161">Web App Manifest</span></span>][MDNWebAppManifest] | <span data-ttu-id="9d357-162">Fournissez un fichier de métadonnées JSON décrivant les informations clés relatives à votre application Web (par exemple, les icônes, le langage et le point d’entrée d’URL \), de sorte que Windows 10 et d’autres plateformes hôtes puissent fournir à vos utilisateurs de Project Web App une interface d’utilisateur d’application native et installable.</span><span class="sxs-lookup"><span data-stu-id="9d357-162">Provide a JSON-based metadata file describing key information about your web app \(such as icons, language, and URL entry point\), so that Windows 10 and other host platforms are able to provide your PWA users with an installable, native app-like experience.</span></span>  |  

<span data-ttu-id="9d357-163">Pour être une bonne solution de Project Web App, votre application doit également présenter la configuration requise suivante.</span><span class="sxs-lookup"><span data-stu-id="9d357-163">To be a great PWA, your app must also meet the following requirements.</span></span>  

| <span data-ttu-id="9d357-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d357-164">Requirement</span></span> | <span data-ttu-id="9d357-165">Détails</span><span class="sxs-lookup"><span data-stu-id="9d357-165">Details</span></span> | 
|:--- |:--- |  
| [<span data-ttu-id="9d357-166">Compatibilité entre les navigateurs</span><span class="sxs-lookup"><span data-stu-id="9d357-166">Cross-browser compatibility</span></span>][MDNCrossBrowserTesting] | <span data-ttu-id="9d357-167">Assurez-vous que le contrôle PWA fonctionne en effectuant des [tests][MicrosoftDeveloperEdgeToolsRemote] dans différents navigateurs et environnements.</span><span class="sxs-lookup"><span data-stu-id="9d357-167">Ensure your PWA works by [testing][MicrosoftDeveloperEdgeToolsRemote] in different browsers and environments.</span></span>  |  
| [<span data-ttu-id="9d357-168">Conception réactive</span><span class="sxs-lookup"><span data-stu-id="9d357-168">Responsive design</span></span>][WikiResponsiveWebDesign] | <span data-ttu-id="9d357-169">Utilisez des dispositions fluides et des images flexibles grâce à une [grille][MDNCssGridLayout]CSS, des [Flexbox][MDNCssFlexibleBoxLayout], [des feuilles CSS et des][MDNCssGridLayout] [Flexbox][MDNCssFlexibleBoxLayout] , des [requêtes multimédias][MDNMediaQueries]et des [images réactives][MDNResponsiveImages] pour adapter votre expérience utilisateur à l’appareil de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9d357-169">Employ fluid layouts and flexible images with CSS [grid][MDNCssGridLayout], [flexbox][MDNCssFlexibleBoxLayout], CSS [grid][MDNCssGridLayout] and [flexbox][MDNCssFlexibleBoxLayout] , [media queries][MDNMediaQueries], and [responsive images][MDNResponsiveImages] to adapt your UX to your user's device.</span></span>  <span data-ttu-id="9d357-170">Utilisez les [Outils d’émulation d’appareil][DevToolsGuide|::ref1::|] de votre navigateur pour effectuer des tests en local, ou configurez une session de [débogage à distance][DevToolsProtocolClientsEdgeDevToolsPreview] pour tester directement sur un appareil cible.</span><span class="sxs-lookup"><span data-stu-id="9d357-170">Use [device emulation tools][DevToolsGuide|::ref1::|] from your browser to test locally, or set up a [remote debugging session][DevToolsProtocolClientsEdgeDevToolsPreview] to test directly on a target device.</span></span>  |  
| [<span data-ttu-id="9d357-171">Liaison Poussée</span><span class="sxs-lookup"><span data-stu-id="9d357-171">Deep linking</span></span>][WikiDeepLinking] | <span data-ttu-id="9d357-172">Acheminez chaque page de votre site vers une URL unique de sorte que les utilisateurs existants puissent vous aider à renforcer un public encore plus large grâce au partage de réseaux sociaux.</span><span class="sxs-lookup"><span data-stu-id="9d357-172">Route each page of your site to a unique URL so existing users may help you engage an even broader audience through social media sharing.</span></span>  |  
| [<span data-ttu-id="9d357-173">Bonnes pratiques</span><span class="sxs-lookup"><span data-stu-id="9d357-173">Best practices</span></span>][Webhint] | <span data-ttu-id="9d357-174">Utilisez les outils de qualité de code comme le [webhint][Webhint] de type Lint pour optimiser l’efficacité, la robustesse, la sécurité et l’accessibilité de votre application.</span><span class="sxs-lookup"><span data-stu-id="9d357-174">Use code quality tools like the [Webhint][Webhint] linter to optimize the efficiency, robustness, safety, and accessibility of your app.</span></span>  |  
| [<span data-ttu-id="9d357-175">Liste de vérification de Project Web App</span><span class="sxs-lookup"><span data-stu-id="9d357-175">Chromium PWA Checklist</span></span>][WebDevGoodPwaChecklist] | <span data-ttu-id="9d357-176">Vérifiez votre PWA par rapport à la liste de vérification de base sur Google Baseline.</span><span class="sxs-lookup"><span data-stu-id="9d357-176">Check your PWA against the Google baseline PWA checklist.</span></span>  |  

<span data-ttu-id="9d357-177">Si vous voulez transformer votre document PWA en application [Microsoft Store][MicrosoftDeveloperStore] , accédez à la documentation sur les [applications Web progressives (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .</span><span class="sxs-lookup"><span data-stu-id="9d357-177">If you want to turn your PWA into a [Microsoft Store][MicrosoftDeveloperStore] application, head to the [Progressive Web Apps (EdgeHTML)][PwaEdgehtmlMicrosoftStore] documentation.</span></span>  
  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

[ImageInstallPwa]: ./media/Install_PWA.png  
[ImageAppMenus]: ./media/App_menus.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Aperçu DevTools Microsoft Edge - Clients de protocole DevTools "  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Émulation"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps.md "Déboguer des applications Web progressives"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Nouveautés de EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Nouveautés de EdgeHTML 14"  
[PwaEdgehtmlIndex]: ../progressive-web-apps-edgehtml/index.md "Applications Web progressives (EdgeHTML) sur Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Applications Web progressives dans la boutique Microsoft"
<!--PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Criteria for automatic submission - Progressive Web Apps in the Microsoft Store"  -->  

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Vue d’ensemble des services de notifications Windows (WNS \)"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Conception pour Xbox et télévision"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Considérations relatives à l’interface utilisateur pour les appareils UWP"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Qu’est-ce qu’une application de plateforme Windows universelle (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Prendre en charge votre application avec des tâches en arrière-plan"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publier des applications et des jeux Windows"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Ouverture d’un compte de développeur"  

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

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Qu’est-ce qu’une application Web progressive? | Web. dev"  

[Webhint]: https://webhint.io "Astuce"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Liaison Poussée-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPs-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Conception de site Web réactif-Wikipédia"  
