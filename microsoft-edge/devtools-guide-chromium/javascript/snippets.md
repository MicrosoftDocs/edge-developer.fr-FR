---
title: Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft Edge, développement Web, outils F12, devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581816"
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





# Exécuter des extraits de code JavaScript sur n’importe quelle page avec Microsoft Edge DevTools   



Si vous vous trouvez vous utilisez le même code dans la [console][DevtoolsConsoleIndex] à plusieurs reprises, envisagez plutôt d’enregistrer le code en tant qu’extrait.  Les extraits sont des scripts que vous créez dans le [panneau **sources** ][DevToolsSourcesPanel].  Ils ont accès au contexte JavaScript de la page et vous pouvez les exécuter sur n’importe quelle page.  Les extraits de vue sont une alternative aux [bookmarklets][WikiBookmarklet].  
Firefox DevTools possède une fonctionnalité semblable à celle des extraits de blocs- [Notes][MDNScratchpad].  

Par exemple, la [**figure 1**](#figure-1) montre la page d’accueil devtools sur la gauche et le code source de l’extrait de code à droite.  

> ##### Figure1  
> Aspect de la page avant d’exécuter l’extrait de page  
> ![Aspect de la page avant d’exécuter l’extrait de page][ImageSnippetSplitScreen]  

L’extrait de code source de la [**figure 1**](#figure-1):  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

La [**figure 2**](#figure-2) montre à quoi ressemble la page après avoir exécuté l’extrait de méthode.  Le **tiroir** de la console s’affiche pour afficher le `Hello, Snippets!` message indiquant que le Snippet enregistre les journaux et le contenu de la page est totalement modifié.  

> ##### Figure 2  
> Aspect de la page après avoir exécuté l’extrait  
> ![Aspect de la page après avoir exécuté l’extrait][ImageSnippetSplitScreenAfter]  

## Ouvrir le volet d’extraits   

Le volet d' **extraits** de liste répertorie vos extraits.  Lorsque vous voulez modifier un extrait de rapport, vous devez l’ouvrir à partir du volet **extraits** .  

> ##### Figure3  
> Volet **snippets**  
> ![Volet Snippets][ImageSnippetsPane]  

### Ouvrir le volet des fragments de fenêtre à l’aide d’une souris   

1.  Cliquez sur l’onglet **sources** pour ouvrir le panneau **sources** .  Le volet **page** s’ouvre généralement par défaut.  

    > ##### Figure 4  
    > Panneau **sources** avec le volet **page** ouvert à gauche  
    > ![Panneau sources avec le volet page ouvert à gauche][ImageSourcesPageEmpty]  

1.  Cliquez sur l’onglet **extraits** de vue pour ouvrir le volet d' **extraits** .  Vous devrez peut-être cliquer sur **autres onglets** pour ![ ][ImageMoreTabsIcon] accéder à l’option **extraits** de vue.  

### Ouvrir le volet d’extraits de fenêtre à l’aide du menu de commandes   

1.  Focalisez votre curseur à l’intérieur du DevTools.  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Commencez `Snippets` à taper, sélectionnez **afficher les extraits**de texte, puis appuyez sur `Enter` pour exécuter la commande.  

    > ##### Figure 5  
    > Commande **afficher les extraits**  
    > ![Commande Afficher les extraits][ImageShowSnippetsSearch]  

## Créer des extraits de   

### Créer un snippet via le volet sources   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez sur **nouvel extrait**.  
1.  Entrez le nom de votre snippet, puis appuyez sur `Enter` Enregistrer.  

    > ##### Figure 6  
    > Attribution d’un nom à un snippet  
    > ![Attribution d’un nom à un snippet][ImageSnippetName]  

### Créer un snippet via le menu de commandes   

1.  Focalisez votre curseur à l’intérieur du DevTools.  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Commencez `Snippet` à taper, sélectionnez **créer un nouveau Snippet**, puis appuyez sur `Enter` pour exécuter la commande.  

    > ##### Figure 7  
    > Commande de création d’un nouveau Snippet  
    > ![Commande de création d’un nouveau Snippet][ImageCreateSnippetSearch]  

Voir [Renommer des extraits de nom](#rename-snippets) si vous souhaitez attribuer un nom personnalisé à votre nouveau snippet.  

## Modifier des extraits de ce profil   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Dans le volet d' **extraits** de code, cliquez sur le nom de l’extrait que vous souhaitez modifier pour l’ouvrir dans l' **éditeur de code**.  

    > ##### Figure8  
    > Éditeur de code  
    > ![Éditeur de code][ImageSnippetEditor]  

1.  Utilisez l' **éditeur de code** pour ajouter du JavaScript à votre snippet.  
1.  Lorsqu’un astérisque apparaît en regard du nom de votre snippet, cela signifie que vous avez du code non enregistré. Appuyez sur `Control` + `S` \ (Windows \) ou `Command` + `S` \ (MacOS \) pour enregistrer.  

    > ##### Figure9  
    > Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré.  
    > ![Un astérisque en regard du nom de l’extrait de code, qui indique du code non enregistré.][ImageUnsavedSnippet]  

## Exécuter des Snippets   

### Exécuter un snippet à partir du panneau sources   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez sur le nom de l’extrait que vous souhaitez exécuter.  L’extrait de code s’ouvre dans l' **éditeur de code**.  
1.  Cliquez sur **exécuter** l’extrait ![ ][ImageRunSnippetIcon] de snippet, ou appuyez sur `Control` + `Enter` \ (Windows \) ou `Command` + `Enter` \ (MacOS \).  

### Exécuter un extrait de commande avec le menu de commandes   

1.  Focalisez votre curseur à l’intérieur du DevTools.  
1.  Appuyez sur `Control` + `Shift` + `P` \ (Windows \) ou `Command` + `Shift` + `P` \ (MacOS \) pour ouvrir le menu de commandes.  
1.  Supprimez le `>` caractère et tapez le `!` caractère suivi du nom de l’extrait que vous voulez exécuter.  

    > ##### Figure10  
    > Exécution d’un snippet à partir du menu de commandes  
    > ![Exécution d’un snippet à partir du menu de commandes][ImageRunSnippetCommand]  

1.  Appuyez `Enter` pour exécuter l’extrait de.  

## Renommer des extraits de nom   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **Renommer**.  

## Supprimer des extraits de   

1.  [Ouvrez le volet d' **extraits** ](#open-the-snippets-pane).  
1.  Cliquez avec le bouton droit sur le nom de l’extrait, puis sélectionnez **supprimer**.  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "Figure 1: apparence de la page avant de l’exécuter"  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Figure 2: aspect de la page après avoir exécuté l’extrait"  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Figure 3: volet Snippets"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Figure 4: volet de sources avec le volet de pages ouvert à gauche"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Figure 5: commande Afficher les extraits"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Figure 6: nommer un snippet"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Figure 7: commande de création d’un nouveau Snippet"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Figure 8: éditeur de code"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Figure 9: un astérisque en regard du nom de l’extrait de code, qui indique le code non enregistré."  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Figure 10: exécution d’un snippet à partir du menu de commandes"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Présentation de la console"  
[DevToolsSourcesPanel]: ../sources.md "Présentation du panneau sources"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Bloc-notes | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Bookmarklet-Wikipédia"  

> [!NOTE]
> Certaines parties de cette page sont des modifications fondées sur le travail créé et [partagé par Google][GoogleSitePolicies] et utilisées conformément aux conditions décrites dans la [licence internationale 4,0 d’attribution Creative][CCA4IL].  
> La page d’origine est disponible [ici](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) et est créée par [Kayce basques][KayceBasques] \ (Technical Writer, chrome devtools \ & phare \).  

[![Licence Creative d’Creative][CCby4Image]][CCA4IL]  
Ce travail est concédé sous une [Licence internationale Creative Commons Attribution4.0][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
