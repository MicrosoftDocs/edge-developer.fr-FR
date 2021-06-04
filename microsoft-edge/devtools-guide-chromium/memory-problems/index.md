---
description: Découvrez comment utiliser Microsoft Edge et DevTools pour rechercher les problèmes de mémoire qui affectent les performances des pages, notamment les fuites de mémoire, les problèmes de mémoire et les collectes fréquentes de la mémoire.
title: Résoudre les problèmes de mémoire
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 3b2405d23dd6ee349484c9ba66d195e3ed12144b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565028"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->
# <a name="fix-memory-problems"></a>Résoudre les problèmes de mémoire  

Découvrez comment utiliser Microsoft Edge et DevTools pour rechercher les problèmes de mémoire qui affectent les performances des pages, notamment les fuites de mémoire, les problèmes de mémoire et les collectes fréquentes de la mémoire.  

### <a name="summary"></a>Résumé  

*   Découvrez la quantité de mémoire que votre page utilise actuellement avec le Gestionnaire des tâches Microsoft Edge navigateur.  
*   Visualisez l’utilisation de la mémoire au fil du temps avec **le panneau** Mémoire.  
*   Identifiez les arbre DOM détachés \(une cause courante de fuites de mémoire\) avec une capture instantanée **du tas.**  
*   Découvrez quand une nouvelle mémoire est allouée dans votre tas JavaScript \(tas JS\) avec **l’instrumentation d’allocation sur la chronologie**.  

## <a name="overview"></a>Vue d'ensemble  

Dans le modèle de performances **RAIL,** l’objectif de vos efforts en matière de performances doit être vos utilisateurs.  

<!--todo: add RAIL section when available  -->  

Les problèmes de mémoire sont importants, car ils sont souvent perceptibles par les utilisateurs.  Les utilisateurs peuvent percevoir les problèmes de mémoire des manières suivantes :  

*   **Les performances d’une page se dégradent progressivement au fil du temps.**  Il s’agit éventuellement d’un symptôme d’une fuite de mémoire.  Une fuite de mémoire se fait lorsqu’un bogue dans la page fait que la page utilise progressivement de plus en plus de mémoire au fil du temps.  
*   **Les performances d’une page sont constamment mauvaises.**  Il s’agit peut-être d’un symptôme d’un problème de mémoire.  La mémoire est en trop lorsqu’une page utilise plus de mémoire que nécessaire pour une vitesse de page optimale.  
*   **Les performances d’une page sont retardées ou semblent régulièrement suspendues.**  Il s’agit éventuellement d’un symptôme de fréquents collectes de la garbage.  Le garbage collection est le moment où le navigateur récupère de la mémoire.  Le navigateur décide quand cela se produit.  Pendant les collections, tous les scripts en cours d’exécution sont suspendus.  Ainsi, si le navigateur collecte beaucoup de données de la garbage, le runtime de script sera beaucoup suspendu.  

### <a name="memory-bloat-how-much-is-too-much"></a>La mémoire est trop grande : quelle est la quantité « trop » ?  

Une fuite de mémoire est facile à définir.  Si un site utilise progressivement de plus en plus de mémoire, vous avez une fuite.  Mais la mémoire est un peu plus difficile à épingler.  Qu’est-ce que l’on qualifie d'« utilisation de trop de mémoire » ?  

Il n’existe pas de chiffres en dur ici, car différents appareils et navigateurs ont des fonctionnalités différentes.  La même page qui s’exécute correctement sur un smartphone haut de gamme peut se crasher sur un smartphone bas de gamme.  

L’essentiel ici est d’utiliser le modèle RAIL et de se concentrer sur vos utilisateurs.  Découvrez quels appareils sont populaires auprès de vos utilisateurs, puis testez votre page sur ces appareils.  Si l’expérience est constamment mauvaise, la page peut dépasser les capacités de mémoire de ces appareils.  

## <a name="monitor-memory-use-in-realtime-with-the-microsoft-edge-browser-task-manager"></a>Surveiller l’utilisation de la mémoire en temps réel avec Microsoft Edge du gestionnaire des tâches du navigateur  

Utilisez le Gestionnaire des Microsoft Edge navigateur comme point de départ pour l’examen de votre problème de mémoire.  Le Gestionnaire Microsoft Edge navigateur est un moniteur en temps réel qui vous indique la quantité de mémoire qu’une page utilise actuellement.  

1.  Sélectionnez `Shift` + `Esc` ou accédez au menu **** Microsoft Edge menu principal,  >  **** puis sélectionnez Plus d’outils Gestionnaire des tâches du navigateur pour ouvrir Microsoft Edge gestionnaire des tâches du navigateur.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Ouverture du Gestionnaire des Microsoft Edge navigateur" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Figure 1 : Ouverture du Gestionnaire des Microsoft Edge navigateur  
    :::image-end:::  
    
1.  Pointez sur l’en-tête de tableau du Gestionnaire des tâches du navigateur Microsoft Edge, ouvrez le menu contextuel \(clic droit\) et activez la mémoire **JavaScript.**  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Activer la mémoire JavaScript" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Figure 2 : Activer la mémoire JavaScript  
    :::image-end:::  
    
Ces deux colonnes vous indiquent différentes choses sur la façon dont votre page utilise la mémoire.  

*   La **colonne Mémoire** représente la mémoire native.  Les nodes DOM sont stockés dans la mémoire native.  Si cette valeur augmente, les nodes DOM sont créés.  
*   La **colonne Mémoire JavaScript** représente le tas JS.  Cette colonne contient deux valeurs.  La valeur qui vous intéresse est le nombre direct \(le nombre entre parenthèses\).  Le nombre en direct représente la quantité de mémoire que les objets accessibles sur votre page utilisent.  Si ce nombre augmente, soit de nouveaux objets sont créés, soit les objets existants augmentent.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <a name="visualize-memory-leaks-with-performance-panel"></a>Visualiser les fuites de mémoire avec le panneau Performances  

Vous pouvez également utiliser le panneau Performances comme autre point de départ dans votre enquête.  Le panneau Performances vous permet de visualiser l’utilisation de la mémoire d’une page au fil du temps.  

1.  Ouvrez **le panneau Performances** sur DevTools.  
1.  Activez la **case à** cocher Mémoire.  
1.  [Effectuer un enregistrement.][DevtoolsEvaluatePerformanceReferenceRecord]  

> [!TIP]
> Il est pratique de démarrer et de terminer votre enregistrement avec un garbage collection forcé.  Pour forcer le collecte de la garbage collection, **sélectionnez** le bouton de collecte de la garbage ![ force garbage collection lors de ][ImageForceGarbageCollectionIcon] l’enregistrement.  

Pour montrer les enregistrements de mémoire, prenons le code ci-dessous :  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Chaque fois que le bouton référencé dans le code est choisi, dix milliers de nodes sont appendés au corps du document et une chaîne d’un million de caractères est enfoncée sur le `div` `x` `x` tableau.  L’exécution de l’exemple de code précédent produit un enregistrement dans le panneau **Performances** comme illustré ci-après.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Croissance simple" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Figure 3 : Croissance simple  
:::image-end:::  

Tout d’abord, une explication de l’interface utilisateur.  Le **graphique HEAP** dans le volet Vue d’ensemble \(sous **NET**\) représente le tas JS. ****  Sous le volet Vue **d’ensemble** se trouve **le** volet Compteur.  L’utilisation de la mémoire est décomposée par **** le tas JS \(identique au graphique **HEAP** dans le volet Vue d’ensemble\), les documents, les nodes DOM, les écouteurs et la mémoire GPU.  Désactiver une case à cocher pour la masquer dans le graphique.  

À présent, une analyse du code est comparée à la figure précédente.  Si vous examinez le compteur de nœuds \(le graphique vert\), il correspond correctement au code.  Le nombre de nœuds augmente en étapes discrètes.  Vous pouvez supposer que chaque augmentation du nombre de nœuds est un appel à `grow()` .  Le graphique de tas JS \(le graphique bleu\) n’est pas aussi simple.  En respectant les meilleures pratiques, le premier dip est **** en fait un garbage collection forcé \(choisissez le bouton de collecte du garbage ![ force garbage ][ImageForceGarbageCollectionIcon] collection\).  Au fur et à mesure de la progression de l’enregistrement, les pics de taille du tas JS s’affichent.  Ceci est naturel et attendu : le code JavaScript crée les nodes DOM sur chaque bouton de votre choix et fait beaucoup de travail lorsqu’il crée la chaîne d’un million de caractères.  L’élément clé ici est le fait que le tas JS se termine plus haut qu’il n’a commencé \(le « début » ici étant le point après le garbage collection forcé\).  Dans le monde réel, si vous avez vu ce modèle d’augmentation de la taille du tas JS ou de la taille du nœud, il peut éventuellement définir une fuite de mémoire.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <a name="discover-detached-dom-tree-memory-leaks-with-heap-snapshots"></a>Découvrir les fuites de mémoire d’arborescence DOM détachée avec des instantanés de tas  

Un nœud DOM est uniquement la garbage collecté lorsqu’il n’y a aucune référence au nœud à partir de l’arborescence DOM ou du code JavaScript en cours d’exécution sur la page.  Un nœud est dit « détaché » lorsqu’il est supprimé de l’arborescence DOM, mais certains javaScript le référencent toujours.  Les nodes DOM détachées sont une cause courante de fuites de mémoire.  Cette section vous apprend à utiliser les profileurs de tas dans DevTools pour identifier les nodes détachées.  

Voici un exemple simple de nodes DOM détachées.  

```javascript
var detachedTree;

function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedTree = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

Le choix du bouton référencé dans le code crée `ul` un nœud avec dix `li` enfants.  Les nodes sont référencés par le code, mais n’existent pas dans l’arborescence DOM, de sorte que chacun d’eux est détaché.  

Les captures instantanées de tas sont un moyen d’identifier les nodes détachées.  Comme son nom l’indique, les captures instantanées de tas vous montrent comment la mémoire est distribuée entre les objets JS et les nodes DOM de votre page au moment de la capture instantanée.  

Pour créer une capture instantanée, ouvrez DevTools et accédez au panneau Mémoire, choisissez la bouton **d’radio** Instantané de tas > bouton Prendre **une** capture instantanée. ****  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Prendre une capture instantanée de tas" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Figure 4 : Prendre une capture instantanée de tas  
:::image-end:::  

Le traitement et le chargement de la capture instantanée peuvent prendre un certain temps.  Une fois terminé, sélectionnez-le dans le panneau de gauche \(nommé **SNAPSHOTS TAS**\).  

Tapez `Detached` dans la zone de texte **Filtre** classe pour rechercher les arbre DOM détachés.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Filtrage des nodes détachées" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Figure 5 : Filtrage des nodes détachées  
:::image-end:::  

Développez les carats pour examiner une arborescence détachée.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Étude de l’arborescence détachée" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Figure 6 : Étude de l’arborescence détachée  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Choisissez un nœud pour l’examiner plus en détail.  Dans le **volet Objets,** vous pouvez consulter plus d’informations sur le code qui le référence.  Par exemple, dans la figure suivante, la `detachedNodes` variable fait référence au nœud.  Pour corriger la fuite de mémoire particulière, vous devez étudier le code qui utilise la variable et vous assurer que la référence au nœud est supprimée lorsqu’elle `detachedUNode` n’est plus nécessaire.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Étude d’un nœud" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Figure 7 : Investigation d’un nœud  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <a name="identify-js-heap-memory-leaks-with-allocation-instrumentation-on-timeline"></a>Identifier les fuites de mémoire de tas JS avec l’instrumentation d’allocation sur la chronologie  

**L’instrumentation d’allocation sur la** chronologie est un autre outil qui peut vous aider à suivre les fuites de mémoire dans votre tas JS.  

Démontrez **l’instrumentation de l’allocation sur la chronologie**  à l’aide du code suivant.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Chaque fois que le bouton référencé dans le code est enfoncé, une chaîne d’un million de caractères est ajoutée au `x` tableau.  

Pour enregistrer une instrumentation d’allocation sur la chronologie, **** ouvrez DevTools, accédez **** au panneau Mémoire, choisissez l’instrumentation **** **d’allocation** sur la bouton d’radio de chronologie, choisissez le bouton Démarrer, effectuez l’action que vous pensez être à l’origine de la fuite de mémoire, puis choisissez le bouton Arrêter l’enregistrement du profil de tas lorsque vous avez ![ ][ImageStopRecordingIcon] terminé.  

Lors de l’enregistrement, notez si des barres bleues s’afficheront sur l’instrumentation d’allocation sur la chronologie, comme dans la figure suivante.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Nouvelles allocations" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Figure 8 : Nouvelles allocations  
:::image-end:::  

Ces barres bleues représentent de nouvelles allocations de mémoire.  Ces nouvelles allocations de mémoire sont vos candidats aux fuites de mémoire.  Vous pouvez effectuer un zoom sur **** une barre pour filtrer le volet Constructeur afin d’afficher uniquement les objets qui ont été alloués pendant la période spécifiée.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Chronologie d’allocation avec zoom avant" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Figure 9 : Chronologie d’allocation avec zoom avant  
:::image-end:::  

Développez l’objet et sélectionnez la valeur pour afficher plus de détails dans le **volet** Objet.  Par exemple, dans la figure suivante, les détails de l’objet nouvellement alloué indiquent qu’il a été alloué à la `x` variable dans `Window` l’étendue.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Détails de l’objet" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Figure 10 : Détails de l’objet  
:::image-end:::  

## <a name="investigate-memory-allocation-by-function"></a>Examiner l’allocation de mémoire par fonction  

Utilisez le type de profilage **d’échantillonnage** d’allocation pour afficher l’allocation de mémoire par fonction JavaScript.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Échantillonnage de l’allocation d’enregistrement" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Figure 11 : Échantillonnage de l’allocation d’enregistrement  
:::image-end:::  

1.  Choisissez la **radio d’échantillonnage** d’allocation.  S’il existe un travail sur la page, vous pouvez le sélectionner comme cible de profilage à l’aide du menu déroulant en face du **bouton** Démarrer.  
1.  Sélectionnez **le bouton** Démarrer.  
1.  Effectuer les actions sur la page web que vous souhaitez examiner.  
1.  Choisissez le **bouton Arrêter** lorsque vous avez terminé toutes vos actions.  

DevTools vous présente une répartition de l’allocation de mémoire par fonction.  L’affichage par défaut **est Épais (bas vers**le haut), qui affiche les fonctions qui ont alloué le plus de mémoire en haut.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Échantillonnage d’allocation" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Figure 12 : Échantillonnage des allocations  
:::image-end:::  

## <a name="spot-frequent-garbage-collections"></a>Repérer les garbage collections fréquentes  

Si votre page s’interrompt fréquemment, vous risquez d’avoir des problèmes de collecte de la garbage collection.  

Vous pouvez utiliser le Gestionnaire des tâches Microsoft Edge navigateur ou les enregistrements de mémoire des performances pour repérer les tâches fréquentes de collecte de la mémoire.  Dans le Gestionnaire des Microsoft Edge navigateur, les **** valeurs Mémoire ou Mémoire **JavaScript** qui tombent ou tombent fréquemment représentent un collecte fréquent de la mémoire.  Dans les enregistrements de performances, les modifications fréquentes \(déplacement et baisse\) du tas JS ou du nombre de nœuds indiquent un collecte fréquent de la mémoire.  

Une fois que vous avez identifié le problème, vous pouvez utiliser une **instrumentation d’allocation** sur l’enregistrement chronologique pour savoir où la mémoire est allouée et quelles fonctions sont à l’origine des allocations.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Performances d’enregistrement : référence de l’analyse des performances"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
