---
description: Découvrez comment utiliser Microsoft Edge DevTools pour afficher et modifier le CSS d’une page CSS.
title: Inspecter la grille CSS dans Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 034fbdf82ddba39fc0818bc6f3add8824c6bb3ac
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439260"
---
# <a name="inspect-css-grid"></a>Inspecter la grille CSS  

Cet article vous explique en détail l’identification des grilles CSS sur un site web et le débogage des problèmes de disposition de grille à l’aide de superpositions de grille personnalisables.  

Les exemples utilisés dans les figures de cet article sont issus des pages web suivantes.  

*   [Zone de fruit][JecFyiDemoCssGridFruit]  
*   [Zone de boîtier de case][JecFyiDemoCssGridSnack]  

## <a name="before-you-begin"></a>Avant de commencer  

CSS Grid est un paradigme de disposition puissant pour le web.  Le guide de disposition de la grille [CSS][MdnCssGridLayout] sur MDN est un excellent point de départ pour apprendre à connaître CSS Grid et les nombreuses fonctionnalités.  

## <a name="discover-css-grids"></a>Découvrir les grilles CSS  

Lorsqu’un élément HTML de votre page s’y est appliqué, un badge s’affiche à côté de celui-ci dans le `display: grid` `display: inline-grid` panneau `grid` [Éléments.][DevtoolsGuideChromiumOpen]  

:::image type="complex" source="../media/grid-discover-grid.msft.png" alt-text="Découvrir la grille" lightbox="../media/grid-discover-grid.msft.png":::
   Découvrir la grille  
:::image-end:::  

Choisissez le badge pour faire bascule l’affichage d’une superposition de grille sur la page.  La superposition apparaît sur l’élément, disposé comme une grille pour afficher la position des lignes et des pistes de la grille :  

:::image type="complex" source="../media/grid-highlight-grid.msft.png" alt-text="Badge De grille bascule" lightbox="../media/grid-highlight-grid.msft.png":::
   Badge De grille bascule  
:::image-end:::  

Ouvrez **le volet** Disposition.  Lorsque des grilles sont incluses sur une page, le volet De disposition inclut une section **Grille** contenant un certain nombre d’options pour afficher les grilles. ****  

:::image type="complex" source="../media/grid-layout-pane.msft.png" alt-text="Volet de disposition" lightbox="../media/grid-layout-pane.msft.png":::
   **Volet** de disposition  
:::image-end:::  

La **** section Grille **du** volet De disposition contient les 2 sous-sections suivantes.  

*   Paramètres d’affichage de superposition  
*   Superpositions de grille  

<!--todo: @zoher verify the details for each of the sub-sections.  -->  

## <a name="overlay-display-settings"></a>Paramètres d’affichage de superposition  

Les **paramètres d’affichage de** superposition se composent de 2 parties suivantes.  

*   Choisissez l’une des options suivantes dans le menu déroulant.  
    
    | Option de ligne | Détails |  
    |:--- |:--- |  
    | **Masquer les étiquettes de ligne** | Masquez les étiquettes des lignes pour chaque superposition de grille. |  
    | **Afficher les numéros de ligne** | Afficher les numéros des lignes pour chaque superposition de grille \(sélectionné par défaut\). |  
    | **Afficher les noms des lignes** | Affichez les noms des lignes pour chaque superposition de grille lorsque des noms sont fournis. |  
    
*  Cochez la case en regard des options suivantes.  
    
    | Option | Détails |  
    |:--- |:--- |  
    | **Afficher les tailles des pistes**  | Affichez \(ou masquez\) les tailles des pistes. |  
    | **Afficher les noms de zone** | Affichez \(ou masquez\) les noms de la zone, lorsque des noms sont fournis. |  
    | **Étendre les lignes de grille** | Affiche \(ou masque\) les extensions de la grille le long de chaque axe.  Par défaut, les lignes de grille sont affichées uniquement à l’intérieur de l’élément avec `display: grid` `display: inline-grid` ou CSS définie sur celui-ci. |  
    
Les sections suivantes fournissent des détails pour chacun des **paramètres d’affichage Superposition.**  

### <a name="show-line-numbers"></a>Afficher les numéros de ligne  

Par défaut, les numéros de ligne positifs et négatifs sont affichés sur la superposition de la grille.  

Pour plus d’informations sur les nombres négatifs dans la superposition de la grille, accédez au placement basé sur une ligne [avec la grille CSS.][MdnLineBasedPlacementCssGrid]  

:::image type="complex" source="../media/grid-show-line-numbers.msft.png" alt-text="Afficher les numéros de ligne" lightbox="../media/grid-show-line-numbers.msft.png":::
   Afficher les numéros de ligne  
:::image-end:::  

### <a name="hide-line-labels"></a>Masquer les étiquettes de ligne  

Choisissez **Masquer les étiquettes de** ligne pour masquer les numéros de ligne.  

:::image type="complex" source="../media/grid-hide-line-labels.msft.png" alt-text="Masquer les étiquettes de ligne" lightbox="../media/grid-hide-line-labels.msft.png":::
   Masquer les étiquettes de ligne  
:::image-end:::  

### <a name="show-line-names"></a>Afficher les noms des lignes  

Pour plus d’informations sur les noms de lignes dans la superposition de grille, accédez à Disposition à l’aide de [lignes de grille nommées.][MdnLayoutUsingNamedGridLines]  

Choisissez **Afficher les noms de ligne** pour afficher les noms de ligne au lieu des nombres.  Dans l’exemple, 4 lignes ont des noms `left` : , , et `middle1` `middle2` `right` .  

<!--In the demo, **orange** element spans from left to right, with `grid-column: left` and `grid-column: right` CSS.  Showing line names makes it easier to visualize the start and end position of the element.  -->  

:::image type="complex" source="../media/grid-show-line-names.msft.png" alt-text="Afficher les noms des lignes" lightbox="../media/grid-show-line-names.msft.png":::
   **Afficher les noms des lignes**  
:::image-end:::  

### <a name="show-track-sizes"></a>Afficher les tailles des pistes  

Activez la **case à cocher** Afficher les tailles des pistes pour afficher les tailles de piste de la grille.  

DevTools s’affiche `[authored size]` et dans chaque étiquette de `[computed size]` ligne.  

| Taille | Détails |  
|:--- |:--- |  
| **taille d’auteur** | Taille définie dans la feuille de style \(omise si elle n’est pas définie\). |  
| **taille calculée** | Taille réelle à l’écran. |  

Dans la démonstration, les `snack-box` tailles de colonne sont définies dans `grid-template-columns:1fr 2fr;` le CSS.  Par conséquent, les étiquettes de ligne de colonne affichent les tailles calculées et les tailles de la colonne.  

| Suivre la taille | Taille de la forme de la forme | Taille calculée |  
|:--- |:--- |:--- |  
| **1fr** &#x2022; **96,66 px** | 1fr | 96,66 px |  
| **2fr** &#x2022; **193,32 px** | 2fr | 193,32 px |  

Les étiquettes de ligne affichent uniquement les tailles calculées, car aucune taille de ligne n’est définie dans la feuille de style.  

| Suivre la taille | Taille de la forme | Taille calculée |  
|:--- |:--- |:--- |  
| **80px** | &nbsp;| 80px |  
| **80px** | &nbsp;| 80px |  

:::image type="complex" source="../media/grid-show-track-sizes.msft.png" alt-text="Afficher les tailles des pistes" lightbox="../media/grid-show-track-sizes.msft.png":::
   **Afficher les tailles des pistes**  
:::image-end:::  

### <a name="show-area-names"></a>Afficher les noms de zone  

Pour afficher les noms de zone, activez la case à cocher Afficher les **noms de** zone.  Dans l’exemple, il y a 3 zones dans la grille : **haut,** **bas1** et **bas2**.  

:::image type="complex" source="../media/grid-show-area-names.msft.png" alt-text="Afficher les noms de zone" lightbox="../media/grid-show-area-names.msft.png":::
   **Afficher les noms de zone**  
:::image-end:::  

### <a name="extend-grid-lines"></a>Étendre les lignes de grille  

Activez la **case à cocher Étendre** les lignes de la grille pour étendre les lignes de grille au bord de la vue le long de chaque axe.  

:::image type="complex" source="../media/grid-extend-grid-lines.msft.png" alt-text="Étendre les lignes de grille" lightbox="../media/grid-extend-grid-lines.msft.png":::
   **Étendre les lignes de grille**  
:::image-end:::  

## <a name="grid-overlays"></a>Superpositions de grille  

La section **Superpositions** de grille contient une liste de grilles présentes sur la page, chacune avec une case à cocher, ainsi que différentes options.  

### <a name="enable-overlay-views-of-multiple-grids"></a>Activer les affichages de superposition de plusieurs grilles  

Pour afficher la grille de superposition pour plusieurs grilles, cochez la case en regard de chaque nom de la grille.  Dans l’exemple, il existe 2 superpositions de grilles activées qui sont chacune représentées avec des couleurs différentes.  

*   `main`  
*   `div.snack-box`  
    
:::image type="complex" source="../media/grid-grid-overlays.msft.png" alt-text="Activer les affichages de superposition de plusieurs grilles" lightbox="../media/grid-grid-overlays.msft.png":::
   Activer les affichages de superposition de plusieurs grilles  
:::image-end:::  

### <a name="customize-the-grid-overlay-color"></a>Personnaliser la couleur de superposition de la grille  

Pour ouvrir le s picker de couleurs et personnaliser la couleur de superposition de la grille, sélectionnez la case à côté du nom de la superposition de la grille.  

:::image type="complex" source="../media/grid-grid-overlays-color.msft.png" alt-text="Personnaliser la couleur de superposition de la grille" lightbox="../media/grid-grid-overlays-color.msft.png":::
   Personnaliser la couleur de superposition de la grille  
:::image-end:::  

### <a name="highlight-the-grid"></a>Surligner la grille  

Pour mettre en surbrillez l’élément HTML dans l’outil **Elements** et faites-le défiler sur la page web, choisissez l’élément **Show** dans le panneau Éléments \( Afficher l’élément dans l’icône du panneau Éléments ![ ](../media/show-element-in-element-panel-icon.msft.png) \).  

:::image type="complex" source="../media/grid-grid-overlays-highlight.msft.png" alt-text="Surligner la grille" lightbox="../media/grid-grid-overlays-highlight.msft.png":::
   Surligner la grille  
:::image-end:::  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumOpen]: ../open/index.md "Ouvrez Microsoft Edge DevTools | Documents Microsoft"  

[JecFyiDemoCssGridFruit]: https://jec.fyi/demo/css-grid-fruit "Grille CSS | jec.fyi"  
[JecFyiDemoCssGridSnack]: https://jec.fyi/demo/css-grid-snack "Grille CSS | jec.fyi"  

[MdnCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Modèle de disposition de grille CSS | MDN"  
[MdnLayoutUsingNamedGridLines]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines "Disposition à l’aide de lignes de grille nommées | MDN"  
[MdnLineBasedPlacementCssGrid]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid "Placement basé sur une ligne avec grille CSS | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/grid) et est créée par [Jecelyn Yeen][JecelynYeen] \(Appui au développeur, Chrome DevTools\)  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[JecelynYeen]: https://developers.google.com/web/resources/contributors/jecelynyeen  
