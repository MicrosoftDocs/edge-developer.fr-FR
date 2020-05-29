---
title: Enregistrement des instantanés des tas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: e6f64b219bc2b28d01780c28cc605d56a07cb491
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611677"
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





# <span data-ttu-id="24e15-103">Enregistrement des instantanés des tas</span><span class="sxs-lookup"><span data-stu-id="24e15-103">How to Record Heap Snapshots</span></span>   



<span data-ttu-id="24e15-104">Découvrez comment enregistrer des instantanés de tas avec le profileur de segments de DevTools Microsoft Edge et Rechercher des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="24e15-104">Learn how to record heap snapshots with the Microsoft Edge DevTools heap profiler and find memory leaks.</span></span>  

<span data-ttu-id="24e15-105">Le Microsoft Edge DevTools de segment de mémoire montre la distribution de mémoire par les objets JavaScript et les nœuds DOM associés de votre page.</span><span class="sxs-lookup"><span data-stu-id="24e15-105">The Microsoft Edge DevTools heap profiler shows memory distribution by the JavaScript objects and related DOM nodes of your page.</span></span>  <span data-ttu-id="24e15-106">Utilisez-la pour prendre des instantanés de tas JavaScript \ (JS Heap \) instantanés, analyser les graphiques de mémoire, comparer des instantanés et détecter des fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="24e15-106">Use it to take JavaScript heap \(JS heap\) snapshots, analyze memory graphs, compare snapshots, and find memory leaks.</span></span>  <span data-ttu-id="24e15-107">Voir aussi [objets en conservation d’arborescence][DevtoolsMemoryProblems101ObjectsRetainingTree].</span><span class="sxs-lookup"><span data-stu-id="24e15-107">See also [Objects retaining tree][DevtoolsMemoryProblems101ObjectsRetainingTree].</span></span>  

## <span data-ttu-id="24e15-108">Prendre un cliché</span><span class="sxs-lookup"><span data-stu-id="24e15-108">Take a snapshot</span></span>  

<span data-ttu-id="24e15-109">Dans le panneau **mémoire** , sélectionnez **prendre une photo**, puis cliquez sur **Démarrer**.</span><span class="sxs-lookup"><span data-stu-id="24e15-109">On the **Memory** panel, choose **Take snapshot**, then click **Start**.</span></span>  <span data-ttu-id="24e15-110">Vous pouvez également appuyer sur `Ctrl` + `E` \ (Windows \) ou `Cmd` + `E` \ (MacOS \).</span><span class="sxs-lookup"><span data-stu-id="24e15-110">You may also press `Ctrl`+`E` \(Windows\) or `Cmd`+`E` \(macOS\).</span></span>  

> ##### <span data-ttu-id="24e15-111">Figure1</span><span class="sxs-lookup"><span data-stu-id="24e15-111">Figure 1</span></span>  
> <span data-ttu-id="24e15-112">Sélectionner type de profil</span><span class="sxs-lookup"><span data-stu-id="24e15-112">Select profiling type</span></span>  
> ![Sélectionner type de profil][ImageProfilingType]  

<span data-ttu-id="24e15-114">Les **captures instantanées** sont initialement stockées dans la mémoire du processus de rendu.</span><span class="sxs-lookup"><span data-stu-id="24e15-114">**Snapshots** are initially stored in the renderer process memory.</span></span>  <span data-ttu-id="24e15-115">Les captures d’écran sont transférées au DevTools à la demande, lorsque vous cliquez sur l’icône de capture d’écran.</span><span class="sxs-lookup"><span data-stu-id="24e15-115">Snapshots are transferred to the DevTools on demand, when you click on the snapshot icon to view it.</span></span>  

<span data-ttu-id="24e15-116">Une fois la capture instantanée chargée dans DevTools et analysée, le numéro sous le titre de l’instantané s’affiche et indique la [taille totale des objets JavaScript accessibles][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="24e15-116">After the snapshot has been loaded into DevTools and has been parsed, the number below the snapshot title appears and shows the [total size of the reachable JavaScript objects][DevtoolsMemoryProblems101ObjectSizes].</span></span>  

> ##### <span data-ttu-id="24e15-117">Figure 2</span><span class="sxs-lookup"><span data-stu-id="24e15-117">Figure 2</span></span>  
> <span data-ttu-id="24e15-118">Taille totale des objets accessibles</span><span class="sxs-lookup"><span data-stu-id="24e15-118">Total size of reachable objects</span></span>  
> ![Taille totale des objets accessibles][ImageTotalSize]  

> [!NOTE]
> <span data-ttu-id="24e15-120">Seuls les objets joignable sont inclus dans les captures d’image.</span><span class="sxs-lookup"><span data-stu-id="24e15-120">Only reachable objects are included in snapshots.</span></span>  <span data-ttu-id="24e15-121">En outre, le fait de prendre un instantané commence toujours par un nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="24e15-121">Also, taking a snapshot always starts with a garbage collection.</span></span>  

## <span data-ttu-id="24e15-122">Effacer des instantanés</span><span class="sxs-lookup"><span data-stu-id="24e15-122">Clear snapshots</span></span>  

<span data-ttu-id="24e15-123">Cliquez sur l’icône **Effacer tous les profils** pour supprimer les snapshots \ (à la fois du devtools et de la mémoire associée au processus de rendu.).</span><span class="sxs-lookup"><span data-stu-id="24e15-123">Click **Clear all profiles** icon to remove snapshots \(both from DevTools and any memory associated with the renderer process\).</span></span>  

> ##### <span data-ttu-id="24e15-124">Figure3</span><span class="sxs-lookup"><span data-stu-id="24e15-124">Figure 3</span></span>  
> <span data-ttu-id="24e15-125">Supprimer des snapshots</span><span class="sxs-lookup"><span data-stu-id="24e15-125">Remove snapshots</span></span>  
> ![Supprimer des snapshots][ImageRemoveSnapshots]  

<span data-ttu-id="24e15-127">La fermeture de la fenêtre DevTools ne supprime pas les profils de la mémoire associée au processus de convertisseur.</span><span class="sxs-lookup"><span data-stu-id="24e15-127">Closing the DevTools window does not delete profiles from the memory associated with the renderer process.</span></span>  <span data-ttu-id="24e15-128">Lors de la réouverture de DevTools, tous les instantanés précédemment exécutés apparaissent dans la liste des instantanés.</span><span class="sxs-lookup"><span data-stu-id="24e15-128">When reopening DevTools, all previously taken snapshots reappear in the list of snapshots.</span></span>  

> [!NOTE]
> <span data-ttu-id="24e15-129">Testez cet exemple d' [objets disséminés][GlitchDevtoolsMemoryExample03] et profilez-le à l’aide du profileur de tas.</span><span class="sxs-lookup"><span data-stu-id="24e15-129">Try out this example of [scattered objects][GlitchDevtoolsMemoryExample03] and profile it using the Heap Profiler.</span></span>  <span data-ttu-id="24e15-130">Vous devez voir un certain nombre d’attributions d’éléments \ (objet \).</span><span class="sxs-lookup"><span data-stu-id="24e15-130">You should see a number of \(object\) item allocations.</span></span>  

## <span data-ttu-id="24e15-131">Afficher des instantanés</span><span class="sxs-lookup"><span data-stu-id="24e15-131">View snapshots</span></span>  

<span data-ttu-id="24e15-132">Affichez les captures d’écran de différentes perspectives pour différentes tâches.</span><span class="sxs-lookup"><span data-stu-id="24e15-132">View snapshots from different perspectives for different tasks.</span></span>  

<span data-ttu-id="24e15-133">**Vue récapitulative** montre les objets regroupés par nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="24e15-133">**Summary view** shows objects grouped by the constructor name.</span></span>  <span data-ttu-id="24e15-134">Vous pouvez l’utiliser pour rechercher les objets \ (et l’utilisation de la mémoire \) en fonction du type de nom de constructeur.</span><span class="sxs-lookup"><span data-stu-id="24e15-134">Use it to hunt down objects \(and the memory use\) based on type grouped by constructor name.</span></span>  <span data-ttu-id="24e15-135">Elle est particulièrement utile pour effectuer **le suivi des fuites DOM**.</span><span class="sxs-lookup"><span data-stu-id="24e15-135">It is particularly helpful for **tracking down DOM leaks**.</span></span>

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

<span data-ttu-id="24e15-136">**Affichage comparaison**.</span><span class="sxs-lookup"><span data-stu-id="24e15-136">**Comparison view**.</span></span>  <span data-ttu-id="24e15-137">Affiche la différence entre deux instantanés.</span><span class="sxs-lookup"><span data-stu-id="24e15-137">Displays the difference between two snapshots.</span></span>  <span data-ttu-id="24e15-138">Utilisez-la pour comparer deux ou plusieurs \ instantanés de mémoire de avant et après une opération.</span><span class="sxs-lookup"><span data-stu-id="24e15-138">Use it to compare two \(or more\) memory snapshots from before and after an operation.</span></span>  <span data-ttu-id="24e15-139">L’examen de la quantité de mémoire et de la mémoire libérée permet de vérifier la présence et la cause d’une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="24e15-139">Inspecting the delta in freed memory and reference count lets you confirm the presence and cause of a memory leak.</span></span>  

<span data-ttu-id="24e15-140">**Affichage contenant**.</span><span class="sxs-lookup"><span data-stu-id="24e15-140">**Containment view**.</span></span>  <span data-ttu-id="24e15-141">Autorise l’exploration du contenu du tas.</span><span class="sxs-lookup"><span data-stu-id="24e15-141">Allows exploration of heap contents.</span></span>  <span data-ttu-id="24e15-142">Le **mode** de conservation fournit une meilleure vue de la structure de l’objet, facilitant l’analyse des objets référencés dans l’espace de noms global \ (fenêtre \) pour découvrir ce qu’ils conservent.</span><span class="sxs-lookup"><span data-stu-id="24e15-142">**Containment view** provides a better view of object structure, helping analyze objects referenced in the global namespace \(window\) to find out what is keeping objects around.</span></span>  <span data-ttu-id="24e15-143">Utilisez-le pour analyser les fermetures et explorer vos objets à un niveau faible.</span><span class="sxs-lookup"><span data-stu-id="24e15-143">Use it to analyze closures and dive into your objects at a low level.</span></span>  

<span data-ttu-id="24e15-144">Pour basculer entre les affichages, utilisez le sélecteur en haut de la vue.</span><span class="sxs-lookup"><span data-stu-id="24e15-144">To switch between views, use the selector at the top of the view.</span></span>  

> ##### <span data-ttu-id="24e15-145">Figure 4</span><span class="sxs-lookup"><span data-stu-id="24e15-145">Figure 4</span></span>  
> <span data-ttu-id="24e15-146">Changer de sélecteur de vues</span><span class="sxs-lookup"><span data-stu-id="24e15-146">Switch views selector</span></span>  
> ![Changer de sélecteur de vues][ImageSwitchViews]  

> [!NOTE]
> <span data-ttu-id="24e15-148">Toutes les propriétés ne sont pas stockées dans le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24e15-148">Not all properties are stored on the JavaScript heap.</span></span>  <span data-ttu-id="24e15-149">Les propriétés implémentées à l’aide d’accesseurs qui exécutent du code natif ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="24e15-149">Properties implemented using getters that run native code are not captured.</span></span>  <span data-ttu-id="24e15-150">Par ailleurs, les valeurs qui ne sont pas des chaînes telles que des nombres ne sont pas capturées.</span><span class="sxs-lookup"><span data-stu-id="24e15-150">Also, non-string values such as numbers are not captured.</span></span>  

### <span data-ttu-id="24e15-151">Affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="24e15-151">Summary view</span></span>  

<span data-ttu-id="24e15-152">À l’origine, une capture d’écran s’ouvre dans l’affichage de synthèse et affiche les totaux d’objets, qui risquent d’être développés pour afficher les instances:</span><span class="sxs-lookup"><span data-stu-id="24e15-152">Initially, a snapshot opens in the Summary view, displaying object totals, which may be expanded to show instances:</span></span>  

> ##### <span data-ttu-id="24e15-153">Figure 5</span><span class="sxs-lookup"><span data-stu-id="24e15-153">Figure 5</span></span>  
> <span data-ttu-id="24e15-154">Affichage de synthèse</span><span class="sxs-lookup"><span data-stu-id="24e15-154">Summary view</span></span>  
> ![Affichage de synthèse][ImageSummaryView]  

<span data-ttu-id="24e15-156">Les entrées de niveau supérieur correspondent à des lignes «total».</span><span class="sxs-lookup"><span data-stu-id="24e15-156">Top-level entries are "total" lines.</span></span>  

| <span data-ttu-id="24e15-157">Entrées de niveau supérieur</span><span class="sxs-lookup"><span data-stu-id="24e15-157">Top-level entries</span></span> | <span data-ttu-id="24e15-158">Description</span><span class="sxs-lookup"><span data-stu-id="24e15-158">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="24e15-159">Constructeur</span><span class="sxs-lookup"><span data-stu-id="24e15-159">Constructor</span></span>** | <span data-ttu-id="24e15-160">Représente tous les objets créés à l’aide de ce constructeur.</span><span class="sxs-lookup"><span data-stu-id="24e15-160">Represents all objects created using this constructor.</span></span>  |  
| **<span data-ttu-id="24e15-161">Distance</span><span class="sxs-lookup"><span data-stu-id="24e15-161">Distance</span></span>** | <span data-ttu-id="24e15-162">affiche la distance à la racine en utilisant le chemin de nœud simple le plus court.</span><span class="sxs-lookup"><span data-stu-id="24e15-162">displays the distance to the root using the shortest simple path of nodes.</span></span>  |  
| **<span data-ttu-id="24e15-163">Taille superficielle</span><span class="sxs-lookup"><span data-stu-id="24e15-163">Shallow size</span></span>** | <span data-ttu-id="24e15-164">Affiche la somme de tailles superficielles de tous les objets créés par une certaine fonction Constructor.</span><span class="sxs-lookup"><span data-stu-id="24e15-164">Displays the sum of shallow sizes of all objects created by a certain constructor function.</span></span>  <span data-ttu-id="24e15-165">La taille superficielle correspond à la taille de la mémoire maintenue par un objet \ (en général, les tableaux et les chaînes ont des tailles superficielles plus grandes».</span><span class="sxs-lookup"><span data-stu-id="24e15-165">The shallow size is the size of memory held by an object \(generally, arrays and strings have larger shallow sizes\).</span></span>  <span data-ttu-id="24e15-166">Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="24e15-166">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  
| **<span data-ttu-id="24e15-167">Taille retenue</span><span class="sxs-lookup"><span data-stu-id="24e15-167">Retained size</span></span>** | <span data-ttu-id="24e15-168">Affiche la taille maximale conservée entre le même jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="24e15-168">Displays the maximum retained size among the same set of objects.</span></span>  <span data-ttu-id="24e15-169">La taille de mémoire que vous pouvez libérer après la suppression d’un objet (et les dépendants n’est plus joignable \) est appelée taille retenue.</span><span class="sxs-lookup"><span data-stu-id="24e15-169">The size of memory that you are able to free after an object is deleted \(and the dependents are made no longer reachable\) is called the retained size.</span></span>  <span data-ttu-id="24e15-170">Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].</span><span class="sxs-lookup"><span data-stu-id="24e15-170">See also [Object sizes][DevtoolsMemoryProblems101ObjectSizes].</span></span>  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

<span data-ttu-id="24e15-171">Après avoir étendu une ligne du total dans l’affichage supérieur, toutes les instances sont affichées.</span><span class="sxs-lookup"><span data-stu-id="24e15-171">After expanding a total line in the upper view, all of the instances are displayed.</span></span>  <span data-ttu-id="24e15-172">Pour chaque instance, les tailles superficielle et retenue sont affichées dans les colonnes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="24e15-172">For each instance, the shallow and retained sizes are displayed in the corresponding columns.</span></span>  <span data-ttu-id="24e15-173">Le nombre après le `@` caractère est l’identificateur unique de l’objet, ce qui vous permet de comparer les instantanés de tas en fonction de chaque objet.</span><span class="sxs-lookup"><span data-stu-id="24e15-173">The number after the `@` character is the unique ID of the object, allowing you to compare heap snapshots on per-object basis.</span></span>  

<span data-ttu-id="24e15-174">N’oubliez pas que les objets jaunes possèdent des références JavaScript et des objets rouges sont des nœuds détachés qui sont référencés à partir d’un arrière-plan jaune.</span><span class="sxs-lookup"><span data-stu-id="24e15-174">Remember that yellow objects have JavaScript references and red objects are detached nodes which are referenced from one with a yellow background.</span></span>  

**<span data-ttu-id="24e15-175">À quoi correspondent les différentes entrées de Constructor (Group \) dans le générateur de mémoire de segment?</span><span class="sxs-lookup"><span data-stu-id="24e15-175">What do the various constructor \(group\) entries in the Heap profiler correspond to?</span></span>**  

> ##### <span data-ttu-id="24e15-176">Figure 6</span><span class="sxs-lookup"><span data-stu-id="24e15-176">Figure 6</span></span>  
> <span data-ttu-id="24e15-177">Groupes de constructeurs</span><span class="sxs-lookup"><span data-stu-id="24e15-177">Constructor groups</span></span>  
> ![Groupes de constructeurs][ImageConstructorGroups]  

| <span data-ttu-id="24e15-179">Entrée Constructor (groupe \)</span><span class="sxs-lookup"><span data-stu-id="24e15-179">Constructor \(group\) entry</span></span> | <span data-ttu-id="24e15-180">Description</span><span class="sxs-lookup"><span data-stu-id="24e15-180">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="24e15-181">\ (propriété globale \)</span><span class="sxs-lookup"><span data-stu-id="24e15-181">\(global property\)</span></span>** | <span data-ttu-id="24e15-182">Objets intermédiaires entre un objet global \ (par exemple, `window` \) et un objet référencé par celui-ci.</span><span class="sxs-lookup"><span data-stu-id="24e15-182">The intermediate objects between a global object \(like `window`\) and an object referenced by it.</span></span>  <span data-ttu-id="24e15-183">Si un objet est créé à l’aide d’un constructeur `Person` et est maintenu par un objet global, le chemin d’accès de conservation ressemble à ceci `[global] > \(global property\) > Person` .</span><span class="sxs-lookup"><span data-stu-id="24e15-183">If an object is created using a constructor `Person` and is held by a global object, the retaining path would look like `[global] > \(global property\) > Person`.</span></span>  <span data-ttu-id="24e15-184">Cela contraste avec la norme, où les objets se référencent directement.</span><span class="sxs-lookup"><span data-stu-id="24e15-184">This contrasts with the norm, where objects directly reference each other.</span></span>  <span data-ttu-id="24e15-185">Il existe des objets intermédiaires pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="24e15-185">Intermediate objects exist for performance reasons.</span></span>  <span data-ttu-id="24e15-186">Les éléments globaux sont modifiés régulièrement et les optimisations d’accès aux propriétés font l’objet d’un bon travail pour les objets non globaux et ne s’applique pas aux globales.</span><span class="sxs-lookup"><span data-stu-id="24e15-186">Globals are modified regularly and property access optimizations do a good job for non-global objects are not applicable for globals.</span></span>  |  
| **<span data-ttu-id="24e15-187">\ (racines \)</span><span class="sxs-lookup"><span data-stu-id="24e15-187">\(roots\)</span></span>** | <span data-ttu-id="24e15-188">Les entrées racines dans l’arborescence conservation sont les entités qui contiennent des références à l’objet sélectionné.</span><span class="sxs-lookup"><span data-stu-id="24e15-188">The root entries in the retaining tree view are the entities that have references to the selected object.</span></span>  <span data-ttu-id="24e15-189">Les entrées pourront également être des références créées par le moteur pour des raisons spécifiques au moteur.</span><span class="sxs-lookup"><span data-stu-id="24e15-189">The entries may also be references created by the engine for engine-specific purposes.</span></span>  <span data-ttu-id="24e15-190">Le moteur comporte des mises en cache qui font référence aux objets, mais ces références sont faibles et n’empêchent pas la collecte d’un objet en raison de l’absence de références réellement fortes.</span><span class="sxs-lookup"><span data-stu-id="24e15-190">The engine has caches which reference objects, but all such references are weak and do not prevent an object from being collected given that there are no truly strong references.</span></span>  |  
| **<span data-ttu-id="24e15-191">\ (fermeture \)</span><span class="sxs-lookup"><span data-stu-id="24e15-191">\(closure\)</span></span>** | <span data-ttu-id="24e15-192">Nombre de références à un groupe d’objets par le biais de la fermeture de fonction.</span><span class="sxs-lookup"><span data-stu-id="24e15-192">A count of references to a group of objects through function closures.</span></span>  |  
| **<span data-ttu-id="24e15-193">\ (matrice, chaîne, nombre, RegExp \)</span><span class="sxs-lookup"><span data-stu-id="24e15-193">\(array, string, number, regexp\)</span></span>** | <span data-ttu-id="24e15-194">Liste de types d’objets avec des propriétés qui font référence à un tableau, une chaîne, un nombre ou une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="24e15-194">A list of object types with properties which reference an Array, String, Number, or regular expression.</span></span>  |  
| **<span data-ttu-id="24e15-195">\ (code compilé \)</span><span class="sxs-lookup"><span data-stu-id="24e15-195">\(compiled code\)</span></span>** | <span data-ttu-id="24e15-196">Tout ce qui concerne le code compilé.</span><span class="sxs-lookup"><span data-stu-id="24e15-196">Everything related to compiled code.</span></span>  <span data-ttu-id="24e15-197">Le script est semblable à une fonction, mais correspond à un `<script>` corps.</span><span class="sxs-lookup"><span data-stu-id="24e15-197">Script is similar to a function, but corresponds to a `<script>` body.</span></span>  <span data-ttu-id="24e15-198">SharedFunctionInfos \ (SFI \) les objets se trouvent dans les fonctions et dans le code compilé.</span><span class="sxs-lookup"><span data-stu-id="24e15-198">SharedFunctionInfos \(SFI\) are objects standing between functions and compiled code.</span></span>  <span data-ttu-id="24e15-199">Les fonctions disposent généralement d’un contexte, même si SFIs.</span><span class="sxs-lookup"><span data-stu-id="24e15-199">Functions usually have a context, while SFIs do not.</span></span>  |  
| <span data-ttu-id="24e15-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, etc.</span><span class="sxs-lookup"><span data-stu-id="24e15-200">**HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, and so on.</span></span>  | <span data-ttu-id="24e15-201">Fait référence à des éléments ou des objets document d’un type particulier référencé par votre code.</span><span class="sxs-lookup"><span data-stu-id="24e15-201">References to elements or document objects of a particular type referenced by your code.</span></span>  |  

<!--todo: add heap profiling summary section when available -->  

### <span data-ttu-id="24e15-202">Affichage comparaison</span><span class="sxs-lookup"><span data-stu-id="24e15-202">Comparison view</span></span>  

<span data-ttu-id="24e15-203">Recherchez les objets perdus en comparant plusieurs instantanés entre eux.</span><span class="sxs-lookup"><span data-stu-id="24e15-203">Find leaked objects by comparing multiple snapshots to each other.</span></span>  <span data-ttu-id="24e15-204">Pour vérifier que l’opération d’une certaine application ne crée pas de fuites (par exemple, une paire d’opérations directes ou inverses, telles que l’ouverture d’un document, puis la fermeture, ne doit pas laisser de place à un autre), vous pouvez suivre le scénario suivant:</span><span class="sxs-lookup"><span data-stu-id="24e15-204">To verify that a certain application operation does not create leaks \(for example, usually a pair of direct and reverse operations, like opening a document, and then closing it, should not leave any garbage\), you may follow the scenario below:</span></span>  

1.  <span data-ttu-id="24e15-205">Prenez un instantané de tas avant d’exécuter une opération.</span><span class="sxs-lookup"><span data-stu-id="24e15-205">Take a heap snapshot before performing an operation.</span></span>  
1.  <span data-ttu-id="24e15-206">Effectuer une opération \ (interagissez avec une page d’une manière que vous pensez être à l’origine d’une fuite \).</span><span class="sxs-lookup"><span data-stu-id="24e15-206">Perform an operation \(interact with a page in some way that you believe to be causing a leak\).</span></span>  
1.  <span data-ttu-id="24e15-207">Effectuez une opération inverse \ (faites l’interaction inverse et répétez-la quelques fois...).</span><span class="sxs-lookup"><span data-stu-id="24e15-207">Perform a reverse operation \(do the opposite interaction and repeat it a few times\).</span></span>  
1.  <span data-ttu-id="24e15-208">Prenez un second instantané de tas et changez le mode d’affichage de celui-ci en **comparaison**, en le comparant à **snapshot 1**.</span><span class="sxs-lookup"><span data-stu-id="24e15-208">Take a second heap snapshot and change the view of this one to **Comparison**, comparing it to **Snapshot 1**.</span></span>  

<span data-ttu-id="24e15-209">Dans l’affichage **comparaison** , la différence entre les deux instantanés s’affiche.</span><span class="sxs-lookup"><span data-stu-id="24e15-209">In the **Comparison** view, the difference between two snapshots is displayed.</span></span>  <span data-ttu-id="24e15-210">Lorsque vous développez une entrée de total, des instances d’objet ajoutées et supprimées sont affichées.</span><span class="sxs-lookup"><span data-stu-id="24e15-210">When expanding a total entry, added and deleted object instances are shown.</span></span>  

> ##### <span data-ttu-id="24e15-211">Figure 7</span><span class="sxs-lookup"><span data-stu-id="24e15-211">Figure 7</span></span>  
> <span data-ttu-id="24e15-212">Affichage comparaison</span><span class="sxs-lookup"><span data-stu-id="24e15-212">Comparison view</span></span>  
> ![Affichage comparaison][ImageComparisonView]  

<!--todo: add HeapProfilingComparison section when available  -->  

### <span data-ttu-id="24e15-214">Affichage contenant</span><span class="sxs-lookup"><span data-stu-id="24e15-214">Containment view</span></span>  

<span data-ttu-id="24e15-215">Le mode de **confinement** est essentiellement une vue aérienne de la structure Objects de votre application.</span><span class="sxs-lookup"><span data-stu-id="24e15-215">The **Containment** view is essentially a "bird's eye view" of the objects structure of your application.</span></span>  <span data-ttu-id="24e15-216">Elle vous permet de lire dans les fermetures de fonctions, d’observer les objets internes de machine virtuelle \ (VM \) qui constituent vos objets JavaScript et de comprendre la quantité de mémoire utilisée par votre application à un niveau très bas.</span><span class="sxs-lookup"><span data-stu-id="24e15-216">It allows you to peek inside function closures, to observe virtual machine \(VM\) internal objects that together make up your JavaScript objects, and to understand how much memory your application uses at a very low level.</span></span>  

| <span data-ttu-id="24e15-217">Points d’entrée du mode contenant</span><span class="sxs-lookup"><span data-stu-id="24e15-217">Containment view entry points</span></span> | <span data-ttu-id="24e15-218">Description</span><span class="sxs-lookup"><span data-stu-id="24e15-218">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="24e15-219">Objets DOMWindow</span><span class="sxs-lookup"><span data-stu-id="24e15-219">DOMWindow objects</span></span>** | <span data-ttu-id="24e15-220">Objets globaux pour le code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24e15-220">Global objects for JavaScript code.</span></span>  |  
| **<span data-ttu-id="24e15-221">Racines GC</span><span class="sxs-lookup"><span data-stu-id="24e15-221">GC roots</span></span>** | <span data-ttu-id="24e15-222">Les racines du GC réel utilisées par le nettoyage de la mémoire virtuelle.</span><span class="sxs-lookup"><span data-stu-id="24e15-222">The actual GC roots used by the garbage of the VM.</span></span>  <span data-ttu-id="24e15-223">Les racines de catalogue global sont composées de cartes d’objets intégrés, de tableaux de symboles, de piles de threads d’ordinateur de construction, de caches de compilation, de gestionnaires d’étendues et de descripteurs globaux.</span><span class="sxs-lookup"><span data-stu-id="24e15-223">GC roots are comprised of built-in object maps, symbol tables, VM thread stacks, compilation caches, handle scopes, and global handles.</span></span>  |  
| **<span data-ttu-id="24e15-224">Objets natifs</span><span class="sxs-lookup"><span data-stu-id="24e15-224">Native objects</span></span>** | <span data-ttu-id="24e15-225">Objets de navigateur «Push» à l’intérieur de la machine virtuelle JavaScript (VM) pour autoriser l’automatisation (par exemple, les nœuds DOM et les règles CSS).</span><span class="sxs-lookup"><span data-stu-id="24e15-225">Browser objects "pushed" inside the JavaScript virtual machine \(JavaScript VM\) to allow automation, for example, DOM nodes, CSS rules.</span></span>  |  

> ##### <span data-ttu-id="24e15-226">Figure8</span><span class="sxs-lookup"><span data-stu-id="24e15-226">Figure 8</span></span>  
> <span data-ttu-id="24e15-227">Affichage contenant</span><span class="sxs-lookup"><span data-stu-id="24e15-227">Containment view</span></span>  
> ![Affichage contenant][ImageContainmentView]  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> <span data-ttu-id="24e15-229">Astuce sur les fermetures.</span><span class="sxs-lookup"><span data-stu-id="24e15-229">A tip about closures.</span></span>  <span data-ttu-id="24e15-230">Nommez les fonctions pour pouvoir distinguer facilement les fermetures de l’instantané.</span><span class="sxs-lookup"><span data-stu-id="24e15-230">Name the functions so you are able to easily distinguish between closures in the snapshot.</span></span>  <span data-ttu-id="24e15-231">Par exemple, cet exemple n’utilise pas de fonctions nommées.</span><span class="sxs-lookup"><span data-stu-id="24e15-231">For example, this example does not use named functions.</span></span>  
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
> <span data-ttu-id="24e15-232">Cet exemple utilise des fonctions nommées:</span><span class="sxs-lookup"><span data-stu-id="24e15-232">This example uses named functions:</span></span>  
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
> > ##### old Figure 9  
> > Name functions to distinguish between closures  
> > ![Name functions to distinguish between closures][ImageDomLeaks]  
> -->  
> 
> > [!NOTE]
> > <span data-ttu-id="24e15-233">Essayez cet exemple pour savoir [pourquoi `eval` ][GlitchDevtoolsMemoryExample07] un élément malveillant analyse l’impact de la fermeture sur la mémoire.</span><span class="sxs-lookup"><span data-stu-id="24e15-233">Try out this example of [why `eval` is evil][GlitchDevtoolsMemoryExample07] to analyze the impact of closures on memory.</span></span>  <span data-ttu-id="24e15-234">Vous serez peut-être également intéressé par le suivi de cet exemple qui vous permet d’accéder à des [allocations de tas][GlitchDevtoolsMemoryExample08]d’enregistrements.</span><span class="sxs-lookup"><span data-stu-id="24e15-234">You may also be interested in following it up with this example that takes you through recording [heap allocations][GlitchDevtoolsMemoryExample08].</span></span>  
> 

## <span data-ttu-id="24e15-235">Chercher un codage en couleurs</span><span class="sxs-lookup"><span data-stu-id="24e15-235">Look up color coding</span></span>  

<span data-ttu-id="24e15-236">Les propriétés et valeurs de propriété des objets ont des types différents et sont en conséquence.</span><span class="sxs-lookup"><span data-stu-id="24e15-236">Properties and property values of objects have different types and are colored accordingly.</span></span>  <span data-ttu-id="24e15-237">Chaque propriété comporte l’un des quatre types suivants.</span><span class="sxs-lookup"><span data-stu-id="24e15-237">Each property has one of four types.</span></span>  

| <span data-ttu-id="24e15-238">Type de propriété</span><span class="sxs-lookup"><span data-stu-id="24e15-238">Property Type</span></span> | <span data-ttu-id="24e15-239">Description</span><span class="sxs-lookup"><span data-stu-id="24e15-239">Description</span></span> |  
|:--- |:--- |  
| **<span data-ttu-id="24e15-240">a: propriété</span><span class="sxs-lookup"><span data-stu-id="24e15-240">a: property</span></span>** | <span data-ttu-id="24e15-241">Propriété standard avec un nom, accessible par le biais de l' `.` opérateur \ (point \) ou par le biais `[` `]` de la notation \ (crochets \), par exemple `["foo bar"]` .</span><span class="sxs-lookup"><span data-stu-id="24e15-241">A regular property with a name, accessed via the `.` \(dot\) operator, or via `[` `]` \(brackets\) notation, for example `["foo bar"]`.</span></span>  |  
| **<span data-ttu-id="24e15-242">0: élément</span><span class="sxs-lookup"><span data-stu-id="24e15-242">0: element</span></span>** | <span data-ttu-id="24e15-243">Propriété standard avec un index numérique, accessible via la `[` `]` notation \ (crochets \).</span><span class="sxs-lookup"><span data-stu-id="24e15-243">A regular property with a numeric index, accessed via `[` `]` \(brackets\) notation.</span></span>  |  
| **<span data-ttu-id="24e15-244">a: var du contexte</span><span class="sxs-lookup"><span data-stu-id="24e15-244">a: context var</span></span>** |  <span data-ttu-id="24e15-245">Variable dans un contexte de fonction, accessible par le nom de la variable à partir de la fermeture d’une fonction.</span><span class="sxs-lookup"><span data-stu-id="24e15-245">A variable in a function context, accessible by the variable name from inside a function closure.</span></span>  |  
| **<span data-ttu-id="24e15-246">a: système prop</span><span class="sxs-lookup"><span data-stu-id="24e15-246">a: system prop</span></span>** | <span data-ttu-id="24e15-247">Propriété ajoutée par le VM JavaScript, qui n’est pas accessible à partir du code JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24e15-247">A property added by the JavaScript VM, not accessible from JavaScript code.</span></span>  |  

<span data-ttu-id="24e15-248">Les objets désignés comme `System` ne disposant pas d’un type JavaScript correspondant;</span><span class="sxs-lookup"><span data-stu-id="24e15-248">Objects designated as `System` do not have a corresponding JavaScript type.</span></span>  <span data-ttu-id="24e15-249">Chacun fait partie de l’implémentation du système d’objets de la machine virtuelle JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24e15-249">Each is part of the object system implementation of the Javascript VM.</span></span>  <span data-ttu-id="24e15-250">V8 alloue la plupart des objets internes dans le même segment de mémoire que les objets JS de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="24e15-250">V8 allocates most of the internal objects in the same heap as the user's JS objects.</span></span>  <span data-ttu-id="24e15-251">C’est alors que les éléments internes sont uniquement en interne.</span><span class="sxs-lookup"><span data-stu-id="24e15-251">So these are just V8 internals.</span></span>  

## <span data-ttu-id="24e15-252">Rechercher un objet spécifique</span><span class="sxs-lookup"><span data-stu-id="24e15-252">Find a specific object</span></span>  

<span data-ttu-id="24e15-253">Pour rechercher un objet dans le tas collecté, vous pouvez effectuer une recherche sur l’ID de l' `Ctrl` + `F` objet.</span><span class="sxs-lookup"><span data-stu-id="24e15-253">To find an object in the collected heap you may search using `Ctrl`+`F` and give the object ID.</span></span>  

## <span data-ttu-id="24e15-254">Découvrir les fuites DOM</span><span class="sxs-lookup"><span data-stu-id="24e15-254">Uncover DOM leaks</span></span>  

<span data-ttu-id="24e15-255">Le profileur de tas a la possibilité de répercuter les dépendances bidirectionnelles entre les objets natifs du navigateur (nœud DOM, règles CSS \) et objets JavaScript.</span><span class="sxs-lookup"><span data-stu-id="24e15-255">The heap profiler has the ability to reflect bidirectional dependencies between browser native objects \(DOM nodes, CSS rules\) and JavaScript objects.</span></span>
<span data-ttu-id="24e15-256">Cela permet de détecter d’éventuelles fuites de fuite en raison de l’oubli d’arborescences DOM dissociées.</span><span class="sxs-lookup"><span data-stu-id="24e15-256">This helps to discover otherwise invisible leaks happening due to forgotten detached DOM subtrees floating around.</span></span>  

<span data-ttu-id="24e15-257">Les fuites DOM risquent d’être plus grandes que vous ne le pensez.</span><span class="sxs-lookup"><span data-stu-id="24e15-257">DOM leaks may be bigger than you think.</span></span>  <span data-ttu-id="24e15-258">Prenons l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="24e15-258">Consider the following sample.</span></span>  <span data-ttu-id="24e15-259">Quand est-ce que le CG #tree?</span><span class="sxs-lookup"><span data-stu-id="24e15-259">When is the #tree GC?</span></span>  

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

<span data-ttu-id="24e15-260">Le `#leaf` maintien d’une référence au parent approprié \ (ParentNode \) et de manière récurrente jusqu’à ce que le `#tree` leafRef soit annulé comme l’arborescence entière sous `#tree` un candidat pour le CG.</span><span class="sxs-lookup"><span data-stu-id="24e15-260">The `#leaf` maintains a reference to the relevant parent \(parentNode\) and recursively up to `#tree`, so only when leafRef is nullified is the WHOLE tree under `#tree` a candidate for GC.</span></span>  

> ##### <span data-ttu-id="24e15-261">Figure9</span><span class="sxs-lookup"><span data-stu-id="24e15-261">Figure 9</span></span>  
> <span data-ttu-id="24e15-262">Sous-arbres DOM</span><span class="sxs-lookup"><span data-stu-id="24e15-262">DOM subtrees</span></span>  
> <span data-ttu-id="24e15-263">! [Sous-arbres DOM] [ImageTreeGc]</span><span class="sxs-lookup"><span data-stu-id="24e15-263">![DOM subtrees][ImageTreeGc]</span></span>  

> [!NOTE]
> <span data-ttu-id="24e15-264">Exemples: Essayez cet exemple de [nœud DOM en fuite][GlitchDevtoolsMemoryExample06] pour savoir où il est susceptible de fuir et comment le détecter.</span><span class="sxs-lookup"><span data-stu-id="24e15-264">Examples:  Try this example of a [leaking DOM node][GlitchDevtoolsMemoryExample06] to understand where it may leak and how to detect it.</span></span>  <span data-ttu-id="24e15-265">Vous pouvez également examiner cet exemple de [fuites DOM plus grandes que prévu][GlitchDevtoolsMemoryExample09].</span><span class="sxs-lookup"><span data-stu-id="24e15-265">You may also look at this example of [DOM leaks being bigger than expected][GlitchDevtoolsMemoryExample09].</span></span>  

<span data-ttu-id="24e15-266">Pour en savoir plus sur les fuites DOM et l’analyse en mémoire notions fondamentales sur [la recherche et le débogage de fuites de mémoire avec Microsoft Edge devtools][GonzaloRuizdeVillaMemory] par Gonzalo Ruiz de Villa.</span><span class="sxs-lookup"><span data-stu-id="24e15-266">To read more about DOM leaks and memory analysis fundamentals checkout [Finding and debugging memory leaks with the Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] by Gonzalo Ruiz de Villa.</span></span>  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

<!--## Feedback   -->  



<!-- image links -->  

[ImageProfilingType]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png "Figure 1: sélectionner le type de profilage"  
[ImageTotalSize]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png "Figure 2: taille totale des objets accessibles"  
[ImageRemoveSnapshots]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png "Figure 3: supprimer des snapshots"  
[ImageSwitchViews]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png "Figure 4: sélecteur de vues basculer"  
[ImageSummaryView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png "Figure 5: vue de synthèse"  
[ImageConstructorGroups]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png "Figure 6: groupes de constructeurs"  
[ImageComparisonView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png "Figure 7: mode comparaison"  
[ImageContainmentView]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png "Figure 8: affichage contenant"  
<!--[ImageDomLeaks]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-domleaks.msft.png "old Figure 9: Name functions to distinguish between closures"  -->  
[ImageTreeGc]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Memory-Problems-Tree-gc.msft.png "figure 9: sous-arbres DOM"  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#object-sizes "Tailles d’objets-terminologie utilisée par la mémoire"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: /microsoft-edge/devtools-guide-chromium/memory-problems/memory-101#objects-retaining-tree "Objets qui conservent une terminologie en mémoire d’arborescence"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "Example-03. html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "Example-06. html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "Example-07. html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "Example-08. html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "Example-09. html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "Example-10. html-Microsoft Edge (chrome) DevTools | Problème"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "mémoire | Diapo"  

> [!NOTE]
> <span data-ttu-id="24e15-285">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="24e15-285">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="24e15-286">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="24e15-286">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="24e15-288">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="24e15-288">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
