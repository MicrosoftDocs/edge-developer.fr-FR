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

# <a name="memory-terminology"></a>Terminologie de la mémoire  

Cet article décrit les termes courants utilisés dans l'analyse de la mémoire et s'applique à divers outils de profilage de mémoire pour différentes langues.  

Les termes et les notions décrits ici font référence au [panneau Mémoire.][DevtoolsMemoryProblemsHeapSnapshots]  Si vous avez déjà travaillé avec le Java, .NET ou un autre profileur de mémoire, cet article peut être actualisé.  

## <a name="object-sizes"></a>Tailles des objets  

Pensez à la mémoire sous la forme d'un graphique avec des types primitifs \(tels que des nombres et des chaînes\) et des objets \(tableaux associatifs\).  Il peut s'afficher sous la forme d'un graphique avec de nombreux points interconnectés tels que la figure suivante.  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Représentation visuelle de la mémoire" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   Représentation visuelle de la mémoire  
:::image-end:::  

Un objet peut contenir de la mémoire de deux manières :  

*   Directement par l'objet.  
*   Implicitement en maintenant des références à d'autres objets, et par conséquent en empêchant leur élimination automatique par un garbage collector.  

Lorsque vous [][DevtoolsMemoryProblemsHeapSnapshots] travaillez avec le panneau Mémoire dans DevTools \(un outil permettant d'examiner les problèmes de mémoire trouvés sous **Mémoire**\), vous pouvez vous retrouver en regardant différentes colonnes d'informations.  Deux éléments se démarquent par la taille **superficiele** et la **taille conservée,** mais que représentent-ils ?  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Tailles superficiels et conservées" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   Tailles superficiels et conservées  
:::image-end:::  

### <a name="shallow-size"></a>Taille superficiele  

Il s'agit de la taille de la mémoire détenue par l'objet.  

La mémoire des objets JavaScript classiques est réservée à leur description et au stockage des valeurs immédiates.  En règle générale, seuls les tableaux et les chaînes peuvent avoir une taille faible significative.  Toutefois, les chaînes et les tableaux externes ont souvent leur stockage principal dans la mémoire du renderer, exposant uniquement un petit objet wrapper sur le tas JavaScript.  

La mémoire du renderer est l'ensemble de la mémoire du processus dans lequel une page inspectée est rendue : mémoire native + mémoire de tas JS de la page + mémoire de tas JS de tous les travailleurs dédiés démarrés par la page.  Néanmoins, même un petit objet peut contenir une grande quantité de mémoire indirectement, en empêchant d'autres objets d'être éliminés par le processus de collecte automatique de la mémoire.  

### <a name="retained-size"></a>Taille conservée  

Il s'agit de la taille de la mémoire qui est libérée une fois que l'objet est supprimé avec les objets dépendants qui ont été rendues inaccessibles à partir des racines garbage **collector**.  

**Les racines** du Garbage Collector sont des **poignées créées** \(locales ou globales\) lors de la création d'une référence à partir de code natif à un objet JavaScript en dehors de V8.  Tous ces handles peuvent être trouvés dans un instantané de tas sous **des racines GC**Handle scope et GC  >  **** ****  >  **racines Global handles**.  Décrire les descripteurs de cette documentation sans plonger dans les détails de l'implémentation du navigateur peut prêter à confusion.  Les racines du garbage collector et les poignées ne sont pas des sujets dont vous avez besoin.  

Il existe de nombreuses racines de garbage collector internes, dont la plupart ne sont pas intéressantes pour les utilisateurs.  Du point de vue des applications, il existe les types de racines suivants.  

*   Objet global Window \(dans chaque iframe\).  Dans les captures instantanées de tas, le champ indique le nombre de références de propriétés sur le chemin de rétention le plus court `distance` de la fenêtre.  
*   Arborescence DOM du document, constituée de tous les nodes DOM natifs accessibles en parcourant le document.  Tous les nœuds n'ont pas de wrappers JavaScript, mais si un nœud possède un wrapper, le nœud est présent alors que le document est en cours d'utilisation.  
*   Parfois, les objets sont conservés par le contexte de débogage dans l'outil **Sources** et la **console,** par exemple après l'évaluation de la console.  Créez des captures instantanées de tas avec un outil **console** effacé et aucun point d'arrêt actif dans le débogger de l'outil **Sources.**

>[!TIP]
> Avant de prendre une [][DevtoolsMemoryProblemsHeapSnapshots] capture instantanée du tas dans l'outil Mémoire, désactivez l'outil **Console** et désactivez les points d'arrêt dans l'outil **Sources.**  Pour effacer **l'outil Console,** exécutez la `clear()` méthode.  

Le graphique de mémoire commence par une racine, qui peut être l'objet du navigateur ou l'objet `window` `Global` d'Node.js module.  Vous ne contrôlez pas la façon dont l'objet racine est collecté.  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Vous ne pouvez pas contrôler la façon dont l'objet racine est collecté." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   Vous ne pouvez pas contrôler la façon dont l'objet racine est collecté.  
:::image-end:::  

Tout ce qui n'est pas accessible à partir de la racine récupère la garbage collected.  

> [!NOTE]
> Les [colonnes Taille superficiele et](#shallow-size) [Taille conservée](#retained-size) représentent toutes deux des données en octets.  

## <a name="objects-retaining-tree"></a>Objets conservant l'arborescence  

Le tas est un réseau d'objets interconnectés.  Dans le monde mathématique, cette structure est appelée graphique **ou** graphique mémoire.  Un graphique est construit à partir **de nods** connectés à l'aide de **bords,** qui sont tous deux attribués à des étiquettes.  

*   **Les nodes** \(ou objets \) sont **étiquetés**à l'aide du nom de la fonction constructeur qui a été utilisée pour les créer. ****  
*   **Les bords** sont étiquetés à l'aide des noms des **propriétés.**  

Découvrez [comment enregistrer un profil à l'aide du profileur de tas.][DevtoolsMemoryProblemsHeapSnapshots]  Dans la figure suivante, certains des éléments notables [][DevtoolsMemoryProblemsHeapSnapshots] de l'enregistrement instantané de tas dans l'outil Mémoire incluent la distance : la distance par rapport à la racine du garbage collector.  Si presque tous les objets du même type sont à la même distance et que certains d'entre eux sont à une plus grande distance, cela vaut la peine d'examiner ce point.  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distance par rapport à la racine" lightbox="../media/memory-problems-root.msft.png":::
   Distance par rapport à la racine  
:::image-end:::  

## <a name="dominators"></a>Dominants  

Les objets dominants sont constitués d'une arborescence, car chaque objet possède exactement un seul dominant.  Un dominant d'un objet peut ne pas avoir de références directes à un objet qu'il dirige ; autrement dit, l'arborescence du sous-arbre n'est pas une arborescence couvrante du graphique.  

Dans la figure suivante, l'instruction suivante est vraie.  

*   Nœud 1 nœud 2  
*   Nœud 2 nœuds 3, 4 et 6  
*   Nœud 3 nœud 5  
*   Nœud 5 nœud 8  
*   Nœud 6 nœud 7  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Structure de l'arborescence de l'dominant" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   Structure de l'arborescence de l'dominant  
:::image-end:::  

Dans la figure suivante, le nœud est l'en-avant-première de , mais il existe également dans chaque chemin simple du garbage `#3` `#10` collector à `#7` `#10` .  Par conséquent, un objet B est le résorbateur d'un objet A si B existe dans chaque chemin d'accès simple de la racine à l'objet A.  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Illustration de l'animation de l'animation de l'animation" lightbox="../media/memory-problems-dominators.msft.gif":::
   Illustration de l'animation de l'animation de l'animation  
:::image-end:::  

## <a name="v8-specifics"></a>Spécificités V8  

Lors du profilage de la mémoire, il est utile de comprendre pourquoi les captures instantanées de tas semblent d'une certaine façon.  Cette section décrit certaines rubriques relatives à la mémoire qui correspondent spécifiquement à la machine virtuelle **JavaScript V8** \(V8 V8 VM ou VM\).  

### <a name="javascript-object-representation"></a>Représentation d'objet JavaScript  

Il existe trois types primitifs :  

*   Nombres \(par exemple `3.14159...` \)  
*   Booléens \( `true` ou `false` \)  
*   Chaînes \(par exemple `"Werner Heisenberg"` \)  

Les primitives ne peuvent pas référencer d'autres valeurs et sont toujours des feuilles ou des nodes terminaux.  

**Les** nombres peuvent être stockés sous l'une ou l'autre des façons :  

*   valeurs d'un nombre integer 31 bits immédiatement appelées petits **nombres d'nombres integers** \(**SMI**s\) ou  
*   objets de tas, appelés nombres **de tas**. Les nombres de tas sont utilisés pour stocker les valeurs qui ne s'intègrent pas dans le formulaire SMI, telles que les **doubles,** ou lorsqu'une valeur doit être encadrée, **** par exemple la définition de propriétés sur celui-ci.  

**Les** chaînes peuvent être stockées dans :  

*   le **tas de la VM,** ou
*   externe dans la **mémoire du renderer**.  Un **objet wrapper** est créé et utilisé pour accéder au stockage externe où, par exemple, les sources de script et d'autres contenus reçus à partir du Web sont stockés, plutôt que copiés sur le tas de l'environnement de ligne de disque.

La mémoire pour les nouveaux objets JavaScript est allouée à partir d'un tas JavaScript dédié \(ou d'un tas **de vm**\).  Ces objets sont gérés par le garbage collector dans V8 et, par conséquent, restent en vie tant qu'il existe au moins une référence forte à ces objets.  

Tout ce qui ne se trouve pas dans le tas JavaScript est appelé **un objet natif.**  Les objets natifs, contrairement aux objets tas, ne sont pas gérés par le garbage collector V8 tout au long de leur durée de vie et peuvent uniquement être accessibles à partir de JavaScript à l'aide de l'objet wrapper JavaScript.  

**La chaîne** Cons est un objet qui se compose de paires de chaînes stockées, puis jointes, et est le résultat de la concatenation.  La jointation du contenu de la **chaîne cons se** produit uniquement selon les besoins.  Par exemple, lorsqu'une sous-chaîne d'une chaîne jointe doit être construite.

Par exemple, si vous concaténer et , vous obtenez une chaîne qui représente le `a` `b` résultat de la `(a, b)` concaténation.  Si vous avez concaté ultérieurement `d` avec ce résultat, vous obtenez une autre **chaîne de inconvénients**: `((a, b, d)` .  

**Le** tableau est un objet avec des clés numériques. **Les tableaux** sont largement utilisés dans la V8 VM pour stocker de grandes quantités de données. Les ensembles de paires clé-valeur, tels que les dictionnaires, sont backed up par **des tableaux**.  

Un objet JavaScript classique est stocké comme un seul des deux types **de tableau** :  

*   propriétés nommées et  
*   éléments numériques  

Lorsqu'il existe un petit nombre de propriétés, les propriétés sont stockées en interne dans l'objet JavaScript.  

**Map** est un objet qui décrit à la fois le type d'objet et la disposition. Par exemple, les cartes sont utilisées pour décrire les hiérarchies d'objets implicites pour un [accès rapide aux propriétés.][V8FastProperties]  

### <a name="object-groups"></a>Groupes d'objets  

Chaque **groupe d'objets natifs** est composé d'objets qui tiennent des références mutuelles les uns aux autres.  Considérons, par exemple, une sous-arbre DOM où chaque nœud possède un lien vers le parent relatif et des liens vers l'enfant suivant et le frère suivant, ce qui a pour effet de former un graphique connecté.  

> [!NOTE]
> Les objets natifs ne sont pas représentés dans le tas JavaScript.  L'absence de représentation est la raison pour laquelle les objets natifs ont une taille nulle. Au lieu de cela, les objets wrapper sont créés.  

Chaque objet wrapper contient une référence à l'objet natif correspondant, pour rediriger les commandes vers celui-ci.  À son tour, un groupe d'objets contient des objets wrapper.  Toutefois, cela ne crée pas de cycle non récollectable, car le Garbage Collector est suffisamment intelligent pour libérer les groupes d'objets dont les wrappers ne sont plus référencés.  Mais l'oubli de libérer un seul wrapper contient le groupe entier et les wrappers associés.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Comment enregistrer des instantanés de tas | Documents Microsoft"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriétés rapides dans V8 | V8"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d'origine se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) et est co-auteure par [Meggin Kearney][MegginKearney] \(Technical Writer\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
