---
title: Enregistrement des instantanés des tas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bd46489d8a8a3fddbff60618b4997784294cccff
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985429"
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





# <span data-ttu-id="94eb4-103">Enregistrement des instantanés des tas</span><span class="sxs-lookup"><span data-stu-id="94eb4-103">How to record heap snapshots</span></span>   



<span data-ttu-id="94eb4-104">Découvrez comment enregistrer des instantanés de tas avec le profileur de segments de DevTools Microsoft Edge et Rechercher des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="94eb4-104">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="94eb4-105">Le Microsoft Edge DevTools de segment de mémoire montre la distribution de mémoire par les objets JavaScript et les nœuds DOM associés de votre page.</span><span class="sxs-lookup"><span data-stu-id="94eb4-105">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="94eb4-106">Utilisez-la pour prendre des instantanés de tas JavaScript \ (JS Heap \) instantanés, analyser les graphiques de mémoire, comparer des instantanés et détecter des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="94eb4-106">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="94eb4-107">Voir aussi [objets en conservation d’arborescence][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="94eb4-107">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="94eb4-108">Prendre un cliché</span><span class="sxs-lookup"><span data-stu-id="94eb4-108">Take a snapshot</span></span>  

<span data-ttu-id="94eb4-109">Dans le panneau **mémoire** , sélectionnez **prendre une photo**, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="94eb4-109">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="94eb4-110">Vous pouvez également appuyer sur `Ctrl` + `E` \ (Windows \) ou `Cmd` + `E` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="94eb4-110">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Sélectionner type de profil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   <span data-ttu-id="94eb4-112">Sélectionner type de profil</span><span class="sxs-lookup"><span data-stu-id="94eb4-112">Select profiling type</span></span>  
:::image-end:::  

<span data-ttu-id="94eb4-113">Les **captures instantanées** sont initialement stockées dans la mémoire du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="94eb4-113">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="94eb4-114">Les captures d’écran sont transférées au DevTools à la demande, lorsque vous cliquez sur l’icône de capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="94eb4-114">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="94eb4-115">Une fois la capture instantanée chargée dans DevTools et analysée, le numéro sous le titre de l’instantané s’affiche et indique la [taille totale des objets JavaScript accessibles][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="94eb4-115">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Taille totale des objets accessibles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   <span data-ttu-id="94eb4-117">Taille totale des objets accessibles</span><span class="sxs-lookup"><span data-stu-id="94eb4-117">Total size of reachable objects</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="94eb4-118">Seuls les objets joignable sont inclus dans les captures d’image.</span><span class="sxs-lookup"><span data-stu-id="94eb4-118">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="94eb4-119">En outre, le fait de prendre un instantané commence toujours par un nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="94eb4-119">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="94eb4-120">Effacer des instantanés</span><span class="sxs-lookup"><span data-stu-id="94eb4-120">Clear snapshots</span></span>  

<span data-ttu-id="94eb4-121">Cliquez sur l’icône **Effacer tous les profils** pour supprimer les snapshots \ (à la fois du devtools et de la mémoire associée au processus de rendu.).</span><span class="sxs-lookup"><span data-stu-id="94eb4-121">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Supprimer des snapshots" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   <span data-ttu-id="94eb4-123">Supprimer des snapshots</span><span class="sxs-lookup"><span data-stu-id="94eb4-123">Remove snapshots</span></span>  
:::image-end:::  

<span data-ttu-id="94eb4-124">La fermeture de la fenêtre DevTools ne supprime pas les profils de la mémoire associée au processus de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="94eb4-124">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="94eb4-125">Lors de la réouverture de DevTools, tous les instantanés précédemment exécutés apparaissent dans la liste des instantanés.</span><span class="sxs-lookup"><span data-stu-id="94eb4-125">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="94eb4-126">Testez cet exemple d' [objets disséminés][GlitchDevtoolsMemoryExample03] et profilez-le à l’aide du profileur de tas.</span><span class="sxs-lookup"><span data-stu-id="94eb4-126">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="94eb4-127">Vous devez voir un certain nombre d’attributions d’éléments \ (objet \).</span><span class="sxs-lookup"><span data-stu-id="94eb4-127">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="94eb4-128">Afficher des instantanés</span><span class="sxs-lookup"><span data-stu-id="94eb4-128">View snapshots</span></span>  

<span data-ttu-id="94eb4-129">Affichez les captures d’écran de différentes perspectives pour différentes tâches.</span><span class="sxs-lookup"><span data-stu-id="94eb4-129">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="94eb4-130">**Vue récapitulative** montre les objets regroupés par nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="94eb4-130">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="94eb4-131">Vous pouvez l’utiliser pour rechercher les objets \ (et l’utilisation de la mémoire \) en fonction du type de nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="94eb4-131">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="94eb4-132">Elle est particulièrement utile pour effectuer **le suivi des fuites DOM**.</span><span class="sxs-lookup"><span data-stu-id="94eb4-132">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="94eb4-133">**Affichage comparaison**.</span><span class="sxs-lookup"><span data-stu-id="94eb4-133">**Comparison view**.</span></span>  <span data-ttu-id="94eb4-134">Affiche la différence entre deux instantanés.</span><span class="sxs-lookup"><span data-stu-id="94eb4-134">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="94eb4-135">Utilisez-la pour comparer deux ou plusieurs \ instantanés de mémoire de avant et après une opération.</span><span class="sxs-lookup"><span data-stu-id="94eb4-135">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="94eb4-136">L’examen de la quantité de mémoire et de la mémoire libérée permet de vérifier la présence et la cause d’une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="94eb4-136">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="94eb4-137">**Affichage contenant**.</span><span class="sxs-lookup"><span data-stu-id="94eb4-137">**Containment view**.</span></span>  <span data-ttu-id="94eb4-138">Autorise l’exploration du contenu du tas.</span><span class="sxs-lookup"><span data-stu-id="94eb4-138">Allows exploration of heap contents.</span></span>  <span data-ttu-id="94eb4-139">Le **mode** de conservation fournit une meilleure vue de la structure de l’objet, facilitant l’analyse des objets référencés dans l’espace de noms global \ (fenêtre \) pour découvrir ce qu’ils conservent.</span><span class="sxs-lookup"><span data-stu-id="94eb4-139">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="94eb4-140">Utilisez-le pour analyser les fermetures et explorer vos objets à un niveau faible.</span><span class="sxs-lookup"><span data-stu-id="94eb4-140">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="94eb4-141">Pour basculer entre les affichages, utilisez le sélecteur en haut de la vue.</span><span class="sxs-lookup"><span data-stu-id="94eb4-141">To switch between views, use the selector at the top of the view.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Changer de sélecteur de vues" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   <span data-ttu-id="94eb4-143">Changer de sélecteur de vues</span><span class="sxs-lookup"><span data-stu-id="94eb4-143">Switch views selector</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="94eb4-144">Toutes les propriétés ne sont pas stockées dans le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="94eb4-144">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="94eb4-145">Les propriétés implémentées à l’aide d’accesseurs qui exécutent du code natif ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="94eb4-145">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="94eb4-146">Par ailleurs, les valeurs qui ne sont pas des chaînes telles que des nombres ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="94eb4-146">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="94eb4-147">Affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="94eb4-147">Summary view</span></span>  

<span data-ttu-id="94eb4-148">À l’origine, une capture d’écran s’ouvre dans l’affichage de synthèse et affiche les totaux d’objets, qui risquent d’être développés pour afficher les instances:</span><span class="sxs-lookup"><span data-stu-id="94eb4-148">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Affichage de synthèse" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   <span data-ttu-id="94eb4-150">Affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="94eb4-150">Summary view</span></span>  
:::image-end:::  

<span data-ttu-id="94eb4-151">Les entrées de niveau supérieur correspondent à des lignes «total».</span><span class="sxs-lookup"><span data-stu-id="94eb4-151">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="94eb4-152">Entrées de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="94eb4-152">Top-level entries</span></span> | <span data-ttu-id="94eb4-153">Description</span><span class="sxs-lookup"><span data-stu-id="94eb4-153">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="94eb4-154">Constructeur</span><span class="sxs-lookup"><span data-stu-id="94eb4-154">Constructor</span></span>** | <span data-ttu-id="94eb4-155">Représente tous les objets créés à l’aide de ce constructeur.</span><span class="sxs-lookup"><span data-stu-id="94eb4-155">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="94eb4-156">Distance</span><span class="sxs-lookup"><span data-stu-id="94eb4-156">Distance</span></span>** | <span data-ttu-id="94eb4-157">affiche la distance à la racine en utilisant le chemin de nœud simple le plus court.</span><span class="sxs-lookup"><span data-stu-id="94eb4-157">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="94eb4-158">Taille superficielle</span><span class="sxs-lookup"><span data-stu-id="94eb4-158">Shallow size</span></span>** | <span data-ttu-id="94eb4-159">Affiche la somme de tailles superficielles de tous les objets créés par une certaine fonction Constructor.</span><span class="sxs-lookup"><span data-stu-id="94eb4-159">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="94eb4-160">La taille superficielle correspond à la taille de la mémoire maintenue par un objet \ (en général, les tableaux et les chaînes ont des tailles superficielles plus grandes».</span><span class="sxs-lookup"><span data-stu-id="94eb4-160">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="94eb4-161">Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="94eb4-161">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="94eb4-162">Taille retenue</span><span class="sxs-lookup"><span data-stu-id="94eb4-162">Retained size</span></span>** | <span data-ttu-id="94eb4-163">Affiche la taille maximale conservée entre le même jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="94eb4-163">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="94eb4-164">La taille de mémoire que vous pouvez libérer après la suppression d’un objet (et les dépendants n’est plus joignable \) est appelée taille retenue.</span><span class="sxs-lookup"><span data-stu-id="94eb4-164">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="94eb4-165">Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="94eb4-165">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="94eb4-166">Après avoir étendu une ligne du total dans l’affichage supérieur, toutes les instances sont affichées.</span><span class="sxs-lookup"><span data-stu-id="94eb4-166">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="94eb4-167">Pour chaque instance, les tailles superficielle et retenue sont affichées dans les colonnes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="94eb4-167">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="94eb4-168">Le nombre après le `@` caractère est l’identificateur unique de l’objet, ce qui vous permet de comparer les instantanés de tas en fonction de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="94eb4-168">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="94eb4-169">N’oubliez pas que les objets jaunes possèdent des références JavaScript et des objets rouges sont des nœuds détachés qui sont référencés à partir d’un arrière-plan jaune.</span><span class="sxs-lookup"><span data-stu-id="94eb4-169">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="94eb4-170">À quoi correspondent les différentes entrées de Constructor (Group \) dans le générateur de mémoire de segment?</span><span class="sxs-lookup"><span data-stu-id="94eb4-170">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Groupes de constructeurs" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   <span data-ttu-id="94eb4-172">Groupes de constructeurs</span><span class="sxs-lookup"><span data-stu-id="94eb4-172">Constructor groups</span></span>  
:::image-end:::  

| <span data-ttu-id="94eb4-173">Entrée Constructor (groupe \)</span><span class="sxs-lookup"><span data-stu-id="94eb4-173">Constructor \(group\) entry</span></span> | <span data-ttu-id="94eb4-174">Description</span><span class="sxs-lookup"><span data-stu-id="94eb4-174">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="94eb4-175">\ (propriété globale \)</span><span class="sxs-lookup"><span data-stu-id="94eb4-175">\(global property\)</span></span>** | <span data-ttu-id="94eb4-176">Objets intermédiaires entre un objet global \ (par exemple, `window` \) et un objet référencé par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="94eb4-176">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="94eb4-177">Si un objet est créé à l’aide d’un constructeur `Person` et est maintenu par un objet global, le chemin d’accès de conservation ressemble à ceci `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="94eb4-177">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="94eb4-178">Cela contraste avec la norme, où les objets se référencent directement.</span><span class="sxs-lookup"><span data-stu-id="94eb4-178">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="94eb4-179">Il existe des objets intermédiaires pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="94eb4-179">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="94eb4-180">Les éléments globaux sont modifiés régulièrement et les optimisations d’accès aux propriétés font l’objet d’un bon travail pour les objets non globaux et ne s’applique pas aux globales.</span><span class="sxs-lookup"><span data-stu-id="94eb4-180">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="94eb4-181">\ (racines \)</span><span class="sxs-lookup"><span data-stu-id="94eb4-181">\(roots\)</span></span>** | <span data-ttu-id="94eb4-182">Les entrées racines dans l’arborescence conservation sont les entités qui contiennent des références à l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="94eb4-182">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="94eb4-183">Les entrées pourront également être des références créées par le moteur pour des raisons spécifiques au moteur.</span><span class="sxs-lookup"><span data-stu-id="94eb4-183">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="94eb4-184">Le moteur comporte des mises en cache qui font référence aux objets, mais ces références sont faibles et n’empêchent pas la collecte d’un objet en raison de l’absence de références réellement fortes.</span><span class="sxs-lookup"><span data-stu-id="94eb4-184">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="94eb4-185">\ (fermeture \)</span><span class="sxs-lookup"><span data-stu-id="94eb4-185">\(closure\)</span></span>** | <span data-ttu-id="94eb4-186">Nombre de références à un groupe d’objets par le biais de la fermeture de fonction.</span><span class="sxs-lookup"><span data-stu-id="94eb4-186">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="94eb4-187">\ (matrice, chaîne, nombre, RegExp \)</span><span class="sxs-lookup"><span data-stu-id="94eb4-187">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="94eb4-188">Liste de types d’objets avec des propriétés qui font référence à un tableau, une chaîne, un nombre ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="94eb4-188">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="94eb4-189">\ (code compilé \)</span><span class="sxs-lookup"><span data-stu-id="94eb4-189">\(compiled code\)</span></span>** | <span data-ttu-id="94eb4-190">Tout ce qui concerne le code compilé.</span><span class="sxs-lookup"><span data-stu-id="94eb4-190">Everything related to compiled code.</span></span>  <span data-ttu-id="94eb4-191">Le script est semblable à une fonction, mais correspond à un `<script>` corps.</span><span class="sxs-lookup"><span data-stu-id="94eb4-191">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="94eb4-192">SharedFunctionInfos \ (SFI \) les objets se trouvent dans les fonctions et dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="94eb4-192">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="94eb4-193">Les fonctions disposent généralement d’un contexte, même si SFIs.</span><span class="sxs-lookup"><span data-stu-id="94eb4-193">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="94eb4-194">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, etc.</span><span class="sxs-lookup"><span data-stu-id="94eb4-194">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="94eb4-195">Fait référence à des éléments ou des objets document d’un type particulier référencé par votre code.</span><span class="sxs-lookup"><span data-stu-id="94eb4-195">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="94eb4-196">Affichage comparaison</span><span class="sxs-lookup"><span data-stu-id="94eb4-196">Comparison view</span></span>  

<span data-ttu-id="94eb4-197">Recherchez les objets perdus en comparant plusieurs instantanés entre eux.</span><span class="sxs-lookup"><span data-stu-id="94eb4-197">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="94eb4-198">Pour vérifier que l’opération d’une certaine application ne crée pas de fuites (par exemple, une paire d’opérations directes ou inverses, telles que l’ouverture d’un document, puis la fermeture, ne doit pas laisser de place à un autre), vous pouvez suivre le scénario suivant:</span><span class="sxs-lookup"><span data-stu-id="94eb4-198">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="94eb4-199">Prenez un instantané de tas avant d’exécuter une opération.</span><span class="sxs-lookup"><span data-stu-id="94eb4-199">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="94eb4-200">Effectuer une opération \ (interagissez avec une page d’une manière que vous pensez être à l’origine d’une fuite \).</span><span class="sxs-lookup"><span data-stu-id="94eb4-200">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="94eb4-201">Effectuez une opération inverse \ (faites l’interaction inverse et répétez-la quelques fois...).</span><span class="sxs-lookup"><span data-stu-id="94eb4-201">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="94eb4-202">Prenez un second instantané de tas et changez le mode d’affichage de celui-ci en **comparaison**, en le comparant à **snapshot 1**.</span><span class="sxs-lookup"><span data-stu-id="94eb4-202">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  
    
<span data-ttu-id="94eb4-203">Dans l’affichage **comparaison** , la différence entre les deux instantanés s’affiche.</span><span class="sxs-lookup"><span data-stu-id="94eb4-203">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="94eb4-204">Lorsque vous développez une entrée de total, des instances d’objet ajoutées et supprimées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="94eb4-204">When expanding a total entry, added and deleted object instances are shown.</span></span>  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Affichage comparaison" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   <span data-ttu-id="94eb4-206">Affichage **comparaison**</span><span class="sxs-lookup"><span data-stu-id="94eb4-206">**Comparison** view</span></span>  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="94eb4-207">Affichage contenant</span><span class="sxs-lookup"><span data-stu-id="94eb4-207">Containment view</span></span>  

<span data-ttu-id="94eb4-208">Le mode de **confinement** est essentiellement une vue aérienne de la structure Objects de votre application.</span><span class="sxs-lookup"><span data-stu-id="94eb4-208">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="94eb4-209">Elle vous permet de lire dans les fermetures de fonctions, d’observer les objets internes de machine virtuelle \ (VM \) qui constituent vos objets JavaScript et de comprendre la quantité de mémoire utilisée par votre application à un niveau très bas.</span><span class="sxs-lookup"><span data-stu-id="94eb4-209">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="94eb4-210">Points d’entrée du mode contenant</span><span class="sxs-lookup"><span data-stu-id="94eb4-210">Containment view entry points</span></span> | <span data-ttu-id="94eb4-211">Description</span><span class="sxs-lookup"><span data-stu-id="94eb4-211">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="94eb4-212">Objets DOMWindow</span><span class="sxs-lookup"><span data-stu-id="94eb4-212">DOMWindow objects</span></span>** | <span data-ttu-id="94eb4-213">Objets globaux pour le code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="94eb4-213">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="94eb4-214">Racines GC</span><span class="sxs-lookup"><span data-stu-id="94eb4-214">GC roots</span></span>** | <span data-ttu-id="94eb4-215">Les racines du GC réel utilisées par le nettoyage de la mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="94eb4-215">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="94eb4-216">Les racines de catalogue global sont composées de cartes d’objets intégrés, de tableaux de symboles, de piles de threads d’ordinateur de construction, de caches de compilation, de gestionnaires d’étendues et de descripteurs globaux.</span><span class="sxs-lookup"><span data-stu-id="94eb4-216">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="94eb4-217">Objets natifs</span><span class="sxs-lookup"><span data-stu-id="94eb4-217">Native objects</span></span>** | <span data-ttu-id="94eb4-218">Objets de navigateur «Push» à l’intérieur de la machine virtuelle JavaScript (VM) pour autoriser l’automatisation (par exemple, les nœuds DOM et les règles CSS).</span><span class="sxs-lookup"><span data-stu-id="94eb4-218">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Affichage contenant" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   <span data-ttu-id="94eb4-220">Affichage **contenant**</span><span class="sxs-lookup"><span data-stu-id="94eb4-220">**Containment** view</span></span>  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="94eb4-221">Astuce sur les fermetures.</span><span class="sxs-lookup"><span data-stu-id="94eb4-221">A tip about closures.</span></span>  <span data-ttu-id="94eb4-222">Nommez les fonctions pour pouvoir distinguer facilement les fermetures de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="94eb4-222">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="94eb4-223">Par exemple, cet exemple n’utilise pas de fonctions nommées.</span><span class="sxs-lookup"><span data-stu-id="94eb4-223">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="94eb4-224">L’extrait de followingcode utilise des fonctions nommées.</span><span class="sxs-lookup"><span data-stu-id="94eb4-224">The followingcode snippet uses named functions.</span></span>  
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
> > <span data-ttu-id="94eb4-225">Essayez cet exemple pour savoir [pourquoi `eval` ][GlitchDevtoolsMemoryExample07] un élément malveillant analyse l’impact de la fermeture sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="94eb4-225">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="94eb4-226">Vous serez peut-être également intéressé par le suivi de cet exemple qui vous permet d’accéder à des [allocations de tas][GlitchDevtoolsMemoryExample08]d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="94eb4-226">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="94eb4-227">Chercher un codage en couleurs</span><span class="sxs-lookup"><span data-stu-id="94eb4-227">Look up color coding</span></span>  

<span data-ttu-id="94eb4-228">Les propriétés et valeurs de propriété des objets ont des types différents et sont en conséquence.</span><span class="sxs-lookup"><span data-stu-id="94eb4-228">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="94eb4-229">Chaque propriété comporte l’un des quatre types suivants.</span><span class="sxs-lookup"><span data-stu-id="94eb4-229">Each property has one of four types.</span></span>  

| <span data-ttu-id="94eb4-230">Type de propriété</span><span class="sxs-lookup"><span data-stu-id="94eb4-230">Property Type</span></span> | <span data-ttu-id="94eb4-231">Description</span><span class="sxs-lookup"><span data-stu-id="94eb4-231">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="94eb4-232">a: propriété</span><span class="sxs-lookup"><span data-stu-id="94eb4-232">a: property</span></span>** | <span data-ttu-id="94eb4-233">Propriété standard avec un nom, accessible par le biais de l' `.` opérateur \ (point \) ou par le biais `[` `]` de la notation \ (crochets \), par exemple `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="94eb4-233">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="94eb4-234">0: élément</span><span class="sxs-lookup"><span data-stu-id="94eb4-234">0: element</span></span>** | <span data-ttu-id="94eb4-235">Propriété standard avec un index numérique, accessible via la `[` `]` notation \ (crochets \).</span><span class="sxs-lookup"><span data-stu-id="94eb4-235">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="94eb4-236">a: var du contexte</span><span class="sxs-lookup"><span data-stu-id="94eb4-236">a: context var</span></span>** |  <span data-ttu-id="94eb4-237">Variable dans un contexte de fonction, accessible par le nom de la variable à partir de la fermeture d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="94eb4-237">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="94eb4-238">a: système prop</span><span class="sxs-lookup"><span data-stu-id="94eb4-238">a: system prop</span></span>** | <span data-ttu-id="94eb4-239">Propriété ajoutée par le VM JavaScript, qui n’est pas accessible à partir du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="94eb4-239">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="94eb4-240">Les objets désignés comme `System` ne disposant pas d’un type JavaScript correspondant;</span><span class="sxs-lookup"><span data-stu-id="94eb4-240">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="94eb4-241">Chacun fait partie de l’implémentation du système d’objets de la machine virtuelle JavaScript.</span><span class="sxs-lookup"><span data-stu-id="94eb4-241">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="94eb4-242">V8 alloue la plupart des objets internes dans le même segment de mémoire que les objets JS de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="94eb4-242">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="94eb4-243">C’est alors que les éléments internes sont uniquement en interne.</span><span class="sxs-lookup"><span data-stu-id="94eb4-243">So these are just V8 internals.</span></span>  

## <span data-ttu-id="94eb4-244">Rechercher un objet spécifique</span><span class="sxs-lookup"><span data-stu-id="94eb4-244">Find a specific object</span></span>  

<span data-ttu-id="94eb4-245">Pour rechercher un objet dans le tas collecté, vous pouvez effectuer une recherche sur l’ID de l' `Ctrl` + `F` objet.</span><span class="sxs-lookup"><span data-stu-id="94eb4-245">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="94eb4-246">Découvrir les fuites DOM</span><span class="sxs-lookup"><span data-stu-id="94eb4-246">Uncover DOM leaks</span></span>  

<span data-ttu-id="94eb4-247">Le profileur de tas a la possibilité de répercuter les dépendances bidirectionnelles entre les objets natifs du navigateur (nœud DOM, règles CSS \) et objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="94eb4-247">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="94eb4-248">Cela permet de détecter d’éventuelles fuites de fuite en raison de l’oubli d’arborescences DOM dissociées.</span><span class="sxs-lookup"><span data-stu-id="94eb4-248">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="94eb4-249">Les fuites DOM risquent d’être plus grandes que vous ne le pensez.</span><span class="sxs-lookup"><span data-stu-id="94eb4-249">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="94eb4-250">Prenons l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="94eb4-250">Consider the following sample.</span></span>  <span data-ttu-id="94eb4-251">Quand est-ce que le CG #tree?</span><span class="sxs-lookup"><span data-stu-id="94eb4-251">When is the #tree GC?</span></span>  

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

<span data-ttu-id="94eb4-252">Le `#leaf` maintien d’une référence au parent approprié \ (ParentNode \) et de manière récurrente jusqu’à ce que le `#tree` leafRef soit annulé comme l’arborescence entière sous `#tree` un candidat pour le CG.</span><span class="sxs-lookup"><span data-stu-id="94eb4-252">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Sous-arbres DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   <span data-ttu-id="94eb4-254">Sous-arbres DOM</span><span class="sxs-lookup"><span data-stu-id="94eb4-254">DOM subtrees</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="94eb4-255">Exemples: Essayez cet exemple de [nœud DOM en fuite][GlitchDevtoolsMemoryExample06] pour savoir où il est susceptible de fuir et comment le détecter.</span><span class="sxs-lookup"><span data-stu-id="94eb4-255">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="94eb4-256">Vous pouvez également examiner cet exemple de [fuites DOM plus grandes que prévu][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="94eb4-256">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="94eb4-257">Pour en savoir plus sur les fuites DOM et l’analyse en mémoire notions fondamentales sur [la recherche et le débogage de fuites de mémoire avec Microsoft Edge devtools][GonzaloRuizdeVillaMemory] par Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="94eb4-257">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

<!--  
## Feedback   


-->  

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
> <span data-ttu-id="94eb4-267">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="94eb4-267">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="94eb4-268">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="94eb4-268">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="94eb4-270">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="94eb4-270">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
