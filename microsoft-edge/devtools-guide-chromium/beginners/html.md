---
title: DevTools pour les débutants
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 8695fe1b2c5d78bd074447acd26a1f01a5833b2d
ms.sourcegitcommit: 8bfa239274e7a4856b961b9cf163b08d96463c10
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2020
ms.locfileid: "10581586"
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

# DevTools pour les débutants: commencez à utiliser HTML et au DOM   

Voici le premier d’une série de didacticiels pour vous apprendre les notions de base du développement Web.  Vous découvrirez également un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui peuvent augmenter votre productivité.  

Dans ce didacticiel, vous allez découvrir HTML et le DOM.  HTML est l’une des technologies fondamentales du développement Web.  Il s’agit de la langue qui contrôle la structure et le contenu de pages Web.  Le DOM est également lié à la structure et au contenu des pages Web, mais vous en saurez plus à ce sujet plus tard.  

## Définis   

Vous allez découvrir le développement Web en créant votre propre site Web.  Au moment où vous effectuez tous les didacticiels de la série *devtools pour les débutants* , votre site fini se présente comme **figure 1**.  

> ##### Figure1  
> Le site terminé  
> ![Le site terminé][ImageHtmlFinished]  

À la fin de ce didacticiel, vous allez comprendre les éléments suivants:  

*   Le code HTML et le DOM créent le contenu que vous voyez sur les pages Web.  
*   La façon dont Microsoft Edge DevTools peut vous aider à tester les modifications HTML et DOM.  
*   Différence entre HTML et le DOM.  

Vous disposez également d’un site Web réel.  Vous pouvez utiliser ce site pour héberger votre c.v. ou votre blog.  

## Conditions préalables   

Avant de suivre ce didacticiel, remplissez les conditions préalables suivantes:  

*   Si vous n’êtes pas familiarisé avec le format HTML, consultez la rubrique [mise en route de HTML][MDNGettingStartedHtml].  
*   Téléchargez le navigateur Web [Microsoft Edge][MicrosoftEdgeInsider] .  Ce didacticiel utilise un ensemble d’outils de développement Web, appelés Microsoft Edge DevTools, qui sont intégrés à Microsoft Edge.  

## Configurer votre code   

Vous envisagez de générer votre site dans un éditeur de code en ligne appelé erreur.  

1.  Ouvrez le [code source][GlitchAlluringShockIndex].  Cet onglet est appelé **onglet Éditeur** tout au long de ce didacticiel.  
    > ##### Figure 2  
    > Onglet Éditeur  
    > ![Onglet Éditeur][ImageHtmlSetup1]  

1.  Cliquez sur **alluring-choc**.  Le menu options de Project s’ouvre dans le coin supérieur gauche.  
    
    > #### Figure3  
    > Menu options de Project  
    > ![Menu options de Project][ImageHtmlSetup2]  
    
1.  Cliquez sur **Remix Project**.  Le problème crée une copie du projet que vous pouvez modifier et qui génère de manière aléatoire un nouveau nom pour le projet.  Le contenu est le même qu’auparavant.  
    
    > ##### Figure 4  
    > Le projet Remixed  
    > ![Le projet Remixed][ImageHtmlSetup3]  
    
1.  Si vous envisagez de terminer le didacticiel suivant de cette série, cliquez sur **se connecter** , puis connectez-vous à votre compte GitHub ou Facebook.  Si vous ne vous connectez pas, vous perdrez la possibilité de modifier ce projet une fois que vous avez fermé l’onglet modification.  
1.  Cliquez sur **Afficher** et sélectionnez **dans une nouvelle fenêtre**.  Un nouvel onglet s’ouvre et affiche la page dynamique.  Cet onglet est appelé **onglet dynamique** tout au long de ce didacticiel.  
    
    > ##### Figure 5  
    > Onglet Live  
    > ![Onglet Live][ImageHtmlSetup4]  
    
## Ajouter du contenu   

Votre site est assez vide.  Pour ajouter du contenu à votre présentation, procédez comme suit.  

1.  Dans l' **onglet Éditeur**, remplacez `<!-- You're "About Me" will go here.  -->` par `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### Figure 6  
    > Le nouveau code est mis en surbrillance dans l’onglet Éditeur  
    > ![Le nouveau code est mis en surbrillance dans l’onglet Éditeur][ImageHtmlAdd1]  
    
1.  Affichez vos modifications sous l' **onglet Live**.  Le texte `About Me` est visible sur la page.  Il est plus grand que le reste du texte, car l' `<h1>` élément représente un titre de section.  Dans votre navigateur Web, les titres sont automatiquement appliqués en taille de police plus grande.  
    
    > ##### Figure 7  
    > Le nouveau titre est affiché dans l’onglet Live  
    > ![Le nouveau titre est affiché dans l’onglet Live][ImageHtmlAdd2]  
    
1.  Dans l' **onglet Éditeur**, insérez `<p>I am learning HTML.  Recent accomplishments:</p>` l’image sur la ligne en dessous de laquelle vous venez d’entrer `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### Figure8  
    > Le nouveau code est mis en surbrillance dans l’onglet Éditeur  
    > ![Le nouveau code est mis en surbrillance dans l’onglet Éditeur][ImageHtmlAdd3]  
    
1.  Affichez votre modification sous l' **onglet Live**.  
1.  Dans l' **onglet Éditeur**, ajoutez la liste de vos réalisations:  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### Figure9  
    > Le nouveau code est mis en surbrillance dans l’onglet Éditeur  
    > ![Le nouveau code est mis en surbrillance dans l’onglet Éditeur][ImageHtmlAdd4]  
    
1.  Revenez à l' **onglet Live** pour vérifier que le nouveau contenu s’affiche correctement.  
    
    > ##### Figure10  
    > La nouvelle liste est affichée sous l’onglet Live  
    > ![La nouvelle liste est affichée sous l’onglet Live][ImageHtmlAdd5]  
    
## Tester les modifications de contenu dans Microsoft Edge DevTools   

Si vous développez une grande page à l’aide d’un grand nombre de fichiers HTML, vous pouvez imaginer qu’il peut être fastidieux de reculer entre l’onglet Éditeur et l’onglet actif de centaines de fois pour voir vos modifications, en particulier si vous ne savez pas exactement ce que vous voulez faire dans la page.  Microsoft Edge DevTools peut vous aider à tester du contenu sans quitter l’onglet Live.  

### Différences entre le format HTML et le DOM   

Avant de commencer à modifier votre contenu à partir de Microsoft Edge DevTools, il est utile de comprendre la différence entre le code HTML et le DOM.  Le meilleur moyen d’apprendre est, par exemple:  

1.  Accédez à l' **onglet Live**.  Le texte s’affiche en bas de la page `A new element!?!` .  
    
    > ###### Figure11  
    > En bas de la page, vous `A new element!?!` pouvez voir le texte  
    > ![En bas de la page, le texte!?! un nouvel élément est visible][ImageHtmlDom1]  
    
1.  Revenez à l' **onglet Éditeur** et essayez de Rechercher ce texte dans `index.html` .  Ce n’est pas là!  
    
    > ##### Figure12  
    > Le texte `A new element!?!` de mystère est introuvable dans `index.html`  
    > ![Le texte du mystère est un nouvel élément!?! est introuvable dans index. html][ImageHtmlDom2]  
    
1.  Revenez à l' **onglet Live**, cliquez avec le bouton droit `A new element!?!` , puis sélectionnez **inspecter**.  
    
    > ##### Figure13  
    > Inspecter du texte  
    > ![Inspecter du texte][ImageHtmlDom3]  
    
    DevTools s’ouvre à côté de votre page.  `<div>A new element!?!</div>` est en surbrillance bleue.  Même si cette structure dans DevTools ressemble à votre code HTML, il s’agit en réalité de l' **arborescence DOM**.  
    
    > ##### Figure14  
    > DevTools est ouvert parallèlement à la page  
    > ![DevTools est ouvert parallèlement à la page][ImageHtmlDom4]  
    
Lors du chargement de la page, le navigateur utilise votre code HTML pour créer le contenu *initial* de la page.  Le DOM représente le contenu *actuel* de la page, qui peut changer au fil du temps.  Le `<div>A new element!?!</div>` contenu mystérieux est ajouté à votre page en raison de la `<script src="new.js"></script>` balise située en bas de votre code html.  Cette balise entraîne l’exécution du code JavaScript.  En savoir plus sur JavaScript dans un didacticiel ultérieur, mais pour le considérer comme un langage de programmation qui peut changer le contenu de votre page.  Dans ce cas particulier, le code JavaScript est ajouté `<div>A new element!?!</div>` à votre page.  C’est la raison pour laquelle ce texte de mystère est visible sur votre page dynamique, mais pas dans votre code HTML.  

### Modifier le DOM   

Si vous voulez tester rapidement les changements de contenu sans quitter l’onglet Live, essayez DevTools.  

1.  Dans DevTools, cliquez avec le bouton droit, `Your site!` puis sélectionnez **modifier en HTML**.  

    > ##### Figure15  
    > Modification du nœud au format HTML  
    > ![Modification du nœud au format HTML][ImageHtmlEdit1]  
    
1.  Remplacez `<p>Your site!</p>` par le code ci-dessous.  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### Figure16  
    > Modification du nœud au format HTML  
    > ![Modification du nœud au format HTML][ImageHtmlEdit2]  
    
1.  `Control` + `Enter` `Command` + `Enter` Pour enregistrer vos modifications ou cliquez en dehors de la zone, appuyez sur \ (Windows \) ou \ (MacOS \).  Vos modifications apparaissent automatiquement dans le mode en direct de votre page.  Le texte `Your site!` a été remplacé par le nouveau contenu.  
    
    > ##### Figure17  
    > Le nouveau contenu apparaît immédiatement sur la page  
    > ![Le nouveau contenu apparaît immédiatement sur la page][ImageHtmlEdit3]  
    
Ce flux de travail est uniquement utile pour tester les modifications de contenu.  Si vous rechargez la page ou que vous fermez l’onglet, vos modifications sont supprimées définitivement.  Si vous utilisez ce flux de travail et que vous voulez enregistrer les modifications, vous devez les copier manuellement dans votre code HTML.  Les deux sections suivantes vous montrent davantage de moyens de changer le contenu de l’arborescence DOM.  

## Réorganiser les nœuds   

Vous pouvez également modifier l’ordre des nœuds DOM.  Par exemple, sur votre page Web, le menu de navigation est proche du bas.  Pour le déplacer vers le haut:  

1.  Recherchez le `<nav>` nœud dans l' **arborescence DOM** de devtools.  
    
    > ##### Figure 18  
    > Le nœud de navigation est surligné en bleu dans DevTools  
    > ![Le nœud de navigation est surligné en bleu dans DevTools][ImageHtmlReorder1]  
    
1.  Faites glisser le `<nav>` nœud vers le haut, de façon à ce qu’il s’agit du premier enfant sous le `<body>` nœud.  
    > ##### Figure 19  
    > Faire glisser le nœud de navigation vers le haut  
    > ![Faire glisser le nœud de navigation vers le haut][ImageHtmlReorder2]  
    
    Le `<nav>` nœud est désormais affiché en haut de votre page.  
    
    > ##### Figure 20  
    > Le nœud de navigation est en haut de la page  
    > ![Le nœud de navigation est en haut de la page][ImageHtmlReorder3]  
    
### Supprimer un nœud   

Vous pouvez également supprimer des nœuds de l’arborescence DOM.  

1.  Dans l' **arborescence DOM**, cliquez sur `<div>A new element!?!</div>` .  DevTools surligne le nœud bleu.  
    
    > ##### Figure 21  
    > Sélection du nœud à supprimer  
    > ![Sélection du nœud à supprimer][ImageHtmlDelete1]  
    
1.  Appuyez sur la `Delete` touche de votre clavier.  Le `<div>A new element!?!</div>` nœud est supprimé de votre arborescence DOM.  
    
    > ##### Figure 22  
    > Le nœud a été supprimé.  
    > ![Le nœud a été supprimé.][ImageHtmlDelete2]  
    
## Copiez vos modifications   

Vous avez presque terminé.  Vous avez apporté des modifications à votre page dans DevTools, mais celles-ci ne sont pas encore enregistrées dans votre code source.  

1.  Actualisez votre **onglet actif**.  Les modifications que vous avez apportées à l’arborescence DOM disparaissent.  Par exemple, le texte `Your site!` revient en haut de la page et le texte `A new element!?!` revient en bas.  
    
    > ##### Figure 23  
    > Les modifications que vous avez apportées ont disparu  
    > ![Les modifications que vous avez apportées ont disparu][ImageHtmlCopy1]  

1.  Copiez le code ci-dessous.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  Revenez à l' **onglet Éditeur** et remplacez le contenu de votre `index.html` fichier par le code que vous venez de copier.  
    
    > ##### Figure 24  
    > Aspect de votre `index.html` fichier  
    > ![Aspect de votre fichier index. html][ImageHtmlCopy2]  
    
## Étapes suivantes   

*   Suivez les étapes ci-dessous pour découvrir comment appliquer un [style à votre][DevToolsBeginnersCss]page et tester les modifications de style dans Microsoft Edge devtools.  
*   Lire [Introduction au DOM][MDNIntroductionDom] pour en savoir plus sur le DOM.  
*   Consultez un cours comme [Introduction au développement Web][CourseraIntroductionToWebDevelopment] pour bénéficier d’une expérience de développement Web plus pratique.  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Figure 1: site terminé"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Figure 2: onglet Éditeur"  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Figure 3: menu options de Project"  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Figure 4: projet Remixed"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Figure 5: onglet Live"  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Figure 6: le nouveau code est mis en surbrillance dans l’onglet Éditeur"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Figure 7: le nouveau titre est affiché dans l’onglet Live"  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Figure 8: le nouveau code est mis en surbrillance dans l’onglet Éditeur"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "Figure 9: le nouveau code est mis en surbrillance dans l’onglet Éditeur"  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Figure 10: la nouvelle liste est affichée sous l’onglet Live"  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "Figure 11: en bas de la page le texte!?! un nouvel élément est visible"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Figure 12: le texte du mystère est un nouvel élément!?! est introuvable dans index. html"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Figure 13: examen de texte"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Figure 14: DevTools est ouvert parallèlement à la page"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Figure 15: modification du nœud au format HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Figure 16: modification du nœud au format HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Figure 17: le nouveau contenu apparaît immédiatement sur la page"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Figure 18: le nœud de navigation est surligné en bleu dans DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "Figure 19: glissement du nœud de navigation vers le haut"  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Figure 20: le nœud de navigation est en haut de la page"  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Figure 21: sélection du nœud à supprimer"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Figure 22: le nœud a été supprimé"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Figure 23: les modifications que vous avez apportées ont disparu"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Figure 24: apparence du fichier index. html"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools pour les débutants: prendre en main CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Présentation du développement Web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index. html-alluring-choc | Problème"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Mise en route de HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/beginners/html) et est créée par [Katherine Jackson][KatherineJackson] \ (Technical Writer Intern, chrome devtools \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
