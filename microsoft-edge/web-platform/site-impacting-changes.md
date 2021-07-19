---
description: Fournit un résumé des modifications à fort impact qui peuvent avoir un impact sur la compatibilité du site.
title: Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, compatibilité, plateforme web
ms.openlocfilehash: 815a350dc82d02e77354f3079880df9ce81750b7
ms.sourcegitcommit: 412ec98cd9f57f74af69acad0a317d1dffa3b323
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/08/2021
ms.locfileid: "11640603"
---
# <a name="site-compatibility-impacting-changes-coming-to-microsoft-edge"></a>Modifications apportées à Microsoft Edge ayant un impact sur la compatibilité des sites  

La plateforme web est un ensemble de technologies utilisées pour la création de pages web.  Les technologies incluent HTML, CSS, JavaScript et de nombreuses autres normes ouvertes.  La plateforme web évolue constamment pour améliorer l’expérience utilisateur, la sécurité et la confidentialité.  Dans certains cas, les modifications peuvent affecter les fonctionnalités des pages web existantes.  Pour plus d’informations sur les modifications à venir de la plateforme web du projet Chromium, accédez à [chronologie de publication de l’état de la plateforme Chrome.][ChromestatusFeaturesSchedule]  

Microsoft Edge adopte la quasi-totalité des modifications apportées en amont à la plateforme web par le projet Chromium.  Les raisons incluent des raisons de fonctionnalité et de compatibilité.  Microsoft reste en contrôle total du navigateur Microsoft Edge et peut différer ou rejeter les modifications.  L’équipe Microsoft Edge décide si les modifications profitent aux utilisateurs du navigateur.  Les fonctionnalités pour lesquelles Microsoft Edge prévoit de s'écarter des modifications apportées à Chromium en termes de calendrier ou de comportement sont indiquées dans le tableau suivant.  Le tableau met également en évidence les modifications à fort impact que l'équipe Microsoft Edge suit de près.  

Relisez souvent cet article.  L’équipe Microsoft Edge met à jour cet article à mesure que la réflexion évolue, que les chronologies se solidifient et que de nouvelles modifications sont annoncées.  

| Modification | Canal Stable | Expérimentation | Informations complémentaires |  
|:--- |:--- |:--- |:--- |
| Dépréciation de la sémantique SDP du Plan B de WebRTC | [Chrome+1](#release-comments) \(Edge v94\)  |  | Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Cette modification rend obsolète un ancien dialecte de protocole de description de session (SDP) appelé Plan B. Il est remplacé par le Plan unifié qui est un format SDP conforme aux spécifications et compatible avec tous les navigateurs. Pour plus d’informations, accédez à [Entrée d’état de la plateforme Chrome][ChromestatusFeature5823036655665152] et [PSA: Chronologie de l’annulation et de la suppression du plan SDP - Veuillez migrer vers le plan unifié][PSADeprecateWebRTCPlanB]. La planification du déploiement de Microsoft pour l’annulation est prévue pour une version après Chrome. La demande d’un [Jeton d’essai webRTC Plan B Reverse Origin][ChromeDevelopersOrigintrialsWebRTCPlanBOriginTrial] permet aux sites de continuer à utiliser l’API dépréciée jusqu’à Edge v96. |
| Cookies par défaut sur `SameSite=Lax` et `SameSite=None-requires-Secure` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v82, Dev v82 | Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à [Entrée État de la plateforme Chrome][ChromestatusFeature5088147346030592].  |  
| Stratégie de référence : par défaut `strict-origin-when-cross-origin` | [Chrome+1](#release-comments) \(Edge v86\)  | Canary v79, Dev v79 | Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à [Entrée État de la plateforme Chrome][ChromestatusFeature6251880185331712].  |  
| Interdire l'utilisation de `XmlHttpRequest` synchrone dans le renvoi d'une page | [Chrome+1](#release-comments) \(Edge v83\) |  | Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  À l'instar de Chrome, Microsoft Edge propose une stratégie de groupe permettant de désactiver cette modification jusqu'à la version 88 de Edge.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à [Entrée État de la plateforme Chrome][ChromestatusFeature4664843055398912].  |  
| Afficher une invite subtile pour les demandes d’autorisations de notification | Edge v84 |  | Les demandes de notification discrètes affichent une icône de demande subtile dans la barre d'adresse pour les autorisations de notification de site demandées à l'aide de l'API `Notifications` ou `Push`, remplaçant ainsi l'interface utilisateur de l'invite de l'autorisation complète ou standard.  Cette fonctionnalité est actuellement activée pour tous les utilisateurs.  Pour refuser les demandes de notification silencieuses, accédez à `edge://settings/content/notifications`.  À l’avenir, l’équipe Microsoft Edge peut envisager de réactiver l’invite de notification complet dans certains scénarios.  |  
| Désactiver TLS/1.0 et TLS/1.1 | Edge v84 |  |  |  
| Bloquer les téléchargements de contenu mixte | [Chrome+1](#release-comments) \(Edge v86\)  |  | Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, y compris la chronologie planifiée par Google pour cette modification, accédez à [Entrée de blog de sécurité Google][GoogleBlogSecurity20200206].  La planification du déploiement de Microsoft sur les types de fichiers à avertir ou bloquer est prévue pour une version après Chrome.  |  
| Déconseiller AppCache | [Chrome+1](#release-comments) \(Edge v86\)  |  | Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la [documentation WebDev.][WebDevAppCacheRemoval]  La planification du déploiement de Microsoft pour l’annulation est prévue pour une version après Chrome.  La demande d’un [Jeton AppCache OriginTrial][ChromeDevelopersOrigintrialsAppCacheOriginTrial] permet aux sites de continuer à utiliser l’API déconseillée jusqu’à Edge v90.  |  
| Suppression d’Adobe Flash | Edge v88  |  | Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à la [feuille de route Chromium Adobe Flash][ChromiumFlashRoadmapSupportRemoved].  | 
| Supprimer la prise en charge FTP | Edge v88  | Edge Beta v87 | Dans Edge v88, la prise en charge FTP est entièrement supprimée.  Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé.  Pour plus d’informations, accédez à [Entrée d’état de la plateforme Chrome.][ChromestatusFeature6246151319715840]  Les entreprises qui ont des sites qui nécessitent toujours la prise en charge FTP peuvent continuer à utiliser FTP en configurant le site pour utiliser le [mode IE.][DeployedgeEdgeIeMode]  | 
| Mise à niveau automatique des images à contenu mixte | Edge v88  |  | Les références \(HTTP\) non sécurisées aux images sont automatiquement mises à niveau vers HTTPS; Si l’image n’est pas disponible sur HTTPS, le téléchargement de l’image échoue. Une [Stratégie de groupe][DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls] est disponible pour contrôler cette fonctionnalité. Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Pour plus d’informations, accédez à [Entrée d’état de la plateforme Chrome.][ChromestatusFeature4926989725073408]  | 
| Authentification HTTP non bloquée lorsque les cookies tiers sont bloqués  | Edge v87  |  | À partir de Edge v87, lorsque les cookies sont bloqués pour les demandes tierces, à l’aide de la stratégie [BlockThirdPartyCookies][DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies] ou de la bascule dans `edge://settings`, l’authentification HTTP est également interdite. Cette modification peut avoir un impact sur mode Entreprise [téléchargements de liste de sites pour Internet Explorer mode][DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy] si le point de terminaison hébergeant la liste nécessite l’utilisation de l’authentification HTTP.  Pour autoriser l’utilisation des cookies et de l’authentification HTTP pour les téléchargements de listes de sites en mode Enterprise, ajoutez un modèle d’URL correspondant à la stratégie [CookiesAllowedForURLs][DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls].  |
| Suppression de 3DES dans TLS  | Edge v93  |  | À partir de Edge v93, la prise en charge de la suite de chiffrement TLS_RSA_WITH_3DES_EDE_CBC_SHA sera supprimée. Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Pour plus d’informations, accédez à [Entrée d’état de la plateforme Chrome.][ChromestatusFeature6678134168485888] En outre, dans Edge v93, une stratégie de compatibilité sera disponible pour prendre en charge les scénarios qui doivent conserver la compatibilité avec les serveurs obsolètes. Cette stratégie de compatibilité devient obsolète et cesse de fonctionner dans Edge v95. Assurez-vous de mettre à jour les serveurs concernés avant cela. |
| Limiter les demandes de réseau privé aux contextes sécurisés  | Edge v93  |  | À partir de la version 93 d'Edge, l'accès aux ressources des réseaux locaux (intranet) à partir de pages sur Internet nécessite que ces pages soient transmises par HTTPS. Ce changement se produit dans le projet Chromium, sur lequel Microsoft Edge est basé. Pour plus d’informations, accédez à [Entrée d’état de la plateforme Chrome.][ChromestatusFeature5436853517811712] Deux stratégies de compatibilité sont disponibles pour prendre en charge les scénarios qui doivent conserver la compatibilité avec les pages non sécurisées: [InsecurePrivateNetworkRequestAllowed][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed] et [InsecurePrivateNetworkRequestAllowedForUrls][DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls]. |

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
      En fonction des commentaires des utilisateurs et des développeurs, la fonctionnalité ou la modification indiquée est fournie en même temps ou après Chrome.  
   :::column-end:::
:::row-end:::

<!-- links -->  

[DeployedgeEdgeIeMode]: /deployedge/edge-ie-mode "À propos du mode IE | Microsoft Docs"  
[DeployedgeEdgeIeModePoliciesConfigureUsingUseEnterpriseModeIeWebsiteListPolicy]: /deployedge/edge-ie-mode-policies#configure-using-the-use-the-enterprise-mode-ie-website-list-policy "Configurer à l’aide de la stratégie Utiliser la liste des sites web IE en mode Entreprise: Configurer les stratégies de mode IE | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesBlockthirdpartycookies]: /deployedge/microsoft-edge-policies#blockthirdpartycookies "BlockThirdPartyCookies: Microsoft Edge - Stratégies | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesCookiesallowedforurls]: /deployedge/microsoft-edge-policies#cookiesallowedforurls "CookiesAllowedForUrls - Microsoft Edge - Stratégies | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesInsecurecontentallowedforurls]:  /deployedge/microsoft-edge-policies#insecurecontentallowedforurls "InsecureContentAllowedForUrls - Microsoft Edge - Stratégies | Microsoft Docs"  
[DeployedgeMicrosoftEdgePoliciesSslversionmin]: /deployedge/microsoft-edge-policies#sslversionmin "SSLVersionMin - Microsoft Edge: Stratégies | Microsoft Docs"  
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowed]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowed "InsecurePrivateNetworkRequestsAllowed: Microsoft Edge - Stratégies | Microsoft Docs"
[DeployEdgeMicrosoftEdgePoliciesInsecurePrivateNetworkRequestAllowedForUrls]: /deployedge/microsoft-edge-policies#insecureprivatenetworkrequestsallowedforurls "InsecurePrivateNetworkRequestsAllowedForUrls: Microsoft Edge - Stratégies | Microsoft Docs"

[ChromestatusFeaturesSchedule]: https://www.chromestatus.com/features/schedule "Calendrier de publication | État de la plateforme Chrome"  
[ChromestatusFeature4664843055398912]: https://chromestatus.com/feature/4664843055398912 "Interdire le XHR synchrone dans le renvoi de la page JavaScript | État de la plateforme Chrome"  
[ChromestatusFeature4926989725073408]: https://chromestatus.com/feature/4926989725073408 "Mise à niveau automatique du contenu mixte d’image | État de la plateforme Chrome"  
[ChromestatusFeature5088147346030592]: https://chromestatus.com/feature/5088147346030592 "Valeur par défaut des cookies SameSite=Lax | État de la plateforme Chrome"  
[ChromestatusFeature6246151319715840]: https://chromestatus.com/feature/6246151319715840 "Dépréciation de la prise en charge de FTP | État de la plateforme Chrome"  
[ChromestatusFeature6251880185331712]: https://chromestatus.com/feature/6251880185331712 "Stratégie de référence : par défaut sur strict-origin-when-cross-origin | État de la plateforme Chrome"  
[ChromestatusFeature6678134168485888]: https://chromestatus.com/feature/6678134168485888 "Supprimer 3DES dans TLS | État de la plateforme Chrome"
[ChromestatusFeature5436853517811712]: https://chromestatus.com/feature/5436853517811712 "Limiter les demandes de réseau privé pour les sous-ressources à des contextes sécurisés | État de la plateforme Chrome"
[ChromestatusFeature5823036655665152]: https://www.chromestatus.com/feature/5823036655665152 "[WebRTC] Dépréciation et suppression du Plan B (déprécié) | État de la plateforme Chrome"
[ChromiumFlashRoadmapSupportRemoved]: https://www.chromium.org/flash-roadmap#TOC-Flash-Support-Removed-from-Chromium-Target:-Chrome-88---Jan-2021- "Prise en charge flash supprimée de Chromium (Cible: Chrome 88+ - Janvier 2021) - Feuille de route flash | Chromium Projets"  

[ChromeDevelopersOrigintrialsAppCacheOriginTrial]: https://developers.chrome.com/origintrials/#/view_trial/1776670052997660673 "Jeton AppCache OriginTrial | Développeurs Chrome"  
[ChromeDevelopersOrigintrialsWebRTCPlanBOriginTrial]: https://developer.chrome.com/origintrials/#/view_trial/3892235977954951169 "WebRTC Plan B Jetons d’essai d’origine inversée | Développeurs Chrome"

[GoogleBlogSecurity20200206]: https://security.googleblog.com/2020/02/protecting-users-from-insecure_6.html "Protection des utilisateurs contre les téléchargements non sécurisés dans Google Chrome - Blog sur la sécurité en ligne Google" 

[WebDevAppCacheRemoval]: https://web.dev/appcache-removal "Préparation de la suppression d’AppCache | web.dev"  

[PSADeprecateWebRTCPlanB]: https://groups.google.com/g/discuss-webrtc/c/UBtZfawdIAA/m/-UVQQcubBQAJ "PSA: Chronologie de l’annulation et de la suppression de SDP plan B - Veuillez migrer vers le plan unifié"

<!--todo:  cleanup links  -->  
