---
description: Fournit un résumé des modifications à fort impact qui peuvent avoir un impact sur la compatibilité des sites
title: Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, compatibilité, plateforme web
ms.openlocfilehash: 194e612c008016299b234de816114d24e5569aef
ms.sourcegitcommit: e150d798161277fd3fc610838ef2611dc08f5cf6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/29/2021
ms.locfileid: "11624786"
---
# <a name="site-compatibility-impacting-changes-coming-to-microsoft-edge"></a>Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites  

La plateforme Web est un ensemble de technologies utilisées pour la création de pages web.  Les technologies incluent HTML, CSS, JavaScript et de nombreuses autres normes ouvertes.  La plateforme Web évolue constamment pour améliorer l’expérience utilisateur, la sécurité et la confidentialité.  Dans certains cas, les modifications peuvent affecter les fonctionnalités des pages web existantes.  Pour plus d’informations sur les modifications Chromium plateforme web de projet à venir, accédez à la chronologie de publication de l’état de la plateforme [Chrome.][ChromestatusFeaturesSchedule]  

Microsoft Edge adopte presque toutes les modifications apportées en amont à la plateforme web à partir Chromium projet.  Les raisons incluent des raisons de fonctionnalité et de compatibilité.  Microsoft reste en contrôle total du navigateur Microsoft Edge et peut différer ou rejeter les modifications.  L’Microsoft Edge décide si la modification est bénéfique aux utilisateurs du navigateur.  Les fonctionnalités dans Microsoft Edge des plans pour s’écarter de Chromium changements de minutage ou de comportement sont indiqués dans le tableau suivant.  Le tableau met également en évidence les modifications à fort impact que l’équipe Microsoft Edge suit.  

Examinez souvent cet article.  L Microsoft Edge de travail met à jour cet article à mesure que la réflexion évolue, que les chronologies se solidifient et que de nouvelles modifications sont annoncées.  

| Modification | Canal Stable | Expérimentation | Informations complémentaires |  
|:--- |:--- |:--- |:--- |
| Cookies par défaut sur `SameSite=Lax` et `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée État de la plateforme [Chrome.][ChromestatusFeature5088147346030592]  |  
| Stratégie de référence : par défaut `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée État de la plateforme [Chrome.][ChromestatusFeature6251880185331712]  |  
| Ne pas être synchrone lors `XmlHttpRequest` du rejet de page | [Chrome+1](#release-comments) \(Edge v83\) |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Matching Chrome, Microsoft Edge offers a Group Policy to turn off this change until Edge v88.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée État de la plateforme [Chrome.][ChromestatusFeature4664843055398912]  |  
| Afficher une invite subtile pour les demandes d’autorisations de notification | Edge v84 |  | Les demandes de notification silencieuses affichent une icône de demande subtile dans la barre d’adresses pour les autorisations de notification de site demandées à l’aide de l’API ou de l’API, en remplaçant l’interface utilisateur complète ou standard de l’invite de présentation des `Notifications` `Push` autorisations.  Cette fonctionnalité est actuellement activée pour tous les utilisateurs.  Pour refuser les demandes de notification silencieuse, accédez à `edge://settings/content/notifications` .  À l’avenir, l’équipe Microsoft Edge peut envisager de réactiver l’invite de notification de volant complète dans certains scénarios.  |  
| Désactiver TLS/1.0 et TLS/1.1 | Edge v84 |  |  |  
| Bloquer les téléchargements de contenu mixte | [Chrome+1](#release-comments) \(Edge v86\)  |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à l’entrée du blog sur [la sécurité Google.][GoogleBlogSecurity20200206]  La planification du déploiement de Microsoft sur les types de fichiers à avertir ou bloquer est planifiée pour une version après Chrome.  |  
| Deprecate AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la [documentation WebDev.][WebDevAppCacheRemoval]  La planification du déploiement de Microsoft pour l’annulation est prévue pour une version après Chrome.  La demande d’un [jeton OriginTrial AppCache][ChromeDevelopersOrigintrialsAppCacheOriginTrial] permet aux sites de continuer à utiliser l’API dépréciée jusqu’à Edge v90.  |  
| Suppression d’Adobe Flash | Edge v88  |  | Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la feuille de [route Chromium Adobe Flash.][ChromiumFlashRoadmapSupportRemoved]  | 
| Supprimer la prise en charge FTP | Edge v88  | Edge Beta v87 | Dans Edge v88, la prise en charge ftp est entièrement supprimée.  Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à l’entrée d’état [de la plateforme Chrome.][ChromestatusFeature6246151319715840]  Les entreprises qui ont des sites qui nécessitent toujours la prise en charge ftp peuvent continuer à utiliser FTP en configurant le site pour utiliser [le mode IE.][DeployedgeEdgeIeMode]  | 
| Autoupgrade mixed content images | Edge v88  |  | Les références \(HTTP\) non sécurisées aux images sont automatiquement mises à niveau vers HTTPS ; Si l’image n’est pas disponible sur HTTPS, le téléchargement de l’image échoue. Une [stratégie de][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] groupe est disponible pour contrôler cette fonctionnalité. Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Pour plus d’informations, accédez à l’entrée État de [la plateforme Chrome.][ChromestatusFeature4926989725073408]  | 
| Authentification HTTP non bloquée lorsque les cookies tiers sont bloqués  | Edge v87  |  | À partir de Edge v87, lorsque les cookies sont bloqués pour les demandes tierces, à l’aide de la stratégie [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] ou de la bascule dans , l’authentification HTTP est également `edge://settings` interdit. Cette modification peut avoir un impact Enterprise [téléchargements][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] de la liste des sites en mode Internet Explorer si le point de terminaison hébergeant la liste nécessite l’utilisation de l’authentification HTTP.  Pour autoriser l’utilisation des cookies et de l’authentification HTTP pour les téléchargements de listes de sites en mode Enterprise, ajoutez un modèle d’URL correspondant à la stratégie [CookiesAllowedForURLs.][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]  |
| Suppression de 3DES dans TLS  | Edge v93  |  | À partir de Edge v93, la prise en charge de TLS_RSA_WITH_3DES_EDE_CBC_SHA suite de chiffrement sera supprimée. Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Pour plus d’informations, accédez à l’entrée État de [la plateforme Chrome.][ChromestatusFeature6678134168485888] En outre, dans Edge v93, une stratégie de compatibilité sera disponible pour prendre en charge les scénarios qui doivent conserver la compatibilité avec les serveurs obsolètes. Cette stratégie de compatibilité deviendra obsolète et cessera de fonctionner dans Edge v95. Assurez-vous de mettre à jour les serveurs touchés avant. |
| Limiter les demandes de réseau privé aux contextes sécurisés  | Edge v93  |  | À partir de Edge v93, l’accès aux ressources sur les réseaux locaux (intranet) à partir de pages sur Internet nécessite que ces pages soient remis via HTTPS. Cette modification se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Pour plus d’informations, accédez à l’entrée État de [la plateforme Chrome.][ChromestatusFeature5436853517811712] Deux stratégies de compatibilité sont disponibles pour prendre en charge les scénarios qui doivent conserver la compatibilité avec les pages non sécurisées : [InsecurePrivateNetworkRequestAllowed][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed] et [InsecurePrivateNetworkRequestAllowedForUrls][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls]. |

##### <a name="release-comments"></a>Publier des commentaires  

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
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Configurer à l’aide de la stratégie de liste Enterprise de sites web En mode IE - Configurer les stratégies de mode IE | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge - Stratégies | Documents Microsoft"  
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed "InsecurePrivateNetworkRequestsAllowed - Microsoft Edge - Stratégies | Documents Microsoft"
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls "InsecurePrivateNetworkRequestsAllowedForUrls - Microsoft Edge - Stratégies | Documents Microsoft"

[ChromestatusFeaturesSchedule]: https://www.chromestatus.com/features/schedule "Calendrier de publication | État de la plateforme Chrome"  
[ChromestatusFeature4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Disallow sync XHR in page dismissal JavaScript | État de la plateforme Chrome"  
[ChromestatusFeature4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Mise à niveau automatique du contenu mixte d’image | État de la plateforme Chrome"  
[ChromestatusFeature5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Valeur par défaut des cookies SameSite=Lax | État de la plateforme Chrome"  
[ChromestatusFeature6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Deprecate FTP support | État de la plateforme Chrome"  
[ChromestatusFeature6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Stratégie de référence : par défaut sur strict-origin-when-cross-origin | État de la plateforme Chrome"  
[ChromestatusFeature6678134168485888]: https://chromestatus.com/feature/6678134168485888 "Supprimer 3DES dans TLS | État de la plateforme Chrome"
[ChromestatusFeature5436853517811712]: https://chromestatus.com/feature/5436853517811712 "Limiter les demandes de réseau privé pour les sous-ressources à des contextes sécurisés | État de la plateforme Chrome"
[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Prise en charge flash supprimée de Chromium (Cible : Chrome 88+ - Jan 2021) - Feuille de route flash | Chromium Projets"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Jeton AppCache OriginTrial | Développeurs Chrome"  

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protection des utilisateurs contre les téléchargements non sécurisés dans Google Chrome - Blog sur la sécurité Google Online" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Préparation de la suppression d’AppCache | web.dev"  

<!--todo:  cleanup links  -->  
