---
description: Découvrez comment enregistrer les modifications apportées dans DevTools sur le disque.
title: Modifier des fichiers avec des espaces de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2021
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement web, outils F12, devtools
ms.openlocfilehash: 17f9ced15dbacd62c9ffe40e4af889925a8155fb
ms.sourcegitcommit: 6cf12643e9959873f8b5d785fd6158eeab74f424
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "11399245"
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

# <a name="edit-files-with-workspaces"></a>Modifier des fichiers avec des espaces de travail  

> [!NOTE]
> L’objectif de ce didacticiel est de fournir des pratiques en configuration et en utilisation des espaces de travail, afin que vous pouvez utiliser les espaces de travail dans vos propres projets.  Vous pouvez enregistrer les modifications apportées au code source, sur votre ordinateur local, que vous avez apportées dans DevTools après avoir activé Les espaces de travail.  

> [!IMPORTANT]
> **Conditions préalables**: avant de commencer ce didacticiel, vous devez savoir comment effectuer les actions suivantes.  
> 
> *   [Utiliser html, CSS et JavaScript pour créer une page web][MDNWebGettingStarted]  
> *   [Utiliser DevTools pour apporter des modifications de base à CSS][DevToolsCssIndex]  
> *   [Exécuter un serveur web HTTP local][MDNSimpleLocalHTTPServer]  

## <a name="overview"></a>Vue d'ensemble  

Les espaces de travail vous permettent d’enregistrer une modification que vous a faites dans Devtools sur une copie locale du même fichier sur votre ordinateur.  Pour ce didacticiel, vous devez avoir les paramètres suivants sur votre ordinateur.  

*   Vous avez le code source de votre site sur votre bureau.  
*   Vous exécutez un serveur web local à partir du répertoire de code source, afin que le site soit accessible à l’adresse `localhost:8080` .  
*   Vous avez ouvert dans Microsoft Edge et vous utilisez DevTools pour modifier le `localhost:8080` CSS du site.  

Une fois les espaces de travail activés, les modifications CSS que vous a faites dans DevTools sont enregistrées dans le code source sur votre bureau.  

## <a name="limitations"></a>Limitations  

Si vous utilisez une infrastructure moderne, il transforme probablement votre code source à partir d’un format facile à gérer dans un format optimisé pour s’exécuter aussi rapidement que possible.  

Les espaces de travail sont généralement en mesure de ma cartographier le code optimisé sur votre code source d’origine à l’aide de [cartes sources.][TreehouseBlogSourceMaps]  Toutefois, il existe de nombreuses variations entre les frameworks sur la façon dont chacune utilise des cartes sources.  Devtools prend simplement en charge toutes les variantes.  

Les espaces de travail ne fonctionnent pas avec l’infrastructure suivante.  

*   Créer une application React  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## <a name="related-feature-local-overrides"></a>Fonctionnalité connexe : substitutions locales  

**Local Overrides** est une autre fonctionnalité DevTools similaire à Workspaces.  Utilisez les substitutions locales lorsque vous souhaitez expérimenter les modifications apportées à une page web et que vous devez afficher les modifications entre les chargements de pages web, mais que vous ne vous souciez pas du mappage de vos modifications au code source de la page web.  

<!--Todo: add section when content is ready  -->  

## <a name="step-1-set-up"></a>Étape 1 : Configurer  

Pour obtenir une expérience pratique avec les espaces de travail, vous pouvez effectuer les actions suivantes.  

### <a name="set-up-the-demo"></a>Configurer la démonstration  

1.  [Ouvrez la démonstration.][GlitchWorkspacesDemo]  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Un projet Glitch" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       Un projet Glitch  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Choose **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  Créez `app` un répertoire sur votre bureau.  Enregistrez des copies des fichiers du `workspaces-demo` répertoire dans `app` le répertoire.  Pour le reste du didacticiel, le répertoire est appelé `~/Desktop/app` .  
1.  Démarrez un serveur web local dans `~/Desktop/app` .  Voici un exemple de code pour le démarrage, mais vous pouvez `SimpleHTTPServer` utiliser n’importe quel serveur de votre préférence.  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  Ouvrez un onglet dans Microsoft Edge et accédez à la version hébergée localement du site.  Vous devriez être en mesure d’y accéder à l’aide d’une URL comme `localhost:8080` ou `http://0.0.0.0:8080` .  Le numéro [de port exact][WikiPortURLs] peut être différent.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Démonstration" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       Démonstration  
    :::image-end:::  
    
### <a name="set-up-devtools"></a>Configurer DevTools  

1.  Sélectionnez `Control` + `Shift` + `J` \(Windows, Linux\) ou `Command` \(macOS\) pour ouvrir le panneau + `Option` + `J` **console** de DevTools.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Panneau console" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       Panneau **console**  
    :::image-end:::  
    
1.  Choisissez **l’outil Sources.**  
1.  Choisissez le **panneau Système de** fichiers.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Panneau Système de fichiers" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       Panneau **Système de** fichiers  
    :::image-end:::  
    
1.  Choisissez **Ajouter un dossier à l’espace de travail.**  
1.  Entrez `~/Desktop/app`.  
1.  Choisissez **Autoriser** pour accorder à DevTools l’autorisation de lire et d’écrire dans le répertoire.  
    Dans le **panneau Système de** fichiers, il y a maintenant un point vert à côté de , et `index.html` `script.js` `styles.css` .  Ces points verts signifient que DevTools a établi un mappage entre les ressources réseau de la page et les fichiers dans `~/Desktop/app` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="Le panneau Système de fichiers affiche désormais un mappage entre les fichiers locaux et les fichiers réseau" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       Le **panneau Système de** fichiers affiche désormais un mappage entre les fichiers locaux et les fichiers réseau  
    :::image-end:::  
    
## <a name="step-2-save-a-css-change-to-disk"></a>Étape 2 : Enregistrer une modification CSS sur le disque  

1.  Ouvrez `styles.css` .  
    
    > [!NOTE]
    > La `color` propriété des éléments est définie sur `h1` `fuchsia` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Afficher styles.css dans un éditeur de texte" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       Afficher `styles.css` dans un éditeur de texte  
    :::image-end:::  
    
1.  Choisissez **l’outil Éléments.**  
1.  Modifiez la valeur de `color` la propriété de `<h1>` l’élément en votre couleur favorite.  
    N’oubliez pas que vous devez choisir l’élément dans l’arborescence DOM pour afficher les règles CSS qui lui sont appliquées dans le `<h1>` **volet Styles.** ****  Le point vert en côté signifie que toute modification que vous `styles.css:1` a faites est mappée sur `~/Desktop/app/styles.css` .  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Indicateur vert qui fait que le fichier est lié" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       Indicateur vert qui fait que le fichier est lié  
    :::image-end:::  
    
1.  Ouvrez `styles.css` à nouveau dans un éditeur de texte.  La `color` propriété est maintenant définie sur votre couleur favorite.  
1.  Actualisez la page.  La couleur de `<h1>` l’élément est toujours définie sur votre couleur favorite.  La modification reste pendant une actualisation, car lorsque vous avez apporté la modification, DevTools a enregistré la modification sur le disque.  Puis, lorsque vous avez actualisé la page, votre serveur local a servi la copie modifiée du fichier à partir du disque.  
    
## <a name="step-3-save-an-html-change-to-disk"></a>Étape 3 : Enregistrer une modification HTML sur le disque  

### <a name="change-html-from-the-elements-panel"></a>Modifier le code HTML à partir du panneau Éléments  

Vous pouvez apporter des modifications au code HTML à partir du panneau d’élément, mais vos modifications apportées à l’arborescence DOM ne sont pas enregistrées sur le disque et n’ont qu’un effet sur la session de navigateur actuelle.  

L’arborescence DOM n’est pas html.  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tool.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** tool  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that are displayed on the **Elements** tool represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the webpage displayed for users may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** tool should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### <a name="change-html-from-the-sources-panel"></a>Modifier le code HTML à partir du panneau Sources  

Si vous souhaitez enregistrer une modification dans le code HTML de la page, faites-le à l’aide du **panneau Sources.**  

1.  Choisissez **l’outil Sources.**  
1.  Choisissez le **panneau Page.**  
1.  Choose **(index)**.  Le code HTML de la page s’ouvre.  
1.  Remplacez `<h1>Workspaces Demo</h1>` par `<h1>I ❤️  Cake</h1>` .  Examinez la figure suivante.  
1.  Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer la modification.  
1.  Actualisez la page.  `<h1>`L’élément affiche toujours le nouveau texte.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Modifier le code HTML à partir du panneau Sources" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       Modifier le code HTML à partir du **panneau Sources**  
    :::image-end:::  
    
1.  Ouvrez `~/Desktop/app/index.html` .  `<h1>`L’élément contient le nouveau texte.  
    
## <a name="step-4-save-a-javascript-change-to-disk"></a>Étape 4 : Enregistrer une modification JavaScript sur le disque  

Le **panneau Sources** est également l’endroit où apporter des modifications à JavaScript.  Mais parfois, vous devez accéder à d’autres panneaux, tels que l’outil **Éléments** ou le panneau **Console,** tout en a apporté des modifications à votre site.  Il existe un moyen d’ouvrir le panneau **Sources** avec d’autres panneaux.  

1.  Choisissez **l’outil Éléments.**  
1.  Sélectionnez `Control` + `Shift` + `P` \(Windows, Linux\) ou `Command` + `Shift` + `P` \(macOS\).  Le **menu Commande** s’ouvre.  
1.  `QS`Tapez, puis choisissez Afficher la source **rapide.**  Au bas de la fenêtre DevTools se trouve désormais un **panneau Source** rapide.  Le panneau affiche le contenu de , qui est le dernier fichier que vous `index.html` avez modifié dans le panneau **Sources.**  Le **panneau Source rapide** vous fournit l’éditeur à partir du panneau **Sources,** afin que vous pouvez modifier des fichiers tout en ayant d’autres panneaux ouverts.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Ouvrir le panneau Source rapide à l’aide du menu Commande" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       Ouvrir le **panneau Source rapide** à l’aide du menu **Commande**  
    :::image-end:::  
    
1.  Sélectionnez `Control` + `P` \(Windows, Linux\) ou `Command` + `P` \(macOS\) **** pour ouvrir la boîte de dialogue Ouvrir un fichier.  Examinez la figure suivante.  
1.  `script`Tapez, puis choisissez **application/script.js**.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Ouvrir script.js à l’aide de la boîte de dialogue Ouvrir un fichier" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       Ouvrir `script.js` à l’aide **de la boîte de dialogue Ouvrir un** fichier  
    :::image-end:::  
    
    > [!NOTE]
    > Le `Save Changes To Disk With Workspaces` lien de la démonstration est régulièrement mis en forme.  
    
1.  Ajoutez le code suivant au bas de la **script.js** à l’aide du **panneau Source** rapide.  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Sélectionnez `Control` + `S` \(Windows, Linux\) ou `Command` + `S` \(macOS\) pour enregistrer la modification.  
1.  Actualisez la page.  
    
    > [!NOTE]
    > Le lien de la page est désormais en italique.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Le lien de la page est désormais en italique" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       Le lien de la page est désormais en italique  
    :::image-end:::  
    
## <a name="next-steps"></a>Étapes suivantes  

Utilisez ce que vous avez appris dans ce didacticiel pour configurer les espaces de travail dans votre propre projet.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  -->  

## <a name="getting-in-touch-with-the-microsoft-edge-devtools-team"></a>Contacter l’équipe DevTools MicrosoftEdge  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Commencer à afficher et modifier les | Documents Microsoft"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Fichiers de démonstration des espaces de travail | Glitch"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Content - CSS: Cascading Style Sheets | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Getting started with the Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Exécution d’un serveur HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Présentation du DOM - Api web | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Présentation des cartes sources | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \(computer networking\) - Wikipedia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution créative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) et est créée par [Kayce Basques][KayceBasques] \(Technical Writer, chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
