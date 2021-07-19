---
description: Tout savoir sur la vue 3D et son utilisation.
title: Vue 3D
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: bd91939a19f02a426834a85ef92eca388f8f1eda
ms.sourcegitcommit: 5e218b24fb21fcfa9c82b99f17373fed1ba5a21c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/30/2021
ms.locfileid: "11203969"
---
# <a name="3d-view"></a>Vue 3D  

Utilisez la **Vue 3D** pour déboguer votre application web en naviguant dans le modèle [DOM (Document Object Model)][MDNDocumentObjectModel] ou le contexte d’empilement [d’index-z.][MDNZIndex]  Avec elle, vous pouvez effectuer les tâches suivantes.  

*   [Explorer la page web traduite dans une perspective 3D](#3d-dom)  
*   [Débogage basé sur un contexte d’empilement d’index z](#z-index)  
*   [Accéder aux fonctionnalités de l’outil Layers à partir de la Vue 3D avec des couches composites](#composited-layers)  
*   [Effacer une partie de l’encombrement dans le volet DOM](#changing-your-view) ou le [volet d’index-z](#change-the-scope-of-your-exploration)  
*   [Choisissez le modèle de couleurs pour déboguer au mieux vos problèmes DOM](#dom-color-type) ou [index-z](#z-index-color-type)  

Si vous souhaitez explorer un prototype de projet de Vue 3D et exécuter le code vous-même, accédez à [Echantillon de vue 3D][GithubMicrosoftedgeDevtoolssamples3dview].  

Sur le côté gauche, il y a trois volets que vous pouvez utiliser pour votre expérience de débogage.  

*   Volet [Index-Z.](#z-index)  Parcourez les différents éléments de l’application web avec le contexte d’index-z à l’esprit.  Le volet **Index-Z** est le volet par défaut.  
*   Volet [DOM 3D.](#3d-dom)  Explorez le DOM dans son ensemble avec tous les éléments facilement accessibles.  Pour accéder au volet, choisissez le volet **DOM** à côté du volet **Index-Z.**  
*   Volet [couches composites](#composited-layers).  Ajoutez un autre élément 3D pour créer une expérience plus complète du point de vue des couches.  Pour accéder au volet, choisissez le volet **Couches composites** à côté du volet **DOM.**  
    
Sur le côté droit, la zone de dessin affiche vos sélections à partir de [Index-Z](#z-index), [DOM 3D](#3d-dom)ou [Couches composites](#composited-layers).  

## <a name="navigating-the-canvas"></a>Navigation dans la zone de dessin  

:::image type="complex" source="../media/3d-view-canvas.msft.png" alt-text="Zone de dessin de vue 3D" lightbox="../media/3d-view-canvas.msft.png":::
   Zone de dessin de vue 3D  
:::image-end:::  

### <a name="keyboard-shortcuts"></a>Raccourcis clavier  

*   Faire pivoter le DOM: pour faire pivoter horizontalement, sélectionnez les touches `left-arrow` et `right-arrow`.  Pour faire pivoter verticalement, sélectionnez les touches `up-arrow`et `down-arrow`.  
*   Naviguez dans le DOM : pour parcourir les éléments adjacents, choisissez un élément, puis sélectionnez les touches `up-arrow` et les `down-arrow`.  

### <a name="mouse-controls"></a>Contrôles de souris  

*   Faire pivoter le DOM: choisissez et faites glisser l’espace de zone de dessin.  
*   Faites un mouvement panoramique autour du DOM: ouvrez le menu contextuel \(clic droit\) et faites glisser le DOM dans la direction que vous souhaitez que le DOM se déplace.  
*   Faire un zoom: faites glisser deux doigts sur le pavé tactile ou utilisez la roulette de défilement sur votre souris.  

### <a name="on-screen-controls"></a>Contrôles à l’écran  

:::image type="complex" source="../media/3d-view-controls-small.msft.png" alt-text="Contrôles à l’écran" lightbox="../media/3d-view-controls-small.msft.png":::
   Contrôles à l’écran  
:::image-end:::  

*   Réinitialisez la vue de la zone de dessin à la vue d'origine :  Cliquez sur le bouton **Réinitialiser la caméra**, ou sur le bouton **Réinitialiser les éléments de la vue et recentrer la caméra** (icône d'actualisation latérale).  
*   Actualisez la zone de dessin \(par exemple, si le navigateur a changé ou si vous avez basculé vers une vue d’émulateur d’appareil\) : sélectionnez le bouton **Reprendre une capture instantanée** ou le bouton **Prendre une nouvelle capture instantanée** \(icône d’actualisation\).  

## <a name="z-index"></a>Index-Z  

:::image type="complex" source="../media/3d-view-z-index-view-box.msft.png" alt-text="Vue d’index-Z" lightbox="../media/3d-view-z-index-view-box.msft.png":::
   Vue d’index-Z  
:::image-end:::  

Bien que le volet **Index-Z** dispose de fonctionnalités partagées avec le volet **DOM 3D**, les volets ont toujours des éléments qui sont propres au volet.  

### <a name="highlight-elements-with-stacking-context"></a>Mettre en surbrillation des éléments avec un contexte d’empilement  

Le paramètre **Mettre en surbrillance les éléments avec le contexte d’empilement** vous permet d’activer \(et de désactiver\) les balises index-z pour les éléments sur la zone de dessin.  La case à cocher est choisie par défaut.  

### <a name="change-the-scope-of-your-exploration"></a>Modifier l’étendue de votre exploration  

Le bouton **Afficher tous les éléments** est le moyen le plus rapide d’afficher tous les éléments du DOM après avoir modifié les paramètres sous celui-ci.  

Le bouton **Afficher uniquement avec un contexte d’empilement** supprime les éléments sans contexte d’empilement et aplatit le DOM pour faciliter la navigation.  

Le bouton **Isoler l’élément sélectionné** est essentiellement trois boutons en un.  Il existe deux case à cocher sous le bouton **Isoler l’élément sélectionné**: la case à cocher **Afficher tous les parents** et la case à cocher **Conserver uniquement les parents avec une nouvelle case à cocher de contexte d’empilement**.  

La case à cocher **Afficher tous les parents** est désactivée par défaut.  Pour afficher l’élément et tous les parents sur la zone de dessin, choisissez un élément et choisissez le bouton **Isoler l’élément sélectionné**.  

Pour afficher l’élément et les parents qui ont un nouveau contexte d’empilement sur la zone de dessin, sélectionnez Le paramètre **Conserver uniquement les parents avec un nouveau contexte d’empilement** et choisissez le bouton **Isoler l’élément sélectionné**.  

Pour afficher l’élément que vous avez choisi sur la zone de dessin, désactiver les deux paramètres et sélectionner le bouton **Isoler l’élément sélectionné**.  

En bas du volet **DOM 3D**, recherchez la case à cocher **Masquer les éléments ayant le même ordre de couleur que leur parent**.  Le choix et la désélection de la case à cocher actualisent les éléments en fonction de votre choix.  Si cette option est choisie, les éléments qui partagent l'ordre de couleur sont aplatis par rapport au parent.  

Ces options ont pour but d'alléger un peu l'encombrement que les pages web plus complexes créent dans votre zone de dessin.  

### <a name="z-index-color-type"></a>Type de couleur d’index-Z  

Les différentes visualisations que vous pouvez utiliser pour le DOM dans votre zone de dessin.  Que vous l'utilisiez pour le plaisir ou parce que les visualisations vous aident à mieux visualiser le DOM, les DevTools ont différentes couleurs et une option **Utiliser la couleur d'arrière-plan**.  Le volet **Index-Z** partage les couleurs **Violet à Blanc** et **Couleur d'arrière-plan** avec le volet **DOM 3D**.  Étant donné l'élément visuel supplémentaire que constituent les étiquettes Index-Z, vos commentaires ont conduit à une réduction du nombre d'options de couleur.  La nouvelle simplicité améliore l’expérience de débogage index-z.  Les boutons d’option vous permettent de faire basculer les options et de sélectionner le type de couleur.  Le type de couleur est soit le plus approprié pour votre projet, soit celui qui vous plaît le plus.  

## <a name="3d-dom"></a>DOM 3D  

:::image type="complex" source="../media/3d-view-dom-purple-box.msft.png" alt-text="Vue DOM" lightbox="../media/3d-view-dom-purple-box.msft.png":::
   Vue DOM  
:::image-end:::  

Si vous souhaitez prendre plus d’une vue de débogage générale, plutôt que l’expérience d’index-z, le **DOM 3D** donne une vue d’ensemble du DOM.  Étant donné que le contexte Index-Z est supprimé, le DOM est empilé plus étroitement et plus proprement.  Le volet **DOM 3D** possède des fonctionnalités similaires, mais il existe quelques nuances.  

### <a name="changing-your-view"></a>Modification de votre vue  

Dans le volet **DOM 3D,** le bouton **Isoler l’élément sélectionné** inclut les case à cocher **Inclure les enfants** et **Inclure les parents**.  Les deux case à cocher sont désactivées par défaut.  Cela signifie que si vous choisissez le bouton **Isoler l’élément sélectionné** après avoir choisi un élément, la zone de dessin affiche l’élément choisi, les parents de l’élément et les enfants de l’élément.  Désactiver le paramètre **Inclure les enfants** et sélectionner de nouveau le bouton **Isoler l’élément sélectionné** pour afficher l’élément choisi et les parents de l’élément.  Si vous activez le paramètre **Inclure les enfants** et désactivez le paramètre **Inclure les parents**, puis choisissez le bouton **Isoler l'élément sélectionné**, la zone de dessin affiche l'élément et ses enfants.  Si vous désactivez les deux paramètres et choisissez le bouton **Isoler l’élément sélectionné**, la zone de dessin affiche uniquement l’élément que vous avez choisi précédemment.  

Un curseur sur le volet de contrôle nommé **Niveau d’imbrication pour la page** avec un numéro à côté de celui-ci.  Le nombre indique le nombre de couches pour le document.  Le fait de faire glisser le curseur vers la gauche entraîne l’éloignement des couches les plus à l’extérieur jusqu’à ce qu’un niveau d'imbrication défini sur `1`, qui n'affiche que l'élément le plus éloigné dans le DOM.  Pour supprimer une partie de l’encombrement, faites glisser le curseur.  Cela vous permet de voir de plus près ce qui se passe dans les niveaux inférieurs.  

### <a name="dom-color-type"></a>Type de couleur DOM  

Le volet **DOM 3D** affiche les options suivantes.  

*   Trois couleurs différentes.  
    *   **Carte thermique: Violet à Blanc**  
    *   **Carte thermique: Bleu à Jaune**  
    *   **Carte thermique: arc-en-ciel**  
*   **Utiliser la couleur d’arrière-plan**  
*   **Utiliser la texture d’écran**  
    
L’option **Utiliser la texture d’écran** ajoute du contexte à votre expérience de débogage.  Il affiche directement le contenu de la page web sur les éléments.  

## <a name="composited-layers"></a>Couches composites

:::image type="complex" source="../media/experiments-layers.msft.png" alt-text="Volet Couches composites" lightbox="../media/experiments-layers.msft.png":::
   Volet des **couches composites**
:::image-end:::  

Le volet **Calques composites** ouvre les éléments de l’outil **Couches** sans modifier les contextes.  Vous pouvez toujours accéder aux détails de chacune des couches et avoir les **faire défiler lentement les rectangles** et **Paint**.

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

L'équipe DevTools Microsoft Edge travaille sur l'interface utilisateur et ajoute plus de fonctionnalités à la vue 3D en fonction de vos commentaires.  Envoyez vos commentaires pour améliorer les DevTools Microsoft Edge.  Sélectionnez l’icône **Envoyer des commentaires** dans DevTools ou sélectionnez `Alt`+ `Shift`+`I` sur Windows/Linux ou `Option`+ `Shift`+`I` sur macOS et entrez les commentaires ou les demandes de fonctionnalités dont vous disposez pour devTools.  

<!-- links -->  

[GithubMicrosoftedgeDevtoolssamples3dview]: https://github.com/MicrosoftEdge/DevToolsSamples/tree/master/3DView "Vue 3D de DevTools Microsoft Edge: MicrosoftEdge/DevToolsSamples | GitHub"  

[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Document Object Model (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "index-z | MDN"  
