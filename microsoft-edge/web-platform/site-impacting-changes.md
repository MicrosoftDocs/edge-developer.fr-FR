---
description: Fournit un récapitulatif des changements à forte incidence qui pourraient affecter la compatibilité du site
title: Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/04/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, compatibilité, plateforme Web
ms.openlocfilehash: bb4d67bf1ab6274a10a83ee750fa9db52ab85464
ms.sourcegitcommit: 4497b399a6ddfa34163b7d3db4f76423d4da3c12
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/05/2020
ms.locfileid: "11156347"
---
# Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites  

Le web évolue constamment pour améliorer l’expérience utilisateur, la sécurité et la confidentialité.  Dans certains cas, les modifications apportées risquent d’avoir une incidence sur les fonctionnalités des pages existantes.  Le tableau suivant récapitule les changements particulièrement importants qui sont en cours de suivi par l’équipe Microsoft Edge.  Consultez régulièrement cet article. l’équipe Microsoft Edge met à jour la page suivante en apportant des réflexions, des chronologies et de nouvelles modifications.  

| Modification | Canal Stable | Expérimentation | Informations complémentaires |  
|:--- |:--- |:--- |:--- |
| Cookies par défaut `SameSite=Lax` `SameSite=None-requires-Secure` | [Chrome + 1](#release-comments) \ (Edge V86 \)  | V82 Canaries, dev V82 | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, accédez à l’entrée d’état de la [plateforme chrome][ChromePlatformStatus5088147346030592].  |  
| Stratégie de renvoi: par défaut `strict-origin-when-cross-origin` | [Chrome + 1](#release-comments) \ (Edge V86 \)  | V79 Canaries, dev V79 | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, accédez à l’entrée d’état de la [plateforme chrome][ChromePlatformStatus6251880185331712].  |  
| Désactiver la synchronisation synchrone `XmlHttpRequest` dans la page | [Chrome + 1](#release-comments) \ (Edge V83 \) |  | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  À la correspondance de chrome, Microsoft Edge propose une stratégie de groupe pour désactiver cette modification jusqu’au V88 Edge.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, accédez à l’entrée d’état de la [plateforme chrome][ChromePlatformStatus4664843055398912].  |  
| Afficher une invite discrète pour les demandes d’autorisation de notification | Bordure V84 |  | Les demandes de notification silencieuse affichent une icône de requête subtile dans la barre d’adresse pour les autorisations de notification de site demandées à l’aide de l' `Notifications` `Push` API ou, en remplaçant l’interface utilisateur d’invite de menu volant d’autorisation complète ou standard.  Cette fonctionnalité est actuellement activée pour tous les utilisateurs.  Pour refuser les demandes de notifications de silence, accédez à `edge://settings/content/notifications` .  À l’avenir, l’équipe Microsoft Edge risque de réactiver l’invite de notifications flyout complète dans certains cas.  |  
| Désactiver TLS/1.0 et TLS/1.1 par défaut | Bordure V84 |  | La stratégie de groupe [SSLMinVersion][DeployedEdgePoliciesSSLMinVersion] autorise la réactivation de TLS/1.0 et TLS/1.1; la stratégie reste disponible jusqu’au tour V90.  |  
| Bloquer les téléchargements de contenu mixte | [Chrome + 1](#release-comments) \ (Edge V86 \)  |  | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris sur la chronologie prévue par Google pour cette modification, accédez à l' [entrée de blog Google Security][GoogleBlogSecurity20200206].  Le planning de déploiement Microsoft des types de fichiers à avertir ou bloquer est planifié pour une version après chrome.  |  
| Déconseillé AppCache | [Chrome + 1](#release-comments) \ (Edge V86 \)  |  | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la [documentation de WebDev][WebDevAppCacheRemoval].  Le planning de déploiement Microsoft pour le retrait est prévu pour une version ultérieure après chrome.  La demande d’un [jeton AppCache OriginTrial][AppCacheOriginTrial] permet aux sites de continuer à utiliser l’API déconseillée jusqu’à l’aide de l’option V90.  |  
| Suppression d’Adobe Flash | Bordure V88  |  | Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la feuille de [route de chrome Adobe Flash][ChromiumFlashRoadmapSupportRemoved].  | 
| Désactiver et supprimer FTP | Bordure V88  | V87 Edge Beta | Dans la version bêta latérale de V87, la prise en charge du protocole FTP est désactivée par défaut. dans le cas d’un V87 de frontière stable, il reste activé.  Dans Edge V88, la prise en charge du protocole FTP est entièrement supprimée.  Cette modification intervient dans le projet de chrome sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à l’entrée d’état de la [plateforme chrome][ChromePlatformStatus6246151319715840].  Les entreprises qui disposent d’un site nécessitant une prise en charge FTP peuvent continuer à utiliser le protocole FTP en configurant le site pour utiliser le [mode IE](https://docs.microsoft.com/deployedge/edge-ie-mode).  |   

##### Commentaires de publication  

:::row:::
   :::column span="1":::
      Chrome + 1
   :::column-end:::
   :::column span="2":::
      Sur la base des commentaires des utilisateurs et des développeurs, la fonctionnalité indiquée ou la modification d’une version après chrome.
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome ou chrome + 1
   :::column-end:::
   :::column span="2":::
      En fonction des commentaires des utilisateurs et des développeurs, de la fonctionnalité ou du changement de navires en même temps ou en une seule dissémination après chrome.
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedEdgePoliciesSSLMinVersion]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin-Microsoft Edge-politiques | Documents Microsoft"  

[ChromePlatformStatus4664843055398912]: https://www.chromestatus.com/feature/4664843055398912 "Empêcher la synchronisation de XHR dans le code JavaScript de page État de la plateforme chrome"  
[ChromePlatformStatus5088147346030592]: https://www.chromestatus.com/feature/5088147346030592 "Cookies par défaut de SameSite = Lax | État de la plateforme chrome"  
[ChromePlatformStatus6251880185331712]: https://www.chromestatus.com/feature/6251880185331712 "Stratégie de renvoi: par défaut en cas d’origine État de la plateforme chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Déconseillé du support FTP État de la plateforme chrome"

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Prise en charge de la prise en charge du chrome (cible: chrome 88 +-Jan 2021) Projets de chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protection des utilisateurs contre les téléchargements insécurisés dans Google Chrome-blog de sécurité Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal/ "Suppression de AppCache"
[AppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Jeton OriginTrial AppCache"

<!--todo:  cleanup links  -->  
