---
description: Découvrez comment enregistrer des captures instantanées de tas avec le profileur de tas Microsoft Edge DevTools et rechercher des fuites de mémoire.
title: Comment enregistrer des captures instantanées de tas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ce7a6f972bed386f96312808428bd74f1241668f
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397803"
---
<!-- Copyright Meggin Kearney 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="how-to-record-heap-snapshots"></a><span data-ttu-id="bf354-104">Comment enregistrer des captures instantanées de tas</span><span class="sxs-lookup"><span data-stu-id="bf354-104">How to record heap snapshots</span></span>  

<span data-ttu-id="bf354-105">Découvrez comment enregistrer des captures instantanées de tas avec le profileur de tas Microsoft Edge DevTools et rechercher des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf354-105">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="bf354-106">Le profileur de tas Microsoft Edge DevTools affiche la distribution de mémoire par les objets JavaScript et les nodes DOM associés de votre page.</span><span class="sxs-lookup"><span data-stu-id="bf354-106">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="bf354-107">Utilisez-le pour prendre des instantanés de tas JavaScript \(tas JS\), analyser des graphiques de mémoire, comparer des captures instantanées et rechercher des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf354-107">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="bf354-108">Accédez à [Objets conservant l’arborescence][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="bf354-108">Navigate to [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <a name="take-a-snapshot"></a><span data-ttu-id="bf354-109">Prendre une capture instantanée</span><span class="sxs-lookup"><span data-stu-id="bf354-109">Take a snapshot</span></span>  

<span data-ttu-id="bf354-110">On the **Memory** panel, choose **Take snapshot,** then choose **Start**.</span><span class="sxs-lookup"><span data-stu-id="bf354-110">On the **Memory** panel, choose **Take snapshot**, then choose **Start**.</span></span>  <span data-ttu-id="bf354-111">Vous pouvez également sélectionner `Ctrl` + `E` \(Windows, Linux\) ou `Cmd` + `E` \(macOS\).</span><span class="sxs-lookup"><span data-stu-id="bf354-111">You may also select `Ctrl`+`E` \(Windows, Linux\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Choisir le type de profilage" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="bf354-113">Choisir le type de profilage</span><span class="sxs-lookup"><span data-stu-id="bf354-113">Choose profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="bf354-114">**Les captures instantanées** sont initialement stockées dans la mémoire du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="bf354-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="bf354-115">Les captures instantanées sont transférées vers DevTools à la demande, lorsque vous choisissez sur l’icône de capture instantanée pour l’afficher.</span><span class="sxs-lookup"><span data-stu-id="bf354-115">Snapshots are transferred to the DevTools on demand, when you choose on the snapshot icon to view it.</span></span>  

<span data-ttu-id="bf354-116">Une fois que la capture instantanée a été chargée dans DevTools et qu’elle a été l’objet d’une recherche, le nombre en dessous du titre de la capture instantanée apparaît et indique la taille totale des objets [JavaScript accessibles.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="bf354-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Taille totale des objets accessibles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="bf354-118">Taille totale des objets accessibles</span><span class="sxs-lookup"><span data-stu-id="bf354-118">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="bf354-119">Seuls les objets accessibles sont inclus dans les captures instantanées.</span><span class="sxs-lookup"><span data-stu-id="bf354-119">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="bf354-120">En outre, la prise d’un instantané commence toujours par un garbage collection.</span><span class="sxs-lookup"><span data-stu-id="bf354-120">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <a name="clear-snapshots"></a><span data-ttu-id="bf354-121">Effacer des captures instantanées</span><span class="sxs-lookup"><span data-stu-id="bf354-121">Clear snapshots</span></span>  

<span data-ttu-id="bf354-122">Sélectionnez **Effacer l’icône** De tous les profils pour supprimer les captures instantanées \(à la fois de DevTools et de toute mémoire associée au processus de rendu\).</span><span class="sxs-lookup"><span data-stu-id="bf354-122">Choose **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Supprimer des captures instantanées" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="bf354-124">Supprimer des captures instantanées</span><span class="sxs-lookup"><span data-stu-id="bf354-124">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="bf354-125">La fermeture de la fenêtre DevTools ne supprime pas les profils de la mémoire associée au processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="bf354-125">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="bf354-126">Lors de la réouverture de DevTools, toutes les captures instantanées précédemment prises réapparaissent dans la liste des captures instantanées.</span><span class="sxs-lookup"><span data-stu-id="bf354-126">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="bf354-127">Essayez cet exemple d’objets [en nuages de points et][GlitchDevtoolsMemoryExample03] profilez-le à l’aide du Profileur de tas.</span><span class="sxs-lookup"><span data-stu-id="bf354-127">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="bf354-128">Un certain nombre d’allocations d’éléments \(object\) sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bf354-128">A number of \(object\) item allocations are displayed.</span></span>  

## <a name="view-snapshots"></a><span data-ttu-id="bf354-129">Afficher des captures instantanées</span><span class="sxs-lookup"><span data-stu-id="bf354-129">View snapshots</span></span>  

<span data-ttu-id="bf354-130">Afficher des captures instantanées sous différentes perspectives pour différentes tâches.</span><span class="sxs-lookup"><span data-stu-id="bf354-130">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="bf354-131">**L’affichage résumé** montre les objets regroupés par nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="bf354-131">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="bf354-132">Utilisez-le pour trouver les objets \(et l’utilisation de la mémoire\) en fonction du type groupé par nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="bf354-132">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="bf354-133">Il est particulièrement utile pour **le suivi des fuites DOM**.</span><span class="sxs-lookup"><span data-stu-id="bf354-133">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="bf354-134">**Vue de comparaison**.</span><span class="sxs-lookup"><span data-stu-id="bf354-134">**Comparison view**.</span></span>  <span data-ttu-id="bf354-135">Affiche la différence entre deux captures instantanées.</span><span class="sxs-lookup"><span data-stu-id="bf354-135">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="bf354-136">Utilisez-le pour comparer deux captures instantanées de mémoire \(ou plus\) avant et après une opération.</span><span class="sxs-lookup"><span data-stu-id="bf354-136">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="bf354-137">L’inspection du delta dans la mémoire libérée et le nombre de références vous permet de confirmer la présence et la cause d’une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf354-137">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="bf354-138">**Affichage d’endiguement**.</span><span class="sxs-lookup"><span data-stu-id="bf354-138">**Containment view**.</span></span>  <span data-ttu-id="bf354-139">Permet d’explorer le contenu du tas.</span><span class="sxs-lookup"><span data-stu-id="bf354-139">Allows exploration of heap contents.</span></span>  <span data-ttu-id="bf354-140">**La vue d’identisation** fournit une meilleure vue de la structure des objets, ce qui permet d’analyser les objets référencés dans l’espace de noms global \(window\) pour savoir ce qui permet de conserver les objets.</span><span class="sxs-lookup"><span data-stu-id="bf354-140">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="bf354-141">Utilisez-le pour analyser les fermetures et vous plonger dans vos objets à un niveau faible.</span><span class="sxs-lookup"><span data-stu-id="bf354-141">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="bf354-142">Pour basculer entre les vues, utilisez le sélecteur en haut de l’affichage.</span><span class="sxs-lookup"><span data-stu-id="bf354-142">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Sélecteur d’affichages de commutateur" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="bf354-144">Sélecteur d’affichages de commutateur</span><span class="sxs-lookup"><span data-stu-id="bf354-144">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="bf354-145">Toutes les propriétés ne sont pas stockées sur le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf354-145">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="bf354-146">Les propriétés implémentées à l’aide de getters qui exécutent du code natif ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="bf354-146">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="bf354-147">En outre, les valeurs autres que des chaînes, telles que les nombres, ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="bf354-147">Also, non-string values such as numbers are not captured.</span></span>  

### <a name="summary-view"></a><span data-ttu-id="bf354-148">Affichage récapitulatif</span><span class="sxs-lookup"><span data-stu-id="bf354-148">Summary view</span></span>  

<span data-ttu-id="bf354-149">Initialement, une capture instantanée s’ouvre dans l’affichage Résumé, affichant les totaux des objets, qui peuvent être étendus pour afficher les instances :</span><span class="sxs-lookup"><span data-stu-id="bf354-149">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Affichage récapitulatif" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="bf354-151">**Affichage récapitulatif**</span><span class="sxs-lookup"><span data-stu-id="bf354-151">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="bf354-152">Les entrées de niveau supérieur sont des lignes « total ».</span><span class="sxs-lookup"><span data-stu-id="bf354-152">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="bf354-153">Entrées de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="bf354-153">Top-level entries</span></span> | <span data-ttu-id="bf354-154">Description</span><span class="sxs-lookup"><span data-stu-id="bf354-154">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bf354-155">Constructeur</span><span class="sxs-lookup"><span data-stu-id="bf354-155">Constructor</span></span>** | <span data-ttu-id="bf354-156">Représente tous les objets créés à l’aide de ce constructeur.</span><span class="sxs-lookup"><span data-stu-id="bf354-156">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="bf354-157">Distance</span><span class="sxs-lookup"><span data-stu-id="bf354-157">Distance</span></span>** | <span data-ttu-id="bf354-158">affiche la distance d’accès à la racine à l’aide du chemin d’accès simple des nodes le plus court.</span><span class="sxs-lookup"><span data-stu-id="bf354-158">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="bf354-159">Taille superficiele</span><span class="sxs-lookup"><span data-stu-id="bf354-159">Shallow size</span></span>** | <span data-ttu-id="bf354-160">Affiche la somme des tailles superficiels de tous les objets créés par une fonction de constructeur.</span><span class="sxs-lookup"><span data-stu-id="bf354-160">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="bf354-161">La taille peu profonde est la taille de la mémoire détenue par un objet \(généralement, les tableaux et les chaînes ont des tailles peu profondes plus grandes\).</span><span class="sxs-lookup"><span data-stu-id="bf354-161">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="bf354-162">Accédez à [tailles d’objet.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="bf354-162">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="bf354-163">Taille conservée</span><span class="sxs-lookup"><span data-stu-id="bf354-163">Retained size</span></span>** | <span data-ttu-id="bf354-164">Affiche la taille maximale conservée parmi le même ensemble d’objets.</span><span class="sxs-lookup"><span data-stu-id="bf354-164">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="bf354-165">La taille de la mémoire que vous pouvez libérer après la suppression d’un objet \(et que les dépendants ne sont plus accessibles\) est appelée taille conservée.</span><span class="sxs-lookup"><span data-stu-id="bf354-165">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="bf354-166">Accédez à [tailles d’objet.][DevtoolsMemoryProblems101ObjectSizes]</span><span class="sxs-lookup"><span data-stu-id="bf354-166">Navigate to [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="bf354-167">Après avoir développé une ligne de total dans l’affichage supérieur, toutes les instances sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bf354-167">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="bf354-168">Pour chaque instance, les tailles peu profondes et conservées sont affichées dans les colonnes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="bf354-168">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="bf354-169">Le nombre après le caractère est l’ID unique de l’objet, ce qui vous permet de comparer des instantanés de tas `@` par objet.</span><span class="sxs-lookup"><span data-stu-id="bf354-169">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="bf354-170">N’oubliez pas que les objets jaunes ont des références JavaScript et que les objets rouges sont des nodes détachées qui sont référencés à partir d’un seul avec un arrière-plan jaune.</span><span class="sxs-lookup"><span data-stu-id="bf354-170">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="bf354-171">À quoi correspondent les différentes entrées constructor \(group\) dans le profileur heap ?</span><span class="sxs-lookup"><span data-stu-id="bf354-171">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Groupes de constructeurs" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="bf354-173">**Groupes de constructeurs**</span><span class="sxs-lookup"><span data-stu-id="bf354-173">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="bf354-174">Constructor \(group\) entry</span><span class="sxs-lookup"><span data-stu-id="bf354-174">Constructor \(group\) entry</span></span> | <span data-ttu-id="bf354-175">Description</span><span class="sxs-lookup"><span data-stu-id="bf354-175">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bf354-176">\(global, propriété\)</span><span class="sxs-lookup"><span data-stu-id="bf354-176">\(global property\)</span></span>** | <span data-ttu-id="bf354-177">Objets intermédiaires entre un objet global \(like \) et un `window` objet référencé par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="bf354-177">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="bf354-178">Si un objet est créé à l’aide d’un constructeur et qu’il est conservé par un objet global, le chemin de rétention peut `Person` être représenté par `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="bf354-178">If an object is created using a constructor `Person` and is held by a global object, the retaining path may be represented as `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="bf354-179">Cela contraste avec la norme, où les objets se référencent directement les uns les autres.</span><span class="sxs-lookup"><span data-stu-id="bf354-179">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="bf354-180">Des objets intermédiaires existent pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="bf354-180">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="bf354-181">Les globales sont modifiées régulièrement et les optimisations de l’accès aux propriétés s’appliquent bien aux objets non globaux qui ne s’appliquent pas aux objets globaux.</span><span class="sxs-lookup"><span data-stu-id="bf354-181">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="bf354-182">\(racines\)</span><span class="sxs-lookup"><span data-stu-id="bf354-182">\(roots\)</span></span>** | <span data-ttu-id="bf354-183">Les entrées racine dans l’arborescence de rétention sont les entités qui ont des références à l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="bf354-183">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="bf354-184">Les entrées peuvent également être des références créées par le moteur à des fins spécifiques au moteur.</span><span class="sxs-lookup"><span data-stu-id="bf354-184">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="bf354-185">Le moteur possède des caches qui référencent des objets, mais toutes ces références sont faibles et n’empêchent pas la collecte d’un objet, étant donné qu’il n’existe aucune référence vraiment forte.</span><span class="sxs-lookup"><span data-stu-id="bf354-185">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="bf354-186">\(fermeture\)</span><span class="sxs-lookup"><span data-stu-id="bf354-186">\(closure\)</span></span>** | <span data-ttu-id="bf354-187">Nombre de références à un groupe d’objets par le biais de fermetures de fonctions.</span><span class="sxs-lookup"><span data-stu-id="bf354-187">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="bf354-188">\(array, string, number, regexp\)</span><span class="sxs-lookup"><span data-stu-id="bf354-188">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="bf354-189">Liste des types d’objets avec des propriétés qui font référence à une expression array, string, number ou régulière.</span><span class="sxs-lookup"><span data-stu-id="bf354-189">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="bf354-190">\(code compilé\)</span><span class="sxs-lookup"><span data-stu-id="bf354-190">\(compiled code\)</span></span>** | <span data-ttu-id="bf354-191">Tout ce qui est lié au code compilé.</span><span class="sxs-lookup"><span data-stu-id="bf354-191">Everything related to compiled code.</span></span>  <span data-ttu-id="bf354-192">Le script est similaire à une fonction, mais correspond à un `<script>` corps.</span><span class="sxs-lookup"><span data-stu-id="bf354-192">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="bf354-193">SharedFunctionInfos \(SFI\) sont des objets se tenant entre les fonctions et le code compilé.</span><span class="sxs-lookup"><span data-stu-id="bf354-193">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="bf354-194">Les fonctions ont généralement un contexte, alors que les SFI ne le font pas.</span><span class="sxs-lookup"><span data-stu-id="bf354-194">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="bf354-195">**HTMLDivElement,** **HTMLAnchorElement,** **DocumentFragment,** etc.</span><span class="sxs-lookup"><span data-stu-id="bf354-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="bf354-196">Références à des éléments ou des objets de document d’un type particulier référencé par votre code.</span><span class="sxs-lookup"><span data-stu-id="bf354-196">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a><span data-ttu-id="bf354-197">Vue de comparaison</span><span class="sxs-lookup"><span data-stu-id="bf354-197">Comparison view</span></span>  

<span data-ttu-id="bf354-198">Recherchez les objets divulgués en comparant plusieurs captures instantanées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="bf354-198">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="bf354-199">Pour vérifier qu’une certaine opération d’application ne crée pas de fuites \(par exemple, une paire d’opérations directes et inversées, comme l’ouverture d’un document, puis sa fermeture, ne doit pas laisser de mémoire\), vous pouvez suivre le scénario ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="bf354-199">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="bf354-200">Prenez une capture instantanée de tas avant d’effectuer une opération.</span><span class="sxs-lookup"><span data-stu-id="bf354-200">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="bf354-201">Effectuez une opération \(interagissez avec une page d’une manière que vous pensez être à l’origine d’une fuite\).</span><span class="sxs-lookup"><span data-stu-id="bf354-201">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="bf354-202">Effectuez une opération inverse \(effectuez l’interaction opposée et répétez-la plusieurs fois\).</span><span class="sxs-lookup"><span data-stu-id="bf354-202">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="bf354-203">Prenez une deuxième capture instantanée de tas  et modifiez l’affichage de celui-ci en comparaison avec la capture **instantanée 1.**</span><span class="sxs-lookup"><span data-stu-id="bf354-203">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="bf354-204">Dans **l’affichage** Comparaison, la différence entre deux captures instantanées s’affiche.</span><span class="sxs-lookup"><span data-stu-id="bf354-204">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="bf354-205">Lors de l’extension d’une entrée totale, les instances d’objet ajoutées et supprimées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="bf354-205">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vue de comparaison" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="bf354-207">**Vue de** comparaison</span><span class="sxs-lookup"><span data-stu-id="bf354-207">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a><span data-ttu-id="bf354-208">Affichage d’endiguement</span><span class="sxs-lookup"><span data-stu-id="bf354-208">Containment view</span></span>  

<span data-ttu-id="bf354-209">La **vue Containment** est essentiellement une « vue d’œil d’enfant » de la structure des objets de votre application.</span><span class="sxs-lookup"><span data-stu-id="bf354-209">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="bf354-210">Il vous permet de regarder dans les fermetures de fonction, d’observer les objets internes de la machine virtuelle \(VM\) qui, ensemble, forment vos objets JavaScript et de comprendre la quantité de mémoire que votre application utilise à un niveau très faible.</span><span class="sxs-lookup"><span data-stu-id="bf354-210">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="bf354-211">Points d’entrée d’affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="bf354-211">Containment view entry points</span></span> | <span data-ttu-id="bf354-212">Description</span><span class="sxs-lookup"><span data-stu-id="bf354-212">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bf354-213">Objets DOMWindow</span><span class="sxs-lookup"><span data-stu-id="bf354-213">DOMWindow objects</span></span>** | <span data-ttu-id="bf354-214">Objets globaux pour le code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf354-214">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="bf354-215">Racines GC</span><span class="sxs-lookup"><span data-stu-id="bf354-215">GC roots</span></span>** | <span data-ttu-id="bf354-216">Racines GC réelles utilisées par la garbage de la VM.</span><span class="sxs-lookup"><span data-stu-id="bf354-216">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="bf354-217">Les racines GC sont composées de cartes d’objets intégrées, de tableaux de symboles, de piles de threads de vm, de caches de compilation, d’étendues de handle et de handles globaux.</span><span class="sxs-lookup"><span data-stu-id="bf354-217">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="bf354-218">Objets natifs</span><span class="sxs-lookup"><span data-stu-id="bf354-218">Native objects</span></span>** | <span data-ttu-id="bf354-219">Objets de navigateur « pushed » à l’intérieur de la machine virtuelle JavaScript \(JavaScript VM\) pour autoriser l’automatisation, par exemple, les nodes DOM, les règles CSS.</span><span class="sxs-lookup"><span data-stu-id="bf354-219">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Affichage d’endiguement" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="bf354-221">**Affichage d’endiguement**</span><span class="sxs-lookup"><span data-stu-id="bf354-221">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="bf354-222">Conseil sur les fermetures.</span><span class="sxs-lookup"><span data-stu-id="bf354-222">A tip about closures.</span></span>  <span data-ttu-id="bf354-223">Nommez les fonctions afin de pouvoir facilement faire la distinction entre les fermetures dans la capture instantanée.</span><span class="sxs-lookup"><span data-stu-id="bf354-223">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="bf354-224">Par exemple, cet exemple n’utilise pas de fonctions nommées.</span><span class="sxs-lookup"><span data-stu-id="bf354-224">For example, this example does not use named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <span data-ttu-id="bf354-225">L’extrait de code suivant utilise des fonctions nommées.</span><span class="sxs-lookup"><span data-stu-id="bf354-225">The followingcode snippet uses named functions.</span></span>  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="bf354-226">Essayez cet exemple de la raison [pour laquelle il est `eval` important][GlitchDevtoolsMemoryExample07] d’analyser l’impact des fermetures sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="bf354-226">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="bf354-227">Vous pouvez également être intéressé par le suivi avec cet exemple qui vous permet d’enregistrer les [allocations de tas][GlitchDevtoolsMemoryExample08].</span><span class="sxs-lookup"><span data-stu-id="bf354-227">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <a name="look-up-color-coding"></a><span data-ttu-id="bf354-228">Rechercher le codage des couleurs</span><span class="sxs-lookup"><span data-stu-id="bf354-228">Look up color coding</span></span>  

<span data-ttu-id="bf354-229">Les propriétés et les valeurs de propriétés des objets ont différents types et sont colorées en conséquence.</span><span class="sxs-lookup"><span data-stu-id="bf354-229">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="bf354-230">Chaque propriété possède l’un des quatre types.</span><span class="sxs-lookup"><span data-stu-id="bf354-230">Each property has one of four types.</span></span>  

| <span data-ttu-id="bf354-231">Type de propriété</span><span class="sxs-lookup"><span data-stu-id="bf354-231">Property Type</span></span> | <span data-ttu-id="bf354-232">Description</span><span class="sxs-lookup"><span data-stu-id="bf354-232">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="bf354-233">a: property</span><span class="sxs-lookup"><span data-stu-id="bf354-233">a: property</span></span>** | <span data-ttu-id="bf354-234">Une propriété normale avec un nom, accessible via l’opérateur `.` \(dot\) ou via `[` `]` la notation \(brackets\), par exemple `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="bf354-234">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="bf354-235">0 : élément</span><span class="sxs-lookup"><span data-stu-id="bf354-235">0: element</span></span>** | <span data-ttu-id="bf354-236">Propriété normale avec un index numérique, accessible via `[` `]` la notation \(brackets\).</span><span class="sxs-lookup"><span data-stu-id="bf354-236">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="bf354-237">a: context var</span><span class="sxs-lookup"><span data-stu-id="bf354-237">a: context var</span></span>** |  <span data-ttu-id="bf354-238">Variable dans un contexte de fonction, accessible par le nom de la variable à partir de l’intérieur d’une fermeture de fonction.</span><span class="sxs-lookup"><span data-stu-id="bf354-238">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="bf354-239">a: system prop</span><span class="sxs-lookup"><span data-stu-id="bf354-239">a: system prop</span></span>** | <span data-ttu-id="bf354-240">Propriété ajoutée par la VM JavaScript, non accessible à partir du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf354-240">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="bf354-241">Les objets désignés comme `System` n’ont pas de type JavaScript correspondant.</span><span class="sxs-lookup"><span data-stu-id="bf354-241">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="bf354-242">Chacune d’elles fait partie de l’implémentation du système d’objet de la VM JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf354-242">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="bf354-243">V8 alloue la plupart des objets internes dans le même tas que les objets JS de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bf354-243">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="bf354-244">Il s’uffit donc de V8 internes.</span><span class="sxs-lookup"><span data-stu-id="bf354-244">So these are just V8 internals.</span></span>  

## <a name="find-a-specific-object"></a><span data-ttu-id="bf354-245">Rechercher un objet spécifique</span><span class="sxs-lookup"><span data-stu-id="bf354-245">Find a specific object</span></span>  

<span data-ttu-id="bf354-246">Pour rechercher un objet dans le tas collecté, vous pouvez effectuer une recherche à l’aide de `Ctrl` + `F` l’ID d’objet et lui donner son ID.</span><span class="sxs-lookup"><span data-stu-id="bf354-246">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <a name="uncover-dom-leaks"></a><span data-ttu-id="bf354-247">Découvrir les fuites DOM</span><span class="sxs-lookup"><span data-stu-id="bf354-247">Uncover DOM leaks</span></span>  

<span data-ttu-id="bf354-248">Le profileur de tas a la possibilité de refléter les dépendances bidirectionnelles entre les objets natifs du navigateur \(nodes DOM, règles CSS\) et les objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bf354-248">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="bf354-249">Cela permet de découvrir d’autres fuites invisibles qui se produisent en raison de sous-arbre DOM détachées oublié flottant.</span><span class="sxs-lookup"><span data-stu-id="bf354-249">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="bf354-250">Les fuites DOM peuvent être plus importantes que vous ne le pensez.</span><span class="sxs-lookup"><span data-stu-id="bf354-250">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="bf354-251">Prenons l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="bf354-251">Consider the following sample.</span></span>  <span data-ttu-id="bf354-252">Quand le GC #tree-il ?</span><span class="sxs-lookup"><span data-stu-id="bf354-252">When is the #tree GC?</span></span>  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

<span data-ttu-id="bf354-253">Il conserve une référence à l’objet parent \(parentNode\) pertinent et de manière récursive jusqu’à , donc uniquement lorsque leafRef est nullifié est l’arborescence WHOLE sous un candidat pour `#leaf` `#tree` `#tree` GC.</span><span class="sxs-lookup"><span data-stu-id="bf354-253">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Sous-arbre DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="bf354-255">Sous-arbre DOM</span><span class="sxs-lookup"><span data-stu-id="bf354-255">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="bf354-256">Exemples : essayez cet exemple de fuite d’un nœud [DOM][GlitchDevtoolsMemoryExample06] pour comprendre où il peut être divulgué et comment le détecter.</span><span class="sxs-lookup"><span data-stu-id="bf354-256">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="bf354-257">Vous pouvez également examiner cet exemple de [fuites DOM plus importantes que prévu.][GlitchDevtoolsMemoryExample09]</span><span class="sxs-lookup"><span data-stu-id="bf354-257">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="bf354-258">Pour en savoir plus sur les fuites DOM et les principes de base de l’analyse de la mémoire, consultez La recherche et le débogage des fuites de mémoire avec [Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] byPéroïoPér.</span><span class="sxs-lookup"><span data-stu-id="bf354-258">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="bf354-259">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="bf354-259">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tailles des objets : terminologie de la mémoire | Documents Microsoft"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Objets conservant l’arborescence - Terminologie de la mémoire | Documents Microsoft"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html - Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "mémoire | Diapositives"  

> [!NOTE]
> <span data-ttu-id="bf354-269">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bf354-269">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="bf354-270">La page d’origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) et est co-auteure par [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="bf354-270">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="bf354-272">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="bf354-272">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
