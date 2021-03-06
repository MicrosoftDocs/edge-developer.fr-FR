---
description: Découvrez comment détecter les problèmes réseau dans le panneau Réseau de Microsoft Edge DevTools.
title: Guide des problèmes de réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 12cc447fa9d8ef8624e8528430eabc25ab523dd0
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398272"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="network-issues-guide"></a>Guide des problèmes de réseau  

Ce guide vous montre comment détecter les problèmes réseau ou les opportunités d’optimisation dans le panneau Réseau de Microsoft Edge DevTools.  

Pour découvrir les principes de base de **l’outil Réseau,** accédez à [Démarrer.][NetworkPerformance]  

## <a name="queued-or-stalled-requests"></a>Demandes en file d’attente ou bloquées  

**Symptômes**  

Six demandes sont téléchargées simultanément.  Après cela, une série de demandes sont en file d’attente ou bloquées.  Une fois l’une des six premières demandes se termine, l’une des demandes de la file d’attente démarre.  

Dans la **cascade de** la figure suivante, les six premières demandes de ressources démarrent `edge-iconx1024.msft.png` simultanément.  Les demandes suivantes sont bloquées jusqu’à ce que l’une des six premières se termine.  

:::image type="complex" source="../media/network-network-disabled-cache-resources-queue.msft.png" alt-text="Exemple de série en file d’attente ou bloquée dans le panneau Réseau" lightbox="../media/network-network-disabled-cache-resources-queue.msft.png":::
   Exemple d’une série en file d’attente ou bloquée dans **l’outil** Réseau  
:::image-end:::  

**Causes**  

Trop de demandes sont faites sur un seul domaine.  Sur les connexions HTTP/1.0 ou HTTP/1.1, Microsoft Edge autorise un maximum de six connexions TCP simultanées par hôte.  

**Correctifs**  

*   Implémentez le partitionnage de domaine si vous devez utiliser HTTP/1.0 ou HTTP/1.1.  
*   Utilisez HTTP/2.  N’utilisez pas le partitionnage de domaine avec HTTP/2.  
*   Supprimer ou différer les demandes inutiles afin que les demandes critiques se téléchargent plus tôt.  
    
## <a name="slow-time-to-first-byte-ttfb"></a>Slow Time To First Byte (TTFB)  

**Symptômes**  

Une demande passe beaucoup de temps à attendre de recevoir le premier byte du serveur.  

Dans la figure suivante, la barre longue et verte de la **cascade** indique que la demande attendait longtemps.  Cela a été simulé à l’aide d’un profil pour limiter la vitesse du réseau et ajouter un délai.  

:::image type="complex" source="../media/network-network-resources-using-dial-up-profile.msft.png" alt-text="Exemple d’une demande dont l’heure est lente au premier sur deux byte" lightbox="../media/network-network-resources-using-dial-up-profile.msft.png":::
   Exemple d’une demande dont l’heure est lente au premier sur deux byte  
:::image-end:::  

**Causes**  

*   La connexion entre le client et le serveur est lente.  
*   Le serveur est lent à répondre.  Hébergez le serveur localement pour déterminer si la connexion ou le serveur est lent.  Si vous obtenez toujours une durée lente jusqu’au premier byte \(TTFB\) lors de l’accès à un serveur local, le serveur est lent.  
    
**Correctifs**  

*   Si la connexion est lente, envisagez d’héberger votre contenu sur un CDN ou de modifier les fournisseurs d’hébergement.  
*   Si le serveur est lent, envisagez d’optimiser les requêtes de base de données, d’implémenter un cache ou de modifier la configuration de votre serveur.  
    
## <a name="slow-content-download"></a>Téléchargement de contenu lent  

**Symptômes**  

Le téléchargement d’une demande prend beaucoup de temps.  

Dans la figure suivante, la longue **** barre bleue dans la cascade en face du png signifie que le téléchargement a pris beaucoup de temps.  

:::image type="complex" source="../media/network-network-resources-edge-devtools.msft.png" alt-text="Exemple de demande longue à télécharger" lightbox="../media/network-network-resources-edge-devtools.msft.png":::
   Exemple de demande longue à télécharger  
:::image-end:::  

**Causes**  

*   La connexion entre le client et le serveur est lente.  
*   Une grande partie du contenu est en cours de téléchargement.  
    
**Correctifs**  

*   Envisagez d’héberger votre contenu sur un CDN ou de modifier les fournisseurs d’hébergement.  
*   Envoyez moins d’octets en optimisant vos demandes.  
    
<!--   ## Contribute knowledge  

Do you have a network issue that should be added to this guide?  

*   Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Choose **Send Feedback** \(![Send Feedback][ImageSendFeedbackIcon]\) in the DevTools or select `Alt`+`Shift`+`I` \(Windows, Linux\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.  
*   [Open an issue][WebFundamentalsIssue] on the docs repo.  -->  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageSendFeedbackIcon]: ../media/smile-icon.msft.png  

<!-- links -->  

[NetworkPerformance]: ./index.md "Inspecter l’activité réseau dans microsoft Edge DevTools | Documents Microsoft"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nouveau problème : MicrosoftDocs/edge-developer"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est trouvée ici et est co-auteure par [Les Basques Decéssaisie \(Rédacteur][KayceBasques] technique, Chrome DevTools \& Évérité\) et [Chef Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\). [](https://developers.google.com/web/tools/chrome-devtools/network/issues)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
