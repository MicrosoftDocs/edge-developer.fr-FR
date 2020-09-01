---
title: Présentation des problèmes de sécurité avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 850dde157a673a84a3e603f22a5e54abd90bde5d
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984300"
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
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Volet sécurité" lightbox="../media/security-security-overview-secure.msft.png":::
       Volet **sécurité**  
    :::image-end:::  
    
## Problèmes courants   

### Origines principales non sécurisées   

Lorsque l’origine principale d’une page n’est pas sécurisée, la **vue d’ensemble** de la sécurité indique que **cette page n’est pas sécurisée**.  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Page non sécurisée" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Page non sécurisée  
:::image-end:::  

Ce problème survient lorsque l’URL visitée a été demandée sur HTTP.  Pour garantir la sécurité de votre application, vous devez la demander sur HTTPs.  Par exemple, si vous observez l’URL dans la barre d’adresses, il est probable que le résultat ressemble à ceci `http://example.com` .  Pour sécuriser l’URL, l’URL devrait être `https://example.com` .  

Si vous avez déjà configuré HTTPs sur votre serveur, il vous suffit de configurer votre serveur pour rediriger toutes les demandes HTTP vers HTTPs.  

Si vous n’avez pas configuré HTTPs sur votre serveur, [cryptez][LetsEncrypt] -vous pour démarrer le processus de manière gratuite et relativement simple.  Vous pouvez également envisagez d’héberger votre site sur un réseau de distribution de contenu (CDN).  La plupart des sites hôtes CDN les plus importants sur HTTPs par défaut.  

> [!TIP]
> La directive [utiliser HTTPS][WebhintUseHttps] dans [webhint][Webhint] permet d’automatiser le processus de vérification de l’utilisation de toutes les demandes HTTP adressées aux HTTPS.  

### Contenu mixte   

Le **contenu mixte** signifie que l’origine principale d’une page est sécurisée, mais que la page a demandé des ressources d’origines non sécurisées.  Les pages de contenu mixte ne sont que partiellement protégées, car le contenu HTTP est accessible aux renifleurs et est vulnérable aux attaques par le biais du milieu.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Contenu mixte" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Contenu mixte  
:::image-end:::  

Dans la figure précédente, cliquez sur **afficher une requête dans le panneau réseau** pour ouvrir le panneau **réseau** et appliquez le `mixed-content:displayed` filtre de sorte que le **Journal réseau** n’affiche que les ressources non sécurisées.  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Ressources mixtes du journal réseau" lightbox="../media/security-network-filter.msft.png":::
   Ressources mixtes du **Journal réseau**  
:::image-end:::  

## Afficher les détails   

### Afficher le certificat d’origine principal   

Dans la **vue d’ensemble**de la sécurité, cliquez sur **afficher le certificat** pour inspecter rapidement le certificat de l’origine principale.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Un certificat d’origine principal;" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Un certificat d’origine principal;  
:::image-end:::  

### Afficher les détails de l’origine   

Cliquez sur l’une des entrées dans le volet de navigation de gauche pour afficher les détails de l’origine.  Dans la page détails, vous pouvez consulter les informations de connexion et de certificat.  Les informations de transparence du certificat apparaissent également lorsqu’elles sont disponibles.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Détails de l’origine principale" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Détails de l’origine principale  
:::image-end:::  

<!--  
 


-->  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Outils de développement Microsoft Edge (chrome) | Documents Microsoft"  
[DevToolsOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  


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
