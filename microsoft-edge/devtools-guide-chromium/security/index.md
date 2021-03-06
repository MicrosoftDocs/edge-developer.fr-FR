---
description: Utilisez le Panneau de sécurité pour vous assurer qu’une page est entièrement protégée par HTTPS.
title: Comprendre les problèmes de sécurité avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 71138ad33afb9eb56055fa522eb35edb71974c89
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397775"
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

# <a name="understand-security-issues-with-microsoft-edge-devtools"></a>Comprendre les problèmes de sécurité avec Microsoft Edge DevTools  

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  Navigate to **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <a name="open-the-security-panel"></a>Ouvrir le panneau de sécurité  

Le **panneau** de sécurité est l’endroit principal dans DevTools pour l’inspection de la sécurité d’une page.  

1.  [Ouvrez DevTools][DevToolsOpen].  
1.  Sélectionnez **l’onglet** Sécurité pour ouvrir **l’outil** Sécurité.  
    
    :::image type="complex" source="../media/security-security-overview-secure.msft.png" alt-text="Panneau de sécurité" lightbox="../media/security-security-overview-secure.msft.png":::
       Panneau **de** sécurité  
    :::image-end:::  
    
## <a name="common-problems"></a>Problèmes courants  

### <a name="non-secure-main-origins"></a>Origines principales non sécurisées  

Lorsque l’origine principale d’une page n’est pas sécurisée, la vue **d’ensemble** de la sécurité indique **que cette page n’est pas sécurisée.**  

:::image type="complex" source="../media/security-security-overview-non-secure.msft.png" alt-text="Page non sécurisée" lightbox="../media/security-security-overview-non-secure.msft.png":::
   Page non sécurisée  
:::image-end:::  

Ce problème se produit lorsque l’URL que vous avez visitée a été demandée sur HTTP.  Pour le sécuriser, vous devez le demander sur HTTPS.  Par exemple, si vous examinez l’URL dans votre barre d’adresses, elle ressemble probablement à `http://example.com` .  Pour sécuriser l’URL doit être `https://example.com` .  

Si vous avez déjà configuré HTTPS sur votre serveur, il vous suffit de configurer votre serveur pour qu’il redirige toutes les requêtes HTTP vers HTTPS.  

Si vous [n’avez][LetsEncrypt] pas installé HTTPS sur votre serveur, chiffrer offre un moyen gratuit et relativement simple de démarrer le processus.  Vous pouvez également envisager d’héberger votre site sur un CDN.  La plupart des PRINCIPAUX CDN hébergent des sites sur HTTPS par défaut maintenant.  

> [!TIP]
> [L’indication Utiliser HTTPS][WebhintUseHttps] dans [webhint][Webhint] peut vous aider à automatiser le processus de s’assurer que toutes les requêtes HTTP sont dirigées vers HTTPS.  

### <a name="mixed-content"></a>Contenu mixte  

**Le contenu mixte** signifie que l’origine principale d’une page est sécurisée, mais que la page a demandé des ressources à partir d’origines non sécurisées.  Les pages de contenu mixte ne sont que partiellement protégées, car le contenu HTTP est accessible aux renifleurs et vulnérable aux attaques de l’homme au milieu.  

:::image type="complex" source="../media/security-security-overview-mixed-secure.msft.png" alt-text="Contenu mixte" lightbox="../media/security-security-overview-mixed-secure.msft.png":::
   Contenu mixte  
:::image-end:::  

Dans la figure précédente, choisissez Afficher **1** **** dans le panneau Réseau pour ouvrir l’outil Réseau et appliquer le filtre afin que le journal réseau affiche uniquement les ressources `mixed-content:displayed` non **** sécurisées.  

:::image type="complex" source="../media/security-network-filter.msft.png" alt-text="Ressources mixtes dans le journal réseau" lightbox="../media/security-network-filter.msft.png":::
   Ressources mixtes dans le **journal réseau**  
:::image-end:::  

## <a name="view-details"></a>Afficher les détails  

### <a name="view-main-origin-certificate"></a>Afficher le certificat d’origine principale  

Dans la **vue d’ensemble de**la sécurité, choisissez **Afficher le certificat** pour inspecter rapidement le certificat pour l’origine principale.  

:::image type="complex" source="../media/security-security-overview-secure-view-certificate.msft.png" alt-text="Un certificat d’origine principale" lightbox="../media/security-security-overview-secure-view-certificate.msft.png":::
   Un certificat d’origine principale  
:::image-end:::  

### <a name="view-origin-details"></a>Afficher les détails de l’origine  

Choisissez l’une des entrées du navigation gauche pour afficher les détails de l’origine.  À partir de la page de détails, vous pouvez afficher les informations de connexion et de certificat.  Les informations de transparence des certificats sont également affichées lorsqu’elles sont disponibles.  

:::image type="complex" source="../media/security-security-overview-mixed-secure-main-origin.msft.png" alt-text="Détails de l’origine principale" lightbox="../media/security-security-overview-mixed-secure-main-origin.msft.png":::
   Détails de l’origine principale  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium/index.md "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevToolsOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[LetsEncrypt]: https://letsencrypt.org "Chiffrement - Certificats SSL/TLS gratuits"  

[Webhint]: https://webhint.io "webhint"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Utiliser le protocole HTTPS | documentation webhint"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/security/index) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
