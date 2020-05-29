---
title: Guide de problèmes réseau
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 018a6ef89242d55cefaa974641be456f4501c557
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611804"
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





# Guide de problèmes réseau   




Ce guide vous montre comment détecter les problèmes de réseau ou les opportunités d’optimisation dans le volet réseau de Microsoft Edge DevTools.  

Pour [plus d’informations][NetworkPerformance] sur les concepts de base du réseau, voir découvrir le panneau de configuration.  

## Demandes mises en file d’attente ou bloquées   

### Symptômes  

Six demandes sont en train de télécharger simultanément.  Après cela, une série de demandes est mise en file d’attente ou bloquée.  Après l’exécution de l’une des six premières demandes, une des requêtes de la file d’attente démarre.  

Dans la [figure 1](#figure-1) **, les six** premières demandes de l' `edge-iconx1024.msft.png` actif commencent simultanément.  Les demandes ultérieures sont bloquées jusqu’à ce que l’une des six nouvelles préfinissements.  

> ##### Figure1  
> Exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau  
> ![Exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau][ImageStalled]  

### Causes  

Il y a trop de demandes sur un domaine unique.  Sur les connexions HTTP/1.0 ou HTTP/1.1, Microsoft Edge autorise un maximum de six connexions TCP simultanées par hôte.  

### Correctifs  

*   Implémentez Domain sharding si vous devez utiliser HTTP/1.0 ou HTTP/1.1.  
*   Utiliser HTTP/2.  N’utilisez pas le domaine sharding avec HTTP/2.  
*   Supprimez ou différez les demandes inutiles de manière à ce que les demandes critiques soient téléchargées plus tôt.  

## Temps lent vers le premier octet (TTFB)   

### Symptômes  

Une requête passe un certain temps en attente de réception du premier octet du serveur.  

Dans la [figure 2](#figure-2), la barre verte longue de la **cascade** indique que la demande est en attente pendant un certain temps.  Il a été simulé à l’aide d’un profil afin de limiter la vitesse du réseau et d’ajouter un délai.  

> ##### Figure 2  
> Exemple d’une requête avec un délai de première octet lent  
> ![Exemple d’une requête avec un délai de première octet lent][ImageSlowTimeToFirstByte]  

### Causes  

*   La connexion entre le client et le serveur est lente.  
*   La réponse du serveur est lente.  Hébergez le serveur localement pour déterminer s’il s’agit d’une connexion ou d’un serveur lent.  Si vous obtenez encore un temps lente pour le premier octet \ (TTFB \) lors de l’accès à un serveur local, le serveur est lent.  

### Correctifs  

*   Si la connexion est lente, envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.  
*   Si le serveur est lent, envisagez d’optimiser les requêtes de base de données, de mettre en cache ou de modifier votre configuration serveur.  

## Téléchargement de contenu lent   

### Symptômes  

Le téléchargement d’une requête prend beaucoup de temps.  

Dans la [figure 3](#figure-3), une barre bleue longue **en regard du** fichier PNG signifie que le téléchargement a duré longtemps.  

> ##### Figure3  
> Exemple d’une requête prenant du temps à télécharger  
> ![Exemple d’une requête prenant du temps à télécharger][ImageSlowContentDownload]  

### Causes  

*   La connexion entre le client et le serveur est lente.  
*   Un grand nombre de contenus est en cours de téléchargement.  

### Correctifs  

*   Envisagez d’héberger votre contenu sur un réseau de distribution de contenu ou de modifier des fournisseurs d’hébergement.  
*   Envoyez moins d’octets en optimisant vos demandes.  

## Compétences de collaboration  

Vous rencontrez un problème réseau qui doit être ajouté à ce guide?  

*   Envoyez un tweet à [@EdgeDevTools][MicrosoftEdgeTweet].  
*   **Send Feedback** ![ ][ImageSendFeedbackIcon] Pour envoyer des commentaires ou des demandes de fonctionnalité, sélectionnez Envoyer des commentaires dans le devtools ou appuyez sur `Alt` + `Shift` + `I` \ (Windows \) ou `Option` + `Shift` + `I` \ (MacOS \).  
*   [Ouvrez un problème][WebFundamentalsIssue] dans le référentiel Samples docs.  

<!--   -->  



<!-- image links -->  

[ImageSendFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/smile-icon.msft.png  

[ImageStalled]: /microsoft-edge/devtools-guide-chromium/media/network-network-disabled-cache-resources-queue.msft.png "Figure 1: exemple d’une série mise en file d’attente ou bloquée dans le panneau réseau"  
[ImageSlowTimeToFirstByte]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-using-dial-up-profile.msft.png "Figure 2: exemple de requête avec un délai de première octet lent"  
[ImageSlowContentDownload]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-edge-devtools.msft.png "Figure 3: exemple de requête dont le téléchargement prend du temps"  

<!-- links -->  

[NetworkPerformance]: /microsoft-edge/devtools-guide-chromium/network/index "Examiner l’activité réseau dans Microsoft Edge DevTools"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Nouveau problème-MicrosoftDocs/Edge-développeur"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/issues) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Jonathan Garbee][JonathanGarbee] \ (Google Developer expertise pour Web Technology \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
