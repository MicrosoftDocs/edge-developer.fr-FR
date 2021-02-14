---
description: Fournit un résumé des modifications à fort impact qui peuvent avoir un impact sur la compatibilité des sites
title: Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/10/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, compatibilité, plateforme web
ms.openlocfilehash: 64cdb417e6bd0aa648c7e1225bb6dc522f3873ce
ms.sourcegitcommit: fe7301d0f62493e42e6a1a81cdbda3457f0343b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/13/2021
ms.locfileid: "11327504"
---
# Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites  

Le web évolue constamment pour améliorer l’expérience utilisateur, la sécurité et la confidentialité.  Dans certains cas, les modifications peuvent être suffisamment importantes pour avoir un impact sur les fonctionnalités des pages existantes.  Le tableau suivant récapitule les modifications particulièrement importantes que l’équipe Microsoft Edge suit actuellement.  Examinez souvent cet article . L’équipe Microsoft Edge met à jour la page suivante à mesure que la réflexion évolue, que les chronologies s’unifient et que de nouvelles modifications sont annoncées.  

| Modification | Canal Stable | Expérimentation | Informations complémentaires |  
|:--- |:--- |:--- |:--- |
| Cookies par défaut sur `SameSite=Lax` et `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée État de la plateforme [Chrome.][ChromePlatformStatus5088147346030592]  |  
| Stratégie de référence : par défaut `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée État de la plateforme [Chrome.][ChromePlatformStatus6251880185331712]  |  
| Ne pas être synchrone lors `XmlHttpRequest` du rejet de page | [Chrome+1](#release-comments) \(Edge v83\) |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Correspondant à Chrome, Microsoft Edge propose une stratégie de groupe pour désactiver cette modification jusqu’à Edge v88.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée État de la plateforme [Chrome.][ChromePlatformStatus4664843055398912]  |  
| Afficher une invite subtile pour les demandes d’autorisations de notification | Edge v84 |  | Les demandes de notification silencieuses affichent une icône de demande subtile dans la barre d’adresses pour les autorisations de notification de site demandées à l’aide de l’API ou de l’API, en remplaçant l’interface utilisateur du message volant d’autorisation complète ou `Notifications` `Push` standard.  Cette fonctionnalité est actuellement activée pour tous les utilisateurs.  Pour refuser les demandes de notification silencieuse, accédez à `edge://settings/content/notifications` .  À l’avenir, l’équipe Microsoft Edge peut envisager de réactiver l’invite de notification de volant complet dans certains scénarios.  |  
| Désactiver TLS/1.0 et TLS/1.1 par défaut | Edge v84 |  | La stratégie de groupe [SSLMinVersion][DeployedgeMicrosoftEdgePoliciesSslversionmin] permet de réactiver TLS/1.0 et TLS/1.1 ; la stratégie reste disponible jusqu’à Edge v90.  |  
| Bloquer les téléchargements de contenu mixte | [Chrome+1](#release-comments) \(Edge v86\)  |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée du blog sur [la sécurité Google.][GoogleBlogSecurity20200206]  La planification du déploiement de Microsoft sur les types de fichiers à avertir ou bloquer est planifiée pour une version après Chrome.  |  
| Deprecate AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la [documentation WebDev.][WebDevAppCacheRemoval]  La planification du déploiement de Microsoft pour l’annulation est prévue pour une version après Chrome.  La demande d’un [jeton OriginTrial AppCache][ChromeDevelopersOrigintrialsAppCacheOriginTrial] permet aux sites de continuer à utiliser l’API dépréciée jusqu’à Edge v90.  |  
| Suppression d’Adobe Flash | Edge v88  |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la feuille de [route Adobe Flash Chromium.][ChromiumFlashRoadmapSupportRemoved]  | 
| Désactiver et supprimer FTP | Edge v88  | Edge Beta v87 | Dans Edge Beta v87, la prise en charge ftp est désactivée par défaut . dans Edge Stable v87, il reste activé.  Dans Edge v88, la prise en charge ftp est entièrement supprimée.  Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à l’entrée d’état [de la plateforme Chrome.][ChromePlatformStatus6246151319715840]  Les entreprises qui ont des sites qui nécessitent toujours la prise en charge de FTP peuvent continuer à utiliser FTP en configurant le site pour qu’il utilise [le mode IE.][DeployedgeEdgeIeMode]  | 
| Autoupgrade mixed content images | Edge v88  |  | Les références \(HTTP\) non sécurisées aux images sont automatiquement mises à niveau vers HTTPS ; Si l’image n’est pas disponible sur HTTPS, le téléchargement de l’image échoue. Une [stratégie de groupe][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] est disponible pour contrôler cette fonctionnalité. Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Pour plus d’informations, accédez à l’entrée État de [la plateforme Chrome.][ChromePlatformStatus4926989725073408]  | 
| Authentification HTTP non bloquée lorsque les cookies tiers sont bloqués  | Edge v87  |  | À partir de Edge v87, lorsque les cookies sont bloqués pour les demandes tierces, à l’aide de la stratégie [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] ou via la page Paramètres Edge, l’authentification HTTP est également interdit. Cette modification peut avoir un impact sur les [téléchargements][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] de liste des sites en mode Entreprise pour le mode Internet Explorer si le point de terminaison hébergeant la liste requiert l’utilisation de l’authentification HTTP.  Pour autoriser l’utilisation des cookies et de l’authentification HTTP pour les téléchargements de listes de sites en mode Entreprise, ajoutez un modèle d’URL correspondant à la stratégie [CookiesAllowedForURLs.][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]  |   

##### Publier des commentaires  

:::row:::
   :::column span="1":::
      Chrome+1  
   :::column-end:::
   :::column span="2":::
      En fonction des commentaires des utilisateurs et des développeurs, la fonctionnalité ou la modification indiquée est fourni une version après Chrome.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Chrome ou Chrome+1  
   :::column-end:::
   :::column span="2":::
      En fonction des commentaires des utilisateurs et des développeurs, la fonctionnalité ou le changement indiqué est fourni en même temps ou une version après Chrome.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "À propos du mode IE | Documents Microsoft"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Configurer à l’aide de la stratégie de liste des sites web En mode Entreprise d’Internet IE : configurer les stratégies de mode IE | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge - Stratégies | Documents Microsoft"  

[ChromePlatformStatus4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Disallow sync XHR in page dismissal JavaScript | État de la plateforme Chrome"  
[ChromePlatformStatus4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Mise à niveau automatique du contenu mixte d’image | État de la plateforme Chrome"  
[ChromePlatformStatus5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Valeur par défaut des cookies SameSite=Lax | État de la plateforme Chrome"  
[ChromePlatformStatus6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Désintépreser la prise en charge de FTP | État de la plateforme Chrome"  
[ChromePlatformStatus6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Stratégie de référence : par défaut sur strict-origin-when-cross-origin | État de la plateforme Chrome"  

[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Prise en charge flash supprimée de Chromium (cible : Chrome 88+ - Jan 2021) - Feuille de route flash | Projets Chromium"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Jeton AppCache OriginTrial | Développeurs Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protection des utilisateurs contre les téléchargements non sécurisés dans Google Chrome - Blog sur la sécurité Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Préparation de la suppression d’AppCache | web.dev"  

<!--todo:  cleanup links  -->  
