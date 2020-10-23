---
description: Découvrez comment utiliser Microsoft Edge DevTools pour afficher et modifier la CSS d’une page CSS.
title: Examiner la grille CSS dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 150aea57aa676580b554cc74292671ed567a0a2c
ms.sourcegitcommit: 6e2b26d41a0aa56ac34e6edc7dddd852ddb415b1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/23/2020
ms.locfileid: "11134011"
---
# Inspecter la grille CSS  

Cet article vous guide tout au long de l’identification des grilles de CSS sur un site Web et au débogage des problèmes de disposition de grille à l’aide de superpositions de grille personnalisées.  

Les exemples présentés dans cet article sont tirés des pages Web suivantes.  

*   [Champ fruit][JecFyiDemoCssGridFruit]  
*   [Zone collation][JecFyiDemoCssGridSnack]  

## Avant de commencer  

Grille CSS est un paradigme de disposition puissant pour le Web.  Pour commencer à vous familiariser avec la grille CSS et les nombreuses fonctionnalités, consultez le Guide de disposition de la [grille CSS][MdnCssGridLayout] sur MDN.  

## Découvrir les grilles CSS  

Lorsqu’un élément HTML de votre page l’a `display: grid` ou `display: inline-grid` lui est appliqué, un `grid` badge s’affiche à côté de celui-ci dans le panneau [éléments][DevtoolsGuideChromiumOpen] .  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-discover-grid.msft.png":::
   Découvrir la grille  
:::image-end:::  

Sélectionnez le badge pour basculer vers l’affichage d’une superposition de grille sur la page.  La superposition s’affiche au-dessus de l’élément, disposé comme une grille pour afficher la position des lignes et des pistes de la grille:  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-highlight-grid.msft.png":::
   Activer/désactiver le badge de grille  
:::image-end:::  

Ouvrir le volet **disposition**  Lorsque les grilles sont incluses sur une page, le volet **disposition** inclut une section **grille** contenant un certain nombre d’options pour afficher les grilles.  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-layout-pane.msft.png":::
   Volet **disposition**  
:::image-end:::  

La section **grille** du volet **disposition** contient les 2 sous-sections suivantes.  

*   Paramètres d’affichage de la superposition  
*   Superpositions de grille  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## Paramètres d’affichage de la superposition  

Les **paramètres d’affichage de la superposition** se composent de 2 parties suivantes.  

*   Dans le menu déroulant, choisissez l’une des options suivantes.  
    
    | Option ligne | Détails |  
    |:--- |:--- |  
    | **Masquer les étiquettes de lignes** | Masquez les étiquettes des lignes pour chaque superposition de grille. |  
    | **Afficher les numéros de ligne** | Afficher les numéros des lignes pour chaque superposition de la grille \ (option activée par défaut). |  
    | **Afficher les noms de lignes** | Afficher les noms des lignes pour chaque superposition de grille lorsque les noms sont fournis. |  
    
*  Cochez la case en regard des options suivantes.  
    
    | Option | Détails |  
    |:--- |:--- |  
    | **Afficher les tailles de suivi**  | Afficher \ (ou masquer \) les tailles des pistes. |  
    | **Afficher les noms des zones** | Afficher \ (ou masquer \) le nom de la zone lorsque des noms sont fournis. |  
    | **Prolonger le quadrillage** | Affiche \ (ou masque) les extensions des dimensions de la grille le long de chaque axe.  Par défaut, les lignes de grille apparaissent uniquement à l’intérieur de l’élément avec `display: grid` ou des `display: inline-grid` styles CSS définis sur celle-ci. |  
    
Les sections suivantes fournissent des détails sur chacun des **paramètres d’affichage de la superposition**.  

### Afficher les numéros de ligne  

Par défaut, les nombres de lignes positifs et négatifs sont affichés dans la superposition de la grille.  

Pour plus d’informations sur les nombres négatifs dans la superposition de la grille, voir [placement en ligne avec CSS Grid][MdnLineBasedPlacementCssGrid].  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-show-line-numbers.msft.png":::
   Afficher les numéros de ligne  
:::image-end:::  

### Masquer les étiquettes de lignes  

Pour masquer les numéros de ligne, sélectionnez **Masquer les étiquettes de lignes** .  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-hide-line-labels.msft.png":::
   Masquer les étiquettes de lignes  
:::image-end:::  

### Afficher les noms de lignes  

<!--todo: @rachel verify the link and text for line name -->  
Pour plus d’informations sur les noms de lignes dans la superposition de grille, accédez à [disposition à l’aide de l’intitulé lignes de grille][MdnLayoutUsingNamedGridLines].  

Sélectionnez **afficher les noms des lignes** pour afficher les noms de lignes au lieu de nombres.  Dans l’exemple, quatre lignes portent des noms: `left` , `middle1` ,, `middle2` et `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-show-line-names.msft.png":::
   **Afficher les noms de lignes**  
:::image-end:::  

### Afficher les tailles de suivi  

Activez la case à cocher **afficher les tailles de suivi** pour afficher les tailles de suivi de la grille.  

DevTools affiche `[authored size]` et `[computed size]` dans chaque étiquette de ligne.  

| Taille | Détails |  
|:--- |:--- |  
| **taille créée** | Taille définie dans la feuille de style \ (omise si non définie \). |  
| **taille calculée** | Taille réelle à l’écran. |  

Dans la démonstration, les `snack-box` tailles de colonnes sont définies dans la `grid-template-columns:1fr 2fr;` feuille de style en cascade (CSS).  Par conséquent, les étiquettes des lignes de colonnes affichent des tailles créées et calculées.  

| Taille du suivi | Taille créée | Taille calculée |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96.66 PX** | 1fr | 96.66 PX |  
| **2fr** &#x2022; **193.32 PX** | 2fr | 193.32 PX |  

Les étiquettes de ligne de ligne n’affichent que des tailles calculées, car il n’y a pas de tailles de lignes définies dans la feuille de style.  

| Taille du suivi | Taille créée | Taille calculée |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Afficher les tailles de suivi**  
:::image-end:::  

### Afficher les noms des zones  

Pour afficher les noms de zone, activez la case à cocher **afficher les noms des zones** .  Dans l’exemple, il existe 3 zones dans la grille: **Top**, **bottom1** et **bottom2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-show-area-names.msft.png":::
   **Afficher les noms des zones**  
:::image-end:::  

### Prolonger le quadrillage  

Activez la case à cocher **prolonger les lignes de grille** pour étendre les lignes de la grille au bord de la fenêtre d’affichage, le long de chaque axe.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Prolonger le quadrillage**  
:::image-end:::  

## Superpositions de grille  

La section **façades de grille** contient une liste des grilles présentes dans la page, chacune avec un élément CheckBox avec des options différentes.  

### Activer les vues de superposition de plusieurs grilles  

<!--todo: @zoher verify and provide updates -->  

Pour afficher la grille Overlay pour plusieurs grilles, activez la case à cocher en regard de chaque nom de la grille.  Dans l’exemple, il est possible d’activer 2 superpositions de grille avec des couleurs différentes.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-grid-overlays.msft.png":::
   Activer les vues de superposition de plusieurs grilles  
:::image-end:::  

### Personnaliser la couleur de superposition de la grille  

Pour ouvrir le sélecteur de couleurs et personnaliser la couleur de superposition de la grille, sélectionnez la zone en regard du nom de la superposition de la grille.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Personnaliser la couleur de superposition de la grille  
:::image-end:::  

### Mettre en surbrillance la grille  

Pour mettre en surbrillance l’élément HTML dans le panneau **éléments** et y faire défiler dans la page Web, sélectionnez l' **élément afficher dans le panneau éléments** \ ( ![ élément d’affichage de l’icône \) du panneau éléments ][ImageShowElementInElementsPanelIcon] .  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Mettre en surbrillance la grille  
:::image-end:::  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageShowElementInElementsPanelIcon]: ../media/show-element-in-element-panel-icon.msft.png  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Grille CSS | JEC. Money"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Grille CSS | JEC. Money"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Disposition Grille CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Mise en page à l’aide de la grille nommée MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Placement en ligne avec grille CSS | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/grid) et est créée par [Jecelyn Yeen][JecelynYeen] \ (développeurs, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
