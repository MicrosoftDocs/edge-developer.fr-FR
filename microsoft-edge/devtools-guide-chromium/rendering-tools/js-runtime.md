---
description: Identifiez les fonctions onéreuses à l’aide du volet Microsoft Edge DevTools Memory.
title: Accélérer le runtime JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f3cf0440579865495f4afc8b1ae4e3940af7b04f
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125355"
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

# <span data-ttu-id="a9a0d-104">Accélérer le runtime JavaScript</span><span class="sxs-lookup"><span data-stu-id="a9a0d-104">Speed up JavaScript runtime</span></span>  

<span data-ttu-id="a9a0d-105">Identifiez les fonctions onéreuses à l’aide du panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="a9a0d-105">Identify expensive functions using the **Memory** panel.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="a9a0d-107">Exemples de profils</span><span class="sxs-lookup"><span data-stu-id="a9a0d-107">Sample Profiles</span></span>  
:::image-end:::  

### <span data-ttu-id="a9a0d-108">Résumé</span><span class="sxs-lookup"><span data-stu-id="a9a0d-108">Summary</span></span>  

*   <span data-ttu-id="a9a0d-109">Enregistrez exactement les fonctions qui ont été appelées et la quantité de mémoire requise par l’échantillonnage d’allocation dans le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="a9a0d-109">Record exactly which functions were called and how much memory each requires with Allocation Sampling in the **Memory** panel.</span></span>  
*   <span data-ttu-id="a9a0d-110">Visualisez vos profils sous forme de graphique à flamme.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-110">Visualize your profiles as a flame chart.</span></span>  
    
## <span data-ttu-id="a9a0d-111">Enregistrer un profil d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="a9a0d-111">Record a Sampling Profile</span></span>  

<span data-ttu-id="a9a0d-112">Si vous remarquez Jank dans votre code JavaScript, recueillez un profil d’échantillonnage.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-112">If you notice jank in your JavaScript, collect a Sampling Profile.</span></span>  <span data-ttu-id="a9a0d-113">Les profils d’échantillonnage montrent où le temps d’exécution est passé sur les fonctions de votre page.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-113">Sampling Profiles show where running time is spent on functions in your page.</span></span>  

1.  <span data-ttu-id="a9a0d-114">Accédez au panneau **mémoire** de devtools.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-114">Go to the **Memory** panel of DevTools.</span></span>  
1.  <span data-ttu-id="a9a0d-115">Sélectionnez la case d’option d’échantillonnage de l' **attribution** .</span><span class="sxs-lookup"><span data-stu-id="a9a0d-115">Select the **Allocation sampling** radio button.</span></span>  
1.  <span data-ttu-id="a9a0d-116">Cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-116">Choose **Start**.</span></span>  
1.  <span data-ttu-id="a9a0d-117">En fonction de ce que vous essayez d’analyser, vous pouvez recharger la page, interagir avec la page ou laisser la page s’exécuter.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-117">Depending on what you are trying to analyze, you may either reload the page, interact with the page, or just let the page run.</span></span>  
1.  <span data-ttu-id="a9a0d-118">Lorsque vous avez terminé, cliquez sur le bouton **arrêter** .</span><span class="sxs-lookup"><span data-stu-id="a9a0d-118">Select the **Stop** button when you are finished.</span></span>  
    
> [!NOTE]
> <span data-ttu-id="a9a0d-119">Vous pouvez également utiliser l' [API utilitaires][DevtoolsConsoleUtilities] de la console pour enregistrer et grouper des profils à partir de la ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-119">You may also use the [Console Utilities API][DevtoolsConsoleUtilities] to record and group profiles from the command line.</span></span>  

## <span data-ttu-id="a9a0d-120">Afficher le profil d’échantillonnage</span><span class="sxs-lookup"><span data-stu-id="a9a0d-120">View Sampling Profile</span></span>  

<span data-ttu-id="a9a0d-121">Lorsque vous avez terminé l’enregistrement, DevTools renseigne automatiquement le panneau **mémoire** sous les **profils d’échantillonnage** avec les données de votre enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-121">When you finish recording, DevTools automatically populates the **Memory** panel under **SAMPLING PROFILES** with the data from your recording.</span></span>  

<span data-ttu-id="a9a0d-122">Le mode par défaut est « **gros» (bas)**.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-122">The default view is **Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="a9a0d-123">Cet affichage vous permet de voir quelles fonctions ont le plus d’impact sur les performances et examine les chemins d’appel vers ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-123">This view enables you to see which functions had the most impact on performance and examine the calling paths to those functions.</span></span>  

### <span data-ttu-id="a9a0d-124">Changer l’ordre de tri</span><span class="sxs-lookup"><span data-stu-id="a9a0d-124">Change sort order</span></span>  

<span data-ttu-id="a9a0d-125">Pour modifier l’ordre de tri, sélectionnez le menu déroulant en regard de la **fonction sélectionner le focus** , ![ ][ImageFocusIcon] puis sélectionnez l’une des options suivantes.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-125">To change the sorting order, select the dropdown menu next to the **focus selected function** \(![focus selected function][ImageFocusIcon]\) icon and then choose one of the following options.</span></span>

<span data-ttu-id="a9a0d-126">**Graphique**.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-126">**Chart**.</span></span>  <span data-ttu-id="a9a0d-127">Affiche un graphique chronologique de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-127">Displays a chronological chart of the recording.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="a9a0d-129">Graphique à flamme</span><span class="sxs-lookup"><span data-stu-id="a9a0d-129">Flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="a9a0d-130">**Gros (haut)**.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-130">**Heavy \(Bottom Up\)**.</span></span>  <span data-ttu-id="a9a0d-131">Répertorie les fonctions en conséquence sur les performances et vous permet d’examiner les chemins d’appel aux fonctions.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-131">Lists functions by impact on performance and enables you to examine the calling paths to the functions.</span></span>  <span data-ttu-id="a9a0d-132">Il s’agit de l’affichage par défaut.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-132">This is the default view.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-heavy-bottom-up.msft.png":::
   <span data-ttu-id="a9a0d-134">Graphique gros</span><span class="sxs-lookup"><span data-stu-id="a9a0d-134">Heavy chart</span></span>  
:::image-end:::  

<span data-ttu-id="a9a0d-135">**Arborescence (haut vers le bas)**.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-135">**Tree \(Top Down\)**.</span></span>  <span data-ttu-id="a9a0d-136">Affiche une image globale de la structure de l’appel, en commençant par la partie supérieure de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-136">Shows an overall picture of the calling structure, starting at the top of the call stack.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-tree-top-down.msft.png":::
   <span data-ttu-id="a9a0d-138">Arborescence</span><span class="sxs-lookup"><span data-stu-id="a9a0d-138">Tree chart</span></span>  
:::image-end:::  

### <span data-ttu-id="a9a0d-139">Exclure des fonctions</span><span class="sxs-lookup"><span data-stu-id="a9a0d-139">Exclude functions</span></span>  

<span data-ttu-id="a9a0d-140">Pour exclure une fonction de votre profil d’échantillonnage, sélectionnez-la, puis **exclude selected function** sélectionnez le ![ bouton exclure la fonction sélectionnée ][ImageExcludeIcon]</span><span class="sxs-lookup"><span data-stu-id="a9a0d-140">To exclude a function from your Sampling Profile, select it and then select the **exclude selected function** \(![exclude selected function][ImageExcludeIcon]\) button.</span></span>  <span data-ttu-id="a9a0d-141">La fonction de requête \ (parent \) de la fonction exclue \ (enfant \) est imputée à la mémoire allouée à la fonction exclue \ (enfant \).</span><span class="sxs-lookup"><span data-stu-id="a9a0d-141">The requesting function \(parent\) of the excluded function \(child\) is charged with the allocated memory assigned to the excluded function \(child\).</span></span>  

<span data-ttu-id="a9a0d-142">Sélectionnez le bouton **restaurer toutes les fonctions** \ ( ![ restaurer toutes les fonctions ][ImageRestoreIcon] \) pour restaurer toutes les fonctions exclues dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-142">Select the **restore all functions** \(![restore all functions][ImageRestoreIcon]\) button to restore all excluded functions back into the recording.</span></span>  

## <span data-ttu-id="a9a0d-143">Afficher le profil d’échantillonnage sous forme de graphique</span><span class="sxs-lookup"><span data-stu-id="a9a0d-143">View Sampling Profile as Chart</span></span>  

<span data-ttu-id="a9a0d-144">Le mode graphique fournit une représentation visuelle du profil d’échantillonnage au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-144">The Chart view provides a visual representation of the Sampling Profile over time.</span></span>  

<span data-ttu-id="a9a0d-145">Après avoir [enregistré un profil d’échantillonnage](#record-a-sampling-profile), vous pouvez l’afficher en tant que graphique de type flamme en [modifiant l’ordre de tri](#change-sort-order) en **graphique**.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-145">After you [record a Sampling Profile](#record-a-sampling-profile), view the recording as a flame chart by [changing the sort order](#change-sort-order) to **Chart**.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart.msft.png":::
   <span data-ttu-id="a9a0d-147">Affichage de graphique à flamme</span><span class="sxs-lookup"><span data-stu-id="a9a0d-147">Flame chart view</span></span>  
:::image-end:::  

<span data-ttu-id="a9a0d-148">Le graphique à flamme est divisé en deux parties.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-148">The flame chart is split into two parts.</span></span>  

| <span data-ttu-id="a9a0d-149">index</span><span class="sxs-lookup"><span data-stu-id="a9a0d-149">index</span></span> | <span data-ttu-id="a9a0d-150">Quatrième</span><span class="sxs-lookup"><span data-stu-id="a9a0d-150">Part</span></span> | <span data-ttu-id="a9a0d-151">Description</span><span class="sxs-lookup"><span data-stu-id="a9a0d-151">Description</span></span> |  
| --- |:--- |:--- |  
| <span data-ttu-id="a9a0d-152">1</span><span class="sxs-lookup"><span data-stu-id="a9a0d-152">1</span></span> | <span data-ttu-id="a9a0d-153">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="a9a0d-153">Overview</span></span> | <span data-ttu-id="a9a0d-154">Un affichage attractif des oiseaux de l’ensemble de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-154">A birds-eye view of the entire recording.</span></span>  <span data-ttu-id="a9a0d-155">La hauteur des barres correspond à la profondeur de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-155">The height of the bars correspond to the depth of the call stack.</span></span>  <span data-ttu-id="a9a0d-156">C’est pourquoi, plus la barre est grande, plus la pile d’appels est profonde.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-156">So, the higher the bar, the deeper the call stack.</span></span>  |  
| <span data-ttu-id="a9a0d-157">deuxième</span><span class="sxs-lookup"><span data-stu-id="a9a0d-157">2</span></span> | <span data-ttu-id="a9a0d-158">Piles d’appels</span><span class="sxs-lookup"><span data-stu-id="a9a0d-158">Call Stacks</span></span> | <span data-ttu-id="a9a0d-159">Il s’agit d’une vue détaillée des fonctions qui ont été appelées lors de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-159">This is an in-depth view of the functions that were called during the recording.</span></span>  <span data-ttu-id="a9a0d-160">L’axe horizontal est le temps et l’axe vertical est la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-160">The horizontal axis is time and vertical axis is the call stack.</span></span>  <span data-ttu-id="a9a0d-161">Les piles sont organisées de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-161">The stacks are organized top-down.</span></span>  <span data-ttu-id="a9a0d-162">Par conséquent, la fonction en haut appelle celle qui s’en trouve au-dessous, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-162">So, the function on top called the one below it, and so on.</span></span>  |  

<span data-ttu-id="a9a0d-163">Les fonctions apparaissent de façon aléatoire.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-163">Functions are colored randomly.</span></span>  <span data-ttu-id="a9a0d-164">Il n’existe aucune corrélation avec les couleurs utilisées dans les autres panneaux.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-164">There is no correlation to the colors used in the other panels.</span></span>  <span data-ttu-id="a9a0d-165">Toutefois, les fonctions sont toujours les mêmes coloriées entre les appels, afin que vous puissiez voir les modèles dans chaque Runtime.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-165">However, functions are always colored the same across invocations so that you are able to see patterns in each runtime.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-highlighted.msft.png":::
   <span data-ttu-id="a9a0d-167">Graphique à flamme annotée</span><span class="sxs-lookup"><span data-stu-id="a9a0d-167">Annotated flame chart</span></span>  
:::image-end:::  

<span data-ttu-id="a9a0d-168">Une pile d’appels de haut niveau n’est pas nécessairement importante, cela signifie simplement que de nombreuses fonctions étaient appelées.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-168">A tall call stack is not necessarily significant, it just means that a lot of functions were called.</span></span>  <span data-ttu-id="a9a0d-169">Mais une barre larges signifie qu’une fonction a duré un certain temps.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-169">But a wide bar means that a function took a long time to complete.</span></span>  <span data-ttu-id="a9a0d-170">Ces suggestions peuvent être optimisées.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-170">These are candidates for optimization.</span></span>  

### <span data-ttu-id="a9a0d-171">Effectuer un zoom avant sur des parties spécifiques de l’enregistrement</span><span class="sxs-lookup"><span data-stu-id="a9a0d-171">Zoom in on specific parts of recording</span></span>  

<span data-ttu-id="a9a0d-172">Maintenez la touche CTRL enfoncée, puis faites glisser la souris vers la gauche et la droite pour effectuer un zoom avant sur certaines parties de la pile d’appels.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-172">Select, hold, and drag your mouse left and right across the overview to zoom in on particular parts of the call stack.</span></span>  <span data-ttu-id="a9a0d-173">Après le zoom, la pile d’appels affiche automatiquement la partie de l’enregistrement que vous avez sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-173">After you zoom, the call stack automatically displays the portion of the recording that you selected.</span></span>  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-zoomed.msft.png":::
   <span data-ttu-id="a9a0d-175">Zoom de graphique</span><span class="sxs-lookup"><span data-stu-id="a9a0d-175">Chart zoomed</span></span>  
:::image-end:::  

### <span data-ttu-id="a9a0d-176">Afficher les détails de la fonction</span><span class="sxs-lookup"><span data-stu-id="a9a0d-176">View function details</span></span>  

<span data-ttu-id="a9a0d-177">Sélectionnez sur une fonction pour afficher la définition dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="a9a0d-177">Select on a function to view the definition in the **Sources** panel.</span></span>  

<span data-ttu-id="a9a0d-178">Pointez sur une fonction pour afficher les données de nom et de minutage.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-178">Hover over a function to display the name and timing data.</span></span>  <span data-ttu-id="a9a0d-179">Les informations suivantes sont fournies.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-179">The following information is provided.</span></span>  

| <span data-ttu-id="a9a0d-180">Données</span><span class="sxs-lookup"><span data-stu-id="a9a0d-180">Detail</span></span> | <span data-ttu-id="a9a0d-181">Description</span><span class="sxs-lookup"><span data-stu-id="a9a0d-181">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="a9a0d-182">Name</span><span class="sxs-lookup"><span data-stu-id="a9a0d-182">Name</span></span>** | <span data-ttu-id="a9a0d-183">Nom de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-183">The name of the function.</span></span>  |  
| **<span data-ttu-id="a9a0d-184">Dimensionnement automatique</span><span class="sxs-lookup"><span data-stu-id="a9a0d-184">Self size</span></span>** | <span data-ttu-id="a9a0d-185">Taille de l’appel actif de la fonction, y compris uniquement les instructions de la fonction.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-185">The size of the current invocation of the function, including only the statements in the function.</span></span>  |  
| **<span data-ttu-id="a9a0d-186">Taille totale</span><span class="sxs-lookup"><span data-stu-id="a9a0d-186">Total size</span></span>** | <span data-ttu-id="a9a0d-187">La taille de l’appel en cours de cette fonction et des fonctions qu’elle appelle.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-187">The size of the current invocation of this function and any functions that it called.</span></span>  |  
| **<span data-ttu-id="a9a0d-188">URL</span><span class="sxs-lookup"><span data-stu-id="a9a0d-188">URL</span></span>** | <span data-ttu-id="a9a0d-189">L’emplacement de la définition de la fonction sous la forme `base.js:261` où `base.js` est le nom du fichier où la fonction est définie et `261` représente le numéro de ligne de la définition.</span><span class="sxs-lookup"><span data-stu-id="a9a0d-189">The location of the function definition in the form of `base.js:261` where `base.js` is the name of the file where the function is defined and `261` is the line number of the definition.</span></span>  |  
<!--*   **Aggregated self time**.  Aggregate time for all invocations of the function across the recording, not including functions called by this function.  -->  
<!--*   **Aggregated total time**.  Aggregate total time for all invocations of the function, including functions called by this function.  -->  
<!--*   **Not optimized**.  If the profiler has detected a potential optimization for the function it lists it here.  -->  

:::image type="complex" source="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png" alt-text="Exemples de profils" lightbox="../media/rendering-tools-gh-nodejs-benchmarks-run-memory-sampling-profiles-chart-hover.msft.png":::
   <span data-ttu-id="a9a0d-191">Afficher les détails des fonctions dans le graphique</span><span class="sxs-lookup"><span data-stu-id="a9a0d-191">View functions details in chart</span></span>  
:::image-end:::  

## <span data-ttu-id="a9a0d-192">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="a9a0d-192">Getting in touch with the Microsoft Edge DevTools team</span></span>  

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
> <span data-ttu-id="a9a0d-196">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a9a0d-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a9a0d-197">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \) et [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="a9a0d-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/rendering-tools/js-execution) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Meggin Kearney][MegginKearney] \(Tech Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="a9a0d-199">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a9a0d-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
