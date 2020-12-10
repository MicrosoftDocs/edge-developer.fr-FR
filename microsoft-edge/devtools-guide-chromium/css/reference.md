---
description: Découvrez de nouveaux flux de travail pour l’affichage et la modification de feuilles CSS dans Microsoft Edge DevTools.
title: Référence CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/19/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 83edc15549b4f8e668af99a4d95966736aaa0992
ms.sourcegitcommit: 3234b32e73c9f8362082d995296bd1c5e4286036
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/09/2020
ms.locfileid: "11204011"
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

# Référence CSS  

Découvrez les nouveaux flux de travail dans les informations de référence détaillées suivantes sur les fonctionnalités de Microsoft Edge DevTools liées à l’affichage et la modification de feuilles CSS.  

Pour en savoir plus sur les concepts de base, voir prendre en [main l’affichage et la modification de feuilles CSS][DevToolsCSSGetStarted] .  

## Sélectionner un élément  

Le panneau **éléments** de devtools vous permet d’afficher ou de modifier la feuille de style CSS d’un élément à la fois.  L’élément sélectionné est mis en surbrillance dans l' **arborescence DOM**.  Les styles de l’élément apparaissent dans le volet **styles** .  Voir [afficher la feuille de style en cascade (CSS) d’un élément][DevToolsCSSGetStartedTutorial] pour un didacticiel.  

> [!NOTE]
> Dans l’illustration suivante, l' `h1` élément qui est surligné dans l' **arborescence DOM** est l’élément sélectionné.  À droite, les styles de l’élément apparaissent dans le volet **styles** .  Sur la gauche, l’élément est mis en surbrillance dans la fenêtre d’affichage, mais uniquement dans la mesure où la souris pointe actuellement sur celle-ci dans l' **arborescence DOM**.  

:::image type="complex" source="../media/css-elements-styles-h1.msft.png" alt-text="Exemple d’élément sélectionné" lightbox="../media/css-elements-styles-h1.msft.png":::
   Exemple d’élément sélectionné  
:::image-end:::  

Utilisez l’une des actions suivantes pour sélectionner un élément.  

*   Dans votre fenêtre d’affichage, pointez sur l’élément, ouvrez le menu contextuel (cliquez avec le bouton droit sur \), puis sélectionnez **inspecter**.  
*   Dans devtools, choisissez **Sélectionner un élément** \ ( ![ Sélectionnez un élément ][ImageSelectAnElementIcon] \) ou `Control` + `Shift` + `C` \ (Windows, Linux \) ou `Command` + `Shift` + `C` \ (MacOS \), puis sélectionnez l’élément dans la fenêtre d’affichage.  
*   Dans DevTools, sélectionnez l’élément dans l' **arborescence DOM**.  
*   Dans DevTools, exécutez une requête telle que `document.querySelector('p')` dans la **console**, pointez sur le résultat, ouvrez le menu contextuel, puis cliquez sur **afficher dans le panneau éléments**.  

## Afficher les feuilles CSS  

### Affichage de la feuille de style externe dans laquelle une règle est définie  

Dans le volet **styles** , cliquez sur le lien en regard d’une règle CSS pour ouvrir la feuille de style externe qui définit la règle.  

S’il s’agit de minified, accédez à la section [rendre un fichier minified lisible][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> Dans l’illustration suivante, une fois que vous avez choisi, `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` vous êtes redirigé vers la ligne 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , où la `.content h1:first-of-type` règle CSS est définie.  

<!--todo:  replace "Master" phrasing in code snippet, if possible.  -->  

:::image type="complex" source="../media/css-elements-styles-h1-highlight.msft.png" alt-text="Affichage de la feuille de style dans laquelle une règle est définie" lightbox="../media/css-elements-styles-h1-highlight.msft.png":::
  Affichage de la feuille de style dans laquelle une règle est définie  
:::image-end:::  

### Afficher uniquement les feuilles CSS appliquées actuellement à un élément  

L’onglet **styles** affiche toutes les règles qui s’appliquent à un élément, y compris les déclarations qui ont été remplacées.  Lorsque vous n’êtes pas intéressé par des déclarations substituées, utilisez l’onglet **calculé** pour afficher uniquement les feuilles CSS qui sont réellement appliquées à un élément.  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Accédez à l’onglet **calculé** dans le panneau **éléments** .  

> [!NOTE]
> Dans le cas d’une fenêtre DevTools large, l’onglet **calculé** n’existe pas.  Le contenu de l’onglet **calculé** est affiché dans l’onglet **styles** .  

Les propriétés héritées sont opaques.  Cochez la case **Afficher tout** pour afficher toutes les valeurs héritées.  

> [!NOTE]
> Dans l’illustration suivante, l’onglet **calculé** montre les propriétés CSS qui sont appliquées à l’élément actuellement sélectionné `h1` .  

:::image type="complex" source="../media/css-elements-computed-h1.msft.png" alt-text="Onglet calculé" lightbox="../media/css-elements-computed-h1.msft.png":::
   Onglet **calculé**  
:::image-end:::  

### Afficher les propriétés CSS par ordre alphabétique  

Utilisez l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Afficher les propriétés CSS héritées  

Cochez la case **Afficher tout** dans l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Afficher le modèle de boîte pour un élément  

Pour afficher [le modèle de zone][MDNBoxModel] d’un élément, accédez à l’onglet **styles** .  Si votre fenêtre DevTools est étroite, le diagramme de **modèle de cadre** est en bas de l’onglet.  

Pour modifier une valeur, sélectionnez et modifiez sur une valeur.  

> [!NOTE]
> Dans l’illustration suivante, le diagramme de **modèle de cadre** sous l’onglet **styles** affiche le modèle de zone de l’élément actuellement sélectionné `h1` .  

:::image type="complex" source="../media/css-elements-styles-h1-2.msft.png" alt-text="Diagramme de modèle de cadre" lightbox="../media/css-elements-styles-h1-2.msft.png":::
   Diagramme de **modèle de cadre**  
:::image-end:::  

### Rechercher et filtrer la CSS d’un élément  

Utilisez la zone de texte **filtre** des **styles** et des onglets **calculés** pour rechercher des propriétés ou des valeurs CSS spécifiques.  

Pour effectuer une recherche dans les propriétés héritées dans l’onglet **calculé** , activez la case à cocher **Afficher tout** .  

> [!NOTE]
> Dans l’illustration suivante, l’onglet **styles** est filtré pour afficher uniquement les règles qui incluent la requête de recherche `color` .  

:::image type="complex" source="../media/css-elements-styles-filter-color.msft.png" alt-text="Filtrer l’onglet styles" lightbox="../media/css-elements-styles-filter-color.msft.png":::
   Filtrer l’onglet **styles**  
:::image-end:::  

> [!NOTE]
> Dans l’illustration suivante, l’onglet **calculé** est filtré pour afficher uniquement les déclarations qui incluent la requête de recherche `100%` .  

:::image type="complex" source="../media/css-elements-computed-filter-100.msft.png" alt-text="Filtrer l’onglet calculé" lightbox="../media/css-elements-computed-filter-100.msft.png":::
   Filtrer l’onglet **calculé**  
:::image-end:::  

### Basculer une pseudo-classe  

Effectuez les opérations suivantes pour basculer une pseudo-classe comme `:active` , `:focus` , `:hover` ou `:visited` .  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le panneau **éléments** , accédez à l’onglet **styles** .  
1.  Choisissez **: HOV**.  
1.  Vérifiez la pseudo-classe que vous souhaitez activer.  

> [!NOTE]
> Dans l’illustration suivante, faites basculer la `:hover` Pseudo-classe.  Dans la fenêtre d’affichage, vérifiez que la `background-color: cornflowerblue` déclaration est appliquée à l’élément, même si celui-ci n’est pas en cours de pointage.  

:::image type="complex" source="../media/css-elements-styles-hov-hover.msft.png" alt-text="Basculer entre la pseudo-classe Hover" lightbox="../media/css-elements-styles-hov-hover.msft.png":::
   Activer/désactiver la `:hover` Pseudo-classe  
:::image-end:::  

Pour un didacticiel interactif, accédez à [Ajouter un PseudoState à une classe][DevToolsCSSGetStartedAddPseudoState].  

### Afficher une page en mode d’impression  

Effectuez les opérations suivantes pour afficher une page en mode d’impression.  

1.  [Ouvrir le menu de commandes][DevToolsCommandMenu].  
1.  Commencez à taper `Rendering` et sélectionnez `Show Rendering` .  
1.  Dans la liste déroulante **émuler les contenus multimédias CSS** , sélectionnez **Imprimer**.  

### Afficher les feuilles CSS utilisées et inutilisées avec l’onglet couverture  

L’onglet couverture vous indique la feuille de style en cascade qui est utilisée réellement par une page.  

1.  `Control` + `Shift` + `P` Dans le menu contextuel, sélectionnez \ (Windows, Linux \) ou `Command` + `Shift` + `P` \ (MacOS \), tandis que devtools est sur le point d' [ouvrir le menu de commandes][DevToolsCommandMenu].  
1.  Commencez à taper `coverage` et sélectionnez **afficher la couverture**.  L’onglet couverture apparaît.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-command-menu-coverage.msft.png" alt-text="Ouverture de l’onglet couverture dans le menu de commandes" lightbox="../media/css-console-command-menu-coverage.msft.png":::
             Ouvrir l’onglet **couverture** dans le **menu de commandes**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/css-console-qs-coverage-empty.msft.png" alt-text="Onglet couverture" lightbox="../media/css-console-qs-coverage-empty.msft.png":::
             Onglet **couverture**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Sélectionnez **Démarrer l’instrumentation et actualiser la page** \ ( ![ commencer l’instrumentation et actualiser la page ][ImageRefreshIcon] \).  La page actualise et l’onglet couverture fournit une vue d’ensemble de la quantité CSS \ (et JavaScript \) utilisée à partir de chaque fichier chargé par le navigateur.  Green représente les feuilles CSS utilisées.  Rouge représente les feuilles CSS inutilisées.  
    
    :::image type="complex" source="../media/css-console-qs-coverage-run.msft.png" alt-text="Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)" lightbox="../media/css-console-qs-coverage-run.msft.png":::
       Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS \ (et JavaScript \)  
    :::image-end:::  

1.  Choisissez un fichier CSS pour afficher une répartition ligne par ligne de la feuille de style CSS qu’il utilise.  
    
    > [!NOTE]
    > Dans l’illustration suivante, les lignes 145 à 147 et 149 à 151 `b66bc881.site-ltr.css` sont inutilisées, tandis que les lignes 163 à 166 sont utilisées.  
    
    :::image type="complex" source="../media/css-sources-css-coverage.msft.png" alt-text="Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées" lightbox="../media/css-sources-css-coverage.msft.png":::
       Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées  
    :::image-end:::  
    
### Forcer le mode aperçu avant impression  

Pour plus d’DevTools, voir [mode aperçu avant impression][DevToolsCssPrintPreview].  

## Modifier CSS  

<!-- todo s/CSS declaration/declaration/ -->  

### Ajouter une déclaration CSS à un élément  

L’ordre des déclarations affecte la façon dont un élément est stylisé, utilisez la liste suivante pour vous aider à ajouter des déclarations de différentes manières.  

*   [Ajoutez une déclaration inline](#add-an-inline-declaration).  Équivalent à l’ajout d’un `style` attribut au code HTML d’un élément.  
*   [Ajoutez une déclaration à une règle de style](#add-a-declaration-to-a-style-rule).  

**Quel flux de travail devez-vous utiliser?** Pour la plupart des scénarios, vous souhaiterez probablement utiliser le flux de travail de déclaration inline.  Les déclarations Inline sont d’une plus grande spécificité par rapport aux déclarations externes, de sorte que le flux de travail intraligne vérifie que les modifications entrent en vigueur dans votre élément attendu.  Pour plus d’informations sur la spécificité, accédez à [types de sélecteur][MDNSelectorTypes].  

Si vous déboguez des styles de l’élément et que vous devez spécifiquement tester ce qui se produit quand une déclaration est définie à des emplacements différents, utilisez l’autre flux de travail.  

#### Ajouter une déclaration en ligne  

Complétez les actions suivantes pour ajouter une déclaration inline.  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le volet **styles** , choisissez entre les crochets de la section **élément. style** .  Le curseur s’attache pour vous permettre d’entrer du texte.  
1.  Entrez un nom de propriété et sélectionnez `Enter` .  
1.  Entrez une valeur valide pour cette propriété, puis sélectionnez `Enter` .  Dans l' **arborescence DOM**, vérifiez qu’un `style` attribut a été ajouté à l’élément.  

> [!NOTE]
> Dans l’illustration suivante, les `margin-top` `background-color` Propriétés et ont été appliquées à l’élément sélectionné.  Dans l' **arborescence DOM** , assurez-vous que les déclarations sont reflétées dans l' `style` attribut d’un élément.  

:::image type="complex" source="../media/css-elements-styles-margin-top-background-color.msft.png" alt-text="Ajouter des déclarations en ligne" lightbox="../media/css-elements-styles-margin-top-background-color.msft.png":::
   Ajouter des déclarations en ligne  
:::image-end:::  

#### Ajouter une déclaration à une règle de style  

Pour ajouter une déclaration à une règle de style existante, procédez comme suit.  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le volet **styles** , choisissez entre les crochets de la règle de style auxquelles vous souhaitez ajouter la déclaration.  Le curseur s’attache pour vous permettre d’entrer du texte.  
1.  Entrez un nom de propriété et sélectionnez `Enter` .  
1.  Entrez une valeur valide pour cette propriété, puis sélectionnez `Enter` .  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style.msft.png" alt-text="Ajout d’une déclaration à une règle de style" lightbox="../media/css-elements-styles-border-bottom-style.msft.png":::
   Ajouter la `border-bottom-style:groove` déclaration à une règle de style  
:::image-end:::  

### Modifier le nom ou la valeur d’une déclaration  

Choisissez et modifiez le nom ou la valeur d’une déclaration pour la modifier.  Voir [modifier les valeurs de déclaration avec des raccourcis clavier](#change-declaration-values-with-keyboard-shortcuts) pour les raccourcis permettant d’incrémenter ou de décrémenter rapidement une valeur par `0.1` ,, ou par `1` `10` `100` unités.  

:::image type="complex" source="../media/css-elements-styles-border-bottom-style-dropdown.msft.png" alt-text="Modification de la valeur d’une déclaration" lightbox="../media/css-elements-styles-border-bottom-style-dropdown.msft.png":::
   Modifiez la valeur de la `border-bottom-style` déclaration.  
:::image-end:::  

### Modification des valeurs de déclaration avec les raccourcis clavier  

Lors de la modification de la valeur d’une déclaration, vous pouvez utiliser les raccourcis clavier suivants pour incrémenter la valeur à un certain montant.  

*   Sélectionnez `Alt` + `Up` \ (Windows, Linux \) ou `Option` + `Up` \ (MacOS \) `0.1` .  
*   `Up`Pour modifier la valeur par `1` ou `0.1` si la valeur actuelle est comprise entre `-1` et `1` .  
*   Sélectionner `Shift` + `Up` pour incrémenter par `10` .  
*   Sélectionnez `Shift` + `Page Up` \ (Windows, Linux \) ou `Shift` + `Command` + `Up` \ (MacOS \) pour incrémenter la valeur `100` .  

La décrémentation fonctionne également.  Il vous suffit de remplacer chaque instance décrite `Up` plus haut par `Down` .  

### Ajouter une classe à un élément  

Pour ajouter une classe à un élément, procédez comme suit.  

1.  [Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.  
1.  Sélectionnez **. CLS**.  
1.  Entrez le nom de la classe dans la zone de texte **Ajouter une nouvelle classe** .  
1.  Sélectionnez `Enter` .  

:::image type="complex" source="../media/css-elements-styles-filter-classes.msft.png" alt-text="Volet classes d’éléments" lightbox="../media/css-elements-styles-filter-classes.msft.png":::
   Volet **classes d’éléments**  
:::image-end:::  

### Basculer une classe  

Pour activer ou désactiver une classe sur un élément, procédez comme suit.  

1.  [Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.  
1.  Ouvrez le volet **classes d’éléments** .  Voir [Ajouter une classe à un élément](#add-a-class-to-an-element).  Sous la zone de texte **Ajouter une nouvelle classe** figurent toutes les classes qui sont appliquées à l’élément spécifique.  
1.  Activez/désactivez la case à cocher en regard de la classe que vous souhaitez activer ou désactiver.  

### Ajouter une règle de style  

Complétez les actions suivantes pour ajouter une nouvelle règle de style.  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Cliquez sur **nouvelle règle de style** \ ( ![ nouvelle règle de style ][ImageNewStyleRuleIcon] \).  DevTools insère une nouvelle règle sous la règle **élément. style** .  

> [!NOTE]
> Dans l’illustration suivante, DevTools ajoute la `h1.devsite-page-title` règle de style après que vous avez choisi **nouvelle règle de style**.  

:::image type="complex" source="../media/css-elements-styles-style-new.msft.png" alt-text="Ajouter une nouvelle règle de style" lightbox="../media/css-elements-styles-style-new.msft.png":::
   Ajouter une nouvelle règle de style  
:::image-end:::  

#### Sélectionner la feuille de style à laquelle ajouter une règle  

Lors de l' [Ajout d’une nouvelle règle de style](#add-a-style-rule), choisissez une **nouvelle règle de style** et maintenez-la enfoncée ![ ][ImageNewStyleRuleIcon] .  

:::image type="complex" source="../media/css-elements-styles-style-new-select-existing.msft.png" alt-text="Sélectionner une feuille de style" lightbox="../media/css-elements-styles-style-new-select-existing.msft.png":::
   Sélectionner une feuille de style  
:::image-end:::  

#### Ajouter une règle de style à un emplacement spécifique  

Pour ajouter une règle de style à un emplacement spécifique, accédez à l’onglet **styles** , procédez comme suit.  

1.  Pointez sur la règle de style qui se trouve directement au-dessus de l’endroit où vous souhaitez ajouter votre nouvelle règle de style.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Choisissez **Insérer une règle de style sous** \ ( ![ Insérer une règle de style ci-dessous ][ImageNewStyleRuleIcon] ).  

:::image type="complex" source="../media/css-elements-styles-insert-style-rule-below.msft.png" alt-text="Insérer une règle de style en dessous" lightbox="../media/css-elements-styles-insert-style-rule-below.msft.png":::
   **Insérer une règle de style en dessous**  
:::image-end:::  

### Afficher la barre d’outils plus d’actions  

La barre d’outils **plus d’actions** vous permet d’effectuer les actions suivantes.  

*   Insérez une règle de style juste en dessous de celle qui vous intéresse.  
*   Ajoutez une `background-color` `color` `box-shadow` `text-shadow` déclaration à la règle de style sur laquelle vous êtes prioritaire.  

Effectuez les opérations suivantes pour afficher la barre d’outils **plus d’actions** .  

1.  Dans l’onglet **styles** , pointez sur une règle de style.  D' **autres actions** ( `...` \) sont affichées dans le coin inférieur droit de la section règle de style.  
    
    > [!NOTE]
    > Dans l’illustration suivante, placez le pointeur de la souris sur la `.header-holder.has-default-focus` règle de style et d' **autres actions** sont affichées dans le coin inférieur droit de la section règle de style.  
    
    :::image type="complex" source="../media/css-elements-styles-new-rule-styles.msft.png" alt-text="Afficher d’autres actions" lightbox="../media/css-elements-styles-new-rule-styles.msft.png":::
       Afficher d' **autres actions** `...`  
    :::image-end:::  
    
1.  Placez le pointeur sur **plus d’actions** `...` pour afficher les actions mentionnées ci-dessus.  
    
    > [!NOTE]
    > L’action **Insérer une règle de style ci-dessous** apparaît après avoir pointé sur **plus d’actions**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png" alt-text="Barre d’outils plus d’actions" lightbox="../media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png":::
       Barre d’outils **plus d’actions**  
    :::image-end:::  
    
### Basculer une déclaration  

Complétez les actions folllwoing pour basculer une déclaration unique sur \ (ou désactivé).  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le volet **styles** , pointez sur la règle qui définit la déclaration.  Une case à cocher est affichée en regard de chaque déclaration.  
1.  Activez/désactivez la case à cocher en regard de la déclaration.  Lorsque vous décochez une déclaration, DevTools la traverse pour indiquer qu’elle n’est plus active.  

> [!NOTE]
> Dans l’illustration suivante, la `margin-top` propriété de l’élément actuellement sélectionné a été activée.  

:::image type="complex" source="../media/css-elements-styles-rule-deactivated.msft.png" alt-text="Basculer une déclaration" lightbox="../media/css-elements-styles-rule-deactivated.msft.png":::
   Basculer une déclaration  
:::image-end:::  

### Ajouter une déclaration couleur d’arrière-plan  

Pour ajouter une `background-color` déclaration à un élément, procédez comme suit.  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `background-color` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Sélectionnez **Ajouter une couleur d’arrière-plan** \ ( ![ icône couleur d’arrière-plan ][ImageAddBackgroundColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-background-color.msft.png" alt-text="Ajouter une couleur d’arrière-plan" lightbox="../media/css-elements-styles-rule-add-background-color.msft.png":::
   **Ajouter une couleur d’arrière-plan**  
:::image-end:::  

### Ajouter une déclaration de couleur  

Pour ajouter une `color` déclaration à un élément, procédez comme suit.  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `color` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Sélectionnez **Ajouter une couleur** \ ( ![ icône Ajouter une couleur ][ImageAddColorIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-color.msft.png" alt-text="Ajouter de la couleur" lightbox="../media/css-elements-styles-rule-add-color.msft.png":::
   **Ajouter de la couleur**  
:::image-end:::  

### Ajouter une déclaration d’ombre Box  

Pour ajouter une `box-shadow` déclaration à un élément, procédez comme suit.  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `box-shadow` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Sélectionnez **Ajouter une ombre de zone** \ ( ![ icône d’ombre dans la zone Ajouter ][ImageAddBoxShadowIcon] \).  

:::image type="complex" source="../media/css-elements-styles-rule-add-box-shadow.msft.png" alt-text="Ajouter une ombre de zone" lightbox="../media/css-elements-styles-rule-add-box-shadow.msft.png":::
   **Ajouter une ombre de zone**  
:::image-end:::  

### Ajouter une déclaration d’ombre textuelle  

Pour ajouter une `text-shadow` déclaration à un élément, procédez comme suit.  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `text-shadow` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Cliquez sur **Ajouter une ombre de texte** \ ( ![ icône Ajouter une ombre de texte ][ImageAddTextShadowIcon] ).  

:::image type="complex" source="../media/css-elements-styles-rule-add-text-shadow.msft.png" alt-text="Ajouter une ombre de texte" lightbox="../media/css-elements-styles-rule-add-text-shadow.msft.png":::
   **Ajouter une ombre de texte**  
:::image-end:::  

### Changer les couleurs à l’aide du sélecteur de couleurs  

Le **Sélecteur de couleurs** fournit une interface utilisateur pour le changement `color` et la `background-color` déclaration.  

Procédez comme suit pour ouvrir le **Sélecteur de couleurs**.  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans l’onglet **styles** , recherchez la `color` `background-color` déclaration, ou similaire, que vous voulez modifier.  À gauche de la `color` valeur, `background-color` ou similaire, il existe un petit carré, qui est un aperçu de la couleur.  
    
    > [!NOTE]
    > Dans l’illustration ci-dessous, le petit carré à gauche de `rgba(0, 0, 0, 0.7)` est un aperçu de cette couleur.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-overlay-color-box.msft.png" alt-text="Aperçu de couleur" lightbox="../media/css-elements-styles-rule-overlay-color-box.msft.png":::
       Aperçu de couleur  
    :::image-end:::  
    
1.  Sélectionnez l’Aperçu pour ouvrir le **Sélecteur de couleurs**.  
    
    :::image type="complex" source="../media/css-elements-styles-rule-color-picker.msft.png" alt-text="Sélecteur de couleurs" lightbox="../media/css-elements-styles-rule-color-picker.msft.png":::
       **Sélecteur de couleurs**  
    :::image-end:::  
    
La figure et la liste suivantes décrit de chaque élément d’interface utilisateur du **Sélecteur de couleurs**.  

:::image type="complex" source="../media/css-elements-styles-rule-color-picker-annotated.msft.png" alt-text="Sélecteur de couleurs, annoté" lightbox="../media/css-elements-styles-rule-color-picker-annotated.msft.png":::
   **Sélecteur de couleurs**, annoté  
:::image-end:::  

:::row:::
   :::column span="1":::
      1  
   :::column-end:::
   :::column span="1":::
      **Niveaux**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      deuxième  
   :::column-end:::
   :::column span="1":::
      **Compte**  
   :::column-end:::
   :::column span="2":::
      Pour plus d’informations, accédez à l' [exemple de couleur de la page à l’aide du](#sample-a-color-off-the-page-with-the-eyedropper)compte-gouttes.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      3D  
   :::column-end:::
   :::column span="1":::
      **Copier dans le Presse-papiers**  
   :::column-end:::
   :::column span="2":::
      Copiez la **valeur d’affichage** dans le presse-papiers.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      n°4  
   :::column-end:::
   :::column span="1":::
      **Valeur d’affichage**  
   :::column-end:::
   :::column span="2":::
      La représentation RVBA, HSLA ou Hex de la couleur.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      n°5  
   :::column-end:::
   :::column span="1":::
      **Palette de couleurs**  
   :::column-end:::
   :::column span="2":::
      Choisissez l’un des carrés pour changer la couleur en carré.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      6  
   :::column-end:::
   :::column span="1":::
      **Teinte**  
   :::column-end:::
   :::column span="2":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      6  
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
      version8  
   :::column-end:::
   :::column span="1":::
      **Sélecteur de valeurs d’affichage**  
   :::column-end:::
   :::column span="2":::
      Basculer entre les représentations RVBA, HSLA et Hex de la couleur actuelle.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      09  
   :::column-end:::
   :::column span="1":::
      **Sélecteur de palettes de couleurs**  
   :::column-end:::
   :::column span="2":::
      Basculer entre la [palette de création matérielle][MaterialDesignColorSystem], une palette personnalisée ou une palette de couleurs de page.  DevTools génère la palette de couleurs de page en fonction des couleurs qu’il trouve dans vos feuilles de style.  
   :::column-end:::
:::row-end:::  

#### Exemple de couleur de la page avec le compte-gouttes  

Lorsque vous ouvrez le **Sélecteur de couleurs**, la **pipette** \ ( ![ pipette ][ImageEyedropperIcon] \) est activée par défaut.  Procédez comme suit pour modifier la couleur sélectionnée sur une autre couleur de la page.  

1.  Placez le pointeur de la souris sur la couleur cible dans la fenêtre d’affichage.  
1.  Confirmez votre choix.  
    
    > [!NOTE]
    > Dans l’illustration ci-dessous, le **Sélecteur de couleurs** affiche une valeur de couleur actuelle de `rgba(0,0,0,0.7)` , qui est proche de noir.  La couleur spécifique doit être modifiée en une version de noir actuellement mise en surbrillance dans la fenêtre d’affichage, une fois que vous avez choisi celle-ci.  
    
    :::image type="complex" source="../media/css-color-picker-eye-dropper.msft.png" alt-text="Utiliser le compte-gouttes" lightbox="../media/css-color-picker-eye-dropper.msft.png":::
       Utiliser le compte-gouttes  
    :::image-end:::  
    
<!--todo:  add the section on the Angle clock section for What's New 88.  -->  

## Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- image links -->  

[ImageAddBackgroundColorIcon]: ../media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: ../media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: ../media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: ../media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: ../media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: ../media/select-an-element-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Exécuter des commandes à l’aide du menu de commandes de Microsoft Edge DevTools | Documents Microsoft"  
[DevToolsCSSGetStarted]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevToolsCSSGetStartedAddPseudoState]: ../css/index.md#add-a-pseudostate-to-a-class "Ajouter un PseudoState à une classe: Familiarisez-vous avec l’affichage et la modification d’une feuille de style CSS | Documents Microsoft"  
[DevToolsCSSGetStartedTutorial]: ../css/index.md#view-the-css-for-an-element "Affichage de la feuille de style en cascade (CSS) d’un élément: commencez à afficher et modifier des feuilles CSS | Documents Microsoft"  
[DevToolsCssPrintPreview]: ../css/print-preview.md "Forcez Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type) | Documents Microsoft"  
[DevToolsJavascriptReferenceFormat]: ../javascript/reference.md#make-a-minified-file-readable "Faire une référence de débogage de fichier minified-JavaScript Documents Microsoft"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Conception système couleur-matériau"  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Le modèle de zone | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Types de sélecteur-spécificité | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/css/reference) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  