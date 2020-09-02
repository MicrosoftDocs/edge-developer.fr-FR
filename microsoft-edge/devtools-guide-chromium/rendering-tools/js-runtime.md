---
title: Accélérer le runtime JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 801de4beeec29010ef63b2bcda950b57d4e544f7
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986184"
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

# <span data-ttu-id="9ca4a-103">Accélérer le runtime JavaScript</span><span class="sxs-lookup"><span data-stu-id="9ca4a-103">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="9ca4a-104">Identifiez les fonctions onéreuses à l’aide du panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="9ca4a-104">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="9ca4a-106">Exemples de profils</span><span class="sxs-lookup"><span data-stu-id="9ca4a-106">Sample Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="9ca4a-107">Résumé</span><span class="sxs-lookup"><span data-stu-id="9ca4a-107">Summary</span></span>  

*   <span data-ttu-id="9ca4a-108">Enregistrez exactement les fonctions qui ont été appelées et la quantité de mémoire requise par l’échantillonnage d’allocation dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="9ca4a-108">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="9ca4a-109">Visualisez vos profils sous forme de graphique à flamme.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-109">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="9ca4a-110">Enregistrer un profil d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="9ca4a-110">Record a Sampling Profile</span></span>  

<span data-ttu-id="9ca4a-111">Si vous remarquez Jank dans votre code JavaScript, recueillez un profil d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-111">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="9ca4a-112">Les profils d’échantillonnage montrent où le temps d’exécution est passé sur les fonctions de votre page.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-112">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="9ca4a-113">Accédez au panneau **mémoire** de devtools.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-113">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="9ca4a-114">Sélectionnez la case d’option d’échantillonnage de l' **attribution** .</span><span class="sxs-lookup"><span data-stu-id="9ca4a-114">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="9ca4a-115">Sélectionnez **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-115">Select **Start**.</span></span>  
1.  <span data-ttu-id="9ca4a-116">En fonction de ce que vous essayez d’analyser, vous pouvez recharger la page, interagir avec la page ou laisser la page s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-116">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="9ca4a-117">Lorsque vous avez terminé, cliquez sur le bouton **arrêter** .</span><span class="sxs-lookup"><span data-stu-id="9ca4a-117">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="9ca4a-118">Vous pouvez également utiliser l' [API utilitaires][DevtoolsConsoleUtilities] de la console pour enregistrer et grouper des profils à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-118">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="9ca4a-119">Afficher le profil d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="9ca4a-119">View Sampling Profile</span></span>  

<span data-ttu-id="9ca4a-120">Lorsque vous avez terminé l’enregistrement, DevTools renseigne automatiquement le panneau **mémoire** sous les **profils d’échantillonnage** avec les données de votre enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-120">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="9ca4a-121">Le mode par défaut est « **gros» (bas)**.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-121">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="9ca4a-122">Cet affichage vous permet de voir quelles fonctions ont le plus d’impact sur les performances et examine les chemins d’appel vers ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-122">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="9ca4a-123">Changer l’ordre de tri</span><span class="sxs-lookup"><span data-stu-id="9ca4a-123">Change sort order</span></span>  

<span data-ttu-id="9ca4a-124">Pour modifier l’ordre de tri, sélectionnez le menu déroulant en regard de la **fonction sélectionner le focus** , ![ ][ImageFocusIcon] puis sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-124">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="9ca4a-125">**Graphique**.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-125">**Chart**.</span></span>  <span data-ttu-id="9ca4a-126">Affiche un graphique chronologique de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-126">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Graphique à flamme" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="9ca4a-128">Graphique à flamme</span><span class="sxs-lookup"><span data-stu-id="9ca4a-128">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="9ca4a-129">**Gros (haut)**.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-129">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="9ca4a-130">Répertorie les fonctions en conséquence sur les performances et vous permet d’examiner les chemins d’appel aux fonctions.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-130">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="9ca4a-131">Il s’agit de l’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-131">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Graphique gros" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="9ca4a-133">Graphique gros</span><span class="sxs-lookup"><span data-stu-id="9ca4a-133">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="9ca4a-134">**Arborescence (haut vers le bas)**.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-134">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="9ca4a-135">Affiche une image globale de la structure de l’appel, en commençant par la partie supérieure de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-135">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Arborescence" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="9ca4a-137">Arborescence</span><span class="sxs-lookup"><span data-stu-id="9ca4a-137">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="9ca4a-138">Exclure des fonctions</span><span class="sxs-lookup"><span data-stu-id="9ca4a-138">Exclude functions</span></span>  

<span data-ttu-id="9ca4a-139">Pour exclure une fonction de votre profil d’échantillonnage, sélectionnez-la, puis **exclude selected function** sélectionnez le ![ bouton exclure la fonction sélectionnée ][ImageExcludeIcon]</span><span class="sxs-lookup"><span data-stu-id="9ca4a-139">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="9ca4a-140">La fonction de requête \ (parent \) de la fonction exclue \ (enfant \) est imputée à la mémoire allouée à la fonction exclue \ (enfant \).</span><span class="sxs-lookup"><span data-stu-id="9ca4a-140">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="9ca4a-141">Sélectionnez le bouton **restaurer toutes les fonctions** \ ( ![ restaurer toutes les fonctions ][ImageRestoreIcon] \) pour restaurer toutes les fonctions exclues dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-141">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="9ca4a-142">Afficher le profil d’échantillonnage sous forme de graphique</span><span class="sxs-lookup"><span data-stu-id="9ca4a-142">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="9ca4a-143">Le mode graphique fournit une représentation visuelle du profil d’échantillonnage au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-143">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="9ca4a-144">Après avoir [enregistré un profil d’échantillonnage](#record-a-sampling-profile), vous pouvez l’afficher en tant que graphique de type flamme en [modifiant l’ordre de tri](#change-sort-order) en **graphique**.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-144">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Affichage de graphique à flamme" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="9ca4a-146">Affichage de graphique à flamme</span><span class="sxs-lookup"><span data-stu-id="9ca4a-146">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="9ca4a-147">Le graphique à flamme est divisé en deux parties.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-147">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="9ca4a-148">index</span><span class="sxs-lookup"><span data-stu-id="9ca4a-148">index</span></span> | <span data-ttu-id="9ca4a-149">Quatrième</span><span class="sxs-lookup"><span data-stu-id="9ca4a-149">Part</span></span> | <span data-ttu-id="9ca4a-150">Description</span><span class="sxs-lookup"><span data-stu-id="9ca4a-150">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="9ca4a-151">1</span><span class="sxs-lookup"><span data-stu-id="9ca4a-151">1</span></span> | <span data-ttu-id="9ca4a-152">Présentation</span><span class="sxs-lookup"><span data-stu-id="9ca4a-152">Overview</span></span> | <span data-ttu-id="9ca4a-153">Un affichage attractif des oiseaux de l’ensemble de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-153">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="9ca4a-154">La hauteur des barres correspond à la profondeur de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-154">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="9ca4a-155">C’est pourquoi, plus la barre est grande, plus la pile d’appels est profonde.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-155">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="9ca4a-156">deuxième</span><span class="sxs-lookup"><span data-stu-id="9ca4a-156">2</span></span> | <span data-ttu-id="9ca4a-157">Piles d’appels</span><span class="sxs-lookup"><span data-stu-id="9ca4a-157">Call Stacks</span></span> | <span data-ttu-id="9ca4a-158">Il s’agit d’une vue détaillée des fonctions qui ont été appelées lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-158">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="9ca4a-159">L’axe horizontal est le temps et l’axe vertical est la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-159">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="9ca4a-160">Les piles sont organisées de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-160">The stacks are organized top-down.</span></span>  <span data-ttu-id="9ca4a-161">Par conséquent, la fonction en haut appelle celle qui s’en trouve au-dessous, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-161">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="9ca4a-162">Les fonctions apparaissent de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-162">Functions are colored randomly.</span></span>  <span data-ttu-id="9ca4a-163">Il n’existe aucune corrélation avec les couleurs utilisées dans les autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-163">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="9ca4a-164">Toutefois, les fonctions sont toujours les mêmes coloriées entre les appels, afin que vous puissiez voir les modèles dans chaque Runtime.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-164">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Graphique à flamme annotée" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="9ca4a-166">Graphique à flamme annotée</span><span class="sxs-lookup"><span data-stu-id="9ca4a-166">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="9ca4a-167">Une pile d’appels de haut niveau n’est pas nécessairement importante, cela signifie simplement que de nombreuses fonctions étaient appelées.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-167">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="9ca4a-168">Mais une barre larges signifie qu’une fonction a duré un certain temps.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-168">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="9ca4a-169">Ces suggestions peuvent être optimisées.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-169">These are candidates for optimization.</span></span>  

### <span data-ttu-id="9ca4a-170">Effectuer un zoom avant sur des parties spécifiques de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="9ca4a-170">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="9ca4a-171">Maintenez la touche CTRL enfoncée, puis faites glisser la souris vers la gauche et la droite pour effectuer un zoom avant sur certaines parties de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-171">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="9ca4a-172">Après le zoom, la pile d’appels affiche automatiquement la partie de l’enregistrement que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-172">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Zoom de graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="9ca4a-174">Zoom de graphique</span><span class="sxs-lookup"><span data-stu-id="9ca4a-174">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="9ca4a-175">Afficher les détails de la fonction</span><span class="sxs-lookup"><span data-stu-id="9ca4a-175">View function details</span></span>  

<span data-ttu-id="9ca4a-176">Sélectionnez sur une fonction pour afficher la définition dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="9ca4a-176">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="9ca4a-177">Pointez sur une fonction pour afficher les données de nom et de minutage.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-177">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="9ca4a-178">Les informations suivantes sont fournies.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-178">The following information is provided.</span></span>  

| <span data-ttu-id="9ca4a-179">Données</span><span class="sxs-lookup"><span data-stu-id="9ca4a-179">Detail</span></span> | <span data-ttu-id="9ca4a-180">Description</span><span class="sxs-lookup"><span data-stu-id="9ca4a-180">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="9ca4a-181">Name</span><span class="sxs-lookup"><span data-stu-id="9ca4a-181">Name</span></span>** | <span data-ttu-id="9ca4a-182">Nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-182">The name of the function.</span></span>  |  
| **<span data-ttu-id="9ca4a-183">Dimensionnement automatique</span><span class="sxs-lookup"><span data-stu-id="9ca4a-183">Self size</span></span>** | <span data-ttu-id="9ca4a-184">Taille de l’appel actif de la fonction, y compris uniquement les instructions de la fonction.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-184">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="9ca4a-185">Taille totale</span><span class="sxs-lookup"><span data-stu-id="9ca4a-185">Total size</span></span>** | <span data-ttu-id="9ca4a-186">La taille de l’appel en cours de cette fonction et des fonctions qu’elle appelle.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-186">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="9ca4a-187">URL</span><span class="sxs-lookup"><span data-stu-id="9ca4a-187">URL</span></span>** | <span data-ttu-id="9ca4a-188">L’emplacement de la définition de la fonction sous la forme `base.js:261` où `base.js` est le nom du fichier où la fonction est définie et `261` représente le numéro de ligne de la définition.</span><span class="sxs-lookup"><span data-stu-id="9ca4a-188">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Afficher les détails des fonctions dans le graphique" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="9ca4a-190">Afficher les détails des fonctions dans le graphique</span><span class="sxs-lookup"><span data-stu-id="9ca4a-190">View functions details in chart</span></span>  
:::image-end:::  

## <span data-ttu-id="9ca4a-191">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9ca4a-191">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageExcludeIcon]: ../media/exclude-icon.msft.png  
[ImageFocusIcon]: ../media/focus-icon.msft.png  
[ImageRestoreIcon]: ../media/restore-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleUtilities]: ../console/utilities.md "Référence sur l’API des utilitaires de console | Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfile]: ../console/utilities.md#profile "XXXXXXX XXXXXXX XXXXXXX XXXXXXX XXXXXXX Documents Microsoft"  
[DevtoolsConsoleUtilitiesProfileEnd]: ../console/utilities.md#profileend "profileEnd-xxx XXXXXXX XXXXXXX xxx xxxxxxx Documents Microsoft"  

> [!NOTE]
> <span data-ttu-id="9ca4a-195">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9ca4a-195">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9ca4a-196">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="9ca4a-196">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="9ca4a-198">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9ca4a-198">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
