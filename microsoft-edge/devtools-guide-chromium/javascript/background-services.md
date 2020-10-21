---
description: Découvrez comment déboguer une extraction en arrière-plan, une synchronisation en arrière-plan, des notifications et des messages envoyés avec Microsoft Edge DevTools.
title: Déboguer les services en arrière-plan avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: fb5e408eb261ae3b2145780a1d7d5566c4501936
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11124816"
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

# <span data-ttu-id="da8bf-104">Déboguer les services en arrière-plan avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="da8bf-104">Debug Background Services With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="da8bf-105">La section **services en arrière-plan** de Microsoft Edge devtools est une collection d’outils pour les API JavaScript qui permet à votre site Web d’envoyer et de recevoir des mises à jour même si votre site Web n’est pas ouvert sur votre site Web.</span><span class="sxs-lookup"><span data-stu-id="da8bf-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="da8bf-106">Un service en arrière-plan est semblable au fonctionnement d’une [processus en arrière-plan] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="da8bf-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="da8bf-107">Microsoft Edge DevTools considère que chacune des API suivantes est un service en arrière-plan:</span><span class="sxs-lookup"><span data-stu-id="da8bf-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="da8bf-108">Récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="da8bf-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="da8bf-109">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="da8bf-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="da8bf-110">Notifications</span><span class="sxs-lookup"><span data-stu-id="da8bf-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="da8bf-111">Messages de type pousser</span><span class="sxs-lookup"><span data-stu-id="da8bf-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="da8bf-112">Microsoft Edge DevTools peut consigner les événements de service en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="da8bf-112">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="da8bf-113">Cela peut vous aider à vous assurer que les événements sont envoyés et reçus comme prévu.</span><span class="sxs-lookup"><span data-stu-id="da8bf-113">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="da8bf-114">Vous pouvez également examiner les détails de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="da8bf-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="da8bf-116">Volet de **messagerie de type pousser**</span><span class="sxs-lookup"><span data-stu-id="da8bf-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="da8bf-117">Récupération en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="da8bf-117">Background Fetch</span></span>  

<span data-ttu-id="da8bf-118">L' **API FETCH en arrière-plan** permet à un **travailleur de service** de télécharger de manière fiable des ressources de grande taille, comme des films ou des podcasts, comme un service en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="da8bf-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="da8bf-119">Pour consigner l’événement FETCH en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert:</span><span class="sxs-lookup"><span data-stu-id="da8bf-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="da8bf-120">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="da8bf-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="da8bf-121">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="da8bf-122">Ouvrir le volet **récupération en arrière-plan** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-122">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="da8bf-124">Volet **récupération en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="da8bf-124">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-125">Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="da8bf-125">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="da8bf-126">Après avoir déclenché une activité de récupération en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="da8bf-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="da8bf-128">Journal des événements dans le volet **récupération en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="da8bf-128">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-129">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="da8bf-129">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="da8bf-131">Afficher les détails d’un événement dans le volet **récupération en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="da8bf-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="da8bf-132">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="da8bf-132">Background Sync</span></span>  

<span data-ttu-id="da8bf-133">L' **API de synchronisation en arrière-plan** permet à un **travailleur de service** hors connexion d’envoyer des données à un serveur dès qu’il a rétabli une connexion Internet fiable.</span><span class="sxs-lookup"><span data-stu-id="da8bf-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="da8bf-134">Pour consigner les événements de synchronisation en arrière-plan pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="da8bf-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="da8bf-135">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="da8bf-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="da8bf-136">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-136">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="da8bf-137">Ouvrir le volet de **synchronisation en arrière-plan** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="da8bf-139">Volet de **synchronisation en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="da8bf-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-140">Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="da8bf-140">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="da8bf-141">Après avoir déclenché une activité de synchronisation en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="da8bf-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="da8bf-143">Journal des événements dans le volet **synchronisation en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="da8bf-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-144">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="da8bf-144">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="da8bf-146">Afficher les détails d’un événement dans le volet **synchronisation en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="da8bf-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="da8bf-147">Notifications</span><span class="sxs-lookup"><span data-stu-id="da8bf-147">Notifications</span></span>  

<span data-ttu-id="da8bf-148">Lorsque le **travailleur** d’un service a reçu un [message envoyé][MDNPush] par un serveur, le travailleur du service utilise l' [API notifications][MDNNotifications] pour afficher les données à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="da8bf-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="da8bf-149">Pour consigner les notifications pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="da8bf-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="da8bf-150">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="da8bf-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="da8bf-151">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-151">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="da8bf-152">Ouvrez le volet **notifications** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="da8bf-154">Volet **notifications**</span><span class="sxs-lookup"><span data-stu-id="da8bf-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-155">Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="da8bf-155">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="da8bf-156">Après avoir déclenché une activité de notification, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="da8bf-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="da8bf-158">Journal des événements dans le volet **notifications**</span><span class="sxs-lookup"><span data-stu-id="da8bf-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-159">Cliquez sur un événement pour afficher ses détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="da8bf-159">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="da8bf-161">Afficher les détails d’un événement dans le volet **notifications**</span><span class="sxs-lookup"><span data-stu-id="da8bf-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="da8bf-162">Messages de type pousser</span><span class="sxs-lookup"><span data-stu-id="da8bf-162">Push Messages</span></span>  

<span data-ttu-id="da8bf-163">Pour afficher une notification de transmission à un utilisateur, un **ouvrier de services** doit d’abord utiliser l' [API du message de transmission][MDNPush] pour recevoir des données d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="da8bf-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="da8bf-164">Lorsque le travailleur du service est prêt à afficher la notification, il utilise l' [API notifications][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="da8bf-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="da8bf-165">Pour consigner les messages envoyés pendant 3 jours, même si DevTools n’est pas ouvert, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="da8bf-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="da8bf-166">[Ouvrez devtools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="da8bf-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="da8bf-167">Ouvrez le volet de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-167">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="da8bf-168">Ouvrez le volet de **messagerie de transmission** .</span><span class="sxs-lookup"><span data-stu-id="da8bf-168">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="da8bf-170">Ouvrir le volet de **messagerie de transmission**</span><span class="sxs-lookup"><span data-stu-id="da8bf-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-171">Cliquez sur **Enregistrer** \ ( ![ enregistrement ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="da8bf-171">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="da8bf-172">Après avoir déclenché une activité de message, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="da8bf-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="da8bf-174">Journal des événements dans le volet de **messagerie de transmission**</span><span class="sxs-lookup"><span data-stu-id="da8bf-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="da8bf-175">Cliquez sur un événement pour afficher les détails dans l’espace situé sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="da8bf-175">Click an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Volet de messagerie de type pousser" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="da8bf-177">Afficher les détails d’un événement dans le volet de **messagerie de transmission**</span><span class="sxs-lookup"><span data-stu-id="da8bf-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="da8bf-178">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="da8bf-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

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
> <span data-ttu-id="da8bf-183">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="da8bf-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="da8bf-184">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="da8bf-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="da8bf-186">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="da8bf-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
