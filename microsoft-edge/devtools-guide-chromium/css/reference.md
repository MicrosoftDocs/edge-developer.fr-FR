---
title: Référence CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 4f0370b83d8c939476a1ed378dbdf750101c9527
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843966"
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



Découvrez de nouveaux flux de travail dans cette référence complète des fonctionnalités de Microsoft Edge DevTools liées à l’affichage et à la modification de feuilles CSS.  

Pour en savoir plus sur les concepts de base, voir prendre en [main l’affichage et la modification de feuilles CSS][DevToolsCSSGetStarted] .  

## Sélectionner un élément   

Le panneau **éléments** de devtools vous permet d’afficher ou de modifier la feuille de style CSS d’un élément à la fois.  L’élément sélectionné est mis en surbrillance dans l' **arborescence DOM**.  Les styles de l’élément apparaissent dans le volet **styles** .  Voir [afficher la feuille de style en cascade (CSS) d’un élément][DevToolsCSSGetStartedTutorial] pour un didacticiel.  

> [!NOTE]
> Dans la [figure 1](#figure-1), l' `h1` élément qui est surligné dans l' **arborescence DOM** est l’élément sélectionné.  À droite, les styles de l’élément apparaissent dans le volet **styles** .  Sur la gauche, l’élément est mis en surbrillance dans la fenêtre d’affichage, mais uniquement dans la mesure où la souris pointe actuellement sur celle-ci dans l' **arborescence DOM**.  

> ##### Figure1  
> Exemple d’élément sélectionné  
> ![Exemple d’élément sélectionné][ImageSelectedElement]  

Il existe de nombreuses façons de sélectionner un élément:  

*   Dans votre fenêtre d’affichage, cliquez avec le bouton droit sur l’élément, puis sélectionnez **inspecter**.  
*   Dans devtools, cliquez sur **Sélectionner un élément** ![ Sélectionnez un élément ][ImageSelectAnElementIcon] ou appuyez sur `Control` + `Shift` + `C` \ (Windows \) ou `Command` + `Shift` + `C` \ (MacOS \), puis cliquez sur l’élément dans la fenêtre d’affichage.  
*   Dans DevTools, cliquez sur l’élément dans l' **arborescence DOM**.  
*   Dans DevTools, exécutez une requête telle que `document.querySelector('p')` dans la **console**, cliquez avec le bouton droit sur le résultat, puis sélectionnez **afficher dans le panneau éléments**.  

## Afficher les feuilles CSS   

### Affichage de la feuille de style externe dans laquelle une règle est définie   

Dans le volet **styles** , cliquez sur le lien en regard d’une règle CSS pour ouvrir la feuille de style externe qui définit la règle.  

Si la feuille de style est minified, voir [rendre un fichier minified lisible][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> Dans la [figure 2](#figure-2), `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` un clic vous permet d’accéder à la ligne 2 de `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , où la `.content h1:first-of-type` règle CSS est définie.  

> ##### Figure 2  
> Affichage de la feuille de style dans laquelle une règle est définie  
> ![Affichage de la feuille de style dans laquelle une règle est définie][ImageViewRuleStylesheet]  

### Afficher uniquement les feuilles CSS appliquées actuellement à un élément   

L’onglet **styles** affiche toutes les règles qui s’appliquent à un élément, y compris les déclarations qui ont été remplacées.  Lorsque vous n’êtes pas intéressé par des déclarations substituées, utilisez l’onglet **calculé** pour afficher uniquement les feuilles CSS qui sont réellement appliquées à un élément.  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Accédez à l’onglet **calculé** dans le panneau **éléments** .  

> [!NOTE]
> Dans le cas d’une fenêtre DevTools large, l’onglet **calculé** n’existe pas.  Le contenu de l’onglet **calculé** est affiché dans l’onglet **styles** .  

Les propriétés héritées sont opaques.  Cochez la case **Afficher tout** pour afficher toutes les valeurs héritées.  

> [!NOTE]
> Dans la [figure 3](#figure-3), l’onglet **calculé** montre les propriétés CSS qui sont appliquées à l’élément actuellement sélectionné `h1` .  

> ##### Figure3  
> Onglet **calculé**  
> ![Onglet calculé][ImageComputedTab]  

### Afficher les propriétés CSS par ordre alphabétique   

Utilisez l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Afficher les propriétés CSS héritées   

Cochez la case **Afficher tout** dans l’onglet **calculé** .  Voir [afficher uniquement la feuille de style CSS qui est réellement appliquée à un élément](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Afficher le modèle de boîte pour un élément   

Pour afficher [le modèle de zone][MDNBoxModel] d’un élément, accédez à l’onglet **styles** .  Si votre fenêtre DevTools est étroite, le diagramme de **modèle de cadre** est en bas de l’onglet.  

Pour modifier une valeur, double-cliquez dessus.  

> [!NOTE]
> Dans la [figure 4](#figure-4), le diagramme de **modèle de cadre** sous l’onglet **styles** montre le modèle de zone de l’élément actuellement sélectionné `h1` .  

> ##### Figure 4  
> Diagramme de **modèle de cadre**  
> ![Diagramme de modèle de cadre][ImageBoxModel]  

### Rechercher et filtrer la CSS d’un élément   

Utilisez la zone de texte **filtre** des **styles** et des onglets **calculés** pour rechercher des propriétés ou des valeurs CSS spécifiques.  

Pour effectuer une recherche dans les propriétés héritées dans l’onglet **calculé** , activez la case à cocher **Afficher tout** .  

> [!NOTE]
> Dans la [figure 5](#figure-5), l’onglet **styles** est filtré pour afficher uniquement les règles qui incluent la requête de recherche `color` .  

> ##### Figure 5  
> Filtrage de l’onglet **styles**  
> ![Filtrage de l’onglet styles][ImageStylesFilter]  

> [!NOTE]
> Dans la [figure 6](#figure-6), l’onglet **calculé** est filtré pour afficher uniquement les déclarations qui incluent la requête de recherche `100%` .  

> ##### Figure 6  
> Filtrage de l’onglet **calculé**  
> ![Filtrage de l’onglet calculé][ImageComputerFilter]  

### Basculer une pseudo-classe   

Pour basculer une pseudo-classe comme `:active` , `:focus` , `:hover` ou `:visited` :  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le panneau **éléments** , accédez à l’onglet **styles** .  
1.  Cliquez sur **: HOV**.  
1.  Vérifiez la pseudo-classe que vous souhaitez activer.  

> [!NOTE]
> Dans la [figure 7](#figure-7), activez la `:hover` Pseudo-classe.  Dans la fenêtre d’affichage, vérifiez que la `background-color: cornflowerblue` déclaration est appliquée à l’élément, même si celui-ci n’est pas en cours de pointage.  

> ##### Figure 7  
> Bascule de la `:hover` Pseudo-classe  
> ![Activation/désactivation de la pseudo-classe Hover][ImagePseudoClass]  

Pour un didacticiel interactif, voir [Ajouter un PseudoState à une classe][DevToolsCSSGetStartedAddPseudoState] . 

### Afficher une page en mode d’impression   

Pour afficher une page en mode impression:  
1.  [Ouvrir le menu de commandes][DevToolsCommandMenu].  
1.  Commencez à taper `Rendering` et sélectionnez `Show Rendering` .  
1.  Dans la liste déroulante **émuler le média CSS** , sélectionnez **Imprimer**.  

### Afficher les feuilles CSS utilisées et inutilisées avec l’onglet couverture   

L’onglet couverture vous indique la feuille de style en cascade qui est utilisée réellement par une page.  

1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) alors que devtools est sur le point d’ouvrir le menu de commandes.  
1.  Commencez à taper `coverage` et sélectionnez **afficher la couverture**.  L’onglet couverture apparaît.  
    
    > ##### Figure8  
    > Ouverture de l’onglet couverture dans le menu de commandes  
    > ![Ouverture de l’onglet couverture dans le menu de commandes][ImageCommandMenu]  
    
    > ##### Figure9  
    > Onglet couverture  
    > ![Onglet couverture][ImageCoverageEmpty]  
    
1.  Cliquez sur **Démarrer la couverture d’instrumentation et actualiser la page** de démarrage de l' ![ instrumentation et actualiser la page ][ImageRefreshIcon] .  La page actualise et l’onglet couverture fournit une vue d’ensemble de la quantité CSS \ (et JavaScript \) utilisée à partir de chaque fichier chargé par le navigateur.  Green représente les feuilles CSS utilisées.  Rouge représente les feuilles CSS inutilisées.  
    
    > ##### Figure10  
    > Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)  
    > ![Vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)][ImageCoverageOverview]  

1.  Cliquez sur un fichier CSS pour afficher une répartition ligne par ligne de la feuille de style CSS qu’il utilise.  
    
    > [!NOTE]
    > Dans la [figure 11](#figure-11), les lignes 145 à 147 et 149 à 151 `b66bc881.site-ltr.css` sont inutilisées, alors que les lignes 163 à 166 sont utilisées.  
    
    > ##### Figure11  
    > Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées  
    > ![Une répartition ligne par ligne de feuilles CSS utilisées et inutilisées][ImageCoverageDetail]  
    
### Forcer le mode aperçu avant impression   

Pour plus d’DevTools, voir [mode aperçu avant impression][DevToolsCssPrintPreview].  

## Modifier CSS   

<!-- todo s/CSS declaration/declaration/ -->  

### Ajouter une déclaration CSS à un élément   

Dans la mesure où l’ordre des déclarations affecte la façon dont un élément est stylisé, vous pouvez ajouter des déclarations de différentes manières:  

*   [Ajoutez une déclaration inline](#add-an-inline-declaration).  Équivalent à l’ajout d’un `style` attribut au code HTML d’un élément.  
*   [Ajoutez une déclaration à une règle de style](#add-a-declaration-to-a-style-rule).  

**Quel flux de travail devez-vous utiliser?** Pour la plupart des scénarios, vous souhaiterez probablement utiliser le flux de travail de déclaration inline.  Les déclarations Inline ont une spécificité supérieure à celle d’un élément externe, de sorte que le flux de travail intraligne vérifie que les modifications entrent en vigueur dans l’élément comme prévu.  Pour plus d’informations sur les [types de sélecteur][MDNSelectorTypes] , voir spécificité.  

Si vous déboguez des styles de l’élément et que vous devez spécifiquement tester ce qui se produit quand une déclaration est définie à des emplacements différents, utilisez l’autre flux de travail.  

#### Ajouter une déclaration en ligne   

Pour ajouter une déclaration en ligne:  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le volet **styles** , cliquez entre les crochets de la section **élément. style** .  Le curseur s’attache pour vous permettre d’entrer du texte.  
1.  Entrez un nom de propriété et appuyez sur `Enter` .  
1.  Entrez une valeur valide pour cette propriété et appuyez sur `Enter` .  Dans l' **arborescence DOM**, vérifiez qu’un `style` attribut a été ajouté à l’élément.  

> [!NOTE]
> Dans [figure 12](#figure-12), les `margin-top` `background-color` Propriétés et ont été appliquées à l’élément sélectionné.  Dans l' **arborescence DOM** , assurez-vous que les déclarations sont reflétées dans l' `style` attribut d’un élément.  

> ##### Figure12  
> Ajout de déclarations Inline  
> ![Ajout de déclarations Inline][ImageInlineDeclarations]  

#### Ajouter une déclaration à une règle de style   

Pour ajouter une déclaration à une règle de style existante:  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le volet **styles** , cliquez entre les crochets de la règle de style auxquelles vous souhaitez ajouter la déclaration.  Le curseur s’attache pour vous permettre d’entrer du texte.  
1.  Entrez un nom de propriété et appuyez sur `Enter` .  
1.  Entrez une valeur valide pour cette propriété et appuyez sur `Enter` .  

> ##### Figure13  
> Ajout `border-bottom-style:groove` de la déclaration à une règle de style  
> ![Ajout d’une déclaration à une règle de style][ImageAddDeclarationExistingRule]  

### Modifier le nom ou la valeur d’une déclaration   

Double-cliquez sur le nom ou la valeur d’une déclaration pour la modifier.  Voir [modifier les valeurs de déclaration avec des raccourcis clavier](#change-declaration-values-with-keyboard-shortcuts) pour les raccourcis permettant d’incrémenter ou de décrémenter rapidement une valeur par `0.1` ,, ou par `1` `10` `100` unités.  

> ##### Figure14  
> Modification de la valeur de l’argument `border-bottom-style`  
> ![Modification de la valeur d’une déclaration][ImageAddDeclarationExistingRule2]  

### Modification des valeurs de déclaration avec les raccourcis clavier   

Lors de la modification de la valeur d’une déclaration, vous pouvez utiliser les raccourcis clavier suivants pour incrémenter la valeur à l’aide d’un montant fixe:  

*   Appuyez sur `Alt` + `Up` \ (Windows \) ou `Option` + `Up` \ (MacOS \) pour incrémenter par `0.1` .  
*   Appuyez sur `Up` pour modifier la valeur par `1` , ou `0.1` si la valeur actuelle est comprise entre `-1` et `1` .  
*   Appuyez sur `Shift` + `Up` pour incrémenter par `10` .  
*   Appuyez sur `Shift` + `Page Up` \ (Windows \) ou `Shift` + `Command` + `Up` \ (MacOS \) pour incrémenter la valeur `100` .  

La décrémentation fonctionne également.  Il vous suffit de remplacer chaque instance décrite `Up` plus haut par `Down` .  

### Ajouter une classe à un élément   

Pour ajouter une classe à un élément:  

1.  [Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.  
1.  Cliquez sur **. CLS**.  
1.  Entrez le nom de la classe dans la zone de texte **Ajouter une nouvelle classe** .  
1.  Appuyez sur `Enter` .  

> ##### Figure15  
> Volet **classes d’éléments**  
> ![Volet classes d’éléments][ImageElementClasses]  

### Basculer une classe   

Pour activer ou désactiver une classe sur un élément:  

1.  [Sélectionnez l’élément](#select-an-element) dans l' **arborescence DOM**.  
1.  Ouvrez le volet **classes d’éléments** .  Voir [Ajouter une classe à un élément](#add-a-class-to-an-element).  Sous la zone de texte **Ajouter une nouvelle classe** figurent toutes les classes qui sont appliquées à cet élément.  
1.  Activez/désactivez la case à cocher en regard de la classe que vous souhaitez activer ou désactiver.  

### Ajouter une règle de style   

Pour ajouter une nouvelle règle de style:  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Cliquez sur **nouvelle règle de style** ![ nouvelle règle de style ][ImageNewStyleRuleIcon] .  DevTools insère une nouvelle règle sous la règle **élément. style** .  

> [!NOTE]
> Dans la [figure 16](#figure-16), devtools ajoute la `h1.devsite-page-title` règle de style après avoir cliqué sur **nouvelle règle de style**.  

> ##### Figure16  
> Ajout d’une nouvelle règle de style  
> ![Ajout d’une nouvelle règle de style][ImageStyleRule]  

#### Sélectionner la feuille de style à laquelle ajouter une règle   

Lors de l' [Ajout d’une nouvelle règle de style](#add-a-style-rule), cliquez de **nouveau** sur la règle de style et maintenez-la enfoncée ![ ][ImageNewStyleRuleIcon] pour sélectionner la feuille de style à laquelle ajouter la règle de style.  

> ##### Figure17  
> Choix d’une feuille de style  
> ![Choix d’une feuille de style][ImageChooseStylesheet]  

#### Ajouter une règle de style à un emplacement spécifique   

Pour ajouter une règle de style à un emplacement spécifique, accédez à l’onglet **styles** :  

1.  Pointez sur la règle de style qui se trouve directement au-dessus de l’endroit où vous souhaitez ajouter votre nouvelle règle de style.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Cliquez sur **Insérer une règle de style sous** ![ Insérer une règle de style ci-dessous ][ImageNewStyleRuleIcon] .  

> ##### Figure 18  
> **Insérer une règle de style en dessous**  
> ![Insérer une règle de style en dessous][ImageInsertStyleRuleBelow]  

### Afficher la barre d’outils plus d’actions   

La barre d’outils **plus d’actions** vous permet d’effectuer les opérations suivantes:  

*   Insérez une règle de style juste en dessous de celle qui vous intéresse.  
*   Ajoutez une `background-color` `color` `box-shadow` `text-shadow` déclaration à la règle de style sur laquelle vous êtes prioritaire.  

Pour afficher la barre d’outils **plus d’actions** :  

1.  Dans l’onglet **styles** , pointez sur une règle de style.  **Plus d’actions** `...` est affiché dans le coin inférieur droit de la section règle de style.  
    
    > [!NOTE]
    > Dans la [figure 19](#figure-19), placez le pointeur sur la `.header-holder.has-default-focus` règle de style et d' **autres actions** sont affichées dans le coin inférieur droit de la section règle de style.  
    
    > ##### Figure 19  
    > Affichage **plus d’actions**  
    > ![Affichage plus d’actions][ImageRevealMore]  
    
1.  Placez le pointeur sur **plus d’actions** `...` pour afficher les actions mentionnées ci-dessus.  
    
    > [!NOTE]
    > L’action **Insérer une règle de style ci-dessous** apparaît après avoir pointé sur **plus d’actions**.  
    
    > ##### Figure 20  
    > Barre d’outils **plus d’actions**  
    > ![Barre d’outils plus d’actions][ImageInsertStyleRuleBelow2]  
    
### Basculer une déclaration   

Pour activer ou désactiver une déclaration unique:  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans le volet **styles** , pointez sur la règle qui définit la déclaration.  Les cases à cocher s’affichent en regard de chaque déclaration.  
1.  Activez ou désactivez la case à cocher en regard de la déclaration.  Lorsque vous décochez une déclaration, DevTools la traverse pour indiquer qu’elle n’est plus active.  

> [!NOTE]
> Dans la [figure 21](#figure-21), la `margin-top` propriété de l’élément actuellement sélectionné a été activée.  

> ##### Figure 21  
> Basculer une déclaration  
> ![Basculer une déclaration][ImageToggleDeclaration]  

### Ajouter une déclaration couleur d’arrière-plan   

Pour ajouter une `background-color` déclaration à un élément:  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `background-color` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Cliquez sur **Ajouter une couleur d’arrière-** ![ plan ajouter une couleur d’arrière-plan ][ImageAddBackgroundColorIcon] .  

> ##### Figure 22  
> **Ajouter une couleur d’arrière-plan**  
> ![Ajouter une couleur d’arrière-plan][ImageAddBackgroundColor]  

### Ajouter une déclaration de couleur   

Pour ajouter une `color` déclaration à un élément:  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `color` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Cliquez sur **Ajouter** une couleur ajouter une couleur ![ ][ImageAddColorIcon] .  

> ##### Figure 23  
> **Ajouter de la couleur**  
> ![Ajouter de la couleur][ImageAddColor]  

### Ajouter une déclaration d’ombre Box   

Pour ajouter une `box-shadow` déclaration à un élément:  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `box-shadow` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Cliquez sur **Ajouter** une ombre de zone Ajouter une ombre ![ ][ImageAddBoxShadowIcon] .  

> ##### Figure 24  
> **Ajouter une ombre de zone**  
> ![Ajouter une ombre de zone][ImageAddBoxShadow]  

### Ajouter une déclaration d’ombre textuelle   

Pour ajouter une `text-shadow` déclaration à un élément:  

1.  Pointez sur la règle de style à laquelle vous souhaitez ajouter la `text-shadow` déclaration.  
1.  [Afficher la barre d’outils **plus d’actions** ](#reveal-the-more-actions-toolbar).  
1.  Cliquez sur **Ajouter une ombre du texte** ![ Ajouter une ombre ][ImageAddTextShadowIcon] .  

> ##### Figure 25  
> **Ajouter une ombre de texte**  
> ![Ajouter une ombre de texte][ImageAddTextShadow]  

### Changer les couleurs à l’aide du sélecteur de couleurs   

Le **Sélecteur de couleurs** fournit une interface utilisateur pour le changement `color` et la `background-color` déclaration.  

Pour ouvrir le **Sélecteur de couleurs**:  

1.  [Sélectionnez un élément](#select-an-element).  
1.  Dans l’onglet **styles** , recherchez la `color` `background-color` déclaration, ou similaire, que vous voulez modifier.  À gauche de la `color` valeur, `background-color` ou similaire, il existe un petit carré, qui est un aperçu de la couleur.  
    
    > [!NOTE]
    > Dans la [figure 26](#figure-26), le petit carré à gauche de `rgba(0, 0, 0, 0.7)` est un aperçu de cette couleur.  
    
    > ##### Figure 26  
    > Aperçu de couleur  
    > ![Aperçu de couleur][ImageColorPreview]  
    
1.  Cliquez sur l’Aperçu pour ouvrir le **Sélecteur de couleurs**.  
    
    > ##### Figure 27  
    > **Sélecteur de couleurs**  
    > ![Sélecteur de couleurs][ImageColorPicker]  
    
Voici une description de chaque élément d’interface utilisateur du sélecteur de **couleurs**:  

> ##### Figure 28  
> Sélecteur de couleurs, annoté  
> ![Sélecteur de couleurs, annoté][ImageColorPickerAnnotated]  

1.  **Nuances de gris**.  
1.  **Pipette**.  Pour en savoir plus, voir [exemple de couleur de la page avec le](#sample-a-color-off-the-page-with-the-eyedropper)compte-gouttes.  
1.  **Copier dans le presse-papiers**.  Copiez la **valeur d’affichage** dans le presse-papiers.  
1.  **Valeur d’affichage**.  La représentation RVBA, HSLA ou Hex de la couleur.  
1.  **Palette de couleurs**.  Cliquez sur l’un de ces carrés pour modifier la couleur de ce carré.  
1.  **Nuance**.  
1.  **Opacity**.  
1.  **Sélecteur de valeurs d’affichage**.  Basculer entre les représentations RVBA, HSLA et Hex de la couleur actuelle.  
1.  **Sélecteur de palette de couleurs**.  Basculer entre la [palette de création matérielle][MaterialDesignColorSystem], une palette personnalisée ou une palette de couleurs de page.  DevTools génère la palette de couleurs de page en fonction des couleurs qu’il trouve dans vos feuilles de style.  

#### Exemple de couleur de la page avec le compte-gouttes   

Lorsque vous ouvrez le **Sélecteur de couleurs**, la pipette de la **pipette** ![ ][ImageEyedropperIcon] est activée par défaut.  Pour changer la couleur sélectionnée en fonction de la couleur de la page, procédez comme suit:  

1.  Placez le pointeur de la souris sur la couleur cible dans la fenêtre d’affichage.  
1.  Cliquez sur pour confirmer.  
    
    > [!NOTE]
    > Dans la [figure 29](#figure-29), le **Sélecteur de couleurs** affiche une valeur de couleur actuelle de `rgba(0,0,0,0.7)` , qui est proche de noir.  Lorsque vous cliquez sur le noir lorsque vous cliquez sur la fenêtre d’affichage, cette couleur doit changer.  
    
    > ##### Figure 29  
    > Utiliser le compte-gouttes  
    > ![Utiliser le compte-gouttes][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Figure 1: exemple d’un élément sélectionné"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Figure 2: affichage de la feuille de calcul à l’endroit où une règle est définie"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Figure 3: onglet calculé"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Figure 4: diagramme de modèle de cadre"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Figure 5: filtrer l’onglet styles"  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Figure 6: filtrage de l’onglet calculé"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Figure 7: activation/désactivation de la pseudo-classe Hover"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Figure 8: ouverture de l’onglet couverture dans le menu de commandes"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Figure 9: onglet couverture"  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Figure 10: vue d’ensemble de la quantité d’utilisation et de la feuille de style CSS (JavaScript)"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Figure 11: une répartition ligne par ligne de feuilles CSS utilisées et inutilisées"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Figure 12: ajout de déclarations Inline"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Figure 13: ajout d’une déclaration à une règle de style"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Figure 14: modification de la valeur d’une déclaration"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Figure 15: volet classes d’éléments"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Figure 16: ajout d’une nouvelle règle de style"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Figure 17: choix d’une feuille de style"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Figure 18: insérer une règle de style en dessous"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "Figure 19: révéler plus d’actions"  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Figure 20: barre d’outils plus d’actions"  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Figure 21: basculer une déclaration"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Figure 22: ajouter une couleur d’arrière-plan"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Figure 23: ajouter une couleur"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Figure 24: ombre de la zone Ajouter"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Figure 25: ajouter une ombre de texte"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Figure 26: aperçu des couleurs"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Figure 27: sélecteur de couleurs"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Figure 28: sélecteur de couleurs, annoté"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Figure 29: utilisation du compte-gouttes"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Exécuter des commandes à l’aide du menu de commande de Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Ajouter un PseudoState à une classe: Familiarisez-vous avec l’affichage et la modification de feuilles CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Affichage de la feuille de style en cascade (CSS) d’un élément: commencez à afficher et modifier des feuilles CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Force Microsoft Edge DevTools en mode d’aperçu avant impression (CSS Print Media Type)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Créer une référence de débogage de fichier minified-JavaScript lisible"  

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
