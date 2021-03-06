---
description: Cette page fournit de la documentation sur la fonctionnalité de prévention du suivi Microsoft Edge (Chromium)
title: Prévention du suivi dans Microsoft Edge (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/07/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, compatibilité, plateforme web, prévention du suivi, suivis, cookies, stockage, blocage des publicités, blocage de suivi, protection contre le suivi
ms.openlocfilehash: 66356ab7ddaa56e46e74560d72b510ba63f7d70a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399287"
---
# <a name="tracking-prevention-in-microsoft-edge-chromium"></a>Prévention du suivi dans Microsoft Edge (Chromium)  

La fonctionnalité de prévention du suivi dans Microsoft Edge protège les utilisateurs contre le suivi en ligne en limitant la possibilité pour les suivis d’accéder au stockage basé sur le navigateur ainsi qu’au réseau.  Il est conçu pour respecter la promesse de confidentialité du navigateur Microsoft [Edge,][MicrosoftEdgeBrowserPrivacyPromise] tout en garantissant l’absence d’impact par défaut sur la compatibilité des sites web ou la politique économique du web.  

Microsoft Edge offre actuellement aux utilisateurs trois niveaux de prévention du suivi, qui sont sélectionnés en naviguant vers `edge://settings/privacy` .  

![Trois paramètres de prévention du suivi][ImageThreeSettingsTrackingPrevention]  

1.  **De base** : niveau de prévention de suivi le moins restrictif conçu pour les utilisateurs qui aiment des publicités personnalisées et qui ne veulent pas être suivis sur le web.  De base, seuls les utilisateurs sont protégés contre les suivis malveillants tels que les empreintes digitales et les cryptomonnaies.  
1.  **Équilibré (par défaut)** : niveau par défaut de prévention du suivi conçu pour les utilisateurs qui souhaitent voir des publicités moins publicitaires qui les suivent sur le web pendant qu’ils naviguent.  Balanced vise à bloquer les suivis des sites avec qui les utilisateurs ne s’engagent jamais tout en réduisant le risque de problèmes de compatibilité sur le web.  
1.  **Strict** : niveau le plus restrictif de prévention du suivi conçu pour les utilisateurs qui sont compatibles avec le site web de commerce pour une confidentialité maximale.  

La fonctionnalité de prévention du suivi dans Microsoft Edge est composé de trois composants principaux qui fonctionnent ensemble pour déterminer si une ressource spécifique d’un site web doit être classée comme suivi et bloquée.  Les composants sont les suivants :  

1.  **Classification** : la façon dont Microsoft Edge détermine si une URL appartient à un suivi.  
1.  **Application :** mesures prises pour protéger les utilisateurs de Microsoft Edge contre les URL classées en tant que suivis.  
1.  **Atténuations** : mécanismes fournis pour garantir que les sites favoris spécifiés par l’utilisateur fonctionnent toujours, tout en offrant une protection par défaut forte.  

Chacun des composants est explorez et expliqué en détail sur cette page.  

## <a name="classification"></a>Classification  

Le premier composant de la fonctionnalité de prévention du suivi dans Microsoft Edge est la classification.  Pour classer les suivis en ligne et les regrouper en catégories, Microsoft Edge utilise les listes de [protection][GitHubDisconnectMeTrackingProtection]Déconnecter [][|::ref1::|Main] le suivi open source.  Les listes sont remis via le composant « Listes de protection de la confiance », qui est consultable sur `edge://components` .  Une fois téléchargées, les listes sont stockées sur le disque où vous pouvez les utiliser pour déterminer si/comment une URL particulière est classée.  

Pour déterminer si une URL est considérée comme un suivi par le système de classification dans Microsoft Edge, une série de noms d’hôtes est vérifiée, en commençant par une correspondance exacte, puis en vérifiant les correspondances partielles pour jusqu’à quatre étiquettes au-delà du domaine de niveau supérieur.  

> **Exemple**:  
> 
> URL : `https://a.subdomain.of.a.known.tracker.test/some/path`  
> 
> Noms d’hôte testés :  
> 
> *   `a.subdomain.of.a.known.tracker.test`  
> *   `of.a.known.tracker.test`  
> *   `a.known.tracker.test`  
> *   `known.tracker.test`  
> *   `tracker.test`  

Si l’un de ces noms d’hôte correspond à un nom d’hôte dans les listes de déconnexion, Microsoft Edge procède à l’évaluation des actions d’application afin d’empêcher le suivi des utilisateurs. [][|::ref2::|Main] [][GitHubDisconnectMeTrackingProtection]  

## <a name="enforcement"></a>Mise en œuvre  

Pour assurer une protection contre les actions de suivi sur le web, Microsoft Edge prend deux actions d’application contre les suivis classifiés :

*   **Restreindre l’accès** au stockage : si une ressource de suivi connue tente d’accéder à un stockage web dans lequel elle peut tenter de faire persister des données sur l’utilisateur, Microsoft Edge bloque cet accès.  Cela inclut la restriction de la possibilité pour ce suivi d’obtenir ou de définir des cookies, ainsi que d’accéder aux API de stockage telles que `IndexedDB` et `localStorage` .  
*   **** Bloquer les chargements de ressources : si une ressource de suivi connue est chargée sur un site web, Microsoft Edge peut bloquer cette charge avant que la demande n’atteigne le réseau en fonction de l’impact de la charge et du paramètre de prévention du suivi qu’un utilisateur a définie.  Les chargements bloqués peuvent inclure des scripts de suivi, des pixels, des iframes, etc.  Cela empêche toute donnée potentiellement envoyée au domaine de suivi et peut même améliorer les temps de chargement et les performances de page en tant qu’effet secondaire.  

Un utilisateur peut choisir l’icône du volant d’informations de la page sur le côté gauche de la barre d’adresses pour savoir quels suivis ont été bloqués sur une page spécifique : 

![Suivis bloqués dans le volant d’informations de la page][ImageBlockedTrackersPageInfoFlyout]  

La façon dont les mesures d’application sont appliquées dépend du niveau de prévention de suivi sélectionné par l’utilisateur et des atténuations qui peuvent s’appliquer.  

## <a name="mitigations"></a>Atténuations  

Pour garantir que la compatibilité web est conservée autant que possible, Microsoft Edge dispose de trois atténuations pour équilibrer les mesures d’application dans des situations spécifiques.  Voici l’atténuation [de la relation d’organisation](#org-relationship-mitigation), l’atténuation [Org Engagement](#org-engagement-mitigation)et la liste [compatExceptions](#the-compatexceptions-list).  

Avant de vous plonger dans les atténuations, il est intéressant de définir le concept d’une « organisation » ou d’une « organisation ».  [La][|::ref3::|Main] déconnexion conserve également une liste appelée [entities.jsqui][GitHubDisconnectMeTrackingProtectionEntitiesJson] définit des groupes d’URL qui sont propriétés de la même organisation/société parente.  La fonctionnalité de prévention du suivi dans [](#org-relationship-mitigation) Microsoft Edge utilise cette liste à la fois dans l’atténuation des relations d’organisation et dans l’atténuation [Org Engagement](#org-engagement-mitigation) pour minimiser l’occurrence des problèmes de compatibilité dus à la prévention du suivi affectant les demandes entre les organisations.  

### <a name="org-relationship-mitigation"></a>Atténuation des relations d’organisation  

Plusieurs sites web populaires conservent à la fois des sites web et des réseaux de distribution de contenu \(CDN\) pour servir des ressources et du contenu statiques à ces sites.  Pour s’assurer que ces types de scénarios ne sont pas affectés par la prévention du suivi, Microsoft Edge exempte un site de la prévention du suivi lorsque le site fait des demandes tierces à d’autres sites de la même organisation parente \(comme défini dans la [entities.js][GitHubDisconnectMeTrackingProtectionEntitiesJson]Déconnecter sur la liste \).  Il est préférable d’illustrer cela par un exemple.  

> **Exemple:**
> 
> Une organisation nommée Org1 possède les domaines et, comme défini dans la liste `org1.test` `org1-cdn.test` Disconnect entities.js[.][GitHubDisconnectMeTrackingProtectionEntitiesJson]  Imaginez qu’il soit classé en tant que suivi et que des mesures de prévention de suivi `org1-cdn.test` lui sont normalement appliquées.  Si un utilisateur visite et que le site tente de charger une ressource à partir de , Microsoft Edge ne prend aucune action d’application contre les demandes faites à même qu’il ne s’agisse pas d’une URL de première `https://org1.test` `https://org1-cdn.test` `org1-cdn.test` partie.  Toutefois, si une autre URL qui ne fait pas partie de l’organisation Org1 tente de charger cette même ressource, la demande est soumise à des mesures d’application, car elle ne fait pas partie de la même organisation.  
> 
> Bien que cela relâche les mesures de prévention pour les sites appartenant à la même organisation, il est peu probable que cela présente un risque élevé en matière de confidentialité, car ces organisations sont en mesure de déterminer les sites/ressources sur lesquels vous avez accédé ainsi à l’aide de données `https://org1.test` `https://org1-cdn.test` internes.  

### <a name="org-engagement-mitigation"></a>Atténuation de l’engagement de l’organisation  

L’atténuation de l’engagement de l’organisation a été créée pour minimiser les risques de compatibilité introduits par la prévention du suivi en veillant à ce que les sites dont les organisations avec qui les utilisateurs s’engagent suffisamment continuent de fonctionner comme prévu sur le web.  Il utilise [l’engagement][ChromiumDesignDocsSiteEngagement] de site pour relâcher les mesures d’application chaque fois qu’un utilisateur a établi une relation en cours \(actuellement définie par un score d’engagement de site de 4,1 ou supérieur\) avec un site donné.  Ceci est illustré à nouveau par un exemple :

> **Exemple:**
> 
> Une organisation nommée Social Org possède les domaines `social.example` et `social-videos.example` .
> 
> Les utilisateurs sont considérés comme ayant une relation avec l’organisation sociale s’ils ont établi un score d’engagement de site supérieur ou supérieur à 4,1 avec l’un des domaines de l’organisation sociale.
> 
> Si un autre site, inclut du contenu tiers \(par exemple, une vidéo incorporée à partir de \) à partir d’un des domaines de l’organisation sociale qui seraient normalement restreints par le suivi des mesures de prévention, le site n’est pas tenu de suivre les mesures de prévention tant que le score d’engagement du site de l’utilisateur avec des domaines de l’organisation sociale est maintenu `https://content-embedder.example` au-dessus du `social-videos.example` seuil.
> 
> Si un site n’appartient pas à une organisation, un utilisateur doit établir un score d’engagement de site de 4,1 ou plus avec lui directement avant que les blocs d’accès au stockage/charge de ressources imposées par la prévention du suivi ne soient relâchés.

L’atténuation de l’engagement de l’organisation est actuellement appliquée uniquement en mode équilibré afin que Microsoft Edge offre les protections les plus élevées possibles pour les utilisateurs qui ont choisi strict.

### <a name="the-compatexceptions-list"></a>Liste CompatExceptions  

En fonction des commentaires des utilisateurs récents reçus par Microsoft, Microsoft Edge conserve une petite liste de sites \(dont la plupart font partie de la catégorie Déconnexion du contenu\) qui ont été rompus en raison de la prévention du suivi, bien que les deux préventions ci-dessus soient en place. Les sites de cette liste ne sont pas exempts des mesures de prévention du suivi.  La liste se trouve sur le disque aux [emplacements décrits](#determining-whetherhow-a-particular-url-is-classified) ci-dessous.  Les utilisateurs peuvent remplacer les entrées qui y sont entrées à l’aide de **l’option** Bloquer dans `edge://settings/content/cookies` .

Pour éviter de conserver cette liste, Microsoft travaille actuellement sur [l’API d’accès][GitHubMsExplainersStorageAccessApi] au stockage dans la base de code Chromium.  [L’API d’accès][GitHubMsExplainersStorageAccessApi] au stockage permet aux développeurs de sites de demander directement l’accès au stockage aux utilisateurs, en fournissant aux utilisateurs plus de transparence sur la façon dont leurs paramètres de confidentialité affectent leur expérience de navigation et en offrant aux développeurs de sites des contrôles pour se débloquer rapidement et de manière intuitive.

Une fois [l’API][GitHubMsExplainersStorageAccessApi] d’accès au stockage implémentée, Microsoft déprécie la liste CompatExceptions et atteint les sites concernés pour les rendre informés des problèmes et leur demander d’utiliser [l’API][GitHubMsExplainersStorageAccessApi] d’accès au stockage à l’avenir.  

## <a name="current-tracking-prevention-behavior"></a>Comportement actuel de prévention du suivi  

Le tableau suivant présente les actions d’application et les atténuations qui sont appliquées à chaque catégorie de suivi classifié dans Microsoft Edge.  

*   Les catégories de suivis définies par les catégories de liste de protection de suivi de déconnexion sont [répertoriées][GitHubDisconnectTrackingProtectionCategories]en haut.  
*   Le long du côté gauche se sont ajoutés les trois niveaux de prévention du suivi dans Microsoft Edge \(Basic, Balanced et Strict\).  
*   La lettre `S` indique que l’accès au stockage est bloqué.  
*   La lettre indique que l’accès au stockage et les charges de ressources \(telles que les `B` demandes réseau\) sont bloqués.  
*   Un tiret \( \) indique qu’aucun bloc n’est appliqué à l’accès au stockage ou `-` aux charges de ressources.  

| | Insélation | Analytique | Contenu | Cryptomining | Empreinte digitale | Social | Other | Prévention de la même organisation | Atténuation de l’engagement de l’organisation |  
| - | - | - | - | - | - | - | - | - | - | - |  
| **De base** | - | - | - | B | B | - | - | Activé | Non applicable |  
| **Équilibré** | S | - | S | B | B | S | S | Activée | Activée |  
| **Strict** | B | B | S | B | B | B | B | Activé | Désactivé |  

> [!NOTE]
> L’atténuation de l’engagement de l’organisation ne s’applique pas aux catégories Cryptomining ou Fingerprinting.  

> [!TIP]
> Le mode strict bloque plus de charges de ressources qu’Avec équilibrage.  Le blocage d’un plus grand nombre de charges de ressources peut entraîner le blocage d’un nombre inférieur de demandes de suivi par le mode Strict, car les suivis qui les font ne sont jamais chargés.  

> [!NOTE]
> La colonne Empreintes digitales dans le comportement [de](#current-tracking-prevention-behavior) prévention du suivi actuel fait référence aux suivis répertoriés dans la liste Fingerprinting en plus d’une autre liste.  Les suivis qui apparaissent uniquement sur la liste fingerprinting sont considérés comme des empreintes digitales non malveillantes et ne sont pas bloqués.

### <a name="inprivate-behavior"></a>Comportement InPrivate  

Dans Microsoft Edge 79, le comportement par défaut était d’appliquer des protections en mode strict dans InPrivate.  Dans Microsoft Edge 80, ce comportement a été remplacé par un commutateur qui permet aux utilisateurs de décider s’il faut appliquer des protections en mode strict ou conserver leurs paramètres habituels lors de la navigation `edge://settings/privacy` inPrivate.  

## <a name="determining-whetherhow-a-particular-url-is-classified"></a>Déterminer si/comment une URL particulière est classifiée  

Le moyen le plus simple de déterminer si une URL spécifique est classée en tant que suivi connu consiste à effectuer les étapes suivantes.  

1.  Ouvrez DevTools et accédez à l’onglet Console.  
1.  Actualisez la page web.  
    1.  Vous pouvez d’abord effacer les **cookies** et les autres données de site pour réinitialiser les scores d’engagement du site et garantir une tablette entièrement nettoyée.  
1.  Recherchez tous les messages `Tracking Prevention blocked access to storage for <URL>` lus.  
    1.  Vous pouvez développer les messages pour voir les URL individuelles qui ont été bloquées.  
1.  Si vous devez déterminer la catégorie dans laquelle se trouve un site bloqué spécifique, le moyen le plus simple de le faire consiste à le rechercher dans la liste Disconnect [services.js.][GitHubDisconnectTrackingProtectionCategories]  Les entrées sont alphabétisées, donc le défilement vers le haut d’un bloc d’entrées de site vous permet de trouver la catégorie spécifique d’un site particulier.  

> [!TIP]
> Si vous avez besoin d’accéder aux listes de prévention du suivi stockées sur le disque, chacune d’elles se trouve dans l’un des deux emplacements.  
>
> **Mises à jour basées** sur les composants : listes téléchargées à partir du composant « Listes de protection de la confiance »  
>
> Windows : `%LOCALAPPDATA%\Microsoft\Edge <OptionalChannelName>\User Data\Trust Protection Lists`  
>
> macOS : `~/Library/Application Support/Microsoft Edge <OptionalChannelName>/Trust Protection Lists`  
>
> **Répertoire d’installation** : listes regroupées avec le programme d’installation de Microsoft Edge.  Si vous avez sélectionné un répertoire d’installation différent, vos chemins d’accès exacts peuvent être différents.  
>
> Windows : `%PROGRAMFILES(x86)%\Microsoft\ Edge <OptionalChannelName>\Application<Version>\Trust Protection Lists`  
>
> macOS : `/Applications/Microsoft Edge.app/Contents/Frameworks/Microsoft Edge Framework.framework/Libraries/Trust Protection Lists`  

## <a name="frequently-asked-questions"></a>Forum Aux Questions  

La section suivante contient des réponses aux questions fréquemment posées sur la fonctionnalité de prévention du suivi dans Microsoft Edge.  

**Existe-t-il un moyen de bloquer ou d’autoriser des suivis spécifiques à des fins de débogage ?**  

Actuellement, Microsoft Edge n’offre qu’une option pour désactiver l’exécution des mesures de prévention du suivi sur un site spécifié.  Cette option est accessible via le flyout d’informations de la page ou via la `edge://settings/privacy/trackingPreventionExceptions` page.  

Cela étant dit, les **options** Bloquer et Autoriser sur la page peuvent être utilisées pour autoriser ou refuser l’accès à des domaines spécifiques au stockage, tels que les cookies et d’autres mécanismes de stockage de **** `edge://settings/content/cookies` navigateur.  Cela est utile pour le débogage des problèmes de site causés par le suivi des mesures de prévention qui bloquent l’accès au stockage pour un site spécifique.  

<!-- image links -->  

[ImageThreeSettingsTrackingPrevention]: ./media/tracking-prevention-settings.png  
[ImageBlockedTrackersPageInfoFlyout]: ./media/page-info-flyout.png  

<!-- links -->  

[MicrosoftEdgeBrowserPrivacyPromise]: https://microsoftedgewelcome.microsoft.com/privacy "Confidentialité - Microsoft Edge"  

[ChromiumDesignDocsSiteEngagement]: https://www.chromium.org/developers/design-documents/site-engagement "Engagement de site : projets Chromium"  

[DisconnectMain]: https://disconnect.me "Déconnexion"  

[GitHubDisconnectMeTrackingProtection]: https://github.com/disconnectme/disconnect-tracking-protection "disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectTrackingProtectionCategories]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/services.json "services.js- disconnectme/disconnect-tracking-protection | Github"  
[GitHubDisconnectMeTrackingProtectionEntitiesJson]: https://github.com/disconnectme/disconnect-tracking-protection/blob/master/entities.json "entities.js- disconnectme/disconnect-tracking-protection | Github"  

[GitHubMsExplainersStorageAccessApi]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/StorageAccessAPI/explainer.md "Explaineur de l’API d’accès au stockage - MSEdgeExplainers/StorageAccessAPI | GitHub"
