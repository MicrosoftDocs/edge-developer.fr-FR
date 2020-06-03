---
title: Utilisation de l’instrumentation d’allocation sur une barre de planning
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: ab7a270e1d599e254aaaf4515b6898cb1d9782fc
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611733"
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





# <span data-ttu-id="39382-103">Utilisation de l’instrumentation d’allocation sur une barre de planning</span><span class="sxs-lookup"><span data-stu-id="39382-103">How to Use Allocation Instrumentation on Timeline</span></span>  



<span data-ttu-id="39382-104">Utilisez l' **instrumentation d’allocation sur la barre de Planning** pour rechercher les objets qui ne sont pas correctement nettoyés de la mémoire et conservez la mémoire.</span><span class="sxs-lookup"><span data-stu-id="39382-104">Use **Allocation instrumentation on timeline** to find objects that are not being properly garbage collected, and continue to retain memory.</span></span>  

## <span data-ttu-id="39382-105">Fonctionnement de l’instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="39382-105">How Allocation instrumentation on timeline works</span></span>  

<span data-ttu-id="39382-106">L' **instrumentation d’allocation sur la chronologie** combine les informations d’instantané détaillées du **profileur de segment de mémoire** avec la mise à jour incrémentielle et le suivi du panneau **performance** .</span><span class="sxs-lookup"><span data-stu-id="39382-106">**Allocation instrumentation on timeline** combines the detailed snapshot information of the **heap profiler** with the incremental updating and tracking of the **Performance** panel.</span></span>  <span data-ttu-id="39382-107">De même, le suivi de l’attribution des tas pour les objets implique le démarrage d’un enregistrement, l’exécution d’une séquence d’actions et l’arrêt de l’enregistrement à des fins d’analyse.</span><span class="sxs-lookup"><span data-stu-id="39382-107">Similarly, tracking heap allocation for objects involves starting a recording, performing a sequence of actions, and stopping the recording for analysis.</span></span>  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

<span data-ttu-id="39382-108">L' **instrumentation d’allocation sur la chronologie** utilise périodiquement des instantanés de tas tout au long de l’enregistrement \ (aussi souvent chaque 50 ms! \) et un instantané final à la fin de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="39382-108">**Allocation instrumentation on timeline** takes heap snapshots periodically throughout the recording \(as frequently as every 50 ms!\) and one final snapshot at the end of the recording.</span></span>  

> ##### <span data-ttu-id="39382-109">Figure1</span><span class="sxs-lookup"><span data-stu-id="39382-109">Figure 1</span></span>  
> **<span data-ttu-id="39382-110">Instrumentation d’allocation sur une barre de planning</span><span class="sxs-lookup"><span data-stu-id="39382-110">Allocation instrumentation on timeline</span></span>**  
> ![Instrumentation d’allocation sur une barre de planning][ImageObjectTracker]  

> [!NOTE]
> <span data-ttu-id="39382-112">Le nombre `@` qui se trouve après est un ID d’objet qui persiste sur les différentes captures d’image effectuées lors de la session d’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="39382-112">The number after the `@` is an object ID that persists across the multiple snapshots taken during the recording session.</span></span>  <span data-ttu-id="39382-113">L’ID d’objet persistant autorise une comparaison précise entre les États des tas.</span><span class="sxs-lookup"><span data-stu-id="39382-113">The persistent object ID enables precise comparison between heap states.</span></span>  <span data-ttu-id="39382-114">Les objets étant déplacés lors du nettoyage de la mémoire, l’affichage de l’adresse d’un objet n’est pas judicieux.</span><span class="sxs-lookup"><span data-stu-id="39382-114">Objects are moved during garbage collections, so displaying the address of an object makes no sense.</span></span>  

## <span data-ttu-id="39382-115">Activer l’instrumentation d’allocation sur la chronologie</span><span class="sxs-lookup"><span data-stu-id="39382-115">Enable Allocation Instrumentation on Timeline</span></span>  

<span data-ttu-id="39382-116">Pour commencer à utiliser l' **instrumentation d’allocation sur la chronologie**, procédez comme suit.</span><span class="sxs-lookup"><span data-stu-id="39382-116">Follow these steps to begin using **Allocation instrumentation on timeline**.</span></span>  

1.  <span data-ttu-id="39382-117">[Ouvrez le devtools][DevtoolsOpenIndex].</span><span class="sxs-lookup"><span data-stu-id="39382-117">[Open the DevTools][DevtoolsOpenIndex].</span></span>  
1.  <span data-ttu-id="39382-118">Ouvrez le panneau **mémoire** , sélectionnez la case **d’option attribution de l’instrumentation sur la chronologie** .</span><span class="sxs-lookup"><span data-stu-id="39382-118">Open the **Memory** panel, select the **Allocation instrumentation on timeline** radio button.</span></span>  
1.  <span data-ttu-id="39382-119">Démarrer l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="39382-119">Start recording.</span></span>  

> ##### <span data-ttu-id="39382-120">Figure 2</span><span class="sxs-lookup"><span data-stu-id="39382-120">Figure 2</span></span>  
> <span data-ttu-id="39382-121">Enregistrer le profil d’allocation du tas</span><span class="sxs-lookup"><span data-stu-id="39382-121">Record heap allocations profiler</span></span>  
> ![Enregistrer le profil d’allocation du tas][ImageRecordHeap]  

## <span data-ttu-id="39382-123">Lire une chronologie d’allocation de tas</span><span class="sxs-lookup"><span data-stu-id="39382-123">Read a heap allocation timeline</span></span>  

<span data-ttu-id="39382-124">La chronologie de l’allocation du tas montre l’emplacement de création des objets et identifie le chemin de conservation.</span><span class="sxs-lookup"><span data-stu-id="39382-124">The heap allocation timeline shows where objects are being created and identifies the retaining path.</span></span>  <span data-ttu-id="39382-125">Dans la [figure 3](#figure-3), les barres du haut indiquent le nombre de nouveaux objets dans le tas.</span><span class="sxs-lookup"><span data-stu-id="39382-125">In [Figure 3](#figure-3), the bars at the top indicate when new objects are found in the heap.</span></span>  

<span data-ttu-id="39382-126">La hauteur de chaque barre correspond à la taille des objets récemment alloués, et la couleur des barres indique si ces objets sont toujours présents dans l’instantané final du tas.</span><span class="sxs-lookup"><span data-stu-id="39382-126">The height of each bar corresponds to the size of the recently allocated objects, and the color of the bars indicate whether or not those objects are still live in the final heap snapshot.</span></span>  <span data-ttu-id="39382-127">Les barres bleues indiquent les objets qui sont toujours en temps réel à la fin de la chronologie, car ils indiquent des objets qui ont été alloués lors de la chronologie, mais qui ont été collectés par le garbage collector.</span><span class="sxs-lookup"><span data-stu-id="39382-127">Blue bars indicate objects that are still live at the end of the timeline, Gray bars indicate objects that were allocated during the timeline, but have since been garbage collected.</span></span>  

> ##### <span data-ttu-id="39382-128">Figure3</span><span class="sxs-lookup"><span data-stu-id="39382-128">Figure 3</span></span>  
> <span data-ttu-id="39382-129">**Instrumentation d’allocation sur un instantané de chronologie**</span><span class="sxs-lookup"><span data-stu-id="39382-129">**Allocation instrumentation on timeline** snapshot</span></span>  
> ![Instrumentation d’allocation sur un instantané de chronologie][ImageCollected]  

<!--In [Figure 4](#figure-4), an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

<span data-ttu-id="39382-131">Vous pouvez utiliser les curseurs de la chronologie ci-dessus pour effectuer un zoom avant sur cet instantané particulier et afficher les objets qui ont été récemment attribués à ce point:</span><span class="sxs-lookup"><span data-stu-id="39382-131">You are able to use the sliders in the timeline above to zoom into that particular snapshot and see the objects that were recently allocated at that point:</span></span>  

> ##### <span data-ttu-id="39382-132">Figure 4</span><span class="sxs-lookup"><span data-stu-id="39382-132">Figure 4</span></span>  
> <span data-ttu-id="39382-133">Effectuer un zoom avant sur un instantané</span><span class="sxs-lookup"><span data-stu-id="39382-133">Zoom into snapshot</span></span>  
> ![Effectuer un zoom avant sur un instantané][ImageSliders]  

<span data-ttu-id="39382-135">Cliquez sur un objet spécifique du tas pour afficher l’arborescence de conservation située dans la partie inférieure de l’instantané de tas.</span><span class="sxs-lookup"><span data-stu-id="39382-135">Clicking on a specific object in the heap shows the retaining tree in the bottom portion of the heap snapshot.</span></span>  <span data-ttu-id="39382-136">Si vous examinez le chemin de conservation de l’objet, vous devez disposer d’informations suffisantes pour comprendre la raison pour laquelle l’objet n’a pas été collecté et vous devez apporter les modifications de code nécessaires pour supprimer la référence inutile.</span><span class="sxs-lookup"><span data-stu-id="39382-136">Examining the retaining path to the object should give you enough information to understand why the object was not collected, and you should make the necessary code changes to remove the unnecessary reference.</span></span>  

## <span data-ttu-id="39382-137">Afficher l’allocation de mémoire par fonction</span><span class="sxs-lookup"><span data-stu-id="39382-137">View memory allocation by function</span></span>   

<span data-ttu-id="39382-138">Vous pouvez afficher l’allocation de mémoire par fonction JavaScript.</span><span class="sxs-lookup"><span data-stu-id="39382-138">You are able to view memory allocation by JavaScript function.</span></span>  <span data-ttu-id="39382-139">Pour plus d’informations, voir [analyser l’allocation de mémoire par fonction][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] .</span><span class="sxs-lookup"><span data-stu-id="39382-139">See [Investigate memory allocation by function][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction] for more information.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageObjectTracker]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png "Figure 1: instrumentation d’allocation sur la chronologie"  
[ImageRecordHeap]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png "Figure 2: enregistrer le profil d’allocation du tas"  
[ImageCollected]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timelines-snapshot.msft.png "Figure 3: instrumentation d’allocation sur un instantané de chronologie"  
[ImageSliders]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png "Figure 4: zoom en instantané"  

<!-- links -->  

[DevToolsOpenIndex]: /microsoft-edge/devtools-guide-chromium/open "Ouvrir Microsoft Edge (chrome) DevTools"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: /microsoft-edge/devtools-guide-chromium/memory-problems/index#investigate-memory-allocation-by-function "Examiner l’allocation de mémoire par fonction-résolution des problèmes de mémoire"  

<!--[HeapProfiler]: ../profile/memory-problems/heap-snapshots ""  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Télécharger un canal Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="39382-147">Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="39382-147">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="39382-148">La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).</span><span class="sxs-lookup"><span data-stu-id="39382-148">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) and is authored by [Meggin Kearney][MegginKearney] \(Technical Writer\).</span></span>  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
<span data-ttu-id="39382-150">Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="39382-150">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  