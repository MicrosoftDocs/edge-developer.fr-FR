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
ms.openlocfilehash: 47c6f98329a1da67e0f2c1a8e6243250992fb599
ms.sourcegitcommit: f4488cf2dfef0aeec04712b2ed933d68b8e93a94
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/17/2021
ms.locfileid: "11608841"
---
# <a name="progressive-web-apps-on-windows-overview"></a>Présentation progressive des applications web sur Windows  

[Les][MDNApps] applications web progressives \(PWAs\) permettent d’accéder aux technologies web ouvertes pour l’interopérabilité entre plateformes et offrent à vos utilisateurs une expérience native de l’application personnalisée pour leurs appareils. Les P PWA sont des sites web [qui][AListApartUnderstandingProgressiveEnhancement] sont progressivement améliorés pour fonctionner comme des applications natives sur les plateformes de prise en charge. Les qualités d’une PWA combinent le meilleur des applications web et natives.  

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
        ### <a name="discoverablemdnpwaadvantagesdiscoverable"></a>[Découvrable][MDNPwaAdvantagesDiscoverable]  
    :::column-end:::
    :::column:::
        ### <a name="installablemdnpwaadvantagesinstallable"></a>[Installable][MDNPwaAdvantagesInstallable]  
    :::column-end:::
    :::column:::
        ### <a name="re-engageablemdnpwaadvantagesreengageable"></a>[Réentrable][MDNPwaAdvantagesReEngageable]  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        À partir des résultats de recherche web et des magasins d’applications de prise en charge  
    :::column-end:::
    :::column:::
        Épingler et lancer à partir de l’écran d’accueil, du menu Démarrer, de la barre des tâches, et ainsi de suite  
    :::column-end:::
    :::column:::
        Envoyer des notifications Push, même lorsque l’application n’est pas active  
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
        ### <a name="network-independentmdnpwaadvantagesnetworkindependent"></a>[Indépendant du réseau][MDNPwaAdvantagesNetworkIndependent]  
    :::column-end:::
    :::column:::
        ### <a name="progressivemdnpwaadvantagesprogressive"></a>[Progressive][MDNPwaAdvantagesProgressive]  
    :::column-end:::
    :::column:::
        ### <a name="safemdnpwaadvantagessafe"></a>[Safe][MDNPwaAdvantagesSafe]  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        Fonctionne en mode hors connexion et dans des conditions de réseau faible  
    :::column-end:::
    :::column:::
        L’expérience est étendue (ou réduite) avec les fonctionnalités de l’appareil  
    :::column-end:::
    :::column:::
        Fournit un point de terminaison HTTPS sécurisé et d’autres protections utilisateur  
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
        ### <a name="responsivemdnpwaadvantagesresponsive"></a>[Réactivité][MDNPwaAdvantagesResponsive]  
    :::column-end:::
    :::column:::
        ### <a name="linkablemdnpwaadvantageslinkable"></a>[Linkable][MDNPwaAdvantagesLinkable]  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  
:::row:::
    :::column:::
        S’adapte à la taille de l’écran, à l’orientation et à la méthode d’entrée de l’utilisateur  
    :::column-end:::
    :::column:::
        Partager et lancer à partir d’un lien hypertexte standard  
    :::column-end:::
    :::column:::
        &nbsp;  
    :::column-end:::
:::row-end:::  

Créez \(ou convertissez\) votre site web existant en PWA pour améliorer l’engagement avec vos utilisateurs. Les améliorations incluent les notifications Push, l’intégration de l’application et la prise en charge hors connexion. Continuez à développer votre audience sur le web ouvert pour que les utilisateurs découvrent votre PWA par le biais de la recherche et du partage de liens. Mieux encore, votre application est mise à jour à l’aide du code de votre serveur web.  

## <a name="pwas-on-microsoft-edge-chromium"></a>P PWAs sur Microsoft Edge (Chromium)  

Lorsque vous créez une application web progressive ciblant des API web standard, votre application peut être déployée sur des plateformes et des appareils et tirer parti des fonctionnalités spécifiques de l’appareil, selon les besoins. Les P PWA dans Microsoft Edge \(Chromium\) ajoutent les avantages suivants à votre site web.  

*   Votre application repose sur une plateforme web basée sur des normes.  
*   Permet à vos utilisateurs d’installer votre application directement à partir du navigateur.  
*   Permet à vos utilisateurs d’installer votre application sans inscription ou déploiement basé sur le Store.  
    
Desktop PWAs are supported on any of the platforms Microsoft Edge \(Chromium\) is [available](https://www.microsoft.com/edge). Les avantages suivants sont inclus.

*   Les applications peuvent être installées directement à partir du navigateur à l’aide de l’icône **Installer** dans la barre de navigation.  
    
    :::image type="complex" source="./media/install-progressive-web-app-icon.png" alt-text="Installer le volant et l’icône de l’application" lightbox="./media/install-progressive-web-app-icon.png":::
       Installer le volant et l’icône de l’application  
    :::image-end:::  
    
*   Les applications peuvent également être installées, exécutés et gérées à partir du menu **Paramètres**  >  **des applications**  
    
    :::image type="complex" source="./media/app-menus.png" alt-text="Éléments de menu de l’application sous paramètres" lightbox="./media/app-menus.png":::
       Éléments de menu de l’application sous paramètres  
    :::image-end:::  
    
*   Les notifications web sont intégrées au système de notification Windows  
*   Magasin de cookies partagé avec le profil de navigateur qui a installé l’application  
*   Accès à d’autres fonctionnalités de navigateur à l’aide du menu Paramètre et plus **\(** \), y compris la validation de certificat, les autorisations de site, la protection de suivi et les `...` extensions de navigateur  
*   Accès total à [Microsoft Edge DevTools][DevtoolsProgressiveWebApps] pour le débogage de votre application  
    
> [!NOTE]
> Pour plus d’informations sur les avantages de PWA, les fonctionnalités à venir et les démonstrations courtes, accédez à la [session Build 2020 PWA.][BuildVideo] 

## <a name="requirements"></a>Conditions préalables  

Pour s’exécuter en tant que PWA, votre application web hébergée sur le serveur doit inclure les conditions minimales suivantes.  

:::row:::
   :::column span="1":::
      [HTTPS][WikiHttps]  
   :::column-end:::
   :::column span="2":::
      Protège vos utilisateurs en fournissant une connexion sécurisée pour la communication de serveur ou d’application.  Les travailleurs de service et les autres technologies PWA fonctionnent uniquement avec des ressources web servies sur une connexion sécurisée \(ou à partir d’une connexion à des fins `localhost` de débogage\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Worker du service][MDNServiceWorkerApi]  
   :::column-end:::
   :::column span="2":::
      Utilise des threads de travail de service pour agir en tant que proxys réseau entre votre serveur et votre application cliente.  Les threads de travail de service assurent la prise en charge hors connexion, la mise en cache des ressources, les notifications Push, la synchronisation des données en arrière-plan et les optimisations des performances de chargement de page.    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Manifeste de l’application web][MDNWebAppManifest]  
   :::column-end:::
   :::column span="2":::
      Fournit un fichier de métadonnées basé sur JSON qui décrit les informations clés sur votre application web, afin que Windows 10 et d’autres plateformes hôtes fournissent à vos utilisateurs PWA une expérience installable et native de l’application.  Les informations clés incluent les icônes, la langue et le point d’entrée d’URL. 
   :::column-end:::
:::row-end:::  

Pour être un excellent PWA, votre application doit également répondre aux exigences suivantes.  

:::row:::
   :::column span="1":::
      [Compatibilité entre navigateurs][MDNCrossBrowserTesting]  
   :::column-end:::
   :::column span="2":::
      Assurez-vous que votre PWA fonctionne [en testant][MicrosoftDeveloperEdgeToolsRemote] dans différents navigateurs et environnements.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Conception réactive][WikiResponsiveWebDesign]  
   :::column-end:::
   :::column span="2":::
      Utilise des dispositions fluides et des images flexibles.  La conception réactive inclut les éléments suivants qui adaptent votre expérience utilisateur à l’appareil de votre utilisateur.  
      
      *   Grille [CSS][MDNCssGridLayout]  
      *   [flexbox][MDNCssFlexibleBoxLayout]  
      *   Grille CSS [et][MDNCssGridLayout] [flexbox][MDNCssFlexibleBoxLayout]  
      *   [requêtes multimédias][MDNMediaQueries]  
      *   [images réactives][MDNResponsiveImages]  
          
      Utilise [les outils d’émulation][DevToolsGuideDeviceModeTestingOtherBrowsers] d’appareil de votre navigateur pour tester localement ou créer une session de débogage à distance sur [Windows][DevtoolsRemoteDebuggingWindows] ou [Android][DevtoolsRemoteDebuggingIndex] pour tester directement sur un appareil cible.
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Liaisons profondes][WikiDeepLinking]  
   :::column-end:::
   :::column span="2":::
      Approvisionnement de chaque page de votre site vers une URL unique afin que les utilisateurs existants vous aident à impliquer un public encore plus large via le partage de réseaux sociaux.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Pratiques de validation et de test][Webhint]  
   :::column-end:::
   :::column span="2":::
      Utilise des outils de qualité du code tels que [le linter Webhint][Webhint] pour optimiser l’efficacité, la robustesse, la sécurité et l’accessibilité de votre application.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Liste de contrôle PWA Chromium][WebDevGoodPwaChecklist]  
   :::column-end:::
   :::column span="2":::
      Vérifie votre PWA par rapport à la liste de vérification PWA de référence google.  
   :::column-end:::
:::row-end:::  

> [!NOTE]
> Pour transformer votre application PWA en [application du Microsoft Store,][MicrosoftDeveloperStore] accédez à [Progressive Web Apps dans le Microsoft Store.][PwaChromiumMicrosoftStore]  
  
## <a name="see-also"></a>Articles associés  

*   [#A0][Davrous20191018MythBustingPwasNewEdgeEdition]  
*   [Une feuille de route progressive pour votre application web progressive][CloudfourThinksProgressiveRoadmapYourWebApp]  
*   [Posts hors connexion avec applications web progressives][MediumWebEdgeOfflinePostsProgressiveWebApps]  
*   [PWA Q&A][AaronGustafsonNotebookPwaQa]  
*   [Se menter sur le Web][JoretegBlogBettingWeb]  
*   [Attribution de noms aux applications web progressives][Fberriman20170626NamingProgressiveWebApps]  
*   [Conception et création d’une application web progressive sans infrastructure (partie 1)][Smashingmagazine201907ProgressiveWebAppFrameworkPart1]  
*   [Conception et création d’une application web progressive sans infrastructure (partie 2)][Smashingmagazine201907ProgressiveWebAppFrameworkPart2]  
*   [Conception et création d’une application web progressive sans infrastructure (partie 3)][Smashingmagazine201907ProgressiveWebAppFrameworkPart3]  
    
<!-- links -->  

[DevtoolsRemoteDebuggingIndex]: ../devtools-guide-chromium/remote-debugging/index.md "Commencer à déboguer à distance les appareils Android | Documents Microsoft"  
[DevtoolsRemoteDebuggingWindows]: ../devtools-guide-chromium/remote-debugging/windows.md "Mise en place du débogage à distance des appareils Windows 10 | Documents Microsoft"  
[DevToolsGuideDeviceModeTestingOtherBrowsers]: ../devtools-guide-chromium/device-mode/testing-other-browsers.md "Émuler et tester d’autres navigateurs | Documents Microsoft"  
[DevtoolsProgressiveWebApps]: ../devtools-guide-chromium/progressive-web-apps/index.md "Déboguer les applications web progressives | Documents Microsoft"  
[PwaChromiumMicrosoftStore]: ./microsoft-store.md "Publier votre application web progressive sur le Microsoft Store | Documents Microsoft"

[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Vue d’ensemble de Windows Push Notification Services (WNS) | Documents Microsoft"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Conception pour xbox et télévision | Documents Microsoft"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Considérations sur l’interface utilisateur pour les appareils UWP | Documents Microsoft"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Qu’est-ce qu’une application de plateforme Windows universelle (UWP) ? | Documents Microsoft"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Prise en charge de votre application avec des tâches en arrière-plan | Documents Microsoft"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Publier des applications et des jeux Windows | Documents Microsoft"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Ouverture d’un compte de développeur | Documents Microsoft"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Mise en avant des applications web progressives dans Microsoft Edge et Windows 10 - Blogs Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API de synchronisation en arrière-plan - État de la plateforme Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebAppManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Manifeste d’application web - État de la plateforme Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Test instantané"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Réalité mixte pour les développeurs"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface Hub"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Microsoft Developer Store"  
[MicrosoftEdge]: https://www.microsoft.com/edge "Télécharger le nouveau navigateur Microsoft Edge"  
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

[BuildVideo]: https://www.youtube.com/watch?v=y4p_QHZtMKM "Vidéo PWA"  

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
