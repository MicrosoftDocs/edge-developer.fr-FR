---
description: Identifiez les fonctions coûteuses à l’aide Microsoft Edge panneau Mémoire DevTools.
title: Accélérer le runtime JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bbac00ab46e205fb692cc3de3e5f08ba854b0911
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565084"
---
<!-- Copyright Kayce Basques and Meggin Kearney

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License. -->
# <a name="speed-up-javascript-runtime"></a><span data-ttu-id="dd177-104">Accélérer le runtime JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd177-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="dd177-105">Identifiez les fonctions coûteuses à l’aide **de l’outil** Mémoire.</span><span class="sxs-lookup"><span data-stu-id="dd177-105">Identify expensive functions using the **Memory** tool.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="dd177-107">Exemples de profils</span><span class="sxs-lookup"><span data-stu-id="dd177-107">Sample Profiles</span></span>  
:::image-end:::  

### <a name="summary"></a><span data-ttu-id="dd177-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="dd177-108">Summary</span></span>  

*   <span data-ttu-id="dd177-109">Enregistrez exactement les fonctions qui ont été appelées et la quantité de mémoire nécessaire avec l’échantillonnage d’allocation dans **l’outil Mémoire.**</span><span class="sxs-lookup"><span data-stu-id="dd177-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** tool.</span></span>  
*   <span data-ttu-id="dd177-110">Visualisez vos profils en tant que graphique graphique graphique.</span><span class="sxs-lookup"><span data-stu-id="dd177-110">Visualize your profiles as a flame chart.</span></span>  
    
## <a name="record-a-sampling-profile"></a><span data-ttu-id="dd177-111">Enregistrer un profil d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="dd177-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="dd177-112">Si vous remarquez jank dans votre JavaScript, collectez un profil d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="dd177-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="dd177-113">Les profils d’échantillonnage indiquent où le temps d’exécution est passé sur les fonctions de votre page.</span><span class="sxs-lookup"><span data-stu-id="dd177-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="dd177-114">Accédez à **l’outil** Mémoire de DevTools.</span><span class="sxs-lookup"><span data-stu-id="dd177-114">Navigate to the **Memory** tool of DevTools.</span></span>  
1.  <span data-ttu-id="dd177-115">Choisissez la **radio d’échantillonnage** d’allocation.</span><span class="sxs-lookup"><span data-stu-id="dd177-115">Choose the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="dd177-116">Choose **Start**.</span><span class="sxs-lookup"><span data-stu-id="dd177-116">Choose **Start**.</span></span>  
1.  <span data-ttu-id="dd177-117">Selon ce que vous essayez d’analyser, vous pouvez soit actualiser la page, interagir avec la page, soit laisser la page s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="dd177-117">Depending on what you are trying to analyze, you may either refresh the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="dd177-118">Lorsque **vous** avez terminé, sélectionnez le bouton Arrêter.</span><span class="sxs-lookup"><span data-stu-id="dd177-118">Choose the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="dd177-119">Vous pouvez également utiliser [l’API des utilitaires console][DevtoolsConsoleUtilities] pour enregistrer et grouper des profils à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="dd177-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <a name="view-sampling-profile"></a><span data-ttu-id="dd177-120">Afficher le profil d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="dd177-120">View Sampling Profile</span></span>  

<span data-ttu-id="dd177-121">Lorsque vous avez terminé l’enregistrement, DevTools remplit automatiquement le panneau Mémoire sous **PROFILS D’ÉCHANTILLONNAGE** avec les données de votre enregistrement. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="dd177-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="dd177-122">L’affichage par défaut **est Heavy \(Bottom Up\).**</span><span class="sxs-lookup"><span data-stu-id="dd177-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="dd177-123">Cette vue vous permet d’examiner les fonctions qui ont eu le plus d’impact sur les performances et d’examiner le chemin d’accès à la demande pour chaque fonction.</span><span class="sxs-lookup"><span data-stu-id="dd177-123">This view allows you to review which functions had the most impact on performance and examine the requesting path for each function.</span></span>  

### <a name="change-sort-order"></a><span data-ttu-id="dd177-124">Modifier l’ordre de tri</span><span class="sxs-lookup"><span data-stu-id="dd177-124">Change sort order</span></span>  

<span data-ttu-id="dd177-125">Pour modifier l’ordre de tri, sélectionnez le menu déroulant en face de l’icône de la fonction sélectionnée du **focus** \( focus selected function \), puis choisissez l’une des ![ options ](../media/focus-icon.msft.png) suivantes.</span><span class="sxs-lookup"><span data-stu-id="dd177-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function](../media/focus-icon.msft.png)\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="dd177-126">**Graphique**.</span><span class="sxs-lookup"><span data-stu-id="dd177-126">**Chart**.</span></span>  <span data-ttu-id="dd177-127">Affiche un graphique chronologique de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dd177-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Graphique de chart chart" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="dd177-129">Graphique de chart chart</span><span class="sxs-lookup"><span data-stu-id="dd177-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="dd177-130">**Heavy \(Bottom Up\)**.</span><span class="sxs-lookup"><span data-stu-id="dd177-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="dd177-131">Répertorie les fonctions par impact sur les performances et vous permet d’examiner les chemins d’accès appelants aux fonctions.</span><span class="sxs-lookup"><span data-stu-id="dd177-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="dd177-132">Il s’agit de l’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="dd177-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Graphique épais" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="dd177-134">Graphique épais</span><span class="sxs-lookup"><span data-stu-id="dd177-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="dd177-135">**Tree \(Top Down\)**.</span><span class="sxs-lookup"><span data-stu-id="dd177-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="dd177-136">Affiche une image globale de la structure d’appel, en commençant en haut de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="dd177-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Graphique d’arborescence" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="dd177-138">Graphique d’arborescence</span><span class="sxs-lookup"><span data-stu-id="dd177-138">Tree chart</span></span>  
:::image-end:::  

### <a name="exclude-functions"></a><span data-ttu-id="dd177-139">Exclure des fonctions</span><span class="sxs-lookup"><span data-stu-id="dd177-139">Exclude functions</span></span>  

<span data-ttu-id="dd177-140">Pour exclure une fonction de votre profil d’échantillonnage, choisissez-la, puis choisissez le bouton exclure la fonction sélectionnée **\(** exclure la ![ fonction sélectionnée ](../media/exclude-icon.msft.png) \).</span><span class="sxs-lookup"><span data-stu-id="dd177-140">To exclude a function from your Sampling Profile, choose it and then choose the **exclude selected function** \(![exclude selected function](../media/exclude-icon.msft.png)\) button.</span></span>  <span data-ttu-id="dd177-141">La fonction de demande \(parent\) de la fonction exclue \(enfant\) est chargée de la mémoire allouée affectée à la fonction exclue \(enfant\).</span><span class="sxs-lookup"><span data-stu-id="dd177-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="dd177-142">Sélectionnez le bouton restaurer **toutes les fonctions** \( restaurer toutes les fonctions \) pour restaurer toutes les fonctions ![ ](../media/restore-icon.msft.png) exclues dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dd177-142">Choose the **restore all functions** \(![restore all functions](../media/restore-icon.msft.png)\) button to restore all excluded functions back into the recording.</span></span>  

## <a name="view-sampling-profile-as-chart"></a><span data-ttu-id="dd177-143">Afficher le profil d’échantillonnage en tant que graphique</span><span class="sxs-lookup"><span data-stu-id="dd177-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="dd177-144">L’affichage Graphique fournit une représentation visuelle du profil d’échantillonnage au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="dd177-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="dd177-145">Après avoir [enregistré un profil d’échantillonnage,](#record-a-sampling-profile)affichez l’enregistrement sous la forme d’un graphique à graphiques en modifiant l’ordre [de tri](#change-sort-order) en **graphique.**</span><span class="sxs-lookup"><span data-stu-id="dd177-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Affichage Graphique de graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="dd177-147">Affichage Graphique de graphique</span><span class="sxs-lookup"><span data-stu-id="dd177-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="dd177-148">Le graphique en graphiques est divisé en deux parties.</span><span class="sxs-lookup"><span data-stu-id="dd177-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="dd177-149">index</span><span class="sxs-lookup"><span data-stu-id="dd177-149">index</span></span> | <span data-ttu-id="dd177-150">Partie</span><span class="sxs-lookup"><span data-stu-id="dd177-150">Part</span></span> | <span data-ttu-id="dd177-151">Description</span><span class="sxs-lookup"><span data-stu-id="dd177-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="dd177-152">1</span><span class="sxs-lookup"><span data-stu-id="dd177-152">1</span></span> | <span data-ttu-id="dd177-153">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="dd177-153">Overview</span></span> | <span data-ttu-id="dd177-154">Vue oculaire de l’intégralité de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dd177-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="dd177-155">La hauteur des barres correspond à la profondeur de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="dd177-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="dd177-156">Ainsi, plus la barre est élevée, plus la pile d’appels est profonde.</span><span class="sxs-lookup"><span data-stu-id="dd177-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="dd177-157">2</span><span class="sxs-lookup"><span data-stu-id="dd177-157">2</span></span> | <span data-ttu-id="dd177-158">Pile des appels</span><span class="sxs-lookup"><span data-stu-id="dd177-158">Call Stacks</span></span> | <span data-ttu-id="dd177-159">Il s’agit d’une vue détaillée des fonctions qui ont été appelées pendant l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="dd177-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="dd177-160">L’axe horizontal est le temps et l’axe vertical est la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="dd177-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="dd177-161">Les piles sont organisées de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="dd177-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="dd177-162">Ainsi, la fonction au-dessus appelait celle en dessous, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="dd177-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="dd177-163">Les fonctions sont colorées de manière aléatoire.</span><span class="sxs-lookup"><span data-stu-id="dd177-163">Functions are colored randomly.</span></span>  <span data-ttu-id="dd177-164">Il n’existe aucune corrélation avec les couleurs utilisées dans les autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="dd177-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="dd177-165">Toutefois, les fonctions sont toujours colorées de la même façon entre les appels, de sorte que vous pouvez observer les modèles dans chaque runtime.</span><span class="sxs-lookup"><span data-stu-id="dd177-165">However, functions are always colored the same across invocations so that you may observe patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Graphique en graphiques à graphiques à annoter" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="dd177-167">Graphique en graphiques à graphiques à annoter</span><span class="sxs-lookup"><span data-stu-id="dd177-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="dd177-168">Une pile d’appels de grande taille n’est pas nécessairement significative, cela signifie simplement que de nombreuses fonctions ont été appelées.</span><span class="sxs-lookup"><span data-stu-id="dd177-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="dd177-169">Toutefois, une barre large signifie qu’une fonction a mis beaucoup de temps à se terminer.</span><span class="sxs-lookup"><span data-stu-id="dd177-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="dd177-170">Ce sont des candidats à l’optimisation.</span><span class="sxs-lookup"><span data-stu-id="dd177-170">These are candidates for optimization.</span></span>  

### <a name="zoom-in-on-specific-parts-of-recording"></a><span data-ttu-id="dd177-171">Zoom sur des parties spécifiques de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="dd177-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="dd177-172">Choisissez, maintenez la souris à gauche et à droite dans la vue d’ensemble, puis faites glisser la souris vers la gauche pour zoomer sur des parties particulières de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="dd177-172">Choose, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="dd177-173">Après avoir zoomé, la pile d’appels affiche automatiquement la partie de l’enregistrement que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="dd177-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Graphique avec zoom" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="dd177-175">Graphique avec zoom</span><span class="sxs-lookup"><span data-stu-id="dd177-175">Chart zoomed</span></span>  
:::image-end:::  

### <a name="view-function-details"></a><span data-ttu-id="dd177-176">Afficher les détails de la fonction</span><span class="sxs-lookup"><span data-stu-id="dd177-176">View function details</span></span>  

<span data-ttu-id="dd177-177">Choisissez une fonction pour afficher la définition dans **l’outil Sources.**</span><span class="sxs-lookup"><span data-stu-id="dd177-177">Choose a function to view the definition in the **Sources** tool.</span></span>  

<span data-ttu-id="dd177-178">Pointez sur une fonction pour afficher le nom et les données de minutage.</span><span class="sxs-lookup"><span data-stu-id="dd177-178">Hover on a function to display the name and timing data.</span></span>  <span data-ttu-id="dd177-179">Les informations suivantes sont fournies.</span><span class="sxs-lookup"><span data-stu-id="dd177-179">The following information is provided.</span></span>  

| <span data-ttu-id="dd177-180">Détail</span><span class="sxs-lookup"><span data-stu-id="dd177-180">Detail</span></span> | <span data-ttu-id="dd177-181">Description</span><span class="sxs-lookup"><span data-stu-id="dd177-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="dd177-182">Name</span><span class="sxs-lookup"><span data-stu-id="dd177-182">Name</span></span>** | <span data-ttu-id="dd177-183">Nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="dd177-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="dd177-184">Taille autonome</span><span class="sxs-lookup"><span data-stu-id="dd177-184">Self size</span></span>** | <span data-ttu-id="dd177-185">Taille de l’appel actuel de la fonction, y compris uniquement les instructions dans la fonction.</span><span class="sxs-lookup"><span data-stu-id="dd177-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="dd177-186">Taille totale</span><span class="sxs-lookup"><span data-stu-id="dd177-186">Total size</span></span>** | <span data-ttu-id="dd177-187">Taille de l’appel actuel de cette fonction et de toutes les fonctions qu’elle a appelées.</span><span class="sxs-lookup"><span data-stu-id="dd177-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="dd177-188">URL</span><span class="sxs-lookup"><span data-stu-id="dd177-188">URL</span></span>** | <span data-ttu-id="dd177-189">L’emplacement de la définition de fonction sous la forme où est le nom du fichier où la fonction est définie et est le numéro de ligne `base.js:261` `base.js` de la `261` définition.</span><span class="sxs-lookup"><span data-stu-id="dd177-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Afficher les détails des fonctions dans le graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="dd177-191">Afficher les détails des fonctions dans le graphique</span><span class="sxs-lookup"><span data-stu-id="dd177-191">View functions details in chart</span></span>  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="dd177-192">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="dd177-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Référence de l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "profile - Console utilities API reference | Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd - Référence de l’API des utilitaires de console | Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="dd177-196">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd177-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="dd177-197">La page d’origine est trouvée ici et est co-auteure par [Les Basques DeCénais (Rédacteur][KayceBasques] technique, Chrome DevTools \& Writer\) et [Meggin Kearney][MegginKearney] \(Tech Writer\). [](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution)</span><span class="sxs-lookup"><span data-stu-id="dd177-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="dd177-199">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="dd177-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
