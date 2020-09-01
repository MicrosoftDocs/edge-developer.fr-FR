---
title: Déboguer les services en arrière-plan avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1fecd6f9c1dceb39482bf8c4ade71918e32dec00
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983275"
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





# <span data-ttu-id="ddc92-103">Déboguer les services en arrière-plan avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ddc92-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="ddc92-104">La section **services en arrière-plan** de Microsoft Edge devtools est une collection d’outils pour les API JavaScript qui permet à votre site Web d’envoyer et de recevoir des mises à jour même si votre site Web n’est pas ouvert sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="ddc92-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="ddc92-105">Un service en arrière-plan est semblable au fonctionnement d’une [processus en arrière-plan] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="ddc92-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="ddc92-106">Microsoft Edge DevTools considère que chacune des API suivantes est un service en arrière-plan:</span><span class="sxs-lookup"><span data-stu-id="ddc92-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="ddc92-107">Récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="ddc92-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="ddc92-108">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="ddc92-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="ddc92-109">Notifications</span><span class="sxs-lookup"><span data-stu-id="ddc92-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="ddc92-110">Messages de type pousser</span><span class="sxs-lookup"><span data-stu-id="ddc92-110">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="ddc92-111">Microsoft Edge DevTools peut consigner les événements de service en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="ddc92-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="ddc92-112">Cela peut vous aider à vous assurer que les événements sont envoyés et reçus comme prévu.</span><span class="sxs-lookup"><span data-stu-id="ddc92-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="ddc92-113">Vous pouvez également examiner les détails de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="ddc92-113">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Afficher les détails d’un événement dans le volet de messagerie de transmission" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="ddc92-115">Afficher les détails d’un événement dans le volet de **messagerie de transmission**</span><span class="sxs-lookup"><span data-stu-id="ddc92-115">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="ddc92-116">Récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="ddc92-116">Background Fetch</span></span>   

<span data-ttu-id="ddc92-117">L' *API FETCH en arrière-plan*permet à un **ouvrier de service** de télécharger de manière fiable des ressources de grande taille, comme des films ou des podcasts, comme service en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="ddc92-117">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="ddc92-118">Pour consigner l’événement FETCH en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert:</span><span class="sxs-lookup"><span data-stu-id="ddc92-118">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="ddc92-119">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="ddc92-119">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="ddc92-120">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-120">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="ddc92-121">Ouvrir le volet **récupération en arrière-plan** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-121">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Volet récupération en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="ddc92-123">Volet **récupération en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="ddc92-123">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-124">Cliquez sur **Enregistrer** \ ( ![ Enregistrer ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ddc92-124">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="ddc92-125">Après avoir déclenché une activité de récupération en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="ddc92-125">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Journal des événements dans le volet récupération en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="ddc92-127">Journal des événements dans le volet **récupération en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="ddc92-127">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-128">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="ddc92-128">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet récupération en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="ddc92-130">Afficher les détails d’un événement dans le volet **récupération en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="ddc92-130">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ddc92-131">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="ddc92-131">Background Sync</span></span>   

<span data-ttu-id="ddc92-132">L' **API de synchronisation en arrière-plan** permet à un **travailleur de service** hors connexion d’envoyer des données à un serveur dès qu’il a rétabli une connexion Internet fiable.</span><span class="sxs-lookup"><span data-stu-id="ddc92-132">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="ddc92-133">Pour consigner les événements de synchronisation en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ddc92-133">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="ddc92-134">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="ddc92-134">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="ddc92-135">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-135">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="ddc92-136">Ouvrir le volet de **synchronisation en arrière-plan** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-136">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Volet de synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="ddc92-138">Volet de **synchronisation en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="ddc92-138">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-139">Cliquez sur **Enregistrer** \ ( ![ Enregistrer ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ddc92-139">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="ddc92-140">Après avoir déclenché une activité de synchronisation en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="ddc92-140">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Journal des événements dans le volet synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="ddc92-142">Journal des événements dans le volet **synchronisation en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="ddc92-142">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-143">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="ddc92-143">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="ddc92-145">Afficher les détails d’un événement dans le volet **synchronisation en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="ddc92-145">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ddc92-146">Notifications</span><span class="sxs-lookup"><span data-stu-id="ddc92-146">Notifications</span></span> 

<span data-ttu-id="ddc92-147">Lorsque le **travailleur** d’un service a reçu un [message envoyé][MDNPush] par un serveur, le travailleur du service utilise l' [API notifications][MDNNotifications] pour afficher les données à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ddc92-147">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="ddc92-148">Pour consigner les notifications pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ddc92-148">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="ddc92-149">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="ddc92-149">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="ddc92-150">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-150">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="ddc92-151">Ouvrez le volet **notifications** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-151">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Volet notifications" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="ddc92-153">Volet **notifications**</span><span class="sxs-lookup"><span data-stu-id="ddc92-153">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-154">Cliquez sur **Enregistrer** \ ( ![ Enregistrer ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ddc92-154">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="ddc92-155">Après avoir déclenché une activité de notification, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="ddc92-155">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Journal des événements dans le volet notifications" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="ddc92-157">Journal des événements dans le volet **notifications**</span><span class="sxs-lookup"><span data-stu-id="ddc92-157">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-158">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="ddc92-158">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet notifications" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="ddc92-160">Afficher les détails d’un événement dans le volet **notifications**</span><span class="sxs-lookup"><span data-stu-id="ddc92-160">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="ddc92-161">Messages de type pousser</span><span class="sxs-lookup"><span data-stu-id="ddc92-161">Push Messages</span></span> 

<span data-ttu-id="ddc92-162">Pour afficher une notification de transmission à un utilisateur, un **ouvrier de services** doit d’abord utiliser l' [API du message de transmission][MDNPush] pour recevoir des données d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="ddc92-162">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="ddc92-163">Lorsque le travailleur du service est prêt à afficher la notification, il utilise l' [API notifications][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="ddc92-163">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="ddc92-164">Pour consigner les messages envoyés pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="ddc92-164">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="ddc92-165">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="ddc92-165">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="ddc92-166">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-166">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="ddc92-167">Ouvrez le volet de **messagerie de transmission** .</span><span class="sxs-lookup"><span data-stu-id="ddc92-167">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="ddc92-169">Volet de **messagerie de type pousser**</span><span class="sxs-lookup"><span data-stu-id="ddc92-169">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-170">Cliquez sur **Enregistrer** \ ( ![ Enregistrer ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="ddc92-170">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="ddc92-171">Après avoir déclenché une activité de message, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="ddc92-171">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Journal des événements dans le volet de messagerie de transmission" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="ddc92-173">Journal des événements dans le volet de **messagerie de transmission**</span><span class="sxs-lookup"><span data-stu-id="ddc92-173">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="ddc92-174">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="ddc92-174">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet de messagerie de transmission" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="ddc92-176">Afficher les détails d’un événement dans le volet de **messagerie de transmission**</span><span class="sxs-lookup"><span data-stu-id="ddc92-176">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Outils de développement Microsoft Edge (chrome) Documents Microsoft"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API notifications | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API de type pousser | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "processus en arrière-plan-Wikipédia"  

> [!NOTE]
> <span data-ttu-id="ddc92-181">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ddc92-181">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ddc92-182">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="ddc92-182">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="ddc92-184">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ddc92-184">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
