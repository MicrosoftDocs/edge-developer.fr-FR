---
description: Utilisez le panneau éléments pour inspecter les fichiers HTML, CSS, DOM et l’accessibilité de votre page.
title: DevTools-éléments
author: MSEdgeTeam
ms.author: msedgedevrel
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools, éléments, html, CSS, points d’arrêt DOM, événements, accessibilité
ms.custom: seodec18
ms.date: 11/19/2020
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 14052bc40b9f94e628f0b575ede6c1ca8ccf179a
ms.sourcegitcommit: a35a6b5bbc21b7df61d08cbc6b074b5325ad4fef
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/17/2020
ms.locfileid: "11232909"
---
# Éléments

Le panneau **éléments** vous permet d’effectuer les opérations suivantes:

* [Identifier et modifier les éléments dans l’arborescence html](#html-tree-view) de la page active
* [Inspecter et modifier des feuilles CSS](./elements/styles.md) sur la page, y compris des Pseudo-États et des Pseudo-éléments
* Présentation de [la disposition CSS et du style en cascade](./elements/computed.md) sur la page
* [Effectuer le suivi des gestionnaires d’événements malveillants](./elements/events.md) pour pouvoir les déboguer
* [Définir des points d’arrêt de débogage pour les modifications visuelles inattendues](./elements/dom-breakpoints.md) afin de sauter dans le code qui les entraîne
* [Obtenez des informations détaillées sur les polices utilisées sur la page](./elements/fonts.md) et leur emplacement de chargement
* [Afficher votre page à partir du point de vue d’un lecteur d’écran](./elements/accessibility.md) pour vérifier et tester l’accessibilité 
* [Passez en revue les modifications](./elements/changes.md) que vous apportez lors du débogage de l’interface utilisateur de votre page.

## Arborescence HTML

![Panneau éléments de DevTools Microsoft Edge](./media/elements.png)

1. **** `Ctrl+B` Pour rechercher un élément dans l' **arborescence html** , utilisez l’outil sélectionner un élément () et cliquez dessus dans la page.

2. Utilisez l’outil de **mise en surbrillance des éléments** `Ctrl+Shift+L` pour localiser un élément sur la page en pointant dessus dans l' **arborescence html**.

3. Ouvrir l’outil de **sélection de couleurs** ( `Ctrl+K` ) pour afficher une liste des couleurs utilisées dans la page active. Pour plus d’informations, cliquez sur une couleur de la liste, puis sur couleur de nuance, de saturation et de luminosité. Le *Sélecteur de couleur* s’ouvre également lorsque vous cliquez sur le carré de couleur en regard d’une valeur de couleur dans le volet **styles** , ce qui vous permet de modifier la couleur d’un élément de page et d’afficher immédiatement les résultats.

4. Le bouton **arborescence d’accessibilité** ( `Ctrl+Shift+A` ) permet d’ouvrir le volet de l' [arborescence d’accessibilité](./elements/accessibility.md) présentant la structure de votre page telle qu’elle apparaîtra dans une technologie d’assistance, telle que le [narrateur Windows](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) lecteur d’écran.

5. Vous pouvez également **Rechercher** ( `Ctrl+F` ) un élément dans l’arborescence html en recherchant son nom de balise, ses attributs ou son contenu de texte.

### Modification des éléments

Vous pouvez modifier un élément en cliquant dessus avec le bouton droit dans l’arborescence HTML et en sélectionnant **modifier en tant que html** dans le menu contextuel. Le menu contextuel fournit également des options permettant de supprimer, de couper, de copier, de coller, de *définir des Pseudo*-classes CSS (*: actif*, *: Focus*, *: hover* Une autre méthode de modification d’un attribut et/ou sa valeur est de double-cliquer sur celui-ci dans l’arborescence HTML.

![Menu contextuel de l’affichage d’arborescence HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> La modification de l’arborescence HTML n’affecte pas le balisage source sous-jacent. L’actualisation de la page annule les modifications et rend uniquement la mise en page déterminée par la source de la page. Vous pouvez **copier** votre code html modifié dans le presse-papiers en cliquant avec le bouton droit sur l’élément souhaité (ou l' `html` élément global, si vous voulez la page entière) pour ouvrir le menu contextuel. (Les options**couper** et **coller** sont également disponibles).

Dans le volet [styles](./elements/styles.md) , vous pouvez également ajouter/supprimer/modifier des Pseudo-États CSS et des Pseudo-éléments.

## Volets d’outils

Une fois que vous avez sélectionné un élément de page intéressant, vous pouvez utiliser les volets d’outils pour examiner de nouveau ses différentes styles et propriétés d’accessibilité, afficher ses écouteurs d’événements et définir des points d’arrêt de mutation DOM.

![Volets outils du panneau éléments](./media/elements_toolpanes.png)

1. [**Styles**](./elements/styles.md): styles actuellement appliqués organisés par feuille de style

2. [**Calculs**](./elements/computed.md): styles actuellement appliqués organisés par des attributs CSS

3. [**Événements**](./elements/events.md): écouteurs d’événements enregistrés sur l’élément actif et éléments ancêtres

4. [**Points d’arrêt DOM**](./elements/dom-breakpoints.md): points d’arrêt de mutation DOM 

5. [**Polices**](./elements/fonts.md): polices appliquées actuellement pour un élément sélectionné

6. [**Accessibilité**](./elements/accessibility.md): propriétés d’accessibilité

7. [**Modifications**](./elements/changes.md): modifications CSS effectuées lors de la session de diagnostic  

## Raccourcis

| Action               | Raccourci               |
|:---------------------|:-----------------------|
| Panneau éléments       | `Ctrl` + `1`           |
| Mise en surbrillance des éléments | `Ctrl` + `Shift` + `L` |
| Sélectionner un élément       | `Ctrl` + `B`           |
| Sélecteur de couleurs         | `Ctrl` + `K`           |
| Arborescence d’accessibilité   | `Ctrl` + `Shift` + `A` |
