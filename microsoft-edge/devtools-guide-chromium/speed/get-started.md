---
title: Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 7efc76fbcb3d1ed6cbd0760f789c8c952030d70c
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611888"
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





# <span data-ttu-id="07557-103">Optimiser la vitesse de votre site Web avec Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="07557-103">Optimize Website Speed With Microsoft Edge DevTools</span></span>   



## <span data-ttu-id="07557-104">Objectif du didacticiel</span><span class="sxs-lookup"><span data-stu-id="07557-104">Goal of tutorial</span></span>  

<span data-ttu-id="07557-105">Ce didacticiel vous explique comment utiliser Microsoft Edge DevTools pour trouver des méthodes pour accélérer le chargement de vos sites Web.</span><span class="sxs-lookup"><span data-stu-id="07557-105">This tutorial teaches you how to use Microsoft Edge DevTools to find ways to make your websites load faster.</span></span>  

## <span data-ttu-id="07557-106">Conditions préalables</span><span class="sxs-lookup"><span data-stu-id="07557-106">Prerequisites</span></span>  

*   <span data-ttu-id="07557-107">Vous devez avoir une connaissance de base du développement Web, semblable à ce qui est enseigné dans cette [Introduction à la classe de développement Web][CourseraIntroductionWebDevelopmentClass].</span><span class="sxs-lookup"><span data-stu-id="07557-107">You should have basic web development experience, similar to what is taught in this [Introduction to Web Development class][CourseraIntroductionWebDevelopmentClass].</span></span>  
*   <span data-ttu-id="07557-108">Vous n’avez aucune information sur les performances du chargement.</span><span class="sxs-lookup"><span data-stu-id="07557-108">You do not need to know anything about load performance.</span></span>  <span data-ttu-id="07557-109">Pour plus d’informations, consultez ce didacticiel.</span><span class="sxs-lookup"><span data-stu-id="07557-109">You learn about it in this tutorial!</span></span>  

## <span data-ttu-id="07557-110">Introduction</span><span class="sxs-lookup"><span data-stu-id="07557-110">Introduction</span></span>   

<span data-ttu-id="07557-111">C’est Thomas.</span><span class="sxs-lookup"><span data-stu-id="07557-111">This is Tony.</span></span>  <span data-ttu-id="07557-112">Thierry est très célèbre dans la société de chat.</span><span class="sxs-lookup"><span data-stu-id="07557-112">Tony is very famous in cat society.</span></span>  <span data-ttu-id="07557-113">Il a créé un site Web de telle sorte que ses fans puissent en savoir plus sur ses produits préférés.</span><span class="sxs-lookup"><span data-stu-id="07557-113">He has built a website so that his fans are able to learn about his favorite foods.</span></span>  <span data-ttu-id="07557-114">Ses fans aiment le site, mais Thomas cesse d’entendre que le site se charge lentement.</span><span class="sxs-lookup"><span data-stu-id="07557-114">His fans love the site, but Tony keeps hearing complaints that the site loads slowly.</span></span>  <span data-ttu-id="07557-115">Thomas vous a demandé de lui permettre d’accélérer le site.</span><span class="sxs-lookup"><span data-stu-id="07557-115">Tony has asked you to help him speed the site up.</span></span>  

> ##### <span data-ttu-id="07557-116">Figure1</span><span class="sxs-lookup"><span data-stu-id="07557-116">Figure 1</span></span>  
> <span data-ttu-id="07557-117">Bernard le chat</span><span class="sxs-lookup"><span data-stu-id="07557-117">Tony the cat</span></span>  
> ![Bernard le chat][ImageTony]  

## <span data-ttu-id="07557-119">Étape 1: Auditez le site</span><span class="sxs-lookup"><span data-stu-id="07557-119">Step 1: Audit the site</span></span>   

<span data-ttu-id="07557-120">Dès que vous avez fini d’améliorer les performances de chargement d’un site, **Commencez toujours par un audit**.</span><span class="sxs-lookup"><span data-stu-id="07557-120">Whenever you set out to improve the load performance of a site, **always start with an audit**.</span></span>  
<span data-ttu-id="07557-121">L’audit comporte 2 fonctions importantes:</span><span class="sxs-lookup"><span data-stu-id="07557-121">The audit has 2 important functions:</span></span>  

*   <span data-ttu-id="07557-122">Il crée un **planning de référence** pour vous pour mesurer les changements ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="07557-122">It creates a **baseline** for you to measure subsequent changes against.</span></span>  
*   <span data-ttu-id="07557-123">Ce service vous donne des **conseils utiles** sur les modifications qui ont le plus d’impact.</span><span class="sxs-lookup"><span data-stu-id="07557-123">It gives you **actionable tips** on what changes have the most impact.</span></span>  

### <span data-ttu-id="07557-124">Configuration</span><span class="sxs-lookup"><span data-stu-id="07557-124">Set up</span></span>   

<span data-ttu-id="07557-125">Tout d’abord, vous devez configurer le site pour pouvoir le modifier ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="07557-125">First, you must set up the site so that you are able to make changes to it later.</span></span>  

1.  <span data-ttu-id="07557-126">[Ouvrez le code source pour le site](https://glitch.com/edit/#!/tony).</span><span class="sxs-lookup"><span data-stu-id="07557-126">[Open the source code for the site](https://glitch.com/edit/#!/tony).</span></span>  <span data-ttu-id="07557-127">Cet onglet est appelé **onglet Éditeur**.</span><span class="sxs-lookup"><span data-stu-id="07557-127">This tab is referred to as the **editor tab**.</span></span>  
    
    > ##### <span data-ttu-id="07557-128">Figure 2</span><span class="sxs-lookup"><span data-stu-id="07557-128">Figure 2</span></span>  
    > <span data-ttu-id="07557-129">Onglet Éditeur</span><span class="sxs-lookup"><span data-stu-id="07557-129">The editor tab</span></span>  
    > ![Onglet Éditeur][ImageEditor]  

1.  <span data-ttu-id="07557-131">Sélectionnez **Thomas**.</span><span class="sxs-lookup"><span data-stu-id="07557-131">Select **tony**.</span></span>  <span data-ttu-id="07557-132">Un menu s’affiche.</span><span class="sxs-lookup"><span data-stu-id="07557-132">A menu appears.</span></span>  
    
    > ##### <span data-ttu-id="07557-133">Figure3</span><span class="sxs-lookup"><span data-stu-id="07557-133">Figure 3</span></span>  
    > <span data-ttu-id="07557-134">Menu qui apparaît après avoir cliqué sur **Thierry**</span><span class="sxs-lookup"><span data-stu-id="07557-134">The menu that appears after clicking **tony**</span></span>  
    > ![Menu qui apparaît après avoir cliqué sur Thierry][ImageMenu]  
    
1.  <span data-ttu-id="07557-136">Sélectionnez **Remix Project**.</span><span class="sxs-lookup"><span data-stu-id="07557-136">Select **Remix Project**.</span></span>  <span data-ttu-id="07557-137">Le nom du projet **passe de Thomas à un** nom généré de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="07557-137">The name of the project changes from **tony** to some randomly-generated name.</span></span>  <span data-ttu-id="07557-138">Vous disposez maintenant de votre propre copie modifiable du code.</span><span class="sxs-lookup"><span data-stu-id="07557-138">You now have your own editable copy of the code.</span></span>  <span data-ttu-id="07557-139">Par la suite, vous pouvez modifier ce code.</span><span class="sxs-lookup"><span data-stu-id="07557-139">Later on, you may make changes to this code.</span></span>  
1.  <span data-ttu-id="07557-140">Sélectionner **Afficher** et sélectionner **dans une nouvelle fenêtre**.</span><span class="sxs-lookup"><span data-stu-id="07557-140">Select **Show** and select **In a New Window**.</span></span>  <span data-ttu-id="07557-141">La démonstration s’ouvre dans un nouvel onglet.  Cet onglet est appelé **onglet démonstration**.  Le chargement du site risque de prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="07557-141">The demo opens in a new tab.  This tab is be referred to as the **demo tab**.  It may take a while for the site to load.</span></span>  
    
    > ##### <span data-ttu-id="07557-142">Figure 4</span><span class="sxs-lookup"><span data-stu-id="07557-142">Figure 4</span></span>  
    > <span data-ttu-id="07557-143">Onglet démonstration</span><span class="sxs-lookup"><span data-stu-id="07557-143">The demo tab</span></span>  
    > ![Onglet démonstration][ImageDemo]  

1.  <span data-ttu-id="07557-145">Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="07557-145">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="07557-146">Microsoft Edge DevTools s’ouvre à côté de la démonstration.</span><span class="sxs-lookup"><span data-stu-id="07557-146">Microsoft Edge DevTools opens up alongside the demo.</span></span>  
    
    > ##### <span data-ttu-id="07557-147">Figure 5</span><span class="sxs-lookup"><span data-stu-id="07557-147">Figure 5</span></span>  
    > <span data-ttu-id="07557-148">DevTools et la démo</span><span class="sxs-lookup"><span data-stu-id="07557-148">DevTools and the demo</span></span>  
    > ![DevTools et la démo][ImageDevtools]  

<span data-ttu-id="07557-150">Pour le reste des captures d’écran de ce didacticiel, DevTools est affiché dans une fenêtre séparée.</span><span class="sxs-lookup"><span data-stu-id="07557-150">For the rest of the screenshots in this tutorial, DevTools is shown in a separate window.</span></span>  <span data-ttu-id="07557-151">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, `Undock` puis sélectionnez **détacher dans une fenêtre séparée**.</span><span class="sxs-lookup"><span data-stu-id="07557-151">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, typing `Undock`, and then selecting **Undock into separate window**.</span></span>  

> ##### <span data-ttu-id="07557-152">Figure 6</span><span class="sxs-lookup"><span data-stu-id="07557-152">Figure 6</span></span>  
> <span data-ttu-id="07557-153">DevTools non attaché</span><span class="sxs-lookup"><span data-stu-id="07557-153">Undocked DevTools</span></span>  
> ![DevTools non attaché][ImageUndocked]  

### <span data-ttu-id="07557-155">Établir un planning de référence</span><span class="sxs-lookup"><span data-stu-id="07557-155">Establish a baseline</span></span>   

<span data-ttu-id="07557-156">Le planning de référence est un enregistrement de la façon dont le site a été traité avant d’améliorer ses performances.</span><span class="sxs-lookup"><span data-stu-id="07557-156">The baseline is a record of how the site performed before you made any performance improvements.</span></span>  

1.  <span data-ttu-id="07557-157">Sélectionnez l’onglet **audits** .  Il est possible qu’il soit masqué derrière le bouton **autres** ![ panneaux supplémentaires ][ImageMorePanelsIcon] .</span><span class="sxs-lookup"><span data-stu-id="07557-157">Select the **Audits** tab.  It may be hidden behind the **More Panels** ![More Panels][ImageMorePanelsIcon] button.</span></span>  <span data-ttu-id="07557-158">Ce panneau comporte une phare, car le projet qui alimente le panneau d’audit est appelé **phare**.</span><span class="sxs-lookup"><span data-stu-id="07557-158">There is a Lighthouse on this panel because the project that powers the Audits panel is named **Lighthouse**.</span></span>  
    
    [!INCLUDE [audits-panel-note](../includes/audits-panel-note.md)]  
    
    > ##### <span data-ttu-id="07557-159">Figure 7</span><span class="sxs-lookup"><span data-stu-id="07557-159">Figure 7</span></span>  
    > <span data-ttu-id="07557-160">Volet d’audit</span><span class="sxs-lookup"><span data-stu-id="07557-160">The Audits panel</span></span>  
    > ![Volet d’audit][ImageAudits]  
    
    <!--todo: add link to Lighthouse when section is available  -->  
    <!-- /web/tools/lighthouse  -->  
    
1.  <span data-ttu-id="07557-162">Associez vos paramètres de configuration d’audit à ceux de la [figure 7](#figure-7).</span><span class="sxs-lookup"><span data-stu-id="07557-162">Match your audit configuration settings to those in [Figure 7](#figure-7).</span></span>  <span data-ttu-id="07557-163">Voici une explication des différentes options disponibles:</span><span class="sxs-lookup"><span data-stu-id="07557-163">Here is an explanation of the different options:</span></span>  

    *   <span data-ttu-id="07557-164">**Appareil**.</span><span class="sxs-lookup"><span data-stu-id="07557-164">**Device**.</span></span>  <span data-ttu-id="07557-165">Définissez sur **mobile** pour modifier la chaîne de l’agent utilisateur et simuler une fenêtre d’affichage mobile.</span><span class="sxs-lookup"><span data-stu-id="07557-165">Setting to **Mobile** changes the user agent string and simulates a mobile viewport.</span></span>  <span data-ttu-id="07557-166">Le paramétrage sur **Bureau** à peu près empêche uniquement les changements de **mobilité** .</span><span class="sxs-lookup"><span data-stu-id="07557-166">Setting to **Desktop** pretty much just disables the **Mobile** changes.</span></span>  
    *   <span data-ttu-id="07557-167">Les **audits**.</span><span class="sxs-lookup"><span data-stu-id="07557-167">**Audits**.</span></span>  <span data-ttu-id="07557-168">La désactivation d’une catégorie empêche le panneau d’audit d’exécuter ces audits et exclut ces audits de votre rapport.</span><span class="sxs-lookup"><span data-stu-id="07557-168">Disabling a category prevents the Audits panel from running those audits, and excludes those audits from your report.</span></span>  <span data-ttu-id="07557-169">Laissez les autres catégories activées si vous voulez voir les types de recommandations qui s’offrent à vous.</span><span class="sxs-lookup"><span data-stu-id="07557-169">Leave the other categories enabled, if you want to see the types of recommendations that are provide.</span></span>  <span data-ttu-id="07557-170">La désactivation des catégories accélère légèrement le processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="07557-170">Disabling categories slightly speeds up the auditing process.</span></span>  
    *   <span data-ttu-id="07557-171">**Limitation**.</span><span class="sxs-lookup"><span data-stu-id="07557-171">**Throttling**.</span></span>  <span data-ttu-id="07557-172">Pour simuler la fonction de **4G lente, le ralenti de l’UC 4x** simule les conditions typiques de navigation sur un appareil mobile.</span><span class="sxs-lookup"><span data-stu-id="07557-172">Setting to **Simulated Slow 4G, 4x CPU Slowdown** simulates the typical conditions of browsing on a mobile device.</span></span>  <span data-ttu-id="07557-173">Son nom est «simulé», car le panneau d’audit n’est pas réellement limité lors du processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="07557-173">It is named "simulated" because the Audits panel does not actually throttle during the auditing process.</span></span>  <span data-ttu-id="07557-174">Au lieu de cela, il s’agit simplement de l’extrapolation du temps nécessaire au chargement de la page dans des conditions mobiles.</span><span class="sxs-lookup"><span data-stu-id="07557-174">Instead, it just extrapolates how long the page would take to load under mobile conditions.</span></span>  <span data-ttu-id="07557-175">En revanche, le paramètre **appliedd...** , qui a pour effet de limiter votre processeur et votre réseau, par le biais d’un processus d’audit plus long.</span><span class="sxs-lookup"><span data-stu-id="07557-175">The **Applied...** setting, on the other hand, actually throttles your CPU and network, with the tradeoff of a longer auditing process.</span></span>  
    *   <span data-ttu-id="07557-176">**Vider le stockage**.</span><span class="sxs-lookup"><span data-stu-id="07557-176">**Clear Storage**.</span></span>  <span data-ttu-id="07557-177">Activez cette case à cocher pour effacer tout le stockage associé à la page avant chaque audit.</span><span class="sxs-lookup"><span data-stu-id="07557-177">Enabling this checkbox clears all storage associated with the page before every audit.</span></span>  <span data-ttu-id="07557-178">Ne renseignez pas ce paramètre si vous souhaitez vérifier la manière dont les visiteurs de votre site se familiarisent avec la première fois.</span><span class="sxs-lookup"><span data-stu-id="07557-178">Leave this setting on if you want to audit how first-time visitors experience your site.</span></span>  <span data-ttu-id="07557-179">Désactivez ce paramètre si vous souhaitez utiliser la répétition d’une visite.</span><span class="sxs-lookup"><span data-stu-id="07557-179">Disable this setting when you want the repeat-visit experience.</span></span>  

1.  <span data-ttu-id="07557-180">Sélectionnez **exécuter les audits**.</span><span class="sxs-lookup"><span data-stu-id="07557-180">Select **Run Audits**.</span></span>  <span data-ttu-id="07557-181">Après 10 à 30 secondes, le volet d’audit affiche un rapport sur les performances de votre site.</span><span class="sxs-lookup"><span data-stu-id="07557-181">After 10 to 30 seconds, the Audits panel shows you a report of the performance of the site.</span></span>  
    
    > ##### <span data-ttu-id="07557-182">Figure8</span><span class="sxs-lookup"><span data-stu-id="07557-182">Figure 8</span></span>  
    > <span data-ttu-id="07557-183">Rapport du volet d’audit des performances du site</span><span class="sxs-lookup"><span data-stu-id="07557-183">The report for the Audits panel of the performance of the site</span></span>  
    > ![Rapport du volet d’audit des performances du site][ImageReport]  

#### <span data-ttu-id="07557-185">Gestion des erreurs de rapport</span><span class="sxs-lookup"><span data-stu-id="07557-185">Handling report errors</span></span>   

<span data-ttu-id="07557-186">Si un message d’erreur apparaît dans votre rapport du panneau d’audit, essayez d’exécuter l’onglet démonstration à partir d’une fenêtre **InPrivate** sans afficher d’autres onglets.</span><span class="sxs-lookup"><span data-stu-id="07557-186">If you ever get an error in your Audits panel report, try running the demo tab from an **InPrivate** window with no other tabs open.</span></span>  <span data-ttu-id="07557-187">Cela garantit que vous exécutez Microsoft Edge à partir de l’État Clean.</span><span class="sxs-lookup"><span data-stu-id="07557-187">This ensures that you are running Microsoft Edge from a clean state.</span></span>  <span data-ttu-id="07557-188">Les extensions Microsoft Edge en particulier interfèrent souvent avec le processus d’audit.</span><span class="sxs-lookup"><span data-stu-id="07557-188">Microsoft Edge Extensions in particular often interfere with the auditing process.</span></span>  

<!--todo: add screen capture for error in audit -->  
<!--
> ##### old Figure 9  
> A report that errored  
> ![A report that errored][ImageError]  
-->  

### <span data-ttu-id="07557-189">Comprendre votre état</span><span class="sxs-lookup"><span data-stu-id="07557-189">Understand your report</span></span>   

<span data-ttu-id="07557-190">Le nombre situé en haut de votre état correspond au score de performance global du site.</span><span class="sxs-lookup"><span data-stu-id="07557-190">The number at the top of your report is the overall performance score for the site.</span></span>  <span data-ttu-id="07557-191">Par la suite, au fur et à mesure que vous apportez des modifications à votre code, vous devriez voir ce numéro augmenter.</span><span class="sxs-lookup"><span data-stu-id="07557-191">Later, as you make changes to the code, you should see this number rise.</span></span>  <span data-ttu-id="07557-192">Un résultat plus élevé correspond à de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="07557-192">A higher score means better performance.</span></span>  

> ##### <span data-ttu-id="07557-193">Figure9</span><span class="sxs-lookup"><span data-stu-id="07557-193">Figure 9</span></span>  
> <span data-ttu-id="07557-194">Le score de performance global</span><span class="sxs-lookup"><span data-stu-id="07557-194">The overall performance score</span></span>  
> <span data-ttu-id="07557-195">! [Score global de performance] [ImageOverall]</span><span class="sxs-lookup"><span data-stu-id="07557-195">![The overall performance score][ImageOverall]</span></span>  

<span data-ttu-id="07557-196">La section **mesures** fournit des mesures quantitatives des performances du site.</span><span class="sxs-lookup"><span data-stu-id="07557-196">The **Metrics** section provides quantitative measurements of the performance of the site.</span></span>  <span data-ttu-id="07557-197">Chaque métrique donne un aperçu d’un aspect différent des performances.</span><span class="sxs-lookup"><span data-stu-id="07557-197">Each metric provides insight into a different aspect of the performance.</span></span>  <span data-ttu-id="07557-198">Par exemple, lorsque le contenu est dessiné à l’écran pour **la première fois** , il s’agit d’un jalon important dans la perception de l’utilisateur du chargement de la page, alors que le **temps nécessaire à l’interactivité** correspond au point où la page semble suffisamment prête pour gérer les interactions utilisateur.</span><span class="sxs-lookup"><span data-stu-id="07557-198">For example, **First Contentful Paint** tells you when content is first painted to the screen, which is an important milestone in the user's perception of the page load, whereas **Time To Interactive** marks the point at which the page appears ready enough to handle user interactions.</span></span>  

> ##### <span data-ttu-id="07557-199">Figure10</span><span class="sxs-lookup"><span data-stu-id="07557-199">Figure 10</span></span>  
> <span data-ttu-id="07557-200">Section mesures</span><span class="sxs-lookup"><span data-stu-id="07557-200">The Metrics section</span></span>  
> <span data-ttu-id="07557-201">! [Section indicateurs] [ImageMetrics]</span><span class="sxs-lookup"><span data-stu-id="07557-201">![The Metrics section][ImageMetrics]</span></span>  

<span data-ttu-id="07557-202">Sélectionnez le bouton bascule surligné en [figure 11](#figure-11) pour afficher une description de chaque métrique, puis cliquez sur **en savoir plus** pour lire la documentation correspondante.</span><span class="sxs-lookup"><span data-stu-id="07557-202">Select the highlighted toggle button in [Figure 11](#figure-11) to see a description for each metric, and click **Learn More** to read documentation about it.</span></span>  

> ##### <span data-ttu-id="07557-203">Figure11</span><span class="sxs-lookup"><span data-stu-id="07557-203">Figure 11</span></span>  
> <span data-ttu-id="07557-204">Sélectionner le bouton bascule surligné pour développer les éléments **métriques**</span><span class="sxs-lookup"><span data-stu-id="07557-204">Select the highlighted toggle button to expand the **Metrics** items</span></span>  
> <span data-ttu-id="07557-205">! [Sélectionnez le bouton bascule surligné pour développer les éléments métriques] [ImageFirstMeaningfulPaint]</span><span class="sxs-lookup"><span data-stu-id="07557-205">![Select the highlighted toggle button to expand the Metrics items][ImageFirstMeaningfulPaint]</span></span>  

<span data-ttu-id="07557-206">Le sous-métrique est une collection de captures d’écran qui vous montrent le mode de chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-206">Below Metrics is a collection of screenshots that show you how the page looked as it loaded.</span></span>  

> ##### <span data-ttu-id="07557-207">Figure12</span><span class="sxs-lookup"><span data-stu-id="07557-207">Figure 12</span></span>  
> <span data-ttu-id="07557-208">Captures d’écran illustrant l’apparence de la page en cours de chargement</span><span class="sxs-lookup"><span data-stu-id="07557-208">Screenshots of how the page looked while loading</span></span>  
> <span data-ttu-id="07557-209">! [Capture d’écran illustrant l’apparence de la page en cours de chargement] [ImageScreenshots]</span><span class="sxs-lookup"><span data-stu-id="07557-209">![Screenshots of how the page looked while loading][ImageScreenshots]</span></span>  

<span data-ttu-id="07557-210">La section **opportunités** fournit des conseils spécifiques pour améliorer les performances de chargement de cette page spécifique.</span><span class="sxs-lookup"><span data-stu-id="07557-210">The **Opportunities** section provides specific tips on how to improve the load performance of this specific page.</span></span>  

> ##### <span data-ttu-id="07557-211">Figure13</span><span class="sxs-lookup"><span data-stu-id="07557-211">Figure 13</span></span>  
> <span data-ttu-id="07557-212">Section opportunités</span><span class="sxs-lookup"><span data-stu-id="07557-212">The Opportunities section</span></span>  
> <span data-ttu-id="07557-213">! [Section opportunités] [ImageOpportunities]</span><span class="sxs-lookup"><span data-stu-id="07557-213">![The Opportunities section][ImageOpportunities]</span></span>  

<span data-ttu-id="07557-214">Sélectionnez une opportunité pour en savoir plus à son sujet.</span><span class="sxs-lookup"><span data-stu-id="07557-214">Select an opportunity to learn more about it.</span></span>  

> ##### <span data-ttu-id="07557-215">Figure14</span><span class="sxs-lookup"><span data-stu-id="07557-215">Figure 14</span></span>  
> <span data-ttu-id="07557-216">**Éliminer l’opportunité de blocage des ressources de blocage des rendez-** vous</span><span class="sxs-lookup"><span data-stu-id="07557-216">**Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="07557-217">! [Éliminer l’opportunité de blocage des ressources de blocage de rendu] [ImageCompression]</span><span class="sxs-lookup"><span data-stu-id="07557-217">![Eliminate render-blocking resources opportunity][ImageCompression]</span></span>  

<span data-ttu-id="07557-218">Pour plus d’informations sur les raisons de la nécessité d’une opportunité, voir **en savoir plus** sur la résolution des problèmes.</span><span class="sxs-lookup"><span data-stu-id="07557-218">Select **Learn More** to see documentation about why an opportunity is important, and specific recommendations on how to fix it.</span></span>  

> ##### <span data-ttu-id="07557-219">Figure15</span><span class="sxs-lookup"><span data-stu-id="07557-219">Figure 15</span></span>  
> <span data-ttu-id="07557-220">Documentation pour l’opportunité de **suppression des ressources de blocage de rendu**</span><span class="sxs-lookup"><span data-stu-id="07557-220">Documentation for the **Eliminate render-blocking resources** opportunity</span></span>  
> <span data-ttu-id="07557-221">! [Documentation pour l’opportunité de suppression des ressources de blocage de rendu] [ImageReference]</span><span class="sxs-lookup"><span data-stu-id="07557-221">![Documentation for the Eliminate render-blocking resources opportunity][ImageReference]</span></span>  

<span data-ttu-id="07557-222">La section **Diagnostics** fournit des informations supplémentaires sur les facteurs qui contribuent au temps de chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-222">The **Diagnostics** section provides more information about factors that contribute to the load time of the page.</span></span>  

> ##### <span data-ttu-id="07557-223">Figure16</span><span class="sxs-lookup"><span data-stu-id="07557-223">Figure 16</span></span>  
> <span data-ttu-id="07557-224">Section Diagnostics</span><span class="sxs-lookup"><span data-stu-id="07557-224">The Diagnostics section</span></span>  
> <span data-ttu-id="07557-225">! [Section Diagnostics] [ImageDiagnostics]</span><span class="sxs-lookup"><span data-stu-id="07557-225">![The Diagnostics section][ImageDiagnostics]</span></span>  

<span data-ttu-id="07557-226">La section **contrôles réussis** vous montre le fonctionnement correct du site.</span><span class="sxs-lookup"><span data-stu-id="07557-226">The **Passed Audits** section shows you what the site is doing correctly.</span></span>  <span data-ttu-id="07557-227">Pour développer la section.</span><span class="sxs-lookup"><span data-stu-id="07557-227">Select to expand the section.</span></span>  

> ##### <span data-ttu-id="07557-228">Figure17</span><span class="sxs-lookup"><span data-stu-id="07557-228">Figure 17</span></span>  
> <span data-ttu-id="07557-229">Section audits transmis</span><span class="sxs-lookup"><span data-stu-id="07557-229">The Passed Audits section</span></span>  
> <span data-ttu-id="07557-230">! [Section réussite d’audit] [ImagePassed]</span><span class="sxs-lookup"><span data-stu-id="07557-230">![The Passed Audits section][ImagePassed]</span></span>  

## <span data-ttu-id="07557-231">Étape 2: expérimenter</span><span class="sxs-lookup"><span data-stu-id="07557-231">Step 2: Experiment</span></span>   

<span data-ttu-id="07557-232">La section opportunités de votre rapport d’audit vous donne des conseils pour améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-232">The Opportunities section of your audit report gives you tips on how to improve the performance of the page.</span></span>  <span data-ttu-id="07557-233">Dans cette section, vous implémentez les modifications recommandées sur le code base, puis vous auditez le site après chaque modification pour mesurer la vitesse de votre site.</span><span class="sxs-lookup"><span data-stu-id="07557-233">In this section, you implement the recommended changes to the codebase, auditing the site after each change to measure how it affects site speed.</span></span>  

### <span data-ttu-id="07557-234">Activer la compression de texte</span><span class="sxs-lookup"><span data-stu-id="07557-234">Enable text compression</span></span>   

<span data-ttu-id="07557-235">Votre rapport déclare qu’il n’est pas l’une des principales opportunités d’améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-235">Your report says that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="07557-236">L’activation de la compression de texte permet d’améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-236">Enabling text compression is an opportunity to improve the performance of the page.</span></span>  

<span data-ttu-id="07557-237">La compression de texte est celle qui consiste à réduire ou compresser la taille d’un fichier texte avant de l’envoyer sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="07557-237">Text compression is when you reduce, or compress, the size of a text file before sending it over the network.</span></span>  <span data-ttu-id="07557-238">Type semblable à la façon dont vous pouvez Zipper un dossier avant de l’envoyer par courrier électronique afin de réduire la taille.</span><span class="sxs-lookup"><span data-stu-id="07557-238">Kind of like how you might zip a folder before emailing it to reduce the size.</span></span>  

<span data-ttu-id="07557-239">Avant d’activer la compression, voici quelques méthodes permettant de vérifier manuellement si les ressources de texte sont comprimées.</span><span class="sxs-lookup"><span data-stu-id="07557-239">Before you enable compression, here are a couple of ways to manually check whether text resources are compressed.</span></span>  

1.  <span data-ttu-id="07557-240">Sélectionnez l’onglet **Network (réseau** ).</span><span class="sxs-lookup"><span data-stu-id="07557-240">Select the **Network** tab.</span></span>  
    
    > ##### <span data-ttu-id="07557-241">Figure 18</span><span class="sxs-lookup"><span data-stu-id="07557-241">Figure 18</span></span>  
    > <span data-ttu-id="07557-242">Panneau réseau</span><span class="sxs-lookup"><span data-stu-id="07557-242">The Network panel</span></span>  
    > <span data-ttu-id="07557-243">! [Panneau réseau] [ImageNetwork]</span><span class="sxs-lookup"><span data-stu-id="07557-243">![The Network panel][ImageNetwork]</span></span>  
    
1.  <span data-ttu-id="07557-244">Sélectionnez l’icône du **paramètre réseau** .</span><span class="sxs-lookup"><span data-stu-id="07557-244">Select the **Network setting** icon.</span></span>  
1.  <span data-ttu-id="07557-245">Cochez la case **utiliser des lignes de requête volumineuses** .</span><span class="sxs-lookup"><span data-stu-id="07557-245">Select the **Use Large Request Rows** checkbox.</span></span>  <span data-ttu-id="07557-246">La hauteur des lignes du tableau de requêtes réseau augmente.</span><span class="sxs-lookup"><span data-stu-id="07557-246">The height of the rows in the table of network requests increases.</span></span>  
    
    > ##### <span data-ttu-id="07557-247">Figure 19</span><span class="sxs-lookup"><span data-stu-id="07557-247">Figure 19</span></span>  
    > <span data-ttu-id="07557-248">Lignes de grande taille dans la table requêtes réseau</span><span class="sxs-lookup"><span data-stu-id="07557-248">Large rows in the network requests table</span></span>  
    > <span data-ttu-id="07557-249">! [Lignes de grande taille dans la table requêtes réseau] [ImageLargeRows]</span><span class="sxs-lookup"><span data-stu-id="07557-249">![Large rows in the network requests table][ImageLargeRows]</span></span>  
    
1.  <span data-ttu-id="07557-250">Si vous ne voyez pas la colonne **taille** dans le tableau des requêtes réseau, cliquez sur l’en-tête de la table, puis sélectionnez **taille**.</span><span class="sxs-lookup"><span data-stu-id="07557-250">If you do not see the **Size** column in the table of network requests, click the table header and then select **Size**.</span></span>  

<span data-ttu-id="07557-251">Chaque cellule **taille** affiche deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="07557-251">Each **Size** cell shows two values.</span></span>  <span data-ttu-id="07557-252">La valeur supérieure correspond à la taille de la ressource téléchargée.</span><span class="sxs-lookup"><span data-stu-id="07557-252">The top value is the size of the downloaded resource.</span></span>  
<span data-ttu-id="07557-253">La valeur inférieure correspond à la taille de la ressource non compressée.</span><span class="sxs-lookup"><span data-stu-id="07557-253">The bottom value is the size of the uncompressed resource.</span></span>  <span data-ttu-id="07557-254">Si les deux valeurs sont identiques, la ressource n’est pas compressée lors de son envoi via le réseau.</span><span class="sxs-lookup"><span data-stu-id="07557-254">If the two values are the same, then the resource is not being compressed when it is sent over the network.</span></span>  <span data-ttu-id="07557-255">Par exemple, dans la [figure 19](#figure-19) , les premières et dernières valeurs de `bundle.js` sont `1.2 MB` et `1.2 MB` .</span><span class="sxs-lookup"><span data-stu-id="07557-255">For example, in [Figure 19](#figure-19) the top and bottom values for `bundle.js` are `1.2 MB` and `1.2 MB`.</span></span>  

<span data-ttu-id="07557-256">Vérifiez la compression en inspectant les en-têtes HTTP d’une ressource:</span><span class="sxs-lookup"><span data-stu-id="07557-256">Check for compression by inspecting the HTTP headers of a resource:</span></span>  

1.  <span data-ttu-id="07557-257">Sélectionnez **bundle. js**.</span><span class="sxs-lookup"><span data-stu-id="07557-257">Select **bundle.js**.</span></span>  
1.  <span data-ttu-id="07557-258">Sélectionnez l’onglet **en-têtes** .</span><span class="sxs-lookup"><span data-stu-id="07557-258">Select the **Headers** tab.</span></span>  
    
    > ##### <span data-ttu-id="07557-259">Figure 20</span><span class="sxs-lookup"><span data-stu-id="07557-259">Figure 20</span></span>  
    > <span data-ttu-id="07557-260">Onglet en-têtes</span><span class="sxs-lookup"><span data-stu-id="07557-260">The Headers tab</span></span>  
    > <span data-ttu-id="07557-261">! [Onglet en-têtes] [ImageHeaders]</span><span class="sxs-lookup"><span data-stu-id="07557-261">![The Headers tab][ImageHeaders]</span></span>  
    
1.  <span data-ttu-id="07557-262">Recherchez un en-tête dans la section **en-têtes de réponse** `content-encoding` .</span><span class="sxs-lookup"><span data-stu-id="07557-262">Search the **Response Headers** section for a `content-encoding` header.</span></span>  <span data-ttu-id="07557-263">Vous ne devez pas voir l’une d’elles, ce qui signifie qu’elle n' `bundle.js` a pas été compactée.</span><span class="sxs-lookup"><span data-stu-id="07557-263">You should not see one, meaning that `bundle.js` was not compressed.</span></span>  <span data-ttu-id="07557-264">Lorsqu’une ressource est compressée, cet en-tête est généralement défini sur `gzip` , `deflate` ou `br` .</span><span class="sxs-lookup"><span data-stu-id="07557-264">When a resource is compressed, this header is usually set to `gzip`, `deflate`, or `br`.</span></span>  <span data-ttu-id="07557-265">Pour obtenir une description de ces valeurs, voir [directives][MDNContentEncodingDirectives] .</span><span class="sxs-lookup"><span data-stu-id="07557-265">See [Directives][MDNContentEncodingDirectives] for an explanation of these values.</span></span>  

<span data-ttu-id="07557-266">C’est suffisant pour les explications.</span><span class="sxs-lookup"><span data-stu-id="07557-266">Enough with the explanations.</span></span>  <span data-ttu-id="07557-267">Le moment est venu d’apporter des modifications.</span><span class="sxs-lookup"><span data-stu-id="07557-267">Time to make some changes!</span></span>  <span data-ttu-id="07557-268">Autorisez la compression de texte en ajoutant quelques lignes de code:</span><span class="sxs-lookup"><span data-stu-id="07557-268">Enable text compression by adding a couple of lines of code:</span></span>  

1.  <span data-ttu-id="07557-269">Dans l’onglet Éditeur, cliquez sur **serveur. js**.</span><span class="sxs-lookup"><span data-stu-id="07557-269">In the editor tab, click **server.js**.</span></span>  
    
    > ##### <span data-ttu-id="07557-270">Figure 21</span><span class="sxs-lookup"><span data-stu-id="07557-270">Figure 21</span></span>  
    > <span data-ttu-id="07557-271">Modification de Server. js</span><span class="sxs-lookup"><span data-stu-id="07557-271">Editing server.js</span></span>  
    > <span data-ttu-id="07557-272">! [Édition Server. js] [ImageServer]</span><span class="sxs-lookup"><span data-stu-id="07557-272">![Editing server.js][ImageServer]</span></span>  
    
1.  <span data-ttu-id="07557-273">Ajoutez le code suivant à **Server. js**.</span><span class="sxs-lookup"><span data-stu-id="07557-273">Add the following code to **server.js**.</span></span>  <span data-ttu-id="07557-274">Assurez-vous d’entrer `app.use(compression())` auparavant `app.use(express.static('build'))` .</span><span class="sxs-lookup"><span data-stu-id="07557-274">Make sure to put `app.use(compression())` before `app.use(express.static('build'))`.</span></span>  

    ```javascript
    const express = require('express');
    const app = express();
    const fs = require('fs');
    const compression = require('compression');

    app.use(compression());
    app.use(express.static('build'));
    
    const listener = app.listen(process.env.PORT || 1234, function () {
        console.log(`Listening on port ${listener.address().port}`);
    });
    ```  
    
    > [!NOTE]
    > <span data-ttu-id="07557-275">En règle générale, vous devez installer le `compression` package par le biais d’une expression similaire `npm i -S compression` , mais cela a déjà été fait pour vous.</span><span class="sxs-lookup"><span data-stu-id="07557-275">Usually, you have to install the `compression` package via something like `npm i -S compression`, but this has already been done for you.</span></span>  
    
1.  <span data-ttu-id="07557-276">Patientez pendant le déploiement de la nouvelle version du site.</span><span class="sxs-lookup"><span data-stu-id="07557-276">Wait for Glitch to deploy the new build of the site.</span></span>  <span data-ttu-id="07557-277">L’animation fantaisie en regard des **Outils** signifie que le site est en cours de recréation et de redéploiement.</span><span class="sxs-lookup"><span data-stu-id="07557-277">The fancy animation next to **Tools** means that the site is getting rebuilt and redeployed.</span></span>  <span data-ttu-id="07557-278">La modification est prête lorsque l’animation en regard des **Outils** est en suspens.</span><span class="sxs-lookup"><span data-stu-id="07557-278">The change is ready when the animation next to **Tools** goes away.</span></span>  <span data-ttu-id="07557-279">Sélectionnez **Afficher** et sélectionnez **de nouveau dans une nouvelle fenêtre** .</span><span class="sxs-lookup"><span data-stu-id="07557-279">Select **Show** and select **In a New Window** again.</span></span>  
    
    <!--
    > ##### Old Figure 22  
    > The animation that indicates that the site is getting built  
    > ![The animation that indicates that the site is getting built][ImageBuilding]  
    -->  
    
<span data-ttu-id="07557-280">Utilisez les flux de travail que vous avez appris précédemment pour vérifier que la compression fonctionne:</span><span class="sxs-lookup"><span data-stu-id="07557-280">Use the workflows that you learned earlier to manually check that the compression is working:</span></span>  

1.  <span data-ttu-id="07557-281">Revenez à l’onglet démonstration et rechargez la page.</span><span class="sxs-lookup"><span data-stu-id="07557-281">Go back to the demo tab and reload the page.</span></span>  <span data-ttu-id="07557-282">La colonne **taille** doit maintenant afficher 2 valeurs différentes pour les ressources de texte comme `bundle.js` .</span><span class="sxs-lookup"><span data-stu-id="07557-282">The **Size** column should now show 2 different values for text resources like `bundle.js`.</span></span>  <span data-ttu-id="07557-283">Dans la [figure 23](#figure-23) , la valeur la plus haute de `256 KB` pour `bundle.js` correspond à la taille du fichier envoyé sur le réseau et la valeur inférieure de `1.2 MB` correspond à la taille de fichier non comprimé.</span><span class="sxs-lookup"><span data-stu-id="07557-283">In [Figure 23](#figure-23) the top value of `256 KB` for `bundle.js` is the size of the file that was sent over the network, and the bottom value of `1.2 MB` is the uncompressed file size.</span></span>  
    
    > ##### <span data-ttu-id="07557-284">Figure 22</span><span class="sxs-lookup"><span data-stu-id="07557-284">Figure 22</span></span>  
    > <span data-ttu-id="07557-285">La colonne taille affiche désormais 2 valeurs différentes pour les ressources de texte</span><span class="sxs-lookup"><span data-stu-id="07557-285">The Size column now shows 2 different values for text resources</span></span>  
    > <span data-ttu-id="07557-286">! [La colonne taille affiche désormais 2 valeurs différentes pour les ressources de texte] [ImageRequests]</span><span class="sxs-lookup"><span data-stu-id="07557-286">![The Size column now shows 2 different values for text resources][ImageRequests]</span></span>  
    
1.  <span data-ttu-id="07557-287">La section **en-têtes de réponse** de `bundle.js` devrait désormais inclure un `content-encoding: gzip` en-tête.</span><span class="sxs-lookup"><span data-stu-id="07557-287">The **Response Headers** section for `bundle.js` should now include a `content-encoding: gzip` header.</span></span>
    
    > ##### <span data-ttu-id="07557-288">Figure 23</span><span class="sxs-lookup"><span data-stu-id="07557-288">Figure 23</span></span>  
    > <span data-ttu-id="07557-289">La section en-têtes de réponse contient désormais un en-tête de codage de contenu</span><span class="sxs-lookup"><span data-stu-id="07557-289">The Response Headers section now contains a content-encoding header</span></span>  
    > <span data-ttu-id="07557-290">! [La section en-têtes de réponse contient désormais un en-tête d’encodage de contenu] [ImageGzip]</span><span class="sxs-lookup"><span data-stu-id="07557-290">![The Response Headers section now contains a content-encoding header][ImageGzip]</span></span>  
    
<span data-ttu-id="07557-291">Auditez de nouveau la page pour mesurer le type de compression de texte d’impact sur les performances de chargement de la page:</span><span class="sxs-lookup"><span data-stu-id="07557-291">Audit the page again to measure what kind of impact text compression has on the load performance of the page:</span></span>  

1.  <span data-ttu-id="07557-292">Sélectionnez l’onglet **audits** .</span><span class="sxs-lookup"><span data-stu-id="07557-292">Select the **Audits** tab.</span></span>  
1.  <span data-ttu-id="07557-293">Activez l’option **effectuer un** audit ![ ][ImagePerformIcon] .</span><span class="sxs-lookup"><span data-stu-id="07557-293">Select **Perform an audit** ![Perform an audit][ImagePerformIcon].</span></span>  
1.  <span data-ttu-id="07557-294">Ne modifiez pas les paramètres comme auparavant.</span><span class="sxs-lookup"><span data-stu-id="07557-294">Leave the settings the same as before.</span></span>  
1.  <span data-ttu-id="07557-295">Sélectionnez **exécuter l’audit**.</span><span class="sxs-lookup"><span data-stu-id="07557-295">Select **Run audit**.</span></span>  
    
    > ##### <span data-ttu-id="07557-296">Figure 24</span><span class="sxs-lookup"><span data-stu-id="07557-296">Figure 24</span></span>  
    > <span data-ttu-id="07557-297">Rapport d’audit après l’activation de la compression de texte</span><span class="sxs-lookup"><span data-stu-id="07557-297">An Audits report after enabling text compression</span></span>  
    > <span data-ttu-id="07557-298">! [Rapport de vérification après activation de la compression de texte] [ImageReport2]</span><span class="sxs-lookup"><span data-stu-id="07557-298">![An Audits report after enabling text compression][ImageReport2]</span></span>  
    
<span data-ttu-id="07557-299">Woohoo!</span><span class="sxs-lookup"><span data-stu-id="07557-299">Woohoo!</span></span>  <span data-ttu-id="07557-300">Cela se présente comme la progression.</span><span class="sxs-lookup"><span data-stu-id="07557-300">That looks like progress.</span></span>  <span data-ttu-id="07557-301">Le score de performance global doit être plus élevé, ce qui signifie que le site est plus rapide.</span><span class="sxs-lookup"><span data-stu-id="07557-301">Your overall performance score should have increased, meaning that the site is getting faster.</span></span>  

#### <span data-ttu-id="07557-302">Compression de texte dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="07557-302">Text compression in the real world</span></span>   

<span data-ttu-id="07557-303">La plupart des serveurs possèdent réellement des correctifs simples, comme pour l’activation du compactage.</span><span class="sxs-lookup"><span data-stu-id="07557-303">Most servers really do have simple fixes like this for enabling compression!</span></span>  <span data-ttu-id="07557-304">Il suffit de procéder à une recherche pour configurer le serveur que vous utilisez pour compresser le texte.</span><span class="sxs-lookup"><span data-stu-id="07557-304">Just do a search on how to configure whatever server you use to compress text.</span></span>  

### <span data-ttu-id="07557-305">Redimensionner des images</span><span class="sxs-lookup"><span data-stu-id="07557-305">Resize images</span></span>   

<span data-ttu-id="07557-306">Votre rapport indique qu’il est recommandé d’éviter les charges utiles réseau énormes pour améliorer les performances de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-306">Your report indicates that avoiding enormous network payloads is one of the top opportunities for improving the performance of the page.</span></span>  <span data-ttu-id="07557-307">Le redimensionnement des images permet de réduire la taille de la charge utile du réseau.</span><span class="sxs-lookup"><span data-stu-id="07557-307">Resizing images helps reduce the size of the network payload.</span></span>  <span data-ttu-id="07557-308">Si votre utilisateur consulte vos images sur un écran d’appareil mobile d’une largeur de 500 pixels, il n’y a rien de plus que d’envoyer une image 1500 à l’échelle des pixels.</span><span class="sxs-lookup"><span data-stu-id="07557-308">If your user is viewing your images on a mobile device screen that is 500-pixels-wide, there is really no point in sending a 1500-pixel-wide image.</span></span>  <span data-ttu-id="07557-309">Idéalement, vous envoyez une image de 500 pixels, le plus souvent.</span><span class="sxs-lookup"><span data-stu-id="07557-309">Ideally, you send a 500-pixel-wide image, at most.</span></span>  

1.  <span data-ttu-id="07557-310">Dans votre rapport, cliquez sur **éviter les charges utiles réseau énormes** pour voir les images qui doivent être redimensionnées.</span><span class="sxs-lookup"><span data-stu-id="07557-310">In your report, click **Avoid enormous network payloads** to see which images should be resized.</span></span>  <span data-ttu-id="07557-311">Il semble que 2 des fichiers jpg dépassent 2000 Ko, ce qui est plus grand que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="07557-311">It looks like 2 of the jpg files are over 2000 KB, which is bigger than necessary.</span></span>  
    
    <!--
    > ##### Old Figure 27  
    > Details about the **Properly size images** opportunity  
    > ![Details about the properly size images opportunity][ImageResize]  
    -->

1.  <span data-ttu-id="07557-312">Dans l’onglet Éditeur, ouvrez `src/model.js` .</span><span class="sxs-lookup"><span data-stu-id="07557-312">Back in the editor tab, open `src/model.js`.</span></span>  
1.  <span data-ttu-id="07557-313">Remplacer `const dir = 'big'` par `const dir = 'small'` .</span><span class="sxs-lookup"><span data-stu-id="07557-313">Replace `const dir = 'big'` with `const dir = 'small'`.</span></span>  <span data-ttu-id="07557-314">Ce répertoire contient des copies des mêmes images qui ont été redimensionnées.</span><span class="sxs-lookup"><span data-stu-id="07557-314">This directory contains copies of the same images which have been resized.</span></span>  
1.  <span data-ttu-id="07557-315">Auditez de nouveau la page pour voir l’incidence de cette modification sur les performances de chargement.</span><span class="sxs-lookup"><span data-stu-id="07557-315">Audit the page again to see how this change affects load performance.</span></span>  
    
    > ##### <span data-ttu-id="07557-316">Figure 25</span><span class="sxs-lookup"><span data-stu-id="07557-316">Figure 25</span></span>  
    > <span data-ttu-id="07557-317">Rapport d’audit après le redimensionnement d’images</span><span class="sxs-lookup"><span data-stu-id="07557-317">An Audits report after resizing images</span></span>  
    > <span data-ttu-id="07557-318">! [Un rapport d’audit après le redimensionnement des images] [ImageReport3]</span><span class="sxs-lookup"><span data-stu-id="07557-318">![An Audits report after resizing images][ImageReport3]</span></span>  

<span data-ttu-id="07557-319">Il semble que la modification n’ait qu’une incidence mineure sur le score de performance global.</span><span class="sxs-lookup"><span data-stu-id="07557-319">Looks like the change only has a minor affect on the overall performance score.</span></span>  <span data-ttu-id="07557-320">Néanmoins, il n’y a pas de distinction entre le résultat et la quantité de données réseau que vous enregistrez pour vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="07557-320">However, one thing that the score does not show clearly is how much network data you are saving your users.</span></span>  <span data-ttu-id="07557-321">La taille totale de l’ancienne photo a été d’environ 5,3 Mo, alors qu’il n’y a que 0,18 mégaoctets.</span><span class="sxs-lookup"><span data-stu-id="07557-321">The total size of the old photos was around 5.3 megabytes, whereas now it is only about 0.18 megabytes.</span></span>  

#### <span data-ttu-id="07557-322">Redimensionnement d’images dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="07557-322">Resizing images in the real world</span></span>   

<span data-ttu-id="07557-323">Dans le cas d’une petite application, il est possible de redimensionner une seule fois comme suit.</span><span class="sxs-lookup"><span data-stu-id="07557-323">For a small app, doing a one-off resize like this may be good enough.</span></span>  <span data-ttu-id="07557-324">Néanmoins, dans le cas d’une application de grande taille, cette solution n’est pas évolutive.</span><span class="sxs-lookup"><span data-stu-id="07557-324">But for a large app, this obviously is not scalable.</span></span>  <span data-ttu-id="07557-325">Voici quelques stratégies de gestion des images dans les applications volumineuses:</span><span class="sxs-lookup"><span data-stu-id="07557-325">Here are some strategies for managing images in large apps:</span></span>  

*   <span data-ttu-id="07557-326">Redimensionnez les images lors de votre processus de génération.</span><span class="sxs-lookup"><span data-stu-id="07557-326">Resize images during your build process.</span></span>  
*   <span data-ttu-id="07557-327">Créez plusieurs tailles de chaque image lors du processus de génération, puis utilisez-la `srcset` dans votre code.</span><span class="sxs-lookup"><span data-stu-id="07557-327">Create multiple sizes of each image during the build process and then use `srcset` in your code.</span></span>  <span data-ttu-id="07557-328">Lors de l’exécution, le navigateur s’occupe de choisir la taille la mieux appropriée pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="07557-328">At runtime, the browser takes care of choosing which size is best for the device.</span></span>  
    <!--See [Relative-sized images][relative].  -->

<!--[relative]: /web/fundamentals/design-and-ux/responsive/images#relative_sized_images  -->  

*   <span data-ttu-id="07557-329">Utilisez un CDN d’image qui vous permet de redimensionner dynamiquement une image lorsque vous la demandez.</span><span class="sxs-lookup"><span data-stu-id="07557-329">Use an image CDN that lets you dynamically resize an image when you request it.</span></span>  
*   <span data-ttu-id="07557-330">Optimisez chaque image au moins.</span><span class="sxs-lookup"><span data-stu-id="07557-330">At the very least, optimize each image.</span></span>  <span data-ttu-id="07557-331">Cela risque de créer des économies considérables.</span><span class="sxs-lookup"><span data-stu-id="07557-331">This may create huge savings.</span></span>  
  <span data-ttu-id="07557-332">L’optimisation consiste à exécuter une image par le biais d’un programme spécial qui réduit la taille du fichier image.</span><span class="sxs-lookup"><span data-stu-id="07557-332">Optimization is when you run an image through a special program that reduces the size of the image file.</span></span>  <span data-ttu-id="07557-333">Pour plus d’informations, voir [optimisation d’image essentielle][EssentialImageOptimization] .</span><span class="sxs-lookup"><span data-stu-id="07557-333">See [Essential Image Optimization][EssentialImageOptimization] for more tips.</span></span>  

### <span data-ttu-id="07557-334">Éliminer les ressources de blocage des rendez-vous</span><span class="sxs-lookup"><span data-stu-id="07557-334">Eliminate render-blocking resources</span></span>   

<span data-ttu-id="07557-335">Votre dernier État dit qu’il est impossible d’éliminer les ressources de blocage de rendu.</span><span class="sxs-lookup"><span data-stu-id="07557-335">Your latest report says that eliminating render-blocking resources is now the biggest opportunity.</span></span>  

<span data-ttu-id="07557-336">Une ressource de blocage de rendu est un fichier JavaScript ou CSS externe que le navigateur doit télécharger, analyser et exécuter avant d’afficher la page.</span><span class="sxs-lookup"><span data-stu-id="07557-336">A render-blocking resource is an external JavaScript or CSS file that the browser must download, parse, and run before it displays the page.</span></span>  <span data-ttu-id="07557-337">L’objectif est d’exécuter uniquement le code CSS principal et le code JavaScript requis pour afficher la page correctement.</span><span class="sxs-lookup"><span data-stu-id="07557-337">The goal is to only run the core CSS and JavaScript code that is required to display the page properly.</span></span>  

<span data-ttu-id="07557-338">La première tâche consiste à trouver le code que vous n’avez pas besoin de réexécuter sur le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-338">The first task, then, is to find code that you do not need to run on page load.</span></span>  

1.  <span data-ttu-id="07557-339">Sélectionnez **éliminer les ressources de blocage de rendu** pour afficher les ressources qui se bloquent:</span><span class="sxs-lookup"><span data-stu-id="07557-339">Select **Eliminate render-blocking resources** to see the resources that are blocking:</span></span>  
    `lodash.js` <span data-ttu-id="07557-340">et `jquery.js` .</span><span class="sxs-lookup"><span data-stu-id="07557-340">and `jquery.js`.</span></span>  
    
    > ##### <span data-ttu-id="07557-341">Figure 26</span><span class="sxs-lookup"><span data-stu-id="07557-341">Figure 26</span></span>  
    > <span data-ttu-id="07557-342">Plus d’informations sur l’opportunité de **suppression des ressources de blocage de rendu**</span><span class="sxs-lookup"><span data-stu-id="07557-342">More information about the **Eliminate render-blocking resources** opportunity</span></span>  
    > <span data-ttu-id="07557-343">! [Pour plus d’informations sur l’opportunité d’élimination des ressources de blocage du rendu] [ImageRender]</span><span class="sxs-lookup"><span data-stu-id="07557-343">![More information about the Eliminate render-blocking resources opportunity][ImageRender]</span></span>  
    
1.  <span data-ttu-id="07557-344">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes, commencez à taper `Coverage` , puis sélectionnez **afficher la couverture**.</span><span class="sxs-lookup"><span data-stu-id="07557-344">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, start typing `Coverage`, and then select **Show Coverage**.</span></span>  
    
    > ##### <span data-ttu-id="07557-345">Figure 27</span><span class="sxs-lookup"><span data-stu-id="07557-345">Figure 27</span></span>  
    > <span data-ttu-id="07557-346">Ouverture du menu de commandes dans le volet audits</span><span class="sxs-lookup"><span data-stu-id="07557-346">Opening the Command Menu from the Audits panel</span></span>  
    > <span data-ttu-id="07557-347">! [Ouverture du menu de commandes dans le volet audits] [ImageCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="07557-347">![Opening the Command Menu from the Audits panel][ImageCommandMenu]</span></span>  
    
    > ##### <span data-ttu-id="07557-348">Figure 28</span><span class="sxs-lookup"><span data-stu-id="07557-348">Figure 28</span></span>  
    > <span data-ttu-id="07557-349">Onglet couverture</span><span class="sxs-lookup"><span data-stu-id="07557-349">The Coverage tab</span></span>  
    > <span data-ttu-id="07557-350">! [Onglet couverture] [ImageCoverage]</span><span class="sxs-lookup"><span data-stu-id="07557-350">![The Coverage tab][ImageCoverage]</span></span>  
    
1.  <span data-ttu-id="07557-351">Sélectionnez **Actualiser** l' ![ actualisation ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="07557-351">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="07557-352">L’onglet **couverture** fournit une vue d’ensemble de la quantité de code `bundle.js` `jquery.js` et `lodash.js` s’exécute pendant le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-352">The **Coverage** tab provides an overview of how much of the code in `bundle.js`, `jquery.js`, and `lodash.js` runs while the page loads.</span></span>  <span data-ttu-id="07557-353">La [figure 30](#figure-30) indique qu’à propos de 76% et de 30% des fichiers jQuery et Lodash ne sont pas utilisés, respectivement.</span><span class="sxs-lookup"><span data-stu-id="07557-353">[Figure 30](#figure-30) says that about 76% and 30% of the jQuery and Lodash files are not used, respectively.</span></span>  
    
    > ##### <span data-ttu-id="07557-354">Figure 29</span><span class="sxs-lookup"><span data-stu-id="07557-354">Figure 29</span></span>  
    > <span data-ttu-id="07557-355">Rapport de couverture</span><span class="sxs-lookup"><span data-stu-id="07557-355">The Coverage report</span></span>  
    > <span data-ttu-id="07557-356">! [Rapport de couverture] [ImageCoverageReport]</span><span class="sxs-lookup"><span data-stu-id="07557-356">![The Coverage report][ImageCoverageReport]</span></span>  
    
1.  <span data-ttu-id="07557-357">Sélectionnez la ligne **jQuery. js** .</span><span class="sxs-lookup"><span data-stu-id="07557-357">Select the **jquery.js** row.</span></span>  <span data-ttu-id="07557-358">DevTools ouvre le fichier dans le volet sources.</span><span class="sxs-lookup"><span data-stu-id="07557-358">DevTools opens the file in the Sources panel.</span></span>  <span data-ttu-id="07557-359">Une ligne de code a été exécutée si une barre bleue est située en regard.</span><span class="sxs-lookup"><span data-stu-id="07557-359">A line of code ran if it has a blue bar next to it.</span></span>  <span data-ttu-id="07557-360">Une barre rouge signifie qu’elle n’a pas été exécutée et qu’elle n’est pas nécessaire sur le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-360">A red bar means it was not run, and is definitely not needed on page load.</span></span>  
    
    > ##### <span data-ttu-id="07557-361">Figure 30</span><span class="sxs-lookup"><span data-stu-id="07557-361">Figure 30</span></span>  
    > <span data-ttu-id="07557-362">Affichage du fichier jQuery dans le panneau sources</span><span class="sxs-lookup"><span data-stu-id="07557-362">Viewing the jQuery file in the Sources panel</span></span>  
    > <span data-ttu-id="07557-363">! [Affichage du fichier jQuery dans le panneau sources] [ImageJQuery]</span><span class="sxs-lookup"><span data-stu-id="07557-363">![Viewing the jQuery file in the Sources panel][ImageJQuery]</span></span>  
    
1.  <span data-ttu-id="07557-364">Parcourez un bit du code jQuery.</span><span class="sxs-lookup"><span data-stu-id="07557-364">Scroll through the jQuery code a bit.</span></span>  <span data-ttu-id="07557-365">Voici quelques-unes des lignes qui s’exécutent uniquement en commentaires.</span><span class="sxs-lookup"><span data-stu-id="07557-365">Some of the lines that get "run" are actually just comments.</span></span>  <span data-ttu-id="07557-366">L’exécution de ce code par le biais d’un Minifier qui tire des commentaires est une autre façon de réduire la taille de ce fichier.</span><span class="sxs-lookup"><span data-stu-id="07557-366">Running this code through a minifier that strips comments is another way to reduce the size of this file.</span></span>  

<span data-ttu-id="07557-367">En résumé, lorsque vous utilisez votre propre code, l’onglet couverture vous permet d’analyser votre code, ligne par ligne, et d’expédier uniquement le code nécessaire au chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-367">In short, when you are working with your own code, the Coverage tab helps you analyze your code, line-by-line, and only ship the code that is needed for page load.</span></span>  

<span data-ttu-id="07557-368">Les fichiers et sont-ils `jquery.js` `lodash.js` même nécessaires pour le chargement de la page?</span><span class="sxs-lookup"><span data-stu-id="07557-368">Are the `jquery.js` and `lodash.js` files even needed to load the page?</span></span>  <span data-ttu-id="07557-369">L’onglet de blocage de requête indique ce qui se produit lorsque les ressources ne sont pas disponibles.</span><span class="sxs-lookup"><span data-stu-id="07557-369">The Request Blocking tab displays what happens when resources are not available.</span></span>  

1.  <span data-ttu-id="07557-370">Sélectionnez l’onglet **Network (réseau** ).</span><span class="sxs-lookup"><span data-stu-id="07557-370">Select the **Network** tab.</span></span>  
1.  <span data-ttu-id="07557-371">Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir de nouveau le menu de commandes.</span><span class="sxs-lookup"><span data-stu-id="07557-371">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu again.</span></span>  
1.  <span data-ttu-id="07557-372">Commencez à taper `blocking` , puis sélectionnez **afficher le blocage de requête**.</span><span class="sxs-lookup"><span data-stu-id="07557-372">Start typing `blocking` and then select **Show Request Blocking**.</span></span>  
    
    > ##### <span data-ttu-id="07557-373">Figure 31</span><span class="sxs-lookup"><span data-stu-id="07557-373">Figure 31</span></span>  
    > <span data-ttu-id="07557-374">Onglet requête de blocage</span><span class="sxs-lookup"><span data-stu-id="07557-374">The Request Blocking tab</span></span>  
    > <span data-ttu-id="07557-375">! [L’onglet de blocage de requête] [ImageBlocking]</span><span class="sxs-lookup"><span data-stu-id="07557-375">![The Request Blocking tab][ImageBlocking]</span></span>  
    
1.  <span data-ttu-id="07557-376">Sélectionnez **Ajouter** un modèle ajouter un modèle ![ ][ImageAddPatternIcon] , tapez `/libs/*` , puis appuyez sur `Enter` pour confirmer.</span><span class="sxs-lookup"><span data-stu-id="07557-376">Select **Add Pattern** ![Add Pattern][ImageAddPatternIcon], type `/libs/*`, and then press `Enter` to confirm.</span></span>  
    
    > ##### <span data-ttu-id="07557-377">Figure 32</span><span class="sxs-lookup"><span data-stu-id="07557-377">Figure 32</span></span>  
    > <span data-ttu-id="07557-378">Ajout d’un modèle pour bloquer toute demande de l' `libs` Annuaire</span><span class="sxs-lookup"><span data-stu-id="07557-378">Adding a pattern to block any request to the `libs` directory</span></span>  
    > <span data-ttu-id="07557-379">! [Ajout d’un modèle pour bloquer une requête dans l’annuaire libs] [ImageLibs]</span><span class="sxs-lookup"><span data-stu-id="07557-379">![Adding a pattern to block any request to the libs directory][ImageLibs]</span></span>  
    
1.  <span data-ttu-id="07557-380">Actualisez la page.</span><span class="sxs-lookup"><span data-stu-id="07557-380">Refresh the page.</span></span>  <span data-ttu-id="07557-381">Les requêtes jQuery et Lodash sont rouges, ce qui signifie que les requêtes ont été bloquées.</span><span class="sxs-lookup"><span data-stu-id="07557-381">The jQuery and Lodash requests are red, meaning that the requests were blocked.</span></span>   <span data-ttu-id="07557-382">Étant donné que la page est toujours chargée et qu’elle est interactive, il semblerait que les ressources suivantes ne soient pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="07557-382">The page still loads and is interactive, so it looks like these resources are not needed whatsoever!</span></span>  
    
    > ##### <span data-ttu-id="07557-383">Figure 33</span><span class="sxs-lookup"><span data-stu-id="07557-383">Figure 33</span></span>  
    > <span data-ttu-id="07557-384">Le volet réseau indique que les requêtes ont été bloquées.</span><span class="sxs-lookup"><span data-stu-id="07557-384">The Network panel shows that the requests have been blocked</span></span>  
    > <span data-ttu-id="07557-385">! [Le panneau réseau indique que les demandes ont été bloquées] [ImageBlockedLibs]</span><span class="sxs-lookup"><span data-stu-id="07557-385">![The Network panel shows that the requests have been blocked][ImageBlockedLibs]</span></span>  
    
1.  <span data-ttu-id="07557-386">Sélectionner **Supprimer tous les modèles** ![ supprimez tous les modèles ][ImageRemoveIcon] pour supprimer le `/libs/*` modèle de blocage.</span><span class="sxs-lookup"><span data-stu-id="07557-386">Select **Remove all patterns** ![Remove all patterns][ImageRemoveIcon] to delete the `/libs/*` blocking pattern.</span></span>  

<span data-ttu-id="07557-387">En règle générale, l’onglet blocage de requête est utile pour simuler le comportement de votre page quand une ressource donnée n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="07557-387">In general, the Request Blocking tab is useful for simulating how your page behaves when any given resource is not available.</span></span>  

<span data-ttu-id="07557-388">À présent, supprimez les références à ces fichiers du code et auditez de nouveau la page:</span><span class="sxs-lookup"><span data-stu-id="07557-388">Now, remove the references to these files from the code and audit the page again:</span></span>  

1.  <span data-ttu-id="07557-389">Dans l’onglet Éditeur, ouvrez `template.html` .</span><span class="sxs-lookup"><span data-stu-id="07557-389">Back in the editor tab, open `template.html`.</span></span>  
1.  <span data-ttu-id="07557-390">Supprimez les éléments `<script src="/libs/lodash.js">` et `<script src="/libs/jquery.js"></script>`.</span><span class="sxs-lookup"><span data-stu-id="07557-390">Delete `<script src="/libs/lodash.js">` and `<script src="/libs/jquery.js"></script>`.</span></span>  
1.  <span data-ttu-id="07557-391">Attendez que le site soit recréé et redéploiement.</span><span class="sxs-lookup"><span data-stu-id="07557-391">Wait for the site to re-build and re-deploy.</span></span>  
1.  <span data-ttu-id="07557-392">Auditez de nouveau la page à partir du volet **vérifications** .</span><span class="sxs-lookup"><span data-stu-id="07557-392">Audit the page again from the **Audits** panel.</span></span>  <span data-ttu-id="07557-393">Votre score global devrait de nouveau s’améliorer.</span><span class="sxs-lookup"><span data-stu-id="07557-393">Your overall score should have improved again.</span></span>  
    
    > ##### <span data-ttu-id="07557-394">Figure 34</span><span class="sxs-lookup"><span data-stu-id="07557-394">Figure 34</span></span>  
    > <span data-ttu-id="07557-395">Rapport d’audit après la suppression des ressources de blocage de rendu</span><span class="sxs-lookup"><span data-stu-id="07557-395">An Audits report after removing the render-blocking resources</span></span>  
    > <span data-ttu-id="07557-396">! [Un rapport d’audit après la suppression des ressources de blocage de rendu] [ImageReport4]</span><span class="sxs-lookup"><span data-stu-id="07557-396">![An Audits report after removing the render-blocking resources][ImageReport4]</span></span>  

#### <span data-ttu-id="07557-397">Optimisation du chemin de rendu critique dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="07557-397">Optimizing the Critical Rendering Path in the real-world</span></span>   

<span data-ttu-id="07557-398">Le **chemin de rendu critique** fait référence au code dont vous avez besoin pour charger une page.</span><span class="sxs-lookup"><span data-stu-id="07557-398">The **Critical Rendering Path** refers to the code that you need to load a page.</span></span>  <span data-ttu-id="07557-399">En règle générale, accélérez le chargement de la page en ne disportant que le code Critical pendant le chargement de la page, puis en chargeant en différé tout le reste.</span><span class="sxs-lookup"><span data-stu-id="07557-399">In general, speed up page load by only shipping critical code during the page load, and then lazy-loading everything else.</span></span>  

<!--[CRP]: /web/fundamentals/performance/critical-rendering-path/  -->  

*   <span data-ttu-id="07557-400">Il est peu probable que vous puissiez retrouver les scripts que vous pouvez supprimer d’un certain temps, mais il se peut que vous trouviez de nombreux scripts que vous n’avez pas besoin de demander pendant le chargement de la page, et qu’ils puissent être demandés de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="07557-400">It is unlikely that you are able to find scripts that you are able to remove outright, but you may find many scripts that you do not need to request during the page load, and instead may be requested asynchronously.</span></span>  <!--See [Using async or defer][async].  -->  
*   <span data-ttu-id="07557-401">Si vous utilisez un Framework, vérifiez qu’il dispose du mode de production.</span><span class="sxs-lookup"><span data-stu-id="07557-401">If you are using a framework, check if it has a production mode.</span></span>  <span data-ttu-id="07557-402">Ce mode peut utiliser une fonctionnalité telle que l’agitation de l' [arborescence][WebpackTreeShaking] afin d’éliminer le code inutile qui bloque le rendu critique.</span><span class="sxs-lookup"><span data-stu-id="07557-402">This mode may use a feature such as [tree shaking][WebpackTreeShaking] in order to eliminate unnecessary code that is blocking the critical render.</span></span>  

<!--[async]: /web/fundamentals/performance/optimizing-content-efficiency/loading-third-party-javascript/#use_async_or_defer  -->  

### <span data-ttu-id="07557-403">Réduire le fonctionnement du thread principal</span><span class="sxs-lookup"><span data-stu-id="07557-403">Do less main thread work</span></span>   

<span data-ttu-id="07557-404">Votre dernier État montre quelques réductions potentielles mineurs dans la section opportunités, mais si vous examinez la section Diagnostics, il semble que le plus grand goulet d’étranglement soit trop important pour le thread principal.</span><span class="sxs-lookup"><span data-stu-id="07557-404">Your latest report shows some minor potential savings in the Opportunities section, but if you look down in the Diagnostics section, it looks like the biggest bottleneck is too much main thread activity.</span></span>  

<span data-ttu-id="07557-405">Le thread principal est l’endroit où le navigateur exécute la majeure partie du processus d’affichage d’une page, telle que l’analyse et l’exécution de HTML, CSS et JavaScript.</span><span class="sxs-lookup"><span data-stu-id="07557-405">The main thread is where the browser does most of the work needed to display a page, such as parsing and running HTML, CSS, and JavaScript.</span></span>  

<span data-ttu-id="07557-406">L’objectif consiste à utiliser le panneau performance pour analyser le travail effectué par le thread principal pendant le chargement de la page, et Rechercher des moyens de différer ou de supprimer le travail inutile.</span><span class="sxs-lookup"><span data-stu-id="07557-406">The goal is to use the Performance panel to analyze what work the main thread is doing while the page loads, and find ways to defer or remove unnecessary work.</span></span>  

1.  <span data-ttu-id="07557-407">Sélectionnez l’onglet **performance** .</span><span class="sxs-lookup"><span data-stu-id="07557-407">Select the **Performance** tab.</span></span>  
1.  <span data-ttu-id="07557-408">Sélectionnez Paramètres de capture des **paramètres de capture** ![ ][ImageCaptureIcon] .</span><span class="sxs-lookup"><span data-stu-id="07557-408">Select **Capture Settings** ![Capture Settings][ImageCaptureIcon].</span></span>  
1.  <span data-ttu-id="07557-409">Définissez **réseau** sur **lente réseau 3G** et **UC** à **6**ralentis.</span><span class="sxs-lookup"><span data-stu-id="07557-409">Set **Network** to **Slow 3G** and **CPU** to **6x slowdown**.</span></span>  <span data-ttu-id="07557-410">Les appareils mobiles présentent généralement plus de contraintes matérielles que les ordinateurs portables ou de bureau, de sorte que ces paramètres vous permettent de vous familiariser avec le chargement de la page comme si vous utilisiez un appareil moins puissant.</span><span class="sxs-lookup"><span data-stu-id="07557-410">Mobile devices typically have more hardware constraints than laptops or desktops, so these settings let you experience the page load as if you were using a less powerful device.</span></span>  
1.  <span data-ttu-id="07557-411">Sélectionnez **Actualiser** l' ![ actualisation ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="07557-411">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  <span data-ttu-id="07557-412">DevTools actualise la page, puis produit une visualisation de tout le temps exécuté pour le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-412">DevTools refreshes the page and then produces a visualization of all the work performed in order to load the page.</span></span>  <span data-ttu-id="07557-413">Cette visualisation est appelée **suivi**.</span><span class="sxs-lookup"><span data-stu-id="07557-413">This visualization is referred to as the **trace**.</span></span>  
    
    > ##### <span data-ttu-id="07557-414">Figure 35</span><span class="sxs-lookup"><span data-stu-id="07557-414">Figure 35</span></span>  
    > <span data-ttu-id="07557-415">Suivi du panneau de performance du chargement de la page</span><span class="sxs-lookup"><span data-stu-id="07557-415">The Performance panel trace of the page load</span></span>  
    > <span data-ttu-id="07557-416">! [Trace du panneau de performance du chargement de la page] [ImagePerformance]</span><span class="sxs-lookup"><span data-stu-id="07557-416">![The Performance panel trace of the page load][ImagePerformance]</span></span>  

<span data-ttu-id="07557-417">Le suivi des activités est affiché dans un ordre chronologique, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="07557-417">The trace shows activity chronologically, from left to right.</span></span>  <span data-ttu-id="07557-418">Les graphiques FPS, UC et NET en haut offrent une vue d’ensemble des images par seconde, de l’activité de l’UC et de l’activité du réseau.</span><span class="sxs-lookup"><span data-stu-id="07557-418">The FPS, CPU, and NET charts at the top give you an overview of frames per second, CPU activity, and network activity.</span></span>  <span data-ttu-id="07557-419">Le bloc de jaune sélectionné que vous voyez dans la [Figure 37](#figure-37) signifie que le processeur était entièrement occupé avec l’activité de script.</span><span class="sxs-lookup"><span data-stu-id="07557-419">The block of yellow selected that you see in [Figure 37](#figure-37) means that the CPU was completely busy with scripting activity.</span></span>  <span data-ttu-id="07557-420">C’est une idée qu’il est possible que vous puissiez accélérer le chargement de la page en effectuant moins de tâches JavaScript.</span><span class="sxs-lookup"><span data-stu-id="07557-420">This is a clue that you may be able to speed up page load by doing less JavaScript work.</span></span>  

> ##### <span data-ttu-id="07557-421">Figure 36</span><span class="sxs-lookup"><span data-stu-id="07557-421">Figure 36</span></span>  
> <span data-ttu-id="07557-422">Section vue d’ensemble du suivi</span><span class="sxs-lookup"><span data-stu-id="07557-422">The Overview section of the trace</span></span>  
> <span data-ttu-id="07557-423">! [Section vue d’ensemble du suivi] [ImageOverview]</span><span class="sxs-lookup"><span data-stu-id="07557-423">![The Overview section of the trace][ImageOverview]</span></span>  

<span data-ttu-id="07557-424">Examinez la trace pour trouver des moyens d’effectuer moins de tâches JavaScript:</span><span class="sxs-lookup"><span data-stu-id="07557-424">Investigate the trace to find ways to do less JavaScript work:</span></span>  

1.  <span data-ttu-id="07557-425">Sélectionnez la section **minutage** pour la développer.</span><span class="sxs-lookup"><span data-stu-id="07557-425">Select the **Timings** section to expand it.</span></span>  <span data-ttu-id="07557-426">En fonction du fait qu’il est possible qu’il y ait quelques mesures de [temporisation][MDNUserTimingApi] , il semble que l’application Thomas utilise le mode développement de réaction.</span><span class="sxs-lookup"><span data-stu-id="07557-426">Based on the fact that there may be a bunch of [Timings][MDNUserTimingApi] measures from React, it seems like Tony's app is using the development mode of React.</span></span>  <span data-ttu-id="07557-427">Basculer vers le mode de production de réagisser risque de générer un service de performance plus simple.</span><span class="sxs-lookup"><span data-stu-id="07557-427">Switching to the production mode of React may yield some easy performance wins.</span></span>  
    
    > ##### <span data-ttu-id="07557-428">Figure 37</span><span class="sxs-lookup"><span data-stu-id="07557-428">Figure 37</span></span>  
    > <span data-ttu-id="07557-429">Section minutage</span><span class="sxs-lookup"><span data-stu-id="07557-429">The Timings section</span></span>  
    > <span data-ttu-id="07557-430">! [Section minutages] [ImageUserTiming]</span><span class="sxs-lookup"><span data-stu-id="07557-430">![The Timings section][ImageUserTiming]</span></span>  

1.  <span data-ttu-id="07557-431">Sélectionnez de nouveau **minutages** pour réduire cette section.</span><span class="sxs-lookup"><span data-stu-id="07557-431">Select **Timings** again to collapse that section.</span></span>  
1.  <span data-ttu-id="07557-432">Naviguez dans la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="07557-432">Browse the **Main** section.</span></span>  <span data-ttu-id="07557-433">Cette section présente un journal chronologique de l’activité principale du thread, de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="07557-433">This section shows a chronological log of main thread activity, from left to right.</span></span>  <span data-ttu-id="07557-434">L’axe y (de haut en bas) montre pourquoi des événements s’est produit.</span><span class="sxs-lookup"><span data-stu-id="07557-434">The y-axis (top to bottom) shows why events occurred.</span></span>  <span data-ttu-id="07557-435">Par exemple, dans [Figure 39](#figure-39), l' `Evaluate Script` événement a entraîné l’exécution de la fonction, qui a entraîné l’exécution de la `(anonymous)` fonction, `(anonymous)` `__webpack__require__` et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="07557-435">For example, in [Figure 39](#figure-39), the `Evaluate Script` event caused the `(anonymous)` function to run, which caused `(anonymous)` to run, which caused `__webpack__require__` to run, and so on.</span></span>  
    
    > ##### <span data-ttu-id="07557-436">Figure 38</span><span class="sxs-lookup"><span data-stu-id="07557-436">Figure 38</span></span>  
    > <span data-ttu-id="07557-437">Section principale</span><span class="sxs-lookup"><span data-stu-id="07557-437">The Main section</span></span>  
    > <span data-ttu-id="07557-438">! [Section principale] [ImageMain]</span><span class="sxs-lookup"><span data-stu-id="07557-438">![The Main section][ImageMain]</span></span>  

1.  <span data-ttu-id="07557-439">Faites défiler vers le bas jusqu’en bas de la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="07557-439">Scroll down to the bottom of the **Main** section.</span></span>  <span data-ttu-id="07557-440">Lorsque vous utilisez une infrastructure, la majeure partie de l’activité la plus grande est provoquée par l’infrastructure, qui est généralement hors de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="07557-440">When you use a framework, most of the upper activity is caused by the framework, which is usually out of your control.</span></span>  <span data-ttu-id="07557-441">L’activité générée par votre application est généralement située en bas.</span><span class="sxs-lookup"><span data-stu-id="07557-441">The activity caused by your app is usually at the bottom.</span></span>  <span data-ttu-id="07557-442">Dans cette application, il semble qu’une fonction nommée `App` génère un grand nombre de requêtes sur une `mineBitcoin` fonction.</span><span class="sxs-lookup"><span data-stu-id="07557-442">In this app, it seems like a function named `App` is causing a lot of requests to a `mineBitcoin` function.</span></span>  <span data-ttu-id="07557-443">Il semble que Thomas utilise les appareils de ses fans pour cryptocurrency...</span><span class="sxs-lookup"><span data-stu-id="07557-443">It sounds like Tony might be using the devices of his fans to mine cryptocurrency...</span></span>  
    
    > ##### <span data-ttu-id="07557-444">Figure 39</span><span class="sxs-lookup"><span data-stu-id="07557-444">Figure 39</span></span>  
    > <span data-ttu-id="07557-445">Survol de l' `mineBitcoin` activité</span><span class="sxs-lookup"><span data-stu-id="07557-445">Hovering over the `mineBitcoin` activity</span></span>  
    > <span data-ttu-id="07557-446">! [Survol de l’activité mineBitcoin] [ImageMine]</span><span class="sxs-lookup"><span data-stu-id="07557-446">![Hovering over the mineBitcoin activity][ImageMine]</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="07557-447">Bien que les requêtes que votre infrastructure effectue généralement hors de votre contrôle, il est possible que vous puissiez structurer votre application de manière à ce que l’infrastructure s’exécute de manière inefficace.</span><span class="sxs-lookup"><span data-stu-id="07557-447">Although the requests that your framework makes are usually out of your control, sometimes you may structure your app in a way that causes the framework to run inefficiently.</span></span>  <span data-ttu-id="07557-448">La restructuration de votre application pour qu’elle utilise efficacement l’infrastructure est un moyen de réduire le coût de fonctionnement du thread principal.</span><span class="sxs-lookup"><span data-stu-id="07557-448">Restructuring your app to use the framework efficiently is a way to do less main thread work.</span></span>  <span data-ttu-id="07557-449">Toutefois, cela nécessite une compréhension approfondie du fonctionnement de l’infrastructure et le type de modification que vous effectuez dans votre propre code afin d’utiliser l’infrastructure plus efficacement.</span><span class="sxs-lookup"><span data-stu-id="07557-449">However, this requires a deep understanding of how your framework works, and what kind of changes you make in your own code in order to use the framework more efficiently.</span></span>  

1.  <span data-ttu-id="07557-450">Développez la section **de haut en bas** .</span><span class="sxs-lookup"><span data-stu-id="07557-450">Expand the **Bottom-Up** section.</span></span>  <span data-ttu-id="07557-451">Dans cet onglet, les activités ont duré le plus longtemps.</span><span class="sxs-lookup"><span data-stu-id="07557-451">This tab breaks down what activities took up the most time.</span></span>  <span data-ttu-id="07557-452">S’il n’y a aucun élément dans la section de haut en bas, cliquez sur l’étiquette de la section **principale** .</span><span class="sxs-lookup"><span data-stu-id="07557-452">If you do not see anything in the Bottom-Up section, click the label for **Main** section.</span></span>  <span data-ttu-id="07557-453">La section **ascendante** affiche uniquement les informations relatives à l’activité, ou au groupe d’activité, que vous avez sélectionné.</span><span class="sxs-lookup"><span data-stu-id="07557-453">The **Bottom-Up** section only shows information for whatever activity, or group of activity, you have currently selected.</span></span>  <span data-ttu-id="07557-454">Par exemple, si vous avez cliqué sur une des `mineBitcoin` activités, la section de **bas en haut** consiste à afficher les informations relatives à cette activité unique.</span><span class="sxs-lookup"><span data-stu-id="07557-454">For example, if you clicked on one of the `mineBitcoin` activities, the **Bottom-Up** section is only going to show information for that one activity.</span></span>  
    
    > ##### <span data-ttu-id="07557-455">Figure 40</span><span class="sxs-lookup"><span data-stu-id="07557-455">Figure 40</span></span>  
    > <span data-ttu-id="07557-456">Onglet inférieur</span><span class="sxs-lookup"><span data-stu-id="07557-456">The Bottom-Up tab</span></span>  
    > <span data-ttu-id="07557-457">! [Onglet inférieur] [ImageBottomUp]</span><span class="sxs-lookup"><span data-stu-id="07557-457">![The Bottom-Up tab][ImageBottomUp]</span></span>  

<span data-ttu-id="07557-458">La colonne **temps libre** vous indique le temps passé directement dans chaque activité.</span><span class="sxs-lookup"><span data-stu-id="07557-458">The **Self Time** column shows you how much time was spent directly in each activity.</span></span>  <span data-ttu-id="07557-459">Par exemple, la [Figure 41](#figure-41) montre qu’environ 63% du temps de thread principal a été dépensé sur la `mineBitcoin` fonction.</span><span class="sxs-lookup"><span data-stu-id="07557-459">For example, [Figure 41](#figure-41) shows that about 63% of main thread time was spent on the `mineBitcoin` function.</span></span>  

<span data-ttu-id="07557-460">Il est temps de voir si l’utilisation du mode de production et la réduction des activités JavaScript accélèrent le chargement de la page.</span><span class="sxs-lookup"><span data-stu-id="07557-460">Time to see whether using production mode and reducing JavaScript activity may speed up the page load.</span></span>  <span data-ttu-id="07557-461">Commencer avec le mode production:</span><span class="sxs-lookup"><span data-stu-id="07557-461">Start with production mode:</span></span>  

1.  <span data-ttu-id="07557-462">Dans l’onglet Éditeur, ouvrez `webpack.config.js` .</span><span class="sxs-lookup"><span data-stu-id="07557-462">In the editor tab, open `webpack.config.js`.</span></span>  
1.  <span data-ttu-id="07557-463">Remplacez `"mode":"development"` par `"mode":"production"` .</span><span class="sxs-lookup"><span data-stu-id="07557-463">Change `"mode":"development"` to `"mode":"production"`.</span></span>  
1.  <span data-ttu-id="07557-464">Attendez la fin du déploiement de la nouvelle Build.</span><span class="sxs-lookup"><span data-stu-id="07557-464">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="07557-465">Auditez de nouveau la page.</span><span class="sxs-lookup"><span data-stu-id="07557-465">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="07557-466">Figure 41</span><span class="sxs-lookup"><span data-stu-id="07557-466">Figure 41</span></span>  
    > <span data-ttu-id="07557-467">Rapport d’audit après la configuration de WebPack pour utiliser le mode de production</span><span class="sxs-lookup"><span data-stu-id="07557-467">An Audits report after configuring webpack to use production mode</span></span>  
    > <span data-ttu-id="07557-468">! [Rapport de vérification après la configuration de WebPack pour utiliser le mode de production] [ImageReport5]</span><span class="sxs-lookup"><span data-stu-id="07557-468">![An Audits report after configuring webpack to use production mode][ImageReport5]</span></span>  

<span data-ttu-id="07557-469">Réduisez les activités JavaScript en supprimant la demande `mineBitcoin` :</span><span class="sxs-lookup"><span data-stu-id="07557-469">Reduce JavaScript activity by removing the request to `mineBitcoin`:</span></span>  

1.  <span data-ttu-id="07557-470">Dans l’onglet Éditeur, ouvrez `src/App.jsx` .</span><span class="sxs-lookup"><span data-stu-id="07557-470">In the editor tab, open `src/App.jsx`.</span></span>  
1.  <span data-ttu-id="07557-471">Transmettez la demande au `this.mineBitcoin(1500)` `constructor` .</span><span class="sxs-lookup"><span data-stu-id="07557-471">Comment out the request to `this.mineBitcoin(1500)` in the `constructor`.</span></span>  
1.  <span data-ttu-id="07557-472">Attendez la fin du déploiement de la nouvelle Build.</span><span class="sxs-lookup"><span data-stu-id="07557-472">Wait for the new build to deploy.</span></span>  
1.  <span data-ttu-id="07557-473">Auditez de nouveau la page.</span><span class="sxs-lookup"><span data-stu-id="07557-473">Audit the page again.</span></span>  
    
    > ##### <span data-ttu-id="07557-474">Figure 42</span><span class="sxs-lookup"><span data-stu-id="07557-474">Figure 42</span></span>  
    > <span data-ttu-id="07557-475">Rapport de vérification après suppression du fonctionnement inutile de JavaScript</span><span class="sxs-lookup"><span data-stu-id="07557-475">An Audits report after removing unnecessary JavaScript work</span></span>  
    > <span data-ttu-id="07557-476">! [Rapport de vérification après suppression du fonctionnement JavaScript inutile] [ImageReport6]</span><span class="sxs-lookup"><span data-stu-id="07557-476">![An Audits report after removing unnecessary JavaScript work][ImageReport6]</span></span>  

<span data-ttu-id="07557-477">Il semble que le dernier changement ait entraîné un décalage massif de performances.</span><span class="sxs-lookup"><span data-stu-id="07557-477">Looks like that last change caused a massive jump in performance!</span></span>  

> [!NOTE]
> <span data-ttu-id="07557-478">Cette section proposait plutôt une présentation du panneau performance.</span><span class="sxs-lookup"><span data-stu-id="07557-478">This section provided a rather brief introduction to the Performance panel.</span></span>  <span data-ttu-id="07557-479">Pour en savoir plus sur l’analyse des performances des pages, voir référence sur l' [analyse des performances][DevtoolsEvaluatePerformanceReference] .</span><span class="sxs-lookup"><span data-stu-id="07557-479">See [Performance Analysis Reference][DevtoolsEvaluatePerformanceReference] to learn more about how to analyze page performance.</span></span>  

<!--todo: add section when available -->  

#### <span data-ttu-id="07557-480">Exécution moins importante du thread principal dans le monde réel</span><span class="sxs-lookup"><span data-stu-id="07557-480">Doing less main thread work in the real world</span></span>   

<span data-ttu-id="07557-481">En règle générale, le panneau **performance** est le moyen le plus courant de comprendre l’activité que votre site effectue au chargement et les manières de supprimer les activités inutiles.</span><span class="sxs-lookup"><span data-stu-id="07557-481">In general, the **Performance** panel is the most common way to understand what activity your site does as it loads, and find ways to remove unnecessary activity.</span></span>  

<span data-ttu-id="07557-482">Si vous préférez une approche qui ressemble davantage à celle- `console.log()` ci, l' [API de minutage des utilisateurs][MDNUserTimingApi] vous permet de marquer de façon arbitraire certaines phases du cycle de vie de votre application afin d’effectuer le suivi de la durée de chacune de ces phases.</span><span class="sxs-lookup"><span data-stu-id="07557-482">If you prefer an approach that feels more like `console.log()`, the [User Timing API][MDNUserTimingApi] enables you to arbitrarily mark up certain phases of your app lifecycle, in order to track how long each of those phases takes.</span></span>  

## <span data-ttu-id="07557-483">Résumé</span><span class="sxs-lookup"><span data-stu-id="07557-483">Summary</span></span>   

*   <span data-ttu-id="07557-484">Dès que vous avez fini d’optimiser les performances de chargement d’un site, commencez toujours par un audit.</span><span class="sxs-lookup"><span data-stu-id="07557-484">Whenever you set out to optimize the load performance of a site, always start with an audit.</span></span>  <span data-ttu-id="07557-485">L’audit établit un planning de référence et vous donne des conseils sur la manière d’améliorer.</span><span class="sxs-lookup"><span data-stu-id="07557-485">The audit establishes a baseline, and gives you tips on how to improve.</span></span>  
*   <span data-ttu-id="07557-486">Apportez une modification à la fois, puis auditez la page après chaque modification afin de savoir comment ce changement d’isolement a un impact sur les performances.</span><span class="sxs-lookup"><span data-stu-id="07557-486">Make one change at a time, and audit the page after each change in order to see how that isolated change affects performance.</span></span>  

<!--
## Next steps   

*   Run audits on your own site!  If you need help interpreting your report, or finding ways to improve your load performance, check out [Feedback](#feedback) for ways to get help from the DevTools community.  Stack Overflow, the mailing list, or Twitter are probably best for these types of questions.  
*   Please leave [feedback](#feedback) on this tutorial.  I really do use the data to make better tutorials for you.  
-->  

<!--    -->  



<!-- image links -->  

[ImageAddPatternIcon]: /microsoft-edge/devtools-guide-chromium/media/add-pattern-icon.msft.png  
[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-icon.msft.png  
[ImageLargeResourceRowsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/large-resource-rows-button-icon.msft.png  
[ImageMorePanelsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-panels-icon.msft.png  
[ImagePerformIcon]: /microsoft-edge/devtools-guide-chromium/media/perform-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRemoveIcon]: /microsoft-edge/devtools-guide-chromium/media/remove-icon.msft.png  

[ImageTony]: /microsoft-edge/devtools-guide-chromium/media/speed-tony.msft.png "Figure 1: Thomas the chat"  
[ImageEditor]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js.msft.png "Figure 2: onglet Éditeur"  
[ImageMenu]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-server-js-remix-project.msft.png "Figure 3: menu qui s’affiche après avoir cliqué sur Thierry"  
[ImageDemo]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live.msft.png "Figure 4: onglet démonstration"  
[ImageDevtools]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-show-live-console.msft.png "Figure 5: DevTools et la démo"  
[ImageUndocked]: /microsoft-edge/devtools-guide-chromium/media/speed-console.msft.png "Figure 6: DevTools non attaché"  
[ImageAudits]: /microsoft-edge/devtools-guide-chromium/media/speed-audits-performance.msft.png "Figure 7: volet d’audit"  
[ImageReport]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-audits-performance-metrics-collapsed.msft.png "Figure 8: rapport du volet d’audit des performances du site"  
<!--[ImageError]: /microsoft-edge/devtools-guide-chromium/media/speed-.msft.png "Old Figure 9: A report that errored"  -->  
[ImageOverall]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-Performance-Metrics-Collapsed-Metrics-Highlighted.msft.png "figure 9: score global de performance"  
[ImageMetrics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-Performance-Metrics-Collapsed-Highlighted.msft.png "figure 10: la section indicateurs"  
[ImageFirstMeaningfulPaint]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-Performance-Metrics-Expanded.msft.png "figure 11: sélectionner le bouton bascule surligné pour développer les éléments métriques"  
[ImageScreenshots]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-performance-View-trace.msft.png "figure 12: captures d’écran illustrant l’apparence de la page en cours de chargement"  
[ImageOpportunities]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-performance-opportunities.msft.png "figure 13: la section opportunités"  
[ImageCompression]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-performance-opportunities-Expanded.msft.png "figure 14: élimination des ressources de blocage de rendu"  
[ImageReference]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-Web-dev-performance-audits.msft.png "figure 15: documentation pour l’opportunité d’élimination des ressources de blocage du rendu"  
[ImageDiagnostics]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-Performance-Diagnostics.msft.png "figure 16: section Diagnostics"  
[ImagePassed]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-audits-performance-passed-audits.msft.png "figure 17: section réussite d’audit"  
[ImageNetwork]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network.msft.png "figure 18: panneau réseau"  
[ImageLargeRows]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-use-large-Request-Rows.msft.png "figure 19: lignes de grande taille dans la table requêtes réseau"  
[ImageHeaders]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-use-large-Request-Rows-Bundle-js.msft.png "figure 20: onglet en-têtes"  
[ImageServer]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Server-js.msft.png "figure 21: modification de Server. js"  
<!--[ImageBuilding]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-server-js-edited.msft.png "Old Figure 22: The animation that indicates that the site is getting built"  -->  
[ImageRequests]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-main.msft.png "figure 22: la colonne taille affiche désormais 2 valeurs différentes pour les ressources texte"  
[ImageGzip]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-Network-Bundle-js-headers-Response.msft.png "figure 23: la section en-têtes de réponse contient désormais un `content-encoding` en-tête"  
[ImageReport2]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-audits-performance.msft.png "figure 24: un rapport d’audit après l’activation de la compression de texte"  
<!--[ImageResize]: /microsoft-edge/devtools-guide-chromium/media/speed-glitch-tony-remix-updated-audits-performance-opportunities-expanded.msft.png "Old Figure 27: Details about the properly size images opportunity"  -->
[ImageReport3]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-compression-Small-images-audits-performance.msft.png "figure 25: un rapport d’audit après le redimensionnement des images"  
[ImageRender]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-audits-performance-oppportunities-Expanded.msft.png "figure 26: informations supplémentaires sur l’opportunité de suppression des ressources de blocage du rendu"  
[ImageCommandMenu]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-audits-performance-oppportunities-Expanded-Command-coverage.msft.png "figure 27: ouverture du menu de commandes dans le volet d’audit"  
[ImageCoverage]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-audits-performance-oppportunities-Expanded-Drawer-coverage.msft.png "figure 28: onglet couverture"  
[ImageCoverageReport]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-audits-performance-oppportunities-Expanded-Drawer-Coverage-RELOADED.msft.png "figure 29: rapport de couverture"  
[ImageJQuery]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-sources-Drawer-Coverage-RELOADED-jQuery-js.msft.png "figure 30: affichage du fichier jQuery dans le panneau sources"  
[ImageBlocking]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Network-Drawer-Request-Blocking-Empty.msft.png "figure 31: onglet de blocage de requête"  
[ImageLibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Network-Drawer-Request-Blocking-added.msft.png "figure 32: ajout d’un modèle pour bloquer une requête dans l’annuaire libs"  
[ImageBlockedLibs]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-Network-RELOADED-Drawer-Request-Blocking-added.msft.png "figure 33: le panneau réseau indique que les requêtes ont été bloquées"  
[ImageReport4]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-2-audits-performance.msft.png "figure 34: un rapport d’audit après la suppression des ressources de blocage de rendu"  
[ImagePerformance]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-performance-Slow-Network-Slow-CPU.msft.png "figure 35: trace du panneau de performance du chargement de la page"  
[ImageOverview]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-main-Highlight.msft.png "figure 36: la section vue d’ensemble du suivi"  
[ImageUserTiming]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings.msft.png "figure 37: section minutages"  
[ImageMain]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-main.msft.png "figure 38: section principale"  
[ImageMine]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings-minebitcoin.msft.png "figure 39: survol de l’activité mineBitcoin"  
[ImageBottomUp]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-performance-Slow-Network-Slow-CPU-timings-Summary-minebitcoin.msft.png "figure 40: onglet inférieur"  
[ImageReport5]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-3-audits-performance.msft.png "Figure 41: un rapport d’audit après la configuration de WebPack pour utiliser le mode de production"  
[ImageReport6]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Speed-glitch-Tony-Remix-updated-4-audits-performance.msft.png "figure 42: un rapport d’audit après la suppression du fonctionnement JavaScript inutile"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReference]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference "Référence d’analyse des performances"  

[CourseraIntroductionWebDevelopmentClass]: https://www.coursera.org/learn/web-development#syllabus "Présentation de la classe développement Web | Coursera"  

[EssentialImageOptimization]: https://images.guide "Optimisation d’image essentielle"  

[MDNContentEncodingDirectives]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Encoding#Directives "Directives-Content-Encoding | MDN"  
[MDNUserTimingApi]: https://developer.mozilla.org/docs/Web/API/User_Timing_API "API de minutage des utilisateurs | MDN"  

[WebpackTreeShaking]: https://webpack.js.org/guides/tree-shaking "Faire secousses de l’arborescence | Pack d’intercomposition"  

> [!NOTE]
> <span data-ttu-id="07557-535">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="07557-535">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="07557-536">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="07557-536">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/speed/get-started) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="07557-538">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="07557-538">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
