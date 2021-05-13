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
# <a name="how-to-use-allocation-instrumentation-on-timeline"></a>Utilisation de l’instrumentation d’allocation sur la chronologie  

Utilisez **l’instrumentation d’allocation** sur la chronologie pour rechercher des objets qui ne sont pas correctement collectés à la mémoire et continuer à conserver la mémoire.  

## <a name="how-allocation-instrumentation-on-timeline-works"></a>Fonctionnement de l’instrumentation d’allocation sur la chronologie  

**L’instrumentation d’allocation** sur la chronologie combine les informations de capture instantanée détaillées du **profileur** de tas avec la mise à jour incrémentielle et le suivi du panneau **Performance.**  De même, le suivi de l’allocation de tas pour les objets implique de démarrer un enregistrement, d’effectuer une séquence d’actions et d’arrêter l’enregistrement pour analyse.  

<!--todo: add profile memory problems (heap profiler) section when available  -->  
<!--todo: add profile evaluate performance (Performance panel) section when available  -->  

**L’instrumentation d’allocation** sur la chronologie prend régulièrement des instantanés de tas dans l’enregistrement \(aussi souvent que toutes les 50 ms\) et une capture instantanée finale à la fin de l’enregistrement.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png" alt-text="Instrumentation d’allocation sur la chronologie" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted.msft.png":::
   **Instrumentation d’allocation sur la chronologie**  
:::image-end:::  

> [!NOTE]
> Nombre après l’ID d’objet qui persiste dans les `@` multiples captures instantanées prises pendant la session d’enregistrement.  L’ID d’objet persistant permet une comparaison précise entre les états de tas.  Les objets sont déplacés pendant les collectes de la garbage, de sorte que l’affichage de l’adresse d’un objet n’a aucun sens.  

## <a name="enable-allocation-instrumentation-on-timeline"></a>Activer l’instrumentation d’allocation sur la chronologie  

Effectuer les actions suivantes pour commencer à utiliser **l’instrumentation d’allocation sur la chronologie**.  

1.  [Ouvrez DevTools][DevtoolsOpenIndex].  
1.  Ouvrez le **panneau** Mémoire, sélectionnez l’instrumentation **d’allocation sur la bouton d’radio** de chronologie.  
1.  Démarrer l’enregistrement.  
    
    :::image type="complex" source="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png" alt-text="Enregistrer le profileur d’allocations de tas" lightbox="../media/memory-problems-memory-allocation-instrumentation-on-timeline-selected.msft.png":::
       Enregistrer le profileur d’allocations de tas  
    :::image-end:::  
    
## <a name="read-a-heap-allocation-timeline"></a>Lire une chronologie d’allocation de tas  

La chronologie d’allocation de tas indique où les objets sont créés et identifie le chemin de rétention.  Dans la figure suivante, les barres en haut indiquent quand de nouveaux objets sont trouvés dans le tas.  

La hauteur de chaque barre correspond à la taille des objets récemment alloués et la couleur des barres indique si ces objets sont toujours ou non en direct dans la capture instantanée finale du tas.  Les barres bleues indiquent les objets qui sont toujours en vie à la fin de la chronologie, les barres grises indiquent les objets qui ont été alloués au cours de la chronologie, mais qui ont depuis été collectés à la garbage.  

:::image type="complex" source="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png" alt-text="Instrumentation d’allocation sur la capture instantanée de chronologie" lightbox="../media/memory-problems-memory-allocation-timelines-snapshot.msft.png":::
   **Instrumentation d’allocation sur la capture instantanée de** chronologie  
:::image-end:::  

<!--In the following figure, an action was performed 3 times.  The sample program caches five objects, so the last five blue bars are expected.  But the left-most blue bar indicates a potential problem.  -->  
<!--todo: redo figure 4 with multiple choose actions  -->  

Vous pouvez utiliser les curseurs de la chronologie ci-dessus pour effectuer un zoom sur cette capture instantanée particulière et passer en revue les objets qui ont été récemment alloués à ce stade :  

:::image type="complex" source="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png" alt-text="Zoom sur une capture instantanée" lightbox="../media/memory-problems-memory-allocation-timeline-snapshot-highlighted-annotated.msft.png":::
   Zoom sur une capture instantanée  
:::image-end:::  

Le choix d’un objet spécifique dans le tas montre l’arborescence de rétention dans la partie inférieure de la capture instantanée du tas.  L’examen du chemin de rétention de l’objet doit vous fournir suffisamment d’informations pour comprendre pourquoi l’objet n’a pas été collecté et vous devez apporter les modifications de code nécessaires pour supprimer la référence inutile.  

## <a name="view-memory-allocation-by-function"></a>Afficher l’allocation de mémoire par fonction  

Vous pouvez afficher l’allocation de mémoire par fonction JavaScript.  Pour plus d’informations, accédez à [Examiner l’allocation de mémoire par fonction.][DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpenIndex]: ../open/index.md "Ouvrez Microsoft Edge (Chromium) DevTools | Documents Microsoft"
[DevtoolsMemoryProblemsIndexInvestigateMemoryAllocationFunction]: ./index.md#investigate-memory-allocation-by-function "Examiner l’allocation de mémoire par fonction - Résoudre les problèmes de mémoire | Documents Microsoft"  

<!--[HeapProfiler]: ./heap-snapshots.md "How to Record Heap Snapshots"  -->  
<!--[PerformancePanel]: ../profile/evaluate-performance/timeline-tool ""  -->  

[MicrosoftEdgeChannel]: https://www.microsoftedgeinsider.com/download "Télécharger un canal Microsoft Edge de données"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/allocation-profiler) et est co-auteure par [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
