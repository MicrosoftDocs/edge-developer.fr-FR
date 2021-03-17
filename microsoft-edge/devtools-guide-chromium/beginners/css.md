---
description: Mise en place de CSS
title: 'DevTools pour les débutants : mise en place de CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/08/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools
ms.openlocfilehash: 6a7135e144123917535e7c43e6a3cd608ec0c8a7
ms.sourcegitcommit: 4b9fb5c1176fdaa5e3c60af2b84e38d5bb86cd81
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "11439436"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# <a name="devtools-for-beginners-get-started-with-css"></a>DevTools pour les débutants : mise en place de CSS  

Dans ce didacticiel, vous allez apprendre à utiliser CSS pour styler une page web.  Vous apprendrez également à utiliser Microsoft Edge DevTools pour expérimenter les modifications CSS.  

L’article suivant est le deuxième didacticiel d’une série de didacticiels qui vous apprend les principes de base du développement web et de Microsoft Edge DevTools.  Vous gagnez en expérience pratique en construisant votre propre site web.  Vous n’avez pas besoin de terminer le premier didacticiel avant de suivre le second.  [La mise en place de votre code](#set-up-your-code) vous montre comment la configurer.  

> [!NOTE]
> Ce didacticiel est conçu pour les néophytes et se concentre à la fois sur les principes de base du développement **web** et sur les principes de base de l’utilisation de DevTools pour expérimenter CSS.  Si vous souhaitez un didacticiel qui se concentre uniquement sur DevTools, accédez à Démarrer avec l’affichage et la modification [de CSS][DevtoolsCssIndex].  

Au début du didacticiel, votre site doit ressembler à la figure suivante.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Apparence actuelle de votre site" lightbox="../media/beginners-css-intro1.msft.png":::
   Apparence actuelle de votre site  
:::image-end:::  

Une fois le didacticiel terminé, votre site doit ressembler à la figure suivante.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Apparence de votre site à la fin du didacticiel" lightbox="../media/beginners-css-intro2.msft.png":::
   Apparence de votre site à la fin du didacticiel  
:::image-end:::  

## <a name="goals"></a>Objectifs  

Suivez ce didacticiel pour mieux comprendre les concepts et les tâches suivants.  

*   Utilisation de CSS pour le style d’une page web.  
*   Comment utiliser Microsoft Edge DevTools pour expérimenter CSS.  
*   Différence entre les infrastructure CSS et CSS.  

Vous construisez un site web réel.  

## <a name="prerequisites"></a>Prérequis  

Avant d’essayer ce didacticiel, remplissez les conditions préalables suivantes.  

*   [Complétez la][DevtoolsBeginnersHtml] mise en place du code HTML et du DOM ou assurez-vous que vous avez une connaissance du code HTML et du DOM semblable à ce qui est appris dans ce didacticiel.  
*   Téléchargez le navigateur web [Microsoft Edge.][MicrosoftEdgeInsider]  Le didacticiel suivant utilise un ensemble d’outils de développement web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurer votre code  

Pour créer votre site, vous devez d’abord effectuer les actions suivantes pour configurer votre code.  

> [!NOTE]
> Si vous avez déjà terminé le premier didacticiel de la série, passez à la section suivante.  Continuez à utiliser votre code du dernier didacticiel, [Get Started with HTML and the DOM][DevtoolsBeginnersHtml].  

1.  Ouvrez le [code source.][GlitchCookedAmphibianIndex]  L’onglet sur le focus de votre navigateur est référencé en tant **qu’onglet d’édition.**  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Onglet Modification" lightbox="../media/beginners-css-setup1.msft.png":::
       Onglet **Modification**  
    :::image-end:::  
    
1.  Choisissez **l’ombrabe**.  Un menu s’insérait.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Menu Options de Projet" lightbox="../media/beginners-css-setup2.msft.png":::
       Menu Options de Projet  
    :::image-end:::  

1.  Sélectionnez **Projet DeNte**.  Glitch crée une copie du projet que vous pouvez modifier.  
    
    > [!NOTE]
    > Glitch génère un nom aléatoire pour le nouveau projet.  
    
1.  Choose **Show** and choose **In a New Window**.  Un autre onglet s’ouvre avec une vue en direct de votre site.  L’onglet sur le focus de votre navigateur est référencé en tant **qu’onglet en direct.**  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Onglet en direct" lightbox="../media/beginners-css-setup3.msft.png":::
       Onglet **en direct**  
    :::image-end:::  

## <a name="understand-css"></a>Comprendre les CSS  

**CSS est** un langage d’ordinateur qui détermine la disposition et le style des pages web.  La figure suivante est un paragraphe avec une bordure.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Le texte a été mis en forme avec le style CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   Le texte a été mis en forme avec le style CSS  
:::image-end:::  

L’extrait de code suivant est le code HTML et CSS utilisé pour créer le paragraphe dans la figure précédente.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` vous semble probablement nouveau.  Le reste doit paraître familier.  Si ce n’est pas le cas, terminez la mise en place du code HTML et du [DOM][DevtoolsBeginnersHtml] avant d’essayer les sections suivantes.  

## <a name="add-inline-styles"></a>Ajouter des styles inline  

Effectuer les actions suivantes pour utiliser des **styles inline** pour appliquer des styles à un seul élément.  

1.  Revenir à l’onglet Édition et ouvrir `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       Ouvrir `index.html` dans l’onglet Modification  
    :::image-end:::  
    
1.  Ajoutez `style="background-color: aliceblue;"` à `<nav>` votre .  Dans le bloc de code ci-dessous, la quatrième ligne de code est celle que vous devez modifier.  Le reste est là, vous êtes donc en mesure de vous assurer que vous placez le nouveau code au bon endroit.  
    
    ```html
    <header>
        <p>Welcome to my site!</p>
    </header>
    <nav style="background-color: aliceblue;">
        <ul>
            <li><a href="/">Home</a></li>
            ...
        ...
    ...
    ```  
    
1.  Pour afficher les modifications, accédez à **l’onglet en direct.**  L’arrière-plan `<nav>` de la section est désormais bleu.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="La couleur d’arrière-plan derrière les liens Accueil et Contact est désormais bleue" lightbox="../media/beginners-css-inline2.msft.png":::
       La couleur d’arrière-plan derrière **les** liens Accueil **et Contact** est désormais bleue  
    :::image-end:::  
    
## <a name="re-use-styles-on-a-single-page-with-internal-stylesheets"></a>Ré-utiliser des styles sur une seule page avec des feuilles de style internes  

Dans un extrait de code précédent, un style inline appliquait un style à une seule `<p>` balise.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Que se passe-t-il si vous souhaitez que tous les éléments de votre page web soient marqués `<p>` de la même manière ?  Vous devez copier et coller le code dans chaque balise `<p>` de votre site.  Cela fait beaucoup de temps et d’efforts.  Et, si vous avez besoin d’apporter une modification, vous devez modifier à nouveau chaque balise.  Effectuer les actions suivantes pour utiliser une feuille de **style** interne afin d’écrire votre feuille de style CSS une seule fois afin qu’elle s’applique à plusieurs éléments.  

1.  Dans l’onglet en direct, choisissez **Contact** pour accéder à la page de contact.  Notez la police de **Famille** et **Contact**.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Page Contact" lightbox="../media/beginners-css-internal1.msft.png":::
       Page Contact  
    :::image-end:::  
    
1.  Dans **l’onglet Éditeur,** ouvrez `contact.html` .  
1.  Ajoutez le code suivant à `contact.html` .  N’oubliez pas que les lignes commençant par et se terminant par ce que vous `<style>` `</style>` devez ajouter.  L’autre code est là pour vous aider à savoir où placer le nouveau code.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  Revenir à **l’onglet en direct.**  
1.  Sélectionnez **Contact** pour revenir à la page de contact.  La police **d’accueil** **et de contact** a changé.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="La police des liens Accueil et Contact a changé" lightbox="../media/beginners-css-internal2.msft.png":::
       La police des **liens** Accueil et **Contact** a changé  
    :::image-end:::  
    
### <a name="understand-internal-stylesheets"></a>Comprendre les feuilles de style internes  

Les feuilles de style internes appliquent des styles à **l’aide de sélecteurs.**  Les sélecteurs sont des modèles qui peuvent s’appliquer à un ou plusieurs éléments HTML.  L’extrait de code précédent a ajouté le style suivant.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` est un sélecteur qui se traduit par « tout `<li>` élément qui contient un élément `<a>` ».  Le navigateur modifie la police des **liens** d’accueil et de **contact,** car chacun des groupes de balises correspond au modèle.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` est une **déclaration**.  Une déclaration est faite des deux parties suivantes.  

:::row:::
   :::column span="1":::
      **property**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      La propriété décrit une manière générale de modifier le style de l’élément.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **value**  
   :::column-end:::
   :::column span="1":::
      `'Courier New', Courier, serif`  
   :::column-end:::
   :::column span="2":::
      La valeur décrit exactement comment le style de l’élément doit changer.  
   :::column-end:::
:::row-end:::  

Par exemple, `font-family: 'Courier New', Courier, serif` donne au navigateur l’instruction suivante : « Définissez la police des éléments qui correspondent au `li a` modèle `'Courier New'` .  Si cette police n’est pas disponible, utilisez `Courier` .  Si ce n’est pas disponible, utilisez `serif` . »  

### <a name="add-multiple-selectors-to-a-ruleset"></a>Ajouter plusieurs sélecteurs à un jeu de règles  

Un bloc de code CSS comme l’extrait de code suivant est appelé un **jeu de règles.**  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Effectuer les actions suivantes pour utiliser des virgules afin d’ajouter plusieurs sélecteurs à un jeu de règles.  

1.  Dans **l’onglet Éditeur,** ouvrez `contact.html` .  
1.  Après `li a` le type `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    L’extrait de code précédent indique au navigateur de styler les éléments de la même façon qu’il styles les éléments `<h1>` qui correspondent au modèle `li a` .  
    
1.  Accédez à **l’onglet en direct.**  
1.  Sélectionnez **le lien** Contact pour revenir à la page de contact.  À présent, **contactez-moi !** a la même police que les liens de navigation.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Le texte Me contacter !  a maintenant la même police que les liens d’accueil et de contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       Le texte **Me contacter !** a maintenant la même police que les liens **d’accueil** **et de** contact  
    :::image-end:::  
    
## <a name="experiment-with-devtools"></a>Expérimenter Avec DevTools  

Lorsque vous poursuivez votre parcours pour devenir un expert en développement web, il se peut que vous trouviez que CSS est difficile.  Vous pouvez écrire du CSS et vous attendre à ce qu’il s’affiche dans un sens, mais le navigateur fait quelque chose de complètement différent.  Microsoft Edge DevTools facilite l’expérimentation des modifications et l’affichage immédiat de l’impact de ces modifications sur la page.  

### <a name="add-a-declaration-to-an-existing-rulest-in-devtools"></a>Ajouter une déclaration à un rulest existant dans DevTools  

Complétez les actions suivantes pour itérer sur le style d’un élément existant, ajoutez une déclaration à un jeu de règles existant.  

1.  Pointez sur le **lien Accueil,** ouvrez le menu contextuel \(clic droit\), puis choisissez **Inspecter**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Inspecter le lien Accueil" lightbox="../media/beginners-css-add1.msft.png":::
       Inspecter le lien Accueil  
    :::image-end:::  
    
    DevTools s’ouvre à côté de votre page.  Le code qui représente le lien Accueil est `<a href="/">Home</a>` mis en surbrillant en bleu dans l’arborescence DOM.  L’extrait de code et l’aperçu doivent être familiers à partir de La mise en route avec [HTML et le DOM][DevtoolsBeginnersHtml].  
    
    :::row:::
       :::column span="":::
          Dans la figure suivante, la déclaration que vous avez précédemment ajoutée s’affiche dans l’onglet Styles sous `font-family: 'Courier New', Courier, serif` `contact.html` l’arborescence DOM. ****  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="L’onglet Styles se trouve sous l’arborescence DOM" lightbox="../media/beginners-css-add2.msft.png":::
             **L’onglet Styles** se trouve sous l’arborescence DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si votre fenêtre DevTools est large, l’onglet Styles se trouve à droite de l’arborescence DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="L’onglet Styles se trouve à droite de l’arborescence DOM" lightbox="../media/beginners-css-add3.msft.png":::
             **L’onglet Styles** se trouve à droite de l’arborescence DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Choisissez la ligne vide `font-family: 'Courier New', Courier, Serif` ci-dessous pour ajouter une nouvelle déclaration.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Ajouter une nouvelle déclaration" lightbox="../media/beginners-css-add4.msft.png":::
       Ajouter une nouvelle déclaration  
    :::image-end:::  
    
1.  Tapez `color` et sélectionnez `Enter` .  L’interface utilisateur de la mise àcomplet automatique suggère des options en cours de taper.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Couleur du type" lightbox="../media/beginners-css-add5.msft.png":::
       Type `color`  
    :::image-end:::  
    
1.  Tapez `magenta` et sélectionnez `Enter` .  Tout le texte de la page de contact est désormais magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Type magenta" lightbox="../media/beginners-css-add6.msft.png":::
       Type `magenta`  
    :::image-end:::  
    
### <a name="edit-a-declaration-in-devtools"></a>Modifier une déclaration dans DevTools  

Effectuer les actions suivantes pour modifier les déclarations existantes dans DevTools.  

1.  Choose the magenta square next to `magenta` .  Un s picker de couleur apparaît.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="S sélectionneur de couleurs" lightbox="../media/beginners-css-edit1.msft.png":::
       S sélectionneur de couleurs  
    :::image-end:::  
    
1.  Utilisez le s sélectionneur de couleurs pour modifier le texte de police en une couleur que vous aimez.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Modifier la couleur de police en violet avec le s picker de couleurs" lightbox="../media/beginners-css-edit2.msft.png":::
       Modifier la couleur de police en violet avec le s picker de couleurs  
    :::image-end:::  
    
### <a name="add-a-new-ruleset-in-devtools"></a>Ajouter un nouveau jeu de règles dans DevTools  

Pour ajouter de nouveaux jeux de règles dans DevTools, complétez les actions suivantes.  

1.  Choose **New Style Rule** \( New Style Rule ![ ](../media/new-style-rule-icon.msft.png) \) which is next to **.cls**.  Un jeu de règles vide apparaît avec `a` le sélecteur.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Ajouter une nouvelle règle" lightbox="../media/beginners-css-rule1.msft.png":::
       Ajouter une nouvelle règle  
    :::image-end:::  
    
1.  Remplacez `a` par `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Remplacer un par un : pointer" lightbox="../media/beginners-css-rule2.msft.png":::
       Remplacer `a` par `a:hover`  
    :::image-end:::  
    
    `:hover` est **une pseudo-classe**.  Utilisez des pseudo-classes pour les éléments de style qui peuvent entrer des états spéciaux.  Par exemple, le `a:hover` style prend effet uniquement lorsque vous pointez sur un `<a>` élément.  
    
1.  Choisissez entre les crochets pour ajouter une nouvelle déclaration.  
1.  Tapez `background-color` le nom de la déclaration et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Tapez couleur d’arrière-plan" lightbox="../media/beginners-css-rule3.msft.png":::
       Type `background-color`  
    :::image-end:::  
    
1.  Tapez `green` la valeur de déclaration et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Type vert" lightbox="../media/beginners-css-rule4.msft.png":::
       Type `green`  
    :::image-end:::  
    
1.  Pointez votre souris sur le **lien Accueil.**  L’arrière-plan du lien devient vert.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Pointez sur le lien Accueil pour révéler son arrière-plan vert" lightbox="../media/beginners-css-rule5.msft.png":::
       Pointez sur le lien Accueil pour révéler son arrière-plan vert  
    :::image-end:::  
    
## <a name="re-use-styles-across-pages-with-external-stylesheets"></a>Ré-utiliser les styles entre les pages avec des feuilles de style externes  

Dans une étape précédente, vous avez ajouté l’extrait de code suivant en tant que feuille de style interne à `contact.html` .  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

Que se passe-t-il si vous `index.html` souhaitez un style identique ?  Que se passe-t-il si vous avez un grand nombre de pages sur lesquelles vous souhaitez appliquer vos styles ?  Vous devez copier et coller la feuille de style interne dans chaque page web de votre site.  Effectuer les actions suivantes pour ajouter une feuille de **style externe** afin de vous permettre d’écrire votre feuille de style CSS une seule fois et de l’appliquer à plusieurs pages.  

1.  Tout d’abord, actualisez l’onglet en direct pour supprimer les modifications que vous avez apportées dans DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Une fois que vous avez actualisé la page, les modifications qui ont été apportées dans DevTools ont disparu." lightbox="../media/beginners-css-external1.msft.png":::
        Une fois que vous avez actualisé la page, les modifications qui ont été apportées dans DevTools ont disparu.  
    :::image-end:::  
    
1.  Revenir à **l’onglet Éditeur et** ouvrir `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Supprimez tout ce `<style>` qui est compris entre `</style>` et, y compris et `<style>` `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="La balise de style a été supprimée" lightbox="../media/beginners-css-external3.msft.png":::
       La balise de style a été supprimée  
    :::image-end:::  
    
1.  Ouvrez `index.html` et `style="background-color: aliceblue;"` supprimez de la `<nav>` balise.  Vous avez maintenant supprimé toutes les CSS que vous avez précédemment ajoutées à votre site.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Le style inline a été supprimé de l’élément de navigation" lightbox="../media/beginners-css-external4.msft.png":::
       Le style inline a été supprimé de l’élément de navigation  
    :::image-end:::  
    
1.  Choose **New File**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Boîte de dialogue nouveau fichier" lightbox="../media/beginners-css-external5.msft.png":::
       Boîte de dialogue nouveau fichier  
    :::image-end:::  
    
1.  Remplacez `cool-file.js` par et choisissez Ajouter un `style.css` **fichier.**  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type style.css" lightbox="../media/beginners-css-external6.msft.png":::
       Type `style.css`  
    :::image-end:::  
    
1.  Ajoutez l’extrait de code suivant à votre `style.css` fichier.  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Ajouter du code à style.css" lightbox="../media/beginners-css-external7.msft.png":::
       Ajouter du code à `style.css`  
    :::image-end:::  
    
    Assurez-vous que vous avez créé une feuille de style externe. Votre code HTML ne sait pas qu’il existe.  
    
1.  Ouvrez `index.html` .  
1.  `<link rel="stylesheet" href="style.css">`Ajoutez-le à votre code HTML.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Lien vers style.css" lightbox="../media/beginners-css-external8.msft.png":::
       Lien vers `style.css`  
    :::image-end:::  
    
1.  Ouvrez `contact.html` le fichier et ajoutez-y le lien.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Lien vers style.css dans contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       Lien vers `style.css` l’en `contact.html`  
    :::image-end:::  
    
1.  Accédez à **l’onglet en direct.**  La page d’accueil possède désormais la même police que la dernière section et une section de navigation bleue.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Page d’accueil" lightbox="../media/beginners-css-external10.msft.png":::
       Page d’accueil  
    :::image-end:::  
    
1.  Choisissez le **lien Contact** pour accéder à la page de contact.  La page de contact a la même mise en forme que la page d’accueil.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Page de contact" lightbox="../media/beginners-css-external11.msft.png":::
       Page de contact  
    :::image-end:::  
    
## <a name="use-a-css-framework"></a>Utiliser une infrastructure CSS  

**Les frameworks CSS** sont des collections de styles conçues par d’autres développeurs qui facilitent la création de sites web attrayants.  Au lieu de définir vous-même les styles, une infrastructure vous fournit une collection de styles que vous pouvez utiliser sur vos éléments de page.  

1.  Copiez le code suivant :  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Ouvrez l’onglet Édition et collez le code dans `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Lien vers l’infrastructure dans contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       Lien vers l’infrastructure dans `contact.html`  
    :::image-end:::  
    
1.  Ouvrez `index.html` le fichier et ajoutez-y le code.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Lien vers l’infrastructure dans index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       Lien vers l’infrastructure dans `index.html`  
    :::image-end:::  
    
1.  Revenir à l’onglet en direct pour afficher vos modifications.  Bien que la couleur d’arrière-plan de l’élément et la police des éléments et des éléments soient identiques, la police des autres éléments `<nav>` `<li>` a `<a>` changé.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Une partie de la police de la page d’accueil a été modifiée en raison de l’infrastructure" lightbox="../media/beginners-css-framework3.msft.png":::
       Une partie de la police de la page d’accueil a été modifiée en raison de l’infrastructure  
    :::image-end:::  
    
### <a name="use-a-class"></a>Utiliser une classe  

Dans la dernière section, vous avez ajouté Bootstrap à vos pages web, ce qui a modifié les polices de certains éléments de votre site.  Les frameworks CSS vous aident à apporter des modifications majeures à votre page avec très peu de code.  Pour modifier votre en-tête, complétez les actions suivantes.  

1.  Copiez l’extrait de code suivant.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Ajoutez l’extrait de code précédent à votre `<header>` balise dans `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Ajouter des classes dans index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Ajouter des classes dans `index.html`  
    :::image-end:::  
    
1.  Ajoutez le code à `<header>` votre balise dans `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Ajouter des classes dans contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Ajouter des classes dans `contact.html`  
    :::image-end:::  
    
1.  Affichez vos modifications dans l’onglet en direct.  Il y a une grande zone grise autour de votre en-tête.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="L’en-tête est maintenant encadré d’une grande zone grise" lightbox="../media/beginners-css-jumbotron3.msft.png":::
       L’en-tête est maintenant encadré d’une grande zone grise  
    :::image-end:::  
    
### <a name="understand-classes"></a>Comprendre les classes  

Les classes vous permet d’affecter des collections de styles à des éléments arbitraires.  Utilisez l’extrait de code suivant pour appliquer plusieurs styles à l’élément après avoir définie `<header>` `class` l’attribut sur `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

L’un des avantages d’une classe est qu’elle vous permet d’appliquer des styles aux éléments de votre souhaitez.  Par exemple, supposons que vous vouliez définir la couleur d’arrière-plan de certains éléments sur `<p>` violet, mais pas sur tous les `<p>` éléments.  Utilisez l’extrait de code suivant pour définir le style dans une classe.  

```css
.custom-background {
  background-color: purple;
}
```  

Ensuite, appliquez la classe uniquement aux éléments `<p>` que vous souhaitez appliquer au style.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### <a name="align-elements"></a>Aligner les éléments  

Effectuer les actions suivantes pour amorcer et fournir des classes pour aligner les éléments.  

1.  Revenir à l’onglet Éditeur et ouvrir `index.html` .  
1.  Ajoutez `class="container-fluid"` à votre `<body>` balise.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Ajouter la classe fluide conteneur" lightbox="../media/beginners-css-align1.msft.png":::
       Ajouter la `container-fluid` classe  
    :::image-end:::  
    
1.  Encapsulez `<nav>` vos éléments et vos `<main>` `<div class="row">` éléments.  Veillez à placer `</div>` après afin de fermer correctement la nouvelle `</main>` balise.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Ajouter une ligne" lightbox="../media/beginners-css-align2.msft.png":::
       Ajouter une ligne  
    :::image-end:::  
    
1.  `class="col-3"`Ajoutez-la `<nav>` à votre balise et à votre `class="col-9"` `<main>` balise.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Ajouter les classes col-3 et col-9" lightbox="../media/beginners-css-align3.msft.png":::
       Ajouter les `col-3` `col-9` classes et les classes  
    :::image-end:::  
    
1.  Affichez vos modifications dans l’onglet en direct.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Le contenu de navigation se trouve maintenant à gauche du contenu principal" lightbox="../media/beginners-css-align4.msft.png":::
       Le contenu de navigation se trouve maintenant à gauche du contenu principal  
    :::image-end:::  
    
## <a name="next-steps"></a>Étapes suivantes  

Félicitations, vous avez terminé.  

*   La meilleure façon d’améliorer le développement web consiste à créer davantage de sites.  Ne vous inquiétez pas de la casse.  Il vous suffit de vous faire plaisir et d’apprendre autant que possible en cours de route.  
*   Pour en savoir plus sur le style des pages web, accédez à [Introduction à CSS][MDNCssFirstSteps].  
*   Pour en savoir plus sur l’utilisation de DevTools pour expérimenter le CSS d’une page, accédez à Démarrer avec l’affichage et la modification [de CSS][DevtoolsCssIndex].  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools pour les débutants : mise en place du code HTML et du dom | Documents Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Mise en place de l’affichage et de la modification des | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html - | Glitch"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Premières étapes de la CSS | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/beginners/css) et est co-auteure par [Le rédacteur technique Principal \(interne][KatherineJackson] rédacteur technique, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
