---
title: Examiner l’activité réseau dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611811"
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





# <span data-ttu-id="625ea-103">Examiner l’activité réseau dans Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="625ea-103">Inspect Network Activity In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="625ea-104">Il s’agit d’un didacticiel d’utilisation des fonctionnalités DevTools les plus fréquemment utilisées associées à l’inspection de l’activité réseau d’une page.</span><span class="sxs-lookup"><span data-stu-id="625ea-104">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="625ea-105">Pour parcourir les fonctionnalités, voir [référence réseau][DevtoolsNetworkReference] .</span><span class="sxs-lookup"><span data-stu-id="625ea-105">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="625ea-106">Quand utiliser le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="625ea-106">When to use the Network panel</span></span>   

<span data-ttu-id="625ea-107">En règle générale, utilisez le panneau réseau pour vous assurer que les ressources sont téléchargées ou chargées comme prévu.</span><span class="sxs-lookup"><span data-stu-id="625ea-107">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="625ea-108">Les cas d’utilisation les plus courants du panneau réseau sont les suivants:</span><span class="sxs-lookup"><span data-stu-id="625ea-108">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="625ea-109">Vérifiez que les ressources sont en train d’être chargées ou téléchargées du tout.</span><span class="sxs-lookup"><span data-stu-id="625ea-109">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="625ea-110">Inspecter les propriétés d’une ressource individuelle, par exemple, les en-têtes HTTP, le contenu, la taille, etc.</span><span class="sxs-lookup"><span data-stu-id="625ea-110">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  

<span data-ttu-id="625ea-111">Si vous cherchez à améliorer les performances de chargement de page, **ne démarrez pas** le panneau réseau.</span><span class="sxs-lookup"><span data-stu-id="625ea-111">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="625ea-112">Il existe de nombreux types de problèmes de performances de chargement qui ne sont pas liés à l’activité réseau.</span><span class="sxs-lookup"><span data-stu-id="625ea-112">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="625ea-113">Commencez avec le panneau audits, car il vous donne des suggestions ciblées sur l’amélioration de votre page.</span><span class="sxs-lookup"><span data-stu-id="625ea-113">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="625ea-114">Voir [optimiser la vitesse du site Web][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="625ea-114">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="625ea-115">Ouvrir le panneau réseau</span><span class="sxs-lookup"><span data-stu-id="625ea-115">Open the Network panel</span></span>   

<span data-ttu-id="625ea-116">Pour tirer le meilleur parti de ce didacticiel, ouvrez la démonstration et testez les fonctionnalités de la page de démonstration.</span><span class="sxs-lookup"><span data-stu-id="625ea-116">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="625ea-117">Ouvrir la [démonstration commencer][GlitchNetworkGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="625ea-117">Open the [Get Started Demo][GlitchNetworkGetStarted] .</span></span>  
    
    > ##### <span data-ttu-id="625ea-118">Figure1</span><span class="sxs-lookup"><span data-stu-id="625ea-118">Figure 1</span></span>  
    > <span data-ttu-id="625ea-119">La démonstration</span><span class="sxs-lookup"><span data-stu-id="625ea-119">The demo</span></span>  
    > ![La démonstration][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  <span data-ttu-id="625ea-121">[Ouvrez devtools][DevToolsOpen] en appuyant sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="625ea-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="625ea-122">Le panneau **console** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="625ea-122">The **Console** panel opens.</span></span>  
    
    > ##### <span data-ttu-id="625ea-123">Figure 2</span><span class="sxs-lookup"><span data-stu-id="625ea-123">Figure 2</span></span>  
    > <span data-ttu-id="625ea-124">La console</span><span class="sxs-lookup"><span data-stu-id="625ea-124">The Console</span></span>  
    > <span data-ttu-id="625ea-125">! [La console] [ImagesTutorialConsole]</span><span class="sxs-lookup"><span data-stu-id="625ea-125">![The Console][ImagesTutorialConsole]</span></span>  
    
    <span data-ttu-id="625ea-126">Vous pouvez [ancrer devtools en bas de la fenêtre][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="625ea-126">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="625ea-127">Figure3</span><span class="sxs-lookup"><span data-stu-id="625ea-127">Figure 3</span></span>  
    > <span data-ttu-id="625ea-128">DevTools ancré en bas de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="625ea-128">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="625ea-129">! [DevTools ancré en bas de la fenêtre] [ImagesTutorialDocked]</span><span class="sxs-lookup"><span data-stu-id="625ea-129">![DevTools docked to the bottom of the window][ImagesTutorialDocked]</span></span>  

1.  <span data-ttu-id="625ea-130">Sélectionnez l’onglet **Network (réseau** ).  Le volet réseau s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="625ea-130">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    > ##### <span data-ttu-id="625ea-131">Figure 4</span><span class="sxs-lookup"><span data-stu-id="625ea-131">Figure 4</span></span>  
    > <span data-ttu-id="625ea-132">DevTools ancré en bas de la fenêtre</span><span class="sxs-lookup"><span data-stu-id="625ea-132">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="625ea-133">! [DevTools ancré en bas de la fenêtre] [ImagesTutorialNetwork]</span><span class="sxs-lookup"><span data-stu-id="625ea-133">![DevTools docked to the bottom of the window][ImagesTutorialNetwork]</span></span>  

<span data-ttu-id="625ea-134">Pour le moment, le volet réseau est vide.</span><span class="sxs-lookup"><span data-stu-id="625ea-134">Right now the Network panel is empty.</span></span>  <span data-ttu-id="625ea-135">DevTools uniquement les journaux d’activité réseau après l’ouverture et aucune activité réseau ne s’est produite depuis que vous avez ouvert DevTools.</span><span class="sxs-lookup"><span data-stu-id="625ea-135">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="625ea-136">Journalisation de l’activité du réseau</span><span class="sxs-lookup"><span data-stu-id="625ea-136">Log network activity</span></span>   

<span data-ttu-id="625ea-137">Pour afficher l’activité réseau provoquée par une page:</span><span class="sxs-lookup"><span data-stu-id="625ea-137">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="625ea-138">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="625ea-138">Reload the page.</span></span>  <span data-ttu-id="625ea-139">Le panneau réseau enregistre toutes les activités du réseau dans le **Journal du réseau**.</span><span class="sxs-lookup"><span data-stu-id="625ea-139">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    > ##### <span data-ttu-id="625ea-140">Figure 5</span><span class="sxs-lookup"><span data-stu-id="625ea-140">Figure 5</span></span>  
    > <span data-ttu-id="625ea-141">Journal du réseau</span><span class="sxs-lookup"><span data-stu-id="625ea-141">The Network Log</span></span>  
    > <span data-ttu-id="625ea-142">! [Journal du réseau] [ImagesTutorialLog]</span><span class="sxs-lookup"><span data-stu-id="625ea-142">![The Network Log][ImagesTutorialLog]</span></span>  
    
    <span data-ttu-id="625ea-143">Chaque ligne du **Journal réseau** représente une ressource.</span><span class="sxs-lookup"><span data-stu-id="625ea-143">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="625ea-144">Par défaut, les ressources sont répertoriées dans l’ordre chronologique.</span><span class="sxs-lookup"><span data-stu-id="625ea-144">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="625ea-145">La principale ressource correspond généralement au document HTML principal.</span><span class="sxs-lookup"><span data-stu-id="625ea-145">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="625ea-146">Le dernier élément de la ressource est le dernier demandé.</span><span class="sxs-lookup"><span data-stu-id="625ea-146">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="625ea-147">Chaque colonne représente des informations sur une ressource.</span><span class="sxs-lookup"><span data-stu-id="625ea-147">Each column represents information about a resource.</span></span>  <span data-ttu-id="625ea-148">La [**figure 6**](#figure-6) montre les colonnes par défaut:</span><span class="sxs-lookup"><span data-stu-id="625ea-148">[**Figure 6**](#figure-6) shows the default columns:</span></span>  

    *   <span data-ttu-id="625ea-149">**Status**.</span><span class="sxs-lookup"><span data-stu-id="625ea-149">**Status**.</span></span>  <span data-ttu-id="625ea-150">Code d’état HTTP de la réponse.</span><span class="sxs-lookup"><span data-stu-id="625ea-150">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="625ea-151">**Type**.</span><span class="sxs-lookup"><span data-stu-id="625ea-151">**Type**.</span></span>  <span data-ttu-id="625ea-152">Type de ressource.</span><span class="sxs-lookup"><span data-stu-id="625ea-152">The resource type.</span></span>  
    *   <span data-ttu-id="625ea-153">**Initiator**.</span><span class="sxs-lookup"><span data-stu-id="625ea-153">**Initiator**.</span></span>  <span data-ttu-id="625ea-154">La cause de la demande de ressource.</span><span class="sxs-lookup"><span data-stu-id="625ea-154">The cause of the resource request.</span></span>  <span data-ttu-id="625ea-155">La sélection d’un lien dans la colonne initiateur vous permet d’accéder au code source à l’origine de la demande.</span><span class="sxs-lookup"><span data-stu-id="625ea-155">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="625ea-156">**Temps**.</span><span class="sxs-lookup"><span data-stu-id="625ea-156">**Time**.</span></span>  <span data-ttu-id="625ea-157">Durée de la requête.</span><span class="sxs-lookup"><span data-stu-id="625ea-157">The duration of the request.</span></span>  
    *   <span data-ttu-id="625ea-158">En **cascade**.</span><span class="sxs-lookup"><span data-stu-id="625ea-158">**Waterfall**.</span></span>  <span data-ttu-id="625ea-159">Représentation graphique des différentes étapes de la requête.</span><span class="sxs-lookup"><span data-stu-id="625ea-159">A graphical representation of the different stages of the request.</span></span>  
        <span data-ttu-id="625ea-160">Placez le pointeur de la souris sur une cascade pour afficher une répartition.</span><span class="sxs-lookup"><span data-stu-id="625ea-160">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="625ea-161">Le graphique au-dessus du journal réseau est appelé vue d’ensemble.</span><span class="sxs-lookup"><span data-stu-id="625ea-161">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="625ea-162">Dans ce didacticiel, vous n’utiliserez pas le graphique de vue d’ensemble et vous pouvez le masquer.</span><span class="sxs-lookup"><span data-stu-id="625ea-162">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="625ea-163">Voir [masquer le volet vue d’ensemble][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="625ea-163">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
        
1.  <span data-ttu-id="625ea-164">Après l’ouverture de DevTools, elle enregistre l’activité réseau dans le journal du réseau.</span><span class="sxs-lookup"><span data-stu-id="625ea-164">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="625ea-165">Pour en expliquer le résultat, observez d’abord la partie inférieure du **Journal du réseau** et prenez note de la dernière activité.</span><span class="sxs-lookup"><span data-stu-id="625ea-165">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="625ea-166">À présent, sélectionnez le bouton **obtenir des données** dans la démonstration.</span><span class="sxs-lookup"><span data-stu-id="625ea-166">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="625ea-167">Regardez de nouveau le journal du **réseau** .</span><span class="sxs-lookup"><span data-stu-id="625ea-167">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="625ea-168">Une nouvelle ressource doit apparaître `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="625ea-168">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="625ea-169">Le fait de sélectionner le bouton **Get Data** a entraîné la demande de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="625ea-169">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    > ##### <span data-ttu-id="625ea-170">Figure 6</span><span class="sxs-lookup"><span data-stu-id="625ea-170">Figure 6</span></span>  
    > <span data-ttu-id="625ea-171">Nouvelle ressource dans le journal réseau</span><span class="sxs-lookup"><span data-stu-id="625ea-171">A new resource in the Network Log</span></span>  
    > <span data-ttu-id="625ea-172">! [Une nouvelle ressource dans le journal du réseau] [ImagesTutorialRuntime]</span><span class="sxs-lookup"><span data-stu-id="625ea-172">![A new resource in the Network Log][ImagesTutorialRuntime]</span></span>  

## <span data-ttu-id="625ea-173">Afficher plus d’informations</span><span class="sxs-lookup"><span data-stu-id="625ea-173">Show more information</span></span>   

<span data-ttu-id="625ea-174">Les colonnes du journal du réseau peuvent être configurées.</span><span class="sxs-lookup"><span data-stu-id="625ea-174">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="625ea-175">Vous pouvez masquer les colonnes que vous n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="625ea-175">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="625ea-176">Il existe également plusieurs colonnes qui sont masquées par défaut, qui peuvent être utiles.</span><span class="sxs-lookup"><span data-stu-id="625ea-176">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="625ea-177">Cliquez avec le bouton droit sur l’en-tête de la table Journal du réseau et sélectionnez **Domain (domaine**).</span><span class="sxs-lookup"><span data-stu-id="625ea-177">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="625ea-178">Le domaine de chaque ressource est désormais affiché.</span><span class="sxs-lookup"><span data-stu-id="625ea-178">The domain of each resource is now shown.</span></span>  
    
    > ##### <span data-ttu-id="625ea-179">Figure 7</span><span class="sxs-lookup"><span data-stu-id="625ea-179">Figure 7</span></span>  
    > <span data-ttu-id="625ea-180">Activation de la colonne Domain</span><span class="sxs-lookup"><span data-stu-id="625ea-180">Enabling the Domain column</span></span>  
    > <span data-ttu-id="625ea-181">! [Activation de la colonne Domain] [ImagesTutorialDomain]</span><span class="sxs-lookup"><span data-stu-id="625ea-181">![Enabling the Domain column][ImagesTutorialDomain]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="625ea-182">Pour afficher l’URL complète d’une ressource, placez le pointeur de la souris sur la cellule de la colonne **nom** .</span><span class="sxs-lookup"><span data-stu-id="625ea-182">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  

## <span data-ttu-id="625ea-183">Simuler une connexion réseau plus lente</span><span class="sxs-lookup"><span data-stu-id="625ea-183">Simulate a slower network connection</span></span>   

<span data-ttu-id="625ea-184">La connexion réseau de l’ordinateur que vous utilisez pour créer des sites est probablement plus rapide que les connexions réseau des appareils mobiles de vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="625ea-184">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="625ea-185">La limitation de la page vous permet d’obtenir une meilleure idée du temps nécessaire au chargement d’une page sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="625ea-185">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="625ea-186">Sélectionner la liste déroulante de **limitation** , définie sur **en ligne** par défaut.</span><span class="sxs-lookup"><span data-stu-id="625ea-186">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    > ##### <span data-ttu-id="625ea-187">Figure8</span><span class="sxs-lookup"><span data-stu-id="625ea-187">Figure 8</span></span>  
    > <span data-ttu-id="625ea-188">Activation de la limitation</span><span class="sxs-lookup"><span data-stu-id="625ea-188">Enabling throttling</span></span>  
    > <span data-ttu-id="625ea-189">! [Activation de la limitation] [ImagesTutorialThrottling]</span><span class="sxs-lookup"><span data-stu-id="625ea-189">![Enabling throttling][ImagesTutorialThrottling]</span></span>  
    
1.  <span data-ttu-id="625ea-190">Sélectionnez **3G lente**.</span><span class="sxs-lookup"><span data-stu-id="625ea-190">Select **Slow 3G**.</span></span>  
    
    > ##### <span data-ttu-id="625ea-191">Figure9</span><span class="sxs-lookup"><span data-stu-id="625ea-191">Figure 9</span></span>  
    > <span data-ttu-id="625ea-192">Sélection du réseau 3G lent</span><span class="sxs-lookup"><span data-stu-id="625ea-192">Selecting Slow 3G</span></span>  
    > <span data-ttu-id="625ea-193">! [Sélection du réseau 3G lente] [ImagesTutorialSlow3G]</span><span class="sxs-lookup"><span data-stu-id="625ea-193">![Selecting Slow 3G][ImagesTutorialSlow3G]</span></span>  
    
1.  <span data-ttu-id="625ea-194">Appuyez de façon prolongée **sur recharger** ![ ][ImageRefreshIcon] et sélectionnez Vider le **cache**.</span><span class="sxs-lookup"><span data-stu-id="625ea-194">Long-press **Reload** ![Reload][ImageRefreshIcon] and then select **Empty Cache And Hard Reload**.</span></span>  
    
    > ##### <span data-ttu-id="625ea-195">Figure10</span><span class="sxs-lookup"><span data-stu-id="625ea-195">Figure 10</span></span>  
    > <span data-ttu-id="625ea-196">Vider le cache et procéder au recharge</span><span class="sxs-lookup"><span data-stu-id="625ea-196">Empty Cache And Hard Reload</span></span>  
    > <span data-ttu-id="625ea-197">! [Vider le cache et télécharger le matériel] [ImagesTutorialHardReload]</span><span class="sxs-lookup"><span data-stu-id="625ea-197">![Empty Cache And Hard Reload][ImagesTutorialHardReload]</span></span>  
    
    <span data-ttu-id="625ea-198">Lorsque vous révisez les visites, le navigateur fournit généralement certains fichiers du [cache][MDNHTTPCache] , ce qui accélère le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="625ea-198">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache] , which speeds up the page load.</span></span>  <span data-ttu-id="625ea-199">Le **vidage du cache et du rechargement forcé** force le navigateur à accéder au réseau pour toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="625ea-199">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="625ea-200">Cette méthode est utile lorsque vous souhaitez voir la façon dont un visiteur commence à se charger de la page.</span><span class="sxs-lookup"><span data-stu-id="625ea-200">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="625ea-201">Le flux **de travail vider le cache et le chargement papier** est uniquement disponible lorsque devtools est ouvert.</span><span class="sxs-lookup"><span data-stu-id="625ea-201">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  

## <span data-ttu-id="625ea-202">Capture de captures d’écran</span><span class="sxs-lookup"><span data-stu-id="625ea-202">Capture screenshots</span></span>   

<span data-ttu-id="625ea-203">Les captures d’écran vous permettent de voir l’aspect d’une page au fil du temps pendant son chargement.</span><span class="sxs-lookup"><span data-stu-id="625ea-203">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="625ea-204">Sélectionnez ![ paramètres ][ImageSettingsIcon] du réseau, puis activez la case à cocher capturer les captures d' **écran** .</span><span class="sxs-lookup"><span data-stu-id="625ea-204">Select ![Network settings][ImageSettingsIcon] and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="625ea-205">Rechargez de nouveau la page par le biais du flux **de travail vider le cache et le chargement papier** .</span><span class="sxs-lookup"><span data-stu-id="625ea-205">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="625ea-206">Pour savoir comment procéder, voir [simuler une connexion plus lente](#simulate-a-slower-network-connection) si vous avez besoin d’un rappel.</span><span class="sxs-lookup"><span data-stu-id="625ea-206">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="625ea-207">Le volet capture d’écran fournit des miniatures illustrant la manière dont la page a été recherchée à différents points au cours du processus de chargement.</span><span class="sxs-lookup"><span data-stu-id="625ea-207">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    > ##### <span data-ttu-id="625ea-208">Figure11</span><span class="sxs-lookup"><span data-stu-id="625ea-208">Figure 11</span></span>  
    > <span data-ttu-id="625ea-209">Captures d’écran du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="625ea-209">Screenshots of the page load</span></span>  
    > <span data-ttu-id="625ea-210">! [Captures d’écran du chargement de la page] [ImagesTutorialAllScreenshots]</span><span class="sxs-lookup"><span data-stu-id="625ea-210">![Screenshots of the page load][ImagesTutorialAllScreenshots]</span></span>  

1.  <span data-ttu-id="625ea-211">Sélectionnez la première miniature.</span><span class="sxs-lookup"><span data-stu-id="625ea-211">Select the first thumbnail.</span></span>  <span data-ttu-id="625ea-212">DevTools indique l’activité réseau qui se produit à ce moment précis.</span><span class="sxs-lookup"><span data-stu-id="625ea-212">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    > ##### <span data-ttu-id="625ea-213">Figure12</span><span class="sxs-lookup"><span data-stu-id="625ea-213">Figure 12</span></span>  
    > <span data-ttu-id="625ea-214">Activité réseau qui se produit pendant la première capture d’écran</span><span class="sxs-lookup"><span data-stu-id="625ea-214">The network activity that was happening during the first screenshot</span></span>  
    > <span data-ttu-id="625ea-215">! [Activité réseau qui se produisait pendant la première capture d’écran] [ImagesTutorialFirstScreenshot]</span><span class="sxs-lookup"><span data-stu-id="625ea-215">![The network activity that was happening during the first screenshot][ImagesTutorialFirstScreenshot]</span></span>  

1.  <span data-ttu-id="625ea-216">Cliquez de ![ ][ImageSettingsIcon] nouveau sur paramètres du réseau et désélectionnez la case à cocher capturer les captures d' **écran** pour fermer le volet captures d’écran.</span><span class="sxs-lookup"><span data-stu-id="625ea-216">Select ![Network settings][ImageSettingsIcon] again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="625ea-217">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="625ea-217">Reload the page again.</span></span>  

## <span data-ttu-id="625ea-218">Inspecter les détails de la ressource</span><span class="sxs-lookup"><span data-stu-id="625ea-218">Inspect the details of the resource</span></span>   

<span data-ttu-id="625ea-219">Pour plus d’informations à ce sujet, sélectionnez une ressource.</span><span class="sxs-lookup"><span data-stu-id="625ea-219">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="625ea-220">Essayez-le maintenant:</span><span class="sxs-lookup"><span data-stu-id="625ea-220">Try it now:</span></span>  

1.  <span data-ttu-id="625ea-221">Sélectionnez `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="625ea-221">Select `getstarted.html`.</span></span>  <span data-ttu-id="625ea-222">L’onglet **en-têtes** est affiché.</span><span class="sxs-lookup"><span data-stu-id="625ea-222">The **Headers** tab is shown.</span></span>  <span data-ttu-id="625ea-223">Utilisez cet onglet pour inspecter les en-têtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="625ea-223">Use this tab to inspect HTTP headers.</span></span>  
    
    > ##### <span data-ttu-id="625ea-224">Figure13</span><span class="sxs-lookup"><span data-stu-id="625ea-224">Figure 13</span></span>  
    > <span data-ttu-id="625ea-225">Onglet en-têtes</span><span class="sxs-lookup"><span data-stu-id="625ea-225">The Headers tab</span></span>  
    > <span data-ttu-id="625ea-226">! [Onglet en-têtes] [ImagesTutorialHeaders]</span><span class="sxs-lookup"><span data-stu-id="625ea-226">![The Headers tab][ImagesTutorialHeaders]</span></span>  
    
1.  <span data-ttu-id="625ea-227">Sélectionnez l’onglet **Aperçu** .  Un rendu de base du code HTML est affiché.</span><span class="sxs-lookup"><span data-stu-id="625ea-227">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    > ##### <span data-ttu-id="625ea-228">Figure14</span><span class="sxs-lookup"><span data-stu-id="625ea-228">Figure 14</span></span>  
    > <span data-ttu-id="625ea-229">Onglet Aperçu</span><span class="sxs-lookup"><span data-stu-id="625ea-229">The Preview tab</span></span>  
    > <span data-ttu-id="625ea-230">! [Onglet Aperçu] [ImagesTutorialPreview]</span><span class="sxs-lookup"><span data-stu-id="625ea-230">![The Preview tab][ImagesTutorialPreview]</span></span>  

     <span data-ttu-id="625ea-231">Cet onglet est utile lorsqu’une API renvoie un code d’erreur en HTML.</span><span class="sxs-lookup"><span data-stu-id="625ea-231">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="625ea-232">Il est possible que vous puissiez lire le code HTML affiché plus facilement que le code source HTML ou lorsque vous examinez des images.</span><span class="sxs-lookup"><span data-stu-id="625ea-232">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="625ea-233">Sélectionnez l’onglet **réponse** .  Le code source HTML est affiché.</span><span class="sxs-lookup"><span data-stu-id="625ea-233">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    > ##### <span data-ttu-id="625ea-234">Figure15</span><span class="sxs-lookup"><span data-stu-id="625ea-234">Figure 15</span></span>  
    > <span data-ttu-id="625ea-235">Onglet réponse</span><span class="sxs-lookup"><span data-stu-id="625ea-235">The Response tab</span></span>  
    > <span data-ttu-id="625ea-236">! [Onglet réponse] [ImagesTutorialResponse]</span><span class="sxs-lookup"><span data-stu-id="625ea-236">![The Response tab][ImagesTutorialResponse]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="625ea-237">Lorsqu’un fichier est minified, le fait de sélectionner le bouton format de **mise** ![ en forme ][ImageFormatIcon] en bas de l’onglet **réponse** reformate le contenu du fichier pour faciliter la lecture.</span><span class="sxs-lookup"><span data-stu-id="625ea-237">When a file is minified, selecting the **Format** ![Format][ImageFormatIcon] button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  

1.  <span data-ttu-id="625ea-238">Sélectionnez l’onglet **minutage** .  Le détail de l’activité réseau de cette ressource est affiché.</span><span class="sxs-lookup"><span data-stu-id="625ea-238">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    > ##### <span data-ttu-id="625ea-239">Figure16</span><span class="sxs-lookup"><span data-stu-id="625ea-239">Figure 16</span></span>  
    > <span data-ttu-id="625ea-240">Onglet Minutage</span><span class="sxs-lookup"><span data-stu-id="625ea-240">The Timing tab</span></span>  
    > <span data-ttu-id="625ea-241">! [Onglet Minutage] [ImagesTutorialTiming]</span><span class="sxs-lookup"><span data-stu-id="625ea-241">![The Timing tab][ImagesTutorialTiming]</span></span>  

1.  <span data-ttu-id="625ea-242">**Close** ![ ][ImageCloseIcon] Pour afficher de nouveau le journal du réseau, sélectionnez Fermer.</span><span class="sxs-lookup"><span data-stu-id="625ea-242">Select **Close** ![Close][ImageCloseIcon] to view the Network Log again.</span></span>  
    
    > ##### <span data-ttu-id="625ea-243">Figure17</span><span class="sxs-lookup"><span data-stu-id="625ea-243">Figure 17</span></span>  
    > <span data-ttu-id="625ea-244">Bouton Fermer</span><span class="sxs-lookup"><span data-stu-id="625ea-244">The Close button</span></span>  
    > <span data-ttu-id="625ea-245">! [Bouton Fermer] [ImagesTutorialCloseTiming]</span><span class="sxs-lookup"><span data-stu-id="625ea-245">![The Close button][ImagesTutorialCloseTiming]</span></span>  

## <span data-ttu-id="625ea-246">Effectuer une recherche dans les en-têtes et réponses du réseau</span><span class="sxs-lookup"><span data-stu-id="625ea-246">Search network headers and responses</span></span>   

<span data-ttu-id="625ea-247">Le volet de **recherche** vous permet d’effectuer une recherche dans les en-têtes et réponses HTTP de toutes les ressources pour une chaîne ou une expression régulière spécifique.</span><span class="sxs-lookup"><span data-stu-id="625ea-247">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="625ea-248">Par exemple, supposons que vous vouliez vérifier que vos ressources utilisent des **stratégies de cache**raisonnables.</span><span class="sxs-lookup"><span data-stu-id="625ea-248">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="625ea-249">Sélectionnez **Rechercher dans Search** ![ ][ImageSearchIcon] .</span><span class="sxs-lookup"><span data-stu-id="625ea-249">Select **Search** ![Search][ImageSearchIcon].</span></span>  <span data-ttu-id="625ea-250">Le volet de recherche s’ouvre à gauche du journal du réseau.</span><span class="sxs-lookup"><span data-stu-id="625ea-250">The Search pane opens to the left of the Network log.</span></span>  
    
    > ##### <span data-ttu-id="625ea-251">Figure 18</span><span class="sxs-lookup"><span data-stu-id="625ea-251">Figure 18</span></span>  
    > <span data-ttu-id="625ea-252">Le volet de recherche</span><span class="sxs-lookup"><span data-stu-id="625ea-252">The Search pane</span></span>  
    > <span data-ttu-id="625ea-253">! [Volet de recherche] [ImagesTutorialSearch]</span><span class="sxs-lookup"><span data-stu-id="625ea-253">![The Search pane][ImagesTutorialSearch]</span></span>  

1.  <span data-ttu-id="625ea-254">Tapez `Cache-Control` et appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="625ea-254">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="625ea-255">Le volet de recherche répertorie toutes les instances `Cache-Control` qu’il recherche dans les en-têtes de ressources ou le contenu.</span><span class="sxs-lookup"><span data-stu-id="625ea-255">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    > ##### <span data-ttu-id="625ea-256">Figure 19</span><span class="sxs-lookup"><span data-stu-id="625ea-256">Figure 19</span></span>  
    > <span data-ttu-id="625ea-257">Résultats de la recherche pour </span><span class="sxs-lookup"><span data-stu-id="625ea-257">Search results for</span></span> `Cache-Control`  
    > <span data-ttu-id="625ea-258">! [Résultats de recherche pour Cache-Control] [ImagesTutorialResults]</span><span class="sxs-lookup"><span data-stu-id="625ea-258">![Search results for Cache-Control][ImagesTutorialResults]</span></span>  

1.  <span data-ttu-id="625ea-259">Sélectionnez un résultat pour afficher la ressource dans laquelle le résultat a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="625ea-259">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="625ea-260">Si vous examinez les détails de la ressource, sélectionnez un résultat pour y accéder directement.</span><span class="sxs-lookup"><span data-stu-id="625ea-260">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="625ea-261">Par exemple, si la requête se trouve dans un en-tête, l’onglet en-têtes s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="625ea-261">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="625ea-262">Si la requête se trouve dans le contenu, l’onglet **réponse** s’ouvre.</span><span class="sxs-lookup"><span data-stu-id="625ea-262">If the query was found in content, the **Response** tab opens.</span></span>  
    
    > ##### <span data-ttu-id="625ea-263">Figure 20</span><span class="sxs-lookup"><span data-stu-id="625ea-263">Figure 20</span></span>  
    > <span data-ttu-id="625ea-264">Résultat de la recherche en surbrillance dans l’onglet en-têtes</span><span class="sxs-lookup"><span data-stu-id="625ea-264">A search result highlighted in the Headers tab</span></span>  
    > <span data-ttu-id="625ea-265">! [Un résultat de recherche en surbrillance dans l’onglet en-têtes] [ImagesTutorialCache]</span><span class="sxs-lookup"><span data-stu-id="625ea-265">![A search result highlighted in the Headers tab][ImagesTutorialCache]</span></span>  
    
1.  <span data-ttu-id="625ea-266">Fermez le volet de recherche et l’onglet en-têtes.</span><span class="sxs-lookup"><span data-stu-id="625ea-266">Close the Search pane and the Headers tab.</span></span>  
    
    > ##### <span data-ttu-id="625ea-267">Figure 21</span><span class="sxs-lookup"><span data-stu-id="625ea-267">Figure 21</span></span>  
    > <span data-ttu-id="625ea-268">Boutons Fermer</span><span class="sxs-lookup"><span data-stu-id="625ea-268">The Close buttons</span></span>  
    > <span data-ttu-id="625ea-269">! [Boutons Fermer] [ImagesTutorialCloseButtons]</span><span class="sxs-lookup"><span data-stu-id="625ea-269">![The Close buttons][ImagesTutorialCloseButtons]</span></span>  
    
## <span data-ttu-id="625ea-270">Filtrer les ressources</span><span class="sxs-lookup"><span data-stu-id="625ea-270">Filter resources</span></span>   

<span data-ttu-id="625ea-271">DevTools fournit de nombreux flux de travail pour filtrer les ressources qui ne sont pas pertinentes pour la tâche en cours.</span><span class="sxs-lookup"><span data-stu-id="625ea-271">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

> ##### <span data-ttu-id="625ea-272">Figure 22</span><span class="sxs-lookup"><span data-stu-id="625ea-272">Figure 22</span></span>  
> <span data-ttu-id="625ea-273">Barre d’outils filtres</span><span class="sxs-lookup"><span data-stu-id="625ea-273">The Filters toolbar</span></span>  
> <span data-ttu-id="625ea-274">! [Barre d’outils filtres] [ImagesTutorialFilters]</span><span class="sxs-lookup"><span data-stu-id="625ea-274">![The Filters toolbar][ImagesTutorialFilters]</span></span>  

<span data-ttu-id="625ea-275">Par défaut, la barre d’outils **filtres** doit être activée.</span><span class="sxs-lookup"><span data-stu-id="625ea-275">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="625ea-276">Si ce n’est pas le cas:</span><span class="sxs-lookup"><span data-stu-id="625ea-276">If not:</span></span>  

1.  <span data-ttu-id="625ea-277">Sélectionnez **Filter** ![ filtre ][ImageFilterIcon] de filtre pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="625ea-277">Select **Filter** ![Filter][ImageFilterIcon] to show it.</span></span>  

### <span data-ttu-id="625ea-278">Filtrer par chaîne, expression régulière ou propriété</span><span class="sxs-lookup"><span data-stu-id="625ea-278">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="625ea-279">La zone de texte **filtre** prend en charge différents types de filtrage.</span><span class="sxs-lookup"><span data-stu-id="625ea-279">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="625ea-280">Entrez `png` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="625ea-280">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="625ea-281">Seuls les fichiers qui contiennent le texte `png` sont affichés.</span><span class="sxs-lookup"><span data-stu-id="625ea-281">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="625ea-282">Dans ce cas, les seuls fichiers correspondant au filtre sont les images PNG.</span><span class="sxs-lookup"><span data-stu-id="625ea-282">In this case the only files that match the filter are the PNG images.</span></span>  
    
    > ##### <span data-ttu-id="625ea-283">Figure 23</span><span class="sxs-lookup"><span data-stu-id="625ea-283">Figure 23</span></span>  
    > <span data-ttu-id="625ea-284">Filtre de chaîne</span><span class="sxs-lookup"><span data-stu-id="625ea-284">A string filter</span></span>  
    > <span data-ttu-id="625ea-285">! [Filtre de chaîne] [ImagesTutorialPNG]</span><span class="sxs-lookup"><span data-stu-id="625ea-285">![A string filter][ImagesTutorialPNG]</span></span>  

1.  <span data-ttu-id="625ea-286">Entrez `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="625ea-286">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="625ea-287">DevTools filtre les ressources dont le nom ne se termine pas par un `j` ou après `c` suivi de 1 ou plusieurs `s` caractères.</span><span class="sxs-lookup"><span data-stu-id="625ea-287">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    > ##### <span data-ttu-id="625ea-288">Figure 24</span><span class="sxs-lookup"><span data-stu-id="625ea-288">Figure 24</span></span>  
    > <span data-ttu-id="625ea-289">Un filtre d’expression régulier</span><span class="sxs-lookup"><span data-stu-id="625ea-289">A regular expression filter</span></span>  
    > <span data-ttu-id="625ea-290">! [Filtre d’expression régulière] [ImagesTutorialRegEx]</span><span class="sxs-lookup"><span data-stu-id="625ea-290">![A regular expression filter][ImagesTutorialRegEx]</span></span>  
    
1.  <span data-ttu-id="625ea-291">Entrez `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="625ea-291">Type `-main.css`.</span></span>  <span data-ttu-id="625ea-292">DevTools filtre `main.css` .</span><span class="sxs-lookup"><span data-stu-id="625ea-292">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="625ea-293">Si un autre fichier correspond au modèle, il sera également filtré.</span><span class="sxs-lookup"><span data-stu-id="625ea-293">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    > ##### <span data-ttu-id="625ea-294">Figure 25</span><span class="sxs-lookup"><span data-stu-id="625ea-294">Figure 25</span></span>  
    > <span data-ttu-id="625ea-295">Un filtre négatif</span><span class="sxs-lookup"><span data-stu-id="625ea-295">A negative filter</span></span>  
    > <span data-ttu-id="625ea-296">! [Un filtre négatif] [ImagesTutorialNegative]</span><span class="sxs-lookup"><span data-stu-id="625ea-296">![A negative filter][ImagesTutorialNegative]</span></span>  
    
1.  <span data-ttu-id="625ea-297">Entrez `domain:cdn.glitch.com` dans la zone de texte du **filtre** .</span><span class="sxs-lookup"><span data-stu-id="625ea-297">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="625ea-298">DevTools filtre les ressources disposant d’une URL qui ne correspond pas à ce domaine.</span><span class="sxs-lookup"><span data-stu-id="625ea-298">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    > ##### <span data-ttu-id="625ea-299">Figure 26</span><span class="sxs-lookup"><span data-stu-id="625ea-299">Figure 26</span></span>  
    > <span data-ttu-id="625ea-300">Filtre de propriétés</span><span class="sxs-lookup"><span data-stu-id="625ea-300">A property filter</span></span>  
    > <span data-ttu-id="625ea-301">! [Filtre de propriétés] [ImagesTutorialProperty]</span><span class="sxs-lookup"><span data-stu-id="625ea-301">![A property filter][ImagesTutorialProperty]</span></span>  

    <span data-ttu-id="625ea-302">Pour obtenir la liste complète des propriétés filtrées [, voir filtrer les demandes par propriétés][DevtoolsReferenceProperty] .</span><span class="sxs-lookup"><span data-stu-id="625ea-302">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
    
1.  <span data-ttu-id="625ea-303">Effacez la zone de texte du **filtre** d’un texte.</span><span class="sxs-lookup"><span data-stu-id="625ea-303">Clear the **Filter** text box of any text.</span></span>  

### <span data-ttu-id="625ea-304">Filtrer par type de ressource</span><span class="sxs-lookup"><span data-stu-id="625ea-304">Filter by resource type</span></span>   

<span data-ttu-id="625ea-305">Pour vous concentrer sur un certain type de fichier, tel que les feuilles de style:</span><span class="sxs-lookup"><span data-stu-id="625ea-305">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="625ea-306">Sélectionnez **CSS**.</span><span class="sxs-lookup"><span data-stu-id="625ea-306">Select **CSS**.</span></span>  <span data-ttu-id="625ea-307">Tous les autres types de fichiers sont filtrés.</span><span class="sxs-lookup"><span data-stu-id="625ea-307">All other file types are filtered out.</span></span>  
    
    > ##### <span data-ttu-id="625ea-308">Figure 27</span><span class="sxs-lookup"><span data-stu-id="625ea-308">Figure 27</span></span>  
    > <span data-ttu-id="625ea-309">Affichage des fichiers CSS uniquement</span><span class="sxs-lookup"><span data-stu-id="625ea-309">Showing CSS files only</span></span>  
    > <span data-ttu-id="625ea-310">! [Affichage des fichiers CSS uniquement] [ImagesTutorialCSS]</span><span class="sxs-lookup"><span data-stu-id="625ea-310">![Showing CSS files only][ImagesTutorialCSS]</span></span>  
    
1.  <span data-ttu-id="625ea-311">Pour afficher les scripts, vous pouvez également appuyer sur `Control` \ (Windows \) ou `Command` \ (MacOS \), puis sélectionner **js**.</span><span class="sxs-lookup"><span data-stu-id="625ea-311">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    > ##### <span data-ttu-id="625ea-312">Figure 28</span><span class="sxs-lookup"><span data-stu-id="625ea-312">Figure 28</span></span>  
    > <span data-ttu-id="625ea-313">Affichage des fichiers CSS et JS uniquement</span><span class="sxs-lookup"><span data-stu-id="625ea-313">Showing CSS and JS files only</span></span>  
    > <span data-ttu-id="625ea-314">! [Affichage des fichiers CSS et JS uniquement] [ImagesTutorialCSSJS]</span><span class="sxs-lookup"><span data-stu-id="625ea-314">![Showing CSS and JS files only][ImagesTutorialCSSJS]</span></span>  
    
1.  <span data-ttu-id="625ea-315">**Tout** sélectionner pour supprimer les filtres et afficher de nouveau toutes les ressources.</span><span class="sxs-lookup"><span data-stu-id="625ea-315">Select **All** to remove the filters and see all resources again.</span></span>  

<span data-ttu-id="625ea-316">Pour plus d’autres flux de travail de filtrage, voir [Filtrer les demandes][DevtoolsNetworkReferenceFilter] .</span><span class="sxs-lookup"><span data-stu-id="625ea-316">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="625ea-317">Bloquer les demandes</span><span class="sxs-lookup"><span data-stu-id="625ea-317">Block requests</span></span>   

<span data-ttu-id="625ea-318">Quel est l’aspect et le comportement d’une page lorsque certaines ressources de la page ne sont pas disponibles?</span><span class="sxs-lookup"><span data-stu-id="625ea-318">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="625ea-319">Est-ce que l’opération échoue entièrement ou fonctionne-t-elle toujours?</span><span class="sxs-lookup"><span data-stu-id="625ea-319">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="625ea-320">Bloquer les requêtes à Rechercher:</span><span class="sxs-lookup"><span data-stu-id="625ea-320">Block requests to find out:</span></span>  

1.  <span data-ttu-id="625ea-321">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le **menu de commandes**.</span><span class="sxs-lookup"><span data-stu-id="625ea-321">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="625ea-322">Figure 29</span><span class="sxs-lookup"><span data-stu-id="625ea-322">Figure 29</span></span>  
    > <span data-ttu-id="625ea-323">Menu de commandes</span><span class="sxs-lookup"><span data-stu-id="625ea-323">The Command Menu</span></span>  
    > <span data-ttu-id="625ea-324">! [Le menu de commandes] [ImagesTutorialCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="625ea-324">![The Command Menu][ImagesTutorialCommandMenu]</span></span>  
    
1.  <span data-ttu-id="625ea-325">Tapez `block` , sélectionnez **afficher le blocage de requête**, puis appuyez sur `Enter` .</span><span class="sxs-lookup"><span data-stu-id="625ea-325">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="625ea-326">Figure 30</span><span class="sxs-lookup"><span data-stu-id="625ea-326">Figure 30</span></span>  
    > <span data-ttu-id="625ea-327">Afficher le blocage de requête</span><span class="sxs-lookup"><span data-stu-id="625ea-327">Show Request Blocking</span></span>  
    > <span data-ttu-id="625ea-328">! [Afficher une demande de blocage] [ImagesTutorialBlock]</span><span class="sxs-lookup"><span data-stu-id="625ea-328">![Show Request Blocking][ImagesTutorialBlock]</span></span>  

1.  <span data-ttu-id="625ea-329">Sélectionnez **Ajouter** un modèle ajouter un modèle ![ ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="625ea-329">Select **Add Pattern** ![Add Pattern][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="625ea-330">Entrez `main.css`.</span><span class="sxs-lookup"><span data-stu-id="625ea-330">Type `main.css`.</span></span>  
    
    > ##### <span data-ttu-id="625ea-331">Figure 31</span><span class="sxs-lookup"><span data-stu-id="625ea-331">Figure 31</span></span>  
    > <span data-ttu-id="625ea-332">Bloquer</span><span class="sxs-lookup"><span data-stu-id="625ea-332">Blocking</span></span> `main.css`  
    > <span data-ttu-id="625ea-333">! [Blocage de main. CSS] [ImagesTutorialAddBlock]</span><span class="sxs-lookup"><span data-stu-id="625ea-333">![Blocking main.css][ImagesTutorialAddBlock]</span></span>  
    
1.  <span data-ttu-id="625ea-334">Cliquez sur **Ajouter**.</span><span class="sxs-lookup"><span data-stu-id="625ea-334">Select **Add**.</span></span>  
1.  <span data-ttu-id="625ea-335">Rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="625ea-335">Reload the page.</span></span>  <span data-ttu-id="625ea-336">Comme prévu, le style de la page est légèrement gâché, car la feuille de style principale a été bloquée.</span><span class="sxs-lookup"><span data-stu-id="625ea-336">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="625ea-337">`main.css`Ligne du journal du réseau.</span><span class="sxs-lookup"><span data-stu-id="625ea-337">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="625ea-338">Le texte rouge signifie que la ressource a été bloquée.</span><span class="sxs-lookup"><span data-stu-id="625ea-338">The red text means that the resource was blocked.</span></span>
    
    > ##### <span data-ttu-id="625ea-339">Figure 32</span><span class="sxs-lookup"><span data-stu-id="625ea-339">Figure 32</span></span>  
    > `main.css` <span data-ttu-id="625ea-340">a été bloqué</span><span class="sxs-lookup"><span data-stu-id="625ea-340">has been blocked</span></span>  
    > <span data-ttu-id="625ea-341">! [main. CSS a été bloqué] [ImagesTutorialBlockedStyles]</span><span class="sxs-lookup"><span data-stu-id="625ea-341">![main.css has been blocked][ImagesTutorialBlockedStyles]</span></span>  

1.  <span data-ttu-id="625ea-342">Désélectionnez la case à cocher **activer le blocage de requête** .</span><span class="sxs-lookup"><span data-stu-id="625ea-342">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="625ea-343">Conclusion</span><span class="sxs-lookup"><span data-stu-id="625ea-343">Conclusion</span></span>  

<span data-ttu-id="625ea-344">Félicitations, vous avez terminé le didacticiel.</span><span class="sxs-lookup"><span data-stu-id="625ea-344">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="625ea-345">Vous savez maintenant comment utiliser le panneau réseau dans Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="625ea-345">You now know how to use the Network panel in the Microsoft Edge DevTools!</span></span>






<span data-ttu-id="625ea-346">Consultez la [référence réseau][DevtoolsNetworkReference] pour découvrir d’autres fonctionnalités devtools liées à l’examen de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="625ea-346">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Figure 1: démonstration"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-console.msft.png "figure 2: console"  
[ImagesTutorialDocked]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-console-Bottom.msft.png "figure 3: DevTools ancré en bas de la fenêtre"  
[ImagesTutorialNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Bottom.msft.png "figure 4: DevTools ancré en bas de la fenêtre"  
[ImagesTutorialLog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network.msft.png "figure 5: journal réseau"  
[ImagesTutorialRuntime]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-New-Resource.msft.png "figure 6: une nouvelle ressource du journal du réseau"  
[ImagesTutorialDomain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Edit-Column.msft.png "figure 7: activation de la colonne Domain"  
[ImagesTutorialThrottling]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-throttling.msft.png "figure 8: activation de la limitation"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-throttling-Slow-3G.msft.png "figure 9: sélectionner la fonction 3G lente"  
[ImagesTutorialHardReload]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Empty-cache-and-hard-reset.msft.png "figure 10: vider le cache et le recharger"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-screenshots.msft.png "figure 11: captures d’écran du chargement de la page"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-screenshots-First.msft.png "figure 12: activité réseau qui se produit pendant la première capture d’écran"  
[ImagesTutorialHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-headers.msft.png "figure 13: onglet en-têtes"  
[ImagesTutorialPreview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-preview.msft.png "figure 14: onglet Aperçu"  
[ImagesTutorialResponse]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Response.msft.png "figure 15: onglet réponse"  
[ImagesTutorialTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-timing.msft.png "figure 16: onglet Minutage"  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Resources-Close-Tabs.msft.png "figure 17: bouton Fermer"  
[ImagesTutorialSearch]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Empty.msft.png "figure 18: volet de recherche"  
[ImagesTutorialResults]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control.msft.png "figure 19: résultats de recherche pour Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Cache-Control-headers-Response-headers.msft.png "figure 20: un résultat de recherche mis en surbrillance dans l’onglet en-têtes"  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Search-Close.msft.png "figure 21: boutons Fermer"  
[ImagesTutorialFilters]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Empty.msft.png "figure 22: barre d’outils filtres"  
[ImagesTutorialPNG]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-png.msft.png "figure 23: filtre de chaîne"  
[ImagesTutorialRegEx]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Regex.msft.png "figure 24: filtre d’expression régulière"  
[ImagesTutorialNegative]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Negative-Statement.msft.png "figure 25: filtre négatif"  
[ImagesTutorialProperty]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-Property-value.msft.png "figure 26: filtre de propriété"  
[ImagesTutorialCSS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-file-type-CSS.msft.png "figure 27: affichage des fichiers CSS uniquement"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-Filter-file-type-CSS-js.msft.png "figure 28: affichage des fichiers CSS et JS uniquement"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Empty.msft.png "figure 29: menu commande"  
[ImagesTutorialBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block.msft.png "figure 30: afficher le blocage de requête"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-Add-Pattern.msft.png "figure 31: blocage de main. css"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Network-glitch-Network-CLI-Block-main-CSS.msft.png "figure 32: main. CSS a été bloqué"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Référence d’analyse du réseau"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Demandes de filtre-référence d’analyse du réseau"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Masquer le volet vue d’ensemble-référence d’analyse du réseau"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Demandes de filtre par propriétés-référence d’analyse du réseau"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Consulter la démonstration d’activité réseau"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Mise en cache HTTP MDN"  

> [!NOTE]
> <span data-ttu-id="625ea-388">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="625ea-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="625ea-389">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/network/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="625ea-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="625ea-391">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="625ea-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
