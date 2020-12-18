---
description: Utilisez le volet mémoire pour
title: DevTools-Memory
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, mémoire, tas, CG, nettoyage de la mémoire, taille retenue, Dominators
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 5ad284f8072cc296743299ec9c4fb2037f8fd883
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232900"
---
# Mémoire

Utilisez le volet **mémoire** pour mesurer votre utilisation des ressources système et comparer des instantanés de tas à différents États de l’exécution du code. Avec ce service, vous pouvez:

- [Courbez la consommation de mémoire de votre page en temps réel](#memory-usage-timeline) et prenez des instantanés du tas.
- [Identifier les problèmes de mémoire potentiels](#snapshot-summary) dans votre code, tels que les objets conservés non attachés au DOM
- [Examiner les données d’utilisation](#snapshot-details) de la mémoire par type d’objet, nombre d’instances, taille et références pour vous aider à isoler les problèmes
- [Appliquer des filtres de données de capture instantanée](#filters) pour réduire le bruit lié aux informations non exploitables
- [Identifier le coût de mémoire d’un objet spécifique](#object-references) et les références le laissant actif
- [Différenciez le tas à différentes phases de votre examen](#snapshot-comparison) pour détecter la source de fuites de mémoire et autres problèmes.

![Panneau mémoire de Microsoft Edge DevTools](./media/memory.png)


## ToolBar

1. **Démarrer/arrêter la session de profil (Ctrl + E)**: l’activation du profileur vous permet d’effectuer le suivi de l’utilisation de la mémoire et de prendre des instantanés du tas.
2. **Importer une session de profil (Ctrl + O)**: charger une session de diagnostic de mémoire de devtools enregistrée.
3. **Exporter la session de profil (Ctrl + S)**: enregistrez la session de diagnostic actuelle sur le disque.
4. **Utiliser l’instantané de segment de mémoire (Ctrl + Maj + T)**: enregistrer les attributions de mémoire actuelles pour un moment donné.


## Chronologie de l’utilisation de la mémoire

Les problèmes de mémoire peuvent entraîner des problèmes de performances importants, ce qui amène votre page à devenir de plus en plus réactive et à laggyr au fil du temps.

La première étape de l’analyse de l’utilisation de la mémoire de votre page consiste à [Démarrer une session de profilage](#toolbar) afin de prendre des instantanés du tas lorsque vous reproduisez les étapes de l’augmentation de la mémoire ou d’une fuite de mémoire suspecte.

Lorsque vous démarrez le profileur de mémoire, vous verrez un graphique de mémoire de processus qui vous permet d’observer la plage de travail privée globale (quantité de mémoire consommée par la page) au fil du temps. Le graphique mémoire montre une vue en direct de la mémoire de processus de l’onglet, qui inclut les octets privés, la mémoire native et le tas JavaScript. 

![Chronologie de l’utilisation de la mémoire](./media/memory_timeline.png)

 Le graphique fournit une indication de la tendance de mémoire de la page, qui vous permet de déterminer s’il est approprié de [prendre une capture de segment](#toolbar) de mémoire pour une comparaison ultérieure, par exemple si vous voyez des périodes de rétention de mémoire inattendue.

### Performance. Mark ()

Vous pouvez ajouter des **marques d’utilisateur** personnalisées à la chronologie pour faciliter l’identification des événements clés au cours de la session d’analyse en appelant la [`Performance.mark()`](https://developer.mozilla.org/docs/Web/API/Performance/mark) méthode à partir de votre code ou de la [**console**](./console.md)devtools.

### Console. takeheapSnapshot ()

Parfois, vous devez prendre des instantanés à des moments spécifiques, par exemple, juste avant une mutation importante du DOM. Dans ces cas-là, vous pouvez prendre des instantanés par programme [`Console.takeHeapSnapshot()`](./console/console-api.md#taking-heap-snapshots) .

## Résumé du snapshot

Le suivi d' [une capture](#toolbar) d’écran génère une vignette de synthèse qui indique la taille du tas JavaScript au moment où la capture instantané a été effectuée, ainsi que le nombre d’objets attribués et une capture d’écran de la page. Vous pouvez continuer à prendre des instantanés à tout moment pendant que vous effectuez une analyse par le biais du scénario utilisateur. Les instantanés génèrent des vignettes supplémentaires, dont chacune indique la différence de mémoire JavaScript par rapport à l’instantané précédent.

![Instantané de tas](./media/memory_snapshot.png)

Cliquez sur les valeurs de la vignette récapitulative pour basculer vers le volet présentant les [Détails des données de capture instantanée](#snapshot-details). Des [problèmes de mémoire potentiels sont signalés](#snapshot-details) par une icône d’information bleue («i»).

## Détails de la photo

Les données du volet *instantané* indiquent les objets créés par votre page, ainsi que les mémoires allouées par les infrastructures JavaScript que vous pouvez consommer.

![Tableau détails de l’instantané](./media/memory_details.png)

Les trois onglets représentent différents affichages des données:

#### Types

Affiche le nombre d’instances et la taille totale des objets sur le tas, regroupés par type d’objet. Par défaut, ces valeurs sont triées par nombre d’instances.

Lorsque vous sélectionnez un objet dans le volet *types* du haut, la table [références d’objet](#object-references) dans le volet inférieur répertorie tous les objets qui pointent vers cet objet.

#### Digne

Affiche une vue hiérarchique des références enfant pour décrire le mode de mise en place des objets associés à l’objet global, ce qui les empêche d’être nettoyés de la mémoire.

Par défaut, les nœuds enfants sont triés en fonction de la taille de la colonne taille retenue, le plus grand en haut.

#### Dominators

Affiche une liste des objets sur le tas qui disposent de références exclusives à d’autres objets. Les Dominators sont triés par taille retenue pour indiquer que les objets consommant la plus grande quantité de mémoire est potentiellement plus facile à libérer.

Voici comment interpréter les colonnes des vues *types, racines* et *Dominators* :

Colonne | Description
:------------ | :-------------
Identificateur (s) | Nom identifiant le mieux l’objet. Par exemple, pour les éléments HTML, les détails de l’instantané indiquent la valeur de l’attribut ID, le cas échéant.
Type | Type d’objet (par exemple, *HTMLDivElement*).
Taille | Taille de l’objet, sans inclure la taille des objets référencés.
Taille retenue | Taille d’objet plus la taille de tous les objets enfants qui n’ont pas d’autres parents. Pour des raisons pratiques, il s’agit de la quantité de mémoire conservée par l’objet, de sorte que si vous supprimez l’objet vous obtenez la quantité de mémoire spécifiée.
Nombre | Nombre d’instances d’objets. Cette valeur s’affiche uniquement dans l’affichage types.

Lorsque vous sélectionnez un objet dans le volet de *Dominators* supérieur, le tableau [références d’objet](#object-references) dans le volet inférieur répertorie tous les objets qui pointent vers cet objet.

### Filtré

Vous pouvez ensuite ajuster les données du tableau de la manière suivante:

![Filtrer les composants intégrés et les ID d’objet](./media/memory_filter.png)

1. **Filtre identificateur**: filtrez les données en recherchant un identificateur d’objet particulier
2. **Regroupement par Dominator**: seuls les objets dotés de références *exclusives* à d’autres objets apparaissent dans l’affichage de niveau supérieur d’objets (il s’agit de l’affichage par défaut dans l’onglet *Dominators* ).
3. **Filtre des composants intégrés/identifiants**: par défaut, les [objets intégrés JavaScript](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects) sont inclus dans la liste. Les ID d’objet de liste peuvent être utiles s’il existe plusieurs objets anonymes qui doivent être différenciés.

Les vues *types, racines* et *Dominators* ont chacune leur propre filtre, de sorte que le filtre n’est pas conservé quand vous basculez vers un autre mode d’affichage.

### Références d’objets

Dans les vues [**types**](#types) et [**Dominators**](#dominators) , le volet inférieur contient une liste **références d’objets** qui affiche des références partagées. Lorsque vous sélectionnez un objet dans le volet supérieur, cette liste affiche tous les objets qui pointent vers cet objet, en d’autres termes, les objets qui gardent l’objet sélectionné actif.

Les références circulaires s’affichent à l’aide d’un astérisque (*) et d’une info-bulle d’information et ne peuvent pas être développés. Sinon, ils vous empêchent de remonter l’arborescence de référence et d’identifier les objets qui conservent de la mémoire.

Pour identifier rapidement les objets équivalents, cochez l’option filtre d' [*ID d’objet d’affichage*](#filters) pour afficher les ID d’objet en regard de noms d’objets dans la colonne *identificateur (s)* . Les objets portant le même ID sont des références partagées.

### Comparaison des snapshots

Cliquez sur un [onglet de comparaison de capture instantanée](#snapshot-details) ou sur le lien de comparaison dans la [vignette de synthèse de capture instantanée](#snapshot-summary)  pour afficher une différence d’information entre les deux instantanés. Dans le volet comparaison, les affichages *Dominators, types* et *racines* fournissent les mêmes [*informations d’instantané*](#snapshot-details) que celles disponibles pour une seule image, avec ces valeurs supplémentaires:

Colonne | Description
:------------ | :-------------
Différences de taille. | Différence entre la taille de l’objet dans l’instantané actuel et sa taille dans l’instantané précédent, sans inclure la taille des objets référencés.
Différence de taille retenue | Différence entre la taille retenue de l’objet dans l’instantané actuel et sa taille de conservation dans l’instantané précédent. La taille retenue inclut la taille de l’objet plus la taille de tous ses objets enfants qui n’ont pas d’autres parents. Pour des raisons pratiques, la taille retenue correspond à la quantité de mémoire conservée par l’objet, de sorte que si vous supprimez l’objet vous obtenez la quantité de mémoire spécifiée.

Vous pouvez utiliser la liste déroulante **scope** pour filtrer les informations différentielles entre les instantanés:

![Filtre d’étendue pour les comparis de capture instantanée](./media/memory_comparison_scope_filter.png)

- <strong>Les objets situés à l’origine de l’instantané n ° instantané <number></strong> indiquent la différence entre les objets ajoutés au tas et supprimés du tas de l’instantané de référence à l’instantané précédent. Par exemple, si le résumé de l’instantané affiche <em> + 205/-195 </em> dans le nombre d’objets, ce filtre vous montrera les dix objets qui ont été ajoutés mais ne sont pas supprimés.

- <strong>Les objets ajoutés entre instantané # <number> et # <number></strong> : affiche tous les objets ajoutés au tas à partir de l’instantané précédent.

- <strong>Tous les objets dans l’instantané # <number></strong> : affiche tous les objets sur le tas (en d’autres termes, un <em> affichage non filtré </em> ).

Par défaut, le filtre *afficher les références non concordantes* est appliqué à l’affichage comparaison pour indiquer des références d’objets qui ne correspondent pas au filtre d’étendue actuel. Vous pouvez désactiver cette option dans le menu déroulant:

![Filtre des références non concordantes pour les comparaisons de capture instantanée](./media/memory_comparison_matching_filter.png)


## Raccourcis

 Action | Raccourci
:------------ | :-------------
Démarrer/arrêter la session de profilage  | `Ctrl` + `E`
Importer une session de profil | `Ctrl` + `O`
Exporter la session de profilage | `Ctrl` + `S`
Instantané de tas | `Ctrl` + `Shift` + `T`

## Problèmes connus

### Une erreur s’est produite lors du démarrage de la session de profilage

Si vous voyez ce message d’erreur: **une erreur s’est produite lors du démarrage de la session de profilage** dans l’outil mémoire, procédez comme suit pour contourner le problème.

1. Appuyez sur `Windows Key`  +  `R` .

2. Dans la boîte de dialogue Exécuter, entrez **services. msc**.
![problèmes connus-1](./media/known_issues_1.PNG)

3. Recherchez le **service collecteur standard de Diagnostics Microsoft (R)** et cliquez dessus avec le bouton droit.
![problèmes connus-2](./media/known_issues_2.PNG)

4. Redémarrez le **service de collecteur standard de Diagnostics Microsoft (R)**.
![problèmes connus-3](./media/known_issues_3.PNG)

5. Fermez les outils de développement Microsoft Edge et l’onglet. Ouvrez un nouvel onglet, accédez à votre page, puis appuyez sur `F12` .

6. Vous devriez maintenant être en mesure de commencer le profilage. 
![problèmes connus-4](./media/known_issues_4-memory.PNG)

Vous rencontrez encore des problèmes? Envoyez-nous vos commentaires à l’aide de l’icône d' **envoi de commentaires** ! 

![problèmes connus-5](./media/known_issues_5.PNG)
