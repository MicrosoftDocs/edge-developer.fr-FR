---
description: Découvrez comment déboguer une extraction en arrière-plan, une synchronisation en arrière-plan, des notifications et des messages envoyés avec Microsoft Edge DevTools.
title: Déboguer les services en arrière-plan avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: df832ed2f56faf6412fd42bc080d8af7705d26d3
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230676"
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

# Déboguer les services en arrière-plan avec Microsoft Edge DevTools  

La section **services en arrière-plan** de Microsoft Edge devtools est une collection d’outils pour les API JavaScript qui permet à votre site Web d’envoyer et de recevoir des mises à jour même si votre site Web n’est pas ouvert sur votre site Web.  
Un service en arrière-plan est semblable au fonctionnement d’une [processus en arrière-plan] [WikiBackgroundProcess].  
Microsoft Edge DevTools considère que chacune des API suivantes est un service en arrière-plan:  

*   [Récupération en arrière-plan](#background-fetch)  
*   [Synchronisation en arrière-plan](#background-sync)  
*   [Notifications](#notifications)  
*   [Messages de type pousser](#push-messages)  
    
Microsoft Edge DevTools peut consigner les événements de service en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert.  
Cela peut vous aider à vous assurer que les événements sont envoyés et reçus comme prévu.  Vous pouvez également examiner les détails de chaque événement.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   Volet de **messagerie de type pousser**  
:::image-end:::  

## Récupération en arrière-plan  

L' **API FETCH en arrière-plan** permet à un **travailleur de service** de télécharger de manière fiable des ressources de grande taille, comme des films ou des podcasts, comme un service en arrière-plan.  Pour consigner l’événement FETCH en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert:  

<!--Todo: add background fetch api section when available -->  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez l’outil de l' **application** .  
1.  Ouvrir le volet **récupération en arrière-plan** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Volet récupération en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       Volet **récupération en arrière-plan**  
    :::image-end:::  
    
1.  Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).  
   Après avoir déclenché une activité de récupération en arrière-plan, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Journal des événements dans le volet récupération en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Journal des événements dans le volet **récupération en arrière-plan**  
    :::image-end:::  
    
1.  Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet récupération en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Afficher les détails d’un événement dans le volet **récupération en arrière-plan**  
    :::image-end:::  
    
## Synchronisation en arrière-plan  

L' **API de synchronisation en arrière-plan** permet à un **travailleur de service** hors connexion d’envoyer des données à un serveur dès qu’il a rétabli une connexion Internet fiable.  Pour consigner les événements de synchronisation en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:  

<!--Todo: add background sync api section when available -->  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez l’outil de l' **application** .  
1.  Ouvrir le volet de **synchronisation en arrière-plan** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Volet de synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       Volet de **synchronisation en arrière-plan**  
    :::image-end:::  
    
1.  Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).  
   Après avoir déclenché une activité de synchronisation en arrière-plan, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Journal des événements dans le volet synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Journal des événements dans le volet **synchronisation en arrière-plan**  
    :::image-end:::  
    
1.  Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Afficher les détails d’un événement dans le volet **synchronisation en arrière-plan**  
    :::image-end:::  
    
## Notifications  

Lorsque le **travailleur** d’un service a reçu un [message envoyé][MDNPush] par un serveur, le travailleur du service utilise l' [API notifications][MDNNotifications] pour afficher les données à un utilisateur.  Pour consigner les notifications pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez l’outil de l' **application** .  
1.  Ouvrez le volet **notifications** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Volet notifications" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       Volet **notifications**  
    :::image-end:::  
    
1.  Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).  
   Après avoir déclenché une activité de notification, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Journal des événements dans le volet notifications" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Journal des événements dans le volet **notifications**  
    :::image-end:::  
    
1.  Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet notifications" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Afficher les détails d’un événement dans le volet **notifications**  
    :::image-end:::  
    
## Messages de type pousser  

Pour afficher une notification de transmission à un utilisateur, un **ouvrier de services** doit d’abord utiliser l' [API du message de transmission][MDNPush] pour recevoir des données d’un serveur.  Lorsque le travailleur du service est prêt à afficher la notification, il utilise l' [API notifications][MDNNotifications].  Pour consigner les messages envoyés pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez l’outil de l' **application** .  
1.  Ouvrez le volet de **messagerie de transmission** .  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Ouvrir le volet de messagerie de transmission" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Ouvrir le volet de **messagerie de transmission**  
    :::image-end:::  
    
1.  Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).  
    Après avoir déclenché une activité de message, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Journal des événements dans le volet de messagerie de transmission" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Journal des événements dans le volet de **messagerie de transmission**  
    :::image-end:::  
    
1.  Cliquez sur un événement pour afficher les détails dans l’espace situé sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet de messagerie de transmission" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Afficher les détails d’un événement dans le volet de **messagerie de transmission**  
    :::image-end:::  
    
## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Outils de développement Microsoft Edge (chrome) Documents Microsoft"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "processus en arrière-plan-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  
[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
