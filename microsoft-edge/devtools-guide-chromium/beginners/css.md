---
title: DevTools pour les débutants
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 0064f0427b6bd5689e888cccfe2c650492898bb2
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581593"
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

Voici le deuxième didacticiel d’une série de didacticiels qui vous explique les notions de base du développement Web et de Microsoft Edge DevTools.  Profitez d’une expérience pratique en créant votre propre site Web.  Il n’est pas nécessaire de terminer le premier didacticiel avant de procéder.  Vous pouvez commencer ici.  La [configuration de votre code](#set-up-your-code) vous montre comment procéder à la configuration.  

> [!NOTE]
> Ce didacticiel est conçu pour les débutants et est axé sur les notions **fondamentales du développement Web** et des notions de base de l’utilisation de devtools pour tester les feuilles CSS.  Si vous avez besoin d’un didacticiel destiné uniquement à DevTools, voir [découvrir comment afficher et modifier des feuilles CSS][DevtoolsCssIndex].  

Votre site se présente actuellement comme suit:  

> ##### Figure1  
> Aspect de votre site  
> ![Aspect de votre site][ImageCssIntro1]  

À la fin du didacticiel, il se présente comme suit:  

> ##### Figure 2  
> Aspect de votre site à la fin du didacticiel  
> ![Aspect de votre site à la fin du didacticiel][ImageCssIntro2]  

## Définis   

À la fin de ce didacticiel, vous allez comprendre les éléments suivants:  

*   Comment utiliser les feuilles CSS pour appliquer un style à une page Web.  
*   Comment utiliser Microsoft Edge DevTools pour tester les feuilles CSS.  
*   Différence entre les infrastructures CSS et CSS.  

Vous disposez également d’un site Web réel.  

## Conditions préalables   

Avant de suivre ce didacticiel, remplissez les conditions préalables suivantes:  

*   Pour plus d’informations, [consultez prise en main de HTML et du DOM][DevToolsBeginnersHtml] ou assurez-vous que vous comprenez bien html et le DOM semblable à ce qui est enseigné dans ce didacticiel.  
*   Téléchargez le navigateur Web [Microsoft Edge][MicrosoftEdgeInsider] .  Ce didacticiel utilise un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.  

## Configurer votre code   

Pour commencer à créer votre site, vous devez configurer votre code:  

1.  **Si vous avez déjà effectué le premier didacticiel de cette série, ignorez cette section.  Continuez à utiliser votre code à partir du dernier didacticiel, de [la mise en route de HTML et du DOM][DevToolsBeginnersHtml].**  
1.  Ouvrez le [code source][GlitchCookedAmphibianIndex].  Cet onglet de votre navigateur sera appelé **onglet édition**.  
    
    > ##### Figure3  
    > Onglet édition  
    > ![Onglet édition][ImageCssSetup1]  
    
1.  Cliquez sur **cuit-Amphibian**.  Un menu s’ouvre.  
    
    > ##### Figure 4  
    > Menu options de Project  
    > ![Menu options de Project][ImageCssSetup2]  

1.  Cliquez sur **Remix Project**.  Le problème crée une copie du projet que vous pouvez modifier.  
    
    > [!NOTE]
    > Le problème génère un nom aléatoire pour le nouveau projet.  
    
1.  Cliquez sur **Afficher** et sélectionnez **dans une nouvelle fenêtre**.  Un autre onglet s’ouvre en mode en direct de votre site.  L' **onglet Live**de votre navigateur s’appelle.  
    
    > ##### Figure 5  
    > Onglet Live  
    > ![Onglet Live][ImageCssSetup3]  

## Comprendre CSS   

**CSS** est un langage informatique qui détermine la disposition et le style des pages Web.  Par exemple, voici un paragraphe avec une bordure:  

> ##### Figure 6  
> Style avec CSS  
> ![Style avec CSS][ImageCssStyled]  

Voici le code HTML et CSS utilisé pour créer ce paragraphe:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` C’est probablement une nouveauté.  Le reste devrait vous être familier.  Si ce n’est pas le cas, terminez- [le en utilisant le code HTML et le DOM][DevToolsBeginnersHtml] avant d’essayer ce didacticiel.  

## Ajouter des styles intralignes   

Utilisez des **styles intralignes** lorsque vous souhaitez appliquer des styles à un seul élément.  Essayez-le maintenant:  

1.  Revenez à l’onglet modification et ouvrez `index.html` .  
    
    > ##### Figure 7  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  Ajoutez `style="background-color: aliceblue;"` à votre `<nav>` .  Dans le bloc de code ci-dessous, la quatrième ligne de code est celle que vous devez modifier.  Le reste est là pour vous permettre de vérifier que vous insérez le nouveau code au bon endroit.  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  Accédez à l' **onglet Live** pour afficher les modifications.  L’arrière-plan de la `<nav>` section est désormais bleu.  
    
    > ##### Figure8  
    > La couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue  
    > ![La couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue][ImageCssInline2]  

## Réutiliser les styles sur une seule page à l’aide de feuilles de style internes   

Auparavant, vous avez vu un style intraligne qui appliquait un style à une `<p>` balise unique comme suit:  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Que faire si vous souhaitez que tous les `<p>` éléments d’une page Web soient stylisés de la même manière?  Vous devez copier et coller le code dans chaque `<p>` balise unique de votre site.  C’est un peu de temps et d’efforts.  Et si vous avez besoin d’effectuer une modification, vous devrez à nouveau modifier chaque balise.  Les **feuilles de style internes** vous permettent d’écrire votre CSS une seule fois pour qu’elle s’applique à plusieurs éléments.  Essayez-le maintenant:  

1.  Dans l’onglet Live, cliquez sur **contact** pour accéder à la page de contact.  Notez la police **Accueil** et **contact**.  
    
    > ##### Figure9  
    > Page de contact  
    > ![Page de contact][ImageCssInternal1]  

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
1.  Cliquez sur le **contact** pour revenir à la page de contact.  La police **Accueil** et **contact** a changé.  
    
    > ##### Figure10  
    > La police des liens accueil et contact a changé  
    > ![La police des liens accueil et contact a changé][ImageCssInternal2]  
    
### Comprendre les feuilles de style internes   

Les feuilles de style internes s’appliquent aux styles à l’aide de **sélecteurs**.  Les sélecteurs sont des modèles qui peuvent être appliqués à un ou plusieurs éléments HTML.  Par exemple, dans le code précédent:  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` est un sélecteur qui se traduit par «any contenant `<li>` `<a>` ».  Le navigateur modifie la police des liens **Accueil** et **contact** , car ils correspondent à ce modèle.  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` est une **déclaration**.  Une déclaration est constituée de deux parties: une **propriété** et une **valeur**.  `font-family` est la propriété et `'Courier New', Courier, serif` est la valeur de cette propriété.  La propriété décrit une méthode générale permettant de modifier le style de l’élément, et la valeur indique exactement le changement.  Par exemple, `font-family: 'Courier New', Courier, serif` donne au navigateur cette instruction: "définissez la police des éléments qui correspondent au modèle `li a` `'Courier New'` .  Si cette police n’est pas disponible, utilisez `Courier` .  Si ce n’est pas le cas, utilisez `serif` .»  

### Ajouter plusieurs sélecteurs à un groupe de règles   

Un bloc de code CSS tel que celui qui apparaît ci-dessous est appelé **RuleSet**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Utilisez des points-virgules pour ajouter plusieurs sélecteurs à un RuleSet.  Essayez-le maintenant:  

1.  Dans l' **onglet Éditeur**, ouvrez `contact.html` .  
1.  Après `li a` type `, h1` .  

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

    Cela indique au navigateur d' `<h1>` avoir des éléments style de la même manière qu’il s’agit d’éléments qui correspondent au modèle `li a` .  
    
1.  Accédez à l' **onglet Live**.  
1.  Cliquez sur le lien de **contact** pour revenir à la page de contact.  Maintenant, **Contactez-moi!** a la même police que les liens de navigation.  
    
    > ##### Figure11  
    > Le texte’contactez-moi! ' possède désormais la même police que les liens accueil et contact  
    > ![Le texte me contacter.  possède désormais la même police que les liens accueil et contact][ImageCssMultiple1]  

## Expérimentez avec DevTools   

À mesure que vous poursuivez le développement Web principal, vous constaterez que les feuilles CSS peuvent être difficiles à utiliser.  Vous écrirez des feuilles CSS et vous attendez à ce qu’elle s’affiche de façon unique, mais le navigateur effectue une opération totalement différente.  Microsoft Edge DevTools vous permet d’expérimenter facilement les modifications et de voir immédiatement l’incidence de ces modifications sur la page.  

### Ajouter une déclaration à une règle existante dans DevTools   

Lorsque vous souhaitez effectuer une itération sur le style d’un élément existant, ajoutez une déclaration à un RuleSet existant.  Essayez-le maintenant:  

1.  Cliquez avec le bouton droit sur le lien **Accueil** et sélectionnez **inspecter**.  
    
    > ##### Figure12  
    > Examen du lien Accueil  
    > ![Examen du lien Accueil][ImageCssAdd1]  
    
    DevTools s’ouvre à côté de votre page.  Le code qui représente le lien Accueil `<a href="/">Home</a>` est surligné en bleu dans l’arborescence DOM.  Pour cela, vous devez être familiarisé [avec la mise en route de HTML et du DOM][DevToolsBeginnersHtml].  Dans l’onglet **styles** sous l’arborescence DOM, vous pouvez voir la `font-family: 'Courier New', Courier, serif` déclaration que vous avez `contact.html` précédemment ajoutée.  
    
    > ##### Figure13  
    > L’onglet styles se trouve sous l’arborescence DOM  
    > ![L’onglet styles se trouve sous l’arborescence DOM][ImageCssAdd2]  
    
    Si votre fenêtre DevTools est large, l’onglet styles se trouve à droite de l’arborescence DOM.  
    
    > ##### Figure14  
    > Onglet styles à droite de l’arborescence DOM  
    > ![Onglet styles à droite de l’arborescence DOM][ImageCssAdd3]  
    
1.  Cliquez sur l’espace blanc ci-dessous `font-family: 'Courier New', Courier, Serif` pour ajouter une nouvelle déclaration.  
    
    > ##### Figure15  
    > Ajout d’une nouvelle déclaration  
    > ![Ajout d’une nouvelle déclaration][ImageCssAdd4]  
    
1.  Tapez `color` , puis appuyez sur `Enter` .  L’interface utilisateur de saisie semi-automatique suggère des options au fur et à mesure que vous tapez.  
    
    > ##### Figure16  
    > Saisie `color`  
    > ![Entrer une couleur][ImageCssAdd5]  

1.  Tapez `magenta` , puis appuyez de `Enter` nouveau.  Tout le texte de la page de contact est désormais magenta.  
    
    > ##### Figure17  
    > Saisie `magenta`  
    > ![Saisie de magenta][ImageCssAdd6]  
    
### Modifier une déclaration dans DevTools   

Vous pouvez également modifier les déclarations existantes dans DevTools.  Essayez-le maintenant:  

1.  Cliquez sur le carré magenta en regard de `magenta` .  Un sélecteur de couleur apparaît.  
    
    > ##### Figure 18  
    > Sélecteur de couleurs  
    > ![Sélecteur de couleurs][ImageCssEdit1]  
    
1.  Utilisez le sélecteur de couleurs pour remplacer le texte de la police par une couleur de votre choix.  
    
    > ##### Figure 19  
    > Modification de la couleur de police en violet grâce au sélecteur de couleurs  
    > ![Modification de la couleur de police en violet grâce au sélecteur de couleurs][ImageCssEdit2]  

### Ajouter un nouveau RuleSet dans DevTools   

Vous pouvez également ajouter de nouvelles règles dans DevTools.  Essayez-le maintenant:  

1.  Cliquez sur **nouvelle règle** de style nouvelle règle de ![ style ][ImageNewStyleRuleIcon] en regard de **. CLS**.  Un RuleSet vide apparaît avec `a` le sélecteur.  
    
    > ##### Figure 20  
    > Ajout d’une nouvelle règle  
    > ![Ajout d’une nouvelle règle][ImageCssRule1]  
    
1.  Remplacer `a` par `a:hover` .  
    
    > ##### Figure 21  
    > Remplacement `a` par `a:hover`  
    > ![Remplacement de a avec a:hover][ImageCssRule2]  
    
    `:hover` est une **Pseudo-classe**.  Utilisez des Pseudo-classes pour appliquer des styles aux éléments spécifiques.  Par exemple, le `a:hover` style n’est appliqué que lorsque vous pointez sur un `<a>` élément.  
    
1.  Cliquez entre les crochets pour ajouter une nouvelle déclaration.  
1.  Tapez `background-color` le nom de la déclaration et appuyez sur `Enter` .  
    
    > ##### Figure 22  
    > Saisie `background-color`  
    > ![Saisie d’une couleur d’arrière-plan][ImageCssRule3]  
    
1.  Tapez `green` la valeur de la déclaration, puis appuyez sur `Enter` .  
    
    > ##### Figure 23  
    > Saisie `green`  
    > ![Saisie de texte vert][ImageCssRule4]  
    
1.  Positionnez le pointeur de la souris sur le lien **Accueil** .  L’arrière-plan du lien devient vert.  
    
    > ##### Figure 24  
    > Survol du lien Accueil pour afficher son arrière-plan vert  
    > ![Survol du lien Accueil pour afficher son arrière-plan vert][ImageCssRule5]  
    
## Réutiliser les styles entre les pages à l’aide de feuilles de style externes   

Auparavant, vous avez ajouté cette feuille de style interne aux `contact.html` éléments suivants:  

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

Que faire si vous souhaitez changer de style `index.html` ?  Que se passe-t-il si vous aviez un *millier* de pages et que vous souhaitez appliquer ces styles à tous les éléments?  Vous devez copier et coller cette feuille de style interne dans chaque page Web de votre site.  Les **feuilles de style externes** vous permettent d’écrire votre CSS une seule fois sur plusieurs pages.  Essayez-le maintenant:  

1.  Tout d’abord, rechargez l’onglet Live pour supprimer les modifications que vous avez apportées dans DevTools.  
    
    > ##### Figure 25  
    >  Après le rechargement de la page, les modifications apportées à DevTools ont disparu  
    > ![ Après le rechargement de la page, les modifications apportées à DevTools ont disparu][ImageCssExternal01]  
    
1.  Revenez à l' **onglet Éditeur** , puis ouvrez `contact.html` .  
    
    > ##### Figure 26  
    > `contact.html`  
    > ![contact. html][ImageCssExternal02]  
    
1.  Supprimez tous `<style>` les éléments entre et `</style>` , y compris `<style>` et `</style>` .  
    
    > ##### Figure 27  
    > La balise de style a été supprimée  
    > ![La balise de style a été supprimée][ImageCssExternal03]  
    
1.  Accédez à `index.html` la balise et supprimez- `style="background-color: aliceblue;"` la `<nav>` .  Vous avez supprimé toutes les feuilles CSS que vous avez précédemment ajoutées à votre site.  
    
    > ##### Figure 28  
    > Le style intraligne a été supprimé de l’élément navigation  
    > ![Le style intraligne a été supprimé de l’élément navigation][ImageCssExternal04]  

1.  Cliquez sur **nouveau fichier**.  
    
    > ##### Figure 29  
    > Boîte de dialogue nouveau fichier  
    > ![Boîte de dialogue nouveau fichier][ImageCssExternal05]  
    
1.  Remplacez `cool-file.js` par `style.css` , puis cliquez sur **Ajouter un fichier**.  
    
    > ##### Figure 30  
    > Saisie `style.css`  
    > ![Saisie de styles. CSS][ImageCssExternal06]  
    
1.  Collez ce code dans les `style.css` éléments suivants:  
    
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
    
    > ##### Figure 31  
    > Ajouter du code à `style.css`  
    > ![Ajouter du code à style. CSS][ImageCssExternal07]  
    
    À ce stade, vous avez créé une feuille de style externe, mais votre code HTML ne sait pas encore qu’il existe.  
    
1.  Ouvrir `index.html` .  
1.  Ajoutez `<link rel="stylesheet" href="style.css">` à votre code html.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### Figure 32  
    > Liaison à `style.css`  
    > ![Liaison à style. CSS][ImageCssExternal08]  

1.  Accédez à `contact.html` l’emplacement du lien et ajoutez-le.  
    
    > ##### Figure 33  
    > Liaison vers `style.css` dans `contact.html`  
    > ![Liaison vers style. CSS dans le fichier contact. html][ImageCssExternal09]  

1.  Accédez à l' **onglet Live**.  La page d’accueil possède désormais la même police que la dernière section et une section de navigation bleue.  
    
    > ##### Figure 34  
    > Page d’accueil  
    > ![Page d’accueil][ImageCssExternal10]  
    
1.  Cliquez sur le lien de **contact** pour accéder à la page de contact.  La page de contact a la même mise en forme que la page d’accueil.  
    
    > ##### Figure 35  
    > Page de contact  
    > ![Page de contact][ImageCssExternal11]  
    
## Utiliser une infrastructure CSS   

Les **infrastructures CSS** sont des collections de styles intégrées par d’autres développeurs, qui simplifient la création de sites Web attractifs.  Au lieu de définir vous-même les styles, une infrastructure vous donne une collection de styles que vous pouvez utiliser sur les éléments de la page.  

1.  Copiez le code suivant:  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Accédez à l’onglet modification et collez le code dans `contact.html` .  
    
    > ##### Figure 36  
    > Liaison vers l’infrastructure dans `contact.html`  
    > ![Liaison vers l’infrastructure dans le fichier contact. html][ImageCssFramework1]  
    
1.  Collez également le code `index.html` .  
    
    > ##### Figure 37  
    > Liaison vers l’infrastructure dans `index.html`  
    > ![Liaison vers l’infrastructure dans index. html][ImageCssFramework2]  
    
1.  Revenez à l’onglet Live pour afficher vos modifications.  Même si la couleur d’arrière-plan de la `<nav>` police et la police des `li a` éléments sont identiques, la police des autres éléments a changé.  
    
    > ##### Figure 38  
    > Une partie de la police de la page d’accueil a changé en raison de l’infrastructure.  
    > ![Une partie de la police de la page d’accueil a changé en raison de l’infrastructure.][ImageCssFramework3]  

### Utiliser une classe   

Dans la dernière section, vous avez ajouté des données d’amorçage dans vos pages Web, ce qui a modifié les polices de certains éléments de votre site.  Les infrastructures CSS vous permettent d’apporter des modifications importantes à votre page avec peu de code.  Essayez-le maintenant en modifiant votre en-tête:  

1.  Copiez ce code:  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Ajoutez ce code à votre `<header>` balise dans `index.html` .  
    
    > ##### Figure 39  
    > Ajouter des classes dans `index.html`  
    > ![Ajout de classes dans index. html][ImageCssJumbotron1]  
    
1.  Ajoutez le code à votre `<header>` balise `contact.html` .  
    
    > ##### Figure 40  
    > Ajouter des classes dans `contact.html`  
    > ![Ajout de classes dans contacts. html][ImageCssJumbotron2]  
    
1.  Affichez vos modifications sous l’onglet Live.  Il y a une grande zone grise dans votre en-tête.  
    
    > ##### Figure 41  
    > L’en-tête est désormais entouré d’un cadre gris.  
    > ![L’en-tête est désormais entouré d’un cadre gris.][ImageCssJumbotron3]  
    
### Comprendre les classes   

Les classes vous permettent d’affecter des collections de styles à des éléments arbitraires.  Par exemple, en définissant l' `class` attribut des `<header>` balises pour `jumbotron` appliquer les styles suivants aux éléments suivants:  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

L’un des avantages des classes réside dans le fait qu’ils vous permettent d’appliquer des styles à tous les éléments souhaités.  Par exemple, supposons que vous vouliez définir la couleur d’arrière-plan de *certains* `<p>` éléments sur pourpre, mais pas sur la *totalité* de ces éléments.  Vous pouvez définir le style dans une classe:  

```css
.custom-background {
  background-color: purple;
}
```  

Puis appliquez la classe uniquement aux `<p>` éléments auxquels vous voulez appliquer un style:  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### Aligner des éléments   

Le bootstrap fournit également des classes permettant d’aligner des éléments.  Essayez-le maintenant:  

1.  Revenez à l’onglet Éditeur, puis ouvrez `index.html` .  
1.  Ajoutez `class="container-fluid"` à votre `<body>` indicateur.  
    
    > ##### Figure 42  
    > Ajout de la `container-fluid` classe  
    > ![Ajout de la classe Container-fluidiques][ImageCssAlign1]  

1.  Renvoyez `<nav>` vos `<main>` éléments et `<div class="row">` .  Assurez-vous d’entrer `</div>` après pour `</main>` fermer correctement la nouvelle balise.  
    
    > ##### Figure 43  
    > Ajout d’une ligne  
    > ![Ajout d’une ligne][ImageCssAlign2]  
    
1.  Ajoutez `class="col-3"` votre `<nav>` indicateur et `class="col-9"` votre `<main>` indicateur.  
    
    > ##### Figure 44  
    > Ajout des `col-3` `col-9` classes et  
    > ![Ajout des classes col-3 et col-9][ImageCssAlign3]  
    
1.  Affichez vos modifications sous l’onglet Live.  
    
    > ##### Figure 45  
    > Le contenu de navigation est désormais à gauche du contenu principal  
    > ![Le contenu de navigation est désormais à gauche du contenu principal][ImageCssAlign4]  
    
## Étapes suivantes   

Félicitations!  C’est terminé!  

*   La meilleure façon d’optimiser le développement Web consiste à créer des sites supplémentaires.  Ne vous inquiétez pas de casser votre contenu.  Amusez-vous et découvrez autant que vous le pouvez.  
*   Pour en savoir plus sur le stylisation des pages Web, voir [Présentation de CSS][MDNCssFirstSteps] .  
*   Pour plus d’informations sur l’utilisation de DevTools dans le cadre d’une feuille de style CSS de page, consultez notre didacticiel sur l' [affichage et la modification][DevtoolsCssIndex] de la feuille de route.  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Figure 1: à quoi ressemble votre site"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "Figure 2: apparence de votre site à la fin du didacticiel"  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Figure 3: onglet édition"  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Figure 4: menu options de Project"  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Figure 5: onglet Live"  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Figure 6: styles avec CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Figure 7: index. html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Figure 8: la couleur d’arrière-plan derrière les liens accueil et contact est désormais bleue"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Figure 9: page de contact"  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Figure 10: la police des liens accueil et contact a changé"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Figure 11: le texte «contactez-moi!» a désormais la même police que les liens accueil et contact."  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Figure 12: examen du lien Accueil"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Figure 13: l’onglet styles se trouve sous l’arborescence DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Figure 14: onglet styles à droite de l’arborescence DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Figure 15: ajout d’une nouvelle déclaration"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Figure 16: couleur de frappe"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Figure 17: saisie de magenta"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Figure 18: sélecteur de couleurs"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "Figure 19: modification de la couleur de police en violet avec le sélecteur de couleurs"  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Figure 20: ajout d’une nouvelle règle"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Figure 21: remplacement de a par a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Figure 22: saisie de la couleur d’arrière-plan"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Figure 23: saisie en vert"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Figure 24: survol du lien Accueil pour afficher son arrière-plan vert"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Figure 25: après le rechargement de la page, les modifications apportées à DevTools ont disparu"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Figure 26: contact. html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Figure 27: la balise de style a été supprimée"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Figure 28: le style intraligne a été supprimé de l’élément navigation"  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Figure 29: boîte de dialogue nouveau fichier"  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Figure 30: saisie de style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Figure 31: ajout de code au style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Figure 32: création d’un lien vers style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Figure 33: création d’un lien vers style. CSS dans le fichier contact. html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Figure 34: page d’accueil"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Figure 35: page de contact"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Figure 36: création d’un lien vers l’infrastructure dans le fichier contact. html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Figure 37: liaisons vers l’infrastructure dans index. html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Figure 38: une partie de la police de la page d’accueil a changé en raison de l’infrastructure"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Figure 39: ajout de classes dans index. html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Figure 40: ajout de classes dans contact. html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Figure 41: l’en-tête est désormais entouré d’un cadre gris"  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Figure 42: ajout de la classe Container-fluidiques"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Figure 43: ajout d’une ligne"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Figure 44: ajout des classes col-3 et col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Figure 45: le contenu de navigation est désormais à gauche du contenu principal"  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools pour les débutants: commencez à utiliser HTML et au DOM"  
[DevtoolsCssIndex]: ../css/index.md "Découvrir comment afficher et modifier des feuilles CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index. html-cuit-Amphibian | Problème"  

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
