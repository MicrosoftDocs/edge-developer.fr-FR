---
description: Mise en place du code HTML et du DOM
title: 'DevTools pour les débutants: mise en place du code HTML et du DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/01/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, développement web, outils f12, devtools, devtools pour débutants, devtools HTML pour débutants, devtools DOM pour débutants, didacticiel devtools html, didacticiel devtools DOM, didacticiel devtools document object model
ms.openlocfilehash: a049ec500e22f89db3ab1e966b55d89c2ad682fe
ms.sourcegitcommit: 8f37c931ecde4d58223113f7e3b42d37cc3df97f
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/10/2021
ms.locfileid: "11643492"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools pour les débutants: mise en place du code HTML et du DOM  

Il s’agit du premier d’une série de didacticiels qui vous enseignent les principes de base du développement web. Découvrez un ensemble d’outils de développement web, nommés Microsoft Edge DevTools, qui peuvent augmenter votre productivité.  

Ce didacticiel décrit le code HTML et le [Modèle objet document](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model) \(DOM\). HTML est l’une des technologies de base du développement web. Il s’agit du langage qui contrôle la structure et le contenu des pages web. Le DOM est également lié à la structure et au contenu des pages web, ce dont nous parlerons ultérieurement.

## <a name="goals"></a>Objectifs  

Vous allez apprendre le développement web en construisant un site web.  Une fois que vous avez terminé tous les didacticiels de la série **DevTools pour les débutants**, votre site terminé peut ressembler à la figure suivante.  

:::image type="complex" source="media/beginners-html-finished.msft.png" alt-text="Site terminé" lightbox="media/beginners-html-finished.msft.png":::
   Site terminé  
:::image-end:::  

À la fin de ce didacticiel, vous devez comprendre les concepts suivants.  

*   Comment le code HTML et le DOM créent le contenu affiché sur les pages web.  
*   Comment Microsoft Edge DevTools peut vous aider à expérimenter les modifications HTML et DOM.  
*   Différence entre le code HTML et le DOM.  

Vous aurez également un site web de travail. Vous pouvez utiliser le site pour héberger votre cv ou votre blog.  

## <a name="prerequisites"></a>Conditions préalables  

Avant d’essayer ce didacticiel, remplissez les conditions préalables suivantes:  

*   Si vous ne connaissez pas le langage HTML, lisez [Mise en route du code HTML][MDNGettingStartedHtml].  
*   Téléchargez le navigateur web [Microsoft Edge][MicrosoftEdgeInsider].  Ce didacticiel utilise un ensemble d’outils de développement web, appelés Microsoft Edge DevTools, qui sont intégrés Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurer votre code  

Vous allez créer un site dans l’éditeur de code en ligne Glitch.  

1.  Ouvrez le [code source][GlitchAlluringShockIndex]. Cet onglet est appelé **onglet Éditeur ** tout au long de ce didacticiel.  
    
    :::image type="complex" source="media/beginners-html-setup1.msft.png" alt-text="Onglet Éditeur" lightbox="media/beginners-html-setup1.msft.png":::
       Onglet Éditeur  
    :::image-end:::  
    
1.  Choisissez **alluring-shock**. Le menu **Options Project** s’ouvre.  
    
    :::image type="complex" source="media/beginners-html-setup2.msft.png" alt-text="Menu Options Project" lightbox="media/beginners-html-setup2.msft.png":::
       Menu Options Project  
    :::image-end:::  
    
1.  Choisissez **remixer Project**. Glitch crée une copie du projet que vous pouvez modifier et génère de manière aléatoire un nouveau nom pour le projet. Le contenu est le même qu’auparavant.  
    
    :::image type="complex" source="media/beginners-html-setup3.msft.png" alt-text="Le projet remixé" lightbox="media/beginners-html-setup3.msft.png":::
       Le projet remixé  
    :::image-end:::  
    
1.  Si vous envisagez de suivre le didacticiel suivant de cette série, choisissez **Se connecter** à Glitch à l’aide de votre compte Facebook, GitHub ou Google; ou envoyez-vous un lien magique par e-mail. Si vous choisissez de ne pas vous connecter à un compte, vous ne pouvez pas modifier le projet après avoir fermé l'onglet Éditeur.

1.  Choisissez **Afficher**  \> **dans une nouvelle fenêtre**.  Un nouvel onglet s’ouvre et affiche la page en direct. Cet onglet est appelé **onglet en direct** tout au long de ce didacticiel.  
    
    :::image type="complex" source="media/beginners-html-setup4.msft.png" alt-text="Onglet en direct" lightbox="media/beginners-html-setup4.msft.png":::
       Onglet en direct  
    :::image-end:::  
    
## <a name="add-content"></a>Ajoutez du contenu  

Votre site a besoin d’informations supplémentaires. Pour ajouter du contenu, complétez les étapes suivantes.  

1. Dans l’**onglet Éditeur**, remplacez `<!-- You're "About Me" will go here.  -->` par `<h1>About Me</h1>`.  
    
    ```html
        ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                </main>
        ...
    ```  
    
    :::image type="complex" source="media/beginners-html-add1.msft.png" alt-text="Le nouveau code est mis en surbrillance dans l'onglet Éditeur." lightbox="media/beginners-html-add1.msft.png":::
        Le nouveau code est mis en surbrillance dans l'onglet Éditeur.  
    :::image-end:::  
    
1. Affichez vos modifications dans l’**onglet en direct**. Le texte `About Me` est visible sur la page. Le texte est plus grand que le texte qui l’entoure, car l’élément `<h1>` représente un titre 1.  Votre navigateur web affiche automatiquement les titres dans des tailles de police plus grandes.  
    
    :::image type="complex" source="media/beginners-html-add2.msft.png" alt-text="Le nouveau titre est visible dans l’onglet en direct" lightbox="media/beginners-html-add2.msft.png":::
       Le nouveau titre est visible dans l’onglet en direct  
    :::image-end:::  
    
1. Retournez dans l’**onglet Éditeur**, insérez `<p>I am learning web development. Recent accomplishments:</p>` sur la ligne ci-dessous `<h1>About Me</h1>`.  
    
    ```html
    ...
        <body>
            <p> Your site!</p>
                <main>
                    <h1>About Me</h1>
                    <p>I am learning web development. Recent accomplishments:</p>
                </main>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add3.msft.png" alt-text="Le code mis à jour est mis en surbrillance dans l'onglet Éditeur" lightbox="media/beginners-html-add3.msft.png":::
        Le code mis à jour est mis en surbrillance dans l'onglet Éditeur  
    :::image-end:::  
    
1. Affichez votre modification dans l’**onglet en direct.**

1. Retournez dans l'**onglet Éditeur**, ajoutez une liste de vos réalisations en utilisant le code suivant.
    
    ```html
    ...
    <p>I am learning web development.  Recent accomplishments:</p>
        <ul>
            <li>Learned how to set up my code in Glitch.</li>
            <li>Added content to my HTML.</li>
            <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
            <li>TODO: Learn the difference between HTML and the DOM.</li>
        </ul>
    ...
    ```  

    :::image type="complex" source="media/beginners-html-add4.msft.png" alt-text="Le code mis à jour est également mis en surbrillance dans l'onglet Éditeur" lightbox="media/beginners-html-add4.msft.png":::
        Le code mis à jour est également mis en surbrillance dans l'onglet Éditeur  
    :::image-end:::  

1. Affichez l’**onglet en direct** pour vous assurer que le nouveau contenu s’affiche correctement.  
    
    :::image type="complex" source="media/beginners-html-add5.msft.png" alt-text="La nouvelle liste est visible dans l’onglet en direct" lightbox="media/beginners-html-add5.msft.png":::
       La nouvelle liste est visible dans l’onglet en direct  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Expérimenter les modifications de contenu dans Microsoft Edge DevTools  

Si vous développez une page avec beaucoup de code HTML, il devient fastidieux de faire des allers-retours entre l’onglet Éditeur et l’onglet en direct pour voir vos modifications. Microsoft Edge DevTools vous permet d’expérimenter les modifications de contenu sans quitter l’**onglet en direct**.  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Découvrez la différence entre le code HTML et le DOM  

Avant de modifier le contenu Microsoft Edge DevTools, nous allons comprendre la différence entre HTML et le DOM. Procédez comme suit pour apprendre à partir d’un exemple.

1. Accédez à l’**onglet en direct**. Au bas de votre page, le texte `A new element!?!` s’affiche.  

    <!--
        :::image type="complex" source="media/beginners-html-dom1.msft.png" alt-text="At the bottom of the page the text A new element!?! displays" lightbox="media/beginners-html-dom1.msft.png":::
        At the bottom of the page the text `A new element!?!` is displays  
        :::image-end:::
    -->
    
1. Ouvrez l’**onglet Éditeur** et essayez de trouver le texte dans `index.html` . Le texte ne s'affiche pas dans cette vue.  

    <!--
        :::image type="complex" source="media/beginners-html-dom2.msft.png" alt-text="The mystery text A new element!?! is not found in index.html" lightbox="media/beginners-html-dom2.msft.png":::
        The mystery text `A new element!?!` is not found in `index.html`  
        :::image-end:::
    -->

1. Ouvrez l’**onglet en direct**, pointez sur `A new element!?!`, ouvrez le menu contextuel (clic droit), puis choisissez **Inspecter**.  
    
    :::image type="complex" source="media/beginners-html-dom3.msft.png" alt-text="Inspection d'un texte" lightbox="media/beginners-html-dom3.msft.png":::
       Inspection d'un texte  
    :::image-end:::  
    
    DevTools s’ouvre à côté de votre page. `<div>A new element!?!</div>` est mis en surbrillance. Bien que cette structure dans DevTools ressemble à du code HTML, il s’agit de l’**arborescence DOM**.  
    
    :::image type="complex" source="media/beginners-html-dom4.msft.png" alt-text="DevTools est ouvert à côté de la page" lightbox="media/beginners-html-dom4.msft.png":::
       DevTools est ouvert à côté de la page  
    :::image-end:::  
    
Lorsque votre page se charge, le navigateur utilise le HTML pour créer le contenu initial de la page. Le DOM représente le contenu actuel de la page, qui peut changer au fil du temps. 

Le `<div>A new element!?!</div>`contenu est ajouté à votre page grâce à la`<script src="new.js"></script>` balise située au bas de votre HTML. Cette balise entraîne l’exécuter du code JavaScript. En savoir plus sur JavaScript dans un [didacticiel ultérieur.](../javascript/index.md)

Pour l’instant, il s’agit d’un langage de script qui peut modifier le contenu de votre page. Dans ce cas, le code JavaScript ajoute `<div>A new element!?!</div>` à votre page. C’est pourquoi ce texte est affiché dans l’**onglet en direct**, mais pas dans le code HTML.  

### <a name="edit-the-dom"></a>Modifier le DOM  

Si vous souhaitez expérimenter rapidement les modifications de contenu sans jamais quitter l’onglet en direct, essayez DevTools.  

1.  Dans DevTools, pointez sur `Your site!`, ouvrez le menu contextuel (clic droit) et choisissez **Modifier en tant que HTML**.  
    
1.  Remplacez `<p>Your site!</p>`par le code suivant.  

```html
    ...
    <header>
        <p><b>Welcome to my site!</b></p>
        <button>Download my resume</button>
    </header>
    ...
```  

:::image type="complex" source="media/beginners-html-edit2.msft.png" alt-text="Mise à jour du nœud au format HTML" lightbox="media/beginners-html-edit2.msft.png":::
    Mise à jour du nœud au format HTML  
::image-end:::  

1.  Sélectionnez `Control`+`Enter` \(Windows, Linux\) ou `Command`+ `Enter` \(macOS\) pour enregistrer vos modifications, ou sélectionnez en dehors de la zone. Vos modifications s’afficheront automatiquement dans l’affichage en direct de votre page. Le texte `Your site!` a été remplacé par le nouveau contenu.  
    
    :::image type="complex" source="media/beginners-html-edit3.msft.png" alt-text="Le nouveau contenu s’affiche immédiatement sur la page" lightbox="media/beginners-html-edit3.msft.png":::
       Le nouveau contenu s’affiche immédiatement sur la page  
    :::image-end:::  
    
Ce flux de travail convient uniquement pour expérimenter les modifications de contenu. Si vous actualisez la page ou fermez l’onglet, vos modifications sont perdues. Si vous souhaitez enregistrer vos modifications, copiez manuellement le code dans votre fichier HTML. Les deux sections suivantes vous montrent d’autres façons de modifier le contenu de l’arborescence DOM.  

## <a name="reorder-nodes"></a>Réorganiser les nœuds

Vous pouvez également modifier l’ordre des nœuds DOM. Par exemple, sur votre page web, le menu de navigation se trouve près du bas. Pour le déplacer vers le haut, effectuez les étapes suivantes.  

1.  Recherchez le `<nav>` nœud dans l’**arborescence DOM** de DevTools.  
    
    :::image type="complex" source="media/beginners-html-reorder1.msft.png" alt-text="Le nœud de navigation est mis en surbrillance dans DevTools" lightbox="media/beginners-html-reorder1.msft.png":::
       Le nœud de navigation est mis en surbrillance dans DevTools  
    :::image-end:::  
    
1.  Faites glisser le `<nav>` nœud vers le haut, afin que le nœud soit le premier enfant après le nœud `<body>`.  
    
    :::image type="complex" source="media/beginners-html-reorder3.msft.png" alt-text="Le nœud de navigation se trouve en haut de la page" lightbox="media/beginners-html-reorder3.msft.png":::
        Le nœud de navigation se trouve en haut de la page  
    :::image-end:::  
    
### <a name="delete-a-node"></a>Supprimer un nœud

Vous pouvez également supprimer des nœuds de l’arborescence DOM. Effectuez les étapes suivantes.

1.  Dans **l’arborescence DOM**, choisissez `<div>A new element!?!</div>`. DevTools met en surbrillance le nœud. 
    
1.  Sélectionnez `Delete` la touche de votre clavier.  Le nœud `<div>A new element!?!</div>` est supprimé de l’arborescence DOM.  
    
    :::image type="complex" source="media/beginners-html-delete2.msft.png" alt-text="Le nœud a été supprimé" lightbox="media/beginners-html-delete2.msft.png":::
       Le nœud a été supprimé  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Copier vos modifications  

Vous avez presque terminé. Vous avez apporté quelques modifications à la page dans DevTools, mais elles ne sont pas enregistrées dans votre code source.  

1.  Actualisez l’ **onglet en direct**. Les modifications que vous avez apportées dans l’arborescence DOM disparaissent. En particulier, le texte `Your site!` revient en haut de la page et le texte `A new element!?!` revient en bas.  
    
    :::image type="complex" source="media/beginners-html-copy1.msft.png" alt-text="Les modifications que vous avez apportées ont disparu" lightbox="media/beginners-html-copy1.msft.png":::
       Les modifications que vous avez apportées ont disparu  
    :::image-end:::  
    
1.  Copiez le code suivant.  
    
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
    
1.  Retournez dans l'**onglet Éditeur** et remplacez le contenu de votre fichier `index.html` par le code que vous avez copié.  
    
    :::image type="complex" source="media/beginners-html-copy2.msft.png" alt-text="Apparence de votre fichier index.html" lightbox="media/beginners-html-copy2.msft.png":::
       Apparence de votre fichier `index.html`  
    :::image-end:::  
    
## <a name="next-steps"></a>Étapes suivantes  

*   Complétez le didacticiel suivant de cette série, [Prise en main avec CSS][DevToolsBeginnersCss], pour apprendre à styler votre page et expérimenter les modifications de style dans Microsoft Edge DevTools.  
*   Lisez [Introduction au DOM][MDNIntroductionDom] pour en savoir plus sur le DOM.  
*   Consultez un cours comme [Introduction au développement web][CourseraIntroductionToWebDevelopment] pour une expérience de développement web pratique.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools pour les débutants: Prise en main de CSS | Microsoft Docs"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Introduction au développement web | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - alluring-shock | Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Prise en main de HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction au DOM | MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page originale se trouve [ici](https://developers.google.com/web/tools/chrome-devtools/beginners/html) et a été créé par [Katherine Jackson][KatherineJackson] (rédactrice technique stagiaire, Chrome DevTools).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution 4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
