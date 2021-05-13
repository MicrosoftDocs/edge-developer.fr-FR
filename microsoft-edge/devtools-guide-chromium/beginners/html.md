---
description: Prise en main html et le DOM
title: 'DevTools pour les débutants : mise en place du code HTML et du DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft Edge, développement web, outils f12, devtools
ms.openlocfilehash: d2893021f5e19ffb714215b27edadba08c8d6f71
ms.sourcegitcommit: 7945939c29dfdd414020f8b05936f605fa2b640e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/13/2021
ms.locfileid: "11564566"
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
# <a name="devtools-for-beginners-get-started-with-html-and-the-dom"></a>DevTools pour les débutants : mise en place du code HTML et du DOM  

Il s’agit du premier d’une série de didacticiels qui vous enseignent les principes de base du développement web.  Découvrez un ensemble d’outils de développement web, nommés Microsoft Edge DevTools, qui peuvent augmenter votre productivité.  

Dans ce didacticiel particulier, vous découvrirez le code HTML et le DOM.  HTML est l’une des technologies de base du développement web.  Il s’agit du langage qui contrôle la structure et le contenu des pages web.  Le DOM est également lié à la structure et au contenu des pages web. En savoir plus à ce sujet ultérieurement.  

## <a name="goals"></a>Objectifs  

Vous allez apprendre le développement web en construisant réellement votre propre site web.  Une fois que vous avez terminé tous les didacticiels de la série **DevTools for Beginners,** votre site terminé peut ressembler à la figure suivante.  

:::image type="complex" source="../media/beginners-html-finished.msft.png" alt-text="Site terminé" lightbox="../media/beginners-html-finished.msft.png":::
   Site terminé  
:::image-end:::  

À la fin de ce didacticiel, vous devez comprendre les rubriques suivantes.  

*   Comment le code HTML et le DOM créent le contenu affiché sur les pages web.  
*   Comment Microsoft Edge DevTools peut vous aider à expérimenter les modifications HTML et DOM.  
*   Différence entre le code HTML et le DOM.  

Vous avez également un site web réel.  Vous pouvez utiliser le site pour héberger votre cv ou votre blog.  

## <a name="prerequisites"></a>Conditions préalables  

Avant d’essayer ce didacticiel, remplissez les conditions préalables suivantes :  

*   Si vous ne connaissez pas le langage HTML, lisez [La mise en place du code HTML.][MDNGettingStartedHtml]  
*   Téléchargez le [Microsoft Edge][MicrosoftEdgeInsider] navigateur web.  Ce didacticiel utilise un ensemble d’outils de développement web, appelés Microsoft Edge DevTools, qui sont intégrés Microsoft Edge.  

## <a name="set-up-your-code"></a>Configurer votre code  

Vous allez créer votre site dans un éditeur de code en ligne appelé Glitch.  

1.  Ouvrez le [code source.][GlitchAlluringShockIndex]  Cet onglet est appelé onglet **Éditeur tout** au long de ce didacticiel.  
    
    :::image type="complex" source="../media/beginners-html-setup1.msft.png" alt-text="Onglet Éditeur" lightbox="../media/beginners-html-setup1.msft.png":::
       Onglet Éditeur  
    :::image-end:::  
    
1.  Choisissez **alluring-en-préc**.  Le menu Project Options s’ouvre dans le coin supérieur gauche.  
    
    :::image type="complex" source="../media/beginners-html-setup2.msft.png" alt-text="Menu Options Project’équipe" lightbox="../media/beginners-html-setup2.msft.png":::
       Menu Options Project’équipe  
    :::image-end:::  
    
1.  Choisissez **Project**.  Glitch crée une copie du projet que vous pouvez modifier et génère de manière aléatoire un nouveau nom pour le projet.  Le contenu est le même qu’auparavant.  
    
    :::image type="complex" source="../media/beginners-html-setup3.msft.png" alt-text="Le projet en cours" lightbox="../media/beginners-html-setup3.msft.png":::
       Le projet en cours  
    :::image-end:::  
    
1.  Si vous prévoyez d’effectuer le didacticiel suivant de cette série, choisissez Se connectez et connectez-vous à Glitch avec votre compte GitHub ou Facebook. ****  Si vous choisissez de ne pas vous inscrire à votre compte, vous perdez la possibilité de modifier le projet après avoir fermé l’onglet Modification.  
1.  Choose **Show** and choose **In a New Window**.  Un nouvel onglet s’ouvre et vous montre la page en direct.  Cet onglet est appelé onglet **en direct tout** au long de ce didacticiel.  
    
    :::image type="complex" source="../media/beginners-html-setup4.msft.png" alt-text="Onglet en direct" lightbox="../media/beginners-html-setup4.msft.png":::
       Onglet en direct  
    :::image-end:::  
    
## <a name="add-content"></a>Ajouter du contenu  

Votre site est assez vide.  Suivez les étapes ci-dessous pour y ajouter du contenu.  

1.  Dans **l’onglet Éditeur,** `<!-- You're "About Me" will go here.  -->` remplacez par `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add1.msft.png" alt-text="Le nouveau code est mis en surbrillant dans l’onglet Éditeur" lightbox="../media/beginners-html-add1.msft.png":::
             Le nouveau code est mis en surbrillant dans l’onglet Éditeur  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Affichez vos modifications dans **l’onglet en direct.**  Le texte `About Me` est visible sur la page.  Texte plus grand que le texte qui l’entoure, car `<h1>` l’élément représente un en-tête de section.  Votre navigateur web styles automatiquement les titres dans des tailles de police plus grandes.  
    
    :::image type="complex" source="../media/beginners-html-add2.msft.png" alt-text="Le nouveau titre est visible dans l’onglet en direct" lightbox="../media/beginners-html-add2.msft.png":::
       Le nouveau titre est visible dans l’onglet en direct  
    :::image-end:::  
    
1.  De retour dans **l’onglet éditeur**, `<p>I am learning HTML.  Recent accomplishments:</p>` insérez sur la ligne ci-dessous où vous avez placé `<h1>About Me</h1>` .  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add3.msft.png" alt-text="Le code mis à jour est mis en surbrillant dans l’onglet Éditeur" lightbox="../media/beginners-html-add3.msft.png":::
             Le code mis à jour est mis en surbrillant dans l’onglet Éditeur  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
1.  Affichez votre modification dans **l’onglet en direct.**  
1.  De retour dans **l’onglet Éditeur,** ajoutez une liste de vos réussites :  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-add4.msft.png" alt-text="Le code mis à jour est également mis en surbrillant dans l’onglet Éditeur" lightbox="../media/beginners-html-add4.msft.png":::
             Le code mis à jour est également mis en surbrillant dans l’onglet Éditeur  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Là encore, revenir à **l’onglet en** direct pour vous assurer que le nouveau contenu s’affiche correctement.  
    
    :::image type="complex" source="../media/beginners-html-add5.msft.png" alt-text="La nouvelle liste est visible dans l’onglet en direct" lightbox="../media/beginners-html-add5.msft.png":::
       La nouvelle liste est visible dans l’onglet en direct  
    :::image-end:::  
    
## <a name="experiment-with-content-changes-in-microsoft-edge-devtools"></a>Expérimenter les modifications de contenu dans Microsoft Edge DevTools  

Si vous développiez une grande page avec beaucoup de code HTML, il est assez fastidieux de faire des allers-retours entre l’onglet de l’éditeur et l’onglet en direct des centaines de fois pour afficher vos modifications, en particulier si vous ne savez pas exactement ce qu’il faut placer sur la page.  Microsoft Edge DevTools vous permet d’expérimenter les modifications de contenu sans quitter **l’onglet en direct.**  

### <a name="learn-the-difference-between-html-and-the-dom"></a>Découvrez la différence entre le code HTML et le DOM  

Avant de commencer à modifier votre contenu à partir Microsoft Edge DevTools, vous devez comprendre la différence entre HTML et le DOM.  La meilleure façon d’apprendre est par exemple :  

1.  Accédez à **l’onglet en direct.**  Au bas de votre page, le texte `A new element!?!` s’affiche.  
    
    :::image type="complex" source="../media/beginners-html-dom1.msft.png" alt-text="Au bas de la page, le texte A nouvel élément!?! s’affiche" lightbox="../media/beginners-html-dom1.msft.png":::
       Au bas de la page, le `A new element!?!` texte s’affiche  
    :::image-end:::  
    
1.  Revenir à **l’onglet Éditeur** et essayer de trouver le texte dans `index.html` .  Le texte n’est pas là.  
    
    :::image type="complex" source="../media/beginners-html-dom2.msft.png" alt-text="Texte de texte texte A nouvel élément!?! est introuvable dans index.html" lightbox="../media/beginners-html-dom2.msft.png":::
       Le texte du `A new element!?!` texte de texte est introuvable dans `index.html`  
    :::image-end:::  
    
1.  Revenir à **l’onglet en**direct, pointez dessus, ouvrez le menu `A new element!?!` contextuel \(clic droit\), puis choisissez **Inspecter**.  
    
    :::image type="complex" source="../media/beginners-html-dom3.msft.png" alt-text="Inspection d’un texte" lightbox="../media/beginners-html-dom3.msft.png":::
       Inspection d’un texte  
    :::image-end:::  
    
    DevTools s’ouvre à côté de votre page.  `<div>A new element!?!</div>` est mis en surbrillant en bleu.  Bien que cette structure dans DevTools ressemble à votre code HTML, il s’agit en fait de l’arborescence **DOM**.  
    
    :::image type="complex" source="../media/beginners-html-dom4.msft.png" alt-text="DevTools est ouvert à côté de la page" lightbox="../media/beginners-html-dom4.msft.png":::
       DevTools est ouvert à côté de la page  
    :::image-end:::  
    
Lorsque votre page se charge, le navigateur prend votre code HTML pour créer le *contenu initial* de la page.  Le DOM représente le *contenu* actuel de la page, qui peut changer au fil du temps.  Le contenu exclusif est ajouté à votre page en raison de la balise en `<div>A new element!?!</div>` bas de votre code `<script src="new.js"></script>` HTML.  Cette balise entraîne l’exécuter du code JavaScript.  En savoir plus sur JavaScript dans un didacticiel ultérieur, mais pour l’instant, il s’agit d’un langage de programmation qui peut modifier le contenu de votre page.  Dans ce cas particulier, du code JavaScript `<div>A new element!?!</div>` s’ajoute à votre page.  C’est pourquoi ce texte est visible sur votre page en direct, mais pas dans votre code HTML.  

### <a name="edit-the-dom"></a>Modifier le DOM  

Si vous souhaitez expérimenter rapidement les modifications de contenu sans quitter l’onglet en direct, essayez DevTools.  

1.  Dans DevTools, pointez sur , ouvrez le `Your site!` menu contextuel \(clic droit\), puis choisissez **Modifier au format HTML.**  
    
    :::image type="complex" source="../media/beginners-html-edit1.msft.png" alt-text="Modification du nœud au format HTML" lightbox="../media/beginners-html-edit1.msft.png":::
       Modification du nœud au format HTML  
    :::image-end:::  
    
1.  Remplacez `<p>Your site!</p>` par le code ci-dessous.  
    
    :::row:::
       :::column span="":::
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
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-edit2.msft.png" alt-text="Mise à jour du nœud au format HTML" lightbox="../media/beginners-html-edit2.msft.png":::
             Mise à jour du nœud au format HTML  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
1.  Sélectionnez `Control` + `Enter` \(Windows, Linux\) ou `Command` + `Enter` \(macOS\) pour enregistrer vos modifications, ou choisissez en dehors de la zone.  Vos modifications s’afficheront automatiquement dans l’affichage en direct de votre page.  Le texte `Your site!` a été remplacé par le nouveau contenu.  
    
    :::image type="complex" source="../media/beginners-html-edit3.msft.png" alt-text="Le nouveau contenu s’affiche immédiatement sur la page" lightbox="../media/beginners-html-edit3.msft.png":::
       Le nouveau contenu s’affiche immédiatement sur la page  
    :::image-end:::  
    
Ce flux de travail est uniquement bon pour expérimenter les modifications de contenu.  Si vous actualisez la page ou fermez l’onglet, vos modifications ont disparu définitivement.  Si vous utilisez ce flux de travail et que vous souhaitez enregistrer vos modifications, vous devez copier manuellement ces modifications dans votre code HTML.  Les deux sections suivantes vous montrent d’autres façons de modifier le contenu à partir de l’arborescence DOM.  

## <a name="reorder-nodes"></a>Réordons les nodes  

Vous pouvez également modifier l’ordre des nodes DOM.  Par exemple, sur votre page web, le menu de navigation se trouve près du bas.  Pour le déplacer vers le haut :  

1.  Recherchez `<nav>` le nœud dans l’arborescence **DOM** de DevTools.  
    
    :::image type="complex" source="../media/beginners-html-reorder1.msft.png" alt-text="Le nœud de navigation est mis en surbrillade en bleu dans DevTools" lightbox="../media/beginners-html-reorder1.msft.png":::
       Le nœud de navigation est mis en surbrillade en bleu dans DevTools  
    :::image-end:::  
    
1.  Faites glisser le nœud vers le haut, afin que le nœud soit `<nav>` le premier enfant du `<body>` nœud.  
    
    :::row:::
       :::column span="":::
          &nbsp;  
       :::column-end:::
       :::column span="":::
          Le `<nav>` nœud s’affiche maintenant en haut de votre page.  
       :::column-end:::
    :::row-end:::  
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder2.msft.png" alt-text="Faire glisser le nœud de navigation vers le haut" lightbox="../media/beginners-html-reorder2.msft.png":::
             Faire glisser le nœud de navigation vers le haut  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          :::image type="complex" source="../media/beginners-html-reorder3.msft.png" alt-text="Le nœud de navigation se trouve en haut de la page" lightbox="../media/beginners-html-reorder3.msft.png":::
             Le nœud de navigation se trouve en haut de la page  
          :::image-end:::  
       :::column-end:::
    :::row-end:::  
    
### <a name="delete-a-node"></a>Supprimer un nœud  

Vous pouvez également supprimer des nodes de l’arborescence DOM.  

1.  Dans **l’arborescence DOM,** choisissez `<div>A new element!?!</div>` .  DevTools met en évidence le nœud bleu.  
    
    :::image type="complex" source="../media/beginners-html-delete1.msft.png" alt-text="Choisir le nœud à supprimer" lightbox="../media/beginners-html-delete1.msft.png":::
       Choisir le nœud à supprimer  
    :::image-end:::  
    
1.  Sélectionnez `Delete` la touche de votre clavier.  Le `<div>A new element!?!</div>` nœud est supprimé de votre arborescence DOM.  
    
    :::image type="complex" source="../media/beginners-html-delete2.msft.png" alt-text="Le nœud a été supprimé" lightbox="../media/beginners-html-delete2.msft.png":::
       Le nœud a été supprimé  
    :::image-end:::  
    
## <a name="copy-your-changes"></a>Copier vos modifications  

Vous avez presque terminé.  Vous avez apporté quelques modifications à votre page dans DevTools, mais elles ne sont pas encore enregistrées dans votre code source.  

1.  Actualisez **votre onglet en direct.**  Les modifications que vous avez apportées dans l’arborescence DOM disparaissent.  En particulier, le texte revient en haut de `Your site!` la page et le texte revient en `A new element!?!` bas.  
    
    :::image type="complex" source="../media/beginners-html-copy1.msft.png" alt-text="Les modifications que vous avez apportées ont disparu" lightbox="../media/beginners-html-copy1.msft.png":::
       Les modifications que vous avez apportées ont disparu  
    :::image-end:::  
    
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
    
1.  Revenir à **l’onglet Éditeur** et remplacer le contenu de votre fichier par le code que vous `index.html` viennent de copier.  
    
    :::image type="complex" source="../media/beginners-html-copy2.msft.png" alt-text="Apparence de index.htmfichier l" lightbox="../media/beginners-html-copy2.msft.png":::
       Apparence `index.html` de votre fichier  
    :::image-end:::  
    
## <a name="next-steps"></a>Étapes suivantes  

*   Complétez le didacticiel suivant de cette série, [Prise en main avec CSS,][DevToolsBeginnersCss]pour apprendre à styler votre page et expérimenter les modifications de style dans Microsoft Edge DevTools.  
*   Lisez [l’introduction au DOM][MDNIntroductionDom] pour en savoir plus sur le DOM.  
*   Consultez un cours comme [Introduction au développement Web][CourseraIntroductionToWebDevelopment] pour obtenir une expérience de développement web plus pratique.  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!--- links --->  

[DevToolsBeginnersCss]: ./css.md "DevTools pour les débutants : Prise en main avec CSS | Documents Microsoft"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Microsoft Edge Insider"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Présentation des outils de | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html - alluring-| Glitch"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Mise en place des | HTML MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Présentation de la | DOM MDN"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine a été [trouvée ici](https://developers.google.com/web/tools/chrome-devtools/beginners/html) et a été co-auteure par [Le rédacteur technique Principal \(Interne][KatherineJackson] au rédacteur technique, Chrome DevTools\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors#kayce-basques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors  
