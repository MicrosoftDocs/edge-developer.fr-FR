---
description: Découvrez les nouveaux flux de travail pour l’affichage et la modification de CSS dans Microsoft Edge DevTools.
title: Référence CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/04/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 0680b08c9809698c1db6c186a7be76a93c31df4b
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564475"
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
# <a name="css-reference"></a>Référence CSS  

Découvrez les nouveaux flux de travail dans la référence complète Microsoft Edge fonctionnalités DevTools relatives à l’affichage et à la modification de CSS.  

Pour en savoir plus sur les bases, [accédez à Prise en main avec l’affichage et la modification de CSS][DevToolsCSSGetStarted].  

## <a name="choose-an-element"></a>Choisir un élément  

**L’outil** Elements de DevTools vous permet d’afficher ou de modifier la CSS d’un élément à la fois.  L’élément sélectionné est mis en surbrillant dans **l’arborescence DOM.**  Les styles de l’élément sont affichés dans le **volet Styles.**  Pour un didacticiel, [accédez à Afficher le CSS d’un élément.][DevToolsCSSGetStartedTutorial]  

> [!NOTE]
> Dans la figure suivante, l’élément mis en surbrillant dans l’arborescence `h1` **DOM** est l’élément sélectionné.  À droite, les styles de l’élément sont affichés dans le **volet Styles.**  À gauche, l’élément est mis en surbrillrillation dans la vue, mais uniquement parce que la souris passe actuellement au-dessus de celui-ci dans l’arborescence **DOM**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Exemple d’élément sélectionné" lightbox="../media/css-elements-styles-h1.msft.png":::
   Exemple d’élément sélectionné  
:::image-end:::  

Utilisez l’une des actions suivantes pour sélectionner un élément.  

*   Dans votreport d’affichage, pointez sur l’élément, ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
*   Dans DevTools, choisissez Sélectionner un élément **\(** Sélectionnez un élément \) ou sélectionnez ![ ](../media/select-an-element-icon.msft.png) `Control` + `Shift` + `C` \(Windows, Linux\) ou `Command` + `Shift` + `C` \(macOS\), puis choisissez l’élément dans la vue.  
*   Dans DevTools, choisissez l’élément dans l’arborescence **DOM**.  
*   Dans DevTools, exécutez une requête comme dans la console, pointez sur le résultat, ouvrez le menu contextuel `document.querySelector('p')` \(clic **** droit\), puis choisissez Révéler dans le panneau **Éléments.**  

## <a name="view-css"></a>Afficher les CSS  

### <a name="view-the-external-stylesheet-where-a-rule-is-defined"></a>Afficher la feuille de style externe dans laquelle une règle est définie  

Dans le **volet Styles,** choisissez le lien en face d’une règle CSS pour ouvrir la feuille de style externe qui définit la règle.  La feuille de style s’ouvre dans le volet **Éditeur** de l’outil **Sources.**  

Si la feuille de style est minifiée, choisissez le **bouton Format** \( Format \), en bas du ![ volet ](../media/format-icon.msft.png) Éditeur. ****  Pour plus d’informations, accédez à [Reformater un fichier JavaScript minifié avec des caractères assez imprimés.][DevToolsJavascriptReferenceFormat]  

> [!NOTE]
> Dans la figure suivante, une fois que vous avez choisi, vous êtes conduit à la ligne 2 de , où la règle `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` `.content h1:first-of-type` CSS est définie.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Affichage de la feuille de style dans laquelle une règle est définie" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Affichage de la feuille de style dans laquelle une règle est définie  
:::image-end:::  

### <a name="view-only-the-css-that-is-actually-applied-to-an-element"></a>Afficher uniquement le CSS réellement appliqué à un élément  

Le **panneau Styles** affiche toutes les règles qui s’appliquent à un élément, y compris les déclarations qui ont été overridées.  Lorsque les déclarations non appliquées ne **** vous intéressent pas, utilisez le panneau Calculé pour afficher uniquement le CSS réellement appliqué à un élément.  

1.  [Sélectionnez un élément.](#choose-an-element)  
1.  Accédez au **panneau Calculé** dans **l’outil Éléments.**  

> [!NOTE]
> Dans une fenêtre DevTools **** large, le panneau Calculé n’existe pas.  Le contenu du panneau **Calculé** est affiché dans le **panneau Styles.**  

Les propriétés héritées sont opaques.  Pour afficher toutes les valeurs héritées, cochez **la case Afficher** tout.  

> [!NOTE]
> Dans la figure suivante, le panneau **Calculé** montre les propriétés CSS appliquées à l’élément actuellement `h1` sélectionné.  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Panneau calculé" lightbox="../media/css-elements-computed-h1.msft.png":::
   Panneau **calculé**  
:::image-end:::  

### <a name="view-css-properties-in-alphabetical-order"></a>Afficher les propriétés CSS par ordre alphabétique  

Utilisez le **panneau calculé.**  Accédez [à Afficher uniquement le CSS réellement appliqué à un élément.](#view-only-the-css-that-is-actually-applied-to-an-element)  

### <a name="view-inherited-css-properties"></a>Afficher les propriétés CSS héritées  

Cochez **la case Afficher** tout dans le panneau **calculé.**  Accédez [à Afficher uniquement le CSS réellement appliqué à un élément.](#view-only-the-css-that-is-actually-applied-to-an-element)  

### <a name="view-the-box-model-for-an-element"></a>Afficher le modèle de zone d’un élément  

Pour afficher [le modèle de zone d’un][MDNBoxModel] élément, accédez au panneau **Styles.**  Si votre fenêtre DevTools **** est étroite, le diagramme DevTools se trouve en bas du panneau.  

Choisissez et modifiez une valeur pour modifier une valeur.  

> [!NOTE]
> Dans la figure suivante, le diagramme **Modèle** de zone dans le panneau **Styles** montre le modèle de case pour l’élément `h1` actuellement sélectionné.  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Diagramme du modèle Box" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   Diagramme **du modèle Box**  
:::image-end:::  

### <a name="search-and-filter-the-css-of-an-element"></a>Rechercher et filtrer le CSS d’un élément  

Utilisez la **zone de** texte **** Filtre des **panneaux Styles** et Calculé pour rechercher des propriétés ou des valeurs CSS spécifiques.  

Pour également rechercher les propriétés héritées dans le **panneau Calculé,** cochez la case **Afficher tout.**  

> [!NOTE]
> Dans la figure suivante, le panneau **Styles** est filtré pour afficher uniquement les règles qui incluent la requête de `color` recherche.  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrer le panneau Styles" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtrer le **panneau Styles**  
:::image-end:::  

> [!NOTE]
> Dans la figure suivante, le panneau **calculé** est filtré pour afficher uniquement les déclarations qui incluent la requête de `100%` recherche.  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrer le panneau calculé" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtrer **le panneau calculé**  
:::image-end:::  

### <a name="toggle-a-pseudo-class"></a>Faire basculer une pseudo-classe  

Effectuer les actions suivantes pour faire basculer une pseudo-classe telle `:active` `:focus` que , ou `:hover` `:visited` .  

1.  [Sélectionnez un élément.](#choose-an-element)  
1.  Dans **l’outil Éléments,** accédez au **panneau Styles.**  
1.  Choose **:hov**.  
1.  Vérifiez la pseudo-classe que vous souhaitez activer.  

> [!NOTE]
> Dans la figure suivante, basculez la `:hover` pseudo-classe.  Dans laport d’affichage, vérifiez que la déclaration est appliquée à l’élément, même si l’élément n’est pas réellement `background-color: cornflowerblue` survolé.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Toggle the :hover pseudo-class" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Faire bascule la `:hover` pseudo-classe  
:::image-end:::  

Pour un didacticiel interactif, [accédez à Ajouter un pseudo-état à une classe.][DevToolsCSSGetStartedAddPseudoState]  

### <a name="view-a-page-in-print-mode"></a>Afficher une page en mode d’impression  

Effectuer les actions suivantes pour afficher une page en mode d’impression.  

1.  [Ouvrez le menu Commande.][DevToolsCommandMenu]  
1.  Commencez à taper `Rendering` et sélectionnez `Show Rendering` .  
1.  For the **Emulate CSS Media** dropdown, choose **print**.  

### <a name="view-used-and-unused-css-with-the-coverage-tool"></a>Afficher les CSS utilisés et inutilisés avec l’outil Couverture  

**L’outil** Couverture vous montre ce que les CSS d’une page utilisent réellement.  

1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\) alors que DevTools [][DevToolsCommandMenu]est en focus pour ouvrir le menu Commande.  
1.  Commencez à taper `coverage` et choisissez Afficher la **couverture.**  **L’outil** Couverture s’affiche.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Ouverture de l’outil Couverture à partir du menu Commande" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Ouvrir **l’outil Couverture** à partir du **menu Commande**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="L’outil Couverture" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             **L’outil Couverture**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Choose **Start instrumenting coverage and refresh the page** \( Start ![ instrumenting coverage and refresh the page ](../media/refresh-icon.msft.png) \).  La page est **** actualisée et l’outil Couverture fournit une vue d’ensemble de la quantité de CSS \(et JavaScript\) utilisée à partir de chaque fichier chargé par le navigateur.  Le vert représente le CSS utilisé.  Le rouge représente les CSS inutilisés.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Vue d’ensemble de la quantité de CSS (et JavaScript) utilisée et inutilisée" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Vue d’ensemble de la quantité de fichiers CSS \(et JavaScript\) utilisées et inutilisées  
    :::image-end:::  

1.  Pour afficher une répartition ligne par ligne du fichier CSS utilisé, choisissez un fichier CSS.  
    
    > [!NOTE]
    > Dans la figure suivante, les lignes 145 à 147 et 149 à 151 sont inutilisées, tandis que les lignes `b66bc881.site-ltr.css` 163 à 166 sont utilisées.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Répartition ligne par ligne des CSS utilisées et inutilisées" lightbox="../media/css-sources-css-coverage.msft.png":::
       Répartition ligne par ligne des CSS utilisées et inutilisées  
    :::image-end:::  
    
### <a name="force-print-preview-mode"></a>Forcer le mode d’aperçu avant impression  

Accédez à [Forcer DevTools en mode Aperçu avant impression.][DevToolsCssPrintPreview]  

## <a name="change-css"></a>Modifier CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### <a name="add-a-css-declaration-to-an-element"></a>Ajouter une déclaration CSS à un élément  

L’ordre des déclarations affecte le style d’un élément. Utilisez la liste suivante pour vous aider à ajouter des déclarations de différentes manières.  

*   [Ajoutez une déclaration inline](#add-an-inline-declaration).  Équivaut à ajouter un `style` attribut au code HTML d’un élément.  
*   [Ajoutez une déclaration à une règle de style.](#add-a-declaration-to-a-style-rule)  

**Quel flux de travail devez-vous utiliser ?** Pour la plupart des scénarios, vous souhaitez probablement utiliser le flux de travail de déclaration inline.  Les déclarations inline ont une spécificité plus élevée que les déclarations externes, de sorte que le flux de travail en ligne garantit que les modifications prennent effet dans votre élément attendu.  Pour plus d’informations sur la spécificité, accédez à [Types de sélecteur.][MDNSelectorTypes]  

Si vous déboguer des styles de l’élément et que vous devez spécifiquement tester ce qui se produit lorsqu’une déclaration est définie à différents endroits, utilisez l’autre flux de travail.  

#### <a name="add-an-inline-declaration"></a>Ajouter une déclaration inline  

Pour ajouter une déclaration inline, complétez les actions suivantes.  

1.  [Sélectionnez un élément.](#choose-an-element)  
1.  Dans le **volet Styles,** choisissez entre les crochets de la section **element.style.**  Le curseur se concentre, ce qui vous permet d’entrer du texte.  
1.  Entrez un nom de propriété et sélectionnez `Enter` .  
1.  Entrez une valeur valide pour cette propriété et sélectionnez `Enter` .  Dans **l’arborescence DOM,** vérifiez qu’un attribut a `style` été ajouté à l’élément.  

> [!NOTE]
> Dans la figure suivante, les propriétés et les propriétés `margin-top` `background-color` ont été appliquées à l’élément sélectionné.  Dans **l’arborescence DOM,** vérifiez que les déclarations sont reflétées dans `style` l’attribut d’un élément.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Ajouter des déclarations inline" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Ajouter des déclarations inline  
:::image-end:::  

#### <a name="add-a-declaration-to-a-style-rule"></a>Ajouter une déclaration à une règle de style  

Effectuer les actions suivantes pour ajouter une déclaration à une règle de style existante.  

1.  [Sélectionnez un élément.](#choose-an-element)  
1.  Dans le **volet Styles,** choisissez entre les crochets de la règle de style à laquelle vous souhaitez ajouter la déclaration.  Le curseur se concentre, ce qui vous permet d’entrer du texte.  
1.  Entrez un nom de propriété et sélectionnez `Enter` .  
1.  Entrez une valeur valide pour cette propriété et sélectionnez `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Ajout d’une déclaration à une règle de style" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Ajouter la `border-bottom-style:groove` déclaration à une règle de style  
:::image-end:::  

### <a name="change-a-declaration-name-or-value"></a>Modifier le nom ou la valeur d’une déclaration  

Choisissez et modifiez le nom ou la valeur d’une déclaration pour la modifier.  Pour obtenir des raccourcis pour incrémenter ou décrémenter rapidement une valeur par , ou par unité, accédez à Modifier les valeurs de déclaration à l’aide de `0.1` `1` `10` `100` [raccourcis clavier.](#change-declaration-values-with-keyboard-shortcuts)  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Modification de la valeur d’une déclaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Modifier la valeur de la `border-bottom-style` déclaration  
:::image-end:::  

### <a name="change-declaration-values-with-keyboard-shortcuts"></a>Modifier les valeurs de déclaration à l’aide de raccourcis clavier  

Lors de la modification de la valeur d’une déclaration, vous pouvez utiliser les raccourcis clavier suivants pour incrémenter la valeur d’une valeur spécifique.  

*   Sélectionnez `Alt` + `Up` \(Windows, Linux\) ou `Option` + `Up` \(macOS\) pour incrémenter par `0.1` .  
*   Sélectionnez `Up` pour modifier la valeur par ou par si la valeur actuelle est entre et `1` `0.1` `-1` `1` .  
*   Sélectionnez `Shift` + `Up` pour incrémenter par `10` .  
*   Sélectionnez `Shift` + `Page Up` \(Windows, Linux\) ou `Shift` + `Command` + `Up` \(macOS\) pour incrémenter la valeur par `100` .  

La décrémentation fonctionne également.  Remplacez simplement chaque instance mentionnée `Up` ci-dessus par `Down` .  

### <a name="add-a-class-to-an-element"></a>Ajouter une classe à un élément  

Pour ajouter une classe à un élément, complétez les actions suivantes.  

1.  [Sélectionnez l’élément](#choose-an-element) dans **l’arborescence DOM.**  
1.  Choisissez **.cls**.  
1.  Entrez le nom de la classe dans la zone de texte Ajouter **une nouvelle** classe.  
1.  Sélectionnez `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Volet Classes d’éléments" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Volet **Classes d’éléments**  
:::image-end:::  

### <a name="toggle-a-class"></a>Faire basculer une classe  

Effectuer les actions suivantes pour activer ou désactiver une classe sur un élément.  

1.  [Sélectionnez l’élément](#choose-an-element) dans **l’arborescence DOM.**  
1.  Ouvrez le **volet Classes** d’éléments.  Accédez à [Ajouter une classe à un élément.](#add-a-class-to-an-element)  Sous la **zone de texte Ajouter une nouvelle** classe se trouverez toutes les classes appliquées à l’élément spécifique.  
1.  Basculez la case à cocher en regard de la classe que vous souhaitez activer ou désactiver.  

### <a name="add-a-style-rule"></a>Ajouter une règle de style  

Pour ajouter une nouvelle règle de style, complétez les actions suivantes.  

1.  [Sélectionnez un élément.](#choose-an-element)  
1.  Choose **New Style Rule** \( New Style Rule ![ ](../media/new-style-rule-icon.msft.png) \).  DevTools insère une nouvelle règle sous la **règle element.style.**  

> [!NOTE]
> Dans la figure suivante, DevTools ajoute la règle de style après avoir `h1.devsite-page-title` choisi Nouvelle règle de **style**.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Ajouter une nouvelle règle de style" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Ajouter une nouvelle règle de style  
:::image-end:::  

#### <a name="choose-which-stylesheet-to-add-a-rule-to"></a>Choisir la feuille de style à laquelle ajouter une règle  

Lorsque [vous ajoutez une nouvelle](#add-a-style-rule)règle de style, choisissez et maintenez la nouvelle règle de **style** \( Nouvelle règle de style \) pour choisir la feuille de style à laquelle ajouter la règle ![ de ](../media/new-style-rule-icon.msft.png) style.  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Choisir une feuille de style" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Choisir une feuille de style  
:::image-end:::  

#### <a name="add-a-style-rule-to-a-specific-location"></a>Ajouter une règle de style à un emplacement spécifique  

Pour ajouter une règle de style à un emplacement spécifique dans le panneau **Styles,** complétez les actions suivantes.  

1.  Pointez sur la règle de style qui se trouve directement au-dessus de l’endroit où vous souhaitez ajouter votre nouvelle règle de style.  
1.  [Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).  
1.  Choose **Insert Style Rule Below** \( Insert Style Rule Below icon ![ ](../media/new-style-rule-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insérer une règle de style en dessous" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Insérer une règle de style en dessous**  
:::image-end:::  

### <a name="reveal-the-more-actions-toolbar"></a>Révéler la barre d’outils Autres actions  

La **barre d’outils Autres actions** vous permet d’effectuer les actions suivantes.  

*   Insérez une règle de style directement sous celle sur qui vous vous concentrez.  
*   Ajoutez une déclaration , ou une déclaration à la règle de style sur qui `background-color` `color` vous vous `box-shadow` `text-shadow` concentrez.  

Effectuer les actions suivantes pour révéler la **barre d’outils Plus d’actions.**  

1.  Dans le panneau **Styles,** pointez sur une règle de style.  **D’autres actions** \( \) sont révélées dans le coin inférieur droit `...` de la section de règle de style.  
    
    > [!NOTE]
    > Dans la figure suivante, pointez sur la règle de style et d’autres actions sont révélés dans le coin inférieur droit de la `.header-holder.has-default-focus` section de règle de style. ****  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Révéler d’autres actions" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Révéler **d’autres actions** \( `...` \)  
    :::image-end:::  
    
1.  Pointez sur **plus d’actions** \( `...` \) pour révéler les actions mentionnées ci-dessus.  
    
    > [!NOTE]
    > **L’action Insérer une règle de style ci-dessous** s’est révélée après avoir survolé **d’autres actions.**  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Barre d’outils Autres actions" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       Barre **d’outils Autres actions**  
    :::image-end:::  
    
### <a name="toggle-a-declaration"></a>Faire basculer une déclaration  

Complétez les actions qui s’annoncent pour faire basculer une déclaration unique sur \(ou off\).  

1.  [Sélectionnez un élément.](#choose-an-element)  
1.  Dans le **volet Styles,** pointez sur la règle qui définit la déclaration.  Une case à cocher s’affiche en regard de chaque déclaration.  
1.  Cochez \(ou décochez\) la case à cocher en regard de la déclaration.  Lorsque vous décochez une déclaration, DevTools la croise pour indiquer qu’elle n’est plus active.  

> [!NOTE]
> Dans la figure suivante, la `margin-top` propriété de l’élément actuellement sélectionné a été éteinte.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Faire basculer une déclaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Faire basculer une déclaration  
:::image-end:::  

### <a name="add-a-background-color-declaration"></a>Ajouter une déclaration de couleur d’arrière-plan  

Effectuer les actions suivantes pour ajouter une `background-color` déclaration à un élément.  

1.  Pointez sur la règle de style à ajouter à `background-color` la déclaration.  
1.  [Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).  
1.  Choose **Add Background Color** \( Add Background Color icon ![ ](../media/add-background-color-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Ajouter une couleur d’arrière-plan" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Ajouter une couleur d’arrière-plan**  
:::image-end:::  

### <a name="add-a-color-declaration"></a>Ajouter une déclaration de couleur  

Effectuer les actions suivantes pour ajouter une `color` déclaration à un élément.  

1.  Pointez sur la règle de style à ajouter à `color` la déclaration.  
1.  [Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).  
1.  Choose **Add Color** \( Add Color icon ![ ](../media/add-color-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Ajouter une couleur" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Ajouter une couleur**  
:::image-end:::  

### <a name="add-a-box-shadow-declaration"></a>Ajouter une déclaration d’ombre de zone  

Effectuer les actions suivantes pour ajouter une `box-shadow` déclaration à un élément.  

1.  Pointez sur la règle de style à ajouter à `box-shadow` la déclaration.  
1.  [Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).  
1.  Choose **Add Box Shadow** \( Add Box Shadow icon ![ ](../media/add-box-shadow-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Ajouter une ombre de zone" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Ajouter une ombre de zone**  
:::image-end:::  

### <a name="add-a-text-shadow-declaration"></a>Ajouter une déclaration d’ombre de texte  

Effectuer les actions suivantes pour ajouter une `text-shadow` déclaration à un élément.  

1.  Pointez sur la règle de style à ajouter à `text-shadow` la déclaration.  
1.  [Révéler la **barre d’outils Actions** plus](#reveal-the-more-actions-toolbar).  
1.  Choose **Add Text Shadow** \( Add Text Shadow icon ![ ](../media/add-text-shadow-icon.msft.png) \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Ajouter une ombre de texte" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Ajouter une ombre de texte**  
:::image-end:::  

### <a name="change-colors-with-the-color-picker"></a>Modifier les couleurs avec le s sélectionneur de couleurs  

Le **s sélectionneur de couleurs** fournit une interface graphique graphique pour la modification `color` et les `background-color` déclarations.  

Effectuer les actions suivantes pour ouvrir le **s picker de couleur**.  

1.  [Sélectionnez un élément.](#choose-an-element)  
1.  Dans le **panneau Styles,** recherchez la déclaration , ou une déclaration similaire, que `color` vous `background-color` souhaitez modifier.  À gauche de la valeur , ou une valeur similaire, il existe un petit carré qui `color` est un aperçu de la `background-color` couleur.  
    
    > [!NOTE]
    > Dans la figure suivante, le petit carré à gauche est un `rgba(0, 0, 0, 0.7)` aperçu de cette couleur.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Aperçu de couleur" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Aperçu de couleur  
    :::image-end:::  
    
1.  Choisissez l’aperçu pour ouvrir le **s picker de couleurs.**  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="S sélectionneur de couleurs" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       S **sélectionneur de couleurs**  
    :::image-end:::  
    
La figure et la liste suivantes dcries de chacun des éléments d’interface utilisateur du s **picker de couleur**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="S sélectionneur de couleurs, annoté" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   Le **s sélectionneur de couleurs,** annoté  
:::image-end:::  

:::row:::
   :::column span="1":::
      1  
   :::column-end:::
   :::column span="1":::
      **Nuances**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      2  
   :::column-end:::
   :::column span="1":::
      **Eyedropper**  
   :::column-end:::
   :::column span="2":::
      Pour plus d’informations, accédez à l’exemple de couleur de la [page avec le eyedropper](#sample-a-color-off-the-page-with-the-eyedropper).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      3  
   :::column-end:::
   :::column span="1":::
      **Copier dans le Presse-papiers**  
   :::column-end:::
   :::column span="2":::
      Copiez **la valeur d’affichage** dans votre Presse-papiers.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      4  
   :::column-end:::
   :::column span="1":::
      **Valeur d’affichage**  
   :::column-end:::
   :::column span="2":::
      Représentation RGBA, HSLA ou Hex de la couleur.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      5  
   :::column-end:::
   :::column span="1":::
      **Palette de couleurs**  
   :::column-end:::
   :::column span="2":::
      Choisissez l’un des carrés pour changer la couleur de ce carré.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      6  
   :::column-end:::
   :::column span="1":::
      **Hue**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      7  
   :::column-end:::
   :::column span="1":::
      **Opacity**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      8  
   :::column-end:::
   :::column span="1":::
      **Commutateur valeur d’affichage**  
   :::column-end:::
   :::column span="2":::
      Bascule entre les représentations RGBA, HSLA et Hex de la couleur actuelle.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      9  
   :::column-end:::
   :::column span="1":::
      **S switcher de palette de couleurs**  
   :::column-end:::
   :::column span="2":::
      Basculez entre la [palette de][MaterialDesignColorSystem]conception de matériaux, une palette personnalisée ou une palette de couleurs de page.  DevTools génère la palette de couleurs de page en fonction des couleurs qu’il trouve dans vos feuilles de style.  
   :::column-end:::
:::row-end:::  

#### <a name="sample-a-color-off-the-page-with-the-eyedropper"></a>Exemple de couleur de la page avec le eyedropper  

Lorsque vous ouvrez le s **picker**de couleur, le **eyedropper** \( ![ Eyedropper ](../media/eyedropper-icon.msft.png) \) est sur par défaut.  Effectuer les actions suivantes pour modifier la couleur sélectionnée en une autre couleur sur la page.  

1.  Pointez sur la couleur cible dans la vue.  
1.  Choisissez de confirmer.  
    
    > [!NOTE]
    > Dans la figure suivante, le s **sélectionneur** de couleurs affiche une valeur de couleur actuelle de , qui est proche `rgba(0,0,0,0.7)` du noir.  La couleur spécifique doit changer pour la version du noir qui est actuellement mise en surbrillant dans la vue une fois que vous l’avez choisie.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Utilisation du eyedropper" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Utilisation du eyedropper  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes avec le menu de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Prise en main Avec l’affichage et la modification des | Documents Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Ajouter un pseudo-état à une classe : Prise en main avec l’affichage et la modification des CSS | Documents Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Afficher le CSS d’un élément : Prise en main avec l’affichage et la modification de CSS | Documents Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forcer Microsoft Edge devTools en mode Aperçu avant impression (type de média d’impression CSS) | Documents Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#reformat-a-minified-javascript-file-with-pretty-print "Reformater un fichier JavaScript minifié avec une impression assez grande : utilisez le débogger | Documents Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Système de couleurs - Conception des matériaux"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Modèle de zone | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Types de sélecteur : | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/reference) et est créée par [Kayce Basques][KayceBasques] \ (Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  