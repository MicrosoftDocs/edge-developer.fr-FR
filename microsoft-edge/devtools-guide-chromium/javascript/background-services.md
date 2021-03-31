---
description: Comment déboguer la récupération en arrière-plan, la synchronisation en arrière-plan, les notifications et les messages Push avec Microsoft Edge DevTools.
title: Débogage des services d’arrière-plan avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 15023098c547d31bf46bd387f849b365c13b38f6
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439527"
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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a>Débogage des services d’arrière-plan avec Microsoft Edge DevTools  

La **section** Services d’arrière-plan de Microsoft Edge DevTools est une collection d’outils pour les API JavaScript qui permet à votre site web d’envoyer et de recevoir des mises à jour même lorsqu’un utilisateur n’a pas votre site web ouvert.  
Un service en arrière-plan est fonctionnellement similaire à un [processus en arrière-plan][WikiBackgroundProcess].  
Microsoft Edge DevTools considère chacune des API suivantes comme un service d’arrière-plan :  

*   [Extraction en arrière-plan](#background-fetch)  
*   [Synchronisation en arrière-plan](#background-sync)  
*   [Notifications](#notifications)  
*   [Push Messages](#push-messages)  
    
Microsoft Edge DevTools peut enregistrer des événements de service en arrière-plan pendant 3 jours, même lorsque DevTools n’est pas ouvert.  
Le journal des événements du service en arrière-plan peut vous aider à vous assurer que les événements sont envoyés et reçus comme prévu.  Vous pouvez également examiner les détails de chaque événement.  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   Volet **De messagerie** push  
:::image-end:::  

## <a name="background-fetch"></a>Extraction en arrière-plan  

**L’API d’extraction en** arrière-plan permet à un **service de** travail de télécharger de manière fiable de grandes ressources, telles que des films ou des podcasts, en tant que service d’arrière-plan.  Pour enregistrer l’événement Background Fetch pendant 3 jours, même lorsque DevTools n’est pas ouvert :  

<!--Todo: add background fetch api section when available -->  

1.  [Ouvrez DevTools][OpenDevTools].  
1.  Ouvrez **l’outil Application.**  
1.  Ouvrez le **panneau Extraction en arrière-plan.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Panneau Extraction en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       Panneau **Extraction en arrière-plan**  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ](../media/record-icon.msft.png) \).  
   Après avoir déclenché une activité de récupération en arrière-plan, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Journal des événements dans le panneau Extraction en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       Journal des événements dans le **panneau Extraction en arrière-plan**  
    :::image-end:::  
    
1.  Choisissez un événement pour afficher ses détails dans l’espace sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet Extraction en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       Afficher les détails d’un événement dans le **volet Extraction** en arrière-plan  
    :::image-end:::  
    
## <a name="background-sync"></a>Synchronisation en arrière-plan  

**L’API de synchronisation** en **** arrière-plan permet à un service de travail hors connexion d’envoyer des données à un serveur une fois qu’il a rétabli une connexion Internet fiable.  Pour enregistrer les événements de synchronisation en arrière-plan pendant 3 jours, même lorsque DevTools n’est pas ouvert :  

<!--Todo: add background sync api section when available -->  

1.  [Ouvrez DevTools][OpenDevTools].  
1.  Ouvrez **l’outil Application.**  
1.  Ouvrez le **volet Synchronisation** en arrière-plan.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Volet Synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       Volet **Synchronisation en** arrière-plan  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ](../media/record-icon.msft.png) \).  
   Après avoir déclenché une activité de synchronisation en arrière-plan, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Journal des événements dans le volet Synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       Journal des événements dans le volet **Synchronisation** en arrière-plan  
    :::image-end:::  
    
1.  Choisissez un événement pour afficher ses détails dans l’espace sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet Synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       Afficher les détails d’un événement dans **le** volet Synchronisation en arrière-plan  
    :::image-end:::  
    
## <a name="notifications"></a>Notifications  

Une fois **qu’un employé** de service a reçu un [message push][MDNPush] d’un serveur, il utilise l’API [Notifications][MDNNotifications] pour afficher les données à un utilisateur.  Pour enregistrer les notifications pendant 3 jours, même lorsque DevTools n’est pas ouvert :  

1.  [Ouvrez DevTools][OpenDevTools].  
1.  Ouvrez **l’outil Application.**  
1.  Ouvrez **le volet Notifications.**  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Volet Notifications" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       Volet **Notifications**  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ](../media/record-icon.msft.png) \).  
   Après avoir déclenché une activité Notifications, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Journal des événements dans le volet Notifications" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       Journal des événements dans le **volet Notifications**  
    :::image-end:::  
    
1.  Choisissez un événement pour afficher ses détails dans l’espace sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet Notifications" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       Afficher les détails d’un événement dans le **volet Notifications**  
    :::image-end:::  
    
## <a name="push-messages"></a>Push Messages  

Pour afficher une notification Push **** à un utilisateur, un service de travail doit d’abord utiliser l’API Push [Message][MDNPush] pour recevoir des données à partir d’un serveur.  Lorsque le service de travail est prêt à afficher la notification, il utilise [l’API Notifications.][MDNNotifications]  Pour enregistrer les messages push pendant 3 jours, même lorsque DevTools n’est pas ouvert :  

1.  [Ouvrez DevTools][OpenDevTools].  
1.  Ouvrez **l’outil Application.**  
1.  Ouvrez **le panneau De messagerie** push.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Ouvrir le volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       Ouvrir le **volet De messagerie** push  
    :::image-end:::  
    
1.  Choose **Record** \( ![ Record ](../media/record-icon.msft.png) \).  
    Après avoir déclenché une activité de message push, DevTools enregistre les événements dans la table.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Journal des événements dans le volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       Journal des événements dans le **volet De messagerie** push  
    :::image-end:::  
    
1.  Choisissez un événement pour afficher les détails dans l’espace sous le tableau.  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       Afficher les détails d’un événement dans le **volet De messagerie** push  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Ouvrez les outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notifications API | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Api Push | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process «Processus en arrière-plan - Wikipedia»  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  
[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
