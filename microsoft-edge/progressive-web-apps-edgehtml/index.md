---
description: Les applications Web progressives s’exécutent en mode natif sur Windows 10.  Voici ce que vous devez savoir en tant que développeur Web.
title: Applications Web progressives (EdgeHTML) sur Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: applications Web progressives, PWA, Edge, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 778502f6db9a89da810b4fb59b10e8fb889fa4b5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10564647"
---
# Applications Web progressives (EdgeHTML) sur Windows  

Avec l’application [Web progressive][MDNApps] (ou simplement PWAS), il n’est pas nécessaire de décider de l’utilisation de technologies ouvertes sur le Web pour l’interopérabilité entre les plateformes et de fournir aux utilisateurs une interface utilisateur de type application personnalisée pour leur appareil.  En effet, les PWAs sont des sites Web qui sont [progressivement améliorés][AListApartUnderstandingProgressiveEnhancement] pour fonctionner comme des applications natives sur les plateformes de support technique.  Les qualités d’une PWA combinent le meilleur des applications web et natives.  

:::row:::
    :::column:::
        ![Icône détectable][ImageISearch]
        ### [Détectable][MDNPwaAdvantagesDiscoverable]
        Dans les résultats de recherche Web et les magasins d’applications de support
    :::column-end:::
    :::column:::
        ![Icône installer][ImageIPackage]
        ### [Installation correcte][MDNPwaAdvantagesInstallable]
        Épingler et lancer à partir de l’écran d’accueil  
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
        Évolution des performances de l’appareil à l’aide de la fonctionnalité  
    :::column-end:::
    :::column:::
        ![Icône sûr][ImageISecurity]
        ### [Approuvés][MDNPwaAdvantagesSafe]
        Fournit un point de terminaison sécurisé HTTPs et d’autres protections de l’utilisateur  
    :::column-end:::
    :::column:::
        ![Icône réactive][ImageIResponsive]
        ### [Réactivité][MDNPwaAdvantagesResponsive]
        S’adapte à la taille/orientation de l’écran de l’utilisateur et méthode d’entrée  
    :::column-end:::
    :::column:::
        ![Icône de liaison][ImageILink]
        ### [Liens hypertexte][MDNPwaAdvantagesLinkable]
        Partager et lancer à partir d’un lien hypertexte standard  
    :::column-end:::
:::row-end:::

En construisant ou en convertissant votre site existant en PWA, vous pouvez contacter votre public actuel grâce aux notifications de transmission et à la prise en charge hors connexion.  En même temps, vous pouvez continuer à créer votre public sur le Web ouvert, car les utilisateurs découvrent votre PWA par le biais de la recherche et du partage de liens.  

## PWAs sur Windows 10 (EdgeHTML)  

> [!NOTE]
> Lorsque vous migrez vers Microsoft Edge (chrome) à partir de EdgeHTML, les plates-formes Web sous-jacentes utilisées par PWAs sont pas identiques.  Les PWAs Edge (chrome) sont installés à partir du navigateur et exécutés dans celui-ci.  Microsoft Edge (EdgeHTML) PWAs s’exécute en tant qu’application de plateforme Windows universelle (UWP) et utilise l’ancienne version d’EdgeHTML Web.  Si vous avez besoin d’un accès à l’API Windows 10 pour votre PWA, cette documentation EdgeHTML est pour vous.  Si votre objectif est la prise en charge de la plateforme interplateforme sans l’accès à l’API Windows spécifique, reportez-vous à la [documentation sur Project Microsoft Edge (chrome)][PwaChromiumIndex].  

Lorsque vous créez une application Web progressive pour tirer parti de Windows 10, vous pouvez distribuer votre PWA via le [Microsoft Store][MicrosoftDeveloperStore], l’intégralité de l’installation de Windows 10 de 600 + millions d’utilisateurs mensuels actifs représente le public de votre application.  Les applications développées de cette manière s’exécutent en tant qu’applications de [plateforme Windows universelles][WindowsUWPGetStartedGuide] et disposent d’un accès tel qu’aux API WinRT.  Notez que le rendu de votre code à partir de la plateforme Web est EdgeHTML lors de l’utilisation des API WinRT, veillez donc à utiliser la détection de fonctionnalités avant d’appeler des API spécifiques de Windows pour s’assurer que votre PWA peut toujours s’exécuter sur toutes les plateformes où Microsoft Edge \ (chrome \) PWAs est disponible.  

[Voici comment prendre en main][PwaEdgehtmlGetStarted] la conversion de votre application Web en un document PWA \ (EdgeHTML \), le test sur Windows 10 et sa distribution dans le Microsoft Store.  

## Configuration requise  

Pour être exécuté en tant que PWA, votre application Web hébergée sur le serveur nécessite au minimum les éléments suivants:  

*   [X] [https][WikiHttps].  Protégez vos utilisateurs en fournissant une connexion sécurisée pour la communication serveur/application.  Les travailleurs de service et autres technologies PWA fonctionnent uniquement avec les ressources Web fournies par le biais d’une connexion sécurisée (ou à partir `localhost` de à des fins de débogage \).  
  
*   [X] [travailleurs de service][MDNServiceWorkerApi].  Les threads de travail de service permettent de faire office de proxy réseau entre votre serveur et votre application cliente afin de fournir une prise en charge hors connexion, une mise en cache de ressources, des notifications de transmission, une synchronisation en arrière-plan  

*   [X] [manifeste de l’application Web][MDNWebAppManifest].  Fournissez un fichier de métadonnées JSON décrivant les informations clés relatives à votre application Web (par exemple, les icônes, le langage et le point d’entrée d’URL \) de sorte que Windows 10 et les autres plateformes hôtes puissent fournir à vos utilisateurs de Project Web App une interface de type autonome et installable.  L’Association de votre site à un manifeste de l’application Web le rend éligible pour [l’inclusion automatique dans le Microsoft Store][PwaEdgehtmlMicrosoftStoreImportingBing] par le biais du service d’indexation Bing.  

Pour être un parfait de PWA, votre application a également besoin des éléments suivants:  

*   [X] [compatibilité entre les navigateurs][MDNCrossBrowserTesting].  Assurez-vous que le contrôle PWA fonctionne en effectuant des [tests][MicrosoftDeveloperEdgeToolsRemote] dans différents navigateurs et environnements.  Sur Windows 10, veillez à tester votre application à la fois dans le navigateur Microsoft Edge et dans l’intégralité de l’interface de Project Web App (par le biais du moteur EdgeHTML \).  
  
*   [X] [conception réactive][WikiResponsiveWebDesign].  Utilisez des dispositions fluides et des images flexibles grâce à des [grilles][MDNCssGridLayout] CSS et/ou [Flexbox][MDNCssFlexibleBoxLayout], des [requêtes multimédias][MDNMediaQueries]et des [images réactives[MDNResponsiveImages] pour adapter votre expérience utilisateur à l’appareil de l’utilisateur.  Utilisez les [Outils d’émulation][DevToolsGuide|::ref1::|] d’appareil de votre navigateur pour effectuer des tests en local, ou configurez une [session de débogage à distance][DevToolsProtocolClientsEdgeDevToolsPreview] pour tester directement sur un appareil cible.  Sur Windows 10, PWAs \ (EdgeHTML \) peuvent également être [personnalisés pour des facteurs de forme][WindowsUWPDesignDevicesIndex] allant au-delà de la version de bureau, des téléphones et des tablettes, notamment: [Xbox et TV][WindowsUWPDesignDevicesDesigningTv], [surface Hub][MicrosoftDeveloperWindowsSurfaceHub]et appareils [Windows mixtes][MicrosoftDeveloperWindowsMixedReality] .  
  
*   [X] [liens en profondeur][WikiDeepLinking].  Acheminez chaque page de votre site vers une URL unique de sorte que les utilisateurs existants puissent vous aider à renforcer un public encore plus large grâce au partage de réseaux sociaux.  

*   [X] [meilleures pratiques][Webhint].  Utilisez les outils de qualité de code comme le [webhint][Webhint] de type Lint pour optimiser l’efficacité, la robustesse, la sécurité et l’accessibilité de votre application.  

Pour transmettre votre application Web progressive au [Microsoft Store][MicrosoftDeveloperStore], vous devez disposer des éléments suivants:  

*   [X] [compte de développeur Microsoft][WindowsUWPPublishDeveloperAccount]  
*   [X] étapes achevées [pour la publication d’une application Windows][WindowsUWPPublishIndex]  

Dans les mois à la réunion, les [critères spécifiques][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] de la réunion Web sont indexés automatiquement par le moteur de recherche Bing dans le Microsoft Store \ (où les développeurs sont en mesure de les gérer directement pour leur public Windows 10).  

Pour plus d’informations, consultez [PWAS (EdgeHTML) sur le Microsoft Store][PwaEdgehtmlMicrosoftStore] .  

## Disponibilité actuelle  

Prise en charge du moteur de navigateur pour les appels disgressifs vers des applications Web pour un certain nombre de composants architecturaux, l’infrastructure réseau la plus importante sous-jacente de l' [API FETCH][MDNFetchApi].  La prise en charge de Project Web App dans le moteur EdgeHTML a été effectuée dans Windows 10 1809 version.  D’autres améliorations apportées aux normes Web étant donné que cette durée ne sera pas incorporée au moteur EdgeHTML, n’oubliez pas d’exécuter des tests de compatibilité et d’utiliser la détection de fonctionnalités pour une utilisation harmonieuse pour la fonctionnalité non prise en charge dans la plateforme EdgeHTML.  

Pour la version à venir de Microsoft Edge \ (chrome \) dans 2020, la plateforme de navigateur prend entièrement en charge les fonctionnalités qui fonctionnent sur tous les appareils dans lesquels le navigateur de chrome est pris en charge.  

Pour EdgeHTML et Windows, voici l’état actuel des technologies Project Web App:  

| Technologie | Objectif | Disponibilité | Notes d’utilisation |  
|:--- |:--- |:--- |:--- |  
| [Manifeste de l’application Web][MDNWebAppManifest] | Fournit des métadonnées d’application au système d’exploitation hôte pour permettre la promotion d’installation et de magasin d’applications.  Requis pour PWAs dans le Microsoft Store.  | [En cours de développement][MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest] | Pour le moment, vous pouvez utiliser le [Générateur PWA][|::ref2::|] pour générer un manifeste JSON conforme au W3C et empaqueter votre application sur différentes plateformes de système d’exploitation.  Pour Windows, le concepteur PWA traduit votre manifeste JSON au `.appxmanifest` format \ (XML \) requis par les applications Windows 10.  |  
| [API Fetch][MDNFetchApi] | Fournit un réseau asynchrone \ (demandes, réponses \) pour les ressources de page |[EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /Build 14393 + | La syntaxe de l' [API de service Worker][MDNServiceWorkerApi] est basée sur les API de réseau Fetch.  Vous pouvez également utiliser l' [API FETCH][MDNFetchApi] plus généralement en guise d’alternative moderne `XMLHttpRequest` .  |  
| [API du travailleur de service][MDNServiceWorkerApi] | Fournit un proxy réseau ou un modèle d’application Web compatible hors connexion, où les scripts basés sur les événements s’exécutent indépendamment des pages Web  | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Support expérimental (en-dessous `Enable Service Workers` \) fourni dans EdgeHTML 16.  Activée par défaut dans EdgeHTML 17 + builds.  |  
| [API du cache][MDNCache] | Fournit un mécanisme de stockage pour les paires requête/réponse réseau | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Voir la note [API du travailleur de service][MDNServiceWorkerApi] ci-dessus.  |  
| [API de type pousser][MDNPushApi] | Permet à un travailleur de service de s’abonner à des notifications de transmission |[EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 +| Voir la note [API du travailleur de service][MDNServiceWorkerApi] ci-dessus.  Les applications Windows 10 \ (y compris PWAs) nécessitent le [service de notifications de transmission Windows (WNS \)][WindowsUWPControlsPatternTilesNotificationsWns] pour transmettre des notifications de transmission, qui prend en charge l' [API Poussée][MDNPushApi]du W3C.  |  
| [API notifications][MDNNotificationsApi] | Permet à un ouvrier de services d’afficher une notification système à l’utilisateur sur un message envoyé. | [EdgeHTML 14 +][DevGuideWhatsNewEdgeHtml14] /Build 14393 + | Les notifications Web dans EdgeHTML sont entièrement intégrées au [Centre de maintenance][MicrosoftSupportWindowsNotificationSettings]Windows 10, où les utilisateurs sont en mesure de gérer les notifications d’application et de définir des [heures de silence][MicrosoftSupportWindowsFocusAssist].  |  
| [API de synchronisation en arrière-plan][MDNSyncManager] | Fournit une API permettant d’avertir le travailleur d’un service que l’utilisateur a reconnecté et de planifier des événements périodiques pour synchroniser les données locales avec le serveur | [En cours de développement][MicrosoftDeveloperEdgePlatformStatusBackgroundSync] | Pour le moment, vous pouvez utiliser l' [API WinRT BackgroundTask][WindowsUWPLaunchResumeBackgroundTasks] native pour implémenter des tâches en arrière-plan pour votre PWA lorsque celle-ci s’exécute en tant qu’application Windows 10.  |  

Voici l’état actuel de la prise en charge du Microsoft Store pour PWAs sur Windows 10:  

| Méthode de soumission du Windows Store | Statut | Détails |  
|:--- |:--- |:--- |  
| Manuel \ (initié par le développeur \) | Disponible | Consultez [PWAS (EdgeHTML) dans la boutique Microsoft][PwaEdgehtmlMicrosoftStore] pour commencer.  |  
| Automatique \ (indexation automatique avec Bing \) | Bientôt disponible | Pour le [moment, nous piloterons][WindowsBlogsWelcomingPWAsEdgeWindows] le processus d’intégration de Project Web App avec un sous-ensemble limité de partenaires d’applications.  Dans les prochains mois, Microsoft se PWAs sur le Web standard pour le Microsoft Store.  Voir [importation automatique de Project Web App avec Bing][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] pour en savoir plus sur les conditions requises du Microsoft Store pour les annonces de Project Web App.  |  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Clients du protocole Microsoft Edge DevTools Preview-DevTools"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Émulation"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Nouveautés de EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Nouveautés de EdgeHTML 14"  
[PwaChromiumIndex]: ../progressive-web-apps-chromium/index.md "Applications Web progressives (chrome) sur Windows"  
[PwaEdgehtmlGetStarted]: ../progressive-web-apps-edgehtml/get-started.md "Découvrir les applications Web progressives (EdgeHTML)"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Applications Web progressives dans la boutique Microsoft"
[PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Critères pour la soumission automatique: applications Web progressives dans le Microsoft Store"  
[PwaEdgehtmlMicrosoftStoreImportingBing]: microsoft-store.md#automatic-pwa-importing-with-bing "Importation automatique de Project Web App avec Bing-progressivement Web Apps (EdgeHTML) dans la boutique Microsoft"  


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
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "Images réactives MDNResponsiveImages | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API du travailleur de service | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Manifeste de l’application Web | MDN"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Webhint]: https://webhint.io "Astuce"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Liaison Poussée-Wikipédia"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPs-Wikipédia"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Conception de site Web réactif-Wikipédia"  
