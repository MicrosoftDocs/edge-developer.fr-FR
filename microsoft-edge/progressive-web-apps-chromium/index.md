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
# Vue d’ensemble des applications Web progressivement sur Windows  

Les [applications Web progressives][MDNApps] \ (PWAS \) offrent un accès aux technologies Web ouvertes pour une interopérabilité multiplateforme et fournissent aux utilisateurs une interface native et de type application adaptée à leurs appareils.  Les PWAs sont des sites Web qui sont [progressivement améliorés][AListApartUnderstandingProgressiveEnhancement] pour fonctionner comme des applications natives sur les plateformes prises en charge.  Les qualités d’une PWA combinent le meilleur des applications web et natives.  

:::row:::
    :::column:::
        :::image type="icon" source="./media/i_search.png":::
        ### [Détectable][MDNPwaAdvantagesDiscoverable]
        Dans les résultats de recherche Web et les magasins d’applications de support
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_package.png":::
        ### [Installation correcte][MDNPwaAdvantagesInstallable]
        Épingler et lancer à partir de l’écran d’accueil, du menu Démarrer, de la barre des tâches, etc.
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_push-notification.png":::
        ### [Nouvelle installation][MDNPwaAdvantagesReEngageable]
        Envoyer des notifications de transmission, même lorsque l’application n’est pas active
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_offline.png":::
        ### [Indépendant du réseau][MDNPwaAdvantagesNetworkIndependent]
        Fonctionne hors ligne et dans des conditions de faible réseau
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_progressive.png":::
        ### [Avantage][MDNPwaAdvantagesProgressive]
        L’accès évolue vers le haut (ou vers le bas) avec les fonctionnalités de l’appareil
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_security.png":::
        ### [Approuvés][MDNPwaAdvantagesSafe]
        Fournit un point de terminaison sécurisé HTTPs et d’autres protections de l’utilisateur
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        :::image type="icon" source="./media/i_responsive.png":::
        ### [Réactivité][MDNPwaAdvantagesResponsive]
        S’adapte à la taille de l’écran ou à l’orientation de l’utilisateur et à la méthode d’entrée
    :::column-end:::
    :::column:::
        :::image type="icon" source="./media/i_link.png":::
        ### [Liens hypertexte][MDNPwaAdvantagesLinkable]
        Partager et lancer à partir d’un lien hypertexte standard
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  


Créez \ (ou convertissez) votre site Web existant vers un site PWA pour améliorer vos engagements.  Les améliorations incluent les notifications de transmission, l’intégration de type application et la prise en charge hors connexion.  Continuez à développer votre public sur le Web ouvert pour que les utilisateurs puissent découvrir votre PWA par le biais de la recherche et du partage de liens.  Mieux, votre application est mise à jour à l’aide de votre code serveur Web.  

## PWAs sur Microsoft Edge (chrome)  

Lorsque vous générez une API standard Web pour cibler une application Web, votre application peut être déployée sur différentes plateformes et appareils et tirer parti des fonctionnalités spécifiques à l’appareil.  PWAs dans Microsoft Edge \ (chrome \) ajoutez les avantages suivants à votre site Web.  

*   Votre application est basée sur une plateforme Web standard.  
*   Permet aux utilisateurs d’installer votre application directement à partir du navigateur.  
*   Permet à vos utilisateurs d’installer votre application sans déploiement ou inscription sur le Windows Store.  
    
Les PWAs de bureau sont prises en charge sur n’importe quelle plateforme Microsoft Edge \ (chrome \) est disponible. Microsoft Edge \ (chrome \) est disponible sur Windows 7, Windows 10 et macOS.  Les avantages suivants sont inclus.  

*   Les applications sont installées directement à partir du navigateur à l’aide de l’icône d' **installation** dans la barre de navigation.  
    
    :::image type="complex" source="./media/install_pwa_icon.png" alt-text="Installer le menu volant et l’icône d’application" lightbox="./media/install_pwa_icon.png":::
       Installer le menu volant et l’icône d’application  
    :::image-end:::  
    
*   Les applications risquent également d’être installées, exécutées et **** gérées dans le menu des  >  **applications** paramètres  
    
    :::image type="complex" source="./media/app_menus.png" alt-text="Éléments de menu de l’application sous paramètres" lightbox="./media/app_menus.png":::
       Éléments de menu de l’application sous paramètres  
    :::image-end:::  
    
*   Les notifications Web sont intégrées dans le système de notification Windows  
*   Magasin de cookies partagés avec le profil de navigateur qui a installé l’application  
*   Accès à d’autres fonctionnalités de navigateur à l’aide du menu **paramètre et plus** \ ( `...` \), avec la validation de certificats, les autorisations de site, la protection contre le suivi et les extensions de navigateur  
*   Un accès complet à [Microsoft Edge devtools][DevtoolsProgressiveWebApps] pour le débogage de votre application  
    
> [!IMPORTANT]
> Pour personnaliser PWAs en particulier pour les Windows 10 qui effectuent des demandes d’API WinRT en utilisant JavaScript, accédez à [documentation spécifique aux fonctionnalités de EdgeHTML PWA] [PwaEdgehtmlIndex].  En savoir plus sur le test de votre PWA sur Windows 10 et son distribution dans le Microsoft Store.  

> [!NOTE]
> Pour plus d’informations sur les avantages, les fonctionnalités à venir et les courtes démonstrations de Project Web App, accédez à la [version 2020 de la session PWA][BuildVideo]. 

## Conditions requises  

Pour être exécuté en tant que PWA, votre application Web hébergée sur un serveur doit inclure la configuration minimale requise.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Protège vos utilisateurs en fournissant une connexion sécurisée pour la communication avec le serveur ou l’application.  Les travailleurs de service et autres technologies PWA fonctionnent uniquement avec les ressources Web fournies par le biais d’une connexion sécurisée (ou à partir `localhost` de à des fins de débogage \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Worker du service][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Utilise des threads de travail de service pour agir en tant que proxy réseau entre votre serveur et votre application cliente.  Les threads de travail en mode hors connexion, de mise en cache des ressources, de notifications de transmission, de synchronisation des données en arrière-plan et d’optimisation des performances de la page.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Manifeste de l’application Web][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Fournit un fichier de métadonnées JSON qui décrit les informations clés relatives à votre application Web, de sorte que les plateformes Windows 10 et d’autres plateformes puissent offrir aux utilisateurs de Project Web App une environnement d’exécution de l’application, qui permet d’installer une application native.  Les informations clés incluent les icônes, la langue et le point d’entrée d’URL. 
   :::column-end:::
:::row-end:::  

Pour être une bonne solution de Project Web App, votre application doit également présenter la configuration requise suivante.  

:::row:::
   :::column span="1":::
      [Compatibilité entre les navigateurs][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Assurez-vous que le contrôle PWA fonctionne en effectuant des [tests][MicrosoftDeveloperEdgeToolsRemote] dans différents navigateurs et environnements.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Conception réactive][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Utilise des dispositions fluides et des images flexibles.  La conception réactive inclut les éléments suivants qui adaptent votre expérience utilisateur à l’appareil de l’utilisateur.  
      
      *   [Grille][MDNCssGridLayout] CSS  
      *   [flexbox][MDNCssFlexibleBoxLayout]  
      *   [Grille][MDNCssGridLayout] CSS et [Flexbox][MDNCssFlexibleBoxLayout]  
      *   [requêtes multimédias][MDNMediaQueries]  
      *   [images réactives][MDNResponsiveImages]  
      
      Utilise des [Outils d’émulation d’appareil][DevToolsGuideDeviceModeTestingOtherBrowsers] de votre navigateur pour le test en local, ou créez une session de débogage à distance sur [Windows][DevtoolsRemoteDebuggingWindows] ou [Android][DevtoolsRemoteDebuggingIndex] pour tester directement sur un appareil cible.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Liaison Poussée][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Route chaque page de votre site vers une URL unique de sorte que les utilisateurs existants puissent vous aider à impliquer un public encore plus large via le partage de réseaux sociaux.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Pratiques en matière de validation et de test][Webhint]  
   :::column-end:::
   :::column span="2":::
      Utilise des outils de qualité de code comme l’élément [webhint][Webhint] de type Lint pour optimiser l’efficacité, la robustesse, la sécurité et l’accessibilité de votre application.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Liste de vérification de Project Web App][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Vérifie votre PWA par rapport à la liste de vérification de base sur Google Baseline.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Pour transformer votre emplacement PWA en application du [Microsoft Store][MicrosoftDeveloperStore] , accédez à [application Web applications (EdgeHTML) sur le Microsoft Store] [PwaEdgehtmlMicrosoftStore].  
  
## Voir également  

*   [PWAs de combustion de mythe][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Plan progressif de votre application Web progressive][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Billets hors ligne avec des applications Web progressives][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Paris sur le Web][JoretegBlogBettingWeb]  
*   [Attribution d’un nom aux applications Web progressives][Fberriman20170626NamingProgressiveWebApps]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 1)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart1]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 2)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart2]  
*   [Conception et création d’une application Web progressive sans infrastructure (partie 3)][Smashingmagazine201907ProgressiveWebApplicationFrameworkPart3]  
    
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
