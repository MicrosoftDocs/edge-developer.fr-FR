---
description: Découvrez comment utiliser Microsoft Edge et DevTools pour rechercher des problèmes de mémoire qui affectent les performances de la page, notamment les fuites de mémoire, l’augmentation de la mémoire et les nettoyages de mémoire fréquents.
title: Résoudre les problèmes de mémoire
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 1d8a24fc360dc307471be33544c9c707736be06d
ms.sourcegitcommit: 99eee78698dc95b2a3fa638a5b063ef449899cda
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/20/2020
ms.locfileid: "11125453"
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

# Résoudre les problèmes de mémoire  

Découvrez comment utiliser Microsoft Edge et DevTools pour rechercher des problèmes de mémoire qui affectent les performances de la page, notamment les fuites de mémoire, l’augmentation de la mémoire et les nettoyages de mémoire fréquents.  

### Résumé  

*   Déterminez la quantité de mémoire utilisée par votre page avec le gestionnaire des tâches du navigateur Microsoft Edge.  
*   Visualisez l’utilisation de la mémoire au fil du temps avec le panneau **mémoire** .  
*   Identifiez les arborescences DOM détachées \ (une cause courante de fuites de mémoire \) avec **instantané de tas**.  
*   Déterminez quand une nouvelle mémoire est allouée dans votre segment JavaScript \ (JS Heap \) avec l' **instrumentation d’allocation sur la chronologie**.  

## Vue d'ensemble  

Dans l’esprit du modèle de performance des **rails** , le focus de vos efforts de performance doit être vos utilisateurs.  

<!--todo: add RAIL section when available  -->  

Des problèmes de mémoire sont importants, car ils sont souvent perceptibles par les utilisateurs.  Les utilisateurs peuvent percevoir des problèmes de mémoire de l’une des façons suivantes:  

*   **Les performances d’une page sont progressivement pires dans le temps**.  Il peut s’agir d’un symptôme de fuite de mémoire.  Une fuite de mémoire se produit lorsqu’un bogue dans la page entraîne l’utilisation progressive de la page avec une plus grande quantité de mémoire au fil du temps.  
*   **Les performances d’une page sont incorrectes**.  Il s’agit peut-être d’un problème de dilatation de mémoire.  L’utilisation de la mémoire est une augmentation de la quantité de mémoire requise pour une page de plus en plus rapide.  
*   **Les performances d’une page sont retardées ou semblent être suspendues fréquemment**.  C’est peut-être le symptôme de nettoyages de la mémoire.  Le nettoyage de la mémoire se trouve lorsque le navigateur récupère de la mémoire.  Le navigateur détermine à quel moment cela se produit.  Pendant les collections, tout le script en cours d’exécution est en pause.  Par conséquent, si le navigateur est en nettoyage de la mémoire, le script Runtime va être mis en pause beaucoup.  

### Augmentation de la mémoire: le volume est «trop».  

Il est facile de définir une fuite de mémoire.  Si un site utilise une plus grande quantité de mémoire, cela signifie que vous avez une fuite.  Mais l’augmentation de la quantité de mémoire est un peu plus difficile à épingler.  Quels sont les critères d’utilisation trop importante de la mémoire?  

Il n’y a pas de numéro de papier ici, car les différents appareils et navigateurs ont différentes fonctionnalités.  La même page qui s’exécute correctement sur un smartphone haut de gamme est susceptible de se bloquer sur un smartphone bas de gamme.  

Pour ce faire, vous pouvez utiliser le modèle de RAIL et sélectionner vos utilisateurs.  Découvrez quels appareils sont populaires avec vos utilisateurs et testez votre page sur ces appareils.  S’il s’agit d’un problème de bonne qualité, il est possible que la page dépasse les capacités de mémoire de ces derniers.  

## Surveiller l’utilisation de la mémoire en temps réel à l’aide du gestionnaire des tâches du navigateur Microsoft Edge  

Utilisez le gestionnaire des tâches du navigateur Microsoft Edge comme point de départ pour l’examen de votre problème de mémoire.  Le gestionnaire des tâches du navigateur Microsoft Edge est un moniteur en temps réel qui vous indique la quantité de mémoire utilisée actuellement par une page.  

1.  `Shift` + `Esc` Dans le menu principal de Microsoft Edge, sélectionnez ou accédez au gestionnaire **des**  >  **tâches du navigateur** Microsoft Edge.  
    
    :::image type="complex" source="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png":::
       Figure 1: ouverture du gestionnaire des tâches du navigateur Microsoft Edge  
    :::image-end:::  
    
1.  Placez le curseur sur l’en-tête de tableau du gestionnaire des tâches du navigateur Microsoft Edge, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et activez la **mémoire JavaScript**.  
    
    :::image type="complex" source="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png":::
       Figure 2: activer la mémoire JavaScript  
    :::image-end:::  
    
Ces deux colonnes vous informent des différents aspects de l’utilisation de la mémoire dans votre page.  

*   La colonne **Memory** représente une mémoire native.  Les nœuds DOM sont stockés dans la mémoire native.  Si cette valeur augmente, les nœuds DOM sont créés.  
*   La colonne de **mémoire JavaScript** représente le tas js.  Cette colonne contient deux valeurs.  La valeur qui vous intéresse correspond au numéro dynamique \ (le nombre entre parenthèses \).  Le numéro dynamique représente la quantité de mémoire utilisée par les objets joignable sur votre page.  Si ce nombre augmente, les nouveaux objets sont créés ou les objets existants sont en augmentation.  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## Visualiser les fuites de mémoire à l’aide du panneau de performance  

Vous pouvez également utiliser le volet performance comme un autre point de départ dans votre examen.  Le panneau performance vous permet de visualiser l’utilisation de la mémoire d’une page dans le temps.  

1.  Ouvrez le panneau de **performance** sur devtools.  
1.  Cochez la case **mémoire** .  
1.  [Créer un enregistrement][DevtoolsEvaluatePerformanceReferenceRecord]  

> [!TIP]
> Il est recommandé de démarrer et de mettre fin à l’enregistrement grâce à un nettoyage de la mémoire forcé.  Cliquez sur le bouton **collecter** le nettoyage de la mémoire pour le nettoyage de la mémoire ![ pour le ][ImageForceGarbageCollectionIcon] nettoyage de la mémoire.  

Pour illustrer les enregistrements de mémoire, considérez le code ci-dessous:  

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

Chaque fois que le bouton référencé dans le code est enfoncé, les `div` nœuds 10000 sont ajoutés au corps du document et une chaîne de 1 million `x` caractères est transplacée sur le `x` tableau.  L’exemple de code précédent génère un enregistrement dans le panneau **performance** comme le montre la figure ci-dessous.  

:::image type="complex" source="../media/memory-problems-glitch-example-1-performance-memory.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-1-performance-memory.msft.png":::
   Figure 3: croissance simple  
:::image-end:::  

Tout d’abord, explication de l’interface utilisateur.  Le graphique **tas** dans le volet **vue d’ensemble** \ (sous **net**\) représente le tas js.  Le volet de **vue d’ensemble** est le volet de **compteur** .  Ici, vous pouvez voir l’utilisation de la mémoire divisée par le tas JS \ (similaire au graphique de **tas** dans le volet **vue d’ensemble** ), aux documents, aux nœuds DOM, aux écouteurs et à la mémoire GPU.  La désactivation d’une case à cocher masque celle-ci du graphique.  

À présent, analyse du code par rapport à la figure précédente.  Si vous examinez le compteur de nœuds \ (le graphique vert), vous pouvez voir qu’il correspond au code.  Le nombre de nœuds augmente par étapes discrètes.  Vous pouvez supposer que chaque augmentation du nombre de nœuds est un appel à `grow()` .  Le graphique de tas JS \ (graphique bleu \) n’est pas aussi simple.  Conformément aux meilleures pratiques, le premier DIP est en fait un nettoyage de la mémoire forcé (atteint en appuyant sur le bouton  **collecter** le nettoyage de la mémoire ![ ][ImageForceGarbageCollectionIcon] ).  En cours d’enregistrement, vous pouvez voir que la taille du tas JS pointe.  Il s’agit d’une opération naturelle et normale: le code JavaScript crée les nœuds DOM sur chaque pression de bouton et effectue un grand nombre de travail lors de la création de la chaîne de 1 million caractères.  Dans le cas présent, il s’agit du fait que le tas JS se termine plus haut que le début du nettoyage de la mémoire.  Dans le monde réel, si vous avez remarqué ce modèle d’augmentation de la taille du tas et de la taille de nœud JS, il peut éventuellement définir une fuite de mémoire.  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## Découvrir des fuites de mémoire d’arborescence DOM détachées avec des instantanés de tas  

Un nœud DOM est uniquement nettoyé lorsqu’il n’y a aucune référence au nœud à partir de l’arborescence DOM ou du code JavaScript en cours d’exécution sur la page.  Un nœud est considéré comme «détaché» lorsque ce dernier est supprimé de l’arborescence DOM, mais que du JavaScript le référence encore.  Les nœuds DOM dissociés sont une cause courante de fuite de mémoire.  Cette section vous explique comment utiliser les profileurs de tas dans DevTools pour identifier les nœuds détachés.  

Voici un exemple simple de nœuds DOM dissociés.  

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

La sélection du bouton référencé dans le code crée un `ul` nœud avec dix `li` enfants.  Les nœuds sont référencés par le code mais n’existent pas dans l’arborescence DOM, de sorte que chacun d’eux est détaché.  

Les instantanés de tas permettent d’identifier les nœuds détachés.  Comme son nom l’indique, les instantanés de tas vous montrent la manière dont la mémoire est distribuée entre les objets JS et les nœuds DOM de votre page au moment de l’instantané.  

Pour créer une capture d’écran, ouvrez DevTools et accédez au panneau **mémoire** , sélectionnez la case d’option **instantané de tas** , puis appuyez sur le bouton **prendre un cliché instantané** .  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png":::
   Figure 4: instantané du tas  
:::image-end:::  

Le processus et le chargement de l’instantané risquent de prendre un certain temps.  Lorsque vous avez terminé, sélectionnez-le dans le volet de gauche \ ( **instantanés de tas**nommés \).  

Entrez `Detached` dans la zone de texte de **filtre de classe** pour rechercher des arborescences DOM détachées.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png":::
   Figure 5: filtrage pour les nœuds détachés  
:::image-end:::  

Développez le carats pour examiner une arborescence dissociée.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png":::
   Figure 6: examen de l’arborescence dissociée  
:::image-end:::  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

Sélectionnez un nœud pour le rechercher davantage.  Dans le volet **objets** , vous pouvez afficher davantage d’informations sur le code qui fait référence à celle-ci.  Par exemple, dans l’illustration suivante, vous pouvez voir que la `detachedNodes` variable fait référence au nœud.  Pour corriger cette fuite de mémoire particulière, vous devez examiner le code qui utilise la `detachedUNode` variable et garantir que la référence au nœud est supprimée lorsque vous n’en avez plus besoin.  

:::image type="complex" source="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png":::
   Figure 7: examen d’un nœud  
:::image-end:::  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## Identifier les fuites de mémoire du tas JS avec l’instrumentation d’allocation sur la chronologie  

L' **instrumentation d’allocation sur la chronologie** est un autre outil qui peut vous aider à effectuer le suivi des fuites de mémoire dans votre tas js.  

Montrez l' **instrumentation d’allocation sur la chronologie**  en utilisant le code suivant.  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

Chaque fois que le bouton référencé dans le code est envoyé, une chaîne de 1 million caractères est ajoutée au `x` tableau.  

Pour enregistrer une instrumentation d’allocation sur la chronologie, ouvrez DevTools, accédez au volet **mémoire** , sélectionnez la case **d’option allocation d’attribution sur la chronologie** , appuyez sur le bouton **Démarrer** , effectuez l’action que vous suspectez à l’origine de la fuite de mémoire, puis appuyez sur le bouton arrêter l’enregistrement du **profil de tas** ![ ][ImageStopRecordingIcon] lorsque vous avez terminé.  

Lors de l’enregistrement, Notez que les barres bleues s’affichent sur la chronologie, comme dans l’illustration suivante.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png":::
   Figure 8: nouvelles attributions  
:::image-end:::  

Ces barres bleues représentent de nouvelles allocations de mémoire.  Ces nouvelles allocations de mémoire sont vos candidats à des fuites de mémoire.  Vous pouvez effectuer un zoom sur une barre pour filtrer le volet **constructor** de façon à afficher uniquement les objets alloués au cours de la période spécifiée.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png":::
   Figure 9: chronologie de l’attribution avec zoom  
:::image-end:::  

Développez l’objet et sélectionnez la valeur pour afficher plus de détails dans le volet des **objets** .  Par exemple, dans l’illustration suivante, en affichant les détails de l’objet nouvellement alloué, vous devez être en mesure de voir qu’il a été alloué à la `x` variable dans l' `Window` étendue.  

:::image type="complex" source="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png":::
   Figure 10: détails de l’objet  
:::image-end:::  

## Examiner l’allocation de mémoire par fonction  

Utilisez le type de classement d' **échantillonnage de répartition** pour afficher l’allocation de mémoire par la fonction JavaScript.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png":::
   Figure 11: échantillonnage d’allocation d’enregistrement  
:::image-end:::  

1.  Sélectionnez la case d’option d’échantillonnage de l' **attribution** .  S’il existe un ouvrier sur la page, vous pouvez le sélectionner en tant que cible de profilage à l’aide du menu déroulant en regard du bouton **Démarrer** .  
1.  Appuyez sur le bouton **Démarrer** .  
1.  Effectuez les actions sur la page que vous voulez examiner.  
1.  Lorsque vous avez terminé, appuyez sur le bouton **arrêter** .  

DevTools montre une répartition de la capacité d’allocation de mémoire par fonction.  Le mode par défaut est **gras (en bas)**, qui affiche les fonctions qui ont alloué la plus grande quantité de mémoire en haut.  

:::image type="complex" source="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png" alt-text="Ouverture du gestionnaire des tâches du navigateur Microsoft Edge" lightbox="../media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png":::
   Figure 12: Echantillonnage de l’attribution  
:::image-end:::  

## Nettoyage de la mémoire  

Si votre page semble être suspendue fréquemment, il est possible que vous ayez des problèmes de nettoyage de la mémoire.  

Vous pouvez utiliser le gestionnaire des tâches du navigateur Microsoft Edge ou des enregistrements de mémoire de performance pour détecter régulièrement un nettoyage de la mémoire.  Dans le gestionnaire des tâches du navigateur Microsoft Edge, il est fréquent de hausser et de reculer la **mémoire** ou les valeurs de **mémoire JavaScript** .  Dans les enregistrements de performance, les modifications fréquentes \ (augmentation et chute de \) sur le tas ou le nombre de nœuds JS indiquent fréquemment un nettoyage de la mémoire.  

Une fois que vous avez identifié le problème, vous pouvez utiliser un **instrumentation d’allocation sur la chronologie** pour savoir où la quantité de mémoire est allouée et quelles fonctions entraînent les attributions.  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageForceGarbageCollectionIcon]: ../media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: ../media/stop-recording-icon.msft.png  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Performance des enregistrements-référence d’analyse des performances"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
