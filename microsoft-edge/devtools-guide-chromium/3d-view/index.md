---
description: En savoir plus sur l’affichage 3D et son utilisation.
title: Vue 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11203969"
---
# Vue 3D  

Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle DOM][MDNDocumentObjectModel] ou le contexte de pile d' [index z][MDNZIndex] .  Vous pouvez effectuer les tâches suivantes.  

*   [Explorer la page Web traduite en perspective 3D](#3d-dom)  
*   [Déboguer en fonction du contexte de pile z-index](#z-index)  
*   [Accéder à la fonctionnalité outil calques à partir de l’affichage 3D avec des couches composites](#composited-layers)  
*   [Effacement de l’encombrement du volet DOM](#changing-your-view) ou du [volet index z](#change-the-scope-of-your-exploration)  
*   [Choisissez le modèle de couleurs pour déboguer au mieux vos problèmes DOM](#dom-color-type) ou [index z](#z-index-color-type)  

Si vous souhaitez explorer le prototype d’un projet 3D et exécuter le code vous-même, accédez à l' [exemple d’affichage 3D][GithubMicrosoftedgeDevtoolssamples3dview].  

Sur le côté gauche se trouvent trois volets que vous pouvez utiliser pour l’utilisation de débogage.  

*   Volet [index Z](#z-index) .  Parcourez les différents éléments de l’application Web à l’aide du contexte de l’index z.  Le volet **indexation Z** est le volet par défaut.  
*   Volet [DOM 3D](#3d-dom) .  Explorez globalement le DOM tout en étant facilement accessible.  Pour accéder au volet, sélectionnez le volet **DOM** en regard du volet **index Z** .  
*   Volet [couches composites](#composited-layers) .  Ajoutez un autre élément 3D pour créer une connaissance plus complète du point de vue des couches.  Pour accéder au volet, sélectionnez le volet **couches composites** en regard du volet **DOM** .  
    
Sur le côté droit, la zone de dessin affiche vos sélections à partir de l' [index Z](#z-index), du [DOM 3D](#3d-dom)ou des [couches composites](#composited-layers).  

## Navigation dans la zone de dessin  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Toile de vue 3D" lightbox="../media/3d-view-canvas.msft.png":::
   Toile de vue 3D  
:::image-end:::  

### Raccourcis clavier  

*   Faire pivoter le DOM: pour faire pivoter horizontalement, sélectionnez les `left-arrow` `right-arrow` touches et.  Pour faire pivoter à la verticale, sélectionnez les `up-arrow` `down-arrow` touches et.  
*   Naviguez dans le DOM: pour parcourir les éléments adjacents, sélectionnez un élément, puis les `up-arrow` `down-arrow` touches et.  

### Contrôles de souris  

*   Faire pivoter le DOM: sélectionnez et faites glisser autour de l’espace de zone de dessin.  
*   Panoramique du DOM: Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et faites-le glisser dans la direction dans laquelle vous voulez que le DOM se déplace.  
*   Zoom: faites glisser deux doigts sur le pavé tactile ou utilisez le volant de défilement de votre souris.  

### Contrôles à l’écran  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Contrôles à l’écran" lightbox="../media/3d-view-controls-small.msft.png":::
   Contrôles à l’écran  
:::image-end:::  

*   Réinitialisation de l’affichage zone de dessin à l’affichage d’origine: cliquez sur le bouton **Réinitialiser l’appareil photo** , ou sélectionnez le bouton **Réinitialiser les éléments dans afficher et recentrer la caméra** \ (icône d’actualisation latérale \).  
*   Actualiser la zone de dessin \ (par exemple, si le navigateur a changé ou s’il a été basculé vers une vue de l’émulateur de périphériques \): cliquez sur le bouton de nouveau **snapshot** ou sur le bouton **prendre un nouvel** instantané.  

## Index Z  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Affichage index Z" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Affichage index Z  
:::image-end:::  

Lorsque le volet **Z-index** comporte des fonctionnalités partagées avec le volet **DOM 3D** , les volets contiennent toujours des éléments propres au volet.  

### Mettre en évidence des éléments avec un contexte de gerbage  

Les **éléments de mise en surbrillance avec un paramètre de contexte d’empilement** vous permettent d’activer \ (et désactivé) les balises z-index pour les éléments de la zone de dessin.  La case à cocher est activée par défaut.  

### Changer l’étendue de votre exploration  

Le bouton **Afficher tous les éléments** est le moyen le plus rapide d’afficher tous les éléments du DOM après avoir modifié les paramètres situés au-dessous.  

Le bouton **afficher uniquement les éléments avec un contexte de empilement** supprime des éléments sans contexte de empilement et aplatit le DOM pour faciliter la navigation.  

Le bouton **isoler l’élément sélectionné** est essentiellement composé de trois boutons.  Deux cases à cocher s’affichent sous le bouton **isoler l’élément sélectionné** : la case à cocher **Afficher tous les parents** et **conserver uniquement les parents avec la nouvelle case à cocher contexte de superposition** .  

La case à cocher **Afficher tous les parents** est activée par défaut.  Pour afficher l’élément et les parents de la zone de dessin, sélectionnez un élément et choisissez le bouton **isoler l’élément sélectionné** .  

Pour afficher l’élément et les parents ayant un nouveau contexte de gerbage sur la zone de dessin, activez le paramètre **conserver uniquement les parents avec le nouveau contexte d’empilage** et sélectionnez le bouton **isoler l’élément sélectionné** .  

Pour afficher l’élément que vous avez sélectionné dans la zone de dessin, désactivez les paramètres, puis cliquez sur le bouton **isoler l’élément sélectionné** .  

Dans la partie inférieure du volet **DOM 3D** , recherchez les **éléments Hide avec le même ordre de peinture que leur** case à cocher parent.  Le choix et la désélection de la case à cocher permet d’actualiser les éléments en fonction de votre choix.  Si cette propriété est activée, les éléments partageant l’ordre de peinture sont aplatis pour le parent.  

Les options sont conçues pour effacer une partie du courrier pêle-mêle qu’il est difficile de créer dans votre zone de dessin.  

### Type de couleur Z-index  

Les différentes visualisations que vous pouvez utiliser pour le DOM dans votre zone de dessin.  Que vous l’utilisiez avec plaisir ou que les visualisations vous permettent de visualiser le DOM plus facilement, l’DevTools d’colorways et une option d’utilisation de la **couleur d’arrière-plan** .  Le volet **Z-index** partage la couleur **pourpre** avec le blanc et la couleur d' **arrière-plan** avec le volet **DOM 3D** .  À partir de l’élément visuel ajouté de l’étiquette de l’index z, vos commentaires ayant entraîné une réduction du nombre d’options de couleurs.  La nouvelle simplicité améliore l’interface de débogage d’index z.  Les cases d’option vous permettent d’activer ou de désactiver les options et de choisir le type de couleur.  Le type de couleur peut être le plus approprié pour votre projet ou pour un projet qui vous plaît le plus.  

## MODÈLE DOM 3D  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="Affichage DOM" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   Affichage DOM  
:::image-end:::  

Si vous souhaitez utiliser davantage d’une vue de débogage générale plutôt que l’interface z-index, le **DOM 3D** fournit une vue globale du DOM.  Dans la mesure où le contexte de l’index z est supprimé, le DOM est empilé plus en détail.  Le volet **DOM 3D** comporte des fonctionnalités similaires, mais il existe quelques nuancements.  

### Changer d’affichage  

Dans le volet **DOM 3D** , le bouton **isoler l’élément sélectionné** inclut les cases à cocher **enfant** et inclure les **parents** .  Les deux cases à cocher sont activées par défaut.  Cela signifie que si vous choisissez le bouton **isoler l’élément sélectionné** après le choix d’un élément, la zone de dessin affiche l’élément sélectionné, les parents de l’élément et les enfants de l’élément.  Désactivez le paramètre **inclure les enfants** , puis sélectionnez de nouveau le bouton **isoler l’élément sélectionné** pour afficher l’élément choisi et les parents de l’élément.  Si vous activez le paramètre **inclure les enfants** et désactivez le paramètre **inclure les parents** , puis sélectionnez le bouton **isoler l’élément sélectionné** , la zone de dessin affiche l’élément et tout enfant.  Si vous désactivez les deux paramètres et sélectionnez le bouton **isoler l’élément sélectionné** , la zone de dessin affiche uniquement l’élément que vous avez précédemment choisi.  

Curseur sur le volet de contrôles intitulé **niveau d’imbrication de la page** avec un nombre en regard de celui-ci.  Le nombre indique le nombre de calques du document.  Le fait de faire glisser le curseur vers la gauche entraîne l’annulation des couches extérieures jusqu’à ce que vous soyez laissé avec un niveau d’imbrication défini sur `1` , qui n’affiche que l’élément le plus lointain dans le DOM.  Pour supprimer une partie du courrier pêle-mêle, faites glisser le curseur.  Cela vous permet de mieux voir ce qui se passe dans les niveaux inférieurs.  

### Type de couleur DOM  

Le volet **DOM 3D** affiche les options suivantes.  

*   Trois colorways différents.  
    *   **Carte thermique engagements-pourpre à blanc**  
    *   **Carte thermique engagements-bleu à jaune**  
    *   **Carte thermique engagements-arc-en-ciel**  
*   **Utiliser la couleur d’arrière-plan**  
*   **Utiliser la texture d’écran**  
    
L’option **utiliser la texture d’écran** ajoute du contexte à votre environnement de débogage.  Il affiche directement le contenu de la page Web sur les éléments.  

## Calques composites

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Volet couches composites" lightbox="../media/experiments-layers.msft.png":::
   Volet **couches composites**
:::image-end:::  

Le volet **couches composites** permet d’ouvrir les éléments de l’outil **calques** sans changer les contextes.  Vous pouvez toujours accéder aux détails de chacune des couches et utiliser les **rectangles de défilement lente** et **Paint**.

## Contacter l’équipe DevTools MicrosoftEdge  

L’équipe Microsoft Edge devtools travaille sur l’interface utilisateur et ajoute plus de fonctionnalités à l’affichage 3D en fonction de vos commentaires.  Envoyez vos commentaires pour vous aider à améliorer Microsoft Edge DevTools.  Cliquez sur l’icône **Envoyer des commentaires** dans le devtools ou sélectionnez `Alt` + `Shift` + `I` sur Windows/Linux ou `Option` + `Shift` + `I` sur MacOS et entrez les commentaires ou les demandes de fonctionnalité dont vous disposez pour le devtools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Affichage 3D de Microsoft Edge DevTools-MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
