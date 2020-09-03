---
description: Découvrez comment enregistrer des instantanés de tas avec le profileur de segments de DevTools Microsoft Edge et Rechercher des fuites de mémoire.
title: Enregistrement des instantanés des tas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 15692b0258de6db66c0b58a2659348a6e849aaca
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993470"
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
   limitations under the License.  -->

# Enregistrement des instantanés des tas  

Découvrez comment enregistrer des instantanés de tas avec le profileur de segments de DevTools Microsoft Edge et Rechercher des fuites de mémoire.  

Le Microsoft Edge DevTools de segment de mémoire montre la distribution de mémoire par les objets JavaScript et les nœuds DOM associés de votre page.  Utilisez-la pour prendre des instantanés de tas JavaScript \ (JS Heap \) instantanés, analyser les graphiques de mémoire, comparer des instantanés et détecter des fuites de mémoire.  Voir aussi [objets en conservation d’arborescence][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## Prendre un cliché  

Dans le panneau **mémoire** , sélectionnez **prendre une photo**, puis cliquez sur **Démarrer**.  Vous pouvez également appuyer sur `Ctrl` + `E` \ (Windows \) ou `Cmd` + `E` \ (MacOS \).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Sélectionner type de profil" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Sélectionner type de profil  
:::image-end:::  

Les **captures instantanées** sont initialement stockées dans la mémoire du processus de rendu.  Les captures d’écran sont transférées au DevTools à la demande, lorsque vous cliquez sur l’icône de capture d’écran.  

Une fois la capture instantanée chargée dans DevTools et analysée, le numéro sous le titre de l’instantané s’affiche et indique la [taille totale des objets JavaScript accessibles][DevtoolsMemoryProblems101ObjectSizes].  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Taille totale des objets accessibles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Taille totale des objets accessibles  
:::image-end:::  

> [!NOTE]
> Seuls les objets joignable sont inclus dans les captures d’image.  En outre, le fait de prendre un instantané commence toujours par un nettoyage de la mémoire.  

## Effacer des instantanés  

Cliquez sur l’icône **Effacer tous les profils** pour supprimer les snapshots \ (à la fois du devtools et de la mémoire associée au processus de rendu.).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Supprimer des snapshots" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Supprimer des snapshots  
:::image-end:::  

La fermeture de la fenêtre DevTools ne supprime pas les profils de la mémoire associée au processus de convertisseur.  Lors de la réouverture de DevTools, tous les instantanés précédemment exécutés apparaissent dans la liste des instantanés.  

> [!NOTE]
> Testez cet exemple d' [objets disséminés][GlitchDevtoolsMemoryExample03] et profilez-le à l’aide du profileur de tas.  Vous devez voir un certain nombre d’attributions d’éléments \ (objet \).  

## Afficher des instantanés  

Affichez les captures d’écran de différentes perspectives pour différentes tâches.  

**Vue récapitulative** montre les objets regroupés par nom de constructeur.  Vous pouvez l’utiliser pour rechercher les objets \ (et l’utilisation de la mémoire \) en fonction du type de nom de constructeur.  Elle est particulièrement utile pour effectuer **le suivi des fuites DOM**.

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Affichage comparaison**.  Affiche la différence entre deux instantanés.  Utilisez-la pour comparer deux ou plusieurs \ instantanés de mémoire de avant et après une opération.  L’examen de la quantité de mémoire et de la mémoire libérée permet de vérifier la présence et la cause d’une fuite de mémoire.  

**Affichage contenant**.  Autorise l’exploration du contenu du tas.  Le **mode** de conservation fournit une meilleure vue de la structure de l’objet, facilitant l’analyse des objets référencés dans l’espace de noms global \ (fenêtre \) pour découvrir ce qu’ils conservent.  Utilisez-le pour analyser les fermetures et explorer vos objets à un niveau faible.  

Pour basculer entre les affichages, utilisez le sélecteur en haut de la vue.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Changer de sélecteur de vues" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Changer de sélecteur de vues  
:::image-end:::  

> [!NOTE]
> Toutes les propriétés ne sont pas stockées dans le tas JavaScript.  Les propriétés implémentées à l’aide d’accesseurs qui exécutent du code natif ne sont pas capturées.  Par ailleurs, les valeurs qui ne sont pas des chaînes telles que des nombres ne sont pas capturées.  

### Affichage de synthèse  

À l’origine, une capture d’écran s’ouvre dans l’affichage de synthèse et affiche les totaux d’objets, qui risquent d’être développés pour afficher les instances:  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Affichage de synthèse" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   Affichage de **synthèse**  
:::image-end:::  

Les entrées de niveau supérieur correspondent à des lignes «total».  

| Entrées de niveau supérieur | Description |  
|:--- |:--- |  
| **Constructeur** | Représente tous les objets créés à l’aide de ce constructeur.  |  
| **Distance** | affiche la distance à la racine en utilisant le chemin de nœud simple le plus court.  |  
| **Taille superficielle** | Affiche la somme de tailles superficielles de tous les objets créés par une certaine fonction Constructor.  La taille superficielle correspond à la taille de la mémoire maintenue par un objet \ (en général, les tableaux et les chaînes ont des tailles superficielles plus grandes».  Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].  |  
| **Taille retenue** | Affiche la taille maximale conservée entre le même jeu d’objets.  La taille de mémoire que vous pouvez libérer après la suppression d’un objet (et les dépendants n’est plus joignable \) est appelée taille retenue.  Voir aussi [tailles d’objet][DevtoolsMemoryProblems101ObjectSizes].  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Après avoir étendu une ligne du total dans l’affichage supérieur, toutes les instances sont affichées.  Pour chaque instance, les tailles superficielle et retenue sont affichées dans les colonnes correspondantes.  Le nombre après le `@` caractère est l’identificateur unique de l’objet, ce qui vous permet de comparer les instantanés de tas en fonction de chaque objet.  

N’oubliez pas que les objets jaunes possèdent des références JavaScript et des objets rouges sont des nœuds détachés qui sont référencés à partir d’un arrière-plan jaune.  

**À quoi correspondent les différentes entrées de Constructor (Group \) dans le générateur de mémoire de segment?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Groupes de constructeurs" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   Groupes de **constructeurs**  
:::image-end:::  

| Entrée Constructor (groupe \) | Description |  
|:--- |:--- |  
| **\ (propriété globale \)** | Objets intermédiaires entre un objet global \ (par exemple, `window` \) et un objet référencé par celui-ci.  Si un objet est créé à l’aide d’un constructeur `Person` et est maintenu par un objet global, le chemin d’accès de conservation ressemble à ceci `[global] > \(global property\) > Person` .  Cela contraste avec la norme, où les objets se référencent directement.  Il existe des objets intermédiaires pour des raisons de performances.  Les éléments globaux sont modifiés régulièrement et les optimisations d’accès aux propriétés font l’objet d’un bon travail pour les objets non globaux et ne s’applique pas aux globales.  |  
| **\ (racines \)** | Les entrées racines dans l’arborescence conservation sont les entités qui contiennent des références à l’objet sélectionné.  Les entrées pourront également être des références créées par le moteur pour des raisons spécifiques au moteur.  Le moteur comporte des mises en cache qui font référence aux objets, mais ces références sont faibles et n’empêchent pas la collecte d’un objet en raison de l’absence de références réellement fortes.  |  
| **\ (fermeture \)** | Nombre de références à un groupe d’objets par le biais de la fermeture de fonction.  |  
| **\ (matrice, chaîne, nombre, RegExp \)** | Liste de types d’objets avec des propriétés qui font référence à un tableau, une chaîne, un nombre ou une expression régulière.  |  
| **\ (code compilé \)** | Tout ce qui concerne le code compilé.  Le script est semblable à une fonction, mais correspond à un `<script>` corps.  SharedFunctionInfos \ (SFI \) les objets se trouvent dans les fonctions et dans le code compilé.  Les fonctions disposent généralement d’un contexte, même si SFIs.  |  
| **HTMLDivElement**, **HTMLAnchorElement**, **DocumentFragment**, etc.  | Fait référence à des éléments ou des objets document d’un type particulier référencé par votre code.  |  

<!--todo: add heap profiling summary section when available -->  

### Affichage comparaison  

Recherchez les objets perdus en comparant plusieurs instantanés entre eux.  Pour vérifier que l’opération d’une certaine application ne crée pas de fuites (par exemple, une paire d’opérations directes ou inverses, telles que l’ouverture d’un document, puis la fermeture, ne doit pas laisser de place à un autre), vous pouvez suivre le scénario suivant:  

1.  Prenez un instantané de tas avant d’exécuter une opération.  
1.  Effectuer une opération \ (interagissez avec une page d’une manière que vous pensez être à l’origine d’une fuite \).  
1.  Effectuez une opération inverse \ (faites l’interaction inverse et répétez-la quelques fois...).  
1.  Prenez un second instantané de tas et changez le mode d’affichage de celui-ci en **comparaison**, en le comparant à **snapshot 1**.  
    
Dans l’affichage **comparaison** , la différence entre les deux instantanés s’affiche.  Lorsque vous développez une entrée de total, des instances d’objet ajoutées et supprimées sont affichées.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Affichage comparaison" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   Affichage **comparaison**  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### Affichage contenant  

Le mode de **confinement** est essentiellement une vue aérienne de la structure Objects de votre application.  Elle vous permet de lire dans les fermetures de fonctions, d’observer les objets internes de machine virtuelle \ (VM \) qui constituent vos objets JavaScript et de comprendre la quantité de mémoire utilisée par votre application à un niveau très bas.  

| Points d’entrée du mode contenant | Description |  
|:--- |:--- |  
| **Objets DOMWindow** | Objets globaux pour le code JavaScript.  |  
| **Racines GC** | Les racines du GC réel utilisées par le nettoyage de la mémoire virtuelle.  Les racines de catalogue global sont composées de cartes d’objets intégrés, de tableaux de symboles, de piles de threads d’ordinateur de construction, de caches de compilation, de gestionnaires d’étendues et de descripteurs globaux.  |  
| **Objets natifs** | Objets de navigateur «Push» à l’intérieur de la machine virtuelle JavaScript (VM) pour autoriser l’automatisation (par exemple, les nœuds DOM et les règles CSS).  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Affichage contenant" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   Affichage **contenant**  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Astuce sur les fermetures.  Nommez les fonctions pour pouvoir distinguer facilement les fermetures de l’instantané.  Par exemple, cet exemple n’utilise pas de fonctions nommées.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function() { // this is NOT a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> L’extrait de followingcode utilise des fonctions nommées.  
> 
> ```javascript
> function createLargeClosure() {
>     var largeStr = new Array(1000000).join('x');
>     var lC = function lC() { // this IS a named function
>         return largeStr;
>     };
>     return lC;
> }
> ```  
> 
> <!--  
> :::image type="complex" source="../media/memory-problems-domleaks.msft.png" alt-text="Name functions to distinguish between closures" lightbox="../media/memory-problems-domleaks.msft.png":::
>    Name functions to distinguish between closures  
> :::image-end:::  
> -->  
> 
> > [!NOTE]
> > Essayez cet exemple pour savoir [pourquoi `eval` ][GlitchDevtoolsMemoryExample07] un élément malveillant analyse l’impact de la fermeture sur la mémoire.  Vous serez peut-être également intéressé par le suivi de cet exemple qui vous permet d’accéder à des [allocations de tas][GlitchDevtoolsMemoryExample08]d’enregistrements.  
> 

## Chercher un codage en couleurs  

Les propriétés et valeurs de propriété des objets ont des types différents et sont en conséquence.  Chaque propriété comporte l’un des quatre types suivants.  

| Type de propriété | Description |  
|:--- |:--- |  
| **a: propriété** | Propriété standard avec un nom, accessible par le biais de l' `.` opérateur \ (point \) ou par le biais `[` `]` de la notation \ (crochets \), par exemple `["foo bar"]` .  |  
| **0: élément** | Propriété standard avec un index numérique, accessible via la `[` `]` notation \ (crochets \).  |  
| **a: var du contexte** |  Variable dans un contexte de fonction, accessible par le nom de la variable à partir de la fermeture d’une fonction.  |  
| **a: système prop** | Propriété ajoutée par le VM JavaScript, qui n’est pas accessible à partir du code JavaScript.  |  

Les objets désignés comme `System` ne disposant pas d’un type JavaScript correspondant;  Chacun fait partie de l’implémentation du système d’objets de la machine virtuelle JavaScript.  V8 alloue la plupart des objets internes dans le même segment de mémoire que les objets JS de l’utilisateur.  C’est alors que les éléments internes sont uniquement en interne.  

## Rechercher un objet spécifique  

Pour rechercher un objet dans le tas collecté, vous pouvez effectuer une recherche sur l’ID de l' `Ctrl` + `F` objet.  

## Découvrir les fuites DOM  

Le profileur de tas a la possibilité de répercuter les dépendances bidirectionnelles entre les objets natifs du navigateur (nœud DOM, règles CSS \) et objets JavaScript.
Cela permet de détecter d’éventuelles fuites de fuite en raison de l’oubli d’arborescences DOM dissociées.  

Les fuites DOM risquent d’être plus grandes que vous ne le pensez.  Prenons l’exemple suivant.  Quand est-ce que le CG #tree?  

```javascript
var select = document.querySelector;
var treeRef = select("#tree");
var leafRef = select("#leaf");
var body = select("body");
body.removeChild(treeRef);
//#tree in not GC yet due to treeRef
treeRef = null;
//#tree is not GC yet due to indirect
//reference from leafRef
leafRef = null;
//#NOW able to be #tree GC
```  

Le `#leaf` maintien d’une référence au parent approprié \ (ParentNode \) et de manière récurrente jusqu’à ce que le `#tree` leafRef soit annulé comme l’arborescence entière sous `#tree` un candidat pour le CG.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Sous-arbres DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Sous-arbres DOM  
:::image-end:::  

> [!NOTE]
> Exemples: Essayez cet exemple de [nœud DOM en fuite][GlitchDevtoolsMemoryExample06] pour savoir où il est susceptible de fuir et comment le détecter.  Vous pouvez également examiner cet exemple de [fuites DOM plus grandes que prévu][GlitchDevtoolsMemoryExample09].  

Pour en savoir plus sur les fuites DOM et l’analyse en mémoire notions fondamentales sur [la recherche et le débogage de fuites de mémoire avec Microsoft Edge devtools][GonzaloRuizdeVillaMemory] par Gonzalo Ruiz de Villa.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tailles d’objets-terminologie de mémoire | Documents Microsoft"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Objets qui conservent une terminologie en mémoire en arborescence | Documents Microsoft"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html-Microsoft Edge (chrome) DevTools | Problème"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html-Microsoft Edge (chrome) DevTools | Problème"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "mémoire | Diapo"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney  
