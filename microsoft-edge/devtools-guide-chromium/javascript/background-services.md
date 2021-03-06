---
description: Comment déboguer la récupération en arrière-plan, la synchronisation en arrière-plan, les notifications et les messages Push avec Microsoft Edge DevTools.
title: Débogage des services d’arrière-plan avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: cf3459e7b5f80a695a855ffdd0c249c2bc223d31
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11398636"
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

# <a name="debug-background-services-with-microsoft-edge-devtools"></a><span data-ttu-id="15a67-104">Débogage des services d’arrière-plan avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="15a67-104">Debug Background Services with Microsoft Edge DevTools</span></span>  

<span data-ttu-id="15a67-105">La **section** Services d’arrière-plan de Microsoft Edge DevTools est une collection d’outils pour les API JavaScript qui permet à votre site web d’envoyer et de recevoir des mises à jour même lorsqu’un utilisateur n’a pas votre site web ouvert.</span><span class="sxs-lookup"><span data-stu-id="15a67-105">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="15a67-106">Un service en arrière-plan est fonctionnellement similaire à un [processus en arrière-plan][WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="15a67-106">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="15a67-107">Microsoft Edge DevTools considère chacune des API suivantes comme un service d’arrière-plan :</span><span class="sxs-lookup"><span data-stu-id="15a67-107">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="15a67-108">Extraction en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="15a67-108">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="15a67-109">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="15a67-109">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="15a67-110">Notifications</span><span class="sxs-lookup"><span data-stu-id="15a67-110">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="15a67-111">Push Messages</span><span class="sxs-lookup"><span data-stu-id="15a67-111">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="15a67-112">Microsoft Edge DevTools peut enregistrer des événements de service en arrière-plan pendant 3 jours, même lorsque DevTools n’est pas ouvert.</span><span class="sxs-lookup"><span data-stu-id="15a67-112">Microsoft Edge DevTools may log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="15a67-113">Le journal des événements du service en arrière-plan peut vous aider à vous assurer que les événements sont envoyés et reçus comme prévu.</span><span class="sxs-lookup"><span data-stu-id="15a67-113">The background service events log may help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="15a67-114">Vous pouvez également examiner les détails de chaque événement.</span><span class="sxs-lookup"><span data-stu-id="15a67-114">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="15a67-116">Volet **De messagerie** push</span><span class="sxs-lookup"><span data-stu-id="15a67-116">The **Push Messaging** pane</span></span>  
:::image-end:::  

## <a name="background-fetch"></a><span data-ttu-id="15a67-117">Extraction en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="15a67-117">Background Fetch</span></span>  

<span data-ttu-id="15a67-118">**L’API d’extraction en** arrière-plan permet à un **service de** travail de télécharger de manière fiable de grandes ressources, telles que des films ou des podcasts, en tant que service d’arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="15a67-118">The **Background Fetch API** enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="15a67-119">Pour enregistrer l’événement Background Fetch pendant 3 jours, même lorsque DevTools n’est pas ouvert :</span><span class="sxs-lookup"><span data-stu-id="15a67-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="15a67-120">[Ouvrez DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="15a67-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="15a67-121">Ouvrez **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="15a67-121">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="15a67-122">Ouvrez le **panneau Extraction en arrière-plan.**</span><span class="sxs-lookup"><span data-stu-id="15a67-122">Open the **Background Fetch** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Panneau Extraction en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="15a67-124">Panneau **Extraction d’arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="15a67-124">The **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-125">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="15a67-125">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="15a67-126">Après avoir déclenché une activité de récupération en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="15a67-126">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Journal des événements dans le panneau Extraction en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="15a67-128">Journal des événements dans le panneau Extraction en **arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="15a67-128">A log of events in the **Background Fetch** panel</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-129">Choisissez un événement pour afficher ses détails dans l’espace sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="15a67-129">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet Extraction en arrière-plan" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="15a67-131">Afficher les détails d’un événement dans le **volet Extraction** en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="15a67-131">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <a name="background-sync"></a><span data-ttu-id="15a67-132">Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="15a67-132">Background Sync</span></span>  

<span data-ttu-id="15a67-133">**L’API de synchronisation** en \*\*\*\* arrière-plan permet à un service de travail hors connexion d’envoyer des données à un serveur une fois qu’il a rétabli une connexion Internet fiable.</span><span class="sxs-lookup"><span data-stu-id="15a67-133">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="15a67-134">Pour enregistrer les événements de synchronisation en arrière-plan pendant 3 jours, même lorsque DevTools n’est pas ouvert :</span><span class="sxs-lookup"><span data-stu-id="15a67-134">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="15a67-135">[Ouvrez DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="15a67-135">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="15a67-136">Ouvrez **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="15a67-136">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="15a67-137">Ouvrez le **volet Synchronisation** en arrière-plan.</span><span class="sxs-lookup"><span data-stu-id="15a67-137">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Volet Synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="15a67-139">Volet **Synchronisation en arrière-plan**</span><span class="sxs-lookup"><span data-stu-id="15a67-139">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-140">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="15a67-140">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="15a67-141">Après avoir déclenché une activité de synchronisation en arrière-plan, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="15a67-141">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Journal des événements dans le volet Synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="15a67-143">Journal des événements dans le volet **Synchronisation** en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="15a67-143">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-144">Choisissez un événement pour afficher ses détails dans l’espace sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="15a67-144">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet Synchronisation en arrière-plan" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="15a67-146">Afficher les détails d’un événement dans **le** volet Synchronisation en arrière-plan</span><span class="sxs-lookup"><span data-stu-id="15a67-146">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <a name="notifications"></a><span data-ttu-id="15a67-147">Notifications</span><span class="sxs-lookup"><span data-stu-id="15a67-147">Notifications</span></span>  

<span data-ttu-id="15a67-148">Une fois **qu’un employé** de service a reçu un [message push][MDNPush] d’un serveur, il utilise l’API [Notifications][MDNNotifications] pour afficher les données à un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="15a67-148">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="15a67-149">Pour enregistrer les notifications pendant 3 jours, même lorsque DevTools n’est pas ouvert :</span><span class="sxs-lookup"><span data-stu-id="15a67-149">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="15a67-150">[Ouvrez DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="15a67-150">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="15a67-151">Ouvrez **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="15a67-151">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="15a67-152">Ouvrez **le volet Notifications.**</span><span class="sxs-lookup"><span data-stu-id="15a67-152">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Volet Notifications" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="15a67-154">Volet **Notifications**</span><span class="sxs-lookup"><span data-stu-id="15a67-154">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-155">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="15a67-155">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="15a67-156">Après avoir déclenché une activité Notifications, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="15a67-156">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Journal des événements dans le volet Notifications" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="15a67-158">Journal des événements dans le **volet Notifications**</span><span class="sxs-lookup"><span data-stu-id="15a67-158">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-159">Choisissez un événement pour afficher ses détails dans l’espace sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="15a67-159">Choose an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet Notifications" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="15a67-161">Afficher les détails d’un événement dans le **volet Notifications**</span><span class="sxs-lookup"><span data-stu-id="15a67-161">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <a name="push-messages"></a><span data-ttu-id="15a67-162">Push Messages</span><span class="sxs-lookup"><span data-stu-id="15a67-162">Push Messages</span></span>  

<span data-ttu-id="15a67-163">Pour afficher une notification Push \*\*\*\* à un utilisateur, un service de travail doit d’abord utiliser l’API Push [Message][MDNPush] pour recevoir des données à partir d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="15a67-163">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="15a67-164">Lorsque le service de travail est prêt à afficher la notification, il utilise [l’API Notifications][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="15a67-164">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="15a67-165">Pour enregistrer les messages push pendant 3 jours, même lorsque DevTools n’est pas ouvert :</span><span class="sxs-lookup"><span data-stu-id="15a67-165">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="15a67-166">[Ouvrez DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="15a67-166">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="15a67-167">Ouvrez **l’outil Application.**</span><span class="sxs-lookup"><span data-stu-id="15a67-167">Open the **Application** tool.</span></span>  
1.  <span data-ttu-id="15a67-168">Ouvrez **le panneau De messagerie** push.</span><span class="sxs-lookup"><span data-stu-id="15a67-168">Open the **Push Messaging** panel.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Ouvrir le volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="15a67-170">Ouvrir le **volet De messagerie** push</span><span class="sxs-lookup"><span data-stu-id="15a67-170">Open the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-171">Choose **Record** \( ![ Record ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="15a67-171">Choose **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="15a67-172">Après avoir déclenché une activité de message push, DevTools enregistre les événements dans la table.</span><span class="sxs-lookup"><span data-stu-id="15a67-172">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Journal des événements dans le volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="15a67-174">Journal des événements dans le **volet De messagerie** push</span><span class="sxs-lookup"><span data-stu-id="15a67-174">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="15a67-175">Choisissez un événement pour afficher les détails dans l’espace sous le tableau.</span><span class="sxs-lookup"><span data-stu-id="15a67-175">Choose an event to view the details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Afficher les détails d’un événement dans le volet De messagerie push" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="15a67-177">Afficher les détails d’un événement dans le **volet De messagerie** push</span><span class="sxs-lookup"><span data-stu-id="15a67-177">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="15a67-178">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="15a67-178">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open/index.md "Ouvrez les outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "Notifications API | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "Api Push | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process «Processus en arrière-plan - Wikipedia»  

> [!NOTE]
> <span data-ttu-id="15a67-183">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="15a67-183">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="15a67-184">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="15a67-184">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="15a67-186">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="15a67-186">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
