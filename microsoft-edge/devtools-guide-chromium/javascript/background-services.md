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





# <span data-ttu-id="6cd07-103">Déboguer les services en arrière-plan avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6cd07-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="6cd07-104">La section **services en arrière-plan** de Microsoft Edge devtools est une collection d’outils pour les API JavaScript qui permet à votre site Web d’envoyer et de recevoir des mises à jour même si votre site Web n’est pas ouvert sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="6cd07-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="6cd07-105">Un service en arrière-plan est semblable au fonctionnement d’une [processus en arrière-plan] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="6cd07-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="6cd07-106">Microsoft Edge DevTools considère que chacune des API suivantes est un service en arrière-plan:</span><span class="sxs-lookup"><span data-stu-id="6cd07-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="6cd07-107">Récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="6cd07-108">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="6cd07-109">Notifications</span><span class="sxs-lookup"><span data-stu-id="6cd07-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="6cd07-110">Messages de type pousser</span><span class="sxs-lookup"><span data-stu-id="6cd07-110">Push Messages</span></span>](#push-messages)  

<span data-ttu-id="6cd07-111">Microsoft Edge DevTools peut consigner les événements de service en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="6cd07-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="6cd07-112">Cela peut vous aider à vous assurer que les événements sont envoyés et reçus comme prévu.</span><span class="sxs-lookup"><span data-stu-id="6cd07-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="6cd07-113">Vous pouvez également examiner les détails de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="6cd07-113">You can also inspect the details of each event.</span></span>  

> ##### <span data-ttu-id="6cd07-114">Figure1</span><span class="sxs-lookup"><span data-stu-id="6cd07-114">Figure 1</span></span>  
> <span data-ttu-id="6cd07-115">Affichage des détails d’un événement dans le volet de messagerie de transmission</span><span class="sxs-lookup"><span data-stu-id="6cd07-115">Viewing the details of an event in the Push Messaging pane</span></span>  
> ![Affichage des détails d’un événement dans le volet de messagerie de transmission][PushDetails]  

## <span data-ttu-id="6cd07-117">Récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-117">Background Fetch</span></span>   

<span data-ttu-id="6cd07-118">L' *API FETCH en arrière-plan*permet à un **ouvrier de service** de télécharger de manière fiable des ressources de grande taille, comme des films ou des podcasts, comme service en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="6cd07-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="6cd07-119">Pour consigner l’événement FETCH en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert:</span><span class="sxs-lookup"><span data-stu-id="6cd07-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="6cd07-120">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="6cd07-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6cd07-121">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="6cd07-122">Ouvrir le volet **récupération en arrière-plan** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-122">Open the **Background Fetch** pane.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-123">Figure 2</span><span class="sxs-lookup"><span data-stu-id="6cd07-123">Figure 2</span></span>  
    > <span data-ttu-id="6cd07-124">Volet récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-124">The Background Fetch pane</span></span>  
    > ![Volet récupération en arrière-plan][FetchEmpty]  
    
1.  <span data-ttu-id="6cd07-126">Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="6cd07-126">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="6cd07-127">Après avoir déclenché une activité de récupération en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="6cd07-127">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-128">Figure3</span><span class="sxs-lookup"><span data-stu-id="6cd07-128">Figure 3</span></span>  
    > <span data-ttu-id="6cd07-129">Journal des événements dans le volet récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-129">A log of events in the Background Fetch pane</span></span>  
    > ![Journal des événements dans le volet récupération en arrière-plan][FetchLog]  
    
1.  <span data-ttu-id="6cd07-131">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="6cd07-131">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-132">Figure 4</span><span class="sxs-lookup"><span data-stu-id="6cd07-132">Figure 4</span></span>  
    > <span data-ttu-id="6cd07-133">Affichage des détails d’un événement dans le volet récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-133">Viewing the details of an event in the Background Fetch pane</span></span>  
    > ![Affichage des détails d’un événement dans le volet récupération en arrière-plan][FetchDetails]  

## <span data-ttu-id="6cd07-135">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-135">Background Sync</span></span>   

<span data-ttu-id="6cd07-136">L' **API de synchronisation en arrière-plan** permet à un **travailleur de service** hors connexion d’envoyer des données à un serveur dès qu’il a rétabli une connexion Internet fiable.</span><span class="sxs-lookup"><span data-stu-id="6cd07-136">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="6cd07-137">Pour consigner les événements de synchronisation en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="6cd07-137">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="6cd07-138">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="6cd07-138">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6cd07-139">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-139">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="6cd07-140">Ouvrir le volet de **synchronisation en arrière-plan** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-140">Open the **Background Sync** pane.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-141">Figure 5</span><span class="sxs-lookup"><span data-stu-id="6cd07-141">Figure 5</span></span>  
    > <span data-ttu-id="6cd07-142">Volet de synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-142">The Background Sync pane</span></span>  
    > ![Volet de synchronisation en arrière-plan][SyncEmpty]  
    
1.  <span data-ttu-id="6cd07-144">Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="6cd07-144">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="6cd07-145">Après avoir déclenché une activité de synchronisation en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="6cd07-145">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-146">Figure 6</span><span class="sxs-lookup"><span data-stu-id="6cd07-146">Figure 6</span></span>  
    > <span data-ttu-id="6cd07-147">Journal des événements dans le volet synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-147">A log of events in the Background Sync pane</span></span>  
    > ![Journal des événements dans le volet synchronisation en arrière-plan][SyncLog]  
    
1.  <span data-ttu-id="6cd07-149">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="6cd07-149">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-150">Figure 7</span><span class="sxs-lookup"><span data-stu-id="6cd07-150">Figure 7</span></span>  
    > <span data-ttu-id="6cd07-151">Affichage des détails d’un événement dans le volet synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="6cd07-151">Viewing the details of an event in the Background Sync pane</span></span>  
    > ![Affichage des détails d’un événement dans le volet synchronisation en arrière-plan][SyncDetails]  
    
## <span data-ttu-id="6cd07-153">Notifications</span><span class="sxs-lookup"><span data-stu-id="6cd07-153">Notifications</span></span> 

<span data-ttu-id="6cd07-154">Lorsque le **travailleur** d’un service a reçu un [message envoyé][MDNPush] par un serveur, le travailleur du service utilise l' [API notifications][MDNNotifications] pour afficher les données à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6cd07-154">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="6cd07-155">Pour consigner les notifications pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="6cd07-155">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="6cd07-156">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="6cd07-156">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6cd07-157">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-157">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="6cd07-158">Ouvrez le volet **notifications** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-158">Open the **Notifications** pane.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-159">Figure8</span><span class="sxs-lookup"><span data-stu-id="6cd07-159">Figure 8</span></span>  
    > <span data-ttu-id="6cd07-160">Volet notifications</span><span class="sxs-lookup"><span data-stu-id="6cd07-160">The Notifications pane</span></span>  
    > ![Volet notifications][NotificationsEmpty]  
    
1.  <span data-ttu-id="6cd07-162">Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="6cd07-162">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="6cd07-163">Après avoir déclenché une activité de notification, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="6cd07-163">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-164">Figure9</span><span class="sxs-lookup"><span data-stu-id="6cd07-164">Figure 9</span></span>  
    > <span data-ttu-id="6cd07-165">Journal des événements dans le volet notifications</span><span class="sxs-lookup"><span data-stu-id="6cd07-165">A log of events in the Notifications pane</span></span>  
    > ![Journal des événements dans le volet notifications][NotificationsLog]  
    
1.  <span data-ttu-id="6cd07-167">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="6cd07-167">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-168">Figure10</span><span class="sxs-lookup"><span data-stu-id="6cd07-168">Figure 10</span></span>  
    > <span data-ttu-id="6cd07-169">Affichage des détails d’un événement dans le volet notifications</span><span class="sxs-lookup"><span data-stu-id="6cd07-169">Viewing the details of an event in the Notifications pane</span></span>  
    > ![Affichage des détails d’un événement dans le volet notifications][NotificationsDetails]  
    
## <span data-ttu-id="6cd07-171">Messages de type pousser</span><span class="sxs-lookup"><span data-stu-id="6cd07-171">Push Messages</span></span> 

<span data-ttu-id="6cd07-172">Pour afficher une notification de transmission à un utilisateur, un **ouvrier de services** doit d’abord utiliser l' [API du message de transmission][MDNPush] pour recevoir des données d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="6cd07-172">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="6cd07-173">Lorsque le travailleur du service est prêt à afficher la notification, il utilise l' [API notifications][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="6cd07-173">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="6cd07-174">Pour consigner les messages envoyés pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="6cd07-174">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="6cd07-175">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="6cd07-175">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="6cd07-176">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-176">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="6cd07-177">Ouvrez le volet de **messagerie de transmission** .</span><span class="sxs-lookup"><span data-stu-id="6cd07-177">Open the **Push Messaging** pane.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-178">Figure11</span><span class="sxs-lookup"><span data-stu-id="6cd07-178">Figure 11</span></span>  
    > <span data-ttu-id="6cd07-179">Volet de messagerie de type pousser</span><span class="sxs-lookup"><span data-stu-id="6cd07-179">The Push Messaging pane</span></span>  
    > ![Volet de messagerie de type pousser][PushEmpty]  

1.  <span data-ttu-id="6cd07-181">Cliquez sur **Enregistrer** l' ![ enregistrement ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="6cd07-181">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="6cd07-182">Après avoir déclenché une activité de message, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="6cd07-182">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-183">Figure12</span><span class="sxs-lookup"><span data-stu-id="6cd07-183">Figure 12</span></span>  
    > <span data-ttu-id="6cd07-184">Journal des événements dans le volet de messagerie de transmission</span><span class="sxs-lookup"><span data-stu-id="6cd07-184">A log of events in the Push Messaging pane</span></span>  
    > ![Journal des événements dans le volet de messagerie de transmission][PushLog]  

1.  <span data-ttu-id="6cd07-186">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="6cd07-186">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="6cd07-187">Figure13</span><span class="sxs-lookup"><span data-stu-id="6cd07-187">Figure 13</span></span>  
    > <span data-ttu-id="6cd07-188">Affichage des détails d’un événement dans le volet de messagerie de transmission</span><span class="sxs-lookup"><span data-stu-id="6cd07-188">Viewing the details of an event in the Push Messaging pane</span></span>  
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
> <span data-ttu-id="6cd07-207">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6cd07-207">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="6cd07-208">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="6cd07-208">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="6cd07-210">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="6cd07-210">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
