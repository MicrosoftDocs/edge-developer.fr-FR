---
title: Résoudre les problèmes de mémoire
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 738ef5fe682633f3100345c922ff12c3c27a7166
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611761"
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





# <span data-ttu-id="e8b7f-103">Résoudre les problèmes de mémoire</span><span class="sxs-lookup"><span data-stu-id="e8b7f-103">Fix Memory Problems</span></span>   



<span data-ttu-id="e8b7f-104">Découvrez comment utiliser Microsoft Edge et DevTools pour rechercher des problèmes de mémoire qui affectent les performances de la page, notamment les fuites de mémoire, l’augmentation de la mémoire et les nettoyages de mémoire fréquents.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-104">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="e8b7f-105">Résumé</span><span class="sxs-lookup"><span data-stu-id="e8b7f-105">Summary</span></span>  

*   <span data-ttu-id="e8b7f-106">Déterminez la quantité de mémoire utilisée par votre page avec le gestionnaire des tâches du navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-106">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="e8b7f-107">Visualisez l’utilisation de la mémoire au fil du temps avec le panneau **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-107">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="e8b7f-108">Identifiez les arborescences DOM détachées \ (une cause courante de fuites de mémoire \) avec **instantané de tas**.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-108">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="e8b7f-109">Déterminez quand une nouvelle mémoire est allouée dans votre segment JavaScript \ (JS Heap \) avec l' **instrumentation d’allocation sur la chronologie**.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-109">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="e8b7f-110">Présentation</span><span class="sxs-lookup"><span data-stu-id="e8b7f-110">Overview</span></span>  

<span data-ttu-id="e8b7f-111">Dans l’esprit du modèle de performance des **rails** , le focus de vos efforts de performance doit être vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-111">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="e8b7f-112">Des problèmes de mémoire sont importants, car ils sont souvent perceptibles par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-112">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="e8b7f-113">Les utilisateurs peuvent percevoir des problèmes de mémoire de l’une des façons suivantes:</span><span class="sxs-lookup"><span data-stu-id="e8b7f-113">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="e8b7f-114">**Les performances d’une page sont progressivement pires dans le temps**.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-114">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="e8b7f-115">Il peut s’agir d’un symptôme de fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-115">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="e8b7f-116">Une fuite de mémoire se produit lorsqu’un bogue dans la page entraîne l’utilisation progressive de la page avec une plus grande quantité de mémoire au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-116">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="e8b7f-117">**Les performances d’une page sont incorrectes**.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-117">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="e8b7f-118">Il s’agit peut-être d’un problème de dilatation de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-118">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="e8b7f-119">L’utilisation de la mémoire est une augmentation de la quantité de mémoire requise pour une page de plus en plus rapide.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-119">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="e8b7f-120">**Les performances d’une page sont retardées ou semblent être suspendues fréquemment**.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-120">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="e8b7f-121">C’est peut-être le symptôme de nettoyages de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-121">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="e8b7f-122">Le nettoyage de la mémoire se trouve lorsque le navigateur récupère de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-122">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="e8b7f-123">Le navigateur détermine à quel moment cela se produit.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-123">The browser decides when this happens.</span></span>  <span data-ttu-id="e8b7f-124">Pendant les collections, tout le script en cours d’exécution est en pause.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-124">During collections, all script running is paused.</span></span>  <span data-ttu-id="e8b7f-125">Par conséquent, si le navigateur est en nettoyage de la mémoire, le script Runtime va être mis en pause beaucoup.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-125">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="e8b7f-126">Augmentation de la mémoire: le volume est «trop».</span><span class="sxs-lookup"><span data-stu-id="e8b7f-126">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="e8b7f-127">Il est facile de définir une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-127">A memory leak is easy to define.</span></span>  <span data-ttu-id="e8b7f-128">Si un site utilise une plus grande quantité de mémoire, cela signifie que vous avez une fuite.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-128">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="e8b7f-129">Mais l’augmentation de la quantité de mémoire est un peu plus difficile à épingler.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-129">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="e8b7f-130">Quels sont les critères d’utilisation trop importante de la mémoire?</span><span class="sxs-lookup"><span data-stu-id="e8b7f-130">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="e8b7f-131">Il n’y a pas de numéro de papier ici, car les différents appareils et navigateurs ont différentes fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-131">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="e8b7f-132">La même page qui s’exécute correctement sur un smartphone haut de gamme est susceptible de se bloquer sur un smartphone bas de gamme.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-132">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="e8b7f-133">Pour ce faire, vous pouvez utiliser le modèle de RAIL et sélectionner vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-133">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="e8b7f-134">Découvrez quels appareils sont populaires avec vos utilisateurs et testez votre page sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-134">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="e8b7f-135">S’il s’agit d’un problème de bonne qualité, il est possible que la page dépasse les capacités de mémoire de ces derniers.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-135">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="e8b7f-136">Surveiller l’utilisation de la mémoire en temps réel à l’aide du gestionnaire des tâches du navigateur Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e8b7f-136">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="e8b7f-137">Utilisez le gestionnaire des tâches du navigateur Microsoft Edge comme point de départ pour l’examen de votre problème de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-137">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="e8b7f-138">Le gestionnaire des tâches du navigateur Microsoft Edge est un moniteur en temps réel qui vous indique la quantité de mémoire utilisée actuellement par une page.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-138">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="e8b7f-139">`Shift` + `Esc` **More tools**  >  Pour ouvrir le gestionnaire des tâches du navigateur Microsoft Edge, appuyez ou accédez au menu principal de Microsoft Edge et sélectionnez autres outils du**Gestionnaire des tâches** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-139">Press `Shift`+`Esc` or go to the Microsoft Edge main menu and select **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    > ##### <span data-ttu-id="e8b7f-140">Figure1</span><span class="sxs-lookup"><span data-stu-id="e8b7f-140">Figure 1</span></span>  
    > <span data-ttu-id="e8b7f-141">Ouverture du gestionnaire des tâches du navigateur Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e8b7f-141">Opening the Microsoft Edge Browser Task Manager</span></span>  
    > ![Ouverture du gestionnaire des tâches du navigateur Microsoft Edge][ImageTaskManager]  
    
1.  <span data-ttu-id="e8b7f-143">Cliquez avec le bouton droit sur l’en-tête de tableau du gestionnaire des tâches du navigateur Microsoft Edge et activez la **mémoire JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-143">Right-click on the table header of the Microsoft Edge Browser Task Manager and enable **JavaScript memory**.</span></span>  
    
    > ##### <span data-ttu-id="e8b7f-144">Figure 2</span><span class="sxs-lookup"><span data-stu-id="e8b7f-144">Figure 2</span></span>  
    > <span data-ttu-id="e8b7f-145">Activer la mémoire JavaScript</span><span class="sxs-lookup"><span data-stu-id="e8b7f-145">Enable JavaScript memory</span></span>  
    > ![Activer la mémoire JavaScript][ImageJavascriptMemory]  
    
<span data-ttu-id="e8b7f-147">Les deux colonnes suivantes vous expliquent comment votre page utilise la mémoire:</span><span class="sxs-lookup"><span data-stu-id="e8b7f-147">These two columns tell you different things about how your page is using memory:</span></span>  

*   <span data-ttu-id="e8b7f-148">La colonne **Memory** représente une mémoire native.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-148">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="e8b7f-149">Les nœuds DOM sont stockés dans la mémoire native.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-149">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="e8b7f-150">Si cette valeur augmente, les nœuds DOM sont créés.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-150">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="e8b7f-151">La colonne de **mémoire JavaScript** représente le tas js.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-151">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="e8b7f-152">Cette colonne contient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-152">This column contains two values.</span></span>  <span data-ttu-id="e8b7f-153">La valeur qui vous intéresse correspond au numéro dynamique \ (le nombre entre parenthèses \).</span><span class="sxs-lookup"><span data-stu-id="e8b7f-153">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="e8b7f-154">Le numéro dynamique représente la quantité de mémoire utilisée par les objets joignable sur votre page.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-154">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="e8b7f-155">Si ce nombre augmente, les nouveaux objets sont créés ou les objets existants sont en augmentation.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-155">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="e8b7f-156">Visualiser les fuites de mémoire à l’aide du panneau de performance</span><span class="sxs-lookup"><span data-stu-id="e8b7f-156">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="e8b7f-157">Vous pouvez également utiliser le volet performance comme un autre point de départ dans votre examen.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-157">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="e8b7f-158">Le panneau performance vous permet de visualiser l’utilisation de la mémoire d’une page dans le temps.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-158">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="e8b7f-159">Ouvrez le panneau de **performance** sur devtools.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-159">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="e8b7f-160">Cochez la case **mémoire** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-160">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="e8b7f-161">[Créer un enregistrement][DevtoolsEvaluatePerformanceReferenceRecord]</span><span class="sxs-lookup"><span data-stu-id="e8b7f-161">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="e8b7f-162">Il est recommandé de démarrer et de mettre fin à l’enregistrement grâce à un nettoyage de la mémoire forcé.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-162">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="e8b7f-163">Cliquez sur le bouton **recueillir** le nettoyage de la mémoire pour le nettoyage de la mémoire ![ ][ImageForceGarbageCollectionIcon] .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-163">Click the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="e8b7f-164">Pour illustrer les enregistrements de mémoire, considérez le code ci-dessous:</span><span class="sxs-lookup"><span data-stu-id="e8b7f-164">To demonstrate memory recordings, consider the code below:</span></span>  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="e8b7f-165">Chaque fois que le bouton référencé dans le code est enfoncé, les `div` nœuds 10000 sont ajoutés au corps du document et une chaîne de 1 million `x` caractères est transplacée sur le `x` tableau.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-165">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="e8b7f-166">L’exécution de ce code génère un enregistrement dans le panneau **performances** , comme [figure 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="e8b7f-166">Running this code produces a recording in the **Performance** panel like [Figure 3](#figure-3).</span></span>  

> ##### <span data-ttu-id="e8b7f-167">Figure3</span><span class="sxs-lookup"><span data-stu-id="e8b7f-167">Figure 3</span></span>  
> <span data-ttu-id="e8b7f-168">Croissance simple</span><span class="sxs-lookup"><span data-stu-id="e8b7f-168">Simple growth</span></span>  
> ![Croissance simple][ImageSimpleGrowth]  

<span data-ttu-id="e8b7f-170">Tout d’abord, explication de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-170">First, an explanation of the user interface.</span></span>  <span data-ttu-id="e8b7f-171">Le graphique **tas** dans le volet **vue d’ensemble** \ (sous **net**\) représente le tas js.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-171">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="e8b7f-172">Le volet de **vue d’ensemble** est le volet de **compteur** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-172">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="e8b7f-173">Ici, vous pouvez voir l’utilisation de la mémoire divisée par le tas JS \ (similaire au graphique de **tas** dans le volet **vue d’ensemble** ), aux documents, aux nœuds DOM, aux écouteurs et à la mémoire GPU.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-173">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="e8b7f-174">La désactivation d’une case à cocher masque celle-ci du graphique.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-174">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="e8b7f-175">À présent, une analyse du code comparé à la [figure 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="e8b7f-175">Now, an analysis of the code compared with [Figure 3](#figure-3).</span></span>  <span data-ttu-id="e8b7f-176">Si vous examinez le compteur de nœuds \ (le graphique vert), vous pouvez voir qu’il correspond au code.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-176">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="e8b7f-177">Le nombre de nœuds augmente par étapes discrètes.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-177">The node count increases in discrete steps.</span></span>  <span data-ttu-id="e8b7f-178">Vous pouvez supposer que chaque augmentation du nombre de nœuds est un appel à `grow()` .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-178">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="e8b7f-179">Le graphique de tas JS \ (graphique bleu \) n’est pas aussi simple.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-179">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="e8b7f-180">Conformément aux meilleures pratiques, le premier DIP est en fait un nettoyage de la mémoire forcé (atteint en appuyant sur le bouton **collecter** le nettoyage de la mémoire ![ ][ImageForceGarbageCollectionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="e8b7f-180">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="e8b7f-181">En cours d’enregistrement, vous pouvez voir que la taille du tas JS pointe.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-181">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="e8b7f-182">Il s’agit d’une opération naturelle et normale: le code JavaScript crée les nœuds DOM sur chaque bouton click et effectue un grand nombre de travail lors de la création de la chaîne de 1 million caractères.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-182">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button click and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="e8b7f-183">Dans le cas présent, il s’agit du fait que le tas JS se termine plus haut que le début du nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-183">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="e8b7f-184">Dans le monde réel, si vous avez remarqué ce modèle d’augmentation de la taille du tas et de la taille de nœud JS, il peut éventuellement définir une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-184">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="e8b7f-185">Découvrir des fuites de mémoire d’arborescence DOM détachées avec des instantanés de tas</span><span class="sxs-lookup"><span data-stu-id="e8b7f-185">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="e8b7f-186">Un nœud DOM est uniquement nettoyé lorsqu’il n’y a aucune référence au nœud à partir de l’arborescence DOM ou du code JavaScript en cours d’exécution sur la page.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-186">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="e8b7f-187">Un nœud est considéré comme «détaché» lorsque ce dernier est supprimé de l’arborescence DOM, mais que du JavaScript le référence encore.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-187">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="e8b7f-188">Les nœuds DOM dissociés sont une cause courante de fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-188">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="e8b7f-189">Cette section vous explique comment utiliser les profileurs de tas dans DevTools pour identifier les nœuds détachés.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-189">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="e8b7f-190">Voici un exemple simple de nœuds DOM dissociés.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-190">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedNodes;
function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedNodes = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="e8b7f-191">Un clic sur le bouton référencé dans le code crée un `ul` nœud avec dix `li` enfants.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-191">Clicking the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="e8b7f-192">Ces nœuds sont référencés par le code mais n’existent pas dans l’arborescence DOM, de sorte que chacun d’eux est détaché.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-192">These nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="e8b7f-193">Les instantanés de tas permettent d’identifier les nœuds détachés.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-193">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="e8b7f-194">Comme son nom l’indique, les instantanés de tas vous montrent la manière dont la mémoire est distribuée entre les objets JS et les nœuds DOM de votre page au moment de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-194">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="e8b7f-195">Pour créer une capture d’écran, ouvrez DevTools et accédez au panneau **mémoire** , sélectionnez la case d’option **instantané de tas** , puis appuyez sur le bouton **prendre un cliché instantané** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-195">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

> ##### <span data-ttu-id="e8b7f-196">Figure 4</span><span class="sxs-lookup"><span data-stu-id="e8b7f-196">Figure 4</span></span>  
> <span data-ttu-id="e8b7f-197">Instantané de tas</span><span class="sxs-lookup"><span data-stu-id="e8b7f-197">Take heap snapshot</span></span>  
> ![Instantané de tas][ImageTakeHeapSnapshot]  

<span data-ttu-id="e8b7f-199">Le processus et le chargement de l’instantané risquent de prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-199">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="e8b7f-200">Lorsque vous avez terminé, sélectionnez-le dans le volet de gauche \ ( **instantanés de tas**nommés \).</span><span class="sxs-lookup"><span data-stu-id="e8b7f-200">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="e8b7f-201">Entrez `Detached` dans la zone de texte de **filtre de classe** pour rechercher des arborescences DOM détachées.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-201">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

> ##### <span data-ttu-id="e8b7f-202">Figure 5</span><span class="sxs-lookup"><span data-stu-id="e8b7f-202">Figure 5</span></span>  
> <span data-ttu-id="e8b7f-203">Filtrage pour les nœuds détachés</span><span class="sxs-lookup"><span data-stu-id="e8b7f-203">Filtering for detached nodes</span></span>  
> ![Filtrage pour les nœuds détachés][ImageFilteringForDetachedNodes]  

<span data-ttu-id="e8b7f-205">Développez le carats pour examiner une arborescence dissociée.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-205">Expand the carats to investigate a detached tree.</span></span>  

> ##### <span data-ttu-id="e8b7f-206">Figure 6</span><span class="sxs-lookup"><span data-stu-id="e8b7f-206">Figure 6</span></span>  
> <span data-ttu-id="e8b7f-207">Examen de l’arborescence dissociée</span><span class="sxs-lookup"><span data-stu-id="e8b7f-207">Investigating detached tree</span></span>  
> ![Examen de l’arborescence dissociée][ImageInvestigatingDetachedTree]  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="e8b7f-209">Cliquez sur un nœud pour le rechercher davantage.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-209">Click on a node to investigate it further.</span></span>  <span data-ttu-id="e8b7f-210">Dans le volet **objets** , vous pouvez afficher davantage d’informations sur le code qui fait référence à celle-ci.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-210">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="e8b7f-211">Par exemple, dans la [figure 7](#figure-7) , vous pouvez voir que la `detachedNodes` variable fait référence au nœud.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-211">For example, in [Figure 7](#figure-7) you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="e8b7f-212">Pour corriger cette fuite de mémoire particulière, vous devez examiner le code qui utilise la `detachedUNode` variable et garantir que la référence au nœud est supprimée lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-212">To fix this particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>

> ##### <span data-ttu-id="e8b7f-213">Figure 7</span><span class="sxs-lookup"><span data-stu-id="e8b7f-213">Figure 7</span></span>  
> <span data-ttu-id="e8b7f-214">Examen d’un nœud</span><span class="sxs-lookup"><span data-stu-id="e8b7f-214">Investigating a node</span></span>  
> ![Examen d’un nœud][ImageInvestigatingNode]  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="e8b7f-216">Identifier les fuites de mémoire du tas JS avec l’instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="e8b7f-216">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="e8b7f-217">L' **instrumentation d’allocation sur la chronologie** est un autre outil qui peut vous aider à effectuer le suivi des fuites de mémoire dans votre tas js.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-217">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="e8b7f-218">Montrez l' **instrumentation d’allocation sur la chronologie** en utilisant le code suivant.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-218">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="e8b7f-219">Chaque fois que le bouton référencé dans le code est envoyé, une chaîne de 1 million caractères est ajoutée au `x` tableau.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-219">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="e8b7f-220">Pour enregistrer une instrumentation d’allocation sur la chronologie, ouvrez DevTools, accédez au volet **mémoire** , sélectionnez la case **d’option allocation d’attribution sur la chronologie** , appuyez sur le bouton **Démarrer** , effectuez l’action que vous suspectez à l’origine de la fuite de mémoire, puis appuyez sur le bouton arrêter l’enregistrement du **profil de tas** ![ ][ImageStopRecordingIcon] lorsque vous avez terminé.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-220">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="e8b7f-221">Lors de l’enregistrement, Notez que les barres bleues s’affichent dans la barre de Planning (par exemple, dans la [figure 8](#figure-8)).</span><span class="sxs-lookup"><span data-stu-id="e8b7f-221">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in [Figure 8](#figure-8).</span></span>  

> ##### <span data-ttu-id="e8b7f-222">Figure8</span><span class="sxs-lookup"><span data-stu-id="e8b7f-222">Figure 8</span></span>  
> <span data-ttu-id="e8b7f-223">Nouvelles attributions</span><span class="sxs-lookup"><span data-stu-id="e8b7f-223">New allocations</span></span>  
> ![Nouvelles attributions][ImageNewAllocations]  

<span data-ttu-id="e8b7f-225">Ces barres bleues représentent de nouvelles allocations de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-225">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="e8b7f-226">Ces nouvelles allocations de mémoire sont vos candidats à des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-226">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="e8b7f-227">Vous pouvez effectuer un zoom sur une barre pour filtrer le volet **constructor** de façon à afficher uniquement les objets alloués au cours de la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-227">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

> ##### <span data-ttu-id="e8b7f-228">Figure9</span><span class="sxs-lookup"><span data-stu-id="e8b7f-228">Figure 9</span></span>  
> <span data-ttu-id="e8b7f-229">Chronologie de l’attribution avec zoom</span><span class="sxs-lookup"><span data-stu-id="e8b7f-229">Zoomed allocation timeline</span></span>  
> ![Chronologie de l’attribution avec zoom][ImageZoomedAllocationTimeline]  

<span data-ttu-id="e8b7f-231">Développez l’objet, puis cliquez sur la valeur pour afficher plus de détails dans le volet des **objets** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-231">Expand the object and click on the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="e8b7f-232">Par exemple, dans la [figure 10](#figure-10), en affichant les détails de l’objet nouvellement alloué, vous devez être en mesure de voir qu’il a été alloué à la `x` variable dans l' `Window` étendue.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-232">For example, in [Figure 10](#figure-10), by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

> ##### <span data-ttu-id="e8b7f-233">Figure10</span><span class="sxs-lookup"><span data-stu-id="e8b7f-233">Figure 10</span></span> 
> <span data-ttu-id="e8b7f-234">Détails de l’objet</span><span class="sxs-lookup"><span data-stu-id="e8b7f-234">Object details</span></span>  
> ![Détails de l’objet][ImageObjectDetail]  

## <span data-ttu-id="e8b7f-236">Examiner l’allocation de mémoire par fonction</span><span class="sxs-lookup"><span data-stu-id="e8b7f-236">Investigate memory allocation by function</span></span>   

<span data-ttu-id="e8b7f-237">Utilisez le type de classement d' **échantillonnage de répartition** pour afficher l’allocation de mémoire par la fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-237">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

> ##### <span data-ttu-id="e8b7f-238">Figure11</span><span class="sxs-lookup"><span data-stu-id="e8b7f-238">Figure 11</span></span>  
> <span data-ttu-id="e8b7f-239">Echantillonnage d’allocation d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="e8b7f-239">Record Allocation sampling</span></span>  
> ![Echantillonnage d’allocation d’enregistrement][ImageRecordAllocationSampling]  

1.  <span data-ttu-id="e8b7f-241">Sélectionnez la case d’option d’échantillonnage de l' **attribution** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-241">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="e8b7f-242">S’il existe un ouvrier sur la page, vous pouvez le sélectionner en tant que cible de profilage à l’aide du menu déroulant en regard du bouton **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-242">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="e8b7f-243">Appuyez sur le bouton **Démarrer** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-243">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="e8b7f-244">Effectuez les actions sur la page que vous voulez examiner.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-244">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="e8b7f-245">Lorsque vous avez terminé, appuyez sur le bouton **arrêter** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-245">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="e8b7f-246">DevTools montre une répartition de la capacité d’allocation de mémoire par fonction.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-246">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="e8b7f-247">Le mode par défaut est **gras (en bas)**, qui affiche les fonctions qui ont alloué la plus grande quantité de mémoire en haut.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-247">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

> ##### <span data-ttu-id="e8b7f-248">Figure12</span><span class="sxs-lookup"><span data-stu-id="e8b7f-248">Figure 12</span></span>  
> <span data-ttu-id="e8b7f-249">Echantillonnage d’attribution</span><span class="sxs-lookup"><span data-stu-id="e8b7f-249">Allocation sampling</span></span>  
>![Echantillonnage d’attribution][ImageAllocationSampling]  

## <span data-ttu-id="e8b7f-251">Nettoyage de la mémoire</span><span class="sxs-lookup"><span data-stu-id="e8b7f-251">Spot frequent garbage collections</span></span>  

<span data-ttu-id="e8b7f-252">Si votre page semble être suspendue fréquemment, il est possible que vous ayez des problèmes de nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-252">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="e8b7f-253">Vous pouvez utiliser le gestionnaire des tâches du navigateur Microsoft Edge ou des enregistrements de mémoire de performance pour détecter régulièrement un nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-253">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="e8b7f-254">Dans le gestionnaire des tâches du navigateur Microsoft Edge, il est fréquent de hausser et de reculer la **mémoire** ou les valeurs de **mémoire JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="e8b7f-254">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="e8b7f-255">Dans les enregistrements de performance, les changements fréquents (augmentation et chute) du tas ou du nombre de nœuds JS indiquent fréquemment un nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-255">In Performance recordings, frequent changes (rising and falling) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="e8b7f-256">Une fois que vous avez identifié le problème, vous pouvez utiliser un **instrumentation d’allocation sur la chronologie** pour savoir où la quantité de mémoire est allouée et quelles fonctions entraînent les attributions.</span><span class="sxs-lookup"><span data-stu-id="e8b7f-256">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageForceGarbageCollectionIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-recording-icon.msft.png  

[ImageTaskManager]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png "Figure 1: ouverture du gestionnaire des tâches du navigateur Microsoft Edge"  
[ImageJavascriptMemory]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png "Figure 2: activer la mémoire JavaScript"  
[ImageSimpleGrowth]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-1-performance-memory.msft.png "Figure 3: croissance simple"  
[ImageTakeHeapSnapshot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png "Figure 4: instantané du tas"  
[ImageFilteringForDetachedNodes]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png "Figure 5: filtrage pour les nœuds détachés"  
[ImageInvestigatingDetachedTree]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png "Figure 6: examen de l’arborescence dissociée"  
[ImageInvestigatingNode]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png "Figure 7: examen d’un nœud"  
[ImageNewAllocations]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png "Figure 8: nouvelles attributions"  
[ImageZoomedAllocationTimeline]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png "Figure 9: chronologie de l’attribution avec zoom"  
[ImageObjectDetail]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png "Figure 10: détails de l’objet"  
[ImageRecordAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png "Figure 11: échantillonnage d’allocation d’enregistrement"  
[ImageAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png "Figure 12: Echantillonnage de l’attribution"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Performance des enregistrements-référence d’analyse des performances"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="e8b7f-270">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8b7f-270">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="e8b7f-271">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).</span><span class="sxs-lookup"><span data-stu-id="e8b7f-271">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="e8b7f-273">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="e8b7f-273">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
