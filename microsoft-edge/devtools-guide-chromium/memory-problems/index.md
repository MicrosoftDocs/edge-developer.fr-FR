---
description: Découvrez comment utiliser Microsoft Edge et DevTools pour rechercher les problèmes de mémoire qui affectent les performances des pages, notamment les fuites de mémoire, les problèmes de mémoire et les collectes fréquentes de la mémoire.
title: Résoudre les problèmes de mémoire
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: afaea8ca561bd975490d9153cda40877786a0f08
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397831"
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

# <a name="fix-memory-problems"></a><span data-ttu-id="9167a-104">Résoudre les problèmes de mémoire</span><span class="sxs-lookup"><span data-stu-id="9167a-104">Fix memory problems</span></span>  

<span data-ttu-id="9167a-105">Découvrez comment utiliser Microsoft Edge et DevTools pour rechercher les problèmes de mémoire qui affectent les performances des pages, notamment les fuites de mémoire, les problèmes de mémoire et les collectes fréquentes de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-105">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <a name="summary"></a><span data-ttu-id="9167a-106">Résumé</span><span class="sxs-lookup"><span data-stu-id="9167a-106">Summary</span></span>  

*   <span data-ttu-id="9167a-107">Découvrez la quantité de mémoire que votre page utilise actuellement avec le Gestionnaire des tâches du navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9167a-107">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="9167a-108">Visualisez l’utilisation de la mémoire au fil du temps avec **le panneau** Mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-108">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="9167a-109">Identifiez les arbre DOM détachés \(une cause courante de fuites de mémoire\) avec une capture instantanée **du tas.**</span><span class="sxs-lookup"><span data-stu-id="9167a-109">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="9167a-110">Découvrez quand une nouvelle mémoire est allouée dans votre tas JavaScript \(tas JS\) avec **l’instrumentation d’allocation sur la chronologie**.</span><span class="sxs-lookup"><span data-stu-id="9167a-110">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <a name="overview"></a><span data-ttu-id="9167a-111">Vue d'ensemble</span><span class="sxs-lookup"><span data-stu-id="9167a-111">Overview</span></span>  

<span data-ttu-id="9167a-112">Dans le modèle de performances **RAIL,** l’objectif de vos efforts en matière de performances doit être vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9167a-112">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="9167a-113">Les problèmes de mémoire sont importants, car ils sont souvent perceptibles par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9167a-113">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="9167a-114">Les utilisateurs peuvent percevoir les problèmes de mémoire des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="9167a-114">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="9167a-115">**Les performances d’une page se dégradent progressivement au fil du temps.**</span><span class="sxs-lookup"><span data-stu-id="9167a-115">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="9167a-116">Il s’agit éventuellement d’un symptôme d’une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-116">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="9167a-117">Une fuite de mémoire se fait lorsqu’un bogue dans la page fait que la page utilise progressivement de plus en plus de mémoire au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9167a-117">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="9167a-118">**Les performances d’une page sont constamment mauvaises.**</span><span class="sxs-lookup"><span data-stu-id="9167a-118">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="9167a-119">Il s’agit peut-être d’un symptôme d’un problème de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-119">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="9167a-120">La mémoire est en trop lorsqu’une page utilise plus de mémoire que nécessaire pour une vitesse de page optimale.</span><span class="sxs-lookup"><span data-stu-id="9167a-120">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="9167a-121">**Les performances d’une page sont retardées ou semblent régulièrement suspendues.**</span><span class="sxs-lookup"><span data-stu-id="9167a-121">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="9167a-122">Il s’agit éventuellement d’un symptôme de fréquents collectes de la garbage.</span><span class="sxs-lookup"><span data-stu-id="9167a-122">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="9167a-123">Le garbage collection est le moment où le navigateur récupère de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-123">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="9167a-124">Le navigateur décide quand cela se produit.</span><span class="sxs-lookup"><span data-stu-id="9167a-124">The browser decides when this happens.</span></span>  <span data-ttu-id="9167a-125">Pendant les collections, tous les scripts en cours d’exécution sont suspendus.</span><span class="sxs-lookup"><span data-stu-id="9167a-125">During collections, all script running is paused.</span></span>  <span data-ttu-id="9167a-126">Ainsi, si le navigateur collecte beaucoup de données de la garbage, le runtime de script sera beaucoup suspendu.</span><span class="sxs-lookup"><span data-stu-id="9167a-126">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <a name="memory-bloat-how-much-is-too-much"></a><span data-ttu-id="9167a-127">La mémoire est trop grande : quelle est la quantité « trop » ?</span><span class="sxs-lookup"><span data-stu-id="9167a-127">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="9167a-128">Une fuite de mémoire est facile à définir.</span><span class="sxs-lookup"><span data-stu-id="9167a-128">A memory leak is easy to define.</span></span>  <span data-ttu-id="9167a-129">Si un site utilise progressivement de plus en plus de mémoire, vous avez une fuite.</span><span class="sxs-lookup"><span data-stu-id="9167a-129">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="9167a-130">Mais la mémoire est un peu plus difficile à épingler.</span><span class="sxs-lookup"><span data-stu-id="9167a-130">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="9167a-131">Qu’est-ce que l’on qualifie d'« utilisation de trop de mémoire » ?</span><span class="sxs-lookup"><span data-stu-id="9167a-131">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="9167a-132">Il n’existe pas de chiffres en dur ici, car différents appareils et navigateurs ont des fonctionnalités différentes.</span><span class="sxs-lookup"><span data-stu-id="9167a-132">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="9167a-133">La même page qui s’exécute correctement sur un smartphone haut de gamme peut se crasher sur un smartphone bas de gamme.</span><span class="sxs-lookup"><span data-stu-id="9167a-133">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="9167a-134">L’essentiel ici est d’utiliser le modèle RAIL et de se concentrer sur vos utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="9167a-134">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="9167a-135">Découvrez quels appareils sont populaires auprès de vos utilisateurs, puis testez votre page sur ces appareils.</span><span class="sxs-lookup"><span data-stu-id="9167a-135">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="9167a-136">Si l’expérience est constamment mauvaise, la page peut dépasser les capacités de mémoire de ces appareils.</span><span class="sxs-lookup"><span data-stu-id="9167a-136">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a><span data-ttu-id="9167a-137">Surveiller l’utilisation de la mémoire en temps réel avec le Gestionnaire des tâches du navigateur Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9167a-137">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="9167a-138">Utilisez le Gestionnaire des tâches du navigateur Microsoft Edge comme point de départ pour l’examen de votre problème de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-138">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="9167a-139">Le Gestionnaire des tâches du navigateur Microsoft Edge est un moniteur en temps réel qui vous indique la quantité de mémoire qu’une page utilise actuellement.</span><span class="sxs-lookup"><span data-stu-id="9167a-139">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="9167a-140">Sélectionnez `Shift` + `Esc` ou accédez au menu  principal de Microsoft Edge,  >   puis sélectionnez Outils de plus pour ouvrir le Gestionnaire des tâches du navigateur Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9167a-140">Select `Shift`+`Esc` or navigate to the Microsoft Edge main menu and choose **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Ouverture du Gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       <span data-ttu-id="9167a-142">Figure 1 : Ouverture du Gestionnaire des tâches du navigateur Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9167a-142">Figure 1:  Opening the Microsoft Edge Browser Task Manager</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="9167a-143">Pointez sur l’en-tête de tableau du Gestionnaire des tâches du navigateur Microsoft Edge, ouvrez le menu contextuel \(clic droit\) et activez la **mémoire JavaScript.**</span><span class="sxs-lookup"><span data-stu-id="9167a-143">Hover on the table header of the Microsoft Edge Browser Task Manager, open the contextual menu \(right-click\), and enable **JavaScript memory**.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Activer la mémoire JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       <span data-ttu-id="9167a-145">Figure 2 : Activer la mémoire JavaScript</span><span class="sxs-lookup"><span data-stu-id="9167a-145">Figure 2:  Enable JavaScript memory</span></span>  
    :::image-end:::  
    
<span data-ttu-id="9167a-146">Ces deux colonnes vous indiquent différentes choses sur la façon dont votre page utilise la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-146">These two columns tell you different things about how your page is using memory.</span></span>  

*   <span data-ttu-id="9167a-147">La **colonne Mémoire** représente la mémoire native.</span><span class="sxs-lookup"><span data-stu-id="9167a-147">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="9167a-148">Les nodes DOM sont stockés dans la mémoire native.</span><span class="sxs-lookup"><span data-stu-id="9167a-148">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="9167a-149">Si cette valeur augmente, des nodes DOM sont créés.</span><span class="sxs-lookup"><span data-stu-id="9167a-149">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="9167a-150">La **colonne Mémoire JavaScript** représente le tas JS.</span><span class="sxs-lookup"><span data-stu-id="9167a-150">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="9167a-151">Cette colonne contient deux valeurs.</span><span class="sxs-lookup"><span data-stu-id="9167a-151">This column contains two values.</span></span>  <span data-ttu-id="9167a-152">La valeur qui vous intéresse est le nombre direct \(le nombre entre parenthèses\).</span><span class="sxs-lookup"><span data-stu-id="9167a-152">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="9167a-153">Le nombre en direct représente la quantité de mémoire que les objets accessibles sur votre page utilisent.</span><span class="sxs-lookup"><span data-stu-id="9167a-153">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="9167a-154">Si ce nombre augmente, soit de nouveaux objets sont créés, soit les objets existants augmentent.</span><span class="sxs-lookup"><span data-stu-id="9167a-154">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a><span data-ttu-id="9167a-155">Visualiser les fuites de mémoire avec le panneau Performances</span><span class="sxs-lookup"><span data-stu-id="9167a-155">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="9167a-156">Vous pouvez également utiliser le panneau Performances comme autre point de départ dans votre enquête.</span><span class="sxs-lookup"><span data-stu-id="9167a-156">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="9167a-157">Le panneau Performances vous permet de visualiser l’utilisation de la mémoire d’une page au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="9167a-157">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="9167a-158">Ouvrez **le panneau Performances** sur DevTools.</span><span class="sxs-lookup"><span data-stu-id="9167a-158">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="9167a-159">Activez la **case à** cocher Mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-159">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="9167a-160">[Effectuer un enregistrement][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="9167a-160">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="9167a-161">Il est pratique de démarrer et de terminer votre enregistrement avec un garbage collection forcé.</span><span class="sxs-lookup"><span data-stu-id="9167a-161">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="9167a-162">Pour forcer le collecte de la garbage collection, **sélectionnez** le bouton de collecte de la garbage ![ force garbage collection lors de ][ImageForceGarbageCollectionIcon] l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="9167a-162">To force garbage collection, choose the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording.</span></span>  

<span data-ttu-id="9167a-163">Pour montrer les enregistrements de mémoire, examinez le code ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="9167a-163">To demonstrate memory recordings, consider the code below:</span></span>  

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

<span data-ttu-id="9167a-164">Chaque fois que le bouton référencé dans le code est choisi, dix milliers de nodes sont appendés au corps du document et une chaîne d’un million de caractères est enfoncée sur le `div` `x` `x` tableau.</span><span class="sxs-lookup"><span data-stu-id="9167a-164">Every time that the button referenced in the code is chosen, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="9167a-165">L’exécution de l’exemple de code précédent produit un enregistrement dans le panneau **Performances** comme illustré ci-après.</span><span class="sxs-lookup"><span data-stu-id="9167a-165">Running the previous code sample produces a recording in the **Performance** panel like the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Croissance simple" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   <span data-ttu-id="9167a-167">Figure 3 : Croissance simple</span><span class="sxs-lookup"><span data-stu-id="9167a-167">Figure 3:  Simple growth</span></span>  
:::image-end:::  

<span data-ttu-id="9167a-168">Tout d’abord, une explication de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9167a-168">First, an explanation of the user interface.</span></span>  <span data-ttu-id="9167a-169">Le **graphique HEAP** dans le **volet** Vue d’ensemble \(en dessous de **NET**\) représente le tas JS.</span><span class="sxs-lookup"><span data-stu-id="9167a-169">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="9167a-170">Sous le volet Vue **d’ensemble** se trouve **le** volet Compteur.</span><span class="sxs-lookup"><span data-stu-id="9167a-170">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="9167a-171">L’utilisation de la mémoire est décomposée par  le tas JS \(identique au graphique **HEAP** dans le volet Vue d’ensemble\), les documents, les nodes DOM, les écouteurs et la mémoire GPU.</span><span class="sxs-lookup"><span data-stu-id="9167a-171">The memory usage is broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="9167a-172">Désactiver une case à cocher pour la masquer dans le graphique.</span><span class="sxs-lookup"><span data-stu-id="9167a-172">Turn off a checkbox to hide it from the graph.</span></span>  

<span data-ttu-id="9167a-173">À présent, une analyse du code est comparée à la figure précédente.</span><span class="sxs-lookup"><span data-stu-id="9167a-173">Now, an analysis of the code compared with the previous figure.</span></span>  <span data-ttu-id="9167a-174">Si vous examinez le compteur de nœuds \(le graphique vert\), il correspond correctement au code.</span><span class="sxs-lookup"><span data-stu-id="9167a-174">If you review the node counter \(the green graph\), it matches up cleanly with the code.</span></span>  <span data-ttu-id="9167a-175">Le nombre de nœuds augmente en étapes discrètes.</span><span class="sxs-lookup"><span data-stu-id="9167a-175">The node count increases in discrete steps.</span></span>  <span data-ttu-id="9167a-176">Vous pouvez supposer que chaque augmentation du nombre de nœuds est un appel à `grow()` .</span><span class="sxs-lookup"><span data-stu-id="9167a-176">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="9167a-177">Le graphique de tas JS \(le graphique bleu\) n’est pas aussi simple.</span><span class="sxs-lookup"><span data-stu-id="9167a-177">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="9167a-178">En respectant les meilleures pratiques, le premier dip est  en fait un garbage collection forcé \(choisissez le bouton de collecte du garbage ![ force garbage ][ImageForceGarbageCollectionIcon] collection\).</span><span class="sxs-lookup"><span data-stu-id="9167a-178">In keeping with best practices, the first dip is actually a forced garbage collection \(choose the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="9167a-179">Au fur et à mesure de la progression de l’enregistrement, les pics de taille du tas JS s’affichent.</span><span class="sxs-lookup"><span data-stu-id="9167a-179">As the recording progresses, the JS heap size spikes are displayed.</span></span>  <span data-ttu-id="9167a-180">Ceci est naturel et attendu : le code JavaScript crée les nodes DOM sur chaque bouton de votre choix et fait beaucoup de travail lorsqu’il crée la chaîne d’un million de caractères.</span><span class="sxs-lookup"><span data-stu-id="9167a-180">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button you choose and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="9167a-181">L’élément clé ici est le fait que le tas JS se termine plus haut qu’il n’a commencé \(le « début » ici étant le point après le garbage collection forcé\).</span><span class="sxs-lookup"><span data-stu-id="9167a-181">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="9167a-182">Dans le monde réel, si vous avez vu ce modèle d’augmentation de la taille du tas ou de la taille du nœud JS, il peut éventuellement définir une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-182">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a><span data-ttu-id="9167a-183">Découvrir les fuites de mémoire d’arborescence DOM détachée avec des instantanés de tas</span><span class="sxs-lookup"><span data-stu-id="9167a-183">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="9167a-184">Un nœud DOM est uniquement la garbage collecté lorsqu’il n’y a aucune référence au nœud à partir de l’arborescence DOM ou du code JavaScript en cours d’exécution sur la page.</span><span class="sxs-lookup"><span data-stu-id="9167a-184">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="9167a-185">Un nœud est dit « détaché » lorsqu’il est supprimé de l’arborescence DOM, mais certains javaScript le référencent toujours.</span><span class="sxs-lookup"><span data-stu-id="9167a-185">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="9167a-186">Les nodes DOM détachées sont une cause courante de fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-186">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="9167a-187">Cette section vous apprend à utiliser les profileurs de tas dans DevTools pour identifier les nodes détachées.</span><span class="sxs-lookup"><span data-stu-id="9167a-187">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="9167a-188">Voici un exemple simple de nodes DOM détachées.</span><span class="sxs-lookup"><span data-stu-id="9167a-188">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="9167a-189">Le choix du bouton référencé dans le code crée `ul` un nœud avec dix `li` enfants.</span><span class="sxs-lookup"><span data-stu-id="9167a-189">Choosing the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="9167a-190">Les nodes sont référencés par le code, mais n’existent pas dans l’arborescence DOM, de sorte que chacun d’eux est détaché.</span><span class="sxs-lookup"><span data-stu-id="9167a-190">The nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="9167a-191">Les captures instantanées de tas sont un moyen d’identifier les nodes détachées.</span><span class="sxs-lookup"><span data-stu-id="9167a-191">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="9167a-192">Comme son nom l’indique, les captures instantanées de tas vous montrent comment la mémoire est distribuée entre les objets JS et les nodes DOM de votre page au moment de la capture instantanée.</span><span class="sxs-lookup"><span data-stu-id="9167a-192">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="9167a-193">Pour créer une capture instantanée, ouvrez DevTools et accédez au panneau Mémoire, choisissez la bouton **d’radio** de capture instantanée de tas > bouton Prendre **une** capture instantanée. </span><span class="sxs-lookup"><span data-stu-id="9167a-193">To create a snapshot, open DevTools and navigate to the **Memory** panel, choose the **Heap snapshot** radio button > **Take snapshot** button.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Prendre une capture instantanée de tas" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   <span data-ttu-id="9167a-195">Figure 4 : Prendre une capture instantanée de tas</span><span class="sxs-lookup"><span data-stu-id="9167a-195">Figure 4:  Take heap snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="9167a-196">Le traitement et le chargement de la capture instantanée peuvent prendre un certain temps.</span><span class="sxs-lookup"><span data-stu-id="9167a-196">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="9167a-197">Une fois terminé, sélectionnez-le dans le panneau de gauche \(nommé **SNAPSHOTS TAS**\).</span><span class="sxs-lookup"><span data-stu-id="9167a-197">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="9167a-198">Tapez `Detached` dans la zone de texte **Filtre** classe pour rechercher des arbre DOM détachés.</span><span class="sxs-lookup"><span data-stu-id="9167a-198">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtrage des nodes détachées" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   <span data-ttu-id="9167a-200">Figure 5 : Filtrage des nodes détachées</span><span class="sxs-lookup"><span data-stu-id="9167a-200">Figure 5:  Filtering for detached nodes</span></span>  
:::image-end:::  

<span data-ttu-id="9167a-201">Développez les carats pour examiner une arborescence détachée.</span><span class="sxs-lookup"><span data-stu-id="9167a-201">Expand the carats to investigate a detached tree.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Étude de l’arborescence détachée" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   <span data-ttu-id="9167a-203">Figure 6 : Étude de l’arborescence détachée</span><span class="sxs-lookup"><span data-stu-id="9167a-203">Figure 6:  Investigating detached tree</span></span>  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="9167a-204">Choisissez un nœud pour l’examiner plus en détail.</span><span class="sxs-lookup"><span data-stu-id="9167a-204">Choose a node to investigate it further.</span></span>  <span data-ttu-id="9167a-205">Dans le **volet Objets,** vous pouvez consulter plus d’informations sur le code qui le référence.</span><span class="sxs-lookup"><span data-stu-id="9167a-205">In the **Objects** pane, you may review more information about the code that is referencing it.</span></span>  <span data-ttu-id="9167a-206">Par exemple, dans la figure suivante, la `detachedNodes` variable fait référence au nœud.</span><span class="sxs-lookup"><span data-stu-id="9167a-206">For example, in the following figure, the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="9167a-207">Pour corriger la fuite de mémoire particulière, vous devez étudier le code qui utilise la variable et vous assurer que la référence au nœud est supprimée lorsqu’elle `detachedUNode` n’est plus nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9167a-207">To fix the particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Investigation d’un nœud" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   <span data-ttu-id="9167a-209">Figure 7 : Investigation d’un nœud</span><span class="sxs-lookup"><span data-stu-id="9167a-209">Figure 7:  Investigating a node</span></span>  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a><span data-ttu-id="9167a-210">Identifier les fuites de mémoire de tas JS avec l’instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="9167a-210">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="9167a-211">**L’instrumentation d’allocation** sur la chronologie est un autre outil qui peut vous aider à suivre les fuites de mémoire dans votre tas JS.</span><span class="sxs-lookup"><span data-stu-id="9167a-211">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="9167a-212">Démontrez **l’instrumentation de l’allocation sur la chronologie**  à l’aide du code suivant.</span><span class="sxs-lookup"><span data-stu-id="9167a-212">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="9167a-213">Chaque fois que le bouton référencé dans le code est enfoncé, une chaîne d’un million de caractères est ajoutée au `x` tableau.</span><span class="sxs-lookup"><span data-stu-id="9167a-213">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="9167a-214">Pour enregistrer une instrumentation d’allocation sur la chronologie,  ouvrez DevTools, accédez  au panneau Mémoire, choisissez l’instrumentation  **d’allocation** sur la bouton d’radio de chronologie, choisissez le bouton Démarrer, effectuez l’action que vous pensez être à l’origine de la fuite de mémoire, puis choisissez le bouton Arrêter l’enregistrement du profil de tas lorsque vous avez ![ ][ImageStopRecordingIcon] terminé.</span><span class="sxs-lookup"><span data-stu-id="9167a-214">To record an Allocation instrumentation on timeline, open DevTools, navigate to the **Memory** panel, choose the **Allocation instrumentation on timeline** radio button, choose the **Start** button, perform the action that you suspect is causing the memory leak, and then choose the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="9167a-215">Lors de l’enregistrement, notez si des barres bleues s’afficheront sur l’instrumentation d’allocation sur la chronologie, comme dans la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="9167a-215">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in the following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Nouvelles allocations" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   <span data-ttu-id="9167a-217">Figure 8 : Nouvelles allocations</span><span class="sxs-lookup"><span data-stu-id="9167a-217">Figure 8:  New allocations</span></span>  
:::image-end:::  

<span data-ttu-id="9167a-218">Ces barres bleues représentent de nouvelles allocations de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-218">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="9167a-219">Ces nouvelles allocations de mémoire sont vos candidats aux fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-219">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="9167a-220">Vous pouvez effectuer un zoom sur  une barre pour filtrer le volet Constructeur afin d’afficher uniquement les objets qui ont été alloués pendant la période spécifiée.</span><span class="sxs-lookup"><span data-stu-id="9167a-220">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Chronologie d’allocation avec zoom avant" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   <span data-ttu-id="9167a-222">Figure 9 : Chronologie d’allocation avec zoom avant</span><span class="sxs-lookup"><span data-stu-id="9167a-222">Figure 9:  Zoomed allocation timeline</span></span>  
:::image-end:::  

<span data-ttu-id="9167a-223">Développez l’objet et sélectionnez la valeur pour afficher plus de détails dans le **volet** Objet.</span><span class="sxs-lookup"><span data-stu-id="9167a-223">Expand the object and select the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="9167a-224">Par exemple, dans la figure suivante, les détails de l’objet nouvellement alloué indiquent qu’il a été alloué à la `x` variable dans `Window` l’étendue.</span><span class="sxs-lookup"><span data-stu-id="9167a-224">For example, in the following figure, in the details of the newly allocated object indicates that it was allocated to the `x` variable in the `Window` scope.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Détails de l’objet" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   <span data-ttu-id="9167a-226">Figure 10 : Détails de l’objet</span><span class="sxs-lookup"><span data-stu-id="9167a-226">Figure 10:  Object details</span></span>  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a><span data-ttu-id="9167a-227">Examiner l’allocation de mémoire par fonction</span><span class="sxs-lookup"><span data-stu-id="9167a-227">Investigate memory allocation by function</span></span>  

<span data-ttu-id="9167a-228">Utilisez le type de profilage **d’échantillonnage** d’allocation pour afficher l’allocation de mémoire par fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9167a-228">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Échantillonnage de l’allocation d’enregistrement" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   <span data-ttu-id="9167a-230">Figure 11 : Échantillonnage de l’allocation d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="9167a-230">Figure 11:  Record Allocation sampling</span></span>  
:::image-end:::  

1.  <span data-ttu-id="9167a-231">Choisissez la **radio d’échantillonnage** d’allocation.</span><span class="sxs-lookup"><span data-stu-id="9167a-231">Choose the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="9167a-232">S’il existe un travail sur la page, vous pouvez le sélectionner comme cible de profilage à l’aide du menu déroulant en face du **bouton** Démarrer.</span><span class="sxs-lookup"><span data-stu-id="9167a-232">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="9167a-233">Sélectionnez **le bouton** Démarrer.</span><span class="sxs-lookup"><span data-stu-id="9167a-233">Choose the **Start** button.</span></span>  
1.  <span data-ttu-id="9167a-234">Effectuer les actions sur la page web que vous souhaitez examiner.</span><span class="sxs-lookup"><span data-stu-id="9167a-234">Complete the actions on the webpage which you want to investigate.</span></span>  
1.  <span data-ttu-id="9167a-235">Choisissez le **bouton Arrêter** lorsque vous avez terminé toutes vos actions.</span><span class="sxs-lookup"><span data-stu-id="9167a-235">Choose the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="9167a-236">DevTools vous présente une répartition de l’allocation de mémoire par fonction.</span><span class="sxs-lookup"><span data-stu-id="9167a-236">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="9167a-237">L’affichage par défaut **est Épais (bas vers**le haut), qui affiche les fonctions qui ont alloué le plus de mémoire en haut.</span><span class="sxs-lookup"><span data-stu-id="9167a-237">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Échantillonnage d’allocation" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   <span data-ttu-id="9167a-239">Figure 12 : Échantillonnage des allocations</span><span class="sxs-lookup"><span data-stu-id="9167a-239">Figure 12:  Allocation sampling</span></span>  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a><span data-ttu-id="9167a-240">Repérer les garbage collections fréquentes</span><span class="sxs-lookup"><span data-stu-id="9167a-240">Spot frequent garbage collections</span></span>  

<span data-ttu-id="9167a-241">Si votre page s’interrompt fréquemment, vous risquez de ne pas avoir de problèmes de collecte de la garbage.</span><span class="sxs-lookup"><span data-stu-id="9167a-241">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="9167a-242">Vous pouvez utiliser le Gestionnaire des tâches du navigateur Microsoft Edge ou les enregistrements de mémoire des performances pour repérer les tâches fréquentes de collecte de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-242">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="9167a-243">Dans le Gestionnaire des tâches du  navigateur Microsoft Edge, les valeurs mémoire en mémoire ou mémoire **JavaScript** qui tombent fréquemment représentent un collecte fréquent de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-243">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="9167a-244">Dans les enregistrements de performances, les modifications fréquentes \(déplacement et baisse\) du tas JS ou du nombre de nœuds indiquent un collecte fréquent de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="9167a-244">In Performance recordings, frequent changes \(rising and falling\) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="9167a-245">Une fois que vous avez identifié le problème, vous pouvez utiliser une **instrumentation d’allocation** sur l’enregistrement chronologique pour savoir où la mémoire est allouée et quelles fonctions sont à l’origine des allocations.</span><span class="sxs-lookup"><span data-stu-id="9167a-245">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="9167a-246">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="9167a-246">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Performances d’enregistrement : référence de l’analyse des performances"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="9167a-248">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9167a-248">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9167a-249">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="9167a-249">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="9167a-251">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9167a-251">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
