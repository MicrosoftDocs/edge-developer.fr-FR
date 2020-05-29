---
title: Présentation des problèmes de sécurité avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611909"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# Présentation des problèmes de sécurité avec Microsoft Edge DevTools   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## Ouvrir le volet sécurité   

Le volet **sécurité** est l’endroit principal de devtools pour vérifier la sécurité d’une page.  

1.  [Ouvrez devtools][DevToolsOpen].  

1.  Cliquez sur l’onglet **sécurité** pour ouvrir le volet **sécurité** .  
    
    > ##### Figure1  
    > Volet sécurité  
    > ![Volet sécurité][ImageSecurityPanel]  
    
## Problèmes courants   

### Origines principales non sécurisées   

Lorsque l’origine principale d’une page n’est pas sécurisée, la **vue d’ensemble** de la sécurité indique que **cette page n’est pas sécurisée**.  

> ##### Figure 2  
> Page non sécurisée  
> ![Page non sécurisée][ImageNonSecurePage]  

Ce problème survient lorsque l’URL visitée a été demandée sur HTTP.  Pour garantir la sécurité de votre application, vous devez la demander sur HTTPs.  Par exemple, si vous observez l’URL dans la barre d’adresses, il est probable que le résultat ressemble à ceci `http://example.com` .  Pour sécuriser l’URL, l’URL devrait être `https://example.com` .  

Si vous avez déjà configuré HTTPs sur votre serveur, il vous suffit de configurer votre serveur pour rediriger toutes les demandes HTTP vers HTTPs.  

Si vous n’avez pas configuré HTTPs sur votre serveur, [cryptez][LetsEncrypt] -vous pour démarrer le processus de manière gratuite et relativement simple.  Vous pouvez également envisagez d’héberger votre site sur un réseau de distribution de contenu (CDN).  La plupart des sites hôtes CDN les plus importants sur HTTPs par défaut.  

> [!TIP]
> La directive [utiliser HTTPS][WebhintUseHttps] dans [webhint][Webhint] permet d’automatiser le processus de vérification de l’utilisation de toutes les demandes HTTP adressées aux HTTPS.  

### Contenu mixte   

Le **contenu mixte** signifie que l’origine principale d’une page est sécurisée, mais que la page a demandé des ressources d’origines non sécurisées.  Les pages de contenu mixte ne sont que partiellement protégées, car le contenu HTTP est accessible aux renifleurs et est vulnérable aux attaques par le biais du milieu.  

> ##### Figure3  
> Contenu mixte  
> ![Contenu mixte][ImageMixedContent]  

Dans la [figure 3](#figure-3), cliquez sur **Afficher 1 requête dans le panneau réseau** pour ouvrir le panneau **réseau** , puis appliquez le `mixed-content:displayed` filtre de sorte que le **Journal réseau** n’affiche que les ressources non sécurisées.  

> ##### Figure 4  
> Ressources mixtes du journal réseau  
> ![Ressources mixtes du journal réseau][ImageMixedResourcesNetworkLog]  

## Afficher les détails   

### Afficher le certificat d’origine principal   

Dans la **vue d’ensemble**de la sécurité, cliquez sur **afficher le certificat** pour inspecter rapidement le certificat de l’origine principale.  

> ##### Figure 5  
> Un certificat d’origine principal;  
> ![Un certificat d’origine principal;][ImageCertificate]  

### Afficher les détails de l’origine   

Cliquez sur l’une des entrées dans le volet de navigation de gauche pour afficher les détails de l’origine.  Dans la page détails, vous pouvez consulter les informations de connexion et de certificat.  Les informations de transparence du certificat apparaissent également lorsqu’elles sont disponibles.  

> ##### Figure 6  
> Détails de l’origine principale  
> ![Détails de l’origine principale][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Figure 1: volet sécurité"  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Figure 2: page non sécurisée"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Figure 3: contenu mixte"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Figure 4: ressources mixtes du journal réseau"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Figure 5: certificat principal d’origine"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Figure 6: détails de l’origine principale"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (chrome)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  


[LetsEncrypt]: https://letsencrypt.org "Utiliser des certificats SSL/TLS sans cryptage"  

[Webhint]: https://webhint.io "Astuce"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Utiliser HTTPs | documentation webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/security/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
