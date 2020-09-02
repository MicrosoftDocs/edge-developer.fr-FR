---
title: Terminologie de mémoire
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: cb258135b7b3c931116d84b1e9b7a548a2b58a6d
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986244"
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

# <span data-ttu-id="44c0b-103">Terminologie de mémoire</span><span class="sxs-lookup"><span data-stu-id="44c0b-103">Memory Terminology</span></span>  

<span data-ttu-id="44c0b-104">Cette section décrit les termes courants utilisés en analyse de la mémoire et est applicable à un large éventail d’outils de profilage de mémoire pour différentes langues.</span><span class="sxs-lookup"><span data-stu-id="44c0b-104">This section describes common terms used in memory analysis, and is applicable to a variety of memory profiling tools for different languages.</span></span>  

<span data-ttu-id="44c0b-105">Les termes et notions décrits ici font référence au [panneau mémoire][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="44c0b-105">The terms and notions described here refer to the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="44c0b-106">Si vous avez déjà utilisé le Java, .NET ou un autre profileur de mémoire, il peut s’agir d’un rappel.</span><span class="sxs-lookup"><span data-stu-id="44c0b-106">If you have ever worked with either the Java, .NET, or some other memory profiler, then this may be a refresher.</span></span>  

## <span data-ttu-id="44c0b-107">Tailles d’objets</span><span class="sxs-lookup"><span data-stu-id="44c0b-107">Object sizes</span></span>  

<span data-ttu-id="44c0b-108">Considérez la mémoire comme un graphique avec les types primitifs \ (comme les nombres et les chaînes \) et les objets \ (matrices associatives \).</span><span class="sxs-lookup"><span data-stu-id="44c0b-108">Think of memory as a graph with primitive types \(like numbers and strings\) and objects \(associative arrays\).</span></span>  <span data-ttu-id="44c0b-109">Elle peut être représentée visuellement sous forme de graphique à l’aide d’un certain nombre de points interconnectés comme suit:</span><span class="sxs-lookup"><span data-stu-id="44c0b-109">It might visually be represented as a graph with a number of interconnected points as follows:</span></span>  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Représentation visuelle de la mémoire" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   <span data-ttu-id="44c0b-111">Représentation visuelle de la mémoire</span><span class="sxs-lookup"><span data-stu-id="44c0b-111">Visual representation of memory</span></span>  
:::image-end:::  

<span data-ttu-id="44c0b-112">Un objet risque de contenir de la mémoire de deux manières:</span><span class="sxs-lookup"><span data-stu-id="44c0b-112">An object may hold memory in two ways:</span></span>  

*   <span data-ttu-id="44c0b-113">Directement par l’objet.</span><span class="sxs-lookup"><span data-stu-id="44c0b-113">Directly by the object.</span></span>  
*   <span data-ttu-id="44c0b-114">Par le biais d’un nettoyage de la mémoire, le nettoyage de la mémoire et la suppression**automatique de ces** objets sont implicites.</span><span class="sxs-lookup"><span data-stu-id="44c0b-114">Implicitly by holding references to other objects, and therefore preventing those objects from being automatically disposed by a garbage collector \(**GC** for short\).</span></span>  

<span data-ttu-id="44c0b-115">Lorsque vous travaillez avec le panneau [mémoire][DevtoolsMemoryProblemsHeapSnapshots] dans devtools \ (outil permettant d’identifier les problèmes de mémoire détectés dans la **mémoire**), vous pouvez vous présenter quelques colonnes d’information différentes.</span><span class="sxs-lookup"><span data-stu-id="44c0b-115">When working with the [Memory][DevtoolsMemoryProblemsHeapSnapshots] panel in DevTools \(a tool for investigating memory issues found under **Memory**\), you may find yourself looking at a few different columns of information.</span></span>  <span data-ttu-id="44c0b-116">Deux éléments qui ressortent sont les suivants: **taille superficielle** et **taille préservée**, mais qu’est-ce que cela représente?</span><span class="sxs-lookup"><span data-stu-id="44c0b-116">Two that stand out are **Shallow Size** and **Retained Size**, but what do these represent?</span></span>  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Taille superficielle et conservée" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   <span data-ttu-id="44c0b-118">Taille superficielle et conservée</span><span class="sxs-lookup"><span data-stu-id="44c0b-118">Shallow and Retained Size</span></span>  
:::image-end:::  

### <span data-ttu-id="44c0b-119">Taille superficielle</span><span class="sxs-lookup"><span data-stu-id="44c0b-119">Shallow size</span></span>  

<span data-ttu-id="44c0b-120">Il s’agit de la taille de mémoire qui est maintenue par l’objet.</span><span class="sxs-lookup"><span data-stu-id="44c0b-120">This is the size of memory that is held by the object.</span></span>  

<span data-ttu-id="44c0b-121">Une mémoire est réservée aux objets JavaScript typiques et pour le stockage des valeurs immédiates.</span><span class="sxs-lookup"><span data-stu-id="44c0b-121">Typical JavaScript objects have some memory reserved for their description and for storing immediate values.</span></span>  <span data-ttu-id="44c0b-122">En règle générale, seuls les tableaux et les chaînes peuvent avoir une taille superficielle significative.</span><span class="sxs-lookup"><span data-stu-id="44c0b-122">Usually, only arrays and strings are able to have a significant shallow size.</span></span>  <span data-ttu-id="44c0b-123">Toutefois, les chaînes et les tableaux externes disposent souvent de leur stockage principal dans la mémoire du convertisseur, en exposant uniquement un petit objet wrapper sur le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44c0b-123">However, strings and external arrays often have their main storage in renderer memory, exposing only a small wrapper object on the JavaScript heap.</span></span>  

<span data-ttu-id="44c0b-124">La mémoire du convertisseur correspond à toute la mémoire du processus sur lequel une page inspectée est affichée: mémoire Native + pile de tas JS de la mémoire du tas page + JS de tous les travailleurs dédiés démarrés par la page.</span><span class="sxs-lookup"><span data-stu-id="44c0b-124">Renderer memory is all memory of the process where an inspected page is rendered: native memory + JS heap memory of the page + JS heap memory of all dedicated workers started by the page.</span></span>  <span data-ttu-id="44c0b-125">Néanmoins, même un petit objet est en mesure de mettre en place une grande quantité de mémoire, en empêchant d’autres objets d’être supprimés par le processus automatique de nettoyage de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="44c0b-125">Nevertheless, even a small object is able to hold a large amount of memory indirectly, by preventing other objects from being disposed of by the automatic garbage collection process.</span></span>  

### <span data-ttu-id="44c0b-126">Taille retenue</span><span class="sxs-lookup"><span data-stu-id="44c0b-126">Retained size</span></span>  

<span data-ttu-id="44c0b-127">Il s’agit de la taille de mémoire qui est libérée une fois que l’objet est supprimé en même temps que les objets dépendants qui ont été rendus injoignables des **racines de nettoyage** de la mémoire \ (racines du CG).</span><span class="sxs-lookup"><span data-stu-id="44c0b-127">This is the size of memory that is freed once the object is deleted along with the dependent objects that were made unreachable from **Garbage Collector roots** \(GC roots\) .</span></span>  

<span data-ttu-id="44c0b-128">Les **racines de nettoyage** de la mémoire (racines de catalogue) sont composées de **Handles** créés \ (local ou global \) lors de la création d’une référence à partir du code natif à un objet JavaScript en dehors de V8.</span><span class="sxs-lookup"><span data-stu-id="44c0b-128">**Garbage Collector roots** \(GC roots\) are made up of **handles** that are created \(either local or global\) when making a reference from native code to a JavaScript object outside of V8.</span></span>  <span data-ttu-id="44c0b-129">Tous ces handles sont disponibles dans une capture d’instantané **GC roots**de tas sous les descripteurs d'  >  **étendue** et de gestionnaires de racines de **catalogue**  >  **Global**.</span><span class="sxs-lookup"><span data-stu-id="44c0b-129">All such handles may be found within a heap snapshot under **GC roots** > **Handle scope** and **GC roots** > **Global handles**.</span></span>  <span data-ttu-id="44c0b-130">La description des descripteurs de cette documentation sans plongée dans les détails de l’implémentation du navigateur risque d’être confus.</span><span class="sxs-lookup"><span data-stu-id="44c0b-130">Describing the handles in this documentation without diving into details of the browser implementation may be confusing.</span></span>  <span data-ttu-id="44c0b-131">Les racines de nettoyage de la mémoire (CG) et les poignées ne sont pas des éléments dont vous devez vous soucier.</span><span class="sxs-lookup"><span data-stu-id="44c0b-131">Both Garbage Collector (GC) roots and the handles are not something you need to worry about.</span></span>  

<span data-ttu-id="44c0b-132">Il existe de nombreuses racines de GC internes, qui ne sont pas pertinentes pour les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="44c0b-132">There are lots of internal GC roots, most of which are not interesting for the users.</span></span>  <span data-ttu-id="44c0b-133">Du point de vue des applications, il existe des types de racines suivants.</span><span class="sxs-lookup"><span data-stu-id="44c0b-133">From the applications standpoint there are following kinds of roots.</span></span>  

*   <span data-ttu-id="44c0b-134">Objet Global Window \ (dans chaque IFRAME).</span><span class="sxs-lookup"><span data-stu-id="44c0b-134">Window global object \(in each iframe\).</span></span>  <span data-ttu-id="44c0b-135">Il existe un champ distance dans les instantanés de tas, qui est le nombre de références de propriété sur le chemin de conservation le plus court à partir de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="44c0b-135">There is a distance field in the heap snapshots which is the number of property references on the shortest retaining path from the window.</span></span>  
*   <span data-ttu-id="44c0b-136">L’arborescence DOM du document se compose de tous les nœuds DOM natifs accessibles en parcourant le document.</span><span class="sxs-lookup"><span data-stu-id="44c0b-136">Document DOM tree consisting of all native DOM nodes reachable by traversing the document.</span></span>  <span data-ttu-id="44c0b-137">Tous les nœuds ne peuvent pas avoir de wrappers JS, mais si un nœud possède un wrapper, il est actif lorsque le document est actif.</span><span class="sxs-lookup"><span data-stu-id="44c0b-137">Not all of the nodes may have JS wrappers but if a node has a wrapper, it is alive while the document is alive.</span></span>  
*   <span data-ttu-id="44c0b-138">Parfois, les objets peuvent être conservés par le contexte du débogueur dans le panneau **sources** et la **console** \ (par exemple, après l’évaluation de la console).</span><span class="sxs-lookup"><span data-stu-id="44c0b-138">Sometimes objects may be retained by the debugger context in the **Sources** panel and the **Console** \(for example after Console evaluation\).</span></span>  <span data-ttu-id="44c0b-139">Créez des captures d’écran de tas à l’aide d’un panneau de **console** pointé et aucun point d’arrêt actif dans le débogueur dans le panneau **sources** .</span><span class="sxs-lookup"><span data-stu-id="44c0b-139">Create heap snapshots with a cleared **Console** panel and no active breakpoints in the debugger in the **Sources** panel.</span></span>

>[!TIP]
> <span data-ttu-id="44c0b-140">Effacez le panneau de la **console** en exécutant `clear()` et désactivez les points d’arrêt dans le panneau **sources** avant de prendre une capture de tas dans le [panneau mémoire][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="44c0b-140">Clear the **Console** panel by running `clear()` and deactivate breakpoints in the **Sources** panel before taking a heap snapshot in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots].</span></span>

<span data-ttu-id="44c0b-141">Le graphique de mémoire commence par une racine, qui est éventuellement l' `window` objet du navigateur ou l' `Global` objet d’un module de Node.js.</span><span class="sxs-lookup"><span data-stu-id="44c0b-141">The memory graph starts with a root, which may be the `window` object of the browser or the `Global` object of a Node.js module.</span></span>  <span data-ttu-id="44c0b-142">Vous ne contrôlez pas la façon dont cet objet racine est récupéré par le garbage collector (pgcd).</span><span class="sxs-lookup"><span data-stu-id="44c0b-142">You do not control how this root object is garbage collected (GCd).</span></span>  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Vous ne pouvez pas contrôler la façon dont l’objet racine est récupéré par le garbage collector." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   <span data-ttu-id="44c0b-144">Vous ne pouvez pas contrôler la façon dont l’objet racine est récupéré par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="44c0b-144">You are not able to control how the root object is garbage collected.</span></span>  
:::image-end:::  

<span data-ttu-id="44c0b-145">Tout ce qui n’est pas accessible à partir de la racine récupère le nettoyage de la mémoire \ (pgcd \).</span><span class="sxs-lookup"><span data-stu-id="44c0b-145">Whatever is not reachable from the root gets garbage collected \(GCd\).</span></span>  

> [!NOTE]
> <span data-ttu-id="44c0b-146">Les colonnes [taille superficielle](#shallow-size) et [taille retenue](#retained-size) représentent les données en octets.</span><span class="sxs-lookup"><span data-stu-id="44c0b-146">Both the [Shallow size](#shallow-size) and [Retained size](#retained-size) columns represent data in bytes.</span></span>  

## <span data-ttu-id="44c0b-147">Arborescence conservation d’objets</span><span class="sxs-lookup"><span data-stu-id="44c0b-147">Objects retaining tree</span></span>  

<span data-ttu-id="44c0b-148">Le tas est un réseau d’objets interconnectés.</span><span class="sxs-lookup"><span data-stu-id="44c0b-148">The heap is a network of interconnected objects.</span></span>  <span data-ttu-id="44c0b-149">Dans le monde mathématique, cette structure s’appelle un graphique **graphique** ou de mémoire.</span><span class="sxs-lookup"><span data-stu-id="44c0b-149">In the mathematical world, this structure is called a **graph** or memory graph.</span></span>  <span data-ttu-id="44c0b-150">Un graphique est créé à partir de **nœuds** connectés par le biais de **bords**, qui sont des étiquettes données.</span><span class="sxs-lookup"><span data-stu-id="44c0b-150">A graph is constructed from **nodes** connected by means of **edges**, both of which are given labels.</span></span>  

*   <span data-ttu-id="44c0b-151">Les **nœuds** \ (ou **objets**\) sont étiquetés à l’aide du nom de la fonction **constructeur** utilisée pour les générer.</span><span class="sxs-lookup"><span data-stu-id="44c0b-151">**Nodes** \(or **objects**\) are labelled using the name of the **constructor** function that was used to build them.</span></span>  
*   <span data-ttu-id="44c0b-152">Les **bords** sont étiquetés à l’aide du nom des **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="44c0b-152">**Edges** are labelled using the names of **properties**.</span></span>  

<span data-ttu-id="44c0b-153">Découvrez [Comment enregistrer un profil à l’aide du profileur de tas][DevtoolsMemoryProblemsHeapSnapshots].</span><span class="sxs-lookup"><span data-stu-id="44c0b-153">Learn [how to record a profile using the Heap Profiler][DevtoolsMemoryProblemsHeapSnapshots].</span></span>  <span data-ttu-id="44c0b-154">Dans l’illustration ci-dessous, certains des éléments percutants que vous pouvez voir dans l’enregistrement instantané de tas dans le [panneau mémoire][DevtoolsMemoryProblemsHeapSnapshots] incluent la distance: la distance du récupérateur de mémoire (CG \).</span><span class="sxs-lookup"><span data-stu-id="44c0b-154">In the following figure, some of the eye-catching things that you may see in the Heap Snapshot recording in the [Memory panel][DevtoolsMemoryProblemsHeapSnapshots] include distance:  the distance from the Garbage Collector \(GC\) root.</span></span>  <span data-ttu-id="44c0b-155">Si la plupart des objets du même type se trouvent à la même distance et qu’ils sont à une distance plus importante, cela peut s’avérer utile.</span><span class="sxs-lookup"><span data-stu-id="44c0b-155">If almost all the objects of the same type are at the same distance, and a few are at a bigger distance, that is something worth investigating.</span></span>  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distance par rapport à la racine" lightbox="../media/memory-problems-root.msft.png":::
   <span data-ttu-id="44c0b-157">Distance par rapport à la racine</span><span class="sxs-lookup"><span data-stu-id="44c0b-157">Distance from root</span></span>  
:::image-end:::  

## <span data-ttu-id="44c0b-158">Dominators</span><span class="sxs-lookup"><span data-stu-id="44c0b-158">Dominators</span></span>  

<span data-ttu-id="44c0b-159">Les objets Dominator sont composés d’une structure arborescente, car chaque objet a exactement un Dominator.</span><span class="sxs-lookup"><span data-stu-id="44c0b-159">Dominator objects are comprised of a tree structure because each object has exactly one dominator.</span></span>  <span data-ttu-id="44c0b-160">Un Dominator d’un objet est susceptible de ne pas faire référence directe à un objet qu’il prédomine; c’est-à-dire que l’arborescence de Dominator n’est pas une arborescence fractionnée du graphique.</span><span class="sxs-lookup"><span data-stu-id="44c0b-160">A dominator of an object may lack direct references to an object it dominates; that is, the tree of the dominator is not a spanning tree of the graph.</span></span>  

<span data-ttu-id="44c0b-161">Dans l’illustration suivante, l’instruction suivante a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="44c0b-161">In the following figure, the following statement are true.</span></span>  

*   <span data-ttu-id="44c0b-162">Le nœud 1 prédomine le nœud 2</span><span class="sxs-lookup"><span data-stu-id="44c0b-162">Node 1 dominates node 2</span></span>  
*   <span data-ttu-id="44c0b-163">Le nœud 2 prédomine les nœuds 3, 4 et 6</span><span class="sxs-lookup"><span data-stu-id="44c0b-163">Node 2 dominates nodes 3, 4 and 6</span></span>  
*   <span data-ttu-id="44c0b-164">Le nœud 3 prédomine le nœud 5</span><span class="sxs-lookup"><span data-stu-id="44c0b-164">Node 3 dominates node 5</span></span>  
*   <span data-ttu-id="44c0b-165">Le nœud 5 prédomine du nœud 8</span><span class="sxs-lookup"><span data-stu-id="44c0b-165">Node 5 dominates node 8</span></span>  
*   <span data-ttu-id="44c0b-166">Le nœud 6 prédomine le nœud 7</span><span class="sxs-lookup"><span data-stu-id="44c0b-166">Node 6 dominates node 7</span></span>  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Structure de l’arborescence Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   <span data-ttu-id="44c0b-168">Structure de l’arborescence Dominator</span><span class="sxs-lookup"><span data-stu-id="44c0b-168">Dominator tree structure</span></span>  
:::image-end:::  

<span data-ttu-id="44c0b-169">Dans l’illustration suivante, `#3` le nœud est le Dominator `#10` , mais `#7` il existe également dans chaque chemin d’accès simple de l’opération de nettoyage de la mémoire `#10` .</span><span class="sxs-lookup"><span data-stu-id="44c0b-169">In the following figure, node `#3` is the dominator of `#10`, but `#7` also exists in every simple path from Garbage Collector \(GC\) to `#10`.</span></span>  <span data-ttu-id="44c0b-170">Par conséquent, un objet B est un Dominator d’un objet A, si B existe dans chaque chemin simple de la racine à l’objet A.</span><span class="sxs-lookup"><span data-stu-id="44c0b-170">Therefore, an object B is a dominator of an object A if B exists in every simple path from the root to the object A.</span></span>  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Illustration Dominator animée" lightbox="../media/memory-problems-dominators.msft.gif":::
   <span data-ttu-id="44c0b-172">Illustration Dominator animée</span><span class="sxs-lookup"><span data-stu-id="44c0b-172">Animated dominator illustration</span></span>  
:::image-end:::  

## <span data-ttu-id="44c0b-173">V8 spécificités</span><span class="sxs-lookup"><span data-stu-id="44c0b-173">V8 specifics</span></span>  

<span data-ttu-id="44c0b-174">Lorsque vous configurez la mémoire, il est utile de comprendre pourquoi les instantanés de tas se présentent de manière spécifique.</span><span class="sxs-lookup"><span data-stu-id="44c0b-174">When profiling memory, it is helpful to understand why heap snapshots look a certain way.</span></span>  <span data-ttu-id="44c0b-175">Cette section décrit certaines rubriques relatives à la mémoire correspondant spécifiquement à la **machine virtuelle JavaScript V8** (VM ou VM).</span><span class="sxs-lookup"><span data-stu-id="44c0b-175">This section describes some memory-related topics specifically corresponding to the **V8 JavaScript virtual machine** \(V8 VM or VM\).</span></span>  

### <span data-ttu-id="44c0b-176">Représentation d’objet JavaScript</span><span class="sxs-lookup"><span data-stu-id="44c0b-176">JavaScript object representation</span></span>  

<span data-ttu-id="44c0b-177">Il existe trois types de primitives:</span><span class="sxs-lookup"><span data-stu-id="44c0b-177">There are three primitive types:</span></span>  

*   <span data-ttu-id="44c0b-178">Numéros \ (par exemple `3.14159...` , \)</span><span class="sxs-lookup"><span data-stu-id="44c0b-178">Numbers \(for example `3.14159...`\)</span></span>  
*   <span data-ttu-id="44c0b-179">Booléens \ ( `true` ou `false` \)</span><span class="sxs-lookup"><span data-stu-id="44c0b-179">Booleans \(`true` or `false`\)</span></span>  
*   <span data-ttu-id="44c0b-180">Chaînes \ (par exemple `"Werner Heisenberg"` , \)</span><span class="sxs-lookup"><span data-stu-id="44c0b-180">Strings \(for example `"Werner Heisenberg"`\)</span></span>  

<span data-ttu-id="44c0b-181">Les primitives ne peuvent pas faire référence à d’autres valeurs et sont toujours des feuilles ou des nœuds de terminaison.</span><span class="sxs-lookup"><span data-stu-id="44c0b-181">Primitives are not able to reference other values and are always leafs or terminating nodes.</span></span>  

<span data-ttu-id="44c0b-182">Les **numéros** peuvent être stockés comme suit:</span><span class="sxs-lookup"><span data-stu-id="44c0b-182">**Numbers** are able to be stored as either:</span></span>  

*   <span data-ttu-id="44c0b-183">valeurs entières de 31 bits immédiate appelées **petits entiers** \ (**SMI**s \), ou</span><span class="sxs-lookup"><span data-stu-id="44c0b-183">an immediate 31-bit integer values called **small integers** \(**SMI**s\), or</span></span>  
*   <span data-ttu-id="44c0b-184">objets tas, appelés numéros de **tas**.</span><span class="sxs-lookup"><span data-stu-id="44c0b-184">heap objects, referred to as **heap numbers**.</span></span> <span data-ttu-id="44c0b-185">Les numéros de tas permettent de stocker des valeurs qui ne s’intègrent pas dans le formulaire SMI, par exemple des **doublons**ou lorsqu’une valeur doit être **boxed**, par exemple pour définir des propriétés sur celle-ci.</span><span class="sxs-lookup"><span data-stu-id="44c0b-185">Heap numbers are used for storing values that do not fit into the SMI form, such as **doubles**, or when a value needs to be **boxed**, such as setting properties on it.</span></span>  

<span data-ttu-id="44c0b-186">Les **chaînes** peuvent être stockées dans l’un ou l’autre des éléments suivants:</span><span class="sxs-lookup"><span data-stu-id="44c0b-186">**Strings** are able to be stored in either:</span></span>  

*   <span data-ttu-id="44c0b-187">le **tas de l’ordinateur virtuel**, ou</span><span class="sxs-lookup"><span data-stu-id="44c0b-187">the **VM heap**, or</span></span>
*   <span data-ttu-id="44c0b-188">en externe dans la **mémoire du convertisseur**.</span><span class="sxs-lookup"><span data-stu-id="44c0b-188">externally in the **memory of the renderer**.</span></span>  <span data-ttu-id="44c0b-189">Un **objet wrapper** est créé et utilisé pour accéder à l’espace de stockage externe (par exemple, les sources de script et le contenu reçu à partir du Web sont stockés, au lieu d’être copiés sur le tas de l’ordinateur virtuel).</span><span class="sxs-lookup"><span data-stu-id="44c0b-189">A **wrapper object** is created and used for accessing external storage where, for example, script sources and other content that is received from the Web is stored, rather than copied onto the VM heap.</span></span>

<span data-ttu-id="44c0b-190">La mémoire pour les nouveaux objets JavaScript est allouée à partir d’un tas JavaScript dédié \ (ou du **tas du VM**).</span><span class="sxs-lookup"><span data-stu-id="44c0b-190">Memory for new JavaScript objects is allocated from a dedicated JavaScript heap \(or **VM heap**\).</span></span>  <span data-ttu-id="44c0b-191">Ces objets sont gérés par le récupérateur de mémoire dans la fonction V8 et ne sont donc pas actifs tant qu’il y a au moins une référence forte.</span><span class="sxs-lookup"><span data-stu-id="44c0b-191">These objects are managed by the garbage collector in V8 and therefore, stay alive as long as there is at least one strong reference to them.</span></span>  

<span data-ttu-id="44c0b-192">Tout élément absent du tas JavaScript est appelé **objet natif**.</span><span class="sxs-lookup"><span data-stu-id="44c0b-192">Anything not in the JavaScript heap is called a **native object**.</span></span>  <span data-ttu-id="44c0b-193">Les objets natifs, contrairement aux objets tas, ne sont pas gérés par le récupérateur de mémoire V8 tout au long de leur cycle de vie et ne peuvent être accessibles qu’à partir de JavaScript à l’aide de l’objet wrapper JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44c0b-193">Native objects, in contrast to heap objects, are not managed by the V8 garbage collector throughout their lifetime, and may only be accessed from JavaScript using the JavaScript wrapper object.</span></span>  

<span data-ttu-id="44c0b-194">**Cons chaîne** est un objet composé de paires de chaînes stockées, puis jointes et qui est le résultat de la concaténation.</span><span class="sxs-lookup"><span data-stu-id="44c0b-194">**Cons string** is an object that consists of pairs of strings stored and then joined, and is a result of concatenation.</span></span>  <span data-ttu-id="44c0b-195">Le contenu de la **chaîne de type cons** est uniquement nécessaire.</span><span class="sxs-lookup"><span data-stu-id="44c0b-195">The joining of the **cons string** contents occurs only as needed.</span></span> <span data-ttu-id="44c0b-196">Par exemple, quand une sous-chaîne d’une chaîne jointe doit être construite.</span><span class="sxs-lookup"><span data-stu-id="44c0b-196">An example would be when a substring of a joined string needs to be constructed.</span></span>

<span data-ttu-id="44c0b-197">Par exemple, si vous concatènent `a` et `b` , vous obtenez une chaîne `(a, b)` qui représente le résultat de la concaténation.</span><span class="sxs-lookup"><span data-stu-id="44c0b-197">For example, if you concatenate `a` and `b`, you get a string `(a, b)` which represents the result of concatenation.</span></span>  <span data-ttu-id="44c0b-198">Dans le cas d’une concaténation ultérieure `d` avec ce résultat, vous obtenez une autre **chaîne cons**: `((a, b, d)` .</span><span class="sxs-lookup"><span data-stu-id="44c0b-198">If you later concatenated `d` with that result, you get another **cons string**: `((a, b, d)`.</span></span>  

<span data-ttu-id="44c0b-199">L’argument **matrice** est un objet doté de touches numériques.</span><span class="sxs-lookup"><span data-stu-id="44c0b-199">**Array** is an object with numeric keys.</span></span> <span data-ttu-id="44c0b-200">Les **tableaux** sont utilisés de manière extensive dans l’ordinateur virtuel V8 pour le stockage de grandes quantités de données.</span><span class="sxs-lookup"><span data-stu-id="44c0b-200">**Arrays** are used extensively in the V8 VM for storing large amounts of data.</span></span> <span data-ttu-id="44c0b-201">Les ensembles de paires clé-valeur, comme les dictionnaires, sont sauvegardés par des **matrices**.</span><span class="sxs-lookup"><span data-stu-id="44c0b-201">Sets of key-value pairs, like dictionaries, are backed up by **arrays**.</span></span>  

<span data-ttu-id="44c0b-202">Un objet JavaScript classique est stocké sous la forme d’un seul type de deux types de **tableau** :</span><span class="sxs-lookup"><span data-stu-id="44c0b-202">A typical JavaScript object is stored as only one of two **array** types:</span></span>  

*   <span data-ttu-id="44c0b-203">propriétés nommées et</span><span class="sxs-lookup"><span data-stu-id="44c0b-203">named properties, and</span></span>  
*   <span data-ttu-id="44c0b-204">éléments numériques</span><span class="sxs-lookup"><span data-stu-id="44c0b-204">numeric elements</span></span>  

<span data-ttu-id="44c0b-205">Dans le cas d’un petit nombre de propriétés, les propriétés sont stockées en interne dans l’objet JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44c0b-205">When there are a small number of properties, the properties are stored internally in the JavaScript object.</span></span>  

<span data-ttu-id="44c0b-206">**Map** est un objet qui décrit à la fois le type d’objet et la disposition.</span><span class="sxs-lookup"><span data-stu-id="44c0b-206">**Map** is an object that describes both the kind of object it is and the layout.</span></span> <span data-ttu-id="44c0b-207">Par exemple, les cartes permettent de décrire des hiérarchies d’objets implicites pour un [accès rapide aux propriétés][V8FastProperties].</span><span class="sxs-lookup"><span data-stu-id="44c0b-207">For example, maps are used to describe implicit object hierarchies for [fast property access][V8FastProperties].</span></span>  

### <span data-ttu-id="44c0b-208">Groupes d’objets</span><span class="sxs-lookup"><span data-stu-id="44c0b-208">Object groups</span></span>  

<span data-ttu-id="44c0b-209">Chaque groupe d' **objets natifs** est constitué d’objets qui contiennent des références réciproques.</span><span class="sxs-lookup"><span data-stu-id="44c0b-209">Each **native objects** group is made up of objects that hold mutual references to each other.</span></span>  <span data-ttu-id="44c0b-210">Prenez en considération, par exemple, une sous-arborescence DOM dans laquelle chaque nœud comporte un lien vers le parent relatif, ainsi que des liens vers l’enfant suivant et le frère suivant, formant ainsi un graphique connecté.</span><span class="sxs-lookup"><span data-stu-id="44c0b-210">Consider, for example, a DOM subtree where every node has a link to the relative parent and links to the next child and next sibling, therefore forming a connected graph.</span></span>  

> [!NOTE]
> <span data-ttu-id="44c0b-211">Les objets natifs ne sont pas représentés dans le tas JavaScript.</span><span class="sxs-lookup"><span data-stu-id="44c0b-211">Native objects are not represented in the JavaScript heap.</span></span>  <span data-ttu-id="44c0b-212">L’absence de représentation est la raison pour laquelle les objets natifs ont une taille égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="44c0b-212">The lack of representation is why native objects have zero size.</span></span> <span data-ttu-id="44c0b-213">Au lieu de cela, les objets wrapper sont créés.</span><span class="sxs-lookup"><span data-stu-id="44c0b-213">Instead, wrapper objects are created.</span></span>  

<span data-ttu-id="44c0b-214">Chaque objet wrapper dispose d’une référence à l’objet natif correspondant pour rediriger les commandes vers ce dernier.</span><span class="sxs-lookup"><span data-stu-id="44c0b-214">Each wrapper object holds a reference to the corresponding native object, for redirecting commands to it.</span></span>  <span data-ttu-id="44c0b-215">En retour, un groupe d’objets contient des objets wrapper.</span><span class="sxs-lookup"><span data-stu-id="44c0b-215">In turn, an object group holds wrapper objects.</span></span>  <span data-ttu-id="44c0b-216">Toutefois, cela ne crée pas de cycle introuvable, car le nettoyage de la mémoire (GC \) est suffisamment intelligent pour libérer les groupes d’objets dont les wrappers ne sont plus référencés.</span><span class="sxs-lookup"><span data-stu-id="44c0b-216">However, this does not create an uncollectable cycle, as Garbage Collector \(GC\) is smart enough to release object groups whose wrappers are no longer referenced.</span></span> <span data-ttu-id="44c0b-217">Néanmoins, si vous oubliez de libérer un wrapper unique, il contient le groupe entier et les wrappers associés.</span><span class="sxs-lookup"><span data-stu-id="44c0b-217">But forgetting to release a single wrapper holds the whole group and associated wrappers.</span></span>  

## <span data-ttu-id="44c0b-218">Contacter l’équipe Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="44c0b-218">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Comment enregistrer des instantanés de tas | Documents Microsoft"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriétés rapides dans V8 | V8"  

> [!NOTE]
> <span data-ttu-id="44c0b-221">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44c0b-221">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="44c0b-222">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="44c0b-222">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="44c0b-224">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="44c0b-224">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
