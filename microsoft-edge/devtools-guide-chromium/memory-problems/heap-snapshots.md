---
description: Découvrez comment enregistrer des instantanés de tas avec le profileur de segments de DevTools Microsoft Edge et Rechercher des fuites de mémoire.
title: Enregistrement des instantanés des tas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 15692b0258de6db66c0b58a2659348a6e849aaca
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993470"
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

# <span data-ttu-id="def0c-104">Enregistrement des instantanés des tas</span><span class="sxs-lookup"><span data-stu-id="def0c-104">How to record heap snapshots</span></span>  

<span data-ttu-id="def0c-105">Découvrez comment enregistrer des instantanés de tas avec le profileur de segments de DevTools Microsoft Edge et Rechercher des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="def0c-105">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="def0c-106">Le Microsoft Edge DevTools de segment de mémoire montre la distribution de mémoire par les objets JavaScript et les nœuds DOM associés de votre page.</span><span class="sxs-lookup"><span data-stu-id="def0c-106">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="def0c-107">Utilisez-la pour prendre des instantanés de tas JavaScript \ (JS Heap \) instantanés, analyser les graphiques de mémoire, comparer des instantanés et détecter des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="def0c-107">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="def0c-108">Voir aussi [objets en conservation d’arborescence][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="def0c-108">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="def0c-109">Prendre un cliché</span><span class="sxs-lookup"><span data-stu-id="def0c-109">Take a snapshot</span></span>  

<span data-ttu-id="def0c-110">Dans le panneau **mémoire** , sélectionnez **prendre une photo**, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="def0c-110">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="def0c-111">Vous pouvez également appuyer sur `Ctrl` + `E` \ (Windows \) ou `Cmd` + `E` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="def0c-111">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Sélectionner type de profil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="def0c-113">Sélectionner type de profil</span><span class="sxs-lookup"><span data-stu-id="def0c-113">Select profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="def0c-114">Les **captures instantanées** sont initialement stockées dans la mémoire du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="def0c-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="def0c-115">Les captures d’écran sont transférées au DevTools à la demande, lorsque vous cliquez sur l’icône de capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="def0c-115">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="def0c-116">Une fois la capture instantanée chargée dans DevTools et analysée, le numéro sous le titre de l’instantané s’affiche et indique la [taille totale des objets JavaScript accessibles][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="def0c-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Taille totale des objets accessibles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="def0c-118">Taille totale des objets accessibles</span><span class="sxs-lookup"><span data-stu-id="def0c-118">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="def0c-119">Seuls les objets joignable sont inclus dans les captures d’image.</span><span class="sxs-lookup"><span data-stu-id="def0c-119">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="def0c-120">En outre, le fait de prendre un instantané commence toujours par un nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="def0c-120">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="def0c-121">Effacer des instantanés</span><span class="sxs-lookup"><span data-stu-id="def0c-121">Clear snapshots</span></span>  

<span data-ttu-id="def0c-122">Cliquez sur l’icône **Effacer tous les profils** pour supprimer les snapshots \ (à la fois du devtools et de la mémoire associée au processus de rendu.).</span><span class="sxs-lookup"><span data-stu-id="def0c-122">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Supprimer des snapshots" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="def0c-124">Supprimer des snapshots</span><span class="sxs-lookup"><span data-stu-id="def0c-124">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="def0c-125">La fermeture de la fenêtre DevTools ne supprime pas les profils de la mémoire associée au processus de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="def0c-125">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="def0c-126">Lors de la réouverture de DevTools, tous les instantanés précédemment exécutés apparaissent dans la liste des instantanés.</span><span class="sxs-lookup"><span data-stu-id="def0c-126">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="def0c-127">Testez cet exemple d' [objets disséminés][GlitchDevtoolsMemoryExample03] et profilez-le à l’aide du profileur de tas.</span><span class="sxs-lookup"><span data-stu-id="def0c-127">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="def0c-128">Vous devez voir un certain nombre d’attributions d’éléments \ (objet \).</span><span class="sxs-lookup"><span data-stu-id="def0c-128">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="def0c-129">Afficher des instantanés</span><span class="sxs-lookup"><span data-stu-id="def0c-129">View snapshots</span></span>  

<span data-ttu-id="def0c-130">Affichez les captures d’écran de différentes perspectives pour différentes tâches.</span><span class="sxs-lookup"><span data-stu-id="def0c-130">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="def0c-131">**Vue récapitulative** montre les objets regroupés par nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="def0c-131">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="def0c-132">Vous pouvez l’utiliser pour rechercher les objets \ (et l’utilisation de la mémoire \) en fonction du type de nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="def0c-132">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="def0c-133">Elle est particulièrement utile pour effectuer **le suivi des fuites DOM**.</span><span class="sxs-lookup"><span data-stu-id="def0c-133">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="def0c-134">**Affichage comparaison**.</span><span class="sxs-lookup"><span data-stu-id="def0c-134">**Comparison view**.</span></span>  <span data-ttu-id="def0c-135">Affiche la différence entre deux instantanés.</span><span class="sxs-lookup"><span data-stu-id="def0c-135">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="def0c-136">Utilisez-la pour comparer deux ou plusieurs \ instantanés de mémoire de avant et après une opération.</span><span class="sxs-lookup"><span data-stu-id="def0c-136">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="def0c-137">L’examen de la quantité de mémoire et de la mémoire libérée permet de vérifier la présence et la cause d’une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="def0c-137">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="def0c-138">**Affichage contenant**.</span><span class="sxs-lookup"><span data-stu-id="def0c-138">**Containment view**.</span></span>  <span data-ttu-id="def0c-139">Autorise l’exploration du contenu du tas.</span><span class="sxs-lookup"><span data-stu-id="def0c-139">Allows exploration of heap contents.</span></span>  <span data-ttu-id="def0c-140">Le **mode** de conservation fournit une meilleure vue de la structure de l’objet, facilitant l’analyse des objets référencés dans l’espace de noms global \ (fenêtre \) pour découvrir ce qu’ils conservent.</span><span class="sxs-lookup"><span data-stu-id="def0c-140">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="def0c-141">Utilisez-le pour analyser les fermetures et explorer vos objets à un niveau faible.</span><span class="sxs-lookup"><span data-stu-id="def0c-141">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="def0c-142">Pour basculer entre les affichages, utilisez le sélecteur en haut de la vue.</span><span class="sxs-lookup"><span data-stu-id="def0c-142">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Changer de sélecteur de vues" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="def0c-144">Changer de sélecteur de vues</span><span class="sxs-lookup"><span data-stu-id="def0c-144">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="def0c-145">Toutes les propriétés ne sont pas stockées dans le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="def0c-145">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="def0c-146">Les propriétés implémentées à l’aide d’accesseurs qui exécutent du code natif ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="def0c-146">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="def0c-147">Par ailleurs, les valeurs qui ne sont pas des chaînes telles que des nombres ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="def0c-147">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="def0c-148">Affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="def0c-148">Summary view</span></span>  

<span data-ttu-id="def0c-149">À l’origine, une capture d’écran s’ouvre dans l’affichage de synthèse et affiche les totaux d’objets, qui risquent d’être développés pour afficher les instances:</span><span class="sxs-lookup"><span data-stu-id="def0c-149">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Affichage de synthèse" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="def0c-151">Affichage de **synthèse**</span><span class="sxs-lookup"><span data-stu-id="def0c-151">**Summary** view</span></span>  
:::image-end:::  

<span data-ttu-id="def0c-152">Les entrées de niveau supérieur correspondent à des lignes «total».</span><span class="sxs-lookup"><span data-stu-id="def0c-152">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="def0c-153">Entrées de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="def0c-153">Top-level entries</span></span> | <span data-ttu-id="def0c-154">Description</span><span class="sxs-lookup"><span data-stu-id="def0c-154">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="def0c-155">Constructeur</span><span class="sxs-lookup"><span data-stu-id="def0c-155">Constructor</span></span>** | <span data-ttu-id="def0c-156">Représente tous les objets créés à l’aide de ce constructeur.</span><span class="sxs-lookup"><span data-stu-id="def0c-156">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="def0c-157">Distance</span><span class="sxs-lookup"><span data-stu-id="def0c-157">Distance</span></span>** | <span data-ttu-id="def0c-158">affiche la distance à la racine en utilisant le chemin de nœud simple le plus court.</span><span class="sxs-lookup"><span data-stu-id="def0c-158">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="def0c-159">Taille superficielle</span><span class="sxs-lookup"><span data-stu-id="def0c-159">Shallow size</span></span>** | <span data-ttu-id="def0c-160">Affiche la somme de tailles superficielles de tous les objets créés par une certaine fonction Constructor.</span><span class="sxs-lookup"><span data-stu-id="def0c-160">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="def0c-161">La taille superficielle correspond à la taille de la mémoire maintenue par un objet \ (en général, les tableaux et les chaînes ont des tailles superficielles plus grandes».</span><span class="sxs-lookup"><span data-stu-id="def0c-161">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="def0c-162">Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="def0c-162">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="def0c-163">Taille retenue</span><span class="sxs-lookup"><span data-stu-id="def0c-163">Retained size</span></span>** | <span data-ttu-id="def0c-164">Affiche la taille maximale conservée entre le même jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="def0c-164">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="def0c-165">La taille de mémoire que vous pouvez libérer après la suppression d’un objet (et les dépendants n’est plus joignable \) est appelée taille retenue.</span><span class="sxs-lookup"><span data-stu-id="def0c-165">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="def0c-166">Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="def0c-166">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="def0c-167">Après avoir étendu une ligne du total dans l’affichage supérieur, toutes les instances sont affichées.</span><span class="sxs-lookup"><span data-stu-id="def0c-167">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="def0c-168">Pour chaque instance, les tailles superficielle et retenue sont affichées dans les colonnes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="def0c-168">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="def0c-169">Le nombre après le `@` caractère est l’identificateur unique de l’objet, ce qui vous permet de comparer les instantanés de tas en fonction de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="def0c-169">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="def0c-170">N’oubliez pas que les objets jaunes possèdent des références JavaScript et des objets rouges sont des nœuds détachés qui sont référencés à partir d’un arrière-plan jaune.</span><span class="sxs-lookup"><span data-stu-id="def0c-170">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="def0c-171">À quoi correspondent les différentes entrées de Constructor (Group \) dans le générateur de mémoire de segment?</span><span class="sxs-lookup"><span data-stu-id="def0c-171">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Groupes de constructeurs" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="def0c-173">Groupes de **constructeurs**</span><span class="sxs-lookup"><span data-stu-id="def0c-173">**Constructor** groups</span></span>  
:::image-end:::  

| <span data-ttu-id="def0c-174">Entrée Constructor (groupe \)</span><span class="sxs-lookup"><span data-stu-id="def0c-174">Constructor \(group\) entry</span></span> | <span data-ttu-id="def0c-175">Description</span><span class="sxs-lookup"><span data-stu-id="def0c-175">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="def0c-176">\ (propriété globale \)</span><span class="sxs-lookup"><span data-stu-id="def0c-176">\(global property\)</span></span>** | <span data-ttu-id="def0c-177">Objets intermédiaires entre un objet global \ (par exemple, `window` \) et un objet référencé par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="def0c-177">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="def0c-178">Si un objet est créé à l’aide d’un constructeur `Person` et est maintenu par un objet global, le chemin d’accès de conservation ressemble à ceci `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="def0c-178">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="def0c-179">Cela contraste avec la norme, où les objets se référencent directement.</span><span class="sxs-lookup"><span data-stu-id="def0c-179">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="def0c-180">Il existe des objets intermédiaires pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="def0c-180">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="def0c-181">Les éléments globaux sont modifiés régulièrement et les optimisations d’accès aux propriétés font l’objet d’un bon travail pour les objets non globaux et ne s’applique pas aux globales.</span><span class="sxs-lookup"><span data-stu-id="def0c-181">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="def0c-182">\ (racines \)</span><span class="sxs-lookup"><span data-stu-id="def0c-182">\(roots\)</span></span>** | <span data-ttu-id="def0c-183">Les entrées racines dans l’arborescence conservation sont les entités qui contiennent des références à l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="def0c-183">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="def0c-184">Les entrées pourront également être des références créées par le moteur pour des raisons spécifiques au moteur.</span><span class="sxs-lookup"><span data-stu-id="def0c-184">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="def0c-185">Le moteur comporte des mises en cache qui font référence aux objets, mais ces références sont faibles et n’empêchent pas la collecte d’un objet en raison de l’absence de références réellement fortes.</span><span class="sxs-lookup"><span data-stu-id="def0c-185">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="def0c-186">\ (fermeture \)</span><span class="sxs-lookup"><span data-stu-id="def0c-186">\(closure\)</span></span>** | <span data-ttu-id="def0c-187">Nombre de références à un groupe d’objets par le biais de la fermeture de fonction.</span><span class="sxs-lookup"><span data-stu-id="def0c-187">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="def0c-188">\ (matrice, chaîne, nombre, RegExp \)</span><span class="sxs-lookup"><span data-stu-id="def0c-188">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="def0c-189">Liste de types d’objets avec des propriétés qui font référence à un tableau, une chaîne, un nombre ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="def0c-189">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="def0c-190">\ (code compilé \)</span><span class="sxs-lookup"><span data-stu-id="def0c-190">\(compiled code\)</span></span>** | <span data-ttu-id="def0c-191">Tout ce qui concerne le code compilé.</span><span class="sxs-lookup"><span data-stu-id="def0c-191">Everything related to compiled code.</span></span>  <span data-ttu-id="def0c-192">Le script est semblable à une fonction, mais correspond à un `<script>` corps.</span><span class="sxs-lookup"><span data-stu-id="def0c-192">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="def0c-193">SharedFunctionInfos \ (SFI \) les objets se trouvent dans les fonctions et dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="def0c-193">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="def0c-194">Les fonctions disposent généralement d’un contexte, même si SFIs.</span><span class="sxs-lookup"><span data-stu-id="def0c-194">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="def0c-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, etc.</span><span class="sxs-lookup"><span data-stu-id="def0c-195">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="def0c-196">Fait référence à des éléments ou des objets document d’un type particulier référencé par votre code.</span><span class="sxs-lookup"><span data-stu-id="def0c-196">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="def0c-197">Affichage comparaison</span><span class="sxs-lookup"><span data-stu-id="def0c-197">Comparison view</span></span>  

<span data-ttu-id="def0c-198">Recherchez les objets perdus en comparant plusieurs instantanés entre eux.</span><span class="sxs-lookup"><span data-stu-id="def0c-198">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="def0c-199">Pour vérifier que l’opération d’une certaine application ne crée pas de fuites (par exemple, une paire d’opérations directes ou inverses, telles que l’ouverture d’un document, puis la fermeture, ne doit pas laisser de place à un autre), vous pouvez suivre le scénario suivant:</span><span class="sxs-lookup"><span data-stu-id="def0c-199">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="def0c-200">Prenez un instantané de tas avant d’exécuter une opération.</span><span class="sxs-lookup"><span data-stu-id="def0c-200">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="def0c-201">Effectuer une opération \ (interagissez avec une page d’une manière que vous pensez être à l’origine d’une fuite \).</span><span class="sxs-lookup"><span data-stu-id="def0c-201">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="def0c-202">Effectuez une opération inverse \ (faites l’interaction inverse et répétez-la quelques fois...).</span><span class="sxs-lookup"><span data-stu-id="def0c-202">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="def0c-203">Prenez un second instantané de tas et changez le mode d’affichage de celui-ci en **comparaison**, en le comparant à **snapshot 1**.</span><span class="sxs-lookup"><span data-stu-id="def0c-203">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="def0c-204">Dans l’affichage **comparaison** , la différence entre les deux instantanés s’affiche.</span><span class="sxs-lookup"><span data-stu-id="def0c-204">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="def0c-205">Lorsque vous développez une entrée de total, des instances d’objet ajoutées et supprimées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="def0c-205">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Affichage comparaison" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="def0c-207">Affichage **comparaison**</span><span class="sxs-lookup"><span data-stu-id="def0c-207">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="def0c-208">Affichage contenant</span><span class="sxs-lookup"><span data-stu-id="def0c-208">Containment view</span></span>  

<span data-ttu-id="def0c-209">Le mode de **confinement** est essentiellement une vue aérienne de la structure Objects de votre application.</span><span class="sxs-lookup"><span data-stu-id="def0c-209">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="def0c-210">Elle vous permet de lire dans les fermetures de fonctions, d’observer les objets internes de machine virtuelle \ (VM \) qui constituent vos objets JavaScript et de comprendre la quantité de mémoire utilisée par votre application à un niveau très bas.</span><span class="sxs-lookup"><span data-stu-id="def0c-210">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="def0c-211">Points d’entrée du mode contenant</span><span class="sxs-lookup"><span data-stu-id="def0c-211">Containment view entry points</span></span> | <span data-ttu-id="def0c-212">Description</span><span class="sxs-lookup"><span data-stu-id="def0c-212">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="def0c-213">Objets DOMWindow</span><span class="sxs-lookup"><span data-stu-id="def0c-213">DOMWindow objects</span></span>** | <span data-ttu-id="def0c-214">Objets globaux pour le code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="def0c-214">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="def0c-215">Racines GC</span><span class="sxs-lookup"><span data-stu-id="def0c-215">GC roots</span></span>** | <span data-ttu-id="def0c-216">Les racines du GC réel utilisées par le nettoyage de la mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="def0c-216">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="def0c-217">Les racines de catalogue global sont composées de cartes d’objets intégrés, de tableaux de symboles, de piles de threads d’ordinateur de construction, de caches de compilation, de gestionnaires d’étendues et de descripteurs globaux.</span><span class="sxs-lookup"><span data-stu-id="def0c-217">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="def0c-218">Objets natifs</span><span class="sxs-lookup"><span data-stu-id="def0c-218">Native objects</span></span>** | <span data-ttu-id="def0c-219">Objets de navigateur «Push» à l’intérieur de la machine virtuelle JavaScript (VM) pour autoriser l’automatisation (par exemple, les nœuds DOM et les règles CSS).</span><span class="sxs-lookup"><span data-stu-id="def0c-219">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Affichage contenant" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="def0c-221">Affichage **contenant**</span><span class="sxs-lookup"><span data-stu-id="def0c-221">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="def0c-222">Astuce sur les fermetures.</span><span class="sxs-lookup"><span data-stu-id="def0c-222">A tip about closures.</span></span>  <span data-ttu-id="def0c-223">Nommez les fonctions pour pouvoir distinguer facilement les fermetures de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="def0c-223">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="def0c-224">Par exemple, cet exemple n’utilise pas de fonctions nommées.</span><span class="sxs-lookup"><span data-stu-id="def0c-224">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="def0c-225">L’extrait de followingcode utilise des fonctions nommées.</span><span class="sxs-lookup"><span data-stu-id="def0c-225">The followingcode snippet uses named functions.</span></span>  
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
> > <span data-ttu-id="def0c-226">Essayez cet exemple pour savoir [pourquoi `eval` ][GlitchDevtoolsMemoryExample07] un élément malveillant analyse l’impact de la fermeture sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="def0c-226">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="def0c-227">Vous serez peut-être également intéressé par le suivi de cet exemple qui vous permet d’accéder à des [allocations de tas][GlitchDevtoolsMemoryExample08]d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="def0c-227">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="def0c-228">Chercher un codage en couleurs</span><span class="sxs-lookup"><span data-stu-id="def0c-228">Look up color coding</span></span>  

<span data-ttu-id="def0c-229">Les propriétés et valeurs de propriété des objets ont des types différents et sont en conséquence.</span><span class="sxs-lookup"><span data-stu-id="def0c-229">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="def0c-230">Chaque propriété comporte l’un des quatre types suivants.</span><span class="sxs-lookup"><span data-stu-id="def0c-230">Each property has one of four types.</span></span>  

| <span data-ttu-id="def0c-231">Type de propriété</span><span class="sxs-lookup"><span data-stu-id="def0c-231">Property Type</span></span> | <span data-ttu-id="def0c-232">Description</span><span class="sxs-lookup"><span data-stu-id="def0c-232">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="def0c-233">a: propriété</span><span class="sxs-lookup"><span data-stu-id="def0c-233">a: property</span></span>** | <span data-ttu-id="def0c-234">Propriété standard avec un nom, accessible par le biais de l' `.` opérateur \ (point \) ou par le biais `[` `]` de la notation \ (crochets \), par exemple `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="def0c-234">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="def0c-235">0: élément</span><span class="sxs-lookup"><span data-stu-id="def0c-235">0: element</span></span>** | <span data-ttu-id="def0c-236">Propriété standard avec un index numérique, accessible via la `[` `]` notation \ (crochets \).</span><span class="sxs-lookup"><span data-stu-id="def0c-236">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="def0c-237">a: var du contexte</span><span class="sxs-lookup"><span data-stu-id="def0c-237">a: context var</span></span>** |  <span data-ttu-id="def0c-238">Variable dans un contexte de fonction, accessible par le nom de la variable à partir de la fermeture d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="def0c-238">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="def0c-239">a: système prop</span><span class="sxs-lookup"><span data-stu-id="def0c-239">a: system prop</span></span>** | <span data-ttu-id="def0c-240">Propriété ajoutée par le VM JavaScript, qui n’est pas accessible à partir du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="def0c-240">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="def0c-241">Les objets désignés comme `System` ne disposant pas d’un type JavaScript correspondant;</span><span class="sxs-lookup"><span data-stu-id="def0c-241">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="def0c-242">Chacun fait partie de l’implémentation du système d’objets de la machine virtuelle JavaScript.</span><span class="sxs-lookup"><span data-stu-id="def0c-242">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="def0c-243">V8 alloue la plupart des objets internes dans le même segment de mémoire que les objets JS de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="def0c-243">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="def0c-244">C’est alors que les éléments internes sont uniquement en interne.</span><span class="sxs-lookup"><span data-stu-id="def0c-244">So these are just V8 internals.</span></span>  

## <span data-ttu-id="def0c-245">Rechercher un objet spécifique</span><span class="sxs-lookup"><span data-stu-id="def0c-245">Find a specific object</span></span>  

<span data-ttu-id="def0c-246">Pour rechercher un objet dans le tas collecté, vous pouvez effectuer une recherche sur l’ID de l' `Ctrl` + `F` objet.</span><span class="sxs-lookup"><span data-stu-id="def0c-246">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="def0c-247">Découvrir les fuites DOM</span><span class="sxs-lookup"><span data-stu-id="def0c-247">Uncover DOM leaks</span></span>  

<span data-ttu-id="def0c-248">Le profileur de tas a la possibilité de répercuter les dépendances bidirectionnelles entre les objets natifs du navigateur (nœud DOM, règles CSS \) et objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="def0c-248">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="def0c-249">Cela permet de détecter d’éventuelles fuites de fuite en raison de l’oubli d’arborescences DOM dissociées.</span><span class="sxs-lookup"><span data-stu-id="def0c-249">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="def0c-250">Les fuites DOM risquent d’être plus grandes que vous ne le pensez.</span><span class="sxs-lookup"><span data-stu-id="def0c-250">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="def0c-251">Prenons l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="def0c-251">Consider the following sample.</span></span>  <span data-ttu-id="def0c-252">Quand est-ce que le CG #tree?</span><span class="sxs-lookup"><span data-stu-id="def0c-252">When is the #tree GC?</span></span>  

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

<span data-ttu-id="def0c-253">Le `#leaf` maintien d’une référence au parent approprié \ (ParentNode \) et de manière récurrente jusqu’à ce que le `#tree` leafRef soit annulé comme l’arborescence entière sous `#tree` un candidat pour le CG.</span><span class="sxs-lookup"><span data-stu-id="def0c-253">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Sous-arbres DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="def0c-255">Sous-arbres DOM</span><span class="sxs-lookup"><span data-stu-id="def0c-255">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="def0c-256">Exemples: Essayez cet exemple de [nœud DOM en fuite][GlitchDevtoolsMemoryExample06] pour savoir où il est susceptible de fuir et comment le détecter.</span><span class="sxs-lookup"><span data-stu-id="def0c-256">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="def0c-257">Vous pouvez également examiner cet exemple de [fuites DOM plus grandes que prévu][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="def0c-257">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="def0c-258">Pour en savoir plus sur les fuites DOM et l’analyse en mémoire notions fondamentales sur [la recherche et le débogage de fuites de mémoire avec Microsoft Edge devtools][GonzaloRuizdeVillaMemory] par Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="def0c-258">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <span data-ttu-id="def0c-259">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="def0c-259">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tailles d’objets-terminologie de mémoire | Documents Microsoft"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Objets qui conservent une terminologie en mémoire en arborescence | Documents Microsoft"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html-Microsoft Edge (chrome) DevTools | Problème"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "mémoire | Diapo"  

> [!NOTE]
> <span data-ttu-id="def0c-269">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="def0c-269">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="def0c-270">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="def0c-270">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="def0c-272">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="def0c-272">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
