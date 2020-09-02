---
description: En savoir plus sur l’affichage 3D et son utilisation.
title: Vue 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: ba1125654c46be6ef4da99efc9ba027ba5e40672
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986079"
---
# Vue 3D  

Utilisez la **vue 3D** pour déboguer votre application Web en naviguant dans le [modèle DOM][MDNDocumentObjectModel] ou le contexte de pile d' [index z][MDNZIndex] .  Vous pouvez également effectuer les tâches suivantes.  

*   [Explorer la page Web traduite en perspective 3D](#3d-dom)  
*   [Déboguer en fonction du contexte de pile z-index](#z-index)  
*   [Effacement de l’encombrement du volet DOM](#changing-your-view) ou du [volet index z](#change-the-scope-of-your-exploration)  
*   [Choisissez le modèle de couleurs pour déboguer au mieux vos problèmes DOM](#dom-color-type) ou [index z](#z-index-color-type)  

Si vous souhaitez explorer le prototype d’un projet 3D et exécuter le code vous-même, voir [exemple d’affichage 3D][GithubMicrosoftedgeDevtoolssamples3dview].   

Sur le côté gauche, il existe deux volets que vous pouvez utiliser pour l’utilisation de débogage.  

1.  Volet [index Z](#z-index) .  Parcourez les différents éléments de l’application Web à l’aide du contexte de l’index z.  Le volet **indexation Z** est le volet par défaut.  
1.  Volet [DOM 3D](#3d-dom) .  Explorez le DOM comme un ensemble de tous les éléments à portée de main.  Pour accéder au volet, sélectionnez dans le volet **DOM** en regard du volet **index Z** .  
    
Sur le côté droit, la zone de dessin affiche les sélections de l' [index Z](#z-index) ou du [DOM 3D](#3d-dom).  

## Navigation dans la zone de dessin  

:::image type="complex" source="../media/canvas.png" alt-text="Toile de vue 3D" lightbox="../media/canvas.png":::
   Toile de vue 3D  
:::image-end:::  

### Raccourcis clavier  

*   Faire pivoter le DOM: pour faire pivoter horizontalement, appuyez sur les `left-arrow` `right-arrow` touches et.  Pour faire pivoter verticalement, appuyez sur les `up-arrow` `down-arrow` touches et.  
*   Naviguez dans le DOM: pour parcourir les éléments adjacents, sélectionnez un élément et appuyez sur les `up-arrow` `down-arrow` touches et.  

### Contrôles de souris  

*   Faire pivoter le DOM: sélectionnez et faites glisser autour de l’espace de zone de dessin.  
*   Panoramique du DOM: Ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \) et faites-le glisser dans la direction dans laquelle vous voulez que le DOM se déplace.  
*   Zoom: faites glisser deux doigts sur le pavé tactile ou utilisez le volant de défilement de votre souris.  

### Contrôles à l’écran  

:::image type="complex" source="../media/controls-small.png" alt-text="Contrôles à l’écran" lightbox="../media/controls-small.png":::
   Contrôles à l’écran  
:::image-end:::  

*   Réinitialisez le mode zone de dessin à l’affichage d’origine: cliquez sur le bouton **Réinitialiser l’appareil photo** , ou sélectionnez le bouton **Réinitialiser les éléments dans afficher et recentrer la caméra** \ (icône d’actualisation latérale \).  
*   Actualiser la zone de dessin \ (par exemple, si le navigateur a changé ou s’il a été basculé vers une vue de l’émulateur de périphériques \): **sélectionnez le bouton** répondre aux **nouvelles** .  

## Index Z  

:::image type="complex" source="../media/z-index-view-box.png" alt-text="Affichage index Z" lightbox="../media/z-index-view-box.png":::
   Affichage index Z  
:::image-end:::  

Lorsque le volet **Z-index** comporte des fonctionnalités partagées avec le volet **DOM 3D** , les volets contiennent toujours des éléments propres au volet.  

### Mettre en évidence des éléments avec un contexte de gerbage  

Les **éléments de mise en surbrillance avec un paramètre de contexte d’empilement** vous permettent d’activer \ (et désactivé) les balises z-index pour les éléments de la zone de dessin.  La case à cocher est activée par défaut.  

### Changer l’étendue de votre exploration  

Le bouton **Afficher tous les éléments** est le moyen le plus rapide d’afficher tous les éléments du DOM après avoir modifié les paramètres ci-dessous.  

Le bouton **afficher uniquement les éléments avec un contexte de empilement** supprime des éléments sans contexte de empilement et aplatit le DOM pour faciliter la navigation.  

Le bouton **isoler l’élément sélectionné** est essentiellement composé de trois boutons.  Deux cases à cocher s’affichent sous le bouton **isoler l’élément sélectionné** : la case à cocher **Afficher tous les parents** et **conserver uniquement les parents avec la nouvelle case à cocher contexte de superposition** .  

La case à cocher **Afficher tous les parents** est activée par défaut.  Si vous sélectionnez un élément dans le volet zone de dessin et sélectionnez **isoler l’élément sélectionné** , la zone de dessin affiche uniquement les éléments et les parents.  

Si vous activez la case à cocher **conserver uniquement les parents avec la nouvelle option contexte d’empilement** , puis sélectionnez l’option **isoler l’élément sélectionné** , la zone de dessin affiche uniquement l’élément et les parents ayant un nouveau contexte d’empilage.  

Si vous désactivez les deux cases à cocher et sélectionnez **isoler l’élément sélectionné** , la zone de dessin affiche uniquement l’élément que vous avez choisi au départ.  

Dans la partie inférieure du panneau **DOM 3D** , recherchez les **éléments Hide avec le même ordre de peinture que leur** case à cocher parent.  La sélection et la désactivation de la case à cocher permet d’actualiser les éléments en fonction de votre sélection.  Si cette option est sélectionnée, les éléments qui partagent l’ordre de peinture sont aplatis pour le parent.  

Les options sont conçues pour effacer une partie du courrier pêle-mêle qu’il est difficile de créer dans votre zone de dessin.  

### Type de couleur Z-index  

Les différentes visualisations que vous pouvez utiliser pour le DOM dans votre zone de dessin.  Que vous l’utilisiez pour plaisir ou que les visualisations vous aident à visualiser le DOM plus facilement, le DevTools possède trois colorways différents, ainsi qu’un paramètre de **couleur d’arrière-plan** .  Les cases d’option vous permettent d’activer ou de désactiver les options et de choisir le type de couleur le plus approprié pour votre projet.  

## MODÈLE DOM 3D  

:::image type="complex" source="../media/dom-purple-box.png" alt-text="Affichage DOM" lightbox="../media/dom-purple-box.png":::
   Affichage DOM  
:::image-end:::  

Si vous souhaitez utiliser davantage d’une vue de débogage générale plutôt que l’interface z-index, le **DOM 3D** fournit une vue globale du DOM.  Dans la mesure où le contexte de l’index z est supprimé, le DOM est empilé plus en détail.  Le volet **DOM 3D** comporte des fonctionnalités similaires, mais il existe quelques nuancements.  

### Changer d’affichage  

Dans le volet **DOM 3D** , le bouton **isoler l’élément sélectionné** inclut les cases à cocher **enfant** et inclure les **parents** .  Par défaut, les deux cases à cocher sont activées, ce qui signifie que la sélection d’un élément dans la zone de dessin permet d’afficher l’élément que vous **avez** choisi, les parents de l’élément et les enfants de l’élément.  Si vous désactivez la case à cocher **inclure les enfants** et que vous sélectionnez de nouveau le bouton **isoler l’élément sélectionné** , l’élément sélectionné et les parents de l’élément doivent s’afficher.  Si vous activez la case à cocher **inclure les enfants** et désélectionnez la case à cocher **inclure les parents** avant de sélectionner l’option **isoler l’élément sélectionné** , la zone de dessin affiche l’élément et tout enfant.  Si vous désactivez les deux cases à cocher et sélectionnez **isoler l’élément sélectionné** , la zone de dessin affiche uniquement l’élément que vous avez sélectionné précédemment.  

Curseur sur le volet de contrôles intitulé niveau d' **imbrication de la page** avec un nombre en regard de celui-ci.  Le nombre indique le nombre de calques du document.  Faire glisser le curseur vers la gauche entraîne l’annulation des couches extérieures jusqu’à ce que vous soyez à gauche avec un niveau d’imbrication défini sur 1, ce qui n’affiche que l’élément le plus lointain dans le DOM.  Le fait de faire glisser le curseur vous permet de supprimer tout le contenu encombrant si vous essayez de consulter de plus près ce qui se passe dans les niveaux inférieurs.  

### Type de couleur DOM  

Outre le **carte thermique engagements-Purple en blanc**, **carte thermique engagements-bleu à jaune**, **carte thermique engagements-arc-** en-ciel et utiliser les cases d’option **couleur d’arrière-plan** , vous pouvez **utiliser la texture d’écran**.  La texture d’écran ajoute du contexte à votre environnement de débogage en affichant le contenu de la page Web directement sur les éléments.  Dans le volet **DOM 3D** , le paramètre de  **type de couleur** reste en cours de travail, car certains sites Web présentent un temps plus difficile pour le rendu de la texture d’écran en 3D.  

## Contacter l’équipe Microsoft Edge DevTools

L’équipe Microsoft Edge devtools travaille sur l’interface utilisateur et ajoute plus de fonctionnalités à l’affichage 3D en fonction de la demande de la part des utilisateurs comme vous.  Envoyez-nous vos commentaires pour vous aider à améliorer Microsoft Edge DevTools.  Il suffit de sélectionner l’icône de commentaires dans le devtools ou d’appuyer sur `Alt` + `Shift` + `I` \ (Windows \) ou d’appuyer sur `Option` + `Shift` + `I` \ (MacOS \) et d’entrer des commentaires ou des demandes de fonctionnalités pour le devtools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Affichage 3D de Microsoft Edge DevTools-MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "DOM (Document Object Model) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index z | MDN"  
