---
description: Fonctionnalités de débogage de grille CSS, demandes de modification et de relecture avec la console réseau, etc.
title: Nouveautés de DevTools (Microsoft Edge 85)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5bd013fae617e9759aa91949acccf936d85f7160
ms.sourcegitcommit: de75fda30bb8964e9a184228d068b4402ec59c3e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "11514360"
---
<!-- Copyright Jecelyn Yeen 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  
# <a name="whats-new-in-devtools-microsoft-edge-85"></a><span data-ttu-id="b0d58-104">Nouveautés de DevTools (Microsoft Edge 85)</span><span class="sxs-lookup"><span data-stu-id="b0d58-104">What's New In DevTools (Microsoft Edge 85)</span></span>  

## <a name="announcements-from-the-microsoft-edge-devtools-team"></a><span data-ttu-id="b0d58-105">Annonces de l'équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b0d58-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="b0d58-106">Les sections suivantes sont une liste des annonces que vous avez peut-être manquées de l'équipe Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0d58-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team.</span></span>  <span data-ttu-id="b0d58-107">Consultez les annonces pour essayer les nouvelles fonctionnalités des extensions DevTools, Microsoft Visual Studio Code, etc.</span><span class="sxs-lookup"><span data-stu-id="b0d58-107">Check out the announcements to try new features in the DevTools, Microsoft Visual Studio Code extensions, and more.</span></span>  <span data-ttu-id="b0d58-108">Pour rester à jour sur toutes les fonctionnalités les plus récentes et les plus importantes de vos outils de développement, téléchargez les canaux d'aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] et suivez l'équipe Microsoft [Edge DevTools][EdgeDevToolsTwitterAccount]sur Twitter.</span><span class="sxs-lookup"><span data-stu-id="b0d58-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow the Microsoft Edge DevTools team on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <a name="css-grid-debugging-features"></a><span data-ttu-id="b0d58-109">Fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="b0d58-109">CSS grid debugging features</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="b0d58-111">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="b0d58-111">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-112">L'équipe Microsoft Edge DevTools collabore avec l'équipe Chrome DevTools et la communauté Chromium pour ajouter de nouvelles fonctionnalités de débogage de grille CSS à DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0d58-112">The Microsoft Edge DevTools team is collaborating with the Chrome DevTools team and Chromium community to add new CSS grid debugging features to DevTools.</span></span>  <span data-ttu-id="b0d58-113">Vous pouvez désormais afficher les numéros de ligne de grille, les intervalles de grille et les lignes de grille étendue sous la mesure d'une superposition sur la page.</span><span class="sxs-lookup"><span data-stu-id="b0d58-113">You are now able to display grid line numbers, grid gaps, and extended grid lines as an on-page overlay.</span></span>  <span data-ttu-id="b0d58-114">De plus, d'autres améliorations des outils de grille seront bientôt disponibles.</span><span class="sxs-lookup"><span data-stu-id="b0d58-114">Plus, more improvements to the grid tools are coming soon.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-grid.msft.png" alt-text="Fonctionnalités de débogage de grille CSS" lightbox="../../media/2020/06/experiments-grid.msft.png":::
   <span data-ttu-id="b0d58-116">Fonctionnalités de débogage de grille CSS</span><span class="sxs-lookup"><span data-stu-id="b0d58-116">CSS grid debugging features</span></span>
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="b0d58-117">Pour activer l'expérience, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer les nouvelles fonctionnalités de débogage de la **grille CSS.** [][DevtoolsExperimentalFeaturesTurnOn]</span><span class="sxs-lookup"><span data-stu-id="b0d58-117">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and select the checkbox next to **Enable new CSS Grid debugging features**.</span></span>  
> 
> <span data-ttu-id="b0d58-118">Pour tester l'expérience avec un exemple, accédez à l'exemple de [planificateur CSS Grid.][CodepenRachelweilYzwBzKM]</span><span class="sxs-lookup"><span data-stu-id="b0d58-118">To try out the experiment with a sample, navigate to [CSS Grid planner example][CodepenRachelweilYzwBzKM].</span></span>  

<span data-ttu-id="b0d58-119">Problème de chrome [#1047356][CR1047356]</span><span class="sxs-lookup"><span data-stu-id="b0d58-119">Chromium issue [#1047356][CR1047356]</span></span>  

### <a name="edit-and-replay-requests-with-the-network-console"></a><span data-ttu-id="b0d58-120">Modifier et relire des demandes à l'aide de la console réseau</span><span class="sxs-lookup"><span data-stu-id="b0d58-120">Edit and Replay requests with the Network Console</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="b0d58-122">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="b0d58-122">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-123">Vous pouvez désormais \*\*\*\* utiliser la modification et la relecture sur les demandes dans le journal réseau à l'aide [][DevtoolsNetworkIndexLogActivity] de la console **réseau.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-123">You are now able to use **Edit and Replay** on requests in the [Network Log][DevtoolsNetworkIndexLogActivity] using the **Network Console**.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png" alt-text="Modifier et relire une demande dans NetworkLog avec la console réseau" lightbox="../../media/2020/06/experiments-network-console-edit-and-replay.msft.png":::
   <span data-ttu-id="b0d58-125">Modifier et relire une demande dans [NetworkLog][DevtoolsNetworkIndexLogActivity] avec la **console réseau**</span><span class="sxs-lookup"><span data-stu-id="b0d58-125">Edit and Replay a request in the [NetworkLog][DevtoolsNetworkIndexLogActivity] with the **Network Console**</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-126">Dans un nouveau panneau, la **console** réseau s'ouvre dans le panneau [DevTools][DevtoolsCustomizeIndexDrawer] et remplit automatiquement les informations de la requête HTTP.</span><span class="sxs-lookup"><span data-stu-id="b0d58-126">A new panel, the **Network Console** opens in the [DevTools Drawer][DevtoolsCustomizeIndexDrawer] and automatically populates with information for the HTTP request.</span></span>  <span data-ttu-id="b0d58-127">Pour afficher la réponse renvoyée par le serveur, modifiez la demande \(si nécessaire\) et sélectionnez **Envoyer.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-127">To display the response returned from the server, edit the request \(if needed\) and select **Send**.</span></span>  

<span data-ttu-id="b0d58-128">Vous pouvez également utiliser la **console réseau pour** créer et envoyer des requêtes HTTP directement à partir de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0d58-128">You may also use the **Network Console** to create and send HTTP requests directly from the DevTools.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-network-console.msft.png" alt-text="Panneau Console réseau" lightbox="../../media/2020/06/experiments-network-console.msft.png":::
   <span data-ttu-id="b0d58-130">Panneau **Console réseau**</span><span class="sxs-lookup"><span data-stu-id="b0d58-130">The **Network Console** panel</span></span>  
:::image-end:::  

> [!TIP]
> <span data-ttu-id="b0d58-131">Pour afficher **la console** réseau dans le panneau principal \(top\) au lieu du panneau [DevTools,][DevtoolsCustomizeIndexDrawer]accédez à déplacer des outils entre [des panneaux.](#move-tools-between-panels)</span><span class="sxs-lookup"><span data-stu-id="b0d58-131">To display **Network Console** in the main \(top\) panel instead of the [DevTools Drawer][DevtoolsCustomizeIndexDrawer], navigate to [moving tools between panels](#move-tools-between-panels).</span></span>  

> [!NOTE]
> <span data-ttu-id="b0d58-132">Pour activer l'expérience, [accédez à Activer][DevtoolsExperimentalFeaturesTurnOn] les fonctionnalités expérimentales et cochez la case en regard de **Activer la console réseau.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-132">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable Network Console**.</span></span>  
> 
> <span data-ttu-id="b0d58-133">Ouvrez [le journal réseau,][DevtoolsNetworkIndexLogActivity]ouvrez le menu contextuel \(clic droit\), puis choisissez **Modifier et relire.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-133">Open the [Network Log][DevtoolsNetworkIndexLogActivity], open the contextual menu \(right-click\), and choose **Edit and Replay**.</span></span>  

<span data-ttu-id="b0d58-134">Problème de chrome [#1093687][CR1093687]</span><span class="sxs-lookup"><span data-stu-id="b0d58-134">Chromium issue [#1093687][CR1093687]</span></span>  

### <a name="service-worker-respondwith-events-in-the-timing-tab"></a><span data-ttu-id="b0d58-135">Événements respondWith du service de travail dans l'onglet Minutage</span><span class="sxs-lookup"><span data-stu-id="b0d58-135">Service worker respondWith events in the Timing tab</span></span>  

<span data-ttu-id="b0d58-136">**L'onglet Calendrier** de **l'outil Réseau** inclut désormais les `respondWith` événements de travail de service.</span><span class="sxs-lookup"><span data-stu-id="b0d58-136">The **Timing** tab of the **Network** tool now includes `respondWith` service worker events.</span></span>  <span data-ttu-id="b0d58-137">L'événement de travail de service indique la durée entre l'heure immédiatement avant le début de l'exécution du handler d'événements de travail de service et le moment où la promesse du `respondWith` `fetch` `respondWith` `fetch` handler est réglée.</span><span class="sxs-lookup"><span data-stu-id="b0d58-137">The `respondWith` service worker event shows the duration from the time immediately before the service worker `fetch` event handler starts running to the time when the `respondWith` promise of the `fetch` handler is settled.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab.msft.png" alt-text="Événement de travail de service respondWith dans l'onglet Minutage du panneau Réseau" lightbox="../../media/2020/06/timing-tab.msft.png":::
   <span data-ttu-id="b0d58-139">Événement `respondWith` de travail de service dans **l'onglet Minutage** de **l'outil** Réseau</span><span class="sxs-lookup"><span data-stu-id="b0d58-139">The `respondWith` service worker event in the **Timing** tab of the **Network** tool</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-140">Développez **la réponse reçue** pour afficher des informations supplémentaires à partir de la réponse comme , et `fetch` `CacheStorageCacheName` `serviceWorkerResponseSource` `ResponseTime` .</span><span class="sxs-lookup"><span data-stu-id="b0d58-140">Expand **Response received** to display additional information from the `fetch` response like `CacheStorageCacheName`, `serviceWorkerResponseSource`, and `ResponseTime`.</span></span>  

:::image type="complex" source="../../media/2020/06/timing-tab2.msft.png" alt-text="Développer la réponse reçue pour afficher des informations supplémentaires à partir de la réponse d'extraction" lightbox="../../media/2020/06/timing-tab2.msft.png":::
   <span data-ttu-id="b0d58-142">Développer **la réponse reçue** pour afficher des informations supplémentaires à partir de la `fetch` réponse</span><span class="sxs-lookup"><span data-stu-id="b0d58-142">Expand **Response received** to display additional information from the `fetch` response</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-143">Problème de chrome [#1066579][CR1066579]</span><span class="sxs-lookup"><span data-stu-id="b0d58-143">Chromium issue [#1066579][CR1066579]</span></span>  

### <a name="webhint-feedback-in-the-issues-panel"></a><span data-ttu-id="b0d58-144">commentaires webhint dans le panneau Problèmes</span><span class="sxs-lookup"><span data-stu-id="b0d58-144">webhint feedback in the Issues panel</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="b0d58-146">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="b0d58-146">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-147">[webhint][WebhintMain] est un outil open source qui fournit des commentaires en temps réel sur l'accessibilité, la compatibilité entre les navigateurs, la sécurité, les performances, les applications de périmètre et d'autres problèmes de développement web courants des sites web.</span><span class="sxs-lookup"><span data-stu-id="b0d58-147">[webhint][WebhintMain] is an open-source tool that provides real-time feedback on the accessibility, cross-browser compatibility, security, performance, PWAs, and other common web development issues of websites.</span></span>  <span data-ttu-id="b0d58-148">Pour passer en revue les commentaires sur les sites web dans [le panneau Problèmes.][DevtoolsIssues]</span><span class="sxs-lookup"><span data-stu-id="b0d58-148">To review webhint feedback in the [Issues][DevtoolsIssues] panel.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-webhint.msft.png" alt-text="commentaires webhint dans le panneau Problèmes" lightbox="../../media/2020/06/experiments-webhint.msft.png":::
   <span data-ttu-id="b0d58-150">commentaires webhint dans le panneau Problèmes</span><span class="sxs-lookup"><span data-stu-id="b0d58-150">webhint feedback in the Issues panel</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="b0d58-151">Pour activer l'expérience, [accédez à Activer][DevtoolsExperimentalFeaturesTurnOn] les fonctionnalités expérimentales et activez la case à cocher en regard de **Activer lahint web.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-151">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable webhint**.</span></span>  
> 
> <span data-ttu-id="b0d58-152">Ouvrez [le panneau Problèmes][DevtoolsIssues] pour afficher les commentaires provenant de lahint web.</span><span class="sxs-lookup"><span data-stu-id="b0d58-152">Open the [Issues][DevtoolsIssues] panel to display feedback from webhint.</span></span>  

<span data-ttu-id="b0d58-153">Problème de chrome [#1070378][CR1070378]</span><span class="sxs-lookup"><span data-stu-id="b0d58-153">Chromium issue [#1070378][CR1070378]</span></span>  

### <a name="move-tools-between-panels"></a><span data-ttu-id="b0d58-154">Déplacer des outils entre des panneaux</span><span class="sxs-lookup"><span data-stu-id="b0d58-154">Move tools between panels</span></span>  

:::image type="complex" source="../../media/2020/06/experimental-tag-14px.msft.png" alt-text="Fonctionnalité expérimentale":::
   <span data-ttu-id="b0d58-156">Fonctionnalité expérimentale</span><span class="sxs-lookup"><span data-stu-id="b0d58-156">Experimental feature</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-157">Normalement, les outils \*\*\*\* tels que **Éléments** et Réseau peuvent uniquement être ouverts dans le panneau principal \(top\) de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0d58-157">Normally, tools such as **Elements** and **Network** may only be opened in the main \(top\) panel of DevTools.</span></span>  <span data-ttu-id="b0d58-158">De même, les **outils** tels que l'affichage **3D** et les problèmes peuvent uniquement être ouverts dans le panneau de caisse \(bas\) de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0d58-158">Similarly, tools such as **3D View** and **Issues** may only be opened in the drawer \(bottom\) panel of DevTools.</span></span>  <span data-ttu-id="b0d58-159">Vous pouvez désormais personnaliser votre disposition DevTools en déplaçant les outils entre les panneaux supérieur et inférieur.</span><span class="sxs-lookup"><span data-stu-id="b0d58-159">You are now able to customize your DevTools layout by moving tools between the top and bottom panels.</span></span>  

:::image type="complex" source="../../media/2020/06/experiments-move-panels.msft.png" alt-text="Déplacer des outils entre des panneaux" lightbox="../../media/2020/06/experiments-move-panels.msft.png":::
   <span data-ttu-id="b0d58-161">Déplacer des outils entre des panneaux</span><span class="sxs-lookup"><span data-stu-id="b0d58-161">Move tools between panels</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="b0d58-162">Pour activer l'expérience, accédez à Activer les fonctionnalités expérimentales et activez la case à cocher en regard de Activer la prise en charge pour déplacer des onglets entre **les panneaux.** [][DevtoolsExperimentalFeaturesTurnOn]</span><span class="sxs-lookup"><span data-stu-id="b0d58-162">To enable the experiment, navigate to [Turn on experimental features][DevtoolsExperimentalFeaturesTurnOn] and choose the checkbox next to **Enable support to move tabs between panels**.</span></span>  

<span data-ttu-id="b0d58-163">Problème de chrome [#897944][CR897944]</span><span class="sxs-lookup"><span data-stu-id="b0d58-163">Chromium issue [#897944][CR897944]</span></span>  

### <a name="improved-initiator-tooltip-in-the-network-panel"></a><span data-ttu-id="b0d58-164">Amélioration de l'aide de l'initiateur dans le panneau Réseau</span><span class="sxs-lookup"><span data-stu-id="b0d58-164">Improved Initiator tooltip in the Network panel</span></span>  

<span data-ttu-id="b0d58-165">Dans Microsoft Edge 83 et 84, les bulles de la colonne Initiator, [][DevtoolsNetworkIndexLogActivity] qui indique la cause de la demande de ressource, dans le journal réseau affiché avec une barre de défilement horizontale.</span><span class="sxs-lookup"><span data-stu-id="b0d58-165">In Microsoft Edge 83 and 84, tooltips for the Initiator column, which shows the cause of the resource request, in the [Network Log][DevtoolsNetworkIndexLogActivity] displayed with a horizontal scrollbar.</span></span>  <span data-ttu-id="b0d58-166">Vous n'avez pu afficher la pile d'appels à l'origine de la demande qu'en faisant défiler horizontalement l'information dans l'bulle.</span><span class="sxs-lookup"><span data-stu-id="b0d58-166">You were only able to display the call stack that initiated the request by scrolling horizontally in the tooltip.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-84.msft.png" alt-text="L'aide de l'initiateur dans Microsoft Edge 84" lightbox="../../media/2020/06/initiator-tooltip-84.msft.png":::
   <span data-ttu-id="b0d58-168">L'aide de l'initiateur dans Microsoft Edge 84</span><span class="sxs-lookup"><span data-stu-id="b0d58-168">The Initiator tooltip in Microsoft Edge 84</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-169">À partir de Microsoft Edge 85, vous pouvez désormais afficher la pile d'appels de l'initiateur dans l'boîte à outils sans faire défiler horizontalement.</span><span class="sxs-lookup"><span data-stu-id="b0d58-169">Starting with Microsoft Edge 85, you are now able to display the Initiator call stack in the tooltip without scrolling horizontally.</span></span>  

:::image type="complex" source="../../media/2020/06/initiator-tooltip-85.msft.png" alt-text="L'aide de l'initiateur dans Microsoft Edge 85" lightbox="../../media/2020/06/initiator-tooltip-85.msft.png":::
   <span data-ttu-id="b0d58-171">L'aide de l'initiateur dans Microsoft Edge 85</span><span class="sxs-lookup"><span data-stu-id="b0d58-171">The Initiator tooltip in Microsoft Edge 85</span></span>
:::image-end:::  

<span data-ttu-id="b0d58-172">Problème de chrome [#1069404][CR1069404]</span><span class="sxs-lookup"><span data-stu-id="b0d58-172">Chromium issue [#1069404][CR1069404]</span></span>  

## <a name="announcements-from-the-chromium-project"></a><span data-ttu-id="b0d58-173">Annonces du projet de Chromium</span><span class="sxs-lookup"><span data-stu-id="b0d58-173">Announcements from the Chromium project</span></span>  

<span data-ttu-id="b0d58-174">Les sections suivantes annoncent des fonctionnalités supplémentaires disponibles dans Microsoft Edge 85 qui ont été contribués au projet open source Chromium.</span><span class="sxs-lookup"><span data-stu-id="b0d58-174">The following sections announce additional features available in Microsoft Edge 85 that were contributed to the open source Chromium project.</span></span>  

### <a name="style-editing-for-css-in-js-frameworks"></a><span data-ttu-id="b0d58-175">Modification du style pour les frameworks CSS-in-JS</span><span class="sxs-lookup"><span data-stu-id="b0d58-175">Style editing for CSS-in-JS frameworks</span></span>  

<span data-ttu-id="b0d58-176">Le **volet Styles** a désormais une meilleure prise en charge de l'édition des styles créés avec les API [CSS Object Model (CSSOM).][CsswgDraftsCssom]</span><span class="sxs-lookup"><span data-stu-id="b0d58-176">The **Styles** pane now has better support for editing styles that were created with the [CSS Object Model (CSSOM)][CsswgDraftsCssom] APIs.</span></span>  <span data-ttu-id="b0d58-177">De nombreuses bibliothèques et infrastructure CSS-in-JS utilisent les API CSSOM sous-programme pour construire des styles.</span><span class="sxs-lookup"><span data-stu-id="b0d58-177">Many CSS-in-JS frameworks and libraries use the CSSOM APIs under the hood to construct styles.</span></span>  

<span data-ttu-id="b0d58-178">Vous pouvez désormais modifier les styles ajoutés dans JavaScript à l'aide [de feuilles de style constructables.][WicgConstructStylesheet]</span><span class="sxs-lookup"><span data-stu-id="b0d58-178">You are now able to edit styles added in JavaScript using [Constructable Stylesheets][WicgConstructStylesheet].</span></span>  <span data-ttu-id="b0d58-179">Les feuilles de style constructables sont un nouveau moyen de créer et de distribuer des styles réutilisables lors de l'utilisation [du DOM d'ombre.][MdnShadowDom]</span><span class="sxs-lookup"><span data-stu-id="b0d58-179">Constructable Stylesheets are a new way to create and distribute reusable styles when using [Shadow DOM][MdnShadowDom].</span></span>  

<span data-ttu-id="b0d58-180">Par exemple, les `h1` styles ajoutés avec `CSSStyleSheet` \(API CSSOM\) n'étaient pas modifiables précédemment.</span><span class="sxs-lookup"><span data-stu-id="b0d58-180">For example, the `h1` styles added with `CSSStyleSheet` \(CSSOM APIs\) were not editable previously.</span></span>  <span data-ttu-id="b0d58-181">Les styles sont désormais modifiables dans le **panneau Styles.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-181">The styles are editable now in the **Styles** panel.</span></span>  

:::image type="complex" source="../../media/2020/06/css-in-js.msft.png" alt-text="Modification de la propriété d'arrière-plan des styles h1 ajoutés avec CSSStyleSheet de rose à lightblue" lightbox="../../media/2020/06/css-in-js.msft.png":::
   <span data-ttu-id="b0d58-183">Modification de `background` la propriété des styles `h1` ajoutés à partir de `CSSStyleSheet` `pink` `lightblue` .</span><span class="sxs-lookup"><span data-stu-id="b0d58-183">Changing the `background` property of the `h1` styles added with `CSSStyleSheet` from `pink` to `lightblue`.</span></span>
:::image-end:::  

<span data-ttu-id="b0d58-184">Essayez cette fonctionnalité avec un [exemple qui utilise CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span><span class="sxs-lookup"><span data-stu-id="b0d58-184">Give this feature a try with a [sample that uses CSS-in-JS][CodepenZoherghadyaliAbdgrpz].</span></span>

<span data-ttu-id="b0d58-185">Problème de chrome [#946975][CR946975]</span><span class="sxs-lookup"><span data-stu-id="b0d58-185">Chromium issue [#946975][CR946975]</span></span>  

### <a name="lighthouse-6-in-the-lighthouse-panel"></a><span data-ttu-id="b0d58-186">Phare 6 dans le panneau Panneau de sélection</span><span class="sxs-lookup"><span data-stu-id="b0d58-186">Lighthouse 6 in the Lighthouse panel</span></span>  

<span data-ttu-id="b0d58-187">Le **panneau Panneau** de bord exécute désormais Le Phare 6.</span><span class="sxs-lookup"><span data-stu-id="b0d58-187">The **Lighthouse** panel is now running Lighthouse 6.</span></span>  <span data-ttu-id="b0d58-188">Pour obtenir la liste complète de toutes les modifications, accédez aux notes de publication [v6.0.0.][GithubGoogleChromeLighthouse600]</span><span class="sxs-lookup"><span data-stu-id="b0d58-188">For a full list of all changes, navigate to [v6.0.0 release notes][GithubGoogleChromeLighthouse600].</span></span>  

<span data-ttu-id="b0d58-189">La classe 6.0 présente trois nouvelles mesures dans le rapport : Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\) et Total Blocking Time \(TBT\).</span><span class="sxs-lookup"><span data-stu-id="b0d58-189">Lighthouse 6.0 introduces three new metrics to the report:  Largest Contentful Paint \(LCP\), Cumulative Layout Shift \(CLS\), and Total Blocking Time \(TBT\).</span></span>  

<span data-ttu-id="b0d58-190">La formule de score de performance a également été reweightée pour mieux refléter l'expérience de chargement de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0d58-190">The performance score formula has also been reweighted to better reflect the loading experience of the user.</span></span>  

<span data-ttu-id="b0d58-191">Problème de chrome [#772558][CR772558]</span><span class="sxs-lookup"><span data-stu-id="b0d58-191">Chromium issue [#772558][CR772558]</span></span>  

#### <a name="first-meaningful-paint-deprecation"></a><span data-ttu-id="b0d58-192">Première dépréciation significative de paint</span><span class="sxs-lookup"><span data-stu-id="b0d58-192">First Meaningful Paint deprecation</span></span>  

<span data-ttu-id="b0d58-193">First Meaningful Paint \(FMP\) is deprecated in Paint 6.0.</span><span class="sxs-lookup"><span data-stu-id="b0d58-193">First Meaningful Paint \(FMP\) is deprecated in Lighthouse 6.0.</span></span>  <span data-ttu-id="b0d58-194">FMP a également été supprimé du panneau **Performances.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-194">FMP has also been removed from the **Performance** panel.</span></span>  <span data-ttu-id="b0d58-195">**La plus grande paint contentful est** le remplacement recommandé pour FMP.</span><span class="sxs-lookup"><span data-stu-id="b0d58-195">**Largest Contentful Paint** is the recommended replacement for FMP.</span></span>  <!--For an explanation of why it was deprecated, navigate to [First Meaningful Paint][WebDevFirstMeaningfulPaint].  -->  

<!--todo: add Largest Contentful Paint when section available  -->  
<!--todo: add First Meaningful Paint link and note when available  -->  

<span data-ttu-id="b0d58-196">Problème de chrome [#1096008][CR1096008]</span><span class="sxs-lookup"><span data-stu-id="b0d58-196">Chromium issue [#1096008][CR1096008]</span></span>  

### <a name="support-for-new-javascript-features"></a><span data-ttu-id="b0d58-197">Prise en charge des nouvelles fonctionnalités JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0d58-197">Support for new JavaScript features</span></span>  

<span data-ttu-id="b0d58-198">DevTools offre désormais une meilleure prise en charge de certaines des dernières fonctionnalités de langage JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b0d58-198">DevTools now has better support for some of the latest JavaScript language features.</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="b0d58-199">[Autocompletion automatique][V8DevOptionalChaining] de la syntaxe de chaînage facultative</span><span class="sxs-lookup"><span data-stu-id="b0d58-199">[Optional chaining][V8DevOptionalChaining] syntax autocompletion</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b0d58-200">L'achèvement automatique de propriété dans la **console prend** désormais en charge la syntaxe de chaînage facultative, par exemple, fonctionne désormais en plus de  `name?.` et `name.` `name[` .</span><span class="sxs-lookup"><span data-stu-id="b0d58-200">Property auto-completion in the **Console** now supports optional chaining syntax, for example,  `name?.` now works in addition to `name.` and `name[`.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="b0d58-201">Mise en surbrillance de [syntaxe pour les champs privés][V8DevClassFieldsPrivate]</span><span class="sxs-lookup"><span data-stu-id="b0d58-201">Syntax highlighting for [private fields][V8DevClassFieldsPrivate]</span></span>  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b0d58-202">les champs de classe privés sont désormais correctement mis en surbrillants et assez imprimés dans le **panneau Sources.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-202">private class fields are now properly syntax-highlighted and pretty-printed in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      <span data-ttu-id="b0d58-203">Mise en surbrillance de syntaxe pour [l'opérateur de hillage nullish][V8DevNullishCoalescing]</span><span class="sxs-lookup"><span data-stu-id="b0d58-203">Syntax highlighting for [Nullish coalescing operator][V8DevNullishCoalescing]</span></span>
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b0d58-204">DevTools imprime maintenant correctement l'opérateur de houillement nullish dans le **panneau Sources.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-204">DevTools now properly pretty-prints the nullish coalescing operator in the **Sources** panel.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="b0d58-205">Problèmes de chrome [#1073903,][CR1073903] [#1083214,][CR1083214] [#1083797][CR1083797]</span><span class="sxs-lookup"><span data-stu-id="b0d58-205">Chromium issues [#1073903][CR1073903], [#1083214][CR1083214], [#1083797][CR1083797]</span></span>  

### <a name="new-app-shortcut-warnings-in-the-manifest-pane"></a><span data-ttu-id="b0d58-206">Avertissements de raccourcis pour les nouvelles applications dans le volet manifeste</span><span class="sxs-lookup"><span data-stu-id="b0d58-206">New app shortcut warnings in the Manifest pane</span></span>  

<span data-ttu-id="b0d58-207">**Les raccourcis d'application** aident les utilisateurs à démarrer rapidement des tâches courantes ou recommandées dans une application web.</span><span class="sxs-lookup"><span data-stu-id="b0d58-207">**App shortcuts** help users quickly start common or recommended tasks within a web app.</span></span>  

<!--todo: add App shortcuts when section is live  -->  

<span data-ttu-id="b0d58-208">Le **volet Manifeste** affiche désormais des avertissements pour les conditions suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0d58-208">The **Manifest** pane now shows warnings for the following conditions.</span></span>  

* <span data-ttu-id="b0d58-209">Les icônes de raccourci de l'application sont plus petites que 96 x 96 pixels</span><span class="sxs-lookup"><span data-stu-id="b0d58-209">The app shortcut icons are smaller than 96x96 pixels</span></span>  
* <span data-ttu-id="b0d58-210">Les icônes de raccourci de l'application et les icônes de manifeste ne sont pas carrées \(étant donné que les icônes sont ignorées\)</span><span class="sxs-lookup"><span data-stu-id="b0d58-210">The app shortcut icons and manifest icons are not square \(since the icons are ignored\)</span></span>  

:::image type="complex" source="../../media/2020/06/app-shortcut-warnings.msft.png" alt-text="Avertissements de raccourci d'application" lightbox="../../media/2020/06/app-shortcut-warnings.msft.png":::
   <span data-ttu-id="b0d58-212">Avertissements de raccourci d'application</span><span class="sxs-lookup"><span data-stu-id="b0d58-212">App shortcut warnings</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-213">Problème de chrome [#955497][CR955497]</span><span class="sxs-lookup"><span data-stu-id="b0d58-213">Chromium issue [#955497][CR955497]</span></span>  

### <a name="consistent-display-of-the-computed-pane"></a><span data-ttu-id="b0d58-214">Affichage cohérent du volet calculé</span><span class="sxs-lookup"><span data-stu-id="b0d58-214">Consistent display of the Computed pane</span></span>  

<span data-ttu-id="b0d58-215">Le **volet Calculé** de l'outil **Éléments** s'affiche désormais de manière cohérente sous la forme d'un volet dans toutes les tailles de laport d'affichage.</span><span class="sxs-lookup"><span data-stu-id="b0d58-215">The **Computed** pane in the **Elements** tool now displays consistently as a pane across all viewport sizes.</span></span>  <span data-ttu-id="b0d58-216">**Auparavant, le volet Calculé** fusionnait à l'intérieur du volet **Styles** lorsque la largeur de laport d'affichage DevTools était étroite.</span><span class="sxs-lookup"><span data-stu-id="b0d58-216">Previously the **Computed** pane merged inside the **Styles** pane when the width of the DevTools viewport was narrow.</span></span>  

:::image type="complex" source="../../media/2020/06/computed-pane.msft.png" alt-text="Le volet Calculé s'affiche de manière cohérente sous la forme d'un volet distinct, même lorsque les DevTools sont étroits" lightbox="../../media/2020/06/computed-pane.msft.png":::
   <span data-ttu-id="b0d58-218">Le **volet Calculé** s'affiche de manière cohérente sous la forme d'un volet distinct, même lorsque les DevTools sont étroits.</span><span class="sxs-lookup"><span data-stu-id="b0d58-218">The **Computed** pane consistently displays as a separate pane even when the DevTools are narrow.</span></span>
:::image-end:::  

<span data-ttu-id="b0d58-219">Problème de chrome [#1073899][CR1073899]</span><span class="sxs-lookup"><span data-stu-id="b0d58-219">Chromium issue [#1073899][CR1073899]</span></span>  

### <a name="bytecode-offsets-for-webassembly-files"></a><span data-ttu-id="b0d58-220">Décalages de bytecode pour les fichiers WebAssembly</span><span class="sxs-lookup"><span data-stu-id="b0d58-220">Bytecode offsets for WebAssembly files</span></span>  

<span data-ttu-id="b0d58-221">DevTools utilise désormais des décalages de bytecode pour afficher les numéros de ligne wasm disassembly.</span><span class="sxs-lookup"><span data-stu-id="b0d58-221">DevTools now uses bytecode offsets for displaying line numbers of Wasm disassembly.</span></span>  
<span data-ttu-id="b0d58-222">Les numéros de ligne vous indiquent plus clairement que vous regardez les données binaires et sont plus cohérents avec la façon dont le runtime Wasm référence les emplacements.</span><span class="sxs-lookup"><span data-stu-id="b0d58-222">The line numbers make it clearer that you are looking at binary data, and is more consistent with how the Wasm runtime references locations.</span></span>  

<span data-ttu-id="b0d58-223">Problème de chrome [#1071432][CR1071432]</span><span class="sxs-lookup"><span data-stu-id="b0d58-223">Chromium issue [#1071432][CR1071432]</span></span>  

### <a name="line-wise-copy-and-cut-in-sources-panel"></a><span data-ttu-id="b0d58-224">Copier et couper au sens des lignes dans le panneau Sources</span><span class="sxs-lookup"><span data-stu-id="b0d58-224">Line-wise copy and cut in Sources Panel</span></span>  

<span data-ttu-id="b0d58-225">Lorsque vous effectuez une copie ou une coupure sans sélection dans l'éditeur du panneau [Sources,][DevtoolsSourcesEditCssJavascript]DevTools copie ou coupe la ligne de contenu actuelle.</span><span class="sxs-lookup"><span data-stu-id="b0d58-225">When performing copy or cut with no selection in the [Sources panel editor][DevtoolsSourcesEditCssJavascript], DevTools copies or cuts the current line of content.</span></span>  

:::image type="complex" source="../../media/2020/06/line-wise-cut.msft.png" alt-text="Avec le curseur à la fin de la ligne 5, copiez la ligne entière à partir de pen.js dans devTools et coller dans Visual Studio Code" lightbox="../../media/2020/06/line-wise-cut.msft.png":::
   <span data-ttu-id="b0d58-227">Avec le curseur à la fin de la ligne 5, copiez la ligne entière à partir de **pen.js** dans devTools et coller dans Visual Studio [Code][VisualStudioCode].</span><span class="sxs-lookup"><span data-stu-id="b0d58-227">With the cursor at the end of Line 5, copying the whole line from **pen.js** in the DevTools and pasting in [Visual Studio Code][VisualStudioCode].</span></span>
:::image-end:::  

<span data-ttu-id="b0d58-228">Problème de chrome [#800028][CR800028]</span><span class="sxs-lookup"><span data-stu-id="b0d58-228">Chromium issue [#800028][CR800028]</span></span>

### <a name="console-settings-updates"></a><span data-ttu-id="b0d58-229">Mises à jour des paramètres de la console</span><span class="sxs-lookup"><span data-stu-id="b0d58-229">Console Settings updates</span></span>  

#### <a name="ungroup-same-console-messages"></a><span data-ttu-id="b0d58-230">Dégrouper les mêmes messages de console</span><span class="sxs-lookup"><span data-stu-id="b0d58-230">Ungroup same console messages</span></span>  

<span data-ttu-id="b0d58-231">Le **groupe semblable** au basculement dans paramètres de la console s'applique désormais aux messages en double.</span><span class="sxs-lookup"><span data-stu-id="b0d58-231">The **Group similar** toggle in Console Settings now applies to duplicate messages.</span></span>  <span data-ttu-id="b0d58-232">Auparavant, il vient d'être appliqué à des messages similaires.</span><span class="sxs-lookup"><span data-stu-id="b0d58-232">Previously it just applied to similar messages.</span></span>  

<span data-ttu-id="b0d58-233">Par exemple, auparavant, DevTools n'a pas désgroupé les messages même si le groupe `hello` **similaire** est décoché.</span><span class="sxs-lookup"><span data-stu-id="b0d58-233">For example, previously, DevTools did not ungroup the `hello` messages even though **Group similar** is unchecked.</span></span>  <span data-ttu-id="b0d58-234">À présent, `hello` les messages sont désgroupés.</span><span class="sxs-lookup"><span data-stu-id="b0d58-234">Now, the `hello` messages are ungrouped.</span></span>  

:::image type="complex" source="../../media/2020/06/ungroup-similar.msft.png" alt-text="Lorsque le groupe similaire est désactivé, les messages Hello sont désgroupés" lightbox="../../media/2020/06/ungroup-similar.msft.png":::
   <span data-ttu-id="b0d58-236">Lorsque **le groupe similaire** est désactivé, les messages sont `hello` désgroupés</span><span class="sxs-lookup"><span data-stu-id="b0d58-236">When **Group similar** is unchecked, the `hello` messages are ungrouped</span></span>
:::image-end:::  

<span data-ttu-id="b0d58-237">Essayez cette fonctionnalité avec un [exemple qui envoie des messages en double à la console.][CodepenZoherghadyaliZyrjgdJ]</span><span class="sxs-lookup"><span data-stu-id="b0d58-237">Give this feature a try with a [sample that sends duplicate messages to the Console][CodepenZoherghadyaliZyrjgdJ].</span></span>  

<span data-ttu-id="b0d58-238">Problème de chrome [#1082963][CR1082963]</span><span class="sxs-lookup"><span data-stu-id="b0d58-238">Chromium issue [#1082963][CR1082963]</span></span>  

### <a name="persisting-selected-context-only-settings"></a><span data-ttu-id="b0d58-239">Persistance des paramètres de contexte sélectionné uniquement</span><span class="sxs-lookup"><span data-stu-id="b0d58-239">Persisting Selected context only settings</span></span>  

<span data-ttu-id="b0d58-240">Seuls **les paramètres de** contexte sélectionnés dans paramètres de la console sont désormais persistants.</span><span class="sxs-lookup"><span data-stu-id="b0d58-240">The **Selected context only** settings in Console Settings is now persisted.</span></span>  <span data-ttu-id="b0d58-241">Auparavant, les paramètres étaient réinitialisés chaque fois que vous avez fermé et rouvert DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0d58-241">Previously the settings were reset every time you closed and reopened DevTools.</span></span>  <span data-ttu-id="b0d58-242">La modification rend le comportement du paramètre cohérent avec les autres options de paramètres de la console.</span><span class="sxs-lookup"><span data-stu-id="b0d58-242">The change makes the setting behavior consistent with other Console Settings options.</span></span>  

:::image type="complex" source="../../media/2020/06/selected-context.msft.png" alt-text="Paramètre de contexte sélectionné uniquement" lightbox="../../media/2020/06/selected-context.msft.png":::
   <span data-ttu-id="b0d58-244">**Paramètre de contexte sélectionné uniquement**</span><span class="sxs-lookup"><span data-stu-id="b0d58-244">**Selected context only** setting</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-245">Problème de chrome [#1055875][CR1055875]</span><span class="sxs-lookup"><span data-stu-id="b0d58-245">Chromium issue [#1055875][CR1055875]</span></span>  

### <a name="performance-panel-updates"></a><span data-ttu-id="b0d58-246">Mises à jour du panneau de performances</span><span class="sxs-lookup"><span data-stu-id="b0d58-246">Performance panel updates</span></span>  

#### <a name="javascript-compilation-cache-information-in-performance-tool"></a><span data-ttu-id="b0d58-247">Informations sur le cache de compilation JavaScript dans **l'outil Performance**</span><span class="sxs-lookup"><span data-stu-id="b0d58-247">JavaScript compilation cache information in **Performance** tool</span></span>  

<span data-ttu-id="b0d58-248">[Les informations du cache de compilation JavaScript][V8DevCodeCaching] sont désormais toujours affichées dans le **panneau** Résumé de l'outil **Performance.**</span><span class="sxs-lookup"><span data-stu-id="b0d58-248">[JavaScript compilation cache information][V8DevCodeCaching] is now always displayed in the **Summary** panel of the **Performance** tool.</span></span>  <span data-ttu-id="b0d58-249">Auparavant, DevTools n'avait rien à voir avec la mise en cache du code si la mise en cache du code ne s'était pas produit.</span><span class="sxs-lookup"><span data-stu-id="b0d58-249">Previously, DevTools did not show anything related to code caching if code caching did not happen.</span></span>  

:::image type="complex" source="../../media/2020/06/js-compilation-cache.msft.png" alt-text="Informations sur le cache de compilation JavaScript" lightbox="../../media/2020/06/js-compilation-cache.msft.png":::
   <span data-ttu-id="b0d58-251">Informations sur le cache de compilation JavaScript</span><span class="sxs-lookup"><span data-stu-id="b0d58-251">JavaScript compilation cache information</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-252">Problème de chrome [#912581][CR912581]</span><span class="sxs-lookup"><span data-stu-id="b0d58-252">Chromium issue [#912581][CR912581]</span></span>  

#### <a name="navigation-timing-alignment-in-the-performance-panel"></a><span data-ttu-id="b0d58-253">Alignement du minutage de navigation dans le panneau Performances</span><span class="sxs-lookup"><span data-stu-id="b0d58-253">Navigation timing alignment in the Performance panel</span></span>  

<span data-ttu-id="b0d58-254">Panneau **Performances** utilisé pour afficher les heures dans les règles en fonction du moment où l'enregistrement a démarré.</span><span class="sxs-lookup"><span data-stu-id="b0d58-254">The **Performance** panel used to show times in the rulers based on when the recording started.</span></span>  <span data-ttu-id="b0d58-255">Le minutage a changé pour les enregistrements où l'utilisateur navigue, où DevTools affiche désormais les temps de règle par rapport à la navigation.</span><span class="sxs-lookup"><span data-stu-id="b0d58-255">The timing has now changed for recordings where the user navigates, where DevTools now shows ruler times relative to the navigation instead.</span></span>  

:::image type="complex" source="../../media/2020/06/nav-timing.msft.png" alt-text="Aligner le minutage de navigation dans l'outil Performances" lightbox="../../media/2020/06/nav-timing.msft.png":::
   <span data-ttu-id="b0d58-257">Aligner le minutage de navigation dans **l'outil Performances**</span><span class="sxs-lookup"><span data-stu-id="b0d58-257">Align navigation timing in **Performance** tool</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-258">Les heures des événements First Paint, First Contentful Paint et Largest Contentful Paint sont mises à jour pour être relatives au début de la navigation, ce qui signifie que le minutage correspond aux minutages signalés par `DOMContentLoaded` `PerformanceObserver` .</span><span class="sxs-lookup"><span data-stu-id="b0d58-258">The times for `DOMContentLoaded`, First Paint, First Contentful Paint, and Largest Contentful Paint events are updated to be relative to the start of the navigation, which means the timing matches the timings reported by `PerformanceObserver`.</span></span>  

<span data-ttu-id="b0d58-259">Problème de chrome [#974550][CR974550]</span><span class="sxs-lookup"><span data-stu-id="b0d58-259">Chromium issue [#974550][CR974550]</span></span>  

### <a name="new-icons-for-breakpoints-conditional-breakpoints-and-logpoints"></a><span data-ttu-id="b0d58-260">Nouvelles icônes pour les points d'arrêt, les points d'arrêt conditionnels et les points d'accès</span><span class="sxs-lookup"><span data-stu-id="b0d58-260">New icons for breakpoints, conditional breakpoints, and logpoints</span></span>  

<span data-ttu-id="b0d58-261">Le **panneau Sources** offre de nouvelles conceptions pour les points d'arrêt, les points d'arrêt conditionnels et les points d'accès.</span><span class="sxs-lookup"><span data-stu-id="b0d58-261">The **Sources** panel has new designs for breakpoints, conditional breakpoints, and logpoints.</span></span>  <span data-ttu-id="b0d58-262">Les points d'arrêt sont représentés par un cercle rouge, comme [Visual Studio code][VisualStudioCode] et [Visual Studio][VisualStudio].</span><span class="sxs-lookup"><span data-stu-id="b0d58-262">Breakpoints are represented by a red circle, just like [Visual Studio Code][VisualStudioCode] and [Visual Studio][VisualStudio].</span></span>  <span data-ttu-id="b0d58-263">Des icônes sont ajoutées pour différencier les points d'arrêt conditionnels et les points d'accès.</span><span class="sxs-lookup"><span data-stu-id="b0d58-263">Icons are added to differentiate conditional breakpoints and logpoints.</span></span>  

:::image type="complex" source="../../media/2020/06/breakpoints.msft.png" alt-text="Points d’arrêt" lightbox="../../media/2020/06/breakpoints.msft.png":::
   <span data-ttu-id="b0d58-265">Points d’arrêt</span><span class="sxs-lookup"><span data-stu-id="b0d58-265">Breakpoints</span></span>  
:::image-end:::  

<span data-ttu-id="b0d58-266">Problème de chrome [#1041830][CR1041830]</span><span class="sxs-lookup"><span data-stu-id="b0d58-266">Chromium issue [#1041830][CR1041830]</span></span>  

## <a name="download-the-microsoft-edge-preview-channels"></a><span data-ttu-id="b0d58-267">Télécharger les canaux d’aperçu Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="b0d58-267">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="b0d58-268">Si vous utilisez Windows ou macOS, envisagez d'utiliser les canaux d'aperçu [Microsoft Edge][MicrosoftEdgePreviewChannels] comme navigateur de développement par défaut.</span><span class="sxs-lookup"><span data-stu-id="b0d58-268">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="b0d58-269">Les canaux de prévisualisation vous donnent accès aux dernières fonctionnalités de DevTools.</span><span class="sxs-lookup"><span data-stu-id="b0d58-269">The preview channels give you access to the latest DevTools features.</span></span>  

## <a name="getting-in-touch-with-microsoft-edge-devtools-team"></a><span data-ttu-id="b0d58-270">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b0d58-270">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Outils de développement Microsoft Edge (Chromium) | Documents Microsoft"  
[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu "Exécuter des commandes avec le menu de commandes Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsCustomizeIndexDrawer]: /microsoft-edge/devtools-guide-chromium/customize/index#drawer "Caisse : personnaliser les paramètres DevTools de Microsoft Edge | Documents Microsoft"
[DevtoolsExperimentalFeaturesTurnOn]: /microsoft-edge/devtools-guide-chromium/experimental-features#turn-on-experimental-features "Activer les fonctions expérimentales – Fonctions expérimentales | Microsoft Docs"  
[DevtoolsIssues]: /microsoft-edge/devtools-guide-chromium/issues "Recherchez et corrigez les problèmes liés à l’outil des problèmes de Microsoft Edge DevTools | Documents Microsoft"
[DevtoolsSourcesEditCssJavascript]: /microsoft-edge/devtools-guide-chromium/sources#edit-css-and-javascript "Modifier CSS et JavaScript : vue d'ensemble du panneau Sources | Documents Microsoft"  
[DevtoolsNetworkIndexLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Journal de l'activité réseau : inspecter l'activité réseau dans microsoft Edge DevTools | Documents Microsoft"

[CodepenZoherghadyaliAbdgrpz]: https://codepen.io/zoherghadyali/full/abdGrPZ "Modification du style pour les frameworks CSS-in-JS | CodePen"
[CodepenZoherghadyaliZyrjgdJ]: https://codepen.io/zoherghadyali/full/zYrjgdJ "Envoyer des messages en double à la console | CodePen"
[CodepenRachelweilYzwBzKM]: https://codepen.io/hxlnt/full/YzwBzKM "Exemple de planificateur CSS Grid | CodePen"

[CRIssuesList]: https://bugs.chromium.org/p/chromium/issues/list "Bogues Chromium"  

[CR772558]: https://crbug.com/772558 "DevTools : mise à jour vers la dernière version de | Bogues Chromium"  
[CR800028]: https://crbug.com/800028 "Le raccourci de ligne en double dans l'éditeur outils de développement ne fonctionne pas après la mise à jour de Chrome | Bogues Chromium"  
[CR912581]: https://crbug.com/912581 "Exposer les scripts mis en cache par V8 dans DevTools/about:tracing | Bogues Chromium"  
[CR946975]: https://crbug.com/946975 "La barre latérale Styles DevTools ne fonctionne pas avec les feuilles de style | Bogues Chromium"  
[CR955497]: https://crbug.com/955497 "Menu de raccourci d'icône d'application pour les applications de | Bogues Chromium"  
[CR974550]: https://crbug.com/974550 "Non-matisation des mesures entre le panneau Perf et performanceObserver | Bogues Chromium"  
[CR1041830]: https://crbug.com/1041830 "Améliorer les couleurs des points d'arrêt | Bogues Chromium"  
[CR1055875]: https://crbug.com/1055875 "La valeur du paramètre de console de contexte sélectionné uniquement n'est pas persistante après la fermeture et la réouverture des outils de développement | Bogues Chromium"  
[CR1066579]: https://crbug.com/1066579 "DevTools : afficher la chronologie d'extraction serviceWorkers par demande dans le panneau réseau | Bogues Chromium"  
[CR1071432]: https://crbug.com/1071432 "Expérience de développement de base wasm | Bogues Chromium"  
[CR1073899]: https://crbug.com/1073899 "L'onglet Style calculé disparaît en mode | Bogues Chromium"  
[CR1073903]: https://crbug.com/1073903 "DevTools : la mise en surbrillance de la syntaxe ne fonctionne pas avec les champs privés | Bogues Chromium"  
[CR1082963]: https://crbug.com/1082963 "Can't disable console's Group similar messages behavior | Bogues Chromium"  
[CR1083214]: https://crbug.com/1083214 "acorn ne prend pas en charge le chaînage facultatif | Bogues Chromium"  
[CR1083797]: https://crbug.com/1083797 "Impression assez rompue pour la | Bogues Chromium"  
[CR1096008]: https://crbug.com/1096008 "Supprimer les | FMP Bogues Chromium"  
[CR1047356]: https://crbug.com/1047356 "Outils Grille CSS/Flexbox/Tableau | Bogues Chromium"  
[CR1093687]: https://crbug.com/1093687 "Créer un outil pour créer et relire des demandes de réseau synthétique | Bogues Chromium"  
[CR1070378]: https://crbug.com/1070378 "Intégrer webhint dans devTools | Bogues Chromium"  
[CR1069404]: https://crbug.com/1069404 "Les fenêtres pop-up de widget [Outils de développement] sont trop | Bogues Chromium"  
[CR897944]: https://crbug.com/897944 "Panneaux de | Bogues Chromium"

[GithubGoogleChromeLighthouse600]: https://github.com/GoogleChrome/lighthouse/releases/tag/v6.0.0 "v6.0.0 - GoogleChrome/| GitHub"  

[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=[DevTools%20Docs%20Feedback] "Nouveau problème : MicrosoftDocs/edge-developer"  

[MdnShadowDom]: https://developer.mozilla.org/docs/Web/Web_Components/Using_shadow_DOM "Utilisation du dom d'ombre | MDN"

[MicrosoftEdgePreviewChannels]: https://www.microsoftedgeinsider.com/download/ "Canaux de préversion de Microsoft Edge"  

[VisualStudio]: https://visualstudio.microsoft.com/ "Visual Studio"
[VisualStudioCode]: https://code.visualstudio.com/ "Code Visual Studio"  

[CsswgDraftsCssom]: https://drafts.csswg.org/cssom "Modèle objet CSS (CSSOM) | Brouillons de l'éditeur de groupe de travail CSS W3C"  

[PostTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Publier un Tweet"  
[EdgeDevToolsTwitterAccount]: https://twitter.com/EdgeDevTools "@EdgeDevTools compte Twitter"  

[V8DevClassFieldsPrivate]: https://v8.dev/features/class-fields#private-class-fields "Champs de classe privés : champs de classes publiques et privées | V8. Dev"  
[V8DevCodeCaching]: https://v8.dev/blog/code-caching-for-devs "Mise en cache du code pour les développeurs JavaScript | V8. Dev"  
[V8DevNullishCoalescing]: https://v8.dev/features/nullish-coalescing "A la fois null et | V8. Dev"  
[V8DevOptionalChaining]: https://v8.dev/features/optional-chaining "Chaîne facultative | V8. Dev"  

[WebhintMain]: https://webhint.io "webhint"  

[WicgConstructStylesheet]: https://wicg.github.io/construct-stylesheets/ "Objets Stylesheet constructables | Groupe de recherche de contenu Web (CG) Web"

<!--[WebDevLighthouseWhatsNew60]: https://web.dev/lighthouse-whats-new-6.0 "What's New in Lighthouse 6.0 | Web.Dev"  -->  
<!--[WebDevVitalsCoreWeb]: https://web.dev/vitals#core-web-vitals "Core Web Vitals - Web Vitals | Web.Dev"  -->  
<!--[WebdevAppShortcuts]: https://alphabet-dev/app-shortcuts "Get things done quickly with app shortcuts | alphabet-dev"  -->  
<!--[WebdevCls]: https://alphabet-dev/cls "Cumulative Layout Shift (CLS) | alphabet-dev"  -->  
<!--[WebdevControlFocus]: https://alphabet-dev/control-focus-with-tabindex "Control focus with tabindex | alphabet-dev"  -->  
<!--[WebdevMeasureSpeedLabField]: https://alphabet-dev/how-to-measure-speed#lab-data-vs-field-data "Lab data vs Field data - How to measure speed? | alphabet-dev"  -->  
<!--[WebdevLabelsText]: https://alphabet-dev/labels-and-text-alternatives "Labels and text alternatives | alphabet-dev"  -->  
<!--[WebdevTbt]: https://alphabet-dev/tbt "Total Blocking Time (TBT) | alphabet-dev"  -->  
<!--[WebFundamentalComponentsShadowdom]: /web/fundamentals/web-components/shadowdom  -->  
<!--[WebDevLcp]: https://web.dev/lcp "Largest Contentful Paint (LCP) | Web.Dev"  -->  
<!--[WebDevFirstMeaningfulPaint]: https://web.dev/first-meaningful-paint "First Meaningful Paint | Web.Dev"  -->  
<!--[WhatsNew201902ConstructableStylesheets]: ../../2019/02/constructable-stylesheets.md "Constructable Stylesheets: seamless reusable styles | Microsoft Docs"  -->  

[TheWebWeWant]: https://webwewant.fyi/ "Le site Web de votre choix"  

> [!NOTE]
> <span data-ttu-id="b0d58-319">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0d58-319">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b0d58-320">La page d’origine est disponible [ici](https://developer.chrome.com/blog/new-in-devtools-85) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)</span><span class="sxs-lookup"><span data-stu-id="b0d58-320">The original page is found [here](https://developer.chrome.com/blog/new-in-devtools-85) and is authored by [Jecelyn Yeen][JecelynYeen] \(Developer advocate, Chrome DevTools\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="b0d58-322">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b0d58-322">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
