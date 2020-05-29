---
title: Déboguer les services en arrière-plan avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 0ac2a057307a939069cbb3b48ecd38c9de71e5db
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581830"
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

> ##### Figure1  
> Affichage des détails d’un événement dans le volet de messagerie de transmission  
> ![Affichage des détails d’un événement dans le volet de messagerie de transmission][PushDetails]  

## Récupération en arrière-plan   

L' *API FETCH en arrière-plan*permet à un **ouvrier de service** de télécharger de manière fiable des ressources de grande taille, comme des films ou des podcasts, comme service en arrière-plan.  Pour consigner l’événement FETCH en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert:  

<!--Todo: add background fetch api section when available -->  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez le volet de l' **application** .  
1.  Ouvrir le volet **récupération en arrière-plan** .  
    
    > ##### Figure 2  
    > Volet récupération en arrière-plan  
    > ![Volet récupération en arrière-plan][FetchEmpty]  
    
1.  Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .  
   Après avoir déclenché une activité de récupération en arrière-plan, DevTools enregistre les événements dans la table.  
    
    > ##### Figure3  
    > Journal des événements dans le volet récupération en arrière-plan  
    > ![Journal des événements dans le volet récupération en arrière-plan][FetchLog]  
    
1.  Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.  
    
    > ##### Figure 4  
    > Affichage des détails d’un événement dans le volet récupération en arrière-plan  
    > ![Affichage des détails d’un événement dans le volet récupération en arrière-plan][FetchDetails]  

## Synchronisation en arrière-plan   

L' **API de synchronisation en arrière-plan** permet à un **travailleur de service** hors connexion d’envoyer des données à un serveur dès qu’il a rétabli une connexion Internet fiable.  Pour consigner les événements de synchronisation en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:  

<!--Todo: add background sync api section when available -->  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez le volet de l' **application** .  
1.  Ouvrir le volet de **synchronisation en arrière-plan** .  
    
    > ##### Figure 5  
    > Volet de synchronisation en arrière-plan  
    > ![Volet de synchronisation en arrière-plan][SyncEmpty]  
    
1.  Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .  
   Après avoir déclenché une activité de synchronisation en arrière-plan, DevTools enregistre les événements dans la table.  
    
    > ##### Figure 6  
    > Journal des événements dans le volet synchronisation en arrière-plan  
    > ![Journal des événements dans le volet synchronisation en arrière-plan][SyncLog]  
    
1.  Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.  
    
    > ##### Figure 7  
    > Affichage des détails d’un événement dans le volet synchronisation en arrière-plan  
    > ![Affichage des détails d’un événement dans le volet synchronisation en arrière-plan][SyncDetails]  
    
## Notifications 

Lorsque le **travailleur** d’un service a reçu un [message envoyé][MDNPush] par un serveur, le travailleur du service utilise l' [API notifications][MDNNotifications] pour afficher les données à un utilisateur.  Pour consigner les notifications pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez le volet de l' **application** .  
1.  Ouvrez le volet **notifications** .  
    
    > ##### Figure8  
    > Volet notifications  
    > ![Volet notifications][NotificationsEmpty]  
    
1.  Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .  
   Après avoir déclenché une activité de notification, DevTools enregistre les événements dans la table.  
    
    > ##### Figure9  
    > Journal des événements dans le volet notifications  
    > ![Journal des événements dans le volet notifications][NotificationsLog]  
    
1.  Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.  
    
    > ##### Figure10  
    > Affichage des détails d’un événement dans le volet notifications  
    > ![Affichage des détails d’un événement dans le volet notifications][NotificationsDetails]  
    
## Messages de type pousser 

Pour afficher une notification de transmission à un utilisateur, un **ouvrier de services** doit d’abord utiliser l' [API du message de transmission][MDNPush] pour recevoir des données d’un serveur.  Lorsque le travailleur du service est prêt à afficher la notification, il utilise l' [API notifications][MDNNotifications].  Pour consigner les messages envoyés pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:  

1.  [Ouvrez devtools][OpenDevTools].  
1.  Ouvrez le volet de l' **application** .  
1.  Ouvrez le volet de **messagerie de transmission** .  
    
    > ##### Figure11  
    > Volet de messagerie de type pousser  
    > ![Volet de messagerie de type pousser][PushEmpty]  

1.  Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .  
    Après avoir déclenché une activité de message, DevTools enregistre les événements dans la table.  
    
    > ##### Figure12  
    > Journal des événements dans le volet de messagerie de transmission  
    > ![Journal des événements dans le volet de messagerie de transmission][PushLog]  

1.  Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.  
    
    > ##### Figure13  
    > Affichage des détails d’un événement dans le volet de messagerie de transmission  
    > ![Affichage des détails d’un événement dans le volet de messagerie de transmission][PushDetails2]  
    
 



<!-- image links -->  

[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[PushDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Figure 1: affichage des détails d’un événement dans le volet de messagerie de transmission"  
[FetchEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-empty.msft.png "Figure 2: volet récupération en arrière-plan"  
[FetchLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch.msft.png "Figure 3: journal des événements dans le volet récupération en arrière-plan"  
[FetchDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-details.msft.png "Figure 4: affichage des détails d’un événement dans le volet récupération en arrière-plan"  
[SyncEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-empty.msft.png "Figure 5: volet de synchronisation en arrière-plan"  
[SyncLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync.msft.png "Figure 6: journal des événements dans le volet synchronisation en arrière-plan"  
[SyncDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-details.msft.png "Figure 7: affichage des détails d’un événement dans le volet synchronisation en arrière-plan"  
[NotificationsEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-empty.msft.png "Figure 8: volet notifications"  
[NotificationsLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications.msft.png "Figure 9: journal des événements dans le volet notifications"  
[NotificationsDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-details.msft.png "Figure 10: affichage des détails d’un événement dans le volet notifications"  
[PushEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-empty.msft.png "Figure 11: volet de messagerie de transmission"  
[PushLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Figure 12: journal des événements dans le volet de messagerie de transmission"  
[PushDetails2]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-details.msft.png "Figure 13: affichage des détails d’un événement dans le volet de messagerie de transmission"  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Outils de développement Microsoft Edge (chrome) ouverts"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "processus en arrière-plan-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  
[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
