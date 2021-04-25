---
description: Cette section décrit les termes courants utilisés dans l'analyse de la mémoire et s'applique à divers outils de profilage de mémoire pour différentes langues.
title: Terminologie de la mémoire
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: c9659255e2bf0082cd1be3e6615c9d54c293b967
ms.sourcegitcommit: 16e2f7232196a57a70b979bbf8b663774b7ddc20
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/25/2021
ms.locfileid: "11519309"
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

# <a name="memory-terminology"></a><span data-ttu-id="18eb3-104">Terminologie de la mémoire</span><span class="sxs-lookup"><span data-stu-id="18eb3-104">Memory terminology</span></span>  

<span data-ttu-id="18eb3-105">Cet article décrit les termes courants utilisés dans l'analyse de la mémoire et s'applique à divers outils de profilage de mémoire pour différentes langues.</span><span class="sxs-lookup"><span data-stu-id="18eb3-105">This article describes common terms used in memory analysis, and is applicable to various memory profiling tools for different languages.</span></span>  

<span data-ttu-id="18eb3-106">Les termes et les notions décrits ici font référence au [panneau Mémoire.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="18eb3-106">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="18eb3-107">Si vous avez déjà travaillé avec le Java, .NET ou un autre profileur de mémoire, cet article peut être actualisé.</span><span class="sxs-lookup"><span data-stu-id="18eb3-107">If you have ever worked with either the Java, .NET, or some other memory profiler, then this article may be a refresher.</span></span>  

## <a name="object-sizes"></a><span data-ttu-id="18eb3-108">Tailles des objets</span><span class="sxs-lookup"><span data-stu-id="18eb3-108">Object sizes</span></span>  

<span data-ttu-id="18eb3-109">Pensez à la mémoire sous la forme d'un graphique avec des types primitifs \(tels que des nombres et des chaînes\) et des objets \(tableaux associatifs\).</span><span class="sxs-lookup"><span data-stu-id="18eb3-109">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="18eb3-110">Il peut s'afficher sous la forme d'un graphique avec de nombreux points interconnectés tels que la figure suivante.</span><span class="sxs-lookup"><span data-stu-id="18eb3-110">It may display as a graph with many interconnected points such as following figure.</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Représentation visuelle de la mémoire" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="18eb3-112">Représentation visuelle de la mémoire</span><span class="sxs-lookup"><span data-stu-id="18eb3-112">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="18eb3-113">Un objet peut contenir de la mémoire de deux manières :</span><span class="sxs-lookup"><span data-stu-id="18eb3-113">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="18eb3-114">Directement par l'objet.</span><span class="sxs-lookup"><span data-stu-id="18eb3-114">Directly by the object.</span></span>  
*   <span data-ttu-id="18eb3-115">Implicitement en maintenant des références à d'autres objets, et par conséquent en empêchant leur élimination automatique par un garbage collector.</span><span class="sxs-lookup"><span data-stu-id="18eb3-115">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector.</span></span>  

<span data-ttu-id="18eb3-116">Lorsque vous [][DevtoolsMemoryProblemsHeapSnapshots] travaillez avec le panneau Mémoire dans DevTools \(un outil permettant d'examiner les problèmes de mémoire trouvés sous **Mémoire**\), vous pouvez vous retrouver en regardant différentes colonnes d'informations.</span><span class="sxs-lookup"><span data-stu-id="18eb3-116">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="18eb3-117">Deux éléments se démarquent par la taille **superficiele** et la **taille conservée,** mais que représentent-ils ?</span><span class="sxs-lookup"><span data-stu-id="18eb3-117">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tailles superficiels et conservées" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="18eb3-119">Tailles superficiels et conservées</span><span class="sxs-lookup"><span data-stu-id="18eb3-119">Shallow and Retained Size</span></span>  
:::image-end:::  

### <a name="shallow-size"></a><span data-ttu-id="18eb3-120">Taille superficiele</span><span class="sxs-lookup"><span data-stu-id="18eb3-120">Shallow size</span></span>  

<span data-ttu-id="18eb3-121">Il s'agit de la taille de la mémoire détenue par l'objet.</span><span class="sxs-lookup"><span data-stu-id="18eb3-121">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="18eb3-122">La mémoire des objets JavaScript classiques est réservée à leur description et au stockage des valeurs immédiates.</span><span class="sxs-lookup"><span data-stu-id="18eb3-122">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="18eb3-123">En règle générale, seuls les tableaux et les chaînes peuvent avoir une taille faible significative.</span><span class="sxs-lookup"><span data-stu-id="18eb3-123">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="18eb3-124">Toutefois, les chaînes et les tableaux externes ont souvent leur stockage principal dans la mémoire du renderer, exposant uniquement un petit objet wrapper sur le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18eb3-124">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="18eb3-125">La mémoire du renderer est l'ensemble de la mémoire du processus dans lequel une page inspectée est rendue : mémoire native + mémoire de tas JS de la page + mémoire de tas JS de tous les travailleurs dédiés démarrés par la page.</span><span class="sxs-lookup"><span data-stu-id="18eb3-125">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="18eb3-126">Néanmoins, même un petit objet peut contenir une grande quantité de mémoire indirectement, en empêchant d'autres objets d'être éliminés par le processus de collecte automatique de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="18eb3-126">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <a name="retained-size"></a><span data-ttu-id="18eb3-127">Taille conservée</span><span class="sxs-lookup"><span data-stu-id="18eb3-127">Retained size</span></span>  

<span data-ttu-id="18eb3-128">Il s'agit de la taille de la mémoire qui est libérée une fois que l'objet est supprimé avec les objets dépendants qui ont été rendues inaccessibles à partir des racines garbage **collector**.</span><span class="sxs-lookup"><span data-stu-id="18eb3-128">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots**.</span></span>  

<span data-ttu-id="18eb3-129">**Les racines** du Garbage Collector sont des **poignées créées** \(locales ou globales\) lors de la création d'une référence à partir de code natif à un objet JavaScript en dehors de V8.</span><span class="sxs-lookup"><span data-stu-id="18eb3-129">**Garbage Collector roots** are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="18eb3-130">Tous ces handles peuvent être trouvés dans un instantané de tas sous **des racines GC**Handle scope et GC  >  \*\*\*\* \*\*\*\*  >  **racines Global handles**.</span><span class="sxs-lookup"><span data-stu-id="18eb3-130">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="18eb3-131">Décrire les descripteurs de cette documentation sans plonger dans les détails de l'implémentation du navigateur peut prêter à confusion.</span><span class="sxs-lookup"><span data-stu-id="18eb3-131">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="18eb3-132">Les racines du garbage collector et les poignées ne sont pas des sujets dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="18eb3-132">Both Garbage Collector roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="18eb3-133">Il existe de nombreuses racines de garbage collector internes, dont la plupart ne sont pas intéressantes pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="18eb3-133">There are lots of internal Garbage Collector roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="18eb3-134">Du point de vue des applications, il existe les types de racines suivants.</span><span class="sxs-lookup"><span data-stu-id="18eb3-134">From the applications standpoint, there are the following kinds of roots.</span></span>  

*   <span data-ttu-id="18eb3-135">Objet global Window \(dans chaque iframe\).</span><span class="sxs-lookup"><span data-stu-id="18eb3-135">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="18eb3-136">Dans les captures instantanées de tas, le champ indique le nombre de références de propriétés sur le chemin de rétention le plus court `distance` de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="18eb3-136">In the heap snapshots, the `distance` field indicates the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="18eb3-137">Arborescence DOM du document, constituée de tous les nodes DOM natifs accessibles en parcourant le document.</span><span class="sxs-lookup"><span data-stu-id="18eb3-137">The document DOM tree, consisting of all native DOM nodes that are reachable by traversing the document.</span></span>  <span data-ttu-id="18eb3-138">Tous les nœuds n'ont pas de wrappers JavaScript, mais si un nœud possède un wrapper, le nœud est présent alors que le document est en cours d'utilisation.</span><span class="sxs-lookup"><span data-stu-id="18eb3-138">Not all of the nodes have JavaScript wrappers, but if a node has a wrapper, the node is alive while the document is alive.</span></span>  
*   <span data-ttu-id="18eb3-139">Parfois, les objets sont conservés par le contexte de débogage dans l'outil **Sources** et la **console,** par exemple après l'évaluation de la console.</span><span class="sxs-lookup"><span data-stu-id="18eb3-139">Sometimes objects are retained by the debug context in the **Sources** tool and the **Console**, such as after Console evaluation.</span></span>  <span data-ttu-id="18eb3-140">Créez des captures instantanées de tas avec un outil **console** effacé et aucun point d'arrêt actif dans le débogger de l'outil **Sources.**</span><span class="sxs-lookup"><span data-stu-id="18eb3-140">Create heap snapshots with a cleared **Console** tool and no active breakpoints in the debugger in the **Sources** tool.</span></span>

>[!TIP]
> <span data-ttu-id="18eb3-141">Avant de prendre une [][DevtoolsMemoryProblemsHeapSnapshots] capture instantanée du tas dans l'outil Mémoire, désactivez l'outil **Console** et désactivez les points d'arrêt dans l'outil **Sources.**</span><span class="sxs-lookup"><span data-stu-id="18eb3-141">Before taking a heap snapshot in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool, clear the **Console** tool and deactivate breakpoints in the **Sources** tool.</span></span>  <span data-ttu-id="18eb3-142">Pour effacer **l'outil Console,** exécutez la `clear()` méthode.</span><span class="sxs-lookup"><span data-stu-id="18eb3-142">To clear the **Console** tool, run the `clear()` method.</span></span>  

<span data-ttu-id="18eb3-143">Le graphique de mémoire commence par une racine, qui peut être l'objet du navigateur ou l'objet `window` `Global` d'Node.js module.</span><span class="sxs-lookup"><span data-stu-id="18eb3-143">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="18eb3-144">Vous ne contrôlez pas la façon dont l'objet racine est collecté.</span><span class="sxs-lookup"><span data-stu-id="18eb3-144">You do not control how the root object is garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Vous ne pouvez pas contrôler la façon dont l'objet racine est collecté." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="18eb3-146">Vous ne pouvez pas contrôler la façon dont l'objet racine est collecté.</span><span class="sxs-lookup"><span data-stu-id="18eb3-146">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="18eb3-147">Tout ce qui n'est pas accessible à partir de la racine récupère la garbage collected.</span><span class="sxs-lookup"><span data-stu-id="18eb3-147">Whatever is not reachable from the root gets garbage collected.</span></span>  

> [!NOTE]
> <span data-ttu-id="18eb3-148">Les [colonnes Taille superficiele et](#shallow-size) [Taille conservée](#retained-size) représentent toutes deux des données en octets.</span><span class="sxs-lookup"><span data-stu-id="18eb3-148">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <a name="objects-retaining-tree"></a><span data-ttu-id="18eb3-149">Objets conservant l'arborescence</span><span class="sxs-lookup"><span data-stu-id="18eb3-149">Objects retaining tree</span></span>  

<span data-ttu-id="18eb3-150">Le tas est un réseau d'objets interconnectés.</span><span class="sxs-lookup"><span data-stu-id="18eb3-150">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="18eb3-151">Dans le monde mathématique, cette structure est appelée graphique **ou** graphique mémoire.</span><span class="sxs-lookup"><span data-stu-id="18eb3-151">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="18eb3-152">Un graphique est construit à partir **de nods** connectés à l'aide de **bords,** qui sont tous deux attribués à des étiquettes.</span><span class="sxs-lookup"><span data-stu-id="18eb3-152">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="18eb3-153">**Les nodes** \(ou objets \) sont **étiquetés**à l'aide du nom de la fonction constructeur qui a été utilisée pour les créer. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="18eb3-153">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="18eb3-154">**Les bords** sont étiquetés à l'aide des noms des **propriétés.**</span><span class="sxs-lookup"><span data-stu-id="18eb3-154">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="18eb3-155">Découvrez [comment enregistrer un profil à l'aide du profileur de tas.][DevtoolsMemoryProblemsHeapSnapshots]</span><span class="sxs-lookup"><span data-stu-id="18eb3-155">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="18eb3-156">Dans la figure suivante, certains des éléments notables [][DevtoolsMemoryProblemsHeapSnapshots] de l'enregistrement instantané de tas dans l'outil Mémoire incluent la distance : la distance par rapport à la racine du garbage collector.</span><span class="sxs-lookup"><span data-stu-id="18eb3-156">In the following figure, some of the notable things in the Heap Snapshot recording in the [Memory][DevtoolsMemoryProblemsHeapSnapshots] tool include distance:  the distance from the Garbage Collector root.</span></span>  <span data-ttu-id="18eb3-157">Si presque tous les objets du même type sont à la même distance et que certains d'entre eux sont à une plus grande distance, cela vaut la peine d'examiner ce point.</span><span class="sxs-lookup"><span data-stu-id="18eb3-157">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distance par rapport à la racine" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="18eb3-159">Distance par rapport à la racine</span><span class="sxs-lookup"><span data-stu-id="18eb3-159">Distance from root</span></span>  
:::image-end:::  

## <a name="dominators"></a><span data-ttu-id="18eb3-160">Dominants</span><span class="sxs-lookup"><span data-stu-id="18eb3-160">Dominators</span></span>  

<span data-ttu-id="18eb3-161">Les objets dominants sont constitués d'une arborescence, car chaque objet possède exactement un seul dominant.</span><span class="sxs-lookup"><span data-stu-id="18eb3-161">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="18eb3-162">Un dominant d'un objet peut ne pas avoir de références directes à un objet qu'il dirige ; autrement dit, l'arborescence du sous-arbre n'est pas une arborescence couvrante du graphique.</span><span class="sxs-lookup"><span data-stu-id="18eb3-162">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="18eb3-163">Dans la figure suivante, l'instruction suivante est vraie.</span><span class="sxs-lookup"><span data-stu-id="18eb3-163">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="18eb3-164">Nœud 1 nœud 2</span><span class="sxs-lookup"><span data-stu-id="18eb3-164">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="18eb3-165">Nœud 2 nœuds 3, 4 et 6</span><span class="sxs-lookup"><span data-stu-id="18eb3-165">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="18eb3-166">Nœud 3 nœud 5</span><span class="sxs-lookup"><span data-stu-id="18eb3-166">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="18eb3-167">Nœud 5 nœud 8</span><span class="sxs-lookup"><span data-stu-id="18eb3-167">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="18eb3-168">Nœud 6 nœud 7</span><span class="sxs-lookup"><span data-stu-id="18eb3-168">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Structure de l'arborescence de l'dominant" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="18eb3-170">Structure de l'arborescence de l'dominant</span><span class="sxs-lookup"><span data-stu-id="18eb3-170">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="18eb3-171">Dans la figure suivante, le nœud est l'en-avant-première de , mais il existe également dans chaque chemin simple du garbage `#3` `#10` collector à `#7` `#10` .</span><span class="sxs-lookup"><span data-stu-id="18eb3-171">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector to `#10`.</span></span>  <span data-ttu-id="18eb3-172">Par conséquent, un objet B est le résorbateur d'un objet A si B existe dans chaque chemin d'accès simple de la racine à l'objet A.</span><span class="sxs-lookup"><span data-stu-id="18eb3-172">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Illustration de l'animation de l'animation de l'animation" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="18eb3-174">Illustration de l'animation de l'animation de l'animation</span><span class="sxs-lookup"><span data-stu-id="18eb3-174">Animated dominator illustration</span></span>  
:::image-end:::  

## <a name="v8-specifics"></a><span data-ttu-id="18eb3-175">Spécificités V8</span><span class="sxs-lookup"><span data-stu-id="18eb3-175">V8 specifics</span></span>  

<span data-ttu-id="18eb3-176">Lors du profilage de la mémoire, il est utile de comprendre pourquoi les captures instantanées de tas semblent d'une certaine façon.</span><span class="sxs-lookup"><span data-stu-id="18eb3-176">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="18eb3-177">Cette section décrit certaines rubriques relatives à la mémoire qui correspondent spécifiquement à la machine virtuelle **JavaScript V8** \(V8 V8 VM ou VM\).</span><span class="sxs-lookup"><span data-stu-id="18eb3-177">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <a name="javascript-object-representation"></a><span data-ttu-id="18eb3-178">Représentation d'objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="18eb3-178">JavaScript object representation</span></span>  

<span data-ttu-id="18eb3-179">Il existe trois types primitifs :</span><span class="sxs-lookup"><span data-stu-id="18eb3-179">There are three primitive types:</span></span>  

*   <span data-ttu-id="18eb3-180">Nombres \(par exemple `3.14159...` \)</span><span class="sxs-lookup"><span data-stu-id="18eb3-180">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="18eb3-181">Booléens \( `true` ou `false` \)</span><span class="sxs-lookup"><span data-stu-id="18eb3-181">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="18eb3-182">Chaînes \(par exemple `"Werner Heisenberg"` \)</span><span class="sxs-lookup"><span data-stu-id="18eb3-182">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="18eb3-183">Les primitives ne peuvent pas référencer d'autres valeurs et sont toujours des feuilles ou des nodes terminaux.</span><span class="sxs-lookup"><span data-stu-id="18eb3-183">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="18eb3-184">**Les** nombres peuvent être stockés sous l'une ou l'autre des façons :</span><span class="sxs-lookup"><span data-stu-id="18eb3-184">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="18eb3-185">valeurs d'un nombre integer 31 bits immédiatement appelées petits **nombres d'nombres integers** \(**SMI**s\) ou</span><span class="sxs-lookup"><span data-stu-id="18eb3-185">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="18eb3-186">objets de tas, appelés nombres **de tas**.</span><span class="sxs-lookup"><span data-stu-id="18eb3-186">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="18eb3-187">Les nombres de tas sont utilisés pour stocker les valeurs qui ne s'intègrent pas dans le formulaire SMI, telles que les **doubles,** ou lorsqu'une valeur doit être encadrée, \*\*\*\* par exemple la définition de propriétés sur celui-ci.</span><span class="sxs-lookup"><span data-stu-id="18eb3-187">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="18eb3-188">**Les** chaînes peuvent être stockées dans :</span><span class="sxs-lookup"><span data-stu-id="18eb3-188">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="18eb3-189">le **tas de la VM,** ou</span><span class="sxs-lookup"><span data-stu-id="18eb3-189">the **VM heap**, or</span></span>
*   <span data-ttu-id="18eb3-190">externe dans la **mémoire du renderer**.</span><span class="sxs-lookup"><span data-stu-id="18eb3-190">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="18eb3-191">Un **objet wrapper** est créé et utilisé pour accéder au stockage externe où, par exemple, les sources de script et d'autres contenus reçus à partir du Web sont stockés, plutôt que copiés sur le tas de l'environnement de ligne de disque.</span><span class="sxs-lookup"><span data-stu-id="18eb3-191">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="18eb3-192">La mémoire pour les nouveaux objets JavaScript est allouée à partir d'un tas JavaScript dédié \(ou d'un tas **de vm**\).</span><span class="sxs-lookup"><span data-stu-id="18eb3-192">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="18eb3-193">Ces objets sont gérés par le garbage collector dans V8 et, par conséquent, restent en vie tant qu'il existe au moins une référence forte à ces objets.</span><span class="sxs-lookup"><span data-stu-id="18eb3-193">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="18eb3-194">Tout ce qui ne se trouve pas dans le tas JavaScript est appelé **un objet natif.**</span><span class="sxs-lookup"><span data-stu-id="18eb3-194">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="18eb3-195">Les objets natifs, contrairement aux objets tas, ne sont pas gérés par le garbage collector V8 tout au long de leur durée de vie et peuvent uniquement être accessibles à partir de JavaScript à l'aide de l'objet wrapper JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18eb3-195">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="18eb3-196">**La chaîne** Cons est un objet qui se compose de paires de chaînes stockées, puis jointes, et est le résultat de la concatenation.</span><span class="sxs-lookup"><span data-stu-id="18eb3-196">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="18eb3-197">La jointation du contenu de la **chaîne cons se** produit uniquement selon les besoins.</span><span class="sxs-lookup"><span data-stu-id="18eb3-197">The joining of the **cons string** contents occurs only as needed.</span></span>  <span data-ttu-id="18eb3-198">Par exemple, lorsqu'une sous-chaîne d'une chaîne jointe doit être construite.</span><span class="sxs-lookup"><span data-stu-id="18eb3-198">For example, when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="18eb3-199">Par exemple, si vous concaténer et , vous obtenez une chaîne qui représente le `a` `b` résultat de la `(a, b)` concaténation.</span><span class="sxs-lookup"><span data-stu-id="18eb3-199">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="18eb3-200">Si vous avez concaté ultérieurement `d` avec ce résultat, vous obtenez une autre **chaîne de inconvénients**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="18eb3-200">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="18eb3-201">**Le** tableau est un objet avec des clés numériques.</span><span class="sxs-lookup"><span data-stu-id="18eb3-201">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="18eb3-202">**Les tableaux** sont largement utilisés dans la V8 VM pour stocker de grandes quantités de données.</span><span class="sxs-lookup"><span data-stu-id="18eb3-202">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="18eb3-203">Les ensembles de paires clé-valeur, tels que les dictionnaires, sont backed up par **des tableaux**.</span><span class="sxs-lookup"><span data-stu-id="18eb3-203">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="18eb3-204">Un objet JavaScript classique est stocké comme un seul des deux types **de tableau** :</span><span class="sxs-lookup"><span data-stu-id="18eb3-204">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="18eb3-205">propriétés nommées et</span><span class="sxs-lookup"><span data-stu-id="18eb3-205">named properties, and</span></span>  
*   <span data-ttu-id="18eb3-206">éléments numériques</span><span class="sxs-lookup"><span data-stu-id="18eb3-206">numeric elements</span></span>  

<span data-ttu-id="18eb3-207">Lorsqu'il existe un petit nombre de propriétés, les propriétés sont stockées en interne dans l'objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18eb3-207">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="18eb3-208">**Map** est un objet qui décrit à la fois le type d'objet et la disposition.</span><span class="sxs-lookup"><span data-stu-id="18eb3-208">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="18eb3-209">Par exemple, les cartes sont utilisées pour décrire les hiérarchies d'objets implicites pour un [accès rapide aux propriétés.][V8FastProperties]</span><span class="sxs-lookup"><span data-stu-id="18eb3-209">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <a name="object-groups"></a><span data-ttu-id="18eb3-210">Groupes d'objets</span><span class="sxs-lookup"><span data-stu-id="18eb3-210">Object groups</span></span>  

<span data-ttu-id="18eb3-211">Chaque **groupe d'objets natifs** est composé d'objets qui tiennent des références mutuelles les uns aux autres.</span><span class="sxs-lookup"><span data-stu-id="18eb3-211">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="18eb3-212">Considérons, par exemple, une sous-arbre DOM où chaque nœud possède un lien vers le parent relatif et des liens vers l'enfant suivant et le frère suivant, ce qui a pour effet de former un graphique connecté.</span><span class="sxs-lookup"><span data-stu-id="18eb3-212">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="18eb3-213">Les objets natifs ne sont pas représentés dans le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="18eb3-213">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="18eb3-214">L'absence de représentation est la raison pour laquelle les objets natifs ont une taille nulle.</span><span class="sxs-lookup"><span data-stu-id="18eb3-214">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="18eb3-215">Au lieu de cela, les objets wrapper sont créés.</span><span class="sxs-lookup"><span data-stu-id="18eb3-215">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="18eb3-216">Chaque objet wrapper contient une référence à l'objet natif correspondant, pour rediriger les commandes vers celui-ci.</span><span class="sxs-lookup"><span data-stu-id="18eb3-216">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="18eb3-217">À son tour, un groupe d'objets contient des objets wrapper.</span><span class="sxs-lookup"><span data-stu-id="18eb3-217">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="18eb3-218">Toutefois, cela ne crée pas de cycle non récollectable, car le Garbage Collector est suffisamment intelligent pour libérer les groupes d'objets dont les wrappers ne sont plus référencés.</span><span class="sxs-lookup"><span data-stu-id="18eb3-218">However, this does not create an uncollectable cycle, as Garbage Collector is smart enough to release object groups whose wrappers are no longer referenced.</span></span>  <span data-ttu-id="18eb3-219">Mais l'oubli de libérer un seul wrapper contient le groupe entier et les wrappers associés.</span><span class="sxs-lookup"><span data-stu-id="18eb3-219">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="18eb3-220">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="18eb3-220">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Comment enregistrer des instantanés de tas | Documents Microsoft"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriétés rapides dans V8 | V8"  

> [!NOTE]
> <span data-ttu-id="18eb3-223">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18eb3-223">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="18eb3-224">La page d'origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) et est co-auteure par [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="18eb3-224">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="18eb3-226">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="18eb3-226">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
