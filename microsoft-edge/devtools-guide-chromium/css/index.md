---
description: Découvrez comment utiliser Microsoft Edge DevTools pour afficher et modifier le CSS d’une page.
title: Prise en main de l’affichage et de la modification de CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: b3d19d34f329fec7a3903fb37e8be3558ba4d31d
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399091"
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

# <a name="get-started-with-viewing-and-changing-css"></a>Prise en main de l’affichage et de la modification de CSS  

Complétez ces didacticiels interactifs pour découvrir les principes de base de l’affichage et de la modification du CSS d’une page à l’aide de Microsoft Edge DevTools.  

## <a name="open-css-examples"></a>Exemples open CSS  

1.  Hold `Control` \(Windows, Linux\) or `Command` \(macOS\) and choose **CSS Examples** to open in a new window.  
    
    [Exemples CSS][GlitchDevToolsCssExamples]  
    
    > [!NOTE]
    > Si vous souhaitez ancrer votre [fenêtre DevTools][DevToolsCustomizePlacement] à droite de votre fenêtre d’affichage \(affichée dans la figure suivante\), choisissez Personnaliser et contrôler **DevTools.** `...`  On the **Customize and control DevTools** drop-down menu, in the **Dock side** section, choose Dock **to right**.  
    
## <a name="view-the-css-for-an-element"></a>Afficher le CSS d’un élément  

1.  [Ouvrez des exemples CSS.](#open-css-examples)  
1.  Pointez sur `Inspect Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
    1.  Dans DevTools, sur l’outil **Elements,** dans le panneau Arborescence **DOM,** l’élément `Inspect Me!` est mis en surbrillrillant.  
        
        :::image type="complex" source="../media/css-elements-inspect-me.msft.png" alt-text="L’élément inspecté est mis en surbrillant dans l’arborescence DOM" lightbox="../media/css-elements-inspect-me.msft.png":::
           L’élément inspecté est mis en surbrillant dans l’arborescence **DOM**  
        :::image-end:::  
        
    1.  Dans `Inspect Me!` l’élément, recherchez la valeur de `data-message` l’attribut et copiez-la.  
1.  Sur la page, dans la **boîte de texte Valeur de `data-message` :** , entrez la valeur.  
1.  Pointez sur `Inspect Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
    1.  Dans DevTools, dans l’outil **Éléments,** sélectionnez le **panneau Styles.**  
    1.  Dans le **panneau Styles,** `Inspect Me!` l’élément est mis en surbrillant.  
    1.  Dans `Inspect Me!` l’élément, recherchez la `aloha` règle de classe.  
        
        > [!NOTE]
        > Cette règle s’affiche, car elle est appliquée à `Inspect Me!` l’élément.  
        
    1.  Dans la `aloha` classe, recherchez la valeur du `padding` style et copiez-la.  
        
        :::image type="complex" source="../media/css-elements-inspect-me-styles.msft.png" alt-text="Les classes CSS sont appliquées à l’élément inspecté sont mises en surbrill" lightbox="../media/css-elements-inspect-me-styles.msft.png":::
           Les classes CSS sont appliquées à l’élément sélectionné, par exemple, sont affichées dans le `aloha` **panneau Styles**  
        :::image-end:::  
        
1.  Sur la page, dans la **boîte de texte Valeur de `padding` :** , entrez la valeur.  

## <a name="add-a-css-declaration-to-an-element"></a>Ajouter une déclaration CSS à un élément  

Utilisez le **panneau Styles** lorsque vous souhaitez modifier ou ajouter des déclarations CSS à un élément.  

> [!NOTE]
> Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.  

1.  [Ouvrez des exemples CSS.](#open-css-examples)  
1.  Pointez sur `Add A Background Color To Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
1.  Choisissez `element.style` en haut du panneau **Styles.**  
1.  Tapez `background-color` et sélectionnez `Enter` .  
1.  Tapez `honeydew` et sélectionnez `Enter` .  Dans **l’arborescence DOM,** une déclaration de style inline appliquée à l’élément s’affiche.  
    
    :::image type="complex" source="../media/css-elements-add-background-color-to-me-styles-p.msft.png" alt-text="Ajouter une déclaration CSS à l’élément à l’aide du panneau Styles" lightbox="../media/css-elements-add-background-color-to-me-styles-p.msft.png":::
       La `background-color:honeydew` déclaration est appliquée à l’élément à l’aide de la section du panneau `element.style` **Styles**  
    :::image-end:::  
    
## <a name="add-a-css-class-to-an-element"></a>Ajouter une classe CSS à un élément  

Pour afficher l’apparence d’un élément lorsqu’une classe CSS est appliquée à un élément ou supprimée d’un élément, accédez au **panneau Styles.**  

> [!NOTE]
> Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.  

1.  [Ouvrez des exemples CSS.](#open-css-examples)  
1.  Pointez sur `Add A Class To Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
1.  Choisissez **.cls**.  DevTools révèle une zone de texte dans laquelle vous pouvez ajouter des classes à l’élément sélectionné.  
1.  Tapez dans la zone de texte Ajouter une nouvelle `color_me` classe, puis **** sélectionnez `Enter` .  Une case à cocher s’affiche sous la **zone** de texte Ajouter une nouvelle classe, dans laquelle vous pouvez l’élémenter ou le désébaser.  Si d’autres classes sont appliquées à l’élément, vous pouvez également les faire basculer `Add A Class To Me!` à partir d’ici.  
    
    :::image type="complex" source="../media/css-elements-add-a-class-to-me-styles-cls.msft.png" alt-text="Appliquer la color_me classe à l’élément" lightbox="../media/css-elements-add-a-class-to-me-styles-cls.msft.png":::
       La `color_me` classe est appliquée à l’élément à l’aide de la section **.cls** du **panneau Styles**  
    :::image-end:::  
    
## <a name="add-a-pseudostate-to-a-class"></a>Ajouter un pseudo-état à une classe  

Utilisez le **panneau Styles** pour appliquer définitivement un pseudo-état CSS à un élément.  DevTools prend `:active` en charge , et `:focus` `:hover` `:visited` .  

> [!NOTE]
> Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.  

1.  [Ouvrez des exemples CSS.](#open-css-examples)  
1.  Pointez sur le `Hover Over Me!` texte.  La couleur d’arrière-plan change.  
1.  Pointez sur `Hover Over Me!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
1.  Dans le **panneau Styles,** choisissez **:hov**.  
1.  Cochez **la case :hover.**  La couleur d’arrière-plan change comme avant, même si vous ne pointez pas réellement sur l’élément.  
    
    :::image type="complex" source="../media/css-elements-hover-over-me-styles-hov-hover.msft.png" alt-text="Basculez le pseudo-état de pointage sur un élément" lightbox="../media/css-elements-hover-over-me-styles-hov-hover.msft.png":::
       Basculez le `:hover` pseudo-état sur un élément  
    :::image-end:::  
    
## <a name="change-the-dimensions-of-an-element"></a>Modifier les dimensions d’un élément  

Utilisez le diagramme interactif **De modèle** de zone dans le panneau **Styles** pour modifier la largeur, la hauteur, l’espacement, la marge ou la longueur de bordure d’un élément.  

> [!NOTE]
> Complétez le didacticiel [Afficher les CSS d’un](#view-the-css-for-an-element) élément avant de le faire.  

1.  [Ouvrez des exemples CSS.](#open-css-examples)  
1.  Pointez sur `Change My Margin!` le texte, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
1.  Dans le diagramme **de modèle Box** dans le panneau **Styles,** pointez sur **remplissage.**  Le remplissage d’un élément est mis en surbrillement dans laport d’affichage.  

    > [!NOTE]
    > Selon la taille de votre fenêtre DevTools, vous devrez peut-être faire défiler jusqu’au bas du panneau **Styles** pour afficher le **modèle box**.  

1.  Double-cliquez sur la marge de gauche dans le modèle **Box,** qui a actuellement une valeur qui signifie que l’élément `-` n’a pas de marge de gauche.  
1.  Tapez `100px` et sélectionnez `Enter` .  Par **défaut, le** modèle Box est en pixels, mais il accepte également d’autres valeurs, telles `25%` que , ou `10vw` .  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-padding.msft.png" alt-text="Pointer sur le remplissage de l’élément" lightbox="../media/css-elements-change-my-margin-styles-padding.msft.png":::
             Pointer sur le remplissage de l’élément  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-elements-change-my-margin-styles-margin-edit.msft.png" alt-text="Modifier la marge gauche de l’élément" lightbox="../media/css-elements-change-my-margin-styles-margin-edit.msft.png":::
             Modifier la marge gauche de l’élément  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
## <a name="debugging-media-queries"></a>Débogage de requêtes multimédias  

[Les requêtes multimédias][MDNUsingMediaGueries] sont un moyen de faire en sorte que votre produit web réagisse aux modifications apportées aux paramètres de configuration de chaque utilisateur.  Le cas d’utilisation le plus significatif consiste à fournir à votre produit une disposition CSS différente en fonction des dimensions de la vue.  L’utilisation de dispositions distinctes permet une disposition d’une colonne pour les appareils mobiles et des dispositions multi-colonnes lorsqu’il y a plus d’espace d’écran disponible.  

Si vous souhaitez déboguer ou tester les requêtes multimédias que vous avez définies dans votre CSS, utilisez les étapes suivantes.  

1.  Ouvrez les outils **** de développement et sélectionnez l’icône de la barre d’outils de l’appareil bascule en deuxième position en haut à gauche, ou sélectionnez `Ctrl` + `Shift` + `M` \( `Cmd` + `Shift` + `M` sur macOS\).  
    
    :::image type="complex" source="../media/css-elements-media-queries-open-device-toolbar.msft.png" alt-text="Ouvrir la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-open-device-toolbar.msft.png":::
       Ouvrir la barre d’outils de l’appareil  
    :::image-end:::  
    
1.  Une fois la barre d’outils de l’appareil ouverte, sélectionnez le menu en haut à droite `...` et choisissez Afficher les requêtes **multimédias.**  Les barres de couleur affichées au-dessus de la page web représentent les différentes requêtes multimédias.  
    
    :::image type="complex" source="../media/css-elements-media-queries-showing-mq.msft.png" alt-text="Afficher les requêtes multimédias dans la barre d’outils de l’appareil" lightbox="../media/css-elements-media-queries-showing-mq.msft.png":::
       Afficher les requêtes multimédias dans la barre d’outils de l’appareil  
    :::image-end:::  
    
1.  Pointez sur les limites des barres pour afficher les valeurs des différentes requêtes multimédias.  Choisissez chacune d’elles pour resizer la page web à mettre en correspondance.  
    
    :::image type="complex" source="../media/css-elements-media-queries-select-bar.msft.png" alt-text="Choisir la requête multimédia dans la barre d’aperçu" lightbox="../media/css-elements-media-queries-select-bar.msft.png":::
       Choisir la requête multimédia dans la barre d’aperçu  
    :::image-end:::  
    
1.  Pour déboguer les requêtes multimédias et ouvrir le fichier CSS dans l’éditeur ; pointez sur l’un des segments de barre, ouvrez le menu contextuel `Sources` \(clic droit\), puis sélectionnez `reveal in source code` .  
    
    :::image type="complex" source="../media/css-elements-media-queries-reveal-in-sources.msft.png" alt-text="Révéler les requêtes multimédias dans l’Éditeur de sources" lightbox="../media/css-elements-media-queries-reveal-in-sources.msft.png":::
       Révéler les requêtes multimédias dans l’Éditeur de sources  
    :::image-end:::  
    
## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Modifier l’emplacement de Microsoft Edge DevTools (Undock, Dock to Bottom, Dock To Left)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Exemples CSS - Microsoft Edge (Chromium) DevTools | Glitch"  

[MDNUsingMediaGueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Utilisation de requêtes multimédias | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
