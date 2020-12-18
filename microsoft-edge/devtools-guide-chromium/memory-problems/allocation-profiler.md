---
description: Utilisez l’instrumentation d’allocation sur la barre de planning pour rechercher les objets qui ne sont pas correctement nettoyés de la mémoire et conservez la mémoire.
title: Utilisation de l’instrumentation d’allocation sur une barre de planning
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/11/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 946c2d8b45f316b491a604c16c37bb2467983222
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11230914"
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

# Utilisation de l’instrumentation d’allocation sur une barre de planning  

Utilisez l' **instrumentation d’allocation sur la barre de Planning** pour rechercher les objets qui ne sont pas correctement nettoyés de la mémoire et conservez la mémoire.  

## Fonctionnement de l’instrumentation d’allocation sur la chronologie  

L' **instrumentation d’allocation sur la chronologie** combine les informations d’instantané détaillées du **profileur de segment de mémoire** avec la mise à jour incrémentielle et le suivi du panneau **performance** .  De même, le suivi de l’attribution des tas pour les objets implique le démarrage d’un enregistrement, l’exécution d’une séquence d’actions et l’arrêt de l’enregistrement à des fins d’analyse.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

L' **instrumentation d’allocation sur la chronologie** utilise périodiquement des instantanés de tas tout au long de l’enregistrement \ (aussi souvent que chaque 50 ms \) et un instantané final à la fin de l’enregistrement.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentation d’allocation sur une barre de planning" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Instrumentation d’allocation sur une barre de planning**  
:::image-end:::  

> [!NOTE]
> Le nombre `@` qui se trouve après est un ID d’objet qui persiste sur les différentes captures d’image effectuées lors de la session d’enregistrement.  L’ID d’objet persistant autorise une comparaison précise entre les États des tas.  Les objets étant déplacés lors du nettoyage de la mémoire, l’affichage de l’adresse d’un objet n’est pas judicieux.  

## Activer l’instrumentation d’allocation sur la chronologie  

Pour commencer à utiliser l' **instrumentation d’allocation sur la chronologie**, procédez comme suit.  

1.  [Ouvrez le devtools][DevtoolsOpenIndex].  
1.  Ouvrez le panneau **mémoire** , sélectionnez la case **d’option attribution de l’instrumentation sur la chronologie** .  
1.  Démarrer l’enregistrement.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Enregistrer le profil d’allocation du tas" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Enregistrer le profil d’allocation du tas  
    :::image-end:::  
    
## Lire une chronologie d’allocation de tas  

La chronologie de l’allocation du tas montre l’emplacement de création des objets et identifie le chemin de conservation.  Dans l’illustration suivante, les barres du haut indiquent le nombre de nouveaux objets dans le tas.  

La hauteur de chaque barre correspond à la taille des objets récemment alloués, et la couleur des barres indique si ces objets sont toujours présents dans l’instantané final du tas.  Les barres bleues indiquent les objets qui sont toujours en temps réel à la fin de la chronologie, car ils indiquent des objets qui ont été alloués lors de la chronologie, mais qui ont été collectés par le garbage collector.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentation d’allocation sur un instantané de chronologie" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Instrumentation d’allocation sur un instantané de chronologie**  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple click actions  -->  

Vous pouvez utiliser les curseurs de la chronologie ci-dessus pour effectuer un zoom sur cet instantané particulier et passer en revue les objets qui ont été récemment attribués à ce point:  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Effectuer un zoom avant sur un instantané" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Effectuer un zoom avant sur un instantané  
:::image-end:::  

Cliquez sur un objet spécifique du tas pour afficher l’arborescence de conservation située dans la partie inférieure de l’instantané de tas.  Si vous examinez le chemin de conservation de l’objet, vous devez disposer d’informations suffisantes pour comprendre la raison pour laquelle l’objet n’a pas été collecté et vous devez apporter les modifications de code nécessaires pour supprimer la référence inutile.  

## Afficher l’allocation de mémoire par fonction  

Vous pouvez afficher l’allocation de mémoire par fonction JavaScript.  Pour plus d’informations, accédez à la section [vérifier l’allocation de mémoire par fonction][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction].  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Ouvrir Microsoft Edge (chrome) DevTools | Documents Microsoft"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Analyser l’allocation de mémoire par fonction-résoudre les problèmes de mémoire Documents Microsoft"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Télécharger un canal Microsoft Edge"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
