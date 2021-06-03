---
description: Utilisez l’instrumentation d’allocation sur la chronologie pour rechercher des objets qui ne sont pas correctement collectés à la mémoire et continuer à conserver la mémoire.
title: Utilisation de l’instrumentation d’allocation sur la chronologie
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: a02249840256b1e5a2469a253d765eb888527662
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564083"
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
# <a name="how-to-use-allocation-instrumentation-on-timeline"></a><span data-ttu-id="2bfe3-104">Utilisation de l’instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="2bfe3-104">How to use Allocation instrumentation on Timeline</span></span>  

<span data-ttu-id="2bfe3-105">Utilisez **l’instrumentation d’allocation** sur la chronologie pour rechercher des objets qui ne sont pas correctement collectés à la mémoire et continuer à conserver la mémoire.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-105">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <a name="how-allocation-instrumentation-on-timeline-works"></a><span data-ttu-id="2bfe3-106">Fonctionnement de l’instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="2bfe3-106">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="2bfe3-107">**L’instrumentation d’allocation** sur la chronologie combine les informations de capture instantanée détaillées du **profileur** de tas avec la mise à jour incrémentielle et le suivi du panneau **Performance.**</span><span class="sxs-lookup"><span data-stu-id="2bfe3-107">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="2bfe3-108">De même, le suivi de l’allocation de tas pour les objets implique de démarrer un enregistrement, d’effectuer une séquence d’actions et d’arrêter l’enregistrement pour analyse.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-108">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="2bfe3-109">**L’instrumentation d’allocation** sur la chronologie prend régulièrement des instantanés de tas dans l’enregistrement \(aussi souvent que toutes les 50 ms\) et une capture instantanée finale à la fin de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-109">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms\) and one final snapshot at the end of the recording.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentation d’allocation sur la chronologie" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **<span data-ttu-id="2bfe3-111">Instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="2bfe3-111">Allocation instrumentation on timeline</span></span>**  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="2bfe3-112">Nombre après l’ID d’objet qui persiste dans les `@` multiples captures instantanées prises pendant la session d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="2bfe3-113">L’ID d’objet persistant permet une comparaison précise entre les états de tas.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="2bfe3-114">Les objets sont déplacés pendant les collectes de la garbage, de sorte que l’affichage de l’adresse d’un objet n’a aucun sens.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <a name="enable-allocation-instrumentation-on-timeline"></a><span data-ttu-id="2bfe3-115">Activer l’instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="2bfe3-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="2bfe3-116">Effectuer les actions suivantes pour commencer à utiliser **l’instrumentation d’allocation sur la chronologie**.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-116">Complete the following actions to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="2bfe3-117">[Ouvrez DevTools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="2bfe3-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="2bfe3-118">Ouvrez le **panneau Mémoire,** sélectionnez l’instrumentation **d’allocation sur la bouton d’radio** de chronologie.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="2bfe3-119">Démarrer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-119">Start recording.</span></span>  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Profileur d’allocations de tas d’enregistrement" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       <span data-ttu-id="2bfe3-121">Profileur d’allocations de tas d’enregistrement</span><span class="sxs-lookup"><span data-stu-id="2bfe3-121">Record heap allocations profiler</span></span>  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a><span data-ttu-id="2bfe3-122">Lire une chronologie d’allocation de tas</span><span class="sxs-lookup"><span data-stu-id="2bfe3-122">Read a heap allocation timeline</span></span>  

<span data-ttu-id="2bfe3-123">La chronologie d’allocation de tas indique où les objets sont créés et identifie le chemin de rétention.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-123">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="2bfe3-124">Dans la figure suivante, les barres en haut indiquent quand de nouveaux objets sont trouvés dans le tas.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-124">In the following figure, the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="2bfe3-125">La hauteur de chaque barre correspond à la taille des objets récemment alloués et la couleur des barres indique si ces objets sont toujours ou non en direct dans la capture instantanée finale du tas.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-125">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="2bfe3-126">Les barres bleues indiquent les objets qui sont toujours en vie à la fin de la chronologie, les barres grises indiquent les objets qui ont été alloués au cours de la chronologie, mais qui ont depuis été collectés à la garbage.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-126">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentation d’allocation sur la capture instantanée de chronologie" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   <span data-ttu-id="2bfe3-128">**Instrumentation d’allocation sur la capture instantanée de** chronologie</span><span class="sxs-lookup"><span data-stu-id="2bfe3-128">**Allocation instrumentation on timeline** snapshot</span></span>  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

<span data-ttu-id="2bfe3-129">Vous pouvez utiliser les curseurs de la chronologie ci-dessus pour effectuer un zoom sur cette capture instantanée particulière et passer en revue les objets qui ont été récemment alloués à ce stade :</span><span class="sxs-lookup"><span data-stu-id="2bfe3-129">You are able to use the sliders in the timeline above to zoom into that particular snapshot and review the objects that were recently allocated at that point:</span></span>  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Zoom sur une capture instantanée" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   <span data-ttu-id="2bfe3-131">Zoom sur une capture instantanée</span><span class="sxs-lookup"><span data-stu-id="2bfe3-131">Zoom into snapshot</span></span>  
:::image-end:::  

<span data-ttu-id="2bfe3-132">Le choix d’un objet spécifique dans le tas montre l’arborescence de rétention dans la partie inférieure de la capture instantanée du tas.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-132">Choosing on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="2bfe3-133">L’examen du chemin de rétention de l’objet doit vous fournir suffisamment d’informations pour comprendre pourquoi l’objet n’a pas été collecté et vous devez apporter les modifications de code nécessaires pour supprimer la référence inutile.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-133">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <a name="view-memory-allocation-by-function"></a><span data-ttu-id="2bfe3-134">Afficher l’allocation de mémoire par fonction</span><span class="sxs-lookup"><span data-stu-id="2bfe3-134">View memory allocation by function</span></span>  

<span data-ttu-id="2bfe3-135">Vous pouvez afficher l’allocation de mémoire par fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2bfe3-135">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="2bfe3-136">Pour plus d’informations, accédez à [Examiner l’allocation de mémoire par fonction.][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]</span><span class="sxs-lookup"><span data-stu-id="2bfe3-136">For more information, navigate to [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].</span></span>  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a><span data-ttu-id="2bfe3-137">Contacter l’équipe DevTools MicrosoftEdge</span><span class="sxs-lookup"><span data-stu-id="2bfe3-137">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Ouvrez Microsoft Edge (Chromium) DevTools | Documents Microsoft"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Examiner l’allocation de mémoire par fonction : résoudre les problèmes de mémoire | Documents Microsoft"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Télécharger un canal Microsoft Edge de données"  

> [!NOTE]
> <span data-ttu-id="2bfe3-141">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2bfe3-141">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2bfe3-142">La page d’origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) et est co-auteure par [Meggin Kearney][MegginKearney] \(Technical Writer\).</span><span class="sxs-lookup"><span data-stu-id="2bfe3-142">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="2bfe3-144">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2bfe3-144">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
