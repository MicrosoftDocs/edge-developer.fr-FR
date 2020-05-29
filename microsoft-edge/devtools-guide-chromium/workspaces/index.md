---
title: Modifier des fichiers avec des espaces de travail
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601851"
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







# Modifier des fichiers avec des espaces de travail   



> [!NOTE]
> L’objectif de ce didacticiel consiste à fournir une pratique pratique pour configurer et utiliser des espaces de travail, afin que vous puissiez utiliser des espaces de travail dans vos propres projets.  Vous pouvez enregistrer les modifications apportées au code source, sur votre ordinateur local, que vous avez effectuées dans DevTools après avoir activé les espaces de travail.  

> [!CAUTION]
> Éléments **requis**: avant de commencer ce didacticiel, vous devez savoir comment:  
> *   [Utiliser HTML, CSS et JavaScript pour créer une page Web][MDNWebGettingStarted]  
> *   [Utiliser DevTools pour apporter des modifications de base à CSS][DevToolsCssIndex]  
> *   [Exécuter un serveur Web HTTP local][MDNSimpleLocalHTTPServer]  

## Présentation   

Les espaces de travail vous permettent d’enregistrer les modifications que vous apportez dans devtools à une copie locale du même fichier sur votre ordinateur.  Par exemple, supposons que:  

*   Vous avez le code source de votre site sur votre ordinateur de bureau.  
*   Vous exécutez un serveur Web local à partir du répertoire de code source, afin que le site soit accessible à l’adresse `localhost:8080` .  
*   Vous avez ouvert `localhost:8080` Microsoft Edge et vous utilisez devtools pour modifier la feuille de style en cascade (CSS) du site.  

Lorsque les espaces de travail sont activés, les modifications que vous apportez dans DevTools sont enregistrées dans le code source sur votre ordinateur de bureau.  

## Limitations   

Si vous utilisez une infrastructure moderne, il est probable que vous transformez votre code source en un format facile à mettre en forme, optimisé pour s’exécuter aussi rapidement que possible.  
Les espaces de travail sont généralement en mesure de mapper le code optimisé dans votre code source d’origine avec l’aide des [cartes sources][TreehouseBlogSourceMaps].  Néanmoins, il existe un grand nombre de variations entre les infrastructures par le biais de cartes sources.  Devtools ne prend pas en charge toutes les variations.  

Les espaces de travail ne fonctionnent pas avec les infrastructures suivantes:  

*   Créer une application réactive  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## Fonctionnalité connexe: substitutions locales   

Les **substitutions locales** sont une autre fonctionnalité devtools similaire aux espaces de travail.  Utilisez les substitutions locales lorsque vous voulez tester des modifications apportées à une page, et que vous avez besoin de voir ces modifications sur les chargements de page, mais vous n’avez pas à vous soucier de mapper vos modifications au code source de la page.  

<!--Todo: add section when content is ready  -->  

## Étape 1: installation   

Suivez ce didacticiel pour obtenir une expérience pratique avec les espaces de travail.  

### Configurer la démonstration   

1.  [Ouvrez la démonstration][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### Figure1  
    > Projet de problème projet ![ d’un problème][ImageGlitchProject]  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  Créer un `app` répertoire sur votre ordinateur de bureau.  Enregistrez des copies des fichiers dans l' `workspaces-demo` Annuaire.  Pour le reste de ce didacticiel, ce répertoire est appelé `~/Desktop/app` .  
1.  Démarrez un serveur Web local dans `~/Desktop/app` .  Vous trouverez ci-dessous un exemple de code permettant de démarrer `SimpleHTTPServer` , mais vous pouvez utiliser le serveur de votre choix.  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  Ouvrez un onglet dans Microsoft Edge et accédez à la version hébergée localement du site.  Vous devriez être en mesure d’y accéder à l’aide d’une URL telle que `localhost:8080` ou `http://0.0.0.0:8080` .  Le [numéro de port][WikiPortURLs] exact est différent.  
    
    > ##### Figure 2  
    > La démonstration  
    > ! [Démonstration] [ImageDemo]  

### Configurer DevTools   

1.  Appuyez sur `Control` + `Shift` + `J` \ (Windows \) ou `Command` + `Option` + `J` \ (MacOS \) pour ouvrir le panneau **console** de devtools.  
    
    > ##### Figure3  
    > Panneau de la **console**  
    > ! [Panneau Console] [ImageConsolePanel]  

1.  Cliquez sur l’onglet **sources** .  
1.  Cliquez sur l’onglet **FileSystem** .  
    
    > ##### Figure 4  
    > Onglet **FileSystem**  
    > ! [L’onglet FileSystem] [ImageFilesystem]  

1.  Cliquez sur **Ajouter un dossier à l’espace de travail**.  
1.  Sélectionnez `~/Desktop/app` .  
1.  Cliquez sur **autoriser** pour accorder à devtools l’autorisation de lecture et d’écriture dans l’annuaire.  
    L’onglet **FileSystem** comporte désormais un point vert en regard de `index.html` , `script.js` et `styles.css` .  Ces points verts indiquent que DevTools a établi une correspondance entre les ressources réseau de la page et les fichiers de `~/Desktop/app` .  
    
    > ##### Figure 5  
    > L’onglet **FileSystem** montre désormais un mappage entre les fichiers locaux et les réseaux  
    > ! [L’onglet FileSystem montre désormais un mappage entre les fichiers locaux et ceux du réseau] [ImageMapping]  

## Étape 2: enregistrer un changement de CSS sur un disque   

1.  Ouvrir `styles.css` .  
    
    > [!NOTE]
    >La `color` propriété d' `h1` éléments est définie sur `fuchsia` .
    
    > ##### Figure 6  
    > Affichage `styles.css` dans un éditeur de texte  
    > ! [Affichage des styles. CSS dans un éditeur de texte] [ImageStylesFuchsia]  


1.  Cliquez sur l’onglet **éléments** .  
1.  Remplacez la valeur de la `color` propriété de l' `<h1>` élément par votre couleur préférée.  
    N’oubliez pas que vous devez cliquer sur l' `<h1>` élément dans l' **arborescence DOM** pour afficher les règles CSS qui lui sont appliquées dans le volet **styles** .  Le point vert en regard `styles.css:1` signifie que toutes les modifications que vous apportez sont mappées `~/Desktop/app/styles.css` .  
    
    > ##### Figure 7  
    > Un indicateur vert dans lequel le fichier est lié  
    > ! [Indicateur vert dans lequel le fichier est lié] [ImageStylesGreen]  

1.  Ouvrez `styles.css` de nouveau dans un éditeur de texte.  La `color` propriété est désormais définie pour votre couleur préférée.  
1.  Rechargez la page.  La couleur de l' `<h1>` élément est toujours définie pour votre couleur préférée.  Cela fonctionne, car lorsque vous avez effectué la modification, DevTools enregistré la modification sur le disque.  Ensuite, lorsque vous rechargez la page, votre serveur local a desservi la copie modifiée du fichier à partir du disque.  

## Étape 3: enregistrer un changement HTML sur le disque   

### Changer le code HTML du panneau éléments  

Vous pouvez modifier le code HTML dans le panneau d’éléments, mais vos modifications apportées à l’arborescence DOM ne sont pas enregistrées sur le disque et ne s’appliquent qu’à la session de navigateur actuelle.  
L’arborescence DOM n’est pas HTML.  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### Changer le code HTML dans le panneau sources   

Si vous voulez enregistrer une modification apportée au code HTML de la page, utilisez le panneau **sources** .  

1.  Cliquez sur l’onglet **sources** .  
1.  Cliquez sur l’onglet **page** .  
1.  Cliquez sur **(index)**.  Le code HTML de la page s’ouvre.  
1.  Remplacer `<h1>Workspaces Demo</h1>` par `<h1>I ❤️  Cake</h1>` .  Voir [figure 8](#figure-8).  
1.  Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.  
1.  Rechargez la page.  Le `<h1>` nouveau texte est encore affiché dans l’élément.  
    
    > ##### Figure8  
    > La ligne 12 a été définie sur `I ❤️  Cake`  
    > ! [Changer le code HTML dans le panneau sources] [ImageSourcesCakeHTML]  

1.  Ouvrir `~/Desktop/app/index.html` .  L' `<h1>` élément contient le nouveau texte.  

## Étape 4: enregistrer un changement JavaScript sur le disque   

Le panneau **sources** est également l’endroit où il est possible de modifier le langage JavaScript.  Néanmoins, il est possible que vous ayez besoin d’accéder à d’autres panneaux, comme le panneau **éléments** ou le panneau de la **console** , tout en apportant des modifications à votre site.  Il est possible de faire en sorte que le panneau **sources** s’ouvre avec d’autres panneaux.  

1.  Cliquez sur l’onglet **éléments** .  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \).  Le **menu de commandes** s’ouvre.  
1.  Tapez `QS` , puis sélectionnez **afficher la source rapide**.  Dans la partie inférieure de la fenêtre DevTools, il existe désormais un onglet **source rapide** .  L’onglet affiche le contenu de `index.html` , qui est le dernier fichier que vous avez modifié dans le panneau **sources** .  L’onglet **source rapide** fournit l’éditeur à partir du panneau **sources** , de sorte que vous pouvez modifier des fichiers en ouvrant d’autres panneaux.  
    
    > ##### Figure9  
    > Ouverture de l’onglet **source rapide** à l’aide du **menu de commandes**  
    > ! [Ouverture de l’onglet source rapide à l’aide du menu de commandes] [ImageCommandMenuQuickSource]  

1.  `Control` + `P` `Command` + `P` Pour ouvrir la boîte de dialogue **ouvrir le fichier** , appuyez sur \ (Windows \) ou \ (MacOS \).  Voir [figure 10](#figure-10).  
1.  Tapez `script` , puis sélectionnez **app/script. js**.  
    
    > ##### Figure10  
    > Ouverture `script.js` à l’aide de la boîte de dialogue **ouvrir le fichier**  
    > ! [Ouverture de script. js à l’aide de la boîte de dialogue Ouvrir le fichier] [ImageOpenFileDialog]  
    
    > [!NOTE]
    > Le `Save Changes To Disk With Workspaces` lien dans la démonstration est appliqué régulièrement.  
    
1.  Ajoutez le code suivant en bas de **script. js** à l’aide de l’onglet **source rapide** .  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer la modification.  
1.  Rechargez la page.  
    
    > [!NOTE]
    > Le lien dans la page est désormais italique.
    
    > ##### Figure11  
    > Le lien dans la page est désormais en italique  
    > ! [Le lien dans la page est désormais italique] [ImageScriptItalic]  

## Étapes suivantes   

Utilisez ce que vous avez appris dans ce didacticiel pour configurer des espaces de travail dans votre projet.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Figure 1: projet de problème avec un nom généré de manière aléatoire"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-demo.msft.png "figure 2: démonstration"  
[ImageConsolePanel]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-console.msft.png "figure 3: le panneau Console"  
[ImageFilesystem]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem.msft.png "figure 4: onglet FileSystem"  
[ImageMapping]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-Folder.msft.png "figure 5: l’onglet FileSystem montre désormais un mappage entre les fichiers locaux et les réseaux"  
[ImageStylesFuchsia]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-FileSystem-CSS.msft.png "figure 6: affichage des styles. CSS dans un éditeur de texte"  
[ImageStylesGreen]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-styles-CSS.msft.png "figure 7: indicateur vert dans lequel le fichier est lié"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-sources-page-H1.msft.png "figure 8: modification du code HTML dans le panneau sources"  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-Show-Quick-source.msft.png "figure 9: ouverture de l’onglet source rapide à l’aide du menu de commande"  
[ImageOpenFileDialog]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Search-script.msft.png "figure 10: ouverture de script. js à l’aide de la boîte de dialogue Ouvrir le fichier"  
[ImageScriptItalic]:/Microsoft-Edge/devtools-Guide-Chromium/Media/Workspaces-Workspaces-Demo-Elements-styles-Quick-Source-script.msft.png "figure 11: le lien dans la page est désormais italique"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Découvrir comment afficher et modifier des feuilles CSS"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Fichiers de démonstration des espaces de travail | Problème"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Contenu-CSS: feuilles de style en cascade | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Commencer à utiliser le Web | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Exécution d’un serveur HTTP local simple | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Introduction aux DOM-Web API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Introduction aux cartes sources | Blog Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Port \ (réseau d’ordinateurs \)-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
