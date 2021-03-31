---
description: Cette section décrit les termes courants utilisés dans l’analyse de la mémoire et s’applique à divers outils de profilage de mémoire pour différentes langues.
title: Terminologie de la mémoire
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1579374be29f0f419ded3bf88f5dea284f0bbb1a
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11397789"
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
   limitations under the License. -->

# <a name="memory-terminology"></a><span data-ttu-id="4e422-104">Terminologie de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4e422-104">Memory terminology</span></span>  

<span data-ttu-id="4e422-105">Cet article décrit les termes courants utilisés dans l’analyse de la mémoire et s’applique à différents outils de profilage de mémoire pour différentes langues.</span><span class="sxs-lookup"><span data-stu-id="4e422-105">This article describes common terms used in memory analysis, and is applicable to various memory profiling tools for different languages.</span></span>  

<span data-ttu-id="4e422-106">Les termes et les notions décrits ici font référence au [panneau Mémoire.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="4e422-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="4e422-107">Si vous avez déjà travaillé avec le Java, .NET ou un autre profileur de mémoire, cet article peut être actualisé.</span><span class="sxs-lookup"><span data-stu-id="4e422-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this article may be a refresher.</span></span>  

## <a name="object-sizes"></a><span data-ttu-id="4e422-108">Tailles des objets</span><span class="sxs-lookup"><span data-stu-id="4e422-108">Object sizes</span></span>  

<span data-ttu-id="4e422-109">Pensez à la mémoire sous la forme d’un graphique avec des types primitifs \(tels que des nombres et des chaînes\) et des objets \(tableaux associatifs\).</span><span class="sxs-lookup"><span data-stu-id="4e422-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="4e422-110">Il peut s’afficher sous la forme d’un graphique avec de nombreux points interconnectés tels que la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="4e422-110">It may display as a graph with many interconnected points such as following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Représentation visuelle de la mémoire" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="4e422-112">Représentation visuelle de la mémoire</span><span class="sxs-lookup"><span data-stu-id="4e422-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="4e422-113">Un objet peut contenir de la mémoire de deux manières :</span><span class="sxs-lookup"><span data-stu-id="4e422-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="4e422-114">Directement par l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e422-114">Directly by the object.</span></span>  
*   <span data-ttu-id="4e422-115">Implicitement en maintenant des références à d’autres objets, et par conséquent en empêchant leur élimination automatique par un garbage collector.</span><span class="sxs-lookup"><span data-stu-id="4e422-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector.</span></span>  

<span data-ttu-id="4e422-116">Lorsque vous [][DevtoolsMemoryProblemsHeapSnapshots] travaillez avec le panneau Mémoire dans DevTools \(un outil permettant d’examiner les problèmes de mémoire trouvés sous **Mémoire**\), vous pouvez vous retrouver en regardant différentes colonnes d’informations.</span><span class="sxs-lookup"><span data-stu-id="4e422-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="4e422-117">Deux éléments se démarquent par **la taille superficiele** et la **taille conservée,** mais que représentent-ils ?</span><span class="sxs-lookup"><span data-stu-id="4e422-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tailles superficiels et conservées" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="4e422-119">Tailles superficiels et conservées</span><span class="sxs-lookup"><span data-stu-id="4e422-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <a name="shallow-size"></a><span data-ttu-id="4e422-120">Taille superficiele</span><span class="sxs-lookup"><span data-stu-id="4e422-120">Shallow size</span></span>  

<span data-ttu-id="4e422-121">Il s’agit de la taille de la mémoire détenue par l’objet.</span><span class="sxs-lookup"><span data-stu-id="4e422-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="4e422-122">La mémoire des objets JavaScript classiques est réservée à leur description et au stockage des valeurs immédiates.</span><span class="sxs-lookup"><span data-stu-id="4e422-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="4e422-123">En règle générale, seuls les tableaux et les chaînes peuvent avoir une taille faible significative.</span><span class="sxs-lookup"><span data-stu-id="4e422-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="4e422-124">Toutefois, les chaînes et les tableaux externes ont souvent leur stockage principal dans la mémoire du renderer, exposant uniquement un petit objet wrapper sur le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e422-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="4e422-125">La mémoire du renderer est l’ensemble de la mémoire du processus dans lequel une page inspectée est rendue : mémoire native + mémoire de tas JS de la page + mémoire de tas JS de tous les travailleurs dédiés démarrés par la page.</span><span class="sxs-lookup"><span data-stu-id="4e422-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="4e422-126">Néanmoins, même un petit objet peut contenir une grande quantité de mémoire indirectement, en empêchant d’autres objets d’être éliminés par le processus de collecte automatique de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="4e422-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <a name="retained-size"></a><span data-ttu-id="4e422-127">Taille conservée</span><span class="sxs-lookup"><span data-stu-id="4e422-127">Retained size</span></span>  

<span data-ttu-id="4e422-128">Il s’agit de la taille de la mémoire qui est libérée une fois que l’objet est supprimé avec les objets dépendants qui ont été rendues inaccessibles à partir des racines garbage **collector**.</span><span class="sxs-lookup"><span data-stu-id="4e422-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots**.</span></span>  

<span data-ttu-id="4e422-129">**Les racines** du Garbage Collector sont des **poignées créées** \(locales ou globales\) lors de la création d’une référence à partir de code natif à un objet JavaScript en dehors de V8.</span><span class="sxs-lookup"><span data-stu-id="4e422-129">**Garbage Collector roots** are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="4e422-130">Tous ces handles peuvent être trouvés dans un instantané de tas sous **des racines GC**Handle scope et GC  >     >  **racines Global handles**.</span><span class="sxs-lookup"><span data-stu-id="4e422-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="4e422-131">Décrire les descripteurs de cette documentation sans plonger dans les détails de l’implémentation du navigateur peut prêter à confusion.</span><span class="sxs-lookup"><span data-stu-id="4e422-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="4e422-132">Les racines du garbage collector et les poignées ne sont pas des sujets dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="4e422-132">Both Garbage Collector roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="4e422-133">Il existe de nombreuses racines de garbage collector internes, dont la plupart ne sont pas intéressantes pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="4e422-133">There are lots of internal Garbage Collector roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="4e422-134">Du point de vue des applications, il existe des types de racines suivants.</span><span class="sxs-lookup"><span data-stu-id="4e422-134">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="4e422-135">Objet global Window \(dans chaque iframe\).</span><span class="sxs-lookup"><span data-stu-id="4e422-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="4e422-136">Il existe un champ de distance dans les captures instantanées de tas qui est le nombre de références de propriétés sur le chemin de rétention le plus court à partir de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4e422-136">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="4e422-137">L’arborescence DOM du document constituée de tous les nodes DOM natifs est accessible en parcourant le document.</span><span class="sxs-lookup"><span data-stu-id="4e422-137">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="4e422-138">Tous les nœuds ne peuvent pas avoir de wrappers JS, mais si un nœud possède un wrapper, il est présent tant que le document est en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="4e422-138">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="4e422-139">Parfois, les objets peuvent être conservés par le contexte du débogger dans le panneau **Sources** et la **console** \(par exemple, après l’évaluation de la console\).</span><span class="sxs-lookup"><span data-stu-id="4e422-139">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="4e422-140">Créez des captures instantanées de tas avec un panneau **console** effacé et aucun point d’arrêt actif dans le débogger du **panneau Sources.**</span><span class="sxs-lookup"><span data-stu-id="4e422-140">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="4e422-141">Désactivez **le panneau console** en exécutant et en désactivant les points d’arrêt dans le panneau Sources avant de prendre une capture instantanée du tas `clear()` dans le panneau [Mémoire.][DevtoolsMemoryProblemsHeapSnapshots] </span><span class="sxs-lookup"><span data-stu-id="4e422-141">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="4e422-142">Le graphique de mémoire commence par une racine, qui peut être l’objet du navigateur ou l’objet `window` `Global` d'Node.js module.</span><span class="sxs-lookup"><span data-stu-id="4e422-142">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="4e422-143">Vous ne contrôlez pas la façon dont cet objet racine est collecté à la garbage.</span><span class="sxs-lookup"><span data-stu-id="4e422-143">You do not control how this root object is garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Vous ne pouvez pas contrôler la façon dont l’objet racine est collecté." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="4e422-145">Vous ne pouvez pas contrôler la façon dont l’objet racine est collecté.</span><span class="sxs-lookup"><span data-stu-id="4e422-145">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="4e422-146">Tout ce qui n’est pas accessible à partir de la racine obtient la garbage collected.</span><span class="sxs-lookup"><span data-stu-id="4e422-146">Whatever is not reachable from the root gets garbage collected.</span></span>  

> [!NOTE]
> <span data-ttu-id="4e422-147">Les [colonnes Taille superficiele et](#shallow-size) [Taille conservée](#retained-size) représentent toutes deux des données en octets.</span><span class="sxs-lookup"><span data-stu-id="4e422-147">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <a name="objects-retaining-tree"></a><span data-ttu-id="4e422-148">Objets conservant l’arborescence</span><span class="sxs-lookup"><span data-stu-id="4e422-148">Objects retaining tree</span></span>  

<span data-ttu-id="4e422-149">Le tas est un réseau d’objets interconnectés.</span><span class="sxs-lookup"><span data-stu-id="4e422-149">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="4e422-150">Dans le monde mathématique, cette structure est appelée graphique **ou** graphique mémoire.</span><span class="sxs-lookup"><span data-stu-id="4e422-150">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="4e422-151">Un graphique est construit à partir **de nods** connectés à l’aide de **bords,** qui sont tous deux attribués à des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="4e422-151">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="4e422-152">**Les nodes** \(ou objets \) sont **étiquetés**à l’aide du nom de la fonction constructeur qui a été utilisée pour les créer. </span><span class="sxs-lookup"><span data-stu-id="4e422-152">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="4e422-153">**Les bords** sont étiquetés à l’aide des noms des **propriétés.**</span><span class="sxs-lookup"><span data-stu-id="4e422-153">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="4e422-154">Découvrez [comment enregistrer un profil à l’aide du Profileur][DevtoolsMemoryProblemsHeapSnapshots]de tas.</span><span class="sxs-lookup"><span data-stu-id="4e422-154">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="4e422-155">Dans la figure suivante, certains des éléments notables [][DevtoolsMemoryProblemsHeapSnapshots] de l’enregistrement instantané de tas dans l’outil Mémoire incluent la distance : la distance par rapport à la racine du garbage collector.</span><span class="sxs-lookup"><span data-stu-id="4e422-155">In the following figure, some of the notable things in the Heap Snapshot recording in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool include distance:  the distance from the Garbage Collector root.</span></span>  <span data-ttu-id="4e422-156">Si presque tous les objets du même type sont à la même distance et que certains d’entre eux se trouve à une plus grande distance, cela vaut la peine d’examiner ce point.</span><span class="sxs-lookup"><span data-stu-id="4e422-156">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distance par rapport à la racine" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="4e422-158">Distance par rapport à la racine</span><span class="sxs-lookup"><span data-stu-id="4e422-158">Distance from root</span></span>  
:::image-end:::  

## <a name="dominators"></a><span data-ttu-id="4e422-159">Dominants</span><span class="sxs-lookup"><span data-stu-id="4e422-159">Dominators</span></span>  

<span data-ttu-id="4e422-160">Les objets dominants sont constitués d’une arborescence, car chaque objet possède exactement un seul dominant.</span><span class="sxs-lookup"><span data-stu-id="4e422-160">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="4e422-161">Un dominant d’un objet peut ne pas avoir de références directes à un objet qu’il dirige ; autrement dit, l’arborescence du sous-arbre n’est pas une arborescence couvrante du graphique.</span><span class="sxs-lookup"><span data-stu-id="4e422-161">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="4e422-162">Dans la figure suivante, l’instruction suivante est vraie.</span><span class="sxs-lookup"><span data-stu-id="4e422-162">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="4e422-163">Nœud 1 nœud 2</span><span class="sxs-lookup"><span data-stu-id="4e422-163">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="4e422-164">Nœud 2 nœuds 3, 4 et 6</span><span class="sxs-lookup"><span data-stu-id="4e422-164">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="4e422-165">Nœud 3 nœud 5</span><span class="sxs-lookup"><span data-stu-id="4e422-165">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="4e422-166">Nœud 5 nœud 8</span><span class="sxs-lookup"><span data-stu-id="4e422-166">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="4e422-167">Nœud 6 nœud 7</span><span class="sxs-lookup"><span data-stu-id="4e422-167">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Structure de l’arborescence de l’dominant" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="4e422-169">Structure de l’arborescence de l’dominant</span><span class="sxs-lookup"><span data-stu-id="4e422-169">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="4e422-170">Dans la figure suivante, le nœud est l’en-avant-première de , mais il existe également dans chaque chemin simple du garbage `#3` `#10` collector à `#7` `#10` .</span><span class="sxs-lookup"><span data-stu-id="4e422-170">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector to `#10`.</span></span>  <span data-ttu-id="4e422-171">Par conséquent, un objet B est le résorbateur d’un objet A si B existe dans chaque chemin d’accès simple de la racine à l’objet A.</span><span class="sxs-lookup"><span data-stu-id="4e422-171">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Illustration de l’animation de l’animation de l’animation" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="4e422-173">Illustration de l’animation de l’animation de l’animation</span><span class="sxs-lookup"><span data-stu-id="4e422-173">Animated dominator illustration</span></span>  
:::image-end:::  

## <a name="v8-specifics"></a><span data-ttu-id="4e422-174">Spécificités V8</span><span class="sxs-lookup"><span data-stu-id="4e422-174">V8 specifics</span></span>  

<span data-ttu-id="4e422-175">Lors du profilage de la mémoire, il est utile de comprendre pourquoi les captures instantanées de tas semblent d’une certaine façon.</span><span class="sxs-lookup"><span data-stu-id="4e422-175">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="4e422-176">Cette section décrit certaines rubriques relatives à la mémoire qui correspondent spécifiquement à la machine virtuelle **JavaScript V8** \(V8 V8 VM ou VM\).</span><span class="sxs-lookup"><span data-stu-id="4e422-176">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <a name="javascript-object-representation"></a><span data-ttu-id="4e422-177">Représentation d’objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="4e422-177">JavaScript object representation</span></span>  

<span data-ttu-id="4e422-178">Il existe trois types primitifs :</span><span class="sxs-lookup"><span data-stu-id="4e422-178">There are three primitive types:</span></span>  

*   <span data-ttu-id="4e422-179">Nombres \(par exemple `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="4e422-179">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="4e422-180">Booléens \( `true` ou `false` \)</span><span class="sxs-lookup"><span data-stu-id="4e422-180">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="4e422-181">Chaînes \(par exemple `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="4e422-181">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="4e422-182">Les primitives ne peuvent pas référencer d’autres valeurs et sont toujours des feuilles ou des nodes terminaux.</span><span class="sxs-lookup"><span data-stu-id="4e422-182">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="4e422-183">**Les** nombres peuvent être stockés sous l’une ou l’autre des façons :</span><span class="sxs-lookup"><span data-stu-id="4e422-183">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="4e422-184">valeurs d’un nombre integer 31 bits immédiatement appelées petits **nombres d’nombres integers** \(**SMI**s\) ou</span><span class="sxs-lookup"><span data-stu-id="4e422-184">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="4e422-185">objets de tas, appelés nombres **de tas**.</span><span class="sxs-lookup"><span data-stu-id="4e422-185">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="4e422-186">Les nombres de tas sont utilisés pour stocker les valeurs qui ne s’intègrent pas dans le formulaire SMI, telles que les **doubles,** ou lorsqu’une valeur doit être encadrée,  par exemple la définition de propriétés sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4e422-186">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="4e422-187">**Les** chaînes peuvent être stockées dans :</span><span class="sxs-lookup"><span data-stu-id="4e422-187">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="4e422-188">le **tas de la VM,** ou</span><span class="sxs-lookup"><span data-stu-id="4e422-188">the **VM heap**, or</span></span>
*   <span data-ttu-id="4e422-189">externe dans la **mémoire du renderer**.</span><span class="sxs-lookup"><span data-stu-id="4e422-189">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="4e422-190">Un **objet wrapper** est créé et utilisé pour accéder au stockage externe où, par exemple, les sources de script et d’autres contenus reçus à partir du Web sont stockés, plutôt que copiés sur le tas de l’environnement de ligne de disque.</span><span class="sxs-lookup"><span data-stu-id="4e422-190">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="4e422-191">La mémoire pour les nouveaux objets JavaScript est allouée à partir d’un tas JavaScript dédié \(ou d’un tas **de vm**\).</span><span class="sxs-lookup"><span data-stu-id="4e422-191">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="4e422-192">Ces objets sont gérés par le garbage collector dans V8 et, par conséquent, restent en vie tant qu’il existe au moins une référence forte à ces objets.</span><span class="sxs-lookup"><span data-stu-id="4e422-192">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="4e422-193">Tout ce qui ne se trouve pas dans le tas JavaScript est appelé **un objet natif.**</span><span class="sxs-lookup"><span data-stu-id="4e422-193">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="4e422-194">Les objets natifs, contrairement aux objets tas, ne sont pas gérés par le garbage collector V8 tout au long de leur durée de vie et peuvent uniquement être accessibles à partir de JavaScript à l’aide de l’objet wrapper JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e422-194">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="4e422-195">**La chaîne** Cons est un objet qui se compose de paires de chaînes stockées, puis jointes, et est le résultat de la concatenation.</span><span class="sxs-lookup"><span data-stu-id="4e422-195">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="4e422-196">La jointation du contenu de la **chaîne cons se** produit uniquement selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="4e422-196">The joining of the **cons string** contents occurs only as needed.</span></span>  <span data-ttu-id="4e422-197">Par exemple, lorsqu’une sous-chaîne d’une chaîne jointe doit être construite.</span><span class="sxs-lookup"><span data-stu-id="4e422-197">For example, when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="4e422-198">Par exemple, si vous concaténer et , vous obtenez une chaîne qui représente le `a` `b` résultat de la `(a, b)` concaténation.</span><span class="sxs-lookup"><span data-stu-id="4e422-198">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="4e422-199">Si vous êtes concaté ultérieurement avec ce résultat, vous obtenez `d` une autre chaîne de **inconvénients**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="4e422-199">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="4e422-200">**Le** tableau est un objet avec des clés numériques.</span><span class="sxs-lookup"><span data-stu-id="4e422-200">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="4e422-201">**Les tableaux** sont largement utilisés dans la V8 VM pour stocker de grandes quantités de données.</span><span class="sxs-lookup"><span data-stu-id="4e422-201">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="4e422-202">Les ensembles de paires clé-valeur, tels que les dictionnaires, sont backed up par **des tableaux**.</span><span class="sxs-lookup"><span data-stu-id="4e422-202">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="4e422-203">Un objet JavaScript classique est stocké comme un seul des deux types **de tableau** :</span><span class="sxs-lookup"><span data-stu-id="4e422-203">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="4e422-204">propriétés nommées et</span><span class="sxs-lookup"><span data-stu-id="4e422-204">named properties, and</span></span>  
*   <span data-ttu-id="4e422-205">éléments numériques</span><span class="sxs-lookup"><span data-stu-id="4e422-205">numeric elements</span></span>  

<span data-ttu-id="4e422-206">Lorsqu’il existe un petit nombre de propriétés, les propriétés sont stockées en interne dans l’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e422-206">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="4e422-207">**Map** est un objet qui décrit à la fois le type d’objet et la disposition.</span><span class="sxs-lookup"><span data-stu-id="4e422-207">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="4e422-208">Par exemple, les cartes sont utilisées pour décrire les hiérarchies d’objets implicites pour un [accès rapide aux propriétés.][V8FastProperties]</span><span class="sxs-lookup"><span data-stu-id="4e422-208">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <a name="object-groups"></a><span data-ttu-id="4e422-209">Groupes d’objets</span><span class="sxs-lookup"><span data-stu-id="4e422-209">Object groups</span></span>  

<span data-ttu-id="4e422-210">Chaque **groupe d’objets natifs** est composé d’objets qui tiennent des références mutuelles les uns aux autres.</span><span class="sxs-lookup"><span data-stu-id="4e422-210">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="4e422-211">Considérons, par exemple, une sous-arbre DOM où chaque nœud possède un lien vers le parent relatif et des liens vers l’enfant suivant et le frère suivant, ce qui a pour effet de former un graphique connecté.</span><span class="sxs-lookup"><span data-stu-id="4e422-211">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="4e422-212">Les objets natifs ne sont pas représentés dans le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4e422-212">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="4e422-213">L’absence de représentation est la raison pour laquelle les objets natifs ont une taille nulle.</span><span class="sxs-lookup"><span data-stu-id="4e422-213">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="4e422-214">Au lieu de cela, les objets wrapper sont créés.</span><span class="sxs-lookup"><span data-stu-id="4e422-214">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="4e422-215">Chaque objet wrapper contient une référence à l’objet natif correspondant, pour rediriger les commandes vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="4e422-215">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="4e422-216">À son tour, un groupe d’objets contient des objets wrapper.</span><span class="sxs-lookup"><span data-stu-id="4e422-216">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="4e422-217">Toutefois, cela ne crée pas de cycle non récollectable, car le Garbage Collector est suffisamment intelligent pour libérer les groupes d’objets dont les wrappers ne sont plus référencés.</span><span class="sxs-lookup"><span data-stu-id="4e422-217">However, this does not create an uncollectable cycle, as Garbage Collector is smart enough to release object groups whose wrappers are no longer referenced.</span></span>  <span data-ttu-id="4e422-218">Mais l’oubli de libérer un seul wrapper contient le groupe entier et les wrappers associés.</span><span class="sxs-lookup"><span data-stu-id="4e422-218">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="4e422-219">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="4e422-219">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Comment enregistrer des instantanés de tas | Documents Microsoft"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriétés rapides dans V8 | V8"  

> [!NOTE]
> <span data-ttu-id="4e422-222">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e422-222">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="4e422-223">La page d’origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) et est co-auteure par [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="4e422-223">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="4e422-225">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="4e422-225">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
