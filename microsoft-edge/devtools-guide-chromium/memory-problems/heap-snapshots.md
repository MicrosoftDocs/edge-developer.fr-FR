---
description: Découvrez comment enregistrer des instantanés de tas à l’Microsoft Edge profileur de tas DevTools et rechercher des fuites de mémoire.
title: Comment enregistrer des captures instantanées de tas
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 5f097cc45facc7f366a99a9564cf6f3d443f2058
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11565014"
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
# <a name="how-to-record-heap-snapshots"></a>Comment enregistrer des captures instantanées de tas  

Découvrez comment enregistrer des instantanés de tas à l’Microsoft Edge profileur de tas DevTools et rechercher des fuites de mémoire.  

Le Microsoft Edge profileur de tas DevTools affiche la distribution de mémoire par les objets JavaScript et les nodes DOM associés de votre page.  Utilisez-le pour prendre des instantanés de tas JavaScript \(tas JS\), analyser des graphiques de mémoire, comparer des captures instantanées et rechercher des fuites de mémoire.  Accédez à [Objets en conservant l’arborescence][DevtoolsMemoryProblems101ObjectsRetainingTree].  

## <a name="take-a-snapshot"></a>Prendre une capture instantanée  

On the **Memory** panel, choose **Take snapshot,** then choose **Start**.  Vous pouvez également sélectionner `Ctrl` + `E` \(Windows, Linux\) ou `Cmd` + `E` \(macOS\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png" alt-text="Choisir le type de profilage" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots.msft.png":::
   Choisir le type de profilage  
:::image-end:::  

**Les captures instantanées** sont initialement stockées dans la mémoire du processus de rendu.  Les captures instantanées sont transférées vers DevTools à la demande, lorsque vous choisissez sur l’icône de capture instantanée pour l’afficher.  

Une fois que la capture instantanée a été chargée dans DevTools et qu’elle a été l’objet d’une recherche, le nombre en dessous du titre de la capture instantanée apparaît et indique la taille totale des objets [JavaScript accessibles.][DevtoolsMemoryProblems101ObjectSizes]  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png" alt-text="Taille totale des objets accessibles" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all.msft.png":::
   Taille totale des objets accessibles  
:::image-end:::  

> [!NOTE]
> Seuls les objets accessibles sont inclus dans les captures instantanées.  En outre, la prise d’une capture instantanée commence toujours par un garbage collection.  

## <a name="clear-snapshots"></a>Effacer des captures instantanées  

Sélectionnez **Effacer l’icône** De tous les profils pour supprimer les captures instantanées \(à la fois de DevTools et de toute mémoire associée au processus de rendu\).  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png" alt-text="Supprimer des captures instantanées" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-all-hover-clear-all-profiles.msft.png":::
   Supprimer des captures instantanées  
:::image-end:::  

La fermeture de la fenêtre DevTools ne supprime pas les profils de la mémoire associée au processus de rendu.  Lors de la réouverture de DevTools, toutes les captures instantanées précédemment prises réapparaissent dans la liste des captures instantanées.  

> [!NOTE]
> Essayez cet exemple d’objets [en nuages de points et][GlitchDevtoolsMemoryExample03] profilez-le à l’aide du Profileur de tas.  Un certain nombre d’allocations d’éléments \(object\) sont affichées.  

## <a name="view-snapshots"></a>Afficher des captures instantanées  

Afficher des captures instantanées sous différentes perspectives pour différentes tâches.  

**L’affichage résumé** montre les objets regroupés par nom de constructeur.  Utilisez-le pour trouver les objets \(et l’utilisation de la mémoire\) en fonction du type groupé par nom de constructeur.  Il est particulièrement utile pour **le suivi des fuites DOM**.

<!--todo: add profile memory problems memory diagnosis (tracking down DOM leaks) section when available  -->  

**Vue de comparaison**.  Affiche la différence entre deux captures instantanées.  Utilisez-le pour comparer deux captures instantanées de mémoire \(ou plus\) avant et après une opération.  L’inspection du delta dans la mémoire libérée et le nombre de références vous permet de confirmer la présence et la cause d’une fuite de mémoire.  

**Affichage d’endiguement**.  Permet d’explorer le contenu du tas.  **La vue d’endiguement** fournit une meilleure vue de la structure des objets, ce qui permet d’analyser les objets référencés dans l’espace de noms global \(window\) pour savoir ce qui permet de conserver les objets.  Utilisez-le pour analyser les fermetures et vous plonger dans vos objets à un niveau faible.  

Pour basculer entre les vues, utilisez le sélecteur en haut de l’affichage.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png" alt-text="Sélecteur de vues de commutateur" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-view-dropdown.msft.png":::
   Sélecteur de vues de commutateur  
:::image-end:::  

> [!NOTE]
> Toutes les propriétés ne sont pas stockées sur le tas JavaScript.  Les propriétés implémentées à l’aide de getters qui exécutent du code natif ne sont pas capturées.  En outre, les valeurs autres que des chaînes, telles que les nombres, ne sont pas capturées.  

### <a name="summary-view"></a>Affichage récapitulatif  

Initialement, une capture instantanée s’ouvre dans l’affichage Résumé, affichant les totaux des objets, qui peuvent être étendus pour afficher les instances :  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png" alt-text="Affichage récapitulatif" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-retainers.msft.png":::
   **Affichage récapitulatif**  
:::image-end:::  

Les entrées de niveau supérieur sont des lignes « total ».  

| Entrées de niveau supérieur | Description |  
|:--- |:--- |  
| **Constructeur** | Représente tous les objets créés à l’aide de ce constructeur.  |  
| **Distance** | affiche la distance d’accès à la racine à l’aide du chemin d’accès simple des nodes le plus court.  |  
| **Taille superficiele** | Affiche la somme des tailles superficiels de tous les objets créés par une fonction de constructeur.  La taille superficiele est la taille de la mémoire détenue par un objet \(généralement, les tableaux et les chaînes ont des tailles peu profondes plus grandes\).  Accédez à [tailles d’objet.][DevtoolsMemoryProblems101ObjectSizes]  |  
| **Taille conservée** | Affiche la taille maximale conservée parmi le même ensemble d’objets.  La taille de la mémoire que vous pouvez libérer après la suppression d’un objet \(et que les dépendants ne sont plus accessibles\) est appelée taille conservée.  Accédez à [tailles d’objet.][DevtoolsMemoryProblems101ObjectSizes]  |  

<!--| **Number of object instances** | Displayed in the # column.  |  -->  

Après avoir développé une ligne de total dans l’affichage supérieur, toutes les instances sont affichées.  Pour chaque instance, les tailles peu profondes et conservées sont affichées dans les colonnes correspondantes.  Le nombre après le caractère est l’ID unique de l’objet, ce qui vous permet de comparer des instantanés de tas `@` par objet.  

N’oubliez pas que les objets jaunes ont des références JavaScript et que les objets rouges sont des nodes détachées qui sont référencés à partir d’un seul avec un arrière-plan jaune.  

**À quoi correspondent les différentes entrées constructor \(group\) dans le profileur heap ?**  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png" alt-text="Groupes de constructeurs" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-constructor-highlight.msft.png":::
   **Groupes de constructeurs**  
:::image-end:::  

| Constructor \(group\) entry | Description |  
|:--- |:--- |  
| **\(global, propriété\)** | Objets intermédiaires entre un objet global \(like \) et un `window` objet référencé par celui-ci.  Si un objet est créé à l’aide d’un constructeur et qu’il est conservé par un objet global, le chemin de rétention peut `Person` être représenté par `[global] > \(global property\) > Person` .  Cela contraste avec la norme, où les objets se référencent directement les uns les autres.  Des objets intermédiaires existent pour des raisons de performances.  Les globales sont modifiées régulièrement et les optimisations de l’accès aux propriétés s’appliquent bien aux objets non globaux qui ne s’appliquent pas aux objets globaux.  |  
| **\(racines\)** | Les entrées racine dans l’arborescence de rétention sont les entités qui ont des références à l’objet sélectionné.  Les entrées peuvent également être des références créées par le moteur à des fins spécifiques au moteur.  Le moteur possède des caches qui référencent des objets, mais toutes ces références sont faibles et n’empêchent pas la collecte d’un objet, étant donné qu’il n’existe aucune référence vraiment forte.  |  
| **\(fermeture\)** | Nombre de références à un groupe d’objets par le biais de fermetures de fonctions.  |  
| **\(array, string, number, regexp\)** | Liste des types d’objets avec des propriétés qui font référence à une expression array, string, number ou régulière.  |  
| **\(code compilé\)** | Tout ce qui est lié au code compilé.  Le script est similaire à une fonction, mais correspond à un `<script>` corps.  SharedFunctionInfos \(SFI\) sont des objets se tenant entre les fonctions et le code compilé.  Les fonctions ont généralement un contexte, alors que les SFI ne le font pas.  |  
| **HTMLDivElement,** **HTMLAnchorElement,** **DocumentFragment,** etc.  | Références à des éléments ou des objets de document d’un type particulier référencé par votre code.  |  

<!--todo: add heap profiling summary section when available -->  

### <a name="comparison-view"></a>Vue de comparaison  

Recherchez les objets divulgués en comparant plusieurs captures instantanées les unes aux autres.  Pour vérifier qu’une certaine opération d’application ne crée pas de fuites \(par exemple, une paire d’opérations directes et inversées, comme l’ouverture d’un document, puis sa fermeture, ne doit pas laisser de mémoire\), vous pouvez suivre le scénario ci-dessous :  

1.  Prenez une capture instantanée de tas avant d’effectuer une opération.  
1.  Effectuez une opération \(interagissez avec une page d’une manière que vous pensez être à l’origine d’une fuite\).  
1.  Effectuez une opération inverse \(effectuez l’interaction opposée et répétez-la plusieurs fois\).  
1.  Prenez une deuxième capture instantanée de tas **** et modifiez l’affichage de celui-ci en comparaison avec la capture **instantanée 1.**  
    
Dans **l’affichage** Comparaison, la différence entre deux captures instantanées s’affiche.  Lors de l’extension d’une entrée totale, les instances d’objet ajoutées et supprimées sont affichées.  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png" alt-text="Vue de comparaison" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-comparison-dropdown.msft.png":::
   **Vue de** comparaison  
:::image-end:::  

<!--todo: add HeapProfilingComparison section when available  -->  

### <a name="containment-view"></a>Affichage d’endiguement  

La **vue Containment** est essentiellement une « vue d’enfant » de la structure des objets de votre application.  Il vous permet de regarder dans les fermetures de fonction, d’observer les objets internes de la machine virtuelle \(VM\) qui, ensemble, forment vos objets JavaScript et de comprendre la quantité de mémoire que votre application utilise à un niveau très faible.  

| Points d’entrée d’affichage de contenu | Description |  
|:--- |:--- |  
| **Objets DOMWindow** | Objets globaux pour le code JavaScript.  |  
| **Racines GC** | Racines GC réelles utilisées par la garbage de la VM.  Les racines GC sont composées de cartes d’objets intégrées, de tableaux de symboles, de piles de threads de vm, de caches de compilation, d’étendues de handle et de handles globaux.  |  
| **Objets natifs** | Objets de navigateur « pushed » à l’intérieur de la machine virtuelle JavaScript \(JavaScript VM\) pour autoriser l’automatisation, par exemple, les nodes DOM, les règles CSS.  |  

:::image type="complex" source="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png" alt-text="Affichage d’endiguement" lightbox="../media/memory-problems-gh-nodejs-benchmarks-run-memory-heap-snapshots-containment-dropdown.msft.png":::
   **Affichage d’endiguement**  
:::image-end:::  

<!--todo: add heap profiling containment section when available  -->  

> [!TIP]
> Conseil sur les fermetures.  Nommez les fonctions afin de pouvoir facilement faire la distinction entre les fermetures dans la capture instantanée.  Par exemple, cet exemple n’utilise pas de fonctions nommées.  
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
> L’extrait de code suivant utilise des fonctions nommées.  
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
> > Essayez cet exemple de la raison [pour laquelle il est `eval` important][GlitchDevtoolsMemoryExample07] d’analyser l’impact des fermetures sur la mémoire.  Vous pouvez également être intéressé par le suivi avec cet exemple qui vous permet d’enregistrer les [allocations de tas][GlitchDevtoolsMemoryExample08].  
> 

## <a name="look-up-color-coding"></a>Rechercher le codage des couleurs  

Les propriétés et les valeurs de propriétés des objets ont différents types et sont colorées en conséquence.  Chaque propriété possède l’un des quatre types.  

| Type de propriété | Description |  
|:--- |:--- |  
| **a: property** | Propriété normale avec un nom, accessible via l’opérateur `.` \(dot\) ou via `[` `]` la notation \(brackets\), par exemple `["foo bar"]` .  |  
| **0 : élément** | Propriété normale avec un index numérique, accessible via `[` `]` la notation \(brackets\).  |  
| **a: context var** |  Variable dans un contexte de fonction, accessible par le nom de la variable à partir de l’intérieur d’une fermeture de fonction.  |  
| **a: system prop** | Propriété ajoutée par la VM JavaScript, non accessible à partir du code JavaScript.  |  

Les objets désignés comme `System` n’ont pas de type JavaScript correspondant.  Chacune d’elles fait partie de l’implémentation du système d’objet de la VM JavaScript.  V8 alloue la plupart des objets internes dans le même tas que les objets JS de l’utilisateur.  Il s’uffit donc de V8 internes.  

## <a name="find-a-specific-object"></a>Rechercher un objet spécifique  

Pour rechercher un objet dans le tas collecté, vous pouvez effectuer une recherche à l’aide de `Ctrl` + `F` l’ID d’objet et lui donner son ID.  

## <a name="uncover-dom-leaks"></a>Découvrir les fuites DOM  

Le profileur de tas a la possibilité de refléter les dépendances bidirectionnelles entre les objets natifs du navigateur \(nodes DOM, règles CSS\) et les objets JavaScript.
Cela permet de découvrir les fuites invisibles qui se produisent en raison de sous-arbre DOM détachées oubliés flottant autour.  

Les fuites DOM peuvent être plus importantes que vous ne le pensez.  Prenons l’exemple suivant.  Quand le GC #tree-il ?  

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

Il conserve une référence à l’objet parent \(parentNode\) pertinent et de manière récursive jusqu’à , donc uniquement lorsque leafRef est nullifié est l’arborescence WHOLE sous un candidat pour `#leaf` `#tree` `#tree` GC.  

:::image type="complex" source="../media/memory-problems-tree-gc.msft.png" alt-text="Sous-arbre DOM" lightbox="../media/memory-problems-tree-gc.msft.png":::
   Sous-arbre DOM  
:::image-end:::  

> [!NOTE]
> Exemples : essayez cet exemple de fuite d’un nœud [DOM][GlitchDevtoolsMemoryExample06] pour comprendre où il peut être divulgué et comment le détecter.  Vous pouvez également examiner cet exemple de [fuites DOM plus importantes que prévu.][GlitchDevtoolsMemoryExample09]  

Pour en savoir plus sur les fuites DOM et les principes de base de l’analyse de la mémoire, consultez La recherche et le débogage des fuites de mémoire avec [les Microsoft Edge DevTools][GonzaloRuizdeVillaMemory] parPéroïenSyr.  

<!--  
> [!NOTE]
> Example: Try this **demo** to play with detached DOM trees.  
-->  

<!--todo: add heap profiling dom leaks section when available  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblems101ObjectSizes]: ./memory-101.md#object-sizes "Tailles des objets : terminologie de la mémoire | Documents Microsoft"  
[DevtoolsMemoryProblems101ObjectsRetainingTree]: ./memory-101.md#objects-retaining-tree "Objets conservant l’arborescence - Terminologie de la mémoire | Documents Microsoft"  

<!--[DevToolsHeapProfilingComparison]: https://developer.alphabet.com/devtools/docs/heap-profiling-comparison ""  -->  
<!--[DevToolsHeapProfilingContainment]: https://developer.alphabet.com/devtools/docs/heap-profiling-containment ""  -->  
<!--[DevtoolsHeapProfilingDomLeaks]: https://developer.alphabet.com/devtools/docs/heap-profiling-dom-leaks ""  -->  
<!--[DevToolsHeapProfilingSummary]: https://developer.alphabet.com/devtools/docs/heap-profiling-summary ""  -->  
<!--[DevtoolsProfileMemoryProblemsDiagnosisCausesMemoryLeaks]: ../profile/memory-problems/memory-diagnosis#narrow-down-causes-of-memory-leaks ""  -->  

[GlitchDevtoolsMemoryExample03]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-03.html "example-03.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample06]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-06.html "example-06.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample07]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-07.html "example-07.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample08]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-08.html "example-08.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample09]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-09.html "example-09.html - Microsoft Edge (Chromium) DevTools | Glitch"  
[GlitchDevtoolsMemoryExample10]: https://microsoft-edge-chromium-devtools.glitch.me/static/memory/example-10.html "example-10.html - Microsoft Edge (Chromium) DevTools | Glitch"  

[GonzaloRuizdeVillaMemory]: https://slid.es/gruizdevilla/memory "mémoire | Diapositives"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/heap-snapshots) et est co-auteure par [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[MegginKearney]: https://developers.google.com/web/resources/contributors#meggin-kearney  
