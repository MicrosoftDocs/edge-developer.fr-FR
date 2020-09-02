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

# Terminologie de mémoire  

Cette section décrit les termes courants utilisés en analyse de la mémoire et est applicable à un large éventail d’outils de profilage de mémoire pour différentes langues.  

Les termes et notions décrits ici font référence au [panneau mémoire][DevtoolsMemoryProblemsHeapSnapshots].  Si vous avez déjà utilisé le Java, .NET ou un autre profileur de mémoire, il peut s’agir d’un rappel.  

## Tailles d’objets  

Considérez la mémoire comme un graphique avec les types primitifs \ (comme les nombres et les chaînes \) et les objets \ (matrices associatives \).  Elle peut être représentée visuellement sous forme de graphique à l’aide d’un certain nombre de points interconnectés comme suit:  

:::image type="complex" source="../media/memory-problems-thinkgraph.msft.png" alt-text="Représentation visuelle de la mémoire" lightbox="../media/memory-problems-thinkgraph.msft.png":::
   Représentation visuelle de la mémoire  
:::image-end:::  

Un objet risque de contenir de la mémoire de deux manières:  

*   Directement par l’objet.  
*   Par le biais d’un nettoyage de la mémoire, le nettoyage de la mémoire et la suppression**automatique de ces** objets sont implicites.  

Lorsque vous travaillez avec le panneau [mémoire][DevtoolsMemoryProblemsHeapSnapshots] dans devtools \ (outil permettant d’identifier les problèmes de mémoire détectés dans la **mémoire**), vous pouvez vous présenter quelques colonnes d’information différentes.  Deux éléments qui ressortent sont les suivants: **taille superficielle** et **taille préservée**, mais qu’est-ce que cela représente?  

:::image type="complex" source="../media/memory-problems-shallow-retained.msft.png" alt-text="Taille superficielle et conservée" lightbox="../media/memory-problems-shallow-retained.msft.png":::
   Taille superficielle et conservée  
:::image-end:::  

### Taille superficielle  

Il s’agit de la taille de mémoire qui est maintenue par l’objet.  

Une mémoire est réservée aux objets JavaScript typiques et pour le stockage des valeurs immédiates.  En règle générale, seuls les tableaux et les chaînes peuvent avoir une taille superficielle significative.  Toutefois, les chaînes et les tableaux externes disposent souvent de leur stockage principal dans la mémoire du convertisseur, en exposant uniquement un petit objet wrapper sur le tas JavaScript.  

La mémoire du convertisseur correspond à toute la mémoire du processus sur lequel une page inspectée est affichée: mémoire Native + pile de tas JS de la mémoire du tas page + JS de tous les travailleurs dédiés démarrés par la page.  Néanmoins, même un petit objet est en mesure de mettre en place une grande quantité de mémoire, en empêchant d’autres objets d’être supprimés par le processus automatique de nettoyage de la mémoire.  

### Taille retenue  

Il s’agit de la taille de mémoire qui est libérée une fois que l’objet est supprimé en même temps que les objets dépendants qui ont été rendus injoignables des **racines de nettoyage** de la mémoire \ (racines du CG).  

Les **racines de nettoyage** de la mémoire (racines de catalogue) sont composées de **Handles** créés \ (local ou global \) lors de la création d’une référence à partir du code natif à un objet JavaScript en dehors de V8.  Tous ces handles sont disponibles dans une capture d’instantané **GC roots**de tas sous les descripteurs d'  >  **étendue** et de gestionnaires de racines de **catalogue**  >  **Global**.  La description des descripteurs de cette documentation sans plongée dans les détails de l’implémentation du navigateur risque d’être confus.  Les racines de nettoyage de la mémoire (CG) et les poignées ne sont pas des éléments dont vous devez vous soucier.  

Il existe de nombreuses racines de GC internes, qui ne sont pas pertinentes pour les utilisateurs.  Du point de vue des applications, il existe des types de racines suivants.  

*   Objet Global Window \ (dans chaque IFRAME).  Il existe un champ distance dans les instantanés de tas, qui est le nombre de références de propriété sur le chemin de conservation le plus court à partir de la fenêtre.  
*   L’arborescence DOM du document se compose de tous les nœuds DOM natifs accessibles en parcourant le document.  Tous les nœuds ne peuvent pas avoir de wrappers JS, mais si un nœud possède un wrapper, il est actif lorsque le document est actif.  
*   Parfois, les objets peuvent être conservés par le contexte du débogueur dans le panneau **sources** et la **console** \ (par exemple, après l’évaluation de la console).  Créez des captures d’écran de tas à l’aide d’un panneau de **console** pointé et aucun point d’arrêt actif dans le débogueur dans le panneau **sources** .

>[!TIP]
> Effacez le panneau de la **console** en exécutant `clear()` et désactivez les points d’arrêt dans le panneau **sources** avant de prendre une capture de tas dans le [panneau mémoire][DevtoolsMemoryProblemsHeapSnapshots].

Le graphique de mémoire commence par une racine, qui est éventuellement l' `window` objet du navigateur ou l' `Global` objet d’un module de Node.js.  Vous ne contrôlez pas la façon dont cet objet racine est récupéré par le garbage collector (pgcd).  

:::image type="complex" source="../media/memory-problems-dontcontrol.msft.png" alt-text="Vous ne pouvez pas contrôler la façon dont l’objet racine est récupéré par le garbage collector." lightbox="../media/memory-problems-dontcontrol.msft.png":::
   Vous ne pouvez pas contrôler la façon dont l’objet racine est récupéré par le garbage collector.  
:::image-end:::  

Tout ce qui n’est pas accessible à partir de la racine récupère le nettoyage de la mémoire \ (pgcd \).  

> [!NOTE]
> Les colonnes [taille superficielle](#shallow-size) et [taille retenue](#retained-size) représentent les données en octets.  

## Arborescence conservation d’objets  

Le tas est un réseau d’objets interconnectés.  Dans le monde mathématique, cette structure s’appelle un graphique **graphique** ou de mémoire.  Un graphique est créé à partir de **nœuds** connectés par le biais de **bords**, qui sont des étiquettes données.  

*   Les **nœuds** \ (ou **objets**\) sont étiquetés à l’aide du nom de la fonction **constructeur** utilisée pour les générer.  
*   Les **bords** sont étiquetés à l’aide du nom des **Propriétés**.  

Découvrez [Comment enregistrer un profil à l’aide du profileur de tas][DevtoolsMemoryProblemsHeapSnapshots].  Dans l’illustration ci-dessous, certains des éléments percutants que vous pouvez voir dans l’enregistrement instantané de tas dans le [panneau mémoire][DevtoolsMemoryProblemsHeapSnapshots] incluent la distance: la distance du récupérateur de mémoire (CG \).  Si la plupart des objets du même type se trouvent à la même distance et qu’ils sont à une distance plus importante, cela peut s’avérer utile.  

:::image type="complex" source="../media/memory-problems-root.msft.png" alt-text="Distance par rapport à la racine" lightbox="../media/memory-problems-root.msft.png":::
   Distance par rapport à la racine  
:::image-end:::  

## Dominators  

Les objets Dominator sont composés d’une structure arborescente, car chaque objet a exactement un Dominator.  Un Dominator d’un objet est susceptible de ne pas faire référence directe à un objet qu’il prédomine; c’est-à-dire que l’arborescence de Dominator n’est pas une arborescence fractionnée du graphique.  

Dans l’illustration suivante, l’instruction suivante a la valeur true.  

*   Le nœud 1 prédomine le nœud 2  
*   Le nœud 2 prédomine les nœuds 3, 4 et 6  
*   Le nœud 3 prédomine le nœud 5  
*   Le nœud 5 prédomine du nœud 8  
*   Le nœud 6 prédomine le nœud 7  

:::image type="complex" source="../media/memory-problems-dominatorsspanning.msft.png" alt-text="Structure de l’arborescence Dominator" lightbox="../media/memory-problems-dominatorsspanning.msft.png":::
   Structure de l’arborescence Dominator  
:::image-end:::  

Dans l’illustration suivante, `#3` le nœud est le Dominator `#10` , mais `#7` il existe également dans chaque chemin d’accès simple de l’opération de nettoyage de la mémoire `#10` .  Par conséquent, un objet B est un Dominator d’un objet A, si B existe dans chaque chemin simple de la racine à l’objet A.  

:::image type="complex" source="../media/memory-problems-dominators.msft.gif" alt-text="Illustration Dominator animée" lightbox="../media/memory-problems-dominators.msft.gif":::
   Illustration Dominator animée  
:::image-end:::  

## V8 spécificités  

Lorsque vous configurez la mémoire, il est utile de comprendre pourquoi les instantanés de tas se présentent de manière spécifique.  Cette section décrit certaines rubriques relatives à la mémoire correspondant spécifiquement à la **machine virtuelle JavaScript V8** (VM ou VM).  

### Représentation d’objet JavaScript  

Il existe trois types de primitives:  

*   Numéros \ (par exemple `3.14159...` , \)  
*   Booléens \ ( `true` ou `false` \)  
*   Chaînes \ (par exemple `"Werner Heisenberg"` , \)  

Les primitives ne peuvent pas faire référence à d’autres valeurs et sont toujours des feuilles ou des nœuds de terminaison.  

Les **numéros** peuvent être stockés comme suit:  

*   valeurs entières de 31 bits immédiate appelées **petits entiers** \ (**SMI**s \), ou  
*   objets tas, appelés numéros de **tas**. Les numéros de tas permettent de stocker des valeurs qui ne s’intègrent pas dans le formulaire SMI, par exemple des **doublons**ou lorsqu’une valeur doit être **boxed**, par exemple pour définir des propriétés sur celle-ci.  

Les **chaînes** peuvent être stockées dans l’un ou l’autre des éléments suivants:  

*   le **tas de l’ordinateur virtuel**, ou
*   en externe dans la **mémoire du convertisseur**.  Un **objet wrapper** est créé et utilisé pour accéder à l’espace de stockage externe (par exemple, les sources de script et le contenu reçu à partir du Web sont stockés, au lieu d’être copiés sur le tas de l’ordinateur virtuel).

La mémoire pour les nouveaux objets JavaScript est allouée à partir d’un tas JavaScript dédié \ (ou du **tas du VM**).  Ces objets sont gérés par le récupérateur de mémoire dans la fonction V8 et ne sont donc pas actifs tant qu’il y a au moins une référence forte.  

Tout élément absent du tas JavaScript est appelé **objet natif**.  Les objets natifs, contrairement aux objets tas, ne sont pas gérés par le récupérateur de mémoire V8 tout au long de leur cycle de vie et ne peuvent être accessibles qu’à partir de JavaScript à l’aide de l’objet wrapper JavaScript.  

**Cons chaîne** est un objet composé de paires de chaînes stockées, puis jointes et qui est le résultat de la concaténation.  Le contenu de la **chaîne de type cons** est uniquement nécessaire. Par exemple, quand une sous-chaîne d’une chaîne jointe doit être construite.

Par exemple, si vous concatènent `a` et `b` , vous obtenez une chaîne `(a, b)` qui représente le résultat de la concaténation.  Dans le cas d’une concaténation ultérieure `d` avec ce résultat, vous obtenez une autre **chaîne cons**: `((a, b, d)` .  

L’argument **matrice** est un objet doté de touches numériques. Les **tableaux** sont utilisés de manière extensive dans l’ordinateur virtuel V8 pour le stockage de grandes quantités de données. Les ensembles de paires clé-valeur, comme les dictionnaires, sont sauvegardés par des **matrices**.  

Un objet JavaScript classique est stocké sous la forme d’un seul type de deux types de **tableau** :  

*   propriétés nommées et  
*   éléments numériques  

Dans le cas d’un petit nombre de propriétés, les propriétés sont stockées en interne dans l’objet JavaScript.  

**Map** est un objet qui décrit à la fois le type d’objet et la disposition. Par exemple, les cartes permettent de décrire des hiérarchies d’objets implicites pour un [accès rapide aux propriétés][V8FastProperties].  

### Groupes d’objets  

Chaque groupe d' **objets natifs** est constitué d’objets qui contiennent des références réciproques.  Prenez en considération, par exemple, une sous-arborescence DOM dans laquelle chaque nœud comporte un lien vers le parent relatif, ainsi que des liens vers l’enfant suivant et le frère suivant, formant ainsi un graphique connecté.  

> [!NOTE]
> Les objets natifs ne sont pas représentés dans le tas JavaScript.  L’absence de représentation est la raison pour laquelle les objets natifs ont une taille égale à zéro. Au lieu de cela, les objets wrapper sont créés.  

Chaque objet wrapper dispose d’une référence à l’objet natif correspondant pour rediriger les commandes vers ce dernier.  En retour, un groupe d’objets contient des objets wrapper.  Toutefois, cela ne crée pas de cycle introuvable, car le nettoyage de la mémoire (GC \) est suffisamment intelligent pour libérer les groupes d’objets dont les wrappers ne sont plus référencés. Néanmoins, si vous oubliez de libérer un wrapper unique, il contient le groupe entier et les wrappers associés.  

## Contacter l’équipe Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsMemoryProblemsHeapSnapshots]: ./heap-snapshots.md "Comment enregistrer des instantanés de tas | Documents Microsoft"  

[V8FastProperties]: https://v8.dev/blog/fast-properties "Propriétés rapides dans V8 | V8"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/memory-problems/memory-101) et est créée par [Meggin Kearney][MegginKearney] \ (Technical Writer \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[MegginKearney]: https://developers.google.com/web/resources/contributors/megginkearney
