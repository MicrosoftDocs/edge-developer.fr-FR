---
description: Découvrir les feuilles CSS
title: 'DevTools pour les débutants: prendre en main CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: fe87b4f840c6d9dde3cdf6455700161ea8d8d31e
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993302"
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

# DevTools pour les débutants: prendre en main CSS  

Dans ce didacticiel, vous allez apprendre à utiliser les feuilles CSS pour appliquer un style à une page Web.  Vous pouvez également apprendre à utiliser Microsoft Edge DevTools pour tester les changements CSS.  

L’article suivant est le deuxième didacticiel d’une série de didacticiels qui vous explique les notions de base du développement Web et de Microsoft Edge DevTools.  Profitez d’une expérience pratique en créant votre propre site Web.  Vous n’avez pas besoin de terminer le premier didacticiel avant de suivre le second.  La [configuration de votre code](#set-up-your-code) vous montre comment procéder à la configuration.  

> [!NOTE]
> Ce didacticiel est conçu pour les débutants et est axé sur les notions **fondamentales du développement Web** et des notions de base de l’utilisation de devtools pour tester les feuilles CSS.  Si vous avez besoin d’un didacticiel destiné uniquement à DevTools, voir [découvrir comment afficher et modifier des feuilles CSS][DevtoolsCssIndex].  

Au début du didacticiel, votre site doit ressembler à la figure suivante.  

:::image type="complex" source="../media/beginners-css-intro1.msft.png" alt-text="Aspect de votre site" lightbox="../media/beginners-css-intro1.msft.png":::
   Aspect de votre site  
:::image-end:::  

À la fin du didacticiel, vous devez vous présenter comme suit.  

:::image type="complex" source="../media/beginners-css-intro2.msft.png" alt-text="Aspect de votre site à la fin du didacticiel" lightbox="../media/beginners-css-intro2.msft.png":::
   Aspect de votre site à la fin du didacticiel  
:::image-end:::  

## Définis  

Suivez ce didacticiel pour mieux comprendre les concepts et les tâches suivants.  

*   Comment utiliser les feuilles CSS pour appliquer un style à une page Web.  
*   Comment utiliser Microsoft Edge DevTools pour tester les feuilles CSS.  
*   Différence entre les infrastructures CSS et CSS.  

Vous créez un site Web réel.  

## Éléments prérequis  

Avant de suivre ce didacticiel, remplissez les conditions préalables suivantes.  

*   Complétez-vous [avec HTML et le DOM][DevtoolsBeginnersHtml] ou assurez-vous que vous comprenez bien html et le DOM semblable à ce qui est enseigné dans ce didacticiel.  
*   Téléchargez le navigateur Web [Microsoft Edge][MicrosoftEdgeInsider] .  Le didacticiel suivant utilise un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.  

## Configurer votre code  

Pour créer votre site, vous devez d’abord effectuer les actions suivantes pour configurer votre code.  

> [!NOTE]
> Si vous avez déjà effectué le premier didacticiel de la série, passez à la section suivante.  Continuez à utiliser votre code à partir du dernier didacticiel, de [la mise en route de HTML et du DOM][DevtoolsBeginnersHtml].  

1.  Ouvrez le [code source][GlitchCookedAmphibianIndex].  L’onglet d’activation de votre navigateur est référencé en tant qu' **onglet de modification**.  
    
    :::image type="complex" source="../media/beginners-css-setup1.msft.png" alt-text="Onglet édition" lightbox="../media/beginners-css-setup1.msft.png":::
       Onglet **édition**  
    :::image-end:::  
    
1.  Sélectionnez **cuit-Amphibian**.  Un menu s’ouvre.  
    
    :::image type="complex" source="../media/beginners-css-setup2.msft.png" alt-text="Menu options de Project" lightbox="../media/beginners-css-setup2.msft.png":::
       Menu options de Project  
    :::image-end:::  

1.  Sélectionnez **Remix Project**.  Le problème crée une copie du projet que vous pouvez modifier.  
    
    > [!NOTE]
    > Le problème génère un nom aléatoire pour le nouveau projet.  
    
1.  Sélectionnez **Afficher** et sélectionner **dans une nouvelle fenêtre**.  Un autre onglet s’ouvre en mode en direct de votre site.  L’onglet actif de votre navigateur est référencé en tant qu' **onglet actif**.  
    
    :::image type="complex" source="../media/beginners-css-setup3.msft.png" alt-text="Onglet Live" lightbox="../media/beginners-css-setup3.msft.png":::
       **Onglet Live**  
    :::image-end:::  

## Comprendre CSS  

**CSS** est un langage informatique qui détermine la disposition et le style des pages Web.  La figure suivante représente un paragraphe avec une bordure.  

:::image type="complex" source="../media/beginners-css-red_paragraph.msft.png" alt-text="Le texte est mis en forme à l’aide de feuilles CSS" lightbox="../media/beginners-css-red_paragraph.msft.png":::
   Le texte est mis en forme à l’aide de feuilles CSS  
:::image-end:::  

L’extrait de code suivant correspond au code HTML et au code CSS utilisé pour créer le paragraphe dans l’illustration précédente.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` C’est probablement une nouveauté.  Le reste devrait vous être familier.  Si ce n’est pas le cas, terminez- [le en utilisant le code HTML et le DOM][DevtoolsBeginnersHtml] avant de commencer les sections suivantes.  

## Ajouter des styles intralignes  

Procédez comme suit pour utiliser des **styles intralignes** et appliquer des styles à un seul élément.  

1.  Revenez à l’onglet modification et ouvrez `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-inline1.msft.png" alt-text="index.html" lightbox="../media/beginners-css-inline1.msft.png":::
       Ouvrir `index.html` dans l’onglet édition  
    :::image-end:::  
    
1.  Ajoutez `style="background-color: aliceblue;"` à votre `<nav>` .  Dans le bloc de code ci-dessous, la quatrième ligne de code est celle que vous devez modifier.  Le reste est là pour vous permettre de vérifier que vous avez bien placé le nouveau code au bon endroit.  
    
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
    
1.  Accédez à l' **onglet Live** pour afficher les modifications.  L’arrière-plan de la `<nav>` section est désormais bleu.  
    
    :::image type="complex" source="../media/beginners-css-inline2.msft.png" alt-text="La couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue" lightbox="../media/beginners-css-inline2.msft.png":::
       La couleur d’arrière-plan derrière les liens **Accueil** et **contact** est désormais bleue  
    :::image-end:::  
    
## Réutiliser les styles sur une seule page à l’aide de feuilles de style internes  

Dans l’extrait de code précédent, un style intraligne a appliqué un style à une seule `<p>` balise.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Que faire si vous souhaitez que tous les `<p>` éléments d’une page Web soient stylisés de la même manière?  Vous devez copier et coller le code dans chaque `<p>` balise unique de votre site.  Il s’agit d’un temps considérable.  Et si vous avez besoin d’effectuer une modification, vous devrez à nouveau modifier chaque balise.  Procédez comme suit pour utiliser une **feuille de style interne** pour écrire votre CSS une seule fois, afin qu’elle s’applique à plusieurs éléments.  

1.  Dans l’onglet Live, sélectionnez **contact** pour accéder à la page de contact.  Notez la police **Accueil** et **contact**.  
    
    :::image type="complex" source="../media/beginners-css-internal1.msft.png" alt-text="Page de contact" lightbox="../media/beginners-css-internal1.msft.png":::
       Page de contact  
    :::image-end:::  
    
1.  Dans l' **onglet Éditeur**, accédez à `contact.html` .  
1.  Ajoutez le code suivant à `contact.html` .  Rappelez-vous que les lignes commençant par `<style>` et se terminant par `</style>` sont celles que vous devez ajouter.  L’autre code est là pour vous indiquer où placer le nouveau code.  
    
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
    
1.  Revenir à l' **onglet Live**.  
1.  Sélectionnez **contact** pour revenir à la page de contact.  La police **Accueil** et **contact** a changé.  
    
    :::image type="complex" source="../media/beginners-css-internal2.msft.png" alt-text="La police des liens accueil et contact a changé" lightbox="../media/beginners-css-internal2.msft.png":::
       La police des liens **Accueil** et **contact** a changé  
    :::image-end:::  
    
### Comprendre les feuilles de style internes  

Les feuilles de style internes s’appliquent aux styles à l’aide de **sélecteurs**.  Les sélecteurs sont des modèles qui peuvent être appliqués à un ou plusieurs éléments HTML.  L’extrait de code précédent a ajouté le style suivant.  

```html
<style>
    li a {
      font-family: 'Courier New', Courier, Serif;
    }
</style>
```  

`li a` est un sélecteur qui devient «tout `<li>` élément contenant un `<a>` élément».  Le navigateur modifie la police des liens **Accueil** et **contact** , car chacun des groupes de balises correspond au modèle.  

```html
<li><a href="/">Home</a></li>
<li><a href="/contact.html">Contact</a></li>
```  

`font-family: 'Courier New', Courier, serif` est une **déclaration**.  Une déclaration est constituée de deux parties suivies.  

:::row:::
   :::column span="1":::
      **Propriétés**  
   :::column-end:::
   :::column span="1":::
      `font-family`  
   :::column-end:::
   :::column span="2":::
      La propriété décrit une manière générale que vous êtes en mesure de modifier le style de l’élément.  
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
      La valeur décrit exactement le mode de modification du style de l’élément.  
   :::column-end:::
:::row-end:::  

Par exemple, `font-family: 'Courier New', Courier, serif` donne au navigateur l’instruction suivante: "définissez la police des éléments qui correspondent au modèle `li a` `'Courier New'` .  Si cette police n’est pas disponible, utilisez `Courier` .  Si ce n’est pas le cas, utilisez `serif` .»  

### Ajouter plusieurs sélecteurs à un groupe de règles  

Un bloc de code CSS tel que celui qui apparaît ci-dessous est appelé **RuleSet**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Effectuez les opérations suivantes pour utiliser des virgules pour ajouter plusieurs sélecteurs à un RuleSet.  

1.  Dans l' **onglet Éditeur**, ouvrez `contact.html` .  
1.  Après `li a` type `, h1` .  
    
    ```html
    <style>
        li a, h1 {
          font-family: 'Courier New', Courier, Serif;
        }
    </style>
    ```  
    
    L’extrait de code précédent indique au navigateur qu' `<h1>` il s’agit de la même façon que les éléments style qui correspondent au modèle `li a` .  
    
1.  Accédez à l' **onglet Live**.  
1.  Cliquez sur le lien de **contact** pour revenir à la page de contact.  Maintenant, **Contactez-moi!** a la même police que les liens de navigation.  
    
    :::image type="complex" source="../media/beginners-css-multiple1.msft.png" alt-text="Le texte me contacter.  possède désormais la même police que les liens accueil et contact" lightbox="../media/beginners-css-multiple1.msft.png":::
       Le texte **me contacter.** possède désormais la même police que les liens **Accueil** et **contact**  
    :::image-end:::  
    
## Expérimentez avec DevTools  

Lorsque vous continuez votre voyage pour devenir un expert en développement Web, il est possible que les feuilles de style CSS soient difficiles.  Vous pouvez écrire du code CSS et vous attendre à ce qu’il s’affiche de façon unique, mais le navigateur a un aspect complètement différent.  Microsoft Edge DevTools vous permet d’expérimenter facilement les modifications et de voir immédiatement l’incidence de ces modifications sur la page.  

### Ajouter une déclaration à une règle existante dans DevTools  

Procédez comme suit pour effectuer une itération sur le style d’un élément existant, ajouter une déclaration à un RuleSet existant.  

1.  Positionnez le pointeur sur le lien **Accueil** , ouvrez le menu contextuel, puis cliquez sur **inspecter**.  
    
    :::image type="complex" source="../media/beginners-css-add1.msft.png" alt-text="Examiner le lien Accueil" lightbox="../media/beginners-css-add1.msft.png":::
       Examiner le lien Accueil  
    :::image-end:::  
    
    DevTools s’ouvre à côté de votre page.  Le code qui représente le lien Accueil `<a href="/">Home</a>` est surligné en bleu dans l’arborescence DOM.  L’extrait de code et l’aperçu doivent être familiers de la mise [en route de HTML et du DOM][DevtoolsBeginnersHtml].  
    
    :::row:::
       :::column span="":::
          Dans l’illustration suivante, la `font-family: 'Courier New', Courier, serif` déclaration que vous avez précédemment ajoutée `contact.html` s’affiche dans l’onglet **styles** sous l’arborescence DOM.  
          
          :::image type="complex" source="../media/beginners-css-add2.msft.png" alt-text="L’onglet styles se trouve sous l’arborescence DOM" lightbox="../media/beginners-css-add2.msft.png":::
             L’onglet **styles** se trouve sous l’arborescence DOM  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          Si votre fenêtre DevTools est large, l’onglet styles se trouve à droite de l’arborescence DOM.  
          
          :::image type="complex" source="../media/beginners-css-add3.msft.png" alt-text="Onglet styles à droite de l’arborescence DOM" lightbox="../media/beginners-css-add3.msft.png":::
             Onglet **styles** à droite de l’arborescence DOM  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Sélectionnez la ligne vide ci-dessous `font-family: 'Courier New', Courier, Serif` pour ajouter une nouvelle déclaration.  
    
    :::image type="complex" source="../media/beginners-css-add4.msft.png" alt-text="Ajouter une nouvelle déclaration" lightbox="../media/beginners-css-add4.msft.png":::
       Ajouter une nouvelle déclaration  
    :::image-end:::  
    
1.  Tapez `color` et sélectionnez `Enter` .  L’interface utilisateur de saisie semi-automatique suggère des options au fur et à mesure que vous tapez.  
    
    :::image type="complex" source="../media/beginners-css-add5.msft.png" alt-text="Couleur de type" lightbox="../media/beginners-css-add5.msft.png":::
       Type `color`  
    :::image-end:::  
    
1.  Tapez `magenta` et sélectionnez `Enter` .  Tout le texte de la page de contact est désormais magenta.  
    
    :::image type="complex" source="../media/beginners-css-add6.msft.png" alt-text="Taper magenta" lightbox="../media/beginners-css-add6.msft.png":::
       Type `magenta`  
    :::image-end:::  
    
### Modifier une déclaration dans DevTools  

Pour modifier des déclarations existantes dans DevTools, procédez comme suit:  

1.  Choisissez le carré magenta en regard de `magenta` .  Un sélecteur de couleur apparaît.  
    
    :::image type="complex" source="../media/beginners-css-edit1.msft.png" alt-text="Sélecteur de couleurs" lightbox="../media/beginners-css-edit1.msft.png":::
       Sélecteur de couleurs  
    :::image-end:::  
    
1.  Utilisez le sélecteur de couleurs pour remplacer le texte de la police par une couleur de votre choix.  
    
    :::image type="complex" source="../media/beginners-css-edit2.msft.png" alt-text="Changer la couleur de la police en violet grâce au sélecteur de couleurs" lightbox="../media/beginners-css-edit2.msft.png":::
       Changer la couleur de la police en violet grâce au sélecteur de couleurs  
    :::image-end:::  
    
### Ajouter un nouveau RuleSet dans DevTools  

Complétez les actions suivantes pour ajouter de nouvelles règles dans DevTools.  

1.  Cliquez sur **nouvelle règle de style** \ ( ![ nouvelle règle de style ][ImageNewStyleRuleIcon] \) en regard de **. CLS**.  Un RuleSet vide apparaît avec `a` le sélecteur.  
    
    :::image type="complex" source="../media/beginners-css-rule1.msft.png" alt-text="Ajouter une nouvelle règle" lightbox="../media/beginners-css-rule1.msft.png":::
       Ajouter une nouvelle règle  
    :::image-end:::  
    
1.  Remplacer `a` par `a:hover` .  
    
    :::image type="complex" source="../media/beginners-css-rule2.msft.png" alt-text="Remplacer a par a:hover" lightbox="../media/beginners-css-rule2.msft.png":::
       Remplacer `a` par `a:hover`  
    :::image-end:::  
    
    `:hover` est une **Pseudo-classe**.  Utilisez des Pseudo-classes pour les éléments de style qui pourraient entrer des États spéciaux.  Par exemple, le `a:hover` style n’est appliqué que lorsque vous pointez sur un `<a>` élément.  
    
1.  Choisissez entre les crochets pour ajouter une nouvelle déclaration.  
1.  Tapez `background-color` le nom de la déclaration et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule3.msft.png" alt-text="Taper couleur d’arrière-plan" lightbox="../media/beginners-css-rule3.msft.png":::
       Type `background-color`  
    :::image-end:::  
    
1.  Tapez `green` la valeur de la déclaration et sélectionnez `Enter` .  
    
    :::image type="complex" source="../media/beginners-css-rule4.msft.png" alt-text="Taper en vert" lightbox="../media/beginners-css-rule4.msft.png":::
       Type `green`  
    :::image-end:::  
    
1.  Positionnez le pointeur de la souris sur le lien **Accueil** .  L’arrière-plan du lien devient vert.  
    
    :::image type="complex" source="../media/beginners-css-rule5.msft.png" alt-text="Placez le pointeur de la souris sur le lien Accueil pour afficher son arrière-plan vert" lightbox="../media/beginners-css-rule5.msft.png":::
       Placez le pointeur de la souris sur le lien Accueil pour afficher son arrière-plan vert  
    :::image-end:::  
    
## Réutiliser les styles entre les pages à l’aide de feuilles de style externes  

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

Que faire si vous souhaitez changer de style `index.html` ?  Que faire si vous avez un grand nombre de pages auxquelles vous souhaitez appliquer vos styles?  Vous devez copier et coller la feuille de style interne dans chaque page Web de votre site.  Procédez comme suit pour ajouter une **feuille de style externe** afin de pouvoir écrire votre CSS une seule fois et l’appliquer à plusieurs pages.  

1.  Tout d’abord, rechargez l’onglet Live pour supprimer les modifications que vous avez apportées dans DevTools.  
    
    :::image type="complex" source="../media/beginners-css-external1.msft.png" alt-text=" Suite à l’actualisation de la page, les modifications apportées à DevTools ont disparu" lightbox="../media/beginners-css-external1.msft.png":::
        Suite à l’actualisation de la page, les modifications apportées à DevTools ont disparu  
    :::image-end:::  
    
1.  Revenez à l' **onglet Éditeur** , puis ouvrez `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-external2.msft.png" alt-text="contact.html" lightbox="../media/beginners-css-external2.msft.png":::
       contact.html  
    :::image-end:::  
    
1.  Supprimez tous `<style>` les éléments entre et `</style>` , y compris `<style>` et `</style>` .  
    
    :::image type="complex" source="../media/beginners-css-external3.msft.png" alt-text="La balise de style a été supprimée" lightbox="../media/beginners-css-external3.msft.png":::
       La balise de style a été supprimée  
    :::image-end:::  
    
1.  Accédez à `index.html` la balise et supprimez- `style="background-color: aliceblue;"` la `<nav>` .  Vous avez supprimé toutes les feuilles CSS que vous avez précédemment ajoutées à votre site.  
    
    :::image type="complex" source="../media/beginners-css-external4.msft.png" alt-text="Le style intraligne a été supprimé de l’élément navigation" lightbox="../media/beginners-css-external4.msft.png":::
       Le style intraligne a été supprimé de l’élément navigation  
    :::image-end:::  
    
1.  Sélectionnez **nouveau fichier**.  
    
    :::image type="complex" source="../media/beginners-css-external5.msft.png" alt-text="Boîte de dialogue nouveau fichier" lightbox="../media/beginners-css-external5.msft.png":::
       Boîte de dialogue nouveau fichier  
    :::image-end:::  
    
1.  Remplacez `cool-file.js` par `style.css` et sélectionnez **Ajouter un fichier**.  
    
    :::image type="complex" source="../media/beginners-css-external6.msft.png" alt-text="Type style. CSS" lightbox="../media/beginners-css-external6.msft.png":::
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
    
    :::image type="complex" source="../media/beginners-css-external7.msft.png" alt-text="Ajouter du code à style. CSS" lightbox="../media/beginners-css-external7.msft.png":::
       Ajouter du code à `style.css`  
    :::image-end:::  
    
    Vérifiez que vous avez créé une feuille de style externe. Votre code HTML n’est pas pris en charge.  
    
1.  Ouvrir `index.html` .  
1.  Ajoutez `<link rel="stylesheet" href="style.css">` à votre code html.  
    
    ```html
    <head>
        ...
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="style.css">
    </head>
    ```  
    
    :::image type="complex" source="../media/beginners-css-external8.msft.png" alt-text="Lien vers style. CSS" lightbox="../media/beginners-css-external8.msft.png":::
       Lien vers `style.css`  
    :::image-end:::  
    
1.  Ouvrez le `contact.html` fichier et ajoutez-y le lien.  
    
    :::image type="complex" source="../media/beginners-css-external9.msft.png" alt-text="Lien vers style. CSS dans contact.html" lightbox="../media/beginners-css-external9.msft.png":::
       Lien vers `style.css` dans `contact.html`  
    :::image-end:::  
    
1.  Accédez à l' **onglet Live**.  La page d’accueil possède désormais la même police que la dernière section et une section de navigation bleue.  
    
    :::image type="complex" source="../media/beginners-css-external10.msft.png" alt-text="Page d’accueil" lightbox="../media/beginners-css-external10.msft.png":::
       Page d’accueil  
    :::image-end:::  
    
1.  Cliquez sur le lien de **contact** pour accéder à la page de contact.  La page de contact a la même mise en forme que la page d’accueil.  
    
    :::image type="complex" source="../media/beginners-css-external11.msft.png" alt-text="Page de contact" lightbox="../media/beginners-css-external11.msft.png":::
       Page de contact  
    :::image-end:::  
    
## Utiliser une infrastructure CSS  

Les **infrastructures CSS** sont des collections de styles intégrées par d’autres développeurs, qui simplifient la création de sites Web attractifs.  Au lieu de définir vous-même les styles, une infrastructure vous fournit une collection de styles que vous pouvez utiliser sur les éléments de la page.  

1.  Copiez le code suivant:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Accédez à l’onglet modification et collez le code dans `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-framework1.msft.png" alt-text="Lien vers l’infrastructure dans contact.html" lightbox="../media/beginners-css-framework1.msft.png":::
       Lien vers l’infrastructure dans `contact.html`  
    :::image-end:::  
    
1.  Ouvrez le `index.html` fichier et ajoutez-y le code.  
    
    :::image type="complex" source="../media/beginners-css-framework2.msft.png" alt-text="Lien vers l’infrastructure dans index.html" lightbox="../media/beginners-css-framework2.msft.png":::
       Lien vers l’infrastructure dans `index.html`  
    :::image-end:::  
    
1.  Revenez à l’onglet Live pour afficher vos modifications.  Même si la couleur d’arrière-plan de l' `<nav>` élément et la police des `<li>` `<a>` éléments et sont identiques, la police des autres éléments a changé.  
    
    :::image type="complex" source="../media/beginners-css-framework3.msft.png" alt-text="Une partie de la police de la page d’accueil a changé en raison de l’infrastructure." lightbox="../media/beginners-css-framework3.msft.png":::
       Une partie de la police de la page d’accueil a changé en raison de l’infrastructure.  
    :::image-end:::  
    
### Utiliser une classe  

Dans la dernière section, vous avez ajouté des données d’amorçage dans vos pages Web, ce qui a modifié les polices de certains éléments de votre site.  Les infrastructures CSS vous permettent d’apporter des modifications importantes à votre page avec peu de code.  Effectuez les opérations suivantes pour modifier votre en-tête.  

1.  Copiez l’extrait de code suivant.  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Ajoutez l’extrait de code précédent à votre `<header>` balise dans `index.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron1.msft.png" alt-text="Ajouter des classes dans index.html" lightbox="../media/beginners-css-jumbotron1.msft.png":::
       Ajouter des classes dans `index.html`  
    :::image-end:::  
    
1.  Ajoutez le code à votre `<header>` balise dans `contact.html` .  
    
    :::image type="complex" source="../media/beginners-css-jumbotron2.msft.png" alt-text="Ajouter des classes dans contact.html" lightbox="../media/beginners-css-jumbotron2.msft.png":::
       Ajouter des classes dans `contact.html`  
    :::image-end:::  
    
1.  Affichez vos modifications sous l’onglet Live.  Il y a une grande zone grise dans l’en-tête.  
    
    :::image type="complex" source="../media/beginners-css-jumbotron3.msft.png" alt-text="L’en-tête est désormais entouré d’un cadre gris." lightbox="../media/beginners-css-jumbotron3.msft.png":::
       L’en-tête est désormais entouré d’un cadre gris.  
    :::image-end:::  
    
### Comprendre les classes  

Les classes vous permettent d’affecter des collections de styles à des éléments arbitraires.  Utilisez l’extrait de code suivant pour appliquer plusieurs styles à l' `<header>` élément après l’avoir défini `class` `jumbotron` .  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

L’un des avantages d’une classe réside dans le fait qu’il vous permet d’appliquer des styles à tous les éléments souhaités.  Par exemple, supposons que vous vouliez définir la couleur d’arrière-plan de certains `<p>` éléments sur pourpre, mais pas sur tous les `<p>` éléments.  Utilisez l’extrait de code suivant pour définir le style d’une classe.  

```css
.custom-background {
  background-color: purple;
}
```  

Ensuite, appliquez la classe uniquement aux `<p>` éléments auxquels vous voulez appliquer un style.  

```html
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
<p>The text is not purple.</p>
<p class="custom-background">The text is purple.</p>
```  

### Aligner des éléments  

Procédez comme suit pour amorcer et fournir des classes permettant d’aligner des éléments.  

1.  Revenez à l’onglet Éditeur, puis ouvrez `index.html` .  
1.  Ajoutez `class="container-fluid"` à votre `<body>` indicateur.  
    
    :::image type="complex" source="../media/beginners-css-align1.msft.png" alt-text="Ajouter la classe Container-fluidiques" lightbox="../media/beginners-css-align1.msft.png":::
       Ajouter la `container-fluid` classe  
    :::image-end:::  
    
1.  Renvoyez `<nav>` vos `<main>` éléments et `<div class="row">` .  Assurez-vous d’entrer `</div>` après pour `</main>` fermer correctement la nouvelle balise.  
    
    :::image type="complex" source="../media/beginners-css-align2.msft.png" alt-text="Ajouter une ligne" lightbox="../media/beginners-css-align2.msft.png":::
       Ajouter une ligne  
    :::image-end:::  
    
1.  Ajoutez `class="col-3"` votre `<nav>` indicateur et `class="col-9"` votre `<main>` indicateur.  
    
    :::image type="complex" source="../media/beginners-css-align3.msft.png" alt-text="Ajouter les classes col-3 et col-9" lightbox="../media/beginners-css-align3.msft.png":::
       Ajouter les `col-3` `col-9` classes et  
    :::image-end:::  
    
1.  Affichez vos modifications sous l’onglet Live.  
    
    :::image type="complex" source="../media/beginners-css-align4.msft.png" alt-text="Le contenu de navigation est désormais à gauche du contenu principal" lightbox="../media/beginners-css-align4.msft.png":::
       Le contenu de navigation est désormais à gauche du contenu principal  
    :::image-end:::  
    
## Étapes suivantes  

Félicitations, vous avez réussi.  

*   La meilleure façon d’optimiser le développement Web consiste à créer des sites supplémentaires.  Ne vous inquiétez pas de casser votre contenu.  Amusez-vous et apprenez autant que possible.  
*   Pour en savoir plus sur le style de pages Web, voir [Présentation des feuilles CSS][MDNCssFirstSteps].  
*   Pour en savoir plus sur l’utilisation de DevTools pour tester la feuille de style en cascade d’une page, voir [découvrir comment afficher et modifier des feuilles CSS][DevtoolsCssIndex].  

<!--- image links --->  

[ImageNewStyleRuleIcon]: ../media/new-style-rule-icon.msft.png  

<!--- links  --->  

[DevtoolsBeginnersHtml]: ./html.md "DevTools pour les débutants: prenez en main HTML et le DOM | Documents Microsoft"  
[DevtoolsCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-cuisin-Amphibian | Problème"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Premiers pas dans la feuille de style CSS | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/beginners/css) et est créée par [Katherine Jackson][KatherineJackson] \ (Technical Writer Intern, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
