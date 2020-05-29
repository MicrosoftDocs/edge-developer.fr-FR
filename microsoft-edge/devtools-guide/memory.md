---
description: Utilisez le volet mémoire pour
title: DevTools-Memory
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, mémoire, tas, CG, nettoyage de la mémoire, taille retenue, Dominators
ms.custom: seodec18
ms.openlocfilehash: 416ba144f7e22bd50f5d2a3437bc21d9d31a9035
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565543"
---
# <span data-ttu-id="509fc-104">Mémoire</span><span class="sxs-lookup"><span data-stu-id="509fc-104">Memory</span></span>

<span data-ttu-id="509fc-105">Utilisez le volet **mémoire** pour mesurer votre utilisation des ressources système et comparer des instantanés de tas à différents États de l’exécution du code.</span><span class="sxs-lookup"><span data-stu-id="509fc-105">Use the **Memory** panel to measure your use of system resources and compare heap snapshots at different states of code execution.</span></span> <span data-ttu-id="509fc-106">Avec ce service, vous pouvez:</span><span class="sxs-lookup"><span data-stu-id="509fc-106">With it, you can:</span></span>

- <span data-ttu-id="509fc-107">[Courbez la consommation de mémoire de votre page en temps réel](#memory-usage-timeline) et prenez des instantanés du tas.</span><span class="sxs-lookup"><span data-stu-id="509fc-107">[Graph the memory consumption of your page in real time](#memory-usage-timeline) and take snapshots of the heap</span></span>
- <span data-ttu-id="509fc-108">[Identifier les problèmes de mémoire potentiels](#snapshot-summary) dans votre code, tels que les objets conservés non attachés au DOM</span><span class="sxs-lookup"><span data-stu-id="509fc-108">[Identify potential memory issues](#snapshot-summary) in your code, such as retained objects not attached to the DOM</span></span>
- <span data-ttu-id="509fc-109">[Examiner les données d’utilisation](#snapshot-details) de la mémoire par type d’objet, nombre d’instances, taille et références pour vous aider à isoler les problèmes</span><span class="sxs-lookup"><span data-stu-id="509fc-109">[Review memory usage data](#snapshot-details) by object type, instance count, size, and references to help isolate issues</span></span>
- <span data-ttu-id="509fc-110">[Appliquer des filtres de données de capture instantanée](#filters) pour réduire le bruit lié aux informations non exploitables</span><span class="sxs-lookup"><span data-stu-id="509fc-110">[Apply snapshot data filters](#filters) to reduce the noise of non-actionable information</span></span>
- <span data-ttu-id="509fc-111">[Identifier le coût de mémoire d’un objet spécifique](#object-references) et les références le laissant actif</span><span class="sxs-lookup"><span data-stu-id="509fc-111">[Identify the memory cost of a specific object](#object-references) and the references keeping it alive</span></span>
- <span data-ttu-id="509fc-112">[Différenciez le tas à différentes phases de votre examen](#snapshot-comparison) pour détecter la source de fuites de mémoire et autres problèmes.</span><span class="sxs-lookup"><span data-stu-id="509fc-112">[Diff the heap at different phases of your investigation](#snapshot-comparison) to track down the source of memory leaks and other problems</span></span>

![Panneau mémoire de Microsoft Edge DevTools](./media/memory.png)


## <span data-ttu-id="509fc-114">ToolBar</span><span class="sxs-lookup"><span data-stu-id="509fc-114">Toolbar</span></span>

1. <span data-ttu-id="509fc-115">**Démarrer/arrêter la session de profil (Ctrl + E)**: l’activation du profileur vous permet d’effectuer le suivi de l’utilisation de la mémoire et de prendre des instantanés du tas.</span><span class="sxs-lookup"><span data-stu-id="509fc-115">**Start/Stop profiling session (Ctrl+E)**: Turning on the profiler enables you to track memory usage and take snapshots of the heap.</span></span>
2. <span data-ttu-id="509fc-116">**Importer une session de profil (Ctrl + O)**: charger une session de diagnostic de mémoire de devtools enregistrée.</span><span class="sxs-lookup"><span data-stu-id="509fc-116">**Import profiling session (Ctrl+O)**: Load a saved  DevTools memory diagnostic session.</span></span>
3. <span data-ttu-id="509fc-117">**Exporter la session de profil (Ctrl + S)**: enregistrez la session de diagnostic actuelle sur le disque.</span><span class="sxs-lookup"><span data-stu-id="509fc-117">**Export profiling session (Ctrl+S)**: Save the current diagnostic session to disk.</span></span>
4. <span data-ttu-id="509fc-118">**Utiliser l’instantané de segment de mémoire (Ctrl + Maj + T)**: enregistrer les attributions de mémoire actuelles pour un moment donné.</span><span class="sxs-lookup"><span data-stu-id="509fc-118">**Take heap snapshot (Ctrl+Shift+T)**: Record current memory allocations for a given point of time.</span></span>


## <span data-ttu-id="509fc-119">Chronologie de l’utilisation de la mémoire</span><span class="sxs-lookup"><span data-stu-id="509fc-119">Memory usage timeline</span></span>

<span data-ttu-id="509fc-120">Les problèmes de mémoire peuvent entraîner des problèmes de performances importants, ce qui amène votre page à devenir de plus en plus réactive et à laggyr au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="509fc-120">Memory problems can be a major culprit of performance issues, causing your page to become increasingly unresponsive and laggy over time.</span></span>

<span data-ttu-id="509fc-121">La première étape de l’analyse de l’utilisation de la mémoire de votre page consiste à [Démarrer une session de profilage](#toolbar) afin de prendre des instantanés du tas lorsque vous reproduisez les étapes de l’augmentation de la mémoire ou d’une fuite de mémoire suspecte.</span><span class="sxs-lookup"><span data-stu-id="509fc-121">The first step to analyzing the memory usage of your page is to [start a profiling session](#toolbar) in order to take before/after snapshots of the heap as you repro the steps causing memory bloat or a suspected memory leak.</span></span>

<span data-ttu-id="509fc-122">Lorsque vous démarrez le profileur de mémoire, vous verrez un graphique de mémoire de processus qui vous permet d’observer la plage de travail privée globale (quantité de mémoire consommée par la page) au fil du temps.</span><span class="sxs-lookup"><span data-stu-id="509fc-122">When you start the memory profiler, you will see a process memory graph that allows you to observe the overall private working set (the amount of memory consumed by the page) over time.</span></span> <span data-ttu-id="509fc-123">Le graphique mémoire montre une vue en direct de la mémoire de processus de l’onglet, qui inclut les octets privés, la mémoire native et le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="509fc-123">The memory graph shows you a live view of the tab's process memory, which includes private bytes, native memory, and the JavaScript heap.</span></span> 

![Chronologie de l’utilisation de la mémoire](./media/memory_timeline.png)

 <span data-ttu-id="509fc-125">Le graphique fournit une indication de la tendance de mémoire de la page, qui vous permet de déterminer s’il est approprié de [prendre une capture de segment](#toolbar) de mémoire pour une comparaison ultérieure, par exemple si vous voyez des périodes de rétention de mémoire inattendue.</span><span class="sxs-lookup"><span data-stu-id="509fc-125">The graph gives you an indication of the memory trend for the page which enables you to judge when it is appropriate to [take a heap snapshot](#toolbar) for later comparison, such as when you see periods of unexpected memory retention.</span></span>

### <span data-ttu-id="509fc-126">Performance. Mark ()</span><span class="sxs-lookup"><span data-stu-id="509fc-126">Performance.mark()</span></span>

<span data-ttu-id="509fc-127">Vous pouvez ajouter des **marques d’utilisateur** personnalisées à la chronologie pour faciliter l’identification des événements clés au cours de la session d’analyse en appelant la [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) méthode à partir de votre code ou de la [**console**](./console.md)devtools.</span><span class="sxs-lookup"><span data-stu-id="509fc-127">You can add custom **User marks** to the timeline to help identify  key events during the course of your analysis session by calling the [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) method from within your code or the  DevTools [**Console**](./console.md).</span></span>

### <span data-ttu-id="509fc-128">Console. takeheapSnapshot ()</span><span class="sxs-lookup"><span data-stu-id="509fc-128">Console.takeheapSnapshot()</span></span>

<span data-ttu-id="509fc-129">Parfois, vous devez prendre des instantanés à des moments spécifiques, par exemple, juste avant une mutation importante du DOM.</span><span class="sxs-lookup"><span data-stu-id="509fc-129">Sometimes you need to take snapshots at very specific points in time, such as immediately before a large mutation of the DOM.</span></span> <span data-ttu-id="509fc-130">Dans ces cas-là, vous pouvez prendre des instantanés par programme [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .</span><span class="sxs-lookup"><span data-stu-id="509fc-130">In these cases,you can take snapshots programmatically with [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots).</span></span>

## <span data-ttu-id="509fc-131">Résumé du snapshot</span><span class="sxs-lookup"><span data-stu-id="509fc-131">Snapshot summary</span></span>

<span data-ttu-id="509fc-132">Le suivi d' [une capture](#toolbar) d’écran génère une vignette de synthèse qui indique la taille du tas JavaScript au moment où la capture instantané a été effectuée, ainsi que le nombre d’objets attribués et une capture d’écran de la page.</span><span class="sxs-lookup"><span data-stu-id="509fc-132">[Taking a snapshot](#toolbar) will generate a summary tile that indicates the size of the JavaScript heap at the time the snapshot was taken, along with the number of objects allocated and a screenshot of the page.</span></span> <span data-ttu-id="509fc-133">Vous pouvez continuer à prendre des instantanés à tout moment pendant que vous effectuez une analyse par le biais du scénario utilisateur.</span><span class="sxs-lookup"><span data-stu-id="509fc-133">You can continue to take snapshots at any time as you run through the user scenario requiring analysis.</span></span> <span data-ttu-id="509fc-134">Les instantanés génèrent des vignettes supplémentaires, dont chacune indique la différence de mémoire JavaScript par rapport à l’instantané précédent.</span><span class="sxs-lookup"><span data-stu-id="509fc-134">The snapshots generate additional tiles, each of which indicates the difference in JavaScript memory from the previous snapshot.</span></span>

![Instantané de tas](./media/memory_snapshot.png)

<span data-ttu-id="509fc-136">Cliquez sur les valeurs de la vignette récapitulative pour basculer vers le volet présentant les [Détails des données de capture instantanée](#snapshot-details).</span><span class="sxs-lookup"><span data-stu-id="509fc-136">Clicking on the values in the summary tile will switch to the pane showing [details of the snapshot data](#snapshot-details).</span></span> <span data-ttu-id="509fc-137">Des [problèmes de mémoire potentiels sont signalés](#snapshot-details) par une icône d’information bleue («i»).</span><span class="sxs-lookup"><span data-stu-id="509fc-137">Potential [memory issues are indicated](#snapshot-details) with a blue informational ("i") icon.</span></span>

## <span data-ttu-id="509fc-138">Détails de la photo</span><span class="sxs-lookup"><span data-stu-id="509fc-138">Snapshot details</span></span>

<span data-ttu-id="509fc-139">Les données du volet *instantané* indiquent les objets créés par votre page, ainsi que les mémoires allouées par les infrastructures JavaScript que vous pouvez consommer.</span><span class="sxs-lookup"><span data-stu-id="509fc-139">The data in the *Snapshot* pane shows the objects created by your page along with any memory allocated by JavaScript frameworks you may be consuming.</span></span>

![Tableau détails de l’instantané](./media/memory_details.png)

<span data-ttu-id="509fc-141">Les trois onglets représentent différents affichages des données:</span><span class="sxs-lookup"><span data-stu-id="509fc-141">The three tabs represent different views of the data:</span></span>

#### <span data-ttu-id="509fc-142">Types</span><span class="sxs-lookup"><span data-stu-id="509fc-142">Types</span></span>

<span data-ttu-id="509fc-143">Affiche le nombre d’instances et la taille totale des objets sur le tas, regroupés par type d’objet.</span><span class="sxs-lookup"><span data-stu-id="509fc-143">Shows the instance count and total size of objects on the heap, grouped by object type.</span></span> <span data-ttu-id="509fc-144">Par défaut, ces valeurs sont triées par nombre d’instances.</span><span class="sxs-lookup"><span data-stu-id="509fc-144">By default, these are sorted by instance count.</span></span>

<span data-ttu-id="509fc-145">Lorsque vous sélectionnez un objet dans le volet *types* du haut, la table [références d’objet](#object-references) dans le volet inférieur répertorie tous les objets qui pointent vers cet objet.</span><span class="sxs-lookup"><span data-stu-id="509fc-145">When you select an object in the upper *Types* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

#### <span data-ttu-id="509fc-146">Digne</span><span class="sxs-lookup"><span data-stu-id="509fc-146">Roots</span></span>

<span data-ttu-id="509fc-147">Affiche une vue hiérarchique des références enfant pour décrire le mode de mise en place des objets associés à l’objet global, ce qui les empêche d’être nettoyés de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="509fc-147">Shows a hierarchical view of child references to describe how objects are rooted to the global object, thus preventing them from being garbage-collected.</span></span>

<span data-ttu-id="509fc-148">Par défaut, les nœuds enfants sont triés en fonction de la taille de la colonne taille retenue, le plus grand en haut.</span><span class="sxs-lookup"><span data-stu-id="509fc-148">By default, the child nodes are sorted by the retained size column, with the largest at the top.</span></span>

#### <span data-ttu-id="509fc-149">Dominators</span><span class="sxs-lookup"><span data-stu-id="509fc-149">Dominators</span></span>

<span data-ttu-id="509fc-150">Affiche une liste des objets sur le tas qui disposent de références exclusives à d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="509fc-150">Shows a list of objects on the heap that have exclusive references to other objects.</span></span> <span data-ttu-id="509fc-151">Les Dominators sont triés par taille retenue pour indiquer que les objets consommant la plus grande quantité de mémoire est potentiellement plus facile à libérer.</span><span class="sxs-lookup"><span data-stu-id="509fc-151">Dominators are sorted by retained size to indicate the objects consuming the most memory that are potentially easiest to free.</span></span>

<span data-ttu-id="509fc-152">Voici comment interpréter les colonnes des vues *types, racines* et *Dominators* :</span><span class="sxs-lookup"><span data-stu-id="509fc-152">Here's how to interpret the columns in the *Types, Roots* and *Dominators* views:</span></span>

<span data-ttu-id="509fc-153">Colonne</span><span class="sxs-lookup"><span data-stu-id="509fc-153">Column</span></span> | <span data-ttu-id="509fc-154">Description</span><span class="sxs-lookup"><span data-stu-id="509fc-154">Description</span></span>
:------------ | :-------------
<span data-ttu-id="509fc-155">Identificateur (s)</span><span class="sxs-lookup"><span data-stu-id="509fc-155">Identifier(s)</span></span> | <span data-ttu-id="509fc-156">Nom identifiant le mieux l’objet.</span><span class="sxs-lookup"><span data-stu-id="509fc-156">Name that best identifies the object.</span></span> <span data-ttu-id="509fc-157">Par exemple, pour les éléments HTML, les détails de l’instantané indiquent la valeur de l’attribut ID, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="509fc-157">For example, for HTML elements the snapshot details show the ID attribute value, if one is used.</span></span>
<span data-ttu-id="509fc-158">Type</span><span class="sxs-lookup"><span data-stu-id="509fc-158">Type</span></span> | <span data-ttu-id="509fc-159">Type d’objet (par exemple, *HTMLDivElement*).</span><span class="sxs-lookup"><span data-stu-id="509fc-159">Object type (for example, *HTMLDivElement*).</span></span>
<span data-ttu-id="509fc-160">Taille</span><span class="sxs-lookup"><span data-stu-id="509fc-160">Size</span></span> | <span data-ttu-id="509fc-161">Taille de l’objet, sans inclure la taille des objets référencés.</span><span class="sxs-lookup"><span data-stu-id="509fc-161">Object size, not including the size of any referenced objects.</span></span>
<span data-ttu-id="509fc-162">Taille retenue</span><span class="sxs-lookup"><span data-stu-id="509fc-162">Retained size</span></span> | <span data-ttu-id="509fc-163">Taille d’objet plus la taille de tous les objets enfants qui n’ont pas d’autres parents.</span><span class="sxs-lookup"><span data-stu-id="509fc-163">Object size plus the size of all child objects that have no other parents.</span></span> <span data-ttu-id="509fc-164">Pour des raisons pratiques, il s’agit de la quantité de mémoire conservée par l’objet, de sorte que si vous supprimez l’objet vous obtenez la quantité de mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="509fc-164">For practical purposes, this is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>
<span data-ttu-id="509fc-165">Nombre</span><span class="sxs-lookup"><span data-stu-id="509fc-165">Count</span></span> | <span data-ttu-id="509fc-166">Nombre d’instances d’objets.</span><span class="sxs-lookup"><span data-stu-id="509fc-166">Number of object instances.</span></span> <span data-ttu-id="509fc-167">Cette valeur s’affiche uniquement dans l’affichage types.</span><span class="sxs-lookup"><span data-stu-id="509fc-167">This value appears only in the Types view.</span></span>

<span data-ttu-id="509fc-168">Lorsque vous sélectionnez un objet dans le volet de *Dominators* supérieur, le tableau [références d’objet](#object-references) dans le volet inférieur répertorie tous les objets qui pointent vers cet objet.</span><span class="sxs-lookup"><span data-stu-id="509fc-168">When you select an object in the upper *Dominators* pane, the [Object references](#object-references) table in the lower pane will list all the objects that point to that object.</span></span>

### <span data-ttu-id="509fc-169">Filtré</span><span class="sxs-lookup"><span data-stu-id="509fc-169">Filters</span></span>

<span data-ttu-id="509fc-170">Vous pouvez ensuite ajuster les données du tableau de la manière suivante:</span><span class="sxs-lookup"><span data-stu-id="509fc-170">You can further adjust data in the table with the following:</span></span>

![Filtrer les composants intégrés et les ID d’objet](./media/memory_filter.png)

1. <span data-ttu-id="509fc-172">**Filtre identificateur**: filtrez les données en recherchant un identificateur d’objet particulier</span><span class="sxs-lookup"><span data-stu-id="509fc-172">**Identifier filter**: Filter out data by searching for a particular object identifier</span></span>
2. <span data-ttu-id="509fc-173">**Regroupement par Dominator**: seuls les objets dotés de références *exclusives* à d’autres objets apparaissent dans l’affichage de niveau supérieur d’objets (il s’agit de l’affichage par défaut dans l’onglet *Dominators* ).</span><span class="sxs-lookup"><span data-stu-id="509fc-173">**Group by dominator**: Only objects with *exclusive* references to other objects are shown in the top-level view of objects (this is the default view in the *Dominators* tab).</span></span>
3. <span data-ttu-id="509fc-174">**Filtre des composants intégrés/identifiants**: par défaut, les [objets intégrés JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) sont inclus dans la liste.</span><span class="sxs-lookup"><span data-stu-id="509fc-174">**Built-ins / IDs filter**: By default, [JavaScript built-in objects](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) are included in the list.</span></span> <span data-ttu-id="509fc-175">Les ID d’objet de liste peuvent être utiles s’il existe plusieurs objets anonymes qui doivent être différenciés.</span><span class="sxs-lookup"><span data-stu-id="509fc-175">Listing object IDs can be useful if there are multiple anonymous objects which need to be differentiated.</span></span>

<span data-ttu-id="509fc-176">Les vues *types, racines* et *Dominators* ont chacune leur propre filtre, de sorte que le filtre n’est pas conservé quand vous basculez vers un autre mode d’affichage.</span><span class="sxs-lookup"><span data-stu-id="509fc-176">The *Types, Roots* and *Dominators* views each has its own filter, so the filter isn't preserved when you switch to another view.</span></span>

### <span data-ttu-id="509fc-177">Références d’objets</span><span class="sxs-lookup"><span data-stu-id="509fc-177">Object references</span></span>

<span data-ttu-id="509fc-178">Dans les vues [**types**](#types) et [**Dominators**](#dominators) , le volet inférieur contient une liste **références d’objets** qui affiche des références partagées.</span><span class="sxs-lookup"><span data-stu-id="509fc-178">In the [**Types**](#types) and [**Dominators**](#dominators) views, the lower pane contains an **Object references** list that displays shared references.</span></span> <span data-ttu-id="509fc-179">Lorsque vous sélectionnez un objet dans le volet supérieur, cette liste affiche tous les objets qui pointent vers cet objet, en d’autres termes, les objets qui gardent l’objet sélectionné actif.</span><span class="sxs-lookup"><span data-stu-id="509fc-179">When you choose an object in the upper pane, this list displays all objects that point to that object--in other words, the objects that are keeping the selected object alive.</span></span>

<span data-ttu-id="509fc-180">Les références circulaires s’affichent à l’aide d’un astérisque (\*) et d’une info-bulle d’information et ne peuvent pas être développés.</span><span class="sxs-lookup"><span data-stu-id="509fc-180">Circular references are shown with an asterisk (\*) and informational tooltip, and cannot be expanded.</span></span> <span data-ttu-id="509fc-181">Sinon, ils vous empêchent de remonter l’arborescence de référence et d’identifier les objets qui conservent de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="509fc-181">Otherwise, they would prevent you from walking up the reference tree and identifying objects that are retaining memory.</span></span>

<span data-ttu-id="509fc-182">Pour identifier rapidement les objets équivalents, cochez l’option filtre d' [*ID d’objet d’affichage*](#filters) pour afficher les ID d’objet en regard de noms d’objets dans la colonne *identificateur (s)* .</span><span class="sxs-lookup"><span data-stu-id="509fc-182">To quickly identify equivalent objects, tick the [*Display object IDs*](#filters) filter option to display object IDs next to object names in the *Identifier(s)* column.</span></span> <span data-ttu-id="509fc-183">Les objets portant le même ID sont des références partagées.</span><span class="sxs-lookup"><span data-stu-id="509fc-183">Objects that have the same ID are shared references.</span></span>

### <span data-ttu-id="509fc-184">Comparaison des snapshots</span><span class="sxs-lookup"><span data-stu-id="509fc-184">Snapshot comparison</span></span>

<span data-ttu-id="509fc-185">Cliquez sur un [onglet de comparaison de capture instantanée](#snapshot-details) ou sur le lien de comparaison dans la [vignette de synthèse de capture instantanée](#snapshot-summary) pour afficher une différence d’information entre les deux instantanés.</span><span class="sxs-lookup"><span data-stu-id="509fc-185">Clicking on a [snapshot comparison tab](#snapshot-details) or comparison link on the [snapshot summary tile](#snapshot-summary)  will show a diff of information between the two snapshots.</span></span> <span data-ttu-id="509fc-186">Dans le volet comparaison, les affichages *Dominators, types* et *racines* fournissent les mêmes [*informations d’instantané*](#snapshot-details) que celles disponibles pour une seule image, avec ces valeurs supplémentaires:</span><span class="sxs-lookup"><span data-stu-id="509fc-186">In the comparison pane, the *Dominators, Types* and *Roots* views provide the same [*snapshot details*](#snapshot-details) you would see for a single snapshots, with these additional values:</span></span>

<span data-ttu-id="509fc-187">Colonne</span><span class="sxs-lookup"><span data-stu-id="509fc-187">Column</span></span> | <span data-ttu-id="509fc-188">Description</span><span class="sxs-lookup"><span data-stu-id="509fc-188">Description</span></span>
:------------ | :-------------
<span data-ttu-id="509fc-189">Différences de taille.</span><span class="sxs-lookup"><span data-stu-id="509fc-189">Size diff.</span></span> | <span data-ttu-id="509fc-190">Différence entre la taille de l’objet dans l’instantané actuel et sa taille dans l’instantané précédent, sans inclure la taille des objets référencés.</span><span class="sxs-lookup"><span data-stu-id="509fc-190">Difference between the size of the object in the current snapshot and its size in the previous snapshot, not including the size of any referenced objects.</span></span>
<span data-ttu-id="509fc-191">Différence de taille retenue</span><span class="sxs-lookup"><span data-stu-id="509fc-191">Retained size diff.</span></span> | <span data-ttu-id="509fc-192">Différence entre la taille retenue de l’objet dans l’instantané actuel et sa taille de conservation dans l’instantané précédent.</span><span class="sxs-lookup"><span data-stu-id="509fc-192">Difference between the retained size of the object in the current snapshot and its retained size in the previous snapshot.</span></span> <span data-ttu-id="509fc-193">La taille retenue inclut la taille de l’objet plus la taille de tous ses objets enfants qui n’ont pas d’autres parents.</span><span class="sxs-lookup"><span data-stu-id="509fc-193">The retained size includes the object size plus the size of all its child objects that have no other parents.</span></span> <span data-ttu-id="509fc-194">Pour des raisons pratiques, la taille retenue correspond à la quantité de mémoire conservée par l’objet, de sorte que si vous supprimez l’objet vous obtenez la quantité de mémoire spécifiée.</span><span class="sxs-lookup"><span data-stu-id="509fc-194">For practical purposes, the retained size is the amount of memory retained by the object, so if you delete the object you reclaim the specified amount of memory.</span></span>

<span data-ttu-id="509fc-195">Vous pouvez utiliser la liste déroulante **scope** pour filtrer les informations différentielles entre les instantanés:</span><span class="sxs-lookup"><span data-stu-id="509fc-195">You can use the **Scope** dropdown to filter differential info between snapshots:</span></span>

![Filtre d’étendue pour les comparis de capture instantanée](./media/memory_comparison_scope_filter.png)

- <strong><span data-ttu-id="509fc-197">Les objets situés à l’origine de l’instantané n ° instantané <number></strong> indiquent la différence entre les objets ajoutés au tas et supprimés du tas de l’instantané de référence à l’instantané précédent.</span><span class="sxs-lookup"><span data-stu-id="509fc-197">Objects left over from Snapshot #<number></strong>: Shows the diff between the objects added to the heap and removed from the heap from the baseline snapshot to the previous snapshot.</span></span> <span data-ttu-id="509fc-198">Par exemple, si le résumé de l’instantané affiche <em> + 205/-195 </em> dans le nombre d’objets, ce filtre vous montrera les dix objets qui ont été ajoutés mais ne sont pas supprimés.</span><span class="sxs-lookup"><span data-stu-id="509fc-198">For example, if the snapshot summary shows <em>+205 / -195</em> in the object count, this filter will show you the ten objects that were added but not removed.</span></span>

- <strong><span data-ttu-id="509fc-199">Les objets ajoutés entre instantané # <number> et # <number></strong> : affiche tous les objets ajoutés au tas à partir de l’instantané précédent.</span><span class="sxs-lookup"><span data-stu-id="509fc-199">Objects added between Snapshot #<number> and #<number></strong>: Shows all objects added to the heap from the previous snapshot.</span></span>

- <strong><span data-ttu-id="509fc-200">Tous les objets dans l’instantané # <number></strong> : affiche tous les objets sur le tas (en d’autres termes, un <em> affichage non filtré </em> ).</span><span class="sxs-lookup"><span data-stu-id="509fc-200">All objects in Snapshot #<number></strong>: Shows all objects on the heap (in other words, an <em>unfiltered</em> view).</span></span>

<span data-ttu-id="509fc-201">Par défaut, le filtre *afficher les références non concordantes* est appliqué à l’affichage comparaison pour indiquer des références d’objets qui ne correspondent pas au filtre d’étendue actuel.</span><span class="sxs-lookup"><span data-stu-id="509fc-201">By default, the *Show non-matching references* filter is applied to the comparison view to indicate object references that don't match the current Scope filter.</span></span> <span data-ttu-id="509fc-202">Vous pouvez désactiver cette option dans le menu déroulant:</span><span class="sxs-lookup"><span data-stu-id="509fc-202">You can turn it off from the dropdown menu:</span></span>

![Filtre des références non concordantes pour les comparaisons de capture instantanée](./media/memory_comparison_matching_filter.png)


## <span data-ttu-id="509fc-204">Associés</span><span class="sxs-lookup"><span data-stu-id="509fc-204">Shortcuts</span></span>

 <span data-ttu-id="509fc-205">Action</span><span class="sxs-lookup"><span data-stu-id="509fc-205">Action</span></span> | <span data-ttu-id="509fc-206">Raccourci</span><span class="sxs-lookup"><span data-stu-id="509fc-206">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="509fc-207">Démarrer/arrêter la session de profilage</span><span class="sxs-lookup"><span data-stu-id="509fc-207">Start / Stop profiling session</span></span>  | `Ctrl` + `E`
<span data-ttu-id="509fc-208">Importer une session de profil</span><span class="sxs-lookup"><span data-stu-id="509fc-208">Import profiling session</span></span> | `Ctrl` + `O`
<span data-ttu-id="509fc-209">Exporter la session de profilage</span><span class="sxs-lookup"><span data-stu-id="509fc-209">Export profiling session</span></span> | `Ctrl` + `S`
<span data-ttu-id="509fc-210">Instantané de tas</span><span class="sxs-lookup"><span data-stu-id="509fc-210">Take heap snapshot</span></span> | `Ctrl` + `Shift` + `T`

## <span data-ttu-id="509fc-211">Problèmes connus</span><span class="sxs-lookup"><span data-stu-id="509fc-211">Known Issues</span></span>

### <span data-ttu-id="509fc-212">Une erreur s’est produite lors du démarrage de la session de profilage</span><span class="sxs-lookup"><span data-stu-id="509fc-212">An error occurred while starting the profiling session</span></span>

<span data-ttu-id="509fc-213">Si vous voyez ce message d’erreur: **une erreur s’est produite lors du démarrage de la session de profilage** dans l’outil mémoire, procédez comme suit pour contourner le problème.</span><span class="sxs-lookup"><span data-stu-id="509fc-213">If you see this error message: **An error occurred while starting the profiling session** in the Memory tool, follow these steps for a workaround.</span></span>

1. <span data-ttu-id="509fc-214">Appuyez sur `Windows Key`  +  `R` .</span><span class="sxs-lookup"><span data-stu-id="509fc-214">Press `Windows Key` + `R`.</span></span>

2. <span data-ttu-id="509fc-215">Dans la boîte de dialogue Exécuter, entrez **services. msc**.</span><span class="sxs-lookup"><span data-stu-id="509fc-215">In the Run dialog, enter **services.msc**.</span></span>
![problèmes connus-1](./media/known_issues_1.PNG)

3. <span data-ttu-id="509fc-217">Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.</span><span class="sxs-lookup"><span data-stu-id="509fc-217">Locate the **Microsoft (R) Diagnostics Hub Standard Collector Service** and right-click it.</span></span>
![problèmes connus-2](./media/known_issues_2.PNG)

4. <span data-ttu-id="509fc-219">Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.</span><span class="sxs-lookup"><span data-stu-id="509fc-219">Restart the **Microsoft (R) Diagnostics Hub Standard Collector Service**.</span></span>
![problèmes connus-3](./media/known_issues_3.PNG)

5. <span data-ttu-id="509fc-221">Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .</span><span class="sxs-lookup"><span data-stu-id="509fc-221">Close the Microsoft Edge Developer Tools and the tab. Open a new tab, navigate to your page, and press `F12`.</span></span>

6. <span data-ttu-id="509fc-222">Vous devriez maintenant être en mesure de commencer le profilage.</span><span class="sxs-lookup"><span data-stu-id="509fc-222">You should now be able to begin profiling.</span></span> 
![problèmes connus-4](./media/known_issues_4-memory.PNG)

<span data-ttu-id="509fc-224">Vous rencontrez encore des problèmes?</span><span class="sxs-lookup"><span data-stu-id="509fc-224">Still running into problems?</span></span> <span data-ttu-id="509fc-225">Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** !</span><span class="sxs-lookup"><span data-stu-id="509fc-225">Please send us your feedback using the **Send feedback** icon!</span></span> 

![problèmes connus-5](./media/known_issues_5.PNG)
