---
description: Découvrez comment utiliser Microsoft Edge DevTools pour afficher et modifier la feuille de style en cascade d’une page.
title: Prise en main de l’affichage et de la modification de réplication Commerce Server
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: f055606ff6140652341627097e7fe7b270dc929c
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993064"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# Prise en main de l’affichage et de la modification de réplication Commerce Server  

Suivez ces didacticiels interactifs pour découvrir les notions de base de l’affichage et de la modification de la CSS d’une page à l’aide de Microsoft Edge DevTools.  

## Exemples de CSS ouverts  

1.  Appuyez `Control` sur \ (Windows \) ou `Command` \ (MacOS \) et sélectionnez **exemples CSS** à ouvrir dans une nouvelle fenêtre.  
    
    [Exemples CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Si vous voulez [ancrer votre fenêtre devtools][DevToolsCustomizePlacement] à droite de votre fenêtre d’affichage \ (affichée dans la figure ci-dessous), sélectionnez **personnaliser et contrôler devtools** `...` .  Dans le menu déroulant **personnaliser et contrôler devtools** , dans la section **ancrer** , sélectionnez **ancrer à droite**.  
    
## Affichage de la feuille de style en cascade pour un élément  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Positionnez le pointeur sur le `Inspect Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
    1.  Dans DevTools, dans le panneau **éléments** , dans l’onglet **arborescence DOM** , l' `Inspect Me!` élément est mis en surbrillance.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="L’élément inspecté est surligné dans l’arborescence DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           Figure 1: l’élément inspecté est surligné dans l' **arborescence DOM**  
        :::image-end:::  
        
    1.  Dans l' `Inspect Me!` élément, recherchez la valeur de l' `data-message` attribut et copiez-la.  
1.  Dans la page, dans la zone **valeur de `data-message` :** , entrez la valeur.  
1.  Positionnez le pointeur sur le `Inspect Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
    1.  Dans DevTools, dans le panneau **éléments** , sélectionnez l’onglet **styles** .  
    1.  Dans l’onglet **styles** , l' `Inspect Me!` élément est mis en surbrillance.  
    1.  Dans l' `Inspect Me!` élément, recherchez la `aloha` règle de classe.  
        
        > [!NOTE]
        > Cette règle s’affiche, car elle est appliquée à l' `Inspect Me!` élément.  
        
    1.  Dans la `aloha` classe, recherchez la valeur du `padding` style et copiez-la.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Les classes CSS appliquées à l’élément inspecté sont mises en surbrillance dans l’onglet styles" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Figure 2: les classes CSS qui sont appliquées à l’élément sélectionné, par exemple `aloha` , sont affichées dans l’onglet **styles**  
        :::image-end:::  
        
1.  Dans la page, dans la zone **valeur de `padding` :** , entrez la valeur.  

## Ajouter une déclaration CSS à un élément  

Utilisez l’onglet **styles** lorsque vous voulez modifier ou ajouter des déclarations CSS à un élément.  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Positionnez le pointeur sur le `Add A Background Color To Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
1.  Sélectionnez `element.style` près du haut de l’onglet **styles** .  
1.  Tapez `background-color` et appuyez sur `Enter` .  
1.  Tapez `honeydew` et appuyez sur `Enter` .  Dans l' **arborescence DOM** , vous devez voir qu’une déclaration de style intraligne a été appliquée à l’élément.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Ajout d’une déclaration CSS à l’élément à l’aide de l’onglet styles" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       Figure 3: la `background-color:honeydew` déclaration a été appliquée à l’élément à l’aide `element.style` de la section de l’onglet **styles** .  
    :::image-end:::  
    
## Ajouter une classe CSS à un élément  

Utilisez l’onglet **styles** pour voir l’apparence d’un élément lorsqu’une classe CSS est appliquée à un élément ou a été supprimée.  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Positionnez le pointeur sur le `Add A Class To Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
1.  Sélectionnez **. CLS**.  DevTools révèle une zone de texte dans laquelle vous pouvez ajouter des classes à l’élément sélectionné.  
1.  Entrez `color_me` dans la zone de texte **Ajouter une nouvelle classe** , puis appuyez sur `Enter` .  Une case à cocher s’affiche sous la zone de texte **Ajouter une nouvelle classe** , dans laquelle vous pouvez activer ou désactiver la classe.  Si d' `Add A Class To Me!` autres classes sont appliquées à l’élément, vous pouvez également basculer chacun d’eux ici.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Application de la classe color_me à l’élément" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       Figure 4: la `color_me` classe a été appliquée à l’élément à l’aide de la section **. CLS** de l’onglet **styles**  
    :::image-end:::  
    
## Ajouter un PseudoState à une classe  

Utilisez l’onglet **styles** pour appliquer de manière définitive une PseudoState CSS à un élément.  DevTools prend en charge `:active` , `:focus` , `:hover` et `:visited` .  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Placez le pointeur sur le `Hover Over Me!` texte.  La couleur d’arrière-plan change.  
1.  Positionnez le pointeur sur le `Hover Over Me!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
1.  Dans l’onglet **styles** , sélectionnez **: HOV**.  
1.  Cochez la case **sensitif** .  La couleur d’arrière-plan change comme auparavant, même si vous n’avez pas réellement pointé sur l’élément.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Activation de la fonction Hover PseudoState sur un élément" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Figure 5: activer/désactiver le `:hover` PseudoState sur un élément  
    :::image-end:::  
    
## Modifier les dimensions d’un élément  

Pour modifier la largeur, la hauteur, le remplissage, la marge ou la taille de la bordure d’un élément, utilisez le diagramme interactif du **modèle de zone** dans l’onglet **styles** .  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Positionnez le pointeur sur le `Change My Margin!` texte, ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
1.  Dans le diagramme de **modèle de zone** de l’onglet **styles** , pointez sur **remplissage**.  Le remplissage d’un élément est mis en surbrillance dans la fenêtre d’affichage.  

    > [!NOTE]
    > En fonction de la taille de votre fenêtre DevTools, il est possible que vous deviez faire défiler vers le bas de l’onglet **styles** pour afficher le **modèle de zone**.  

1.  Double-cliquez sur la marge gauche dans le **modèle de zone**, ce qui a pour effet de savoir `-` que l’élément n’a pas de marge gauche.  
1.  Tapez `100px` et appuyez sur `Enter` .  Le **modèle Box** utilise par défaut la valeur pixels, mais accepte également d’autres valeurs, comme `25%` , ou `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Survol du remplissage de l’élément" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Figure 6: survol du remplissage de l’élément  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Modification de la marge gauche de l’élément" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Figure 7: modification de la marge gauche de l’élément  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## Débogage de requêtes multimédias  

Les [requêtes multimédias][MDNUsingMediaGueries] permettent de répartir le produit Web aux modifications apportées aux paramètres de configuration de chaque utilisateur.  Le cas d’utilisation le plus notable consiste à fournir à votre produit une disposition CSS différente selon les dimensions de la fenêtre d’affichage.  L’utilisation de dispositions séparées autorise la mise en page à une colonne pour les appareils mobiles et les mises en page de plusieurs colonnes lorsque davantage de surface d’écran est disponible.  

Si vous souhaitez déboguer ou tester les requêtes multimédias que vous avez définies dans votre CSS, procédez comme suit.  

1.  Ouvrez les outils de développement et sélectionnez l’icône **basculer la barre d’outils** de l’appareil dans le coin supérieur gauche, ou appuyez sur `Ctrl` + `Shift` + `M` \ ( `Cmd` + `Shift` + `M` sur MacOS \).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Ouverture de la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Figure 8: ouverture de la barre d’outils de l’appareil  
    :::image-end:::  
    
1.  Ouvrez la barre d’outils de l’appareil, sélectionnez le `...` menu dans le coin supérieur droit, puis sélectionnez **afficher les requêtes multimédias**.  Vous devez voir les barres de couleur qui s’affichent au-dessus de l’affichage de la page qui représentent les différentes requêtes multimédia.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Affichage de requêtes multimédias dans la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Figure 9: affichage de requêtes multimédias dans la barre d’outils de l’appareil  
    :::image-end:::  
    
1.  Placez le pointeur de la souris sur les limites dans les barres pour afficher les valeurs des différentes requêtes multimédias. Sélectionnez chaque pour redimensionner la page Web pour qu’elle corresponde.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Sélection d’une requête multimédia dans la barre d’aperçu" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Figure 10: sélectionner une requête multimédia dans la barre d’aperçu  
    :::image-end:::  
    
1.  Pour déboguer des requêtes multimédias et ouvrir le fichier CSS dans l' `Sources` éditeur, pointez sur l’un des segments de la barre, ouvrez le menu contextuel \ (cliquez avec le bouton droit sur \), puis sélectionnez `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Affichage de requêtes multimédias dans l’éditeur de sources" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Figure 11: affichage de requêtes multimédias dans l’éditeur de sources  
    :::image-end:::  
    
<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemples CSS-Microsoft Edge (chrome) DevTools | Problème"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
