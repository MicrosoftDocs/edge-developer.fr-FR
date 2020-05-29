---
title: Découvrir comment afficher et modifier des feuilles CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601816"
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





# Découvrir comment afficher et modifier des feuilles CSS   



Suivez ces didacticiels interactifs pour découvrir les notions de base de l’affichage et de la modification de la CSS d’une page à l’aide de Microsoft Edge DevTools.  

## Exemples de CSS ouverts  

1.  Maintenez la touche Windows enfoncée `Control` `Command` et cliquez sur les **exemples CSS** pour ouvrir une nouvelle fenêtre.  
    
    [Exemples CSS][GlitchDevToolsCssExamples]  

> [!NOTE]
> Si vous voulez [ancrer votre fenêtre devtools][DevToolsCustomizePlacement] à droite de votre fenêtre d’affichage \ (illustrée dans la [figure 1](#figure-1)\), cliquez sur **personnaliser et contrôler devtools** `...` .  Dans le menu déroulant **personnaliser et contrôler devtools** , dans la section **ancrer** , sélectionnez **ancrer à droite**.  
    
## Affichage de la feuille de style en cascade pour un élément   

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Cliquez avec le bouton droit sur le `Inspect Me!` texte, puis sélectionnez **inspecter**.  
    1.  Dans DevTools, dans le panneau **éléments** , dans l’onglet **arborescence DOM** , l' `Inspect Me!` élément est mis en surbrillance.  
        
        > ##### Figure1  
        > L’élément inspecté est surligné dans l' **arborescence DOM**  
        > ![L’élément inspecté est surligné dans l’arborescence DOM][ImageInspect]  
        
    1.  Dans l' `Inspect Me!` élément, recherchez la valeur de l' `data-message` attribut et copiez-la.  
1.  Dans la page, dans la zone **valeur de `data-message` :** , entrez la valeur.  
1.  Cliquez avec le bouton droit sur le `Inspect Me!` texte, puis sélectionnez **inspecter**.  
    
    1.  Dans DevTools, dans le panneau **éléments** , sélectionnez l’onglet **styles** .  
    1.  Dans l’onglet **styles** , l' `Inspect Me!` élément est mis en surbrillance.  
    1.  Dans l' `Inspect Me!` élément, recherchez la `aloha` règle de classe.  
        
        > [!NOTE]
        > Cette règle s’affiche, car elle est appliquée à l' `Inspect Me!` élément.  
        
    1.  Dans la `aloha` classe, recherchez la valeur du `padding` style et copiez-la.  
        
        > ##### Figure 2  
        > Les classes CSS qui sont appliquées à l’élément sélectionné, par exemple `aloha` , sont affichées dans l’onglet **styles** .  
        > ![Les classes CSS appliquées à l’élément inspecté sont mises en surbrillance dans l’onglet styles][ImageAloha]  
        
1.  Dans la page, dans la zone **valeur de `padding` :** , entrez la valeur.  

## Ajouter une déclaration CSS à un élément   

Utilisez l’onglet **styles** lorsque vous voulez modifier ou ajouter des déclarations CSS à un élément.  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Cliquez avec le bouton droit sur le `Add A Background Color To Me!` texte, puis sélectionnez **inspecter**.  
1.  Cliquez `element.style` près du haut de l’onglet **styles** .  
1.  Tapez `background-color` et appuyez sur `Enter` .  
1.  Tapez `honeydew` et appuyez sur `Enter` .  Dans l' **arborescence DOM** , vous devez voir qu’une déclaration de style intraligne a été appliquée à l’élément.  

> ##### Figure3  
> La `background-color:honeydew` déclaration a été appliquée à l’élément à l’aide `element.style` de la section de l’onglet **styles** .  
> ![Ajout d’une déclaration CSS à l’élément à l’aide de l’onglet styles][ImageDeclaration]  

## Ajouter une classe CSS à un élément   

Utilisez l’onglet **styles** pour voir l’apparence d’un élément lorsqu’une classe CSS est appliquée à un élément ou a été supprimée.  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Cliquez avec le bouton droit sur l' `Add A Class To Me!` élément, puis sélectionnez **inspecter**.  
1.  Cliquez sur **. CLS**.  DevTools révèle une zone de texte dans laquelle vous pouvez ajouter des classes à l’élément sélectionné.  
1.  Entrez `color_me` dans la zone de texte **Ajouter une nouvelle classe** , puis appuyez sur `Enter` .  Une case à cocher s’affiche sous la zone de texte **Ajouter une nouvelle classe** , dans laquelle vous pouvez activer ou désactiver la classe.  Si d' `Add A Class To Me!` autres classes sont appliquées à l’élément, vous pouvez également basculer chacun d’eux ici.  

> ##### Figure 4  
> La `color_me` classe a été appliquée à l’élément à l’aide de la section **. CLS** de l’onglet **styles** .  
> ![Application de la classe color_me à l’élément][ImageApplyClass]  

## Ajouter un PseudoState à une classe   

Utilisez l’onglet **styles** pour appliquer de manière définitive une PseudoState CSS à un élément.  DevTools prend en charge `:active` , `:focus` , `:hover` et `:visited` .  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Placez le pointeur sur le `Hover Over Me!` texte.  La couleur d’arrière-plan change.  
1.  Cliquez avec le bouton droit sur le `Hover Over Me!` texte, puis sélectionnez **inspecter**.  
1.  Dans l’onglet **styles** , cliquez sur **: HOV**.  
1.  Cochez la case **sensitif** .  La couleur d’arrière-plan change comme auparavant, même si vous n’avez pas réellement pointé sur l’élément.  

> ##### Figure 5  
> Activer/désactiver le `:hover` PseudoState sur un élément  
> ![Activation de la fonction Hover PseudoState sur un élément][ImageSetHover]  

## Modifier les dimensions d’un élément   

Pour modifier la largeur, la hauteur, le remplissage, la marge ou la taille de la bordure d’un élément, utilisez le diagramme interactif du **modèle de zone** dans l’onglet **styles** .  

> [!NOTE]
> Complétez la [fenêtre d’affichage de la feuille de style en cascade pour un élément](#view-the-css-for-an-element) , avant d’effectuer celle-ci.  

1.  [Exemples de CSS ouverts](#open-css-examples).  
1.  Cliquez avec le bouton droit sur l' `Change My Margin!` élément, puis sélectionnez **inspecter**.  
1.  Dans le diagramme de **modèle de zone** de l’onglet **styles** , pointez sur **remplissage**.  Le remplissage d’un élément est mis en surbrillance dans la fenêtre d’affichage.  

    > [!NOTE]
    > En fonction de la taille de votre fenêtre DevTools, il est possible que vous deviez faire défiler vers le bas de l’onglet **styles** pour afficher le **modèle de zone**.  

1.  Double-cliquez sur la marge gauche dans le **modèle de zone**, ce qui a pour effet de savoir `-` que l’élément n’a pas de marge gauche.  
1.  Tapez `100px` et appuyez sur `Enter` .  Le **modèle Box** utilise par défaut la valeur pixels, mais accepte également d’autres valeurs, comme `25%` , ou `10vw` .  

> ##### Figure 6  
> Survol du remplissage de l’élément  
> ![Survol du remplissage de l’élément][ImageShowPadding]  

> ##### Figure 7  
> Modification de la marge gauche de l’élément  
> ![Modification de la marge gauche de l’élément][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Figure 1: l’élément inspecté est surligné dans l’arborescence DOM"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Figure 2: les classes CSS appliquées à l’élément inspecté sont mises en surbrillance dans l’onglet styles"  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Figure 3: ajouter une déclaration CSS à l’élément à l’aide de l’onglet styles"  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Figure 4: application de la classe color_me à l’élément"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Figure 5: activer/désactiver le survol PseudoState sur un élément"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Figure 6: survol du remplissage de l’élément"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Figure 7: modification de la marge gauche de l’élément"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Changer la position de Microsoft Edge DevTools (détacher, ancrer en bas, ancrer à gauche)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemples CSS-Microsoft Edge (chrome) DevTools | Problème"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
