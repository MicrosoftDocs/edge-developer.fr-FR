---
description: En savoir plus sur l’affichage 3D et son utilisation.
title: Vue 3D
author: erdraud
ms.author: erdraud
ms.date: 11/27/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: f2ae80426da71797d4bee4060d33965f04047e19
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2020
ms.locfileid: "10565007"
---
# Vue 3D

Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) DOM ou le contexte de pile d' [index z](https://developer.mozilla.org/en-US/docs/Web/CSS/z-index) . Vous pouvez: 

- [Découvrir la page Web traduite en 3D perspevtive](#3d-dom)
- [Déboguer en fonction du contexte de pile z-index](#z-index)
- [Effacement de l’encombrement du volet DOM](#changing-your-view) ou du [volet index z](#change-the-scope-of-your-exploration)
- [Choisissez le modèle de couleurs pour déboguer au mieux vos problèmes DOM](#dom-color-type) ou [index z](#z-index-color-type)

Deux volets peuvent être utilisés pour l’utilisation de débogage.

1. **Index Z** Parcourez les différents éléments de l’application Web à l’aide du contexte de l’index z. Il s’agit du volet par défaut.
2. **modèle DOM 3D** Explorez le DOM comme un ensemble de tous les éléments à portée de main. Pour accéder à ce volet, cliquez sur le volet «DOM» en regard du volet «Z-index».

![toile de vue 3D](./media/canvas.png)

## Navigation dans la zone de dessin

### Raccourcis clavier
- Faire pivoter le DOM: utilisez les touches de direction vers la gauche et la droite pour faire pivoter l’axe horizontal, puis appuyez sur les flèches vers le haut et le bas pour faire pivoter verticalement.
- Naviguer dans le DOM: si un élément est sélectionné, vous pouvez utiliser les flèches vers le haut et le bas pour parcourir les éléments adjacents

### Contrôles de souris
- Faire pivoter le DOM: cliquez et faites glisser autour de l’espace de zone de dessin.
- Panoramique du DOM: cliquez avec le bouton droit et faites glisser dans la direction dans laquelle vous voulez que le DOM se déplace.
- Zoom: faites glisser deux doigts sur le pavé tactile ou utilisez le volant de défilement de votre souris.

![contrôles à l’écran](./media/controls-small.png)
### Contrôles à l’écran
- Réinitialisation de l’affichage de zone de dessin à l’affichage d’origine: cliquez sur le bouton «Réinitialiser la caméra» ou cliquez sur l’icône ressemblant à un bouton d’actualisation latérale et ayant «réinitialiser les éléments dans l’affichage et recentrer la caméra».
- Actualiser la zone de dessin (par exemple, si le navigateur a changé ou s’il a été basculé vers un affichage émulateur d’appareil): cliquez sur le bouton indiquant «reprenez l’instantané» ou cliquez sur le bouton qui ressemble à une icône d’actualisation et dont le texte de pointage comporte une nouvelle capture d’écran.

![Affichage index Z](./media/z-index-view-box.png)

## Index Z

Lorsque le volet de l’index Z comporte des fonctionnalités partagées avec le volet DOM, celles-ci possèdent toujours des éléments uniques dans le volet.

### Mettre en évidence des éléments avec un contexte de gerbage

Ce paramètre vous permet d’activer ou de désactiver les balises d’index z pour les éléments de la zone de dessin. La case à cocher est activée par défaut.

### Changer l’étendue de votre exploration

Le bouton **Afficher tous les éléments** est le moyen le plus rapide d’afficher tous les éléments du DOM après avoir modifié les paramètres ci-dessous.

**Afficher uniquement les éléments avec le contexte de gerbage** supprime des éléments sans contexte de empilement et aplatit le DOM pour faciliter la navigation.

Le filtre d' **élément d’isolation sélectionné** est essentiellement trois boutons en un. Il existe deux cases à cocher sous ce bouton: l’un est «afficher tout le parent» et «conserver uniquement les parents avec le nouveau contexte de gerbage». 

La case à cocher «Afficher tout le parent» est activée par défaut. Si vous sélectionnez un élément dans le volet zone de dessin, puis cliquez sur **isoler l’élément sélectionné**, la zone de dessin n’affiche que l’élément et ses parents.

Si vous sélectionnez «conserver uniquement les parents avec un nouveau contexte de gerbage», puis cliquez sur **isoler l’élément sélectionné**, la zone de dessin n’affiche que l’élément et les parents ayant un nouveau contexte de gerbage.

Si vous désactivez les deux cases à cocher et cliquez sur **isoler l’élément sélectionné**, l’élément Canvas affichera uniquement l’élément que vous avez choisi au départ.

Dans la partie inférieure du panneau contrôles se trouvent les **éléments Hide avec le même ordre de peinture que leur** bouton bascule parent. La sélection et la désactivation de la case à cocher entraînent le rechargement des éléments en fonction de votre sélection. Si cette option est sélectionnée, les éléments qui partagent l’ordre de peinture seront aplatis pour le parent.

Ces options sont conçues pour effacer une partie du courrier pêle-mêle qu’il est difficile de créer dans votre zone de dessin.

### Type de couleur Z-index

Voici les différentes visualisations que vous pouvez utiliser pour le DOM dans votre zone de dessin. Que vous l’utilisiez avec plaisir ou qu’il vous aide à visualiser davantage le DOM, nous avons trois différences colorways ainsi qu’un paramètre «couleur d’arrière-plan». Les cases d’option vous permettent d’activer ou de désactiver les options et de choisir le type de couleur le plus approprié pour votre projet (ou qui vous plaît le plus).

![Affichage DOM](./media/dom-purple-box.png)

## MODÈLE DOM 3D

Si vous souhaitez utiliser davantage d’une vue de débogage générale plutôt que l’interface z-index, le DOM 3D fournit une vue globale du DOM. Dans la mesure où le contexte de l’index z est supprimé, le DOM est empilé plus en détail. Ce volet est doté de fonctionnalités similaires, mais il existe quelques nuancements.

### Changer d’affichage

Dans le volet **DOM 3D** , le filtre d' **élément d’isolation sélectionné** a «include Children» et «include parents». Par défaut, les deux cases à cocher sont activées, ce qui signifie que le fait de cliquer sur le bouton **isoler l’élément sélectionné** après avoir sélectionné un élément dans la zone de dessin affiche l’élément choisi, les parents de l’élément et les enfants de l’élément. Si vous désélectionnez la case à cocher «inclure les enfants» et que vous cliquez de nouveau sur le bouton **isoler l’élément sélectionné** , l’élément sélectionné et les parents de l’élément s’afficheront. Si vous activez la case à cocher «inclure les enfants» et désélectionnez la case à cocher «inclure les parents» avant de cliquer sur **isoler l’élément sélectionné**, l’élément de la zone de dessin s’affiche alors avec ses enfants. Si vous désactivez les deux cases à cocher et cliquez sur **isoler l’élément sélectionné**, la zone de dessin n’affiche que l’élément que vous avez sélectionné précédemment.

Vous remarquerez qu’un curseur apparaît dans le volet de contrôles intitulé **niveau d’imbrication** avec un nombre en regard de celui-ci. Le nombre indique le nombre de calques dans le document. Le fait de faire glisser le curseur vers la gauche entraîne le retrait des couches les plus extérieures jusqu’à ce que vous soyez à l’intérieur d’un niveau d’imbrication de 1, en affichant uniquement l’élément le plus lointain dans le DOM. Cela vous permet de supprimer tout le courrier pêle-mêle si vous essayez de consulter de plus près ce qui se passe dans les niveaux inférieurs.

### Type de couleur DOM

Vous remarquerez que, en plus du *pourpre sur le blanc*, du *bleu au jaune*, de l’arc-en- *ciel*et de l’utilisation des options de *couleur d’arrière-plan* , la texture d’écran est *utilisée*. La texture d’écran ajoute du contexte à votre environnement de débogage en affichant le contenu de la page Web directement sur les éléments. C’est toujours en cours de travail, dans la mesure où certains sites Web présentent un temps plus difficile pour le rendu de la texture d’écran en 3D. 

## Étapes suivantes

Nous travaillons sur l’interface utilisateur et nous ajoutons davantage de fonctionnalités à la vue 3D en fonction de la demande de la part des utilisateurs comme vous. Envoyez-nous vos commentaires pour que nous puissions continuer à améliorer Microsoft Edge DevTools pour vous. Il suffit de cliquer sur l’icône de commentaire dans le devtools ou `Alt`  +  `Shift`  +  `I` d’appuyer sur Windows ( `Option`  +  `Shift`  +  `I` sur Mac) et d’entrer des commentaires ou des demandes de fonctionnalités pour le devtools.