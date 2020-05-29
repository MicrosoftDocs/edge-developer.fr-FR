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
ms.openlocfilehash: 482f498e246ee265424f7b80ff3cd67f78501ee2
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583034"
---
# Applications Web progressives sur Windows  

Grâce aux [applications Web progressives][MDNApps] \ (ou simplement à PWAS \), il n’est pas nécessaire de décider de l’utilisation d’une interface Web ouverte pour l’interopérabilité entre les plateformes et de fournir aux utilisateurs une interface utilisateur de type application adaptée à leurs appareils.  Les PWAs sont des sites Web qui sont [progressivement améliorés][AListApartUnderstandingProgressiveEnhancement] pour fonctionner comme des applications natives sur les plateformes prises en charge.  Les qualités d’une PWA combinent le meilleur des applications web et natives.  

:::row:::
    :::column:::
        ![Icône détectable][ImageISearch]
        ### [Détectable][MDNPwaAdvantagesDiscoverable]
        Dans les résultats de recherche Web et les magasins d’applications de support
    :::column-end:::
    :::column:::
        ![Icône installer][ImageIPackage]
        ### [Installation correcte][MDNPwaAdvantagesInstallable]
        Épingler et lancer à partir de l’écran d’accueil, du menu Démarrer, de la barre des tâches, etc.
    :::column-end:::
    :::column:::
        ![Icône de réinstallation][ImageIPushNotification]
        ### [Nouvelle installation][MDNPwaAdvantagesReEngageable]
        Envoyer des notifications de transmission, même lorsque l’application n’est pas active
    :::column-end:::
    :::column:::
        ![Icône indépendante du réseau][ImageIOffline]
        ### [Indépendant du réseau][MDNPwaAdvantagesNetworkIndependent]
        Fonctionne hors ligne et dans des conditions de faible réseau
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Icône progressif][ImageIProgressive]
        ### [Avantage][MDNPwaAdvantagesProgressive]
        L’accès évolue vers le haut (ou vers le bas) avec les fonctionnalités de l’appareil
    :::column-end:::
    :::column:::
        ![Icône sûr][ImageISecurity]
        ### [Approuvés][MDNPwaAdvantagesSafe]
        Fournit un point de terminaison sécurisé HTTPs et d’autres protections de l’utilisateur
    :::column-end:::
    :::column:::
        ![Icône réactive][ImageIResponsive]
        ### [Réactivité][MDNPwaAdvantagesResponsive]
        S’adapte à la taille de l’écran ou à l’orientation de l’utilisateur et à la méthode d’entrée
    :::column-end:::
    :::column:::
        ![Icône de liaison][ImageILink]
        ### [Liens hypertexte][MDNPwaAdvantagesLinkable]
        Partager et lancer à partir d’un lien hypertexte standard
    :::column-end:::
:::row-end:::

En construisant ou en convertissant votre site existant vers une application Project Web App, vous vous engagez à améliorer la qualité de votre public grâce à des notifications de transmission, une intégration de type application et une prise en charge hors connexion.  En même temps, vous devez continuer à créer votre public sur le Web ouvert, car les utilisateurs découvrent votre PWA par le biais de la recherche et du partage de liens.  Mieux, vous pouvez mettre à jour votre application en mettant simplement à jour votre code serveur Web.  

## PWAs sur Microsoft Edge (chrome)  

Lorsque vous générez une API standard Web pour cibler une application Web, votre application peut être déployée sur différentes plateformes et appareils et tirer parti des fonctionnalités spécifiques à l’appareil disponibles.  PWAs dans Microsoft Edge \ (chrome \) sont entièrement conformes aux normes du point de vue de la plateforme Web et permettent aux utilisateurs d’installer l’application directement à partir du navigateur sans nécessiter de déploiement ou d’inscription sur le Windows Store.  Les PWAs de bureau sont prises en charge sur n’importe quelle plate-forme Microsoft Edge \ (chrome \) est disponible, y compris Windows 7, Windows 10 et macOS.  Voici d’autres avantages:  

*   Les applications sont installées directement à partir du navigateur à l’aide de l’icône d' **installation** dans la barre de navigation.  
    
    ![Installer le menu volant et l’icône d’application][ImageInstallPwa]  
    
*   Les applications pourront également être installées, exécutées et gérées à partir du menu **paramètres**des  >  **applications**  
    
    ![Éléments de menu de l’application sous paramètres][ImageAppMenus]  

*   Les notifications Web sont intégrées dans le système de notification Windows
*   Magasin de cookies partagés avec le profil de navigateur qui a installé l’application
*   Accès à d’autres fonctionnalités de navigateur via le `...` menu, notamment la validation de certificats, les autorisations de site, la protection contre le suivi et les extensions de navigateur
*   Un accès complet à [Microsoft Edge devtools][DevtoolsProgressiveWebApps] pour le débogage de votre application  

> [!IMPORTANT]
> Pour personnaliser PWAs en particulier pour Windows 10 qui effectue des demandes d’API WinRT en utilisant JavaScript, voir la [documentation spécifique aux fonctionnalités de EdgeHTML de Project Web App][PwaEdgehtmlIndex].  En savoir plus sur le test de votre PWA sur Windows 10 et son distribution dans le Microsoft Store.  

## Configuration requise  

Pour être exécuté en tant que PWA, votre application Web hébergée sur un serveur doit inclure la configuration minimale requise.  

|  | Condition requise | Détails | 
|:--- |:--- |:--- |  
| X | [HTTPS][WikiHttps] | Protégez vos utilisateurs en fournissant une connexion sécurisée pour la communication avec le serveur ou l’application.  Les travailleurs de service et autres technologies PWA fonctionnent uniquement avec les ressources Web fournies par le biais d’une connexion sécurisée (ou à partir `localhost` de à des fins de débogage \).  |  
| X | [Travailleurs de service][MDNServiceWorkerApi] | Les threads de travail de service permettent de faire office de proxy réseau entre votre serveur et votre application cliente afin de fournir une prise en charge hors connexion, une mise en cache de ressources, des notifications de transmission, une synchronisation en arrière-plan  |  
| X | [Manifeste de l’application Web][MDNWebAppManifest] | Fournissez un fichier de métadonnées JSON décrivant les informations clés relatives à votre application Web (par exemple, les icônes, le langage et le point d’entrée d’URL \), de sorte que Windows 10 et d’autres plateformes hôtes puissent fournir à vos utilisateurs de Project Web App une interface d’utilisateur d’application native et installable.  |  

Pour être une bonne solution de Project Web App, votre application doit également présenter la configuration requise suivante.  

|  | Condition requise | Détails | 
|:--- |:--- |:--- |  
| X | [Compatibilité entre les navigateurs][MDNCrossBrowserTesting] | Assurez-vous que le contrôle PWA fonctionne en effectuant des [tests][MicrosoftDeveloperEdgeToolsRemote] dans différents navigateurs et environnements.  |  
| X | [Conception réactive][WikiResponsiveWebDesign] | Utilisez des dispositions fluides et des images flexibles grâce à une [grille][MDNCssGridLayout]CSS, des [Flexbox][MDNCssFlexibleBoxLayout], [des feuilles CSS et des][MDNCssGridLayout] [Flexbox][MDNCssFlexibleBoxLayout] , des [requêtes multimédias][MDNMediaQueries]et des [images réactives][MDNResponsiveImages] pour adapter votre expérience utilisateur à l’appareil de l’utilisateur.  Utilisez les [Outils d’émulation d’appareil][DevToolsGuide|::ref1::|] de votre navigateur pour effectuer des tests en local, ou configurez une session de [débogage à distance][DevToolsProtocolClientsEdgeDevToolsPreview] pour tester directement sur un appareil cible.  |  
| X | [Liaison Poussée][WikiDeepLinking] | Acheminez chaque page de votre site vers une URL unique de sorte que les utilisateurs existants puissent vous aider à renforcer un public encore plus large grâce au partage de réseaux sociaux.  |  
| X | [Bonnes pratiques][Webhint] | Utilisez les outils de qualité de code comme le [webhint][Webhint] de type Lint pour optimiser l’efficacité, la robustesse, la sécurité et l’accessibilité de votre application.  |  
| X | [Liste de vérification de Project Web App][WebDevGoodPwaChecklist] | Vérifiez votre PWA par rapport à la liste de vérification de base sur Google Baseline.  |  

Si vous voulez transformer votre document PWA en application [Microsoft Store][MicrosoftDeveloperStore] , accédez à la documentation sur les [applications Web progressives (EdgeHTML)][PwaEdgehtmlMicrosoftStore] .  

## Disponibilité actuelle  

La prise en charge du moteur de navigateur pour les demandes d’applications Web progressives pour un certain nombre de composants architecturaux, l’infrastructure réseau la plus importante sous-jacente de l' [API FETCH][MDNFetchApi].  

Dans le cadre de l’utilisation de Microsoft Edge \ (chrome), la plateforme de navigateur prend en charge les fonctionnalités suivantes sur les appareils dans lesquels Microsoft Edge \ (chrome \) est pris en charge.  

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

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clients du protocole Microsoft Edge DevTools Preview-DevTools"  
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

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[WebDevGoodPwaChecklist]: https://web.dev/pwa-checklist "Qu’est-ce qu’une application Web progressive? | Web. dev"  

[Webhint]: https://webhint.io "Astuce"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Liaison Poussée-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPs-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Conception de site Web réactif-Wikipédia"  
