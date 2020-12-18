---
description: Cette page fournit une documentation sur la fonctionnalité de protection contre le suivi de Microsoft Edge (chrome)
title: Protection contre le suivi dans Microsoft Edge (chrome)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilité, plateforme Web, prévention du suivi, suivis, cookies, stockage, blocage de publicités, blocage du suivi, protection contre le suivi
ms.openlocfilehash: a767e55a44c4d416b6d40ca12eb49f2c3a722010
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11231149"
---
# Protection contre le suivi dans Microsoft Edge (chrome)  

La fonctionnalité de protection contre le suivi de Microsoft Edge protège les utilisateurs du suivi en ligne en restreignant la capacité des assureurs à accéder au stockage via le navigateur et au réseau.  Il repose sur le respect de la [politique de confidentialité du navigateur][MicrosoftEdgeBrowserPrivacyPromise] Microsoft Edge, tout en veillant à ce qu’il n’y ait aucun impact par défaut sur le site Web ou la viabilité économique du Web.  

Microsoft Edge offre actuellement aux utilisateurs trois niveaux de protection contre le suivi, qui sont sélectionnés en naviguant vers `edge://settings/privacy` .  

![Trois paramètres de prévention du suivi][ImageThreeSettingsTrackingPrevention]  

1.  **Basique** : niveau de protection le moins restrictif qui est conçu pour les utilisateurs qui apprécieront des publicités personnalisées et qui ne sont pas suivies sur le Web.  Basique protège uniquement les utilisateurs contre les suivis malveillants tels que les empreintes digitales et la cryptominers.  
1.  **Équilibré (par défaut)** -niveau de suivi par défaut conçu pour les utilisateurs qui souhaitent afficher moins de publications sur le Web lors de leur navigation.  Équilibré a pour but de bloquer les suivis des sites que les utilisateurs ne peuvent pas utiliser tout en minimisant le risque de problèmes de compatibilité sur le Web.  
1.  **** Le niveau de prévention du suivi le plus restrictif est limité aux utilisateurs qui ont la même compatibilité avec le site Web pour une confidentialité optimale.  

La fonctionnalité de protection contre le suivi de Microsoft Edge est composée de trois composants principaux qui travaillent ensemble pour déterminer si une ressource spécifique d’un site Web doit être classée comme suivi et bloquée.  Les composants sont les suivants:  

1.  **Classification** : la façon dont Microsoft Edge détermine si une URL appartient à un suivi.  
1.  **Application** : actions prises pour protéger les utilisateurs de Microsoft Edge des URL classées comme suivis.  
1.  **Réductions** -les mécanismes fournis pour garantir le bon fonctionnement des sites préférés définis par l’utilisateur, tout en offrant une protection renforcée par défaut.  

Chacun des composants est exploré et expliqué en détail dans cette page.  

## Classification  

Le premier composant de la fonctionnalité de protection contre le suivi de Microsoft Edge est la classification.  Pour classer des traceurs en ligne et les regrouper dans des catégories, Microsoft Edge [utilise les][|::ref1::|Main] [listes de protection contre le suivi][GitHubDisconnectMeTrackingProtection]d’ouverture de code source ouvertes.  Les listes sont transmises via le composant «listes de protection d’approbation», qui est visible à l’adresse `edge://components` .  Après avoir été téléchargées, les listes sont stockées sur un disque où vous pouvez les utiliser pour déterminer si une URL particulière est classée.  

Pour déterminer si une URL est considérée comme un suivi par le système de classification dans Microsoft Edge, une série de noms d’hôtes est vérifiée, en commençant par une correspondance exacte et en continuant de rechercher les correspondances partielles pour quatre étiquettes au-delà du domaine de niveau supérieur.  

> **Exemple**:  
> 
> URL `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Noms d’hôtes testés:  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Si l’un de ces noms d’hôtes correspond à un nom d’hôte dans les [listes][GitHubDisconnectMeTrackingProtection]de [déconnexion][|::ref2::|Main] , Microsoft Edge s’exécute en évaluant les actions d’application pour empêcher le suivi des utilisateurs.  

## Mise en œuvre  

Pour vous assurer de la protection contre le suivi des actions sur le Web, Microsoft Edge prend deux mesures d’exécution contre les contrôleurs classés:

*   **Restreindre l’accès au stockage** : si une ressource de suivi connue tente d’accéder à un espace de stockage Web où il est possible de faire persister les données relatives à l’utilisateur, Microsoft Edge empêche cet accès.  Cela inclut la possibilité de limiter la capacité à ce suivi d’obtenir ou de définir des cookies ainsi que des API de stockage Access telles que `IndexedDB` et `localStorage` .  
*   **Bloquer les chargements de ressources** : si une ressource de suivi connue est en cours de chargement sur un site Web, Microsoft Edge peut bloquer ce chargement avant que la demande n’atteigne le réseau en fonction de l’impact de la mise à niveau du chargement et du paramètre de protection de suivi défini par l’utilisateur.  Les chargements bloqués peuvent inclure les scripts de suivi, les pixels, les iframes, etc.  Cela empêche toute transmission de données au domaine de suivi et peut même améliorer les temps de chargement et les performances des pages en tant qu’effet secondaire.  

Un utilisateur risque de cliquer sur l’icône du menu volant infos page située sur le côté gauche de la barre d’adresse pour savoir quels suivis ont été bloqués sur une page spécifique: 

![Suivis bloqués dans le menu volant infos page][ImageBlockedTrackersPageInfoFlyout]  

Le mode d’application appliqué dépend du niveau de prévention de suivi choisi par l’utilisateur et des réductions qui peuvent s’appliquer.  

## Solutions de contournement  

Pour vous assurer que la compatibilité Web est conservée le plus possible, Microsoft Edge a trois atténuations pour vous aider à équilibrer les mesures dans des situations spécifiques.  Il s’agit de l’atténuation de la [relation d’organisation](#org-relationship-mitigation), de l’atténuation de l’engagement de l' [organisation](#org-engagement-mitigation)et de la [liste CompatExceptions](#the-compatexceptions-list).  

Avant de vous plonger dans les atténuations, il est préférable de définir le concept d’une «organisation» ou d’une «organisation» pour court.  La [fonction de][GitHubDisconnectMeTrackingProtectionEntitiesJson] [déconnexion][|::ref3::|Main] gère également une liste appeléeentities.jsqui définit des groupes d’URL appartenant à la même organisation ou société parente.  La fonctionnalité de protection contre le suivi de Microsoft Edge utilise cette liste à la fois dans l’atténuation de la [relation d’organisation](#org-relationship-mitigation) et dans le cadre de l’intervention de l' [organisation](#org-engagement-mitigation) pour limiter l’apparition de problèmes de compatibilité liés à une prévention affectant des demandes interentreprises.  

### Réduction de la relation d’organisation  

Plusieurs sites Web populaires permettent de gérer les sites Web et les réseaux de distribution de contenu (CDN \) pour fournir des ressources et du contenu statiques à ces sites.  Pour vous assurer que ces types de scénarios ne sont pas affectés par le suivi de la protection, Microsoft Edge exempte un site de la protection contre le suivi lorsque le site effectue des demandes tierces à d’autres sites appartenant à la même [entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson]organisation parente  C’est le meilleur illustré par un exemple.  

> **Exemple:**
> 
> Une organisation nommée Org1 possède les domaines `org1.test` et `org1-cdn.test` , comme indiqué dans la [liste déconnecter entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson].  Imaginez qu' `org1-cdn.test` il s’agit d’un suivi et que les mesures de prévention du suivi sont généralement appliquées.  Si un utilisateur effectue une visite `https://org1.test` et que le site essaie de charger une ressource `https://org1-cdn.test` , Microsoft Edge ne prend en charge aucune action de mise en application contre les demandes effectuées `org1-cdn.test` , même s’il ne s’agit pas d’une URL d’une première partie.  Toutefois, si une autre URL qui ne fait pas partie de l’organisation Org1 tente de charger cette même ressource, cette dernière fera l’objet de mises en œuvre, car elle ne fait pas partie de la même organisation.  
> 
> Même si cela assouplit le suivi des mesures de prévention des sites qui appartiennent à la même organisation, il est peu probable que cela entraîne une forte probabilité de confidentialité dans la mesure où ces organisations sont en mesure de déterminer les sites ou ressources auxquels vous avez accédé à partir de `https://org1.test` `https://org1-cdn.test` données principales internes.  

### Réduction des engagements de l’Organisation  

L’atténuation de l’engagement de l’organisation a été créée pour réduire les risques de compatibilité introduits par le suivi de la prévention en s’assurant que les sites appartenant à des organisations dont les utilisateurs s’engagent à fonctionner comme prévu sur le Web.  Ce service utilise l' [engagement de site][ChromiumDesignDocsSiteEngagement] pour assouplir les vigueur dès qu’un utilisateur a établi une relation en cours (actuellement définie par un score d’engagement de 4,1 ou plus) sur un site donné.  C’est le meilleur illustré par un exemple:

> **Exemple:**
> 
> Le nom d’une organisation est propriétaire de Domains `social.example` et `social-videos.example` .
> 
> Les utilisateurs sont considérés comme ayant une relation avec l’organisation sociale s’ils ont établi un score d’engagement de site de 4,1 ou supérieur avec l’un des domaines qu’ils possèdent.
> 
> S’il s’agit d’un autre site, `https://content-embedder.example` le contenu d’un site tiers (par exemple, une vidéo incorporée à partir de `social-videos.example` \) n’est pas accessible à partir de l’un des domaines qu’il possède en principe par le biais du suivi des engagements de prévention du suivi, le site est exempt du suivi des engagements de prévention du suivi.
> 
> Si un site n’est pas membre d’une organisation, un utilisateur doit établir un score d’engagement de site de 4,1 ou une version ultérieure avant tout bloc d’accès ou de charge de ressources de stockage imposé par la prévention de suivi.

Pour l’instant, l’atténuation de l’engagement est appliquée uniquement en mode équilibré, de sorte que Microsoft Edge offre les meilleures protections possibles pour les utilisateurs qui ont opté pour une application stricte.

### La liste CompatExceptions  

Sur la base des commentaires des utilisateurs récents reçus par Microsoft Edge, Microsoft Edge conserve une petite liste de sites (la plupart des sites dans la catégorie de contenu de déconnexion) qui étaient interrompus suite à une protection contre le suivi, malgré les deux mesures de prévention prédéfinies en vigueur. Les sites figurant dans cette liste sont exemptés de suivi des mesures de prévention.  La liste est disponible sur le disque aux [emplacements](#determining-whetherhow-a-particular-url-is-classified) décrits ci-dessous.  Les utilisateurs peuvent remplacer les entrées qui s’y trouvent à l’aide de l’option **bloquer** dans `edge://settings/content/cookies` .

Pour éviter que cette liste ne bouge, Microsoft travaille actuellement sur l’API d' [accès au stockage][GitHubMsExplainersStorageAccessApi] du code base de chrome.  L' [API d’accès au stockage][GitHubMsExplainersStorageAccessApi] permet aux développeurs de sites de demander directement l’accès au stockage aux utilisateurs et d’offrir aux utilisateurs une plus grande transparence quant à la façon dont leurs paramètres de vie privée influent sur leur interface de navigation et leur permettant d’offrir des contrôles de développement rapide et intuitif.

Une fois l' [API d’accès au stockage][GitHubMsExplainersStorageAccessApi] mise en œuvre, Microsoft dépréciera la liste CompatExceptions et communiquera aux sites concernés pour les informer des problèmes et demander à l’utilisateur d’utiliser l' [API de stockage][GitHubMsExplainersStorageAccessApi] en déplacement vers l’avant.  

## Comportement de prévention du suivi actuel  

Le tableau suivant répertorie les actions d’application et les atténuations appliquées à chaque catégorie de suivi classé dans Microsoft Edge.  

*   Dans la partie supérieure se trouvent les catégories de suivis définies par les [catégories de liste de protection de suivi de déconnexion][GitHubDisconnectTrackingProtectionCategories].  
*   Le côté gauche présente les trois niveaux de prévention du suivi dans Microsoft Edge \ (standard, équilibré et strict \).  
*   La lettre `S` indique que l’accès au stockage est bloqué.  
*   La lettre `B` indique que l’accès au stockage et les charges de ressources (par exemple, les requêtes réseau) sont bloqués.  
*   Un trait d’Union \ ( `-` \) indique qu’aucun bloc n’est appliqué à l’accès au stockage ou aux charges de ressources.  

| | Publicité | Analytique | Contenu | Cryptomining | Empreinte digitale | Social | Other | Même réduction d’organisation | Réduction des engagements de l’Organisation |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **De base** | - | - | - | B | B | - | - | Activé | Non applicable |  
| **Manquant** | S | - | S | B | B | S | S | Activée | Activée |  
| **Strict** | B | B | S | B | B | B | B | Activé | Désactivé |  

> [!NOTE]
> L’atténuation de l’engagement de l’organisation ne s’applique pas aux catégories d’empreintes Cryptomining ou d’empreintes digitales.  

> [!TIP]
> Le mode strict bloque davantage de charge de ressources qu’équilibrées.  Le blocage de plus de charge de ressources peuvent entraîner un mode strict qui semble bloquer moins de demandes de suivi que le fait d’être équilibré dans la mesure où les suivis de la demande ne seront jamais chargés.  

> [!NOTE]
> La colonne d’empreinte digitale du [comportement de prévention du suivi actuel](#current-tracking-prevention-behavior) fait référence aux suivis figurant sur la liste d’empreintes digitales en plus d’une autre liste.  Les chenilles qui apparaissent uniquement sur la liste d’empreintes digitales sont considérées comme des empreintes digitales non malveillantes et ne sont pas bloquées.

### Comportement InPrivate  

Dans Microsoft Edge 79, le comportement par défaut consiste à appliquer des protections en mode strict dans le cadre de l’InPrivate.  Dans Microsoft Edge 80, ce comportement a été remplacé par un commutateur permettant `edge://settings/privacy` aux utilisateurs de décider s’il convient d’appliquer des protections en mode strict ou de conserver leurs paramètres normaux lors de la navigation InPrivate.  

## Déterminer si une URL particulière est classée ou non  

Le moyen le plus simple de déterminer s’il s’agit d’une URL spécifique comme un suivi connu consiste à effectuer les étapes suivantes.  

1.  Ouvrez DevTools et accédez à l’onglet de la console.  
1.  Rechargez la page.  
    1.  Il est possible que vous souhaitiez effacer **les cookies et autres données de site** d’abord pour rétablir les scores d’engagement de site et garantir une ardoise entièrement claire.  
1.  Recherchez les messages lus `Tracking Prevention blocked access to storage for <URL>` .  
    1.  Vous pouvez développer les messages pour afficher les URL individuelles bloquées.  
1.  Si vous avez besoin d’identifier la catégorie dans laquelle se trouve un site bloqué spécifique, le moyen le plus simple est de le Rechercher dans la [liste déconnecter services.js][GitHubDisconnectTrackingProtectionCategories].  Les entrées sont classées par ordre alphabétique, de sorte que le défilement en haut d’un bloc d’entrées de site permet de rechercher la catégorie spécifique d’un site particulier.  

> [!TIP]
> Si vous avez besoin d’accéder aux listes de prévention du suivi stockées sur le disque, chacune d’elles se trouve dans l’un des deux emplacements suivantes.  
>
> **Mises à jour basées sur les composants** -listes téléchargées à partir du composant «listes de protection d’approbation»  
>
> Windows `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> MacOS `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Répertoire d’installation** : listes qui sont regroupées avec le programme d’installation de Microsoft Edge.  Si vous avez sélectionné un autre répertoire d’installation, vos chemins d’accès exacts sont différents.  
>
> Windows `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> MacOS `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## Forum Aux Questions  

La section suivante contient des réponses aux questions fréquemment posées sur la fonctionnalité de prévention du suivi dans Microsoft Edge.  

**Est-il possible de bloquer ou d’autoriser des assureurs spécifiques à des fins de débogage?**  

Pour le moment, Microsoft Edge n’expose qu’une option permettant de désactiver l’exécution des mesures de prévention du suivi sur un site spécifié.  Cette option est accessible via le menu volant infos page ou par le biais de la `edge://settings/privacy/trackingPreventionExceptions` page.  

Comme nous l’avons dit, il est possible d’utiliser les options **bloquer** et **autoriser** sur la `edge://settings/content/cookies` page pour autoriser ou refuser l’accès d’un domaine spécifique au stockage tel que les cookies et d’autres mécanismes de stockage du navigateur.  Cette fonctionnalité est utile pour le débogage des problèmes de site causés par le suivi des mesures de prévention et l’accès au stockage pour un site spécifique.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Vie privée-Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Engagement de site-projets de chrome"  

[DisconnectMain]: https://disconnect.me "Se"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/Disconnect-Track-protection | GitHub"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.jssur-disconnectme/le suivi de la déconnexion-protection | GitHub"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.jssur-disconnectme/le suivi de la déconnexion-protection | GitHub"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Explainst Storage API-MSEdgeExplainers/StorageAccessAPI | GitHub"
